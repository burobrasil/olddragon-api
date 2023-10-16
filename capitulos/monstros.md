Monstros
========

Endpoints:

- [Listar monstros](#listar-monstros)
- [Obter monstro específico](#obter-monstro-específico)

Listar monstros
--------------

* `GET /monstros.json` retorna todos os monstros.

###### Exemplo de resposta JSON
<!-- START monsters_index.json -->
[
  {
    "id": "abelhas-assassinas",
    "name": "Abelhas assassinas",
    "flavor": "Agressivas e venenosas, fazem colmeia nos subterrâneos e tocas.",
    "concept": "inseto",
    "size": "medio",
    "habitats": [

    ],
    "alignment": "neutro",
    "variant": false,
    "access": "limited",
    "fontes": [

    ],
    "url": "https://olddragon.com.br/monstros/abelhas-assassinas.json"
  },
  {
    "id": "orc",
    "name": "Orc",
    "flavor": "Selvagens e brutais, visam a expansão de seus territórios por meio de invasões e constantes ataques aos outros povos.",
    "concept": "humanoide",
    "size": "medio",
    "habitats": [
      "qualquer"
    ],
    "alignment": "caotico",
    "variant": false,
    "access": "limited",
    "fontes": [

    ],
    "url": "https://olddragon.com.br/monstros/orc.json"
  }
]
<!-- END monsters_index.json -->
###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/monstros.json
```

Obter monstro específico
------------------------

- `GET /monstros/orc.json` retorna o monstro específico para a ID informada (neste exemplo, a ID é `orc`).

###### Exemplo de resposta JSON
<!-- START monsters_show.json -->
{
  "id": "orc",
  "name": "Orc",
  "flavor": "Selvagens e brutais, visam a expansão de seus territórios por meio de invasões e constantes ataques aos outros povos.",
  "concept": "humanoide",
  "size": "medio",
  "habitats": [
    "qualquer"
  ],
  "alignment": "caotico",
  "variant": false,
  "access": "limited",
  "fontes": [

  ],
  "url": "https://olddragon.com.br/monstros/orc.json"
}
<!-- END monsters_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/monstros/orc.json
```
