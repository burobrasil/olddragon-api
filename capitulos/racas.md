Raças
========

Endpoints:

- [Listar racas](#listar-racas)
- [Obter raça específica](#obter-raca-específica)

Listar raças
--------------

* `GET /racas.json` retorna todos as raças.

###### Exemplo de resposta JSON
<!-- START character_races_index.json -->
```json
[
  {
    "id": "anao",
    "type": "CharacterRace",
    "name": "Anão",
    "flavor": "Orgulhosos Habitantes dos Salões sob a Montanha.",
    "movement": 6,
    "infravision": 18,
    "alignment_tendency": "ordeiro",
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
    "movement": 9,
    "infravision": 18,
    "alignment_tendency": "neutro",
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
    "movement": 9,
    "infravision": 0,
    "alignment_tendency": null,
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
  "movement": 6,
  "infravision": 18,
  "alignment_tendency": "ordeiro",
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
