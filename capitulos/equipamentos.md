Equipamentos
============

Endpoints:

- [Listar equipamentos](#listar-equipamentos)
- [Obter equipamento específico](#obter-equipamento-específico)

Listar equipamentos
--------------

- `GET /equipamentos.json` retorna todos os equipamentos.

_Parâmetros opcionais de URL_:

* `ids[]` - Lista de IDs de equipamentos. Exemplo: `ids[]=adaga&ids[]=escudo`.

###### Exemplo de resposta JSON
<!-- START equipment_index.json -->
```json
[
  {
    "id": "adaga",
    "type": "Equipment",
    "name": "Adaga",
    "concept": "weapon",
    "updated_at": "2023-01-01T00:00:00.000",
    "access": "complete",
    "cost": 200,
    "damage": "1d4",
    "bonus_ca": null,
    "weight_in_load": 1,
    "weight_in_grams": null,
    "description": "Pequena, Perfurante, Arremesso (9)\n",
    "fontes": [
      {
        "page": 58,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      }
    ],
    "url": "https://olddragon.com.br/equipamentos/adaga.json"
  },
  {
    "id": "escudo",
    "type": "Equipment",
    "name": "Escudo",
    "concept": "shield",
    "updated_at": "2023-01-01T00:00:00.000",
    "access": "complete",
    "cost": 800,
    "damage": null,
    "bonus_ca": 1,
    "weight_in_load": 1,
    "weight_in_grams": null,
    "description": "Leve, Mão Exclusiva, Madeira.\n",
    "fontes": [
      {
        "page": 60,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      }
    ],
    "url": "https://olddragon.com.br/equipamentos/escudo.json"
  },
  {
    "id": "espada-curta",
    "type": "Equipment",
    "name": "Espada Curta",
    "concept": "weapon",
    "updated_at": "2023-01-01T00:00:00.000",
    "access": "complete",
    "cost": 600,
    "damage": "1d6",
    "bonus_ca": null,
    "weight_in_load": 1,
    "weight_in_grams": null,
    "description": "Pequena, Cortante.",
    "fontes": [
      {
        "page": 58,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      }
    ],
    "url": "https://olddragon.com.br/equipamentos/espada-curta.json"
  },
  {
    "id": "lanca",
    "type": "Equipment",
    "name": "Lança",
    "concept": "weapon",
    "updated_at": "2023-01-01T00:00:00.000",
    "access": "complete",
    "cost": 400,
    "damage": "1d6",
    "bonus_ca": null,
    "weight_in_load": 2,
    "weight_in_grams": null,
    "description": "Média, Madeira, Perfurante, Arremesso (12), Haste, Versátil, Contrainvestida.",
    "fontes": [
      {
        "page": 58,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      }
    ],
    "url": "https://olddragon.com.br/equipamentos/lanca.json"
  },
  {
    "id": "tocha",
    "type": "Equipment",
    "name": "Tocha",
    "concept": "misc",
    "updated_at": "2023-01-01T00:00:00.000",
    "access": "complete",
    "cost": 100,
    "damage": null,
    "bonus_ca": null,
    "weight_in_load": null,
    "weight_in_grams": 500,
    "description": "5 unidades.\n",
    "fontes": [
      {
        "page": 62,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      }
    ],
    "url": "https://olddragon.com.br/equipamentos/tocha.json"
  }
]
```
<!-- END equipment_index.json -->
###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/equipamentos.json
```

###### Copiar como HTTPie

``` shell
http https://olddragon.com.br/equipamentos.json
```

Obter equipamento específico
------------------------

- `GET /equipamentos/adaga.json` retorna o equipamento específico para a ID informada (neste exemplo, a ID é `adaga`)

###### Exemplo de resposta JSON
<!-- START equipment_show.json -->
```json
{
  "id": "adaga",
  "type": "Equipment",
  "name": "Adaga",
  "concept": "weapon",
  "updated_at": "2023-01-01T00:00:00.000",
  "access": "complete",
  "cost": 200,
  "damage": "1d4",
  "bonus_ca": null,
  "weight_in_load": 1,
  "weight_in_grams": null,
  "description": "Pequena, Perfurante, Arremesso (9)\n",
  "fontes": [
    {
      "page": 58,
      "compact": false,
      "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
    }
  ],
  "url": "https://olddragon.com.br/equipamentos/adaga.json"
}
```
<!-- END equipment_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/equipamentos/adaga.json
```

###### Copiar como HTTPie

``` shell
http https://olddragon.com.br/equipamentos/adaga.json
```
