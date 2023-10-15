Livros
======

Endpoints:

- [Listar livros](#listar-livros)
- [Obter livro específico](#obter-livro-específico)

Listar livros
-------------

* `GET /livros.json` retorna todos os livros.

###### Exemplo de resposta JSON
<!-- START digital_items_index.json -->
```json
{
  "data": [
    {
      "id": "ajuda",
      "type": "livros",
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
        "description": "Esta livro concede uma ajuda de sua divindade, anulando a perda de até 1d4 pontos de vida +1 a cada 2 níveis do conjurador, do próximo dano sofrido pelo conjurador. Pontos de vida anulados que sobram após o próximo dano recebido pelo conjurador, devem ser descartados.\n"
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
        "self": "https://olddragon.com.br/livros/ajuda.json"
      }
    },
    {
      "id": "bom-fruto",
      "type": "livros",
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
        "description": "Com esta livro, o conjurador é capaz de abençoar 2d4 frutos e torná-los mágicos. Quem comer destes frutos recuperará 1 ponto de vida perdido por nível do conjurador. A cada 24 horas, apenas 8 pontos de vida podem ser recuperados com esta livro.\n"
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
        "self": "https://olddragon.com.br/livros/bom-fruto.json"
      }
    }
  ],
  "links": {
    "first": "/livros.json?page=1",
    "self": "/livros.json?page=1",
    "next": "/livros.json?page=2",
    "last": "/livros.json?page=10"
  },
  "meta": {
    "pages": 10,
    "count": 100
  }
}
```
<!-- END digital_items_index.json -->
###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/livros.json
```

Obter livro específica
----------------------

* `GET /livros/orc.json` retorna a livro específica para a ID informada.



###### Exemplo de resposta JSON
<!-- START digital_items_show.json -->
```json
{
  "data": {
    "id": "ajuda",
    "type": "livros",
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
      "description": "Esta livro concede uma ajuda de sua divindade, anulando a perda de até 1d4 pontos de vida +1 a cada 2 níveis do conjurador, do próximo dano sofrido pelo conjurador. Pontos de vida anulados que sobram após o próximo dano recebido pelo conjurador, devem ser descartados.\n"
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
      "self": "https://olddragon.com.br/livros/ajuda.json"
    }
  }
}
```
<!-- END digital_items_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/livros/ajuda.json
```

### Observações sobre atributos

O atributo `reverse` denota que esta livro possui uma livro reversa. Por exemplo, a livro "Abrir" retorna com `attributes.reverse` positiva, bem como uma `relationships.reverse_spell` apontando para a livro reversa "Trancar".

O atributo `access` é explicado em [Acesso](https://github.com/burobrasil/olddragon-api/blob/master/capitulos/acesso.md#acesso).
