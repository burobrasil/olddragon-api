Raças
========

Endpoints:

- [Listar raças](#listar-racas)
- [Obter raça específica](#obter-raca-específica)
- [Listar minhas raças](#listar-minhas-racas)
- [Listar raças comunitárias](#listar-racas-comunitarias)

Campos Obsoletos
----------------

> **Aviso de Depreciação**: Os seguintes campos serão removidos no futuro próximo. Por favor, migre para os novos campos de objeto aninhado.

| Campo obsoleto | Substituição |
|----------------|--------------|
| `fontes[].digital_item_url` | Use o objeto `digital_item` com `id`, `name`, `url` |

Listar raças
--------------

* `GET /racas.json` retorna todos as raças.

_Parâmetros opcionais de URL_:

* `ids[]` - Lista de IDs de raças. Exemplo: `ids[]=anao&ids[]=elfo`.

###### Exemplo de resposta JSON
<!-- START character_races_index.json -->
```json
[
  {
    "id": "anao",
    "type": "CharacterRace",
    "name": "Anão",
    "flavor": "Orgulhosos Habitantes dos Salões sob a Montanha.",
    "access": "complete",
    "description": "Honrados, perfeccionistas e reservados, os anões são conhecidos não só pela sua peculiar aparência, mas sobretudo pela forma como se relacionam com as outras raças e com a sua própria história.\n\nDe aparência robustas e rústica, corpulentos e com uma inconfundível grande barba, anões vivem junto dos seus clãs com as montanhas sobre suas cabeças, minerando, forjando, reverenciando seus antepassados e comemorando com cerveja e suas famosas bebidas fortes.\n\nOs Salões sob a Montanha, onde vivem isolados, são locais sagrados e reverenciados por eles. Lá, adotam um estilo de vida comedido, voltado ao trabalho, entrecortando o silêncio apenas com suas canções de trabalho e suas frequentes comemorações.\n\nSão guiados pela honra e pelo sentimento de gratidão por todos aqueles que ajudaram a construir o orgulho que sentem das suas origens, quando lideraram a raça anã em feitos de superação, conquista e guerra contra seus inimigos.\n\nComo bons tradicionalistas, colocam sua família, seu clã e principalmente sua raça acima de todas as coisas, inclusive de si mesmos e de suas vontades pessoais.\n\nBuscam honrar suas origens tentando demonstrar que são dignos de fazer parte do que eles costumam chamar: povo perfeito.\n\nExímios forjadores, trabalham o metal à sua vontade. Não há nada que eles não possam forjar, e não há nenhum objeto de metal que não fique perfeito após um anão aplicar suas técnicas ancestrais de metalurgia.\n\nCom pensamento lógico acurado, se destacam na engenharia, nas construções, nos trabalhos pesados, mas, ao mesmo tempo, demonstram pouca aptidão às artes arcanas.\n\nFora de suas terras, se mostram orgulhosos e defensores de suas origens, fazendo questão de sempre comparar tudo à volta com a versão melhorada a qual os anões são capazes de criar.",
    "personality": "Orgulho, tradição e obsessão são três importantes palavras para descrever a personalidade anã.\n\nOrgulhosos de tudo relativo ao seu povo, estão a todo tempo lembrando a todos da importância, da imponência, da qualidade, da grandiosidade do seu povo, das canções que glorificam as vitórias sobre seus inimigos.\n\nUm anão é quase um escravo dos feitos dos seus antepassados. Um herói anão é, antes de tudo, uma régua de perfeição. Um grau a admirar, perseguir e atingir.\n\nTradição, para eles, não é uma mera forma de passar aos mais novos os costumes de seu povo, e sim um estilo de vida e um código de honra. Uma espécie de linha guia para basear suas ações e seu pensamento.\n\nO anão é um ser obcecado. Pela defesa dos seus ideais, pelo seu povo, pela perfeição do seu trabalho.\n\nSeja a excelência em batalha, o minucioso trabalho de forja de armas e armaduras, a fermentação precisa da cerveja, a composição da canção que zomba dos orcs, o ideal de vida do anão está centrado na perfeição num nível próximo da idolatria espiritual.",
    "adventure": "Partir para as aventuras é mais do que uma opção para alguns anões, sendo, em alguns casos, uma forma de reverenciar as tradições do seu povo.\n\nCom uma memória repleta de feitos épicos e exemplos a admirar e a seguir, provar-se capaz jogando-se no mundo é, sem dúvida, o mais importante dos motivadores para um anão aventurar-se.\n\nO anão quer provar sua capacidade, sua habilidade, resiliência e ser digno de portar o nome de seu clã.\n\nAnões aventureiros são guiados pelo exemplo e pelo orgulho dos feitos os quais podem realizar e que deixarão para as futuras gerações.",
    "mv": 6,
    "mve": null,
    "mvn": null,
    "mvv": null,
    "infravision": 18,
    "alignment_tendency": "ordeiro",
    "picture": null,
    "thumb_picture": null,
    "abilities": [
      {
        "name": "Mineradores",
        "description": "Por milênios, anões aprendem desde cedo a avaliar passagens e condições de muralhas e portais.\n\nPor isso são capazes de detectar, mesmo que não estejam analisando ativamente, com um resultado de 1 em 1d6, anomalias em pedras, como armadilhas em cavernas ou fossos escondidos, ou com um resultado de 1-2 em 1d6 caso estejam efetivamente procurando.\n",
        "mechanic_type": "none",
        "mechanic_config": {}
      },
      {
        "name": "Vigoroso",
        "description": "Os anões são muito resistentes aos efeitos que afetem seu corpo, recebendo um bônus de +1 em qualquer teste de JPC.\n",
        "mechanic_type": "bonus_jp",
        "mechanic_config": {
          "options": [
            "jpc"
          ]
        }
      },
      {
        "name": "Armas grandes",
        "description": "São restritas para anões que podem usar apenas armas médias e pequenas. Armas grandes forjadas como um item racial anão são consideradas armas médias para um anão.\n",
        "mechanic_type": "none",
        "mechanic_config": {}
      },
      {
        "name": "Inimigos",
        "description": "Anões são inimigos naturais e disputam território com orcs, ogros e hobgoblins e, por isso, os ataques dos anões contra essas criaturas são considerados ataques fáceis.\n",
        "mechanic_type": "none",
        "mechanic_config": {}
      }
    ],
    "fontes": [
      {
        "page": 22,
        "compact": false,
        "digital_item": {
          "id": "lb1",
          "name": "Livro I: Regras Básicas",
          "url": "https://olddragon.com.br/livros/lb1.json"
        },
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      },
      {
        "page": null,
        "compact": true,
        "digital_item": {
          "id": "srd",
          "name": "SRD: Documento de Referência",
          "url": "https://olddragon.com.br/livros/srd.json"
        },
        "digital_item_url": "https://olddragon.com.br/livros/srd.json"
      }
    ],
    "url": "https://olddragon.com.br/racas/anao.json"
  },
  {
    "id": "elfo",
    "type": "CharacterRace",
    "name": "Elfo",
    "flavor": "Misteriosos, Longevos e Graciosos habitantes das Florestas.",
    "access": "complete",
    "description": "Os elfos são das mais longevas raças encontradas nos mundos de fantasia e a sua relação com o tempo doutrina boa parte das suas características, personalidade e a forma como as outras raças os enxergam e se relacionam com eles.\n\nFisicamente são esguios e até um pouco franzinos se comparados a um humano, além de ligeiramente mais baixos. Seus cabelos, compridos para machos e fêmeas, estão sempre penteados, adornados com acessórios e podem ser encontrados em praticamente todas as cores.\n\nA característica física mais marcante de um elfo está nas suas orelhas – pontudas e longas –, muito embora o traço dos seus olhos – amendoados, delicados e levemente alongados – seja uma característica igualmente marcante.\n\nA relação do elfo com o tempo dita sua forma de pensar e agir. Como frequentemente atingem 1.000 anos de vida, elfos se sentem compelidos a ocuparem suas vidas com o que mais valorizam como a dança, a música, a esgrima, o arqueirismo e a magia arcana.\n\nIsso pode fazer as pessoas acreditarem que Elfos são distantes ou, de certa forma, um pouco fúteis. Um erro comum cometido pelos observadores menos atentos.\n\nOutra característica dos elfos, sobretudo os que estão fora da sua terra, é a distância, dando-lhes uma certa característica de frieza e até prepotência. Por se considerarem estranhos fora de suas fronteiras, possuem dificuldade de se envolver nos problemas das outras raças, refletindo na dificuldade de criar laços de amizade.\n\nNo entanto, quando um elfo é conquistado como amigo, a amizade se mostrará duradoura. A amizade de um elfo dura mais do que muitas vidas, costumam dizer os humanos os quais puderam provar desse relacionamento. Vivendo tantos séculos, esta é uma verdade incontestável.",
    "personality": "Viver tanto tempo molda a personalidade de um elfo. O ritmo do tempo é excepcional para um elfo. As mudanças ocorrem tão depressa que se tornam complicadas de seguir, então, para que se importar? Melhor é focar na qualidade e não na quantidade. Se 100 espadas medianas podem ser confeccionadas, um elfo prefere gastar o mesmo tempo numa única peça exemplar em qualidade e perfeição.\n\nCom tanto tempo disponível para aprender tantas coisas, desperdiçar tempo seria uma opção bem óbvia, mas aí se esconde uma grandeza da sua raça. Ao contrário do que possa parecer, elfos gostam de coisas bem-feitas e duradouras, assim como eles. Serviço bem-feito é sempre aquele com a maior duração.\n\nEssa relação entre qualidade, tempo e perfeição molda todo o pensamento élfico e a construção da sua personalidade.",
    "adventure": "Apesar de bem mais raros que os humanos, elfos não são aventureiros improváveis. A fome por conhecimento, desejo por viajar, a vontade de provar-se para os seus como um elfo exemplar e, principalmente, o tempo disponível, são as principais forças a empurrar um elfo para a vida aventureira.\n\nAs coisas mudam tão rapidamente que acompanhar as mudanças, ou mesmo fazer parte destas mudanças, pode ser uma interessante força motriz para eles.\n\nEles querem acompanhar o que acontece, se aperfeiçoarem e se provarem como capazes.\n\nElfos são aventureiros observadores que querem entender o mundo onde vivem.",
    "mv": 9,
    "mve": null,
    "mvn": null,
    "mvv": null,
    "infravision": 18,
    "alignment_tendency": "neutro",
    "picture": null,
    "thumb_picture": null,
    "abilities": [
      {
        "name": "Percepção Natural",
        "description": "A forma como as casas élficas são construídas, respeitando a forma natural das árvores e abrigos, dá aos elfos uma percepção especial no que diz respeito a portas e passagens não convencionais e até mesmo secretas.\n\nAo passarem a até 6 metros de uma porta secreta, mesmo que não a estejam procurando, os elfos podem detectá-la com um resultado 1 em 1d6, ou com um resultado de 1-2 em 1d6 caso estejam efetivamente procurando pela porta secreta.\n",
        "mechanic_type": "none",
        "mechanic_config": {}
      },
      {
        "name": "Graciosos",
        "description": "Os elfos controlam com precisão seus movimentos no espaço ao redor do seu corpo, recebendo um bônus de +1 em qualquer teste de JPD.\n",
        "mechanic_type": "bonus_jp",
        "mechanic_config": {
          "options": [
            "jpd"
          ]
        }
      },
      {
        "name": "Arma Racial",
        "description": "Os elfos possuem familiaridade com o arqueirismo, o qual consideram uma arte marcial, recebendo um bônus de +1 nos danos causados em seus ataques à distância com os arcos.\n",
        "mechanic_type": "bonus_damage",
        "mechanic_config": {
          "value": 1,
          "condition": "arrow"
        }
      },
      {
        "name": "Imunidades",
        "description": "Os elfos são imunes a efeitos ou magias que envolvam sono e também contra a paralisação causada por um Ghoul.\n",
        "mechanic_type": "none",
        "mechanic_config": {}
      }
    ],
    "fontes": [
      {
        "page": 20,
        "compact": false,
        "digital_item": {
          "id": "lb1",
          "name": "Livro I: Regras Básicas",
          "url": "https://olddragon.com.br/livros/lb1.json"
        },
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      },
      {
        "page": null,
        "compact": true,
        "digital_item": {
          "id": "srd",
          "name": "SRD: Documento de Referência",
          "url": "https://olddragon.com.br/livros/srd.json"
        },
        "digital_item_url": "https://olddragon.com.br/livros/srd.json"
      }
    ],
    "url": "https://olddragon.com.br/racas/elfo.json"
  },
  {
    "id": "humano",
    "type": "CharacterRace",
    "name": "Humano",
    "flavor": "Os mais Comuns, Versáteis e Adaptáveis Aventureiros.",
    "access": "complete",
    "description": "Com enorme variabilidade cultural e disseminados por todos os cantos do mundo, os humanos possuem muita facilidade em assumir o lugar central na maioria dos cenários e, quando analisados sob essa ótica, revelam sua verdadeira força.\n\nVocê conseguirá encontrar humanos em praticamente todos os habitats possíveis, vivendo sob todos os climas, domando o ambiente ao seu bel prazer. Eles se adaptam, se moldam e se espalham como quase nenhuma outra raça – e fazem isso rápido, muito rápido.\n\nPossuem as mais variadas características físicas, muitos tons de cabelo, cores de olhos, pesos e alturas. São encontrados dos mais franzinos aos mais brutamontes. Se aparentam serem frágeis, com uma vida curta, carecendo de poderes ou habilidades especiais, compensam com sua capacidade de organização e expansão, que podem ser impressionantes.\n\nPara o padrão dos mundos de fantasia, humanos se reproduzem muito rápido. Expandem-se com extrema velocidade, ocupam áreas as quais outras raças não conseguem e, por viverem pouco se comparados a outras raças, se relacionam com o tempo de uma forma totalmente diferente. Durante o período da infância de um elfo, um Império humano pode se erguer, viver seu apogeu e desaparecer por completo. Acredite, isso pode ser assustador para um elfo ou um anão.\n\nIsso faz com que os humanos sejam a raça padrão dos mundos de Fantasia, menos pelo seu poder como indivíduo e muito mais pela sua capacidade de se organizar, de assimilar, se desenvolver e ocupar.",
    "personality": "Como na aparência física, os humanos são diversos e versáteis. Sua personalidade é plural. Abraçam todas as linhas de pensamento e é difícil estabelecer um padrão de pensamento e comportamento quando falamos de humanos.\n\nSe observados pelo prisma temporal, os humanos são ultrarrápidos, pois aprendem técnicas e tecnologias as quais avançam e melhoram no espaço de uma única geração. Quando se expandem, nunca atacam e fogem em seguida. Sempre dominam, se estabelecem, permanecem, colonizam e só vão embora quando sua força política e de organização social os impede de continuar onde estão.\n\nHumanos são afeitos a quantidade. Se um elfo leva anos para forjar uma cimitarra obra-prima, aplicando técnicas beirando o sobrenatural na forja, humanos abraçam a produtividade e quantidade.\n\nDo ponto de vista da pluralidade, apesar de parecer um contrassenso, os humanos aceitam bem as diferenças, sobretudo se comparados com outras raças. Convivem com anões, halflings e elfos, algumas vezes até mesmo até assimilando suas colônias, desde que, claro, estes estrangeiros não impeçam seus contínuos planos de expansão, acúmulo de poder e sobrevivência.",
    "adventure": "O humano aventureiro é um retrato do humano padrão. Adaptável, imaginativo, aguerrido e ambicioso.\n\nAventuram-se pelas mais diversas razões – desde para se sustentar até para acumular poder, glória ou fama. A ambição do humano, por qualquer motivo que seja, é a força motriz a qual os tira do conforto de suas choupanas levando-os aos túneis escuros dos subterrâneos.\n\nEles querem deixar um legado, fazer seu nome famoso, virar uma lenda e se tornar um exemplo.\n\nHumanos aventureiros são orgulhosos por deixarem sua marca no mundo.",
    "mv": 9,
    "mve": null,
    "mvn": null,
    "mvv": null,
    "infravision": 0,
    "alignment_tendency": null,
    "picture": null,
    "thumb_picture": null,
    "abilities": [
      {
        "name": "Aprendizado",
        "description": "Humanos aprendem tudo o que se propõem a fazer de forma muito mais rápida que as outras raças. Com isso, um humano recebe um bônus de 10% sobre toda experiência (XP) recebida.\n",
        "mechanic_type": "bonus_xp",
        "mechanic_config": {
          "percentage": 10
        }
      },
      {
        "name": "Adaptabilidade",
        "description": "Os humanos são muito adaptáveis e diversos entre si, fazendo com que possam escolher onde alocar um bônus nas suas Jogadas de Proteção. Humanos recebem um bônus de +1 em uma única JP à sua escolha.\n",
        "mechanic_type": "bonus_jp",
        "mechanic_config": {
          "options": [
            "jpc",
            "jpd",
            "jps"
          ]
        }
      }
    ],
    "fontes": [
      {
        "page": 18,
        "compact": false,
        "digital_item": {
          "id": "lb1",
          "name": "Livro I: Regras Básicas",
          "url": "https://olddragon.com.br/livros/lb1.json"
        },
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      },
      {
        "page": null,
        "compact": true,
        "digital_item": {
          "id": "srd",
          "name": "SRD: Documento de Referência",
          "url": "https://olddragon.com.br/livros/srd.json"
        },
        "digital_item_url": "https://olddragon.com.br/livros/srd.json"
      }
    ],
    "url": "https://olddragon.com.br/racas/humano.json"
  }
]
```
<!-- END character_races_index.json -->
###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/racas.json
```

###### Copiar como HTTPie

``` shell
http https://olddragon.com.br/racas.json
```

Obter raca específica
------------------------

- `GET /racas/anao.json` retorna a raca específica para a ID informada (neste exemplo, a ID é `anao`).

###### Exemplo de resposta JSON
<!-- START character_races_show.json -->
```json
{
  "id": "anao",
  "type": "CharacterRace",
  "name": "Anão",
  "flavor": "Orgulhosos Habitantes dos Salões sob a Montanha.",
  "access": "complete",
  "description": "Honrados, perfeccionistas e reservados, os anões são conhecidos não só pela sua peculiar aparência, mas sobretudo pela forma como se relacionam com as outras raças e com a sua própria história.\n\nDe aparência robustas e rústica, corpulentos e com uma inconfundível grande barba, anões vivem junto dos seus clãs com as montanhas sobre suas cabeças, minerando, forjando, reverenciando seus antepassados e comemorando com cerveja e suas famosas bebidas fortes.\n\nOs Salões sob a Montanha, onde vivem isolados, são locais sagrados e reverenciados por eles. Lá, adotam um estilo de vida comedido, voltado ao trabalho, entrecortando o silêncio apenas com suas canções de trabalho e suas frequentes comemorações.\n\nSão guiados pela honra e pelo sentimento de gratidão por todos aqueles que ajudaram a construir o orgulho que sentem das suas origens, quando lideraram a raça anã em feitos de superação, conquista e guerra contra seus inimigos.\n\nComo bons tradicionalistas, colocam sua família, seu clã e principalmente sua raça acima de todas as coisas, inclusive de si mesmos e de suas vontades pessoais.\n\nBuscam honrar suas origens tentando demonstrar que são dignos de fazer parte do que eles costumam chamar: povo perfeito.\n\nExímios forjadores, trabalham o metal à sua vontade. Não há nada que eles não possam forjar, e não há nenhum objeto de metal que não fique perfeito após um anão aplicar suas técnicas ancestrais de metalurgia.\n\nCom pensamento lógico acurado, se destacam na engenharia, nas construções, nos trabalhos pesados, mas, ao mesmo tempo, demonstram pouca aptidão às artes arcanas.\n\nFora de suas terras, se mostram orgulhosos e defensores de suas origens, fazendo questão de sempre comparar tudo à volta com a versão melhorada a qual os anões são capazes de criar.",
  "personality": "Orgulho, tradição e obsessão são três importantes palavras para descrever a personalidade anã.\n\nOrgulhosos de tudo relativo ao seu povo, estão a todo tempo lembrando a todos da importância, da imponência, da qualidade, da grandiosidade do seu povo, das canções que glorificam as vitórias sobre seus inimigos.\n\nUm anão é quase um escravo dos feitos dos seus antepassados. Um herói anão é, antes de tudo, uma régua de perfeição. Um grau a admirar, perseguir e atingir.\n\nTradição, para eles, não é uma mera forma de passar aos mais novos os costumes de seu povo, e sim um estilo de vida e um código de honra. Uma espécie de linha guia para basear suas ações e seu pensamento.\n\nO anão é um ser obcecado. Pela defesa dos seus ideais, pelo seu povo, pela perfeição do seu trabalho.\n\nSeja a excelência em batalha, o minucioso trabalho de forja de armas e armaduras, a fermentação precisa da cerveja, a composição da canção que zomba dos orcs, o ideal de vida do anão está centrado na perfeição num nível próximo da idolatria espiritual.",
  "adventure": "Partir para as aventuras é mais do que uma opção para alguns anões, sendo, em alguns casos, uma forma de reverenciar as tradições do seu povo.\n\nCom uma memória repleta de feitos épicos e exemplos a admirar e a seguir, provar-se capaz jogando-se no mundo é, sem dúvida, o mais importante dos motivadores para um anão aventurar-se.\n\nO anão quer provar sua capacidade, sua habilidade, resiliência e ser digno de portar o nome de seu clã.\n\nAnões aventureiros são guiados pelo exemplo e pelo orgulho dos feitos os quais podem realizar e que deixarão para as futuras gerações.",
  "mv": 6,
  "mve": null,
  "mvn": null,
  "mvv": null,
  "infravision": 18,
  "alignment_tendency": "ordeiro",
  "picture": null,
  "thumb_picture": null,
  "abilities": [
    {
      "name": "Mineradores",
      "description": "Por milênios, anões aprendem desde cedo a avaliar passagens e condições de muralhas e portais.\n\nPor isso são capazes de detectar, mesmo que não estejam analisando ativamente, com um resultado de 1 em 1d6, anomalias em pedras, como armadilhas em cavernas ou fossos escondidos, ou com um resultado de 1-2 em 1d6 caso estejam efetivamente procurando.\n",
      "mechanic_type": "none",
      "mechanic_config": {}
    },
    {
      "name": "Vigoroso",
      "description": "Os anões são muito resistentes aos efeitos que afetem seu corpo, recebendo um bônus de +1 em qualquer teste de JPC.\n",
      "mechanic_type": "bonus_jp",
      "mechanic_config": {
        "options": [
          "jpc"
        ]
      }
    },
    {
      "name": "Armas grandes",
      "description": "São restritas para anões que podem usar apenas armas médias e pequenas. Armas grandes forjadas como um item racial anão são consideradas armas médias para um anão.\n",
      "mechanic_type": "none",
      "mechanic_config": {}
    },
    {
      "name": "Inimigos",
      "description": "Anões são inimigos naturais e disputam território com orcs, ogros e hobgoblins e, por isso, os ataques dos anões contra essas criaturas são considerados ataques fáceis.\n",
      "mechanic_type": "none",
      "mechanic_config": {}
    }
  ],
  "fontes": [
    {
      "page": 22,
      "compact": false,
      "digital_item": {
        "id": "lb1",
        "name": "Livro I: Regras Básicas",
        "url": "https://olddragon.com.br/livros/lb1.json"
      },
      "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
    },
    {
      "page": null,
      "compact": true,
      "digital_item": {
        "id": "srd",
        "name": "SRD: Documento de Referência",
        "url": "https://olddragon.com.br/livros/srd.json"
      },
      "digital_item_url": "https://olddragon.com.br/livros/srd.json"
    }
  ],
  "url": "https://olddragon.com.br/racas/anao.json"
}
```
<!-- END character_races_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/racas/anao.json
```

###### Copiar como HTTPie

``` shell
http https://olddragon.com.br/racas/anao.json
```

Listar minhas raças
--------------------

* `GET /racas/minhas.json` retorna todas as raças personalizadas do usuário autenticado.

**Requer autenticação.**

###### Exemplo de resposta JSON
<!-- START character_races_my.json -->
```json
[
  {
    "id": "550e8400-e29b-41d4-a716-446655440000",
    "type": "CharacterRace",
    "name": "Raça Personalizada Um",
    "flavor": "Uma raça de teste",
    "access": "complete",
    "description": "Esta é uma raça customizada criada por um jogador para testes.",
    "personality": "",
    "adventure": "",
    "mv": 9,
    "mve": null,
    "mvn": null,
    "mvv": null,
    "infravision": 0,
    "alignment_tendency": null,
    "picture": null,
    "thumb_picture": null,
    "abilities": [],
    "fontes": [],
    "author": {
      "handler": "jogador",
      "url": "https://olddragon.com.br/perfis/jogador.json"
    },
    "url": "https://olddragon.com.br/racas/550e8400-e29b-41d4-a716-446655440000.json"
  }
]
```
<!-- END character_races_my.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/racas/minhas.json -H "Authorization: Bearer <token>"
```

###### Copiar como HTTPie

``` shell
http https://olddragon.com.br/racas/minhas.json Authorization:"Bearer <token>"
```

Listar raças comunitárias
--------------------------

* `GET /racas/comunitarias.json` retorna todas as raças personalizadas compartilhadas pela comunidade (homebrew).

_Parâmetros opcionais de URL_:

* `name` - Filtro por nome. Exemplo: `name=Vampiro`.
* `order` - Ordenação (`name` ou `likes`). Padrão: `likes`.

###### Exemplo de resposta JSON
<!-- START character_races_homebrew.json -->
```json
[
  {
    "id": "550e8400-e29b-41d4-a716-446655440001",
    "type": "CharacterRace",
    "name": "Raça Personalizada Dois",
    "flavor": "Outra raça de teste",
    "access": "complete",
    "description": "Esta é outra raça customizada criada por um jogador para testes.",
    "personality": "",
    "adventure": "",
    "mv": 9,
    "mve": null,
    "mvn": null,
    "mvv": null,
    "infravision": 0,
    "alignment_tendency": null,
    "picture": null,
    "thumb_picture": null,
    "abilities": [],
    "fontes": [],
    "author": {
      "handler": "outro_jogador",
      "url": "https://olddragon.com.br/perfis/outro_jogador.json"
    },
    "url": "https://olddragon.com.br/racas/550e8400-e29b-41d4-a716-446655440001.json"
  }
]
```
<!-- END character_races_homebrew.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/racas/comunitarias.json
```

###### Copiar como HTTPie

``` shell
http https://olddragon.com.br/racas/comunitarias.json
```

### Habilidades Raciais (Abilities)

Cada raça possui um array de `abilities` (habilidades) que descrevem as características especiais e mecânicas da raça. A partir de agora, cada habilidade inclui dois novos campos que definem como a habilidade funciona mecanicamente:

#### Campos das habilidades

* `name`: Nome da habilidade (ex: "Vigoroso", "Adaptabilidade")
* `description`: Descrição textual da habilidade
* `mechanic_type`: Tipo de mecânica que a habilidade aplica
* `mechanic_config`: Configuração específica da mecânica (estrutura varia conforme o `mechanic_type`)

#### Tipos de Mecânicas (`mechanic_type`)

Os valores possíveis para `mechanic_type` são:

* `none`: Habilidade puramente descritiva, sem mecânica automática
* `bonus_damage`: Bônus de dano em condições específicas
* `natural_weapon`: Arma natural da raça (ex: garras, mordida)
* `bonus_hp`: Bônus de pontos de vida por nível
* `bonus_xp`: Bônus percentual de experiência
* `bonus_jp`: **Requer seleção do jogador** - Bônus em Jogada de Proteção (JP)
* `base_armor`: Classe de Armadura base da raça
* `load_modifier`: Modificador de carga máxima
* `armor_weight_modifier`: Redução de peso de armaduras
* `max_load_override`: Substituição completa da carga máxima
* `daily_ability`: Habilidade com usos limitados por dia
* `rogue_talent_bonus`: Bônus em talentos de ladrão
* `variable_construction`: **Requer seleção do jogador** - Opções de construção variável (ex: Autokthon, Cambion, Meio-Dragão)

#### Mecânicas que Requerem Seleção

**Importante**: A maioria das habilidades é aplicada automaticamente. Apenas dois tipos requerem escolha do jogador:

1. **`bonus_jp`** (Bônus em JP): O jogador deve escolher qual JP recebe o bônus
   ```json
   {
     "mechanic_type": "bonus_jp",
     "mechanic_config": {
       "options": ["jpc", "jpd", "jps"]
     }
   }
   ```
   - Apenas uma escolha é permitida por habilidade
   - A escolha do jogador é armazenada em `race_mechanic_selections` no personagem

2. **`variable_construction`** (Construção Variável): O jogador escolhe entre opções predefinidas ou cria opções personalizadas
   ```json
   {
     "mechanic_type": "variable_construction",
     "mechanic_config": {
       "selections_required": 2,
       "available_options": [
         {
           "key": "arma_embutida",
           "name": "Arma Embutida",
           "description": "...",
           "creates_mechanic": "natural_weapon"
         },
         {
           "key": "armadura_leve",
           "name": "Armadura Leve",
           "description": "...",
           "creates_mechanic": "base_armor",
           "mechanic_config": {"ac": 13}
         }
       ]
     }
   }
   ```
   - `selections_required`: Quantidade de opções que o jogador deve escolher
   - `available_options`: Array com as opções disponíveis
   - Cada opção pode criar uma nova mecânica (`creates_mechanic`) com sua própria configuração
   - Algumas raças permitem opções personalizadas (custom) onde o jogador define nome e descrição

#### Exemplos de Configurações

**Bônus de XP** (`bonus_xp`):
```json
{
  "mechanic_type": "bonus_xp",
  "mechanic_config": {
    "percentage": 10
  }
}
```

**Bônus de HP** (`bonus_hp`):
```json
{
  "mechanic_type": "bonus_hp",
  "mechanic_config": {
    "value": 1
  }
}
```

**Arma Natural** (`natural_weapon`):
```json
{
  "mechanic_type": "natural_weapon",
  "mechanic_config": {
    "name": "Garras",
    "damage": "1d4",
    "damage_type": "slashing",
    "weapon_size": "medium"
  }
}
```

**Bônus de Dano** (`bonus_damage`):
```json
{
  "mechanic_type": "bonus_damage",
  "mechanic_config": {
    "value": 1,
    "condition": "arrow"
  }
}
```

Para mais detalhes sobre como as seleções do jogador são armazenadas, consulte a seção "Seleções de Habilidades Raciais" na documentação de personagens.
