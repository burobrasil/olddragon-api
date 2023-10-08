Old Dragon Online API
=====================

Bem vindo à API do Old Dragon Online! Se você quer integrar sua aplicação com o OldDragon.com.br ou criar uma nova aplicação utilizando dados do ODO, você está no lugar certo. Obrigado por fazer parte da incrível comunidade Old Dragon!

Esta API ainda está em constante desenvolvimento. Se você achar qualquer problema ou tiver dificuldade com algo que deva ser um erro, abra uma "Issue" neste repositório, ou envie um email para odonline@olddragon.com.br.

Chamadas para API
-----------------

Todas as URLs começam com **`https://olddragon.com.br/`**. URLs devem usar HTTPS, HTTP não é suportado.

Para fazer uma chamada para carregar todos os monstros disponíveis para usuários não loggados, basta fazer uma chamada para `https://olddragon.com.br/monstros.json`. Usando cURL, é assim:

``` shell
curl -A 'MinhaAplicacao (seunome@example.com)' https://olddragon.com.br/monstros.json
```

Autenticação
------------

Ainda estamos desenvolvendo um sistema de autenticação para APIs. Portanto, todas as chamadas feitas via API por enquato terão acesso como um usuário visitante, não-logado. Logo, você terá acesso apenas a monstros gratuitos e públicos.

Identifique sua aplicação
-------------------------

Você deve incluir o cabeçalho HTTP `User-Agent` com ambos os dados:

* O nome da sua aplicação
* Um endereço de email para contactar o desenvolvedor

Nós usamos estas informações para poder entrar em contato com você caso haja algum problema, ou para reconhecer o seu trabalho. Exemplo: `User-Agent: O Maravilhoso Gerador de Personagens (magodesenvolvedor@example.com)`

Se você não incluir um cabeçalho `User-Agent`, você poderá receber o erro `400 Bad Request`.

Apenas JSON
-----------

Nós apenas aceitamos e usamos JSON em todas as chamadas da API. Você deve incluir o cabeçalho HTTP `Content-Type` como `Content-Type: application/json; charset=utf-8` em chamadas POST ou PUT. Todas as URLs da API tem final `.json` para indicar que retornam JSON. Você também pode optar por enviar o cabeçalho `Accept: application/json`.

A API tem inspiração no protocolo JSON:API v1.1, embora não implementemos o mesmo, em prol de simplicidade e minimalismo.

Paginação
---------

Todas as coleções de resultado tem seu resultado paginado.

Nós retornamos o JSON com a seguinte estrutura:

```json
{
  "data": [
    // objetos retornados
  ],
  "links": {
    "first": "/coisas.json?page=1",
    "self": "/coisas.json?page=10",
    "next": "/coisas.json?page=11",
    "last": "/coisas.json?page=20"
  },
  "meta": {
    "pages": 20,
    "count": 500
  }
}
```

No resultado, dentro de `links`, é possível identificar a primeira página (`first`), a própria página atual (`self`), a próxima página (`next`), e a última página da coleção (`last`). Dentro de `meta`, é possível identificar o número total de páginas (`pages`) e o número total de itens na coleção (`count`).

Todos os dados e paginação são sempre referentes a atual filtragem.

Cache HTTP
----------

Você deve usar os cabeçalhos de atualidade HTTP para acelerar a sua aplicação e aliviar a carga nos nossos servidores. A maioria das respostas da API incluirá um cabeçalho `ETag` ou `Last-Modified`. Quando você requisitar um recurso pela primeira vez, armazene esses valores. Em solicitações subsequentes, submeta-os de volta para nós como `If-None-Match` e `If-Modified-Since`, respectivamente. Se o recurso não tiver sido alterado desde a sua última solicitação, você receberá uma resposta `304 Not Modified` sem corpo, poupando-lhe tempo e largura de banda ao enviar algo que você já possui.

Tratando Erros
--------------

Clientes da API devem esperar e tratar de maneira elegante erros temporários do servidor e limites de uso. Recomendamos incorporar tentativas elegantes de 5xx e 429 desde o início na sua integração, para que os erros sejam tratados automaticamente.

### Limitação de uso (429 Too Many Requests)

Retornamos uma resposta [429 Too Many Requests](http://tools.ietf.org/html/draft-nottingham-http-new-status-02#section-4) quando você excedeu um limite de uso. Consulte o cabeçalho de resposta `Retry-After` para determinar quanto tempo esperar (em segundos) antes de tentar a solicitação novamente.

Planeje com antecedência para tratar com elegância os modos de falha que a contrapressão da API exercerá sobre sua integração. Vários limites de taxa estão em vigor, por exemplo, para solicitações GET vs POST e limites por segundo/hora/dia, e eles são ajustados dinamicamente, então respondê-los dinamicamente é essencial, particularmente em níveis de tráfego elevados.

Para ter uma noção de escala, o primeiro limite de taxa que você comumente encontrará é atualmente de 50 solicitações por período de 10 segundos por endereço IP.

### Erros no Servidor ([5xx server errors](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#5xx_Server_errors))

Se o Old Dragon Online estiver com problemas, você receberá uma resposta com um código de status 5xx indicando um erro no servidor. 500 (Internal Server Error), 502 (Bad Gateway), 503 (Service Unavailable), e 504 (Gateway Timeout) podem ser tentados novamente com [redução exponencial](https://en.wikipedia.org/wiki/Exponential_backoff).

### Página não encontrada (404 Not Found)

Solicitações de API podem receber 404 devido a conteúdo excluído, uma conta inativa, permissões de usuário ausentes, etc. Detecte estas condições para dar aos seus usuários uma explicação clara sobre por que eles não podem se conectar ao Basecamp. Não tente novamente automaticamente essas solicitações.

Conteúdo em texto rico (rich text)
----------------------------------

Muitos recursos, incluindo mensagens, documentos e comentários, representam seu conteúdo como texto rico (rich text) em HTML e Markdown. O conteúdo em texto rico pode conter listas, citações em bloco, formatação simples e anexos inline, como menções, imagens e arquivos.

Endpoints da API
----------------
<!-- START API ENDPOINTS -->
- [Campanhas](https://github.com/burobrasil/olddragon-api/blob/master/sections/campanhas.md#campanhas)
- [Equipamentos](https://github.com/burobrasil/olddragon-api/blob/master/sections/equipamentos.md#equipamentos)
- [Magias](https://github.com/burobrasil/olddragon-api/blob/master/sections/magias.md#magias)
- [Monstros](https://github.com/burobrasil/olddragon-api/blob/master/sections/monstros.md#monstros)
- [Personagens](https://github.com/burobrasil/olddragon-api/blob/master/sections/personagens.md#personagens)
<!-- END API ENDPOINTS -->

Suporte
------------

Se você tem alguma dúvida sobre a API, envie um email para odonline@olddragon.com.br.

Licença
-------

Toda a documentação de API neste repositório de código é licenciado sob a [Creative Commons (CC BY-SA 4.0)](http://creativecommons.org/licenses/by-sa/4.0/). Compartilhe, remixe, e distribua como desejar.