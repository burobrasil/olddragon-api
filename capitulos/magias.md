Magias
======

Endpoints:

- [Listar magias](#listar-magias)
- [Obter magia específico](#obter-magia-específico)

Listar magias
-------------

* `GET /magias.json` retorna todos os magias.

###### Exemplo de resposta JSON
<!-- START GET /magias.json -->
```json
{
  "data": [
    {
      "id": "ajuda",
      "type": "magias",
      "attributes": {
        "name": "Ajuda",
        "arcane": null,
        "divine": 2,
        "necromancer": null,
        "illusionist": null,
        "updated_at": "2023-05-31T22:12:53.030-03:00",
        "reverse": false,
        "access": "complete",
        "range": "toque",
        "duration": "2 turnos",
        "jp": "nenhuma",
        "description": "Esta magia concede uma ajuda de sua divindade, anulando a perda de até 1d4 pontos de vida +1 a cada 2 níveis do conjurador, do próximo dano sofrido pelo conjurador. Pontos de vida anulados que sobram após o próximo dano recebido pelo conjurador, devem ser descartados.\n"
      },
      "relationships": {
        "fontes": [
          {
            "id": "lb1",
            "type": "fontes",
            "attributes": {
              "page": 105
            },
            "relationships": {
              "livro": {
                "id": "lb1",
                "type": "livros",
                "links": {
                  "self": "https://olddragon.com.br/livros/lb1.json"
                }
              }
            }
          }
        ]
      },
      "links": {
        "self": "https://olddragon.com.br/magias/ajuda.json"
      }
    },
    {
      "id": "bom-fruto",
      "type": "magias",
      "attributes": {
        "name": "Bom Fruto",
        "arcane": null,
        "divine": 2,
        "necromancer": null,
        "illusionist": null,
        "updated_at": "2023-05-31T22:12:53.460-03:00",
        "reverse": false,
        "access": "complete",
        "range": "toque",
        "duration": "especial",
        "jp": "nenhuma",
        "description": "Com esta magia, o conjurador é capaz de abençoar 2d4 frutos e torná-los mágicos. Quem comer destes frutos recuperará 1 ponto de vida perdido por nível do conjurador. A cada 24 horas, apenas 8 pontos de vida podem ser recuperados com esta magia.\n"
      },
      "relationships": {
        "fontes": [
          {
            "id": "lb1",
            "type": "fontes",
            "attributes": {
              "page": 108
            },
            "relationships": {
              "livro": {
                "id": "lb1",
                "type": "livros",
                "links": {
                  "self": "https://olddragon.com.br/livros/lb1.json"
                }
              }
            }
          }
        ]
      },
      "links": {
        "self": "https://olddragon.com.br/magias/bom-fruto.json"
      }
    }
  ],
  "links": {
    "first": "/magias.json?page=1",
    "self": "/magias.json?page=1",
    "next": "/magias.json?page=2",
    "last": "/magias.json?page=10"
  },
  "meta": {
    "pages": 10,
    "count": 100
  }
}
```
<!-- END GET /magias.json -->
###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/magias.json
```

Obter magia específica
----------------------

* `GET /magias/orc.json` retorna a magia específica para a ID informada.

###### Exemplo de resposta JSON
<!-- START GET /magias/ajuda.json -->
```json
{
  "data": {
    "id": "ajuda",
    "type": "magias",
    "attributes": {
      "name": "Ajuda",
      "arcane": null,
      "divine": 2,
      "necromancer": null,
      "illusionist": null,
      "updated_at": "2023-05-31T22:12:53.030-03:00",
      "reverse": false,
      "access": "complete",
      "range": "toque",
      "duration": "2 turnos",
      "jp": "nenhuma",
      "description": "Esta magia concede uma ajuda de sua divindade, anulando a perda de até 1d4 pontos de vida +1 a cada 2 níveis do conjurador, do próximo dano sofrido pelo conjurador. Pontos de vida anulados que sobram após o próximo dano recebido pelo conjurador, devem ser descartados.\n"
    },
    "relationships": {
      "fontes": [
        {
          "id": "lb1",
          "type": "fontes",
          "attributes": {
            "page": 105
          },
          "relationships": {
            "livro": {
              "id": "lb1",
              "type": "livros",
              "links": {
                "self": "https://olddragon.com.br/livros/lb1.json"
              }
            }
          }
        }
      ]
    },
    "links": {
      "self": "https://olddragon.com.br/magias/ajuda.json"
    }
  }
}
```
<!-- END GET /magias/ajuda.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/magias/ajuda.json
```
