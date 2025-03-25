Raças
========

Endpoints:

- [Listar racas](#listar-racas)
- [Obter raça específica](#obter-raca-específica)

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
    "description": "Honrados, perfeccionistas e reservados, os anões são conhecidos não só pela sua peculiar aparência, mas sobretudo pela forma como se relacionam com as outras raças e com a sua própria história.\n\nDe aparência robustas e rústica, corpulentos e com uma inconfundível grande barba, anões vivem junto dos seus clãs com as montanhas sobre suas cabeças, minerando, forjando, reverenciando seus antepassados e comemorando com cerveja e suas famosas bebidas fortes.\n\nOs Salões sob a Montanha, onde vivem isolados, são locais sagrados e reverenciados por eles. Lá, adotam um estilo de vida comedido, voltado ao trabalho, entrecortando o silêncio apenas com suas canções de trabalho e suas frequentes comemorações.\n\nSão guiados pela honra e pelo sentimento de gratidão por todos aqueles que ajudaram a construir o orgulho que sentem das suas origens, quando lideraram a raça anã em feitos de superação, conquista e guerra contra seus inimigos.\n\nComo bons tradicionalistas, colocam sua família, seu clã e principalmente sua raça acima de todas as coisas, inclusive de si mesmos e de suas vontades pessoais.\n\nBuscam honrar suas origens tentando demonstrar que são dignos de fazer parte do que eles costumam chamar: povo perfeito.\n\nExímios forjadores, trabalham o metal à sua vontade. Não há nada que eles não possam forjar, e não há nenhum objeto de metal que não fique perfeito após um anão aplicar suas técnicas ancestrais de metalurgia.\n\nCom pensamento lógico acurado, se destacam na engenharia, nas construções, nos trabalhos pesados, mas, ao mesmo tempo, demonstram pouca aptidão às artes arcanas.\n\nFora de suas terras, se mostram orgulhosos e defensores de suas origens, fazendo questão de sempre comparar tudo à volta com a versão melhorada a qual os anões são capazes de criar.\n\n# Personalidade\n\nOrgulho, tradição e obsessão são três importantes palavras para descrever a personalidade anã.\n\nOrgulhosos de tudo relativo ao seu povo, estão a todo tempo lembrando a todos da importância, da imponência, da qualidade, da grandiosidade do seu povo, das canções que glorificam as vitórias sobre seus inimigos.\n\nUm anão é quase um escravo dos feitos dos seus antepassados. Um herói anão é, antes de tudo, uma régua de perfeição. Um grau a admirar, perseguir e atingir.\n\nTradição, para eles, não é uma mera forma de passar aos mais novos os costumes de seu povo, e sim um estilo de vida e um código de honra. Uma espécie de linha guia para basear suas ações e seu pensamento.\n\nO anão é um ser obcecado. Pela defesa dos seus ideais, pelo seu povo, pela perfeição do seu trabalho.\n\nSeja a excelência em batalha, o minucioso trabalho de forja de armas e armaduras, a fermentação precisa da cerveja, a composição da canção que zomba dos orcs, o ideal de vida do anão está centrado na perfeição num nível próximo da idolatria espiritual.\n\n# O Anão nas Aventuras\n\nPartir para as aventuras é mais do que uma opção para alguns anões, sendo, em alguns casos, uma forma de reverenciar as tradições do seu povo.\n\nCom uma memória repleta de feitos épicos e exemplos a admirar e a seguir, provar-se capaz jogando-se no mundo é, sem dúvida, o mais importante dos motivadores para um anão aventurar-se.\n\nO anão quer provar sua capacidade, sua habilidade, resiliência e ser digno de portar o nome de seu clã.\n\nAnões aventureiros são guiados pelo exemplo e pelo orgulho dos feitos os quais podem realizar e que deixarão para as futuras gerações.\n\n## Perguntas para se responder ao criar um anão:\n\n* **Pergunta 1:** _Do que seu anão mais se orgulha das suas tradições?_\n* **Pergunta 2:** _O que seu anão busca provar ou realizar?_\n* **Pergunta 3:** _O que seu anão possui como principal obsessão?_\n",
    "movement": 6,
    "infravision": 18,
    "alignment_tendency": "ordeiro",
    "picture": null,
    "thumb_picture": null,
    "abilities": [
      {
        "name": "Mineradores",
        "description": "Por milênios, anões aprendem desde cedo a avaliar passagens e condições de muralhas e portais.\n\nPor isso são capazes de detectar, mesmo que não estejam analisando ativamente, com um resultado de 1 em 1d6, anomalias em pedras, como armadilhas em cavernas ou fossos escondidos, ou com um resultado de 1-2 em 1d6 caso estejam efetivamente procurando.\n"
      },
      {
        "name": "Vigoroso",
        "description": "Os anões são muito resistentes aos efeitos que afetem seu corpo, recebendo um bônus de +1 em qualquer teste de JPC.\n"
      },
      {
        "name": "Armas grandes",
        "description": "São restritas para anões que podem usar apenas armas médias e pequenas. Armas grandes forjadas como um item racial anão são consideradas armas médias para um anão.\n"
      },
      {
        "name": "Inimigos",
        "description": "Anões são inimigos naturais e disputam território com orcs, ogros e hobgoblins e, por isso, os ataques dos anões contra essas criaturas são considerados ataques fáceis.\n"
      }
    ],
    "fontes": [
      {
        "page": 22,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      },
      {
        "page": null,
        "compact": true,
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
    "description": "Os elfos são das mais longevas raças encontradas nos mundos de fantasia e a sua relação com o tempo doutrina boa parte das suas características, personalidade e a forma como as outras raças os enxergam e se relacionam com eles.\n\nFisicamente são esguios e até um pouco franzinos se comparados a um humano, além de ligeiramente mais baixos. Seus cabelos, compridos para machos e fêmeas, estão sempre penteados, adornados com acessórios e podem ser encontrados em praticamente todas as cores.\n\nA característica física mais marcante de um elfo está nas suas orelhas – pontudas e longas –, muito embora o traço dos seus olhos – amendoados, delicados e levemente alongados – seja uma característica igualmente marcante.\n\nA relação do elfo com o tempo dita sua forma de pensar e agir. Como frequentemente atingem 1.000 anos de vida, elfos se sentem compelidos a ocuparem suas vidas com o que mais valorizam como a dança, a música, a esgrima, o arqueirismo e a magia arcana.\n\nIsso pode fazer as pessoas acreditarem que Elfos são distantes ou, de certa forma, um pouco fúteis. Um erro comum cometido pelos observadores menos atentos.\n\nOutra característica dos elfos, sobretudo os que estão fora da sua terra, é a distância, dando-lhes uma certa característica de frieza e até prepotência. Por se considerarem estranhos fora de suas fronteiras, possuem dificuldade de se envolver nos problemas das outras raças, refletindo na dificuldade de criar laços de amizade.\n\nNo entanto, quando um elfo é conquistado como amigo, a amizade se mostrará duradoura. A amizade de um elfo dura mais do que muitas vidas, costumam dizer os humanos os quais puderam provar desse relacionamento. Vivendo tantos séculos, esta é uma verdade incontestável.\n\n# Personalidade\n\nViver tanto tempo molda a personalidade de um elfo. O ritmo do tempo é excepcional para um elfo. As mudanças ocorrem tão depressa que se tornam complicadas de seguir, então, para que se importar? Melhor é focar na qualidade e não na quantidade. Se 100 espadas medianas podem ser confeccionadas, um elfo prefere gastar o mesmo tempo numa única peça exemplar em qualidade e perfeição.\n\nCom tanto tempo disponível para aprender tantas coisas, desperdiçar tempo seria uma opção bem óbvia, mas aí se esconde uma grandeza da sua raça. Ao contrário do que possa parecer, elfos gostam de coisas bem-feitas e duradouras, assim como eles. Serviço bem-feito é sempre aquele com a maior duração.\n\nEssa relação entre qualidade, tempo e perfeição molda todo o pensamento élfico e a construção da sua personalidade.\n\n# O Elfo nas Aventuras\n\nApesar de bem mais raros que os humanos, elfos não são aventureiros improváveis. A fome por conhecimento, desejo por viajar, a vontade de provar-se para os seus como um elfo exemplar e, principalmente, o tempo disponível, são as principais forças a empurrar um elfo para a vida aventureira.\n\nAs coisas mudam tão rapidamente que acompanhar as mudanças, ou mesmo fazer parte destas mudanças, pode ser uma interessante força motriz para eles.\n\nEles querem acompanhar o que acontece, se aperfeiçoarem e se provarem como capazes.\n\nElfos são aventureiros observadores que querem entender o mundo onde vivem.\n\n## Perguntas para se responder ao criar um elfo:\n\n* **Pergunta 1:** _O que seu elfo busca provar? Para si ou para seus iguais?_\n* **Pergunta 2:** _O que seu elfo pensa sobre estar com outras raças?_\n* **Pergunta 3:** _O que seu elfo sente por estar longe de sua terra?_\n",
    "movement": 9,
    "infravision": 18,
    "alignment_tendency": "neutro",
    "picture": null,
    "thumb_picture": null,
    "abilities": [
      {
        "name": "Percepção Natural",
        "description": "A forma como as casas élficas são construídas, respeitando a forma natural das árvores e abrigos, dá aos elfos uma percepção especial no que diz respeito a portas e passagens não convencionais e até mesmo secretas.\n\nAo passarem a até 6 metros de uma porta secreta, mesmo que não a estejam procurando, os elfos podem detectá-la com um resultado 1 em 1d6, ou com um resultado de 1-2 em 1d6 caso estejam efetivamente procurando pela porta secreta.\n"
      },
      {
        "name": "Graciosos",
        "description": "Os elfos controlam com precisão seus movimentos no espaço ao redor do seu corpo, recebendo um bônus de +1 em qualquer teste de JPD.\n"
      },
      {
        "name": "Arma Racial",
        "description": "Os elfos possuem familiaridade com o arqueirismo, o qual consideram uma arte marcial, recebendo um bônus de +1 nos danos causados em seus ataques à distância com os arcos.\n"
      },
      {
        "name": "Imunidades",
        "description": "Os elfos são imunes a efeitos ou magias que envolvam sono e também contra a paralisação causada por um Ghoul.\n"
      }
    ],
    "fontes": [
      {
        "page": 20,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      },
      {
        "page": null,
        "compact": true,
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
    "description": "Com enorme variabilidade cultural e disseminados por todos os cantos do mundo, os humanos possuem muita facilidade em assumir o lugar central na maioria dos cenários e, quando analisados sob essa ótica, revelam sua verdadeira força.\n\nVocê conseguirá encontrar humanos em praticamente todos os habitats possíveis, vivendo sob todos os climas, domando o ambiente ao seu bel prazer. Eles se adaptam, se moldam e se espalham como quase nenhuma outra raça – e fazem isso rápido, muito rápido.\n\nPossuem as mais variadas características físicas, muitos tons de cabelo, cores de olhos, pesos e alturas. São encontrados dos mais franzinos aos mais brutamontes. Se aparentam serem frágeis, com uma vida curta, carecendo de poderes ou habilidades especiais, compensam com sua capacidade de organização e expansão, que podem ser impressionantes.\n\nPara o padrão dos mundos de fantasia, humanos se reproduzem muito rápido. Expandem-se com extrema velocidade, ocupam áreas as quais outras raças não conseguem e, por viverem pouco se comparados a outras raças, se relacionam com o tempo de uma forma totalmente diferente. Durante o período da infância de um elfo, um Império humano pode se erguer, viver seu apogeu e desaparecer por completo. Acredite, isso pode ser assustador para um elfo ou um anão.\n\nIsso faz com que os humanos sejam a raça padrão dos mundos de Fantasia, menos pelo seu poder como indivíduo e muito mais pela sua capacidade de se organizar, de assimilar, se desenvolver e ocupar.\n\n# Personalidade\n\nComo na aparência física, os humanos são diversos e versáteis. Sua personalidade é plural. Abraçam todas as linhas de pensamento e é difícil estabelecer um padrão de pensamento e comportamento quando falamos de humanos.\n\nSe observados pelo prisma temporal, os humanos são ultrarrápidos, pois aprendem técnicas e tecnologias as quais avançam e melhoram no espaço de uma única geração. Quando se expandem, nunca atacam e fogem em seguida. Sempre dominam, se estabelecem, permanecem, colonizam e só vão embora quando sua força política e de organização social os impede de continuar onde estão.\n\nHumanos são afeitos a quantidade. Se um elfo leva anos para forjar uma cimitarra obra-prima, aplicando técnicas beirando o sobrenatural na forja, humanos abraçam a produtividade e quantidade.\n\nDo ponto de vista da pluralidade, apesar de parecer um contrassenso, os humanos aceitam bem as diferenças, sobretudo se comparados com outras raças. Convivem com anões, halflings e elfos, algumas vezes até mesmo até assimilando suas colônias, desde que, claro, estes estrangeiros não impeçam seus contínuos planos de expansão, acúmulo de poder e sobrevivência.\n\n# O Humano nas Aventuras\n\nO humano aventureiro é um retrato do humano padrão. Adaptável, imaginativo, aguerrido e ambicioso.\n\nAventuram-se pelas mais diversas razões – desde para se sustentar até para acumular poder, glória ou fama. A ambição do humano, por qualquer motivo que seja, é a força motriz a qual os tira do conforto de suas choupanas levando-os aos túneis escuros dos subterrâneos.\n\nEles querem deixar um legado, fazer seu nome famoso, virar uma lenda e se tornar um exemplo.\n\nHumanos aventureiros são orgulhosos por deixarem sua marca no mundo.\n\n## Perguntas para se responder ao criar um humano:\n\n* **Pergunta 1:** _O que seu humano usa como motivo para aventurar-se?_\n* **Pergunta 2:** _O que seu humano respeita? O que ele busca defender?_\n* **Pergunta 3:** _O que seu humano odeia? O que ele deseja destruir?_\n",
    "movement": 9,
    "infravision": 0,
    "alignment_tendency": null,
    "picture": null,
    "thumb_picture": null,
    "abilities": [
      {
        "name": "Aprendizado",
        "description": "Humanos aprendem tudo o que se propõem a fazer de forma muito mais rápida que as outras raças. Com isso, um humano recebe um bônus de 10% sobre toda experiência (XP) recebida.\n"
      },
      {
        "name": "Adaptabilidade",
        "description": "Os humanos são muito adaptáveis e diversos entre si, fazendo com que possam escolher onde alocar um bônus nas suas Jogadas de Proteção. Humanos recebem um bônus de +1 em uma única JP à sua escolha.\n"
      }
    ],
    "fontes": [
      {
        "page": 18,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      },
      {
        "page": null,
        "compact": true,
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
  "description": "Honrados, perfeccionistas e reservados, os anões são conhecidos não só pela sua peculiar aparência, mas sobretudo pela forma como se relacionam com as outras raças e com a sua própria história.\n\nDe aparência robustas e rústica, corpulentos e com uma inconfundível grande barba, anões vivem junto dos seus clãs com as montanhas sobre suas cabeças, minerando, forjando, reverenciando seus antepassados e comemorando com cerveja e suas famosas bebidas fortes.\n\nOs Salões sob a Montanha, onde vivem isolados, são locais sagrados e reverenciados por eles. Lá, adotam um estilo de vida comedido, voltado ao trabalho, entrecortando o silêncio apenas com suas canções de trabalho e suas frequentes comemorações.\n\nSão guiados pela honra e pelo sentimento de gratidão por todos aqueles que ajudaram a construir o orgulho que sentem das suas origens, quando lideraram a raça anã em feitos de superação, conquista e guerra contra seus inimigos.\n\nComo bons tradicionalistas, colocam sua família, seu clã e principalmente sua raça acima de todas as coisas, inclusive de si mesmos e de suas vontades pessoais.\n\nBuscam honrar suas origens tentando demonstrar que são dignos de fazer parte do que eles costumam chamar: povo perfeito.\n\nExímios forjadores, trabalham o metal à sua vontade. Não há nada que eles não possam forjar, e não há nenhum objeto de metal que não fique perfeito após um anão aplicar suas técnicas ancestrais de metalurgia.\n\nCom pensamento lógico acurado, se destacam na engenharia, nas construções, nos trabalhos pesados, mas, ao mesmo tempo, demonstram pouca aptidão às artes arcanas.\n\nFora de suas terras, se mostram orgulhosos e defensores de suas origens, fazendo questão de sempre comparar tudo à volta com a versão melhorada a qual os anões são capazes de criar.\n\n# Personalidade\n\nOrgulho, tradição e obsessão são três importantes palavras para descrever a personalidade anã.\n\nOrgulhosos de tudo relativo ao seu povo, estão a todo tempo lembrando a todos da importância, da imponência, da qualidade, da grandiosidade do seu povo, das canções que glorificam as vitórias sobre seus inimigos.\n\nUm anão é quase um escravo dos feitos dos seus antepassados. Um herói anão é, antes de tudo, uma régua de perfeição. Um grau a admirar, perseguir e atingir.\n\nTradição, para eles, não é uma mera forma de passar aos mais novos os costumes de seu povo, e sim um estilo de vida e um código de honra. Uma espécie de linha guia para basear suas ações e seu pensamento.\n\nO anão é um ser obcecado. Pela defesa dos seus ideais, pelo seu povo, pela perfeição do seu trabalho.\n\nSeja a excelência em batalha, o minucioso trabalho de forja de armas e armaduras, a fermentação precisa da cerveja, a composição da canção que zomba dos orcs, o ideal de vida do anão está centrado na perfeição num nível próximo da idolatria espiritual.\n\n# O Anão nas Aventuras\n\nPartir para as aventuras é mais do que uma opção para alguns anões, sendo, em alguns casos, uma forma de reverenciar as tradições do seu povo.\n\nCom uma memória repleta de feitos épicos e exemplos a admirar e a seguir, provar-se capaz jogando-se no mundo é, sem dúvida, o mais importante dos motivadores para um anão aventurar-se.\n\nO anão quer provar sua capacidade, sua habilidade, resiliência e ser digno de portar o nome de seu clã.\n\nAnões aventureiros são guiados pelo exemplo e pelo orgulho dos feitos os quais podem realizar e que deixarão para as futuras gerações.\n\n## Perguntas para se responder ao criar um anão:\n\n* **Pergunta 1:** _Do que seu anão mais se orgulha das suas tradições?_\n* **Pergunta 2:** _O que seu anão busca provar ou realizar?_\n* **Pergunta 3:** _O que seu anão possui como principal obsessão?_\n",
  "movement": 6,
  "infravision": 18,
  "alignment_tendency": "ordeiro",
  "picture": null,
  "thumb_picture": null,
  "abilities": [
    {
      "name": "Mineradores",
      "description": "Por milênios, anões aprendem desde cedo a avaliar passagens e condições de muralhas e portais.\n\nPor isso são capazes de detectar, mesmo que não estejam analisando ativamente, com um resultado de 1 em 1d6, anomalias em pedras, como armadilhas em cavernas ou fossos escondidos, ou com um resultado de 1-2 em 1d6 caso estejam efetivamente procurando.\n"
    },
    {
      "name": "Vigoroso",
      "description": "Os anões são muito resistentes aos efeitos que afetem seu corpo, recebendo um bônus de +1 em qualquer teste de JPC.\n"
    },
    {
      "name": "Armas grandes",
      "description": "São restritas para anões que podem usar apenas armas médias e pequenas. Armas grandes forjadas como um item racial anão são consideradas armas médias para um anão.\n"
    },
    {
      "name": "Inimigos",
      "description": "Anões são inimigos naturais e disputam território com orcs, ogros e hobgoblins e, por isso, os ataques dos anões contra essas criaturas são considerados ataques fáceis.\n"
    }
  ],
  "fontes": [
    {
      "page": 22,
      "compact": false,
      "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
    },
    {
      "page": null,
      "compact": true,
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
