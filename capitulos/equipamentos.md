Equipamentos
============

Endpoints:

- [Listar equipamentos](#listar-equipamentos)
- [Obter equipamento específico](#obter-equipamento-específico)

Listar equipamentos
--------------

* `GET /equipamentos.json` retorna todos os equipamentos.

###### Exemplo de resposta JSON
<!-- START GET /equipamentos.json -->
```json
{
  "data": [
    {
      "id": "adaga",
      "type": "equipamentos",
      "attributes": {
        "name": "Adaga",
        "concept": "weapon",
        "updated_at": "2023-05-31T21:58:15.299-03:00",
        "access": "complete",
        "cost": 200,
        "damage": "1d4",
        "bonus_ca": null,
        "weight_in_load": 1,
        "weight_in_grams": null,
        "description": "Pequena, Perfurante, Arremesso (9)",
        "picture": "https://public.olddragon.com.br/example"
      },
      "relationships": {
        "fontes": [
          {
            "id": "lb1",
            "type": "fontes",
            "attributes": {
              "page": 58
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
        "self": "https://olddragon.com.br/equipamentos/adaga.json"
      }
    },
    {
      "id": "arco-longo",
      "type": "equipamentos",
      "attributes": {
        "name": "Arco Longo",
        "concept": "weapon",
        "updated_at": "2023-05-31T21:58:20.800-03:00",
        "access": "complete",
        "cost": 6000,
        "damage": null,
        "bonus_ca": null,
        "weight_in_load": 3,
        "weight_in_grams": null,
        "description": "Grande, Disparo (45), Duas Mãos",
        "picture": "https://public.olddragon.com.br/example"
      },
      "relationships": {
        "fontes": [
          {
            "id": "lb1",
            "type": "fontes",
            "attributes": {
              "page": 58
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
        "self": "https://olddragon.com.br/equipamentos/arco-longo.json"
      }
    }
  ],
  "links": {
    "first": "/equipamentos.json?page=1",
    "self": "/equipamentos.json?page=1",
    "next": "/equipamentos.json?page=2",
    "last": "/equipamentos.json?page=10"
  },
  "meta": {
    "pages": 10,
    "count": 100
  }
}
```
<!-- END GET /equipamentos.json -->
###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/equipamentos.json
```

Obter equipamento específico
------------------------

* `GET /equipamentos/adaga.json` retorna o equipamento específico para a ID informada.

###### Exemplo de resposta JSON
<!-- START GET /equipamentos/adaga.json -->
```json
{
  "data": {
    "id": "adaga",
    "type": "equipamentos",
    "attributes": {
      "name": "Adaga",
      "concept": "weapon",
      "updated_at": "2023-05-31T21:58:15.299-03:00",
      "access": "complete",
      "cost": 200,
      "damage": "1d4",
      "bonus_ca": null,
      "weight_in_load": 1,
      "weight_in_grams": null,
      "description": "Pequena, Perfurante, Arremesso (9)",
      "picture": "https://public.olddragon.com.br/example"
    },
    "relationships": {
      "fontes": [
        {
          "id": "lb1",
          "type": "fontes",
          "attributes": {
            "page": 58
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
      "self": "https://olddragon.com.br/equipamentos/adaga.json"
    }
  }
}
```
<!-- END GET /equipamentos/adaga.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/equipamentos/adaga.json
```
