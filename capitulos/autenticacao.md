Autenticação
============

Nós usamos o autenticação [OAuth 2.0](https://oauth.net/2/) em conjunto com [OpenID Connect](https://openid.net/developers/how-connect-works/).

Recomendamos fortemente que aplicações que integrem conosco façam uso de bibliotecas existentes para integração OAuth 2.0 e OpenID Connect, já que o protocolo tem diversos detalhes e nuâncias que podem abrir brechas de segurança para sua aplicação e usuários em casos de descuido.

Registre sua aplicação
----------------------

O primeiro passo é cadastrar sua aplicação conosco. Para isso, envie um email para odonline@olddragon.com.br informando:

- O nome da sua aplicação
- Descrição do que sua aplicação faz ou irá fazer
- Uma URL de resposta para sua aplicação (exemplo: `https://example.org/callback`)

Acesso de Usuários
------------------

Você precisa ter uma conta em [olddragon.com.br](https://olddragon.com.br) usando o mesmo endereço de email remetente, assim iremos vincular à sua conta. Em breve, você poderá criar e gerenciar suas aplicações no próprio site, sem precisar entrar em contato conosco por email.

A autenticação de usuários é importante para que os mesmos acessem conteúdos digitais exclusivos de suas contas, como monstros, equipamentos, magias e livros digitais que adquiriram em suas contas. Por exemplo, o monstro [Normósia](https://olddragon.com.br/monstros/normosia) é exclusivo do livro [ARKHI](https://olddragon.com.br/livros/arkhi), e somente usuários que compraram este livro digital tem acesso a este monstro no Old Dragon Online. A autenticação também é primordial para, por exemplo, listar campanhas e personagens, já que estes somente são possíveis de listar se soubermos qual usuário que está tentando listar suas campanhas e personagens.

Configurações OAuth e OpenID Connect
------------------------------------

A URL [https://olddragon.com.br/.well-known/openid-configuration](https://olddragon.com.br/.well-known/openid-configuration) pode ser usada para auto-configurar seu cliente OpenID Connect.

É necessário utilizar a extensão [PKCE](https://oauth.net/2/pkce/).

Recomendamos solicitar os escopos (`scopes`) `openid email content.read offline_access`, que irão possibilitar descobrir o email do usuário, acessar o conteúdo (como personagens), e ter um `refresh_token` para atualizar o acesso.

O `code` é válido por 5 minutos. O `access_token` é válido por 1 hora. O `refresh_token` é válido por 1 ano. Se você receber um erro 401, é porque seu `access_token` expirou e deverá utilizar um _refresh flow grant_ para conseguir um novo.

Para ter acesso ao `refresh_token`, solicite `prompt=consent` na fase de requisição de autenticação (_auth request_), em conjunto com um escopo (`scope`) `offline_access` (conforme já mencionado acima).

Códigos de exemplo
------------------

### PHP

`index.php`:

```php
<?php
require 'vendor/autoload.php';

session_start();

// Geração de PKCE manual
function generateCodeVerifier($length = 64) {
    $randomBytes = random_bytes($length);
    return rtrim(strtr(base64_encode($randomBytes), '+/', '-_'), '=');
}
$codeVerifier = generateCodeVerifier();

function base64_urlencode($input) {
    return rtrim(strtr(base64_encode($input), '+/', '-_'), '=');
}

function generateCodeChallenge($codeVerifier) {
    return base64_urlencode(hash('sha256', $codeVerifier, true));
}
$codeChallenge = generateCodeChallenge($codeVerifier);

$_SESSION['codeVerifier'] = $codeVerifier; // Armazenar para mais tarde

$provider = new League\OAuth2\Client\Provider\GenericProvider([
    'clientId'                => getenv('CLIENT_ID'),
    'clientSecret'            => getenv('CLIENT_SECRET'),
    'redirectUri'             => getenv('CALLBACK_URL'), // ex: "https://example.org/callback.php"
    'urlAuthorize'            => 'https://olddragon.com.br/authorize',
    'urlAccessToken'          => 'https://olddragon.com.br/token',
    'urlResourceOwnerDetails' => 'https://olddragon.com.br/'
]);

$authUrl = $provider->getAuthorizationUrl([
    'scope'  => 'openid email content.read offline_access',
    'prompt' => 'consent', // for getting a refresh token
    'code_challenge' => $codeChallenge,
    'code_challenge_method' => 'S256'
]);

echo "<html><head><title>OldDragon OAuth2 PHP</title><link rel='stylesheet' href='https://unpkg.com/simpledotcss@2.1.0/simple.min.css'></head><body>";
echo "<h2>Integração com Old Dragon</h2>";
echo "<center><a href='$authUrl'>Login com OldDragon</a>";
```

`callback.php`:

```php
<?php
require 'vendor/autoload.php';

session_start();

$provider = new League\OAuth2\Client\Provider\GenericProvider([
    'clientId'                => getenv('CLIENT_ID'),
    'clientSecret'            => getenv('CLIENT_SECRET'),
    'redirectUri'             => getenv('CALLBACK_URL'), // ex: "https://example.org/callback.php"
    'urlAuthorize'            => 'https://olddragon.com.br/authorize',
    'urlAccessToken'          => 'https://olddragon.com.br/token',
    'urlResourceOwnerDetails' => 'https://olddragon.com.br/'
]);

if (!isset($_GET['code'])) {
    exit('Invalid request');
}

$accessToken = $provider->getAccessToken('authorization_code', [
    'code' => $_GET['code'],
    'code_verifier' => $_SESSION['codeVerifier'] // Use the stored code verifier
]);

$_SESSION['accessToken'] = $accessToken->getToken();
$_SESSION['codeVerifier'] = null;

if (isset($accessToken->getValues()['id_token'])) {
    $_SESSION['idToken'] = $accessToken->getValues()['id_token'];
}

if ($accessToken->getRefreshToken()) {
    $_SESSION['refreshToken'] = $accessToken->getRefreshToken();
}

// Use Guzzle to make an authenticated API request
$client = new GuzzleHttp\Client();
$response = $client->request('GET', 'https://olddragon.com.br/campanhas.json', [
    'headers' => [
        'Authorization' => 'Bearer ' . $_SESSION['accessToken']
    ]
]);
$body = $response->getBody();

echo "<html><head><title>OldDragon OAuth2 PHP</title><link rel='stylesheet' href='https://unpkg.com/simpledotcss@2.1.0/simple.min.css'></head><body>";
echo "<h2>Access Token</h2><pre>" . $_SESSION['accessToken'] . "</pre>";
echo "<h2>ID Token</h2><pre>" . $_SESSION['idToken'] . "</pre>";
echo "<h2>Refresh Token</h2><pre>" . $_SESSION['refreshToken'] . "</pre>";
echo "<h2>/campanhas.json</h2><pre>" . $body . "</pre>";
```

### JavaScript (Node.js + Express.js)

`server.js`:

```javascript
const express = require("express");
const passport = require("passport");
const OAuth2Strategy = require("passport-oauth2");
const session = require("express-session");
const axios = require("axios");

passport.use(
  "oauth2",
  new OAuth2Strategy(
    {
      authorizationURL: "https://olddragon.com.br/authorize",
      tokenURL: "https://olddragon.com.br/token",
      clientID: process.env.CLIENT_ID,
      clientSecret: process.env.CLIENT_SECRET,
      callbackURL: `https://${process.env.PROJECT_DOMAIN}.glitch.me/callback`,
      scope: "openid email content.read offline_access",
      prompt: "consent",
      scopeSeparator: " ",
    },
    (accessToken, refreshToken, profile, cb) => {
      profile.accessToken = accessToken;
      profile.refreshToken = refreshToken;
      return cb(null, profile);
    }
  )
);

passport.serializeUser((user, done) => done(null, user));
passport.deserializeUser((obj, done) => done(null, obj));

const app = express();

app.use(
  session({
    secret: process.env.SESSION_SECRET,
    resave: false,
    saveUninitialized: true,
  })
);

app.use(passport.initialize());
app.use(passport.session());

app.get("/", (req, res) => {
  res.send(
    `<html><head><title>OldDragon OAuth2 Node.js</title><link rel='stylesheet' href='https://unpkg.com/simpledotcss@2.1.0/simple.min.css'></head><body>` +
      `<h2>Integração com Old Dragon</h2>` +
      `<a href="/login">Login com OldDragon</a>`
  );
});

app.get("/login", passport.authenticate("oauth2"));

app.get("/callback", (req, res, next) => {
  passport.authenticate("oauth2", (err, user, info) => {
    if (err) {
      console.error("Authentication Error:", err);
      return res.send("Authentication Error: " + err.message);
    }
    if (!user) {
      console.error("Authentication Failed:", info);
      return res.redirect("/");
    }
    req.logIn(user, async (err) => {
      if (err) {
        console.error("Login Error:", err);
        return next(err);
      }

      // Agora vamos usar os tokens
      try {
        const response = await axios.get(
          "https://olddragon.com.br/campanhas.json",
          {
            headers: {
              Authorization: `Bearer ${req.user.accessToken}`,
            },
          }
        );
        res.send(
          `<html><head><title>OldDragon OAuth2 Node.js</title><link rel='stylesheet' href='https://unpkg.com/simpledotcss@2.1.0/simple.min.css'></head><body>` +
            `<h2>Access Token</h2><pre>${req.user.accessToken}</pre>"` +
            `<h2>/campanhas.json</h2><pre>${JSON.stringify(
              response.data
            )}</pre>`
        );
      } catch (error) {
        console.error("Error fetching campanhas:", error);
        if (error.response && error.response.status === 401) {
          // Handle token expiration, e.g., try to refresh the token
          // If refresh token is also expired, redirect to login
        }
        res.status(500).send("Error fetching campanhas");
      }
    });
  })(req, res, next);
});

app.listen(3000, () => {
  console.log("Server is running...");
});
```
