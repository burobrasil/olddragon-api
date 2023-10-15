Magias
======

Endpoints:

- [Listar magias](#listar-magias)
- [Obter magia específico](#obter-magia-específico)

Listar magias
-------------

- `GET /magias.json` retorna todos os magias.

_Parâmetros opcionais de URL_:

Este endpoint, sem nenhum parâmetro, retorna:

- `order` - ordena a lista. Opções são `name` (padrão), `reverse_name`, `circle`, `reverse_circle`.
- `name` - filtragem parcial pelo nome. Por exemplo, se for passado `abe`, serão retornadas as magias "Abençoar" e "Arma Abençoada".
- `schools[]` - filtragem com lista (_array_) das escolas de magias. Opções são `arcane` (Arcana), `divine` (Divina), `necromancer` (Necromante), e `illusionist` (Ilusionista). Deixe em branco ou sem este parâmetro para retornar de todas as escolas de magia. Várias podem ser informadas para retornar de mais de uma escola ao mesmo tempo.
- `circles[]` - filtragem com lista (_array_) dos círculos da magia. Caso a magia possua mais de um círculo (como "Ampliar Plantas", que é Arcana de 4o cículo e Divina de 3o círculo), será considerado o círculo menor das magias filtradas no parâmetro `schools[]` (ou de todas caso não esteja presente). Opções são `1o`, `2o`, `3o`, `4o`, `5o`, `6o`, `7o`, `8o`, `9o`. Vários podem ser informados para retornar de mais de um círculo de magia ao mesmo tempo.
- `sources[]` - filtragem com lista (_array_) das fontes das magias. O ID do livro (como `c520caa7-e1de-4919-b273-190be862f4eb` para o LB1) deve ser informado para referenciar o livro. Vários podem ser informados para retornar de mais de um livro ao mesmo tempo.

###### Exemplo de resposta JSON
<!-- START spells_index.json -->
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
<!-- END spells_index.json -->
###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/magias.json
```

Obter magia específica
----------------------

- `GET /magias/ajuda.json` retorna a magia específica para a ID informada (neste exemplo, a ID é `ajuda`).

###### Exemplo de resposta JSON
<!-- START spells_show.json -->
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
<!-- END spells_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/magias/ajuda.json
```

### Observações sobre atributos

O atributo `reverse` denota que esta magia possui uma magia reversa. Por exemplo, a magia "Abrir" retorna com `attributes.reverse` positiva, bem como uma `relationships.reverse_spell` apontando para a magia reversa "Trancar".

O atributo `access` é explicado em [Acesso](https://github.com/burobrasil/olddragon-api/blob/master/capitulos/acesso.md#acesso).
