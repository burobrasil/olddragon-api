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
```json
{
  "data": [
    {
      "id": "abelha-diamante",
      "type": "monstros",
      "attributes": {
        "name": "Abelha-diamante",
        "flavor": "Abelhas gigantes (30cm) de temperamento agressivo. Constroem colmeias subterrâneas.",
        "concept": "animal",
        "size": "miudo",
        "habitats": [
          "desertos"
        ],
        "alignment": "neutro",
        "variant": false,
        "access": "limited"
      },
      "links": {
        "self": "https://olddragon.com.br/monstros/abelha-diamante.json"
      }
    },
    {
      "id": "abelhas-assassinas",
      "type": "monstros",
      "attributes": {
        "name": "Abelhas assassinas",
        "flavor": "Agressivas e venenosas, fazem colmeia nos subterrâneos e tocas.",
        "concept": "inseto",
        "size": "medio",
        "habitats": [],
        "alignment": "neutro",
        "variant": false,
        "access": "limited"
      },
      "links": {
        "self": "https://olddragon.com.br/monstros/abelhas-assassinas.json"
      }
    }
  ],
  "links": {
    "first": "/monstros.json?page=1",
    "self": "/monstros.json?page=1",
    "next": "/monstros.json?page=2",
    "last": "/monstros.json?page=20"
  },
  "meta": {
    "pages": 20,
    "count": 400
  }
}
```
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
```json
{
  "data": {
    "id": "orc",
    "type": "monstros",
    "attributes": {
      "name": "Orc",
      "flavor": "Selvagens e brutais, visam a expansão de seus territórios por meio de invasões e constantes ataques aos outros povos.",
      "concept": "humanoide",
      "size": "medio",
      "habitats": ["qualquer"],
      "alignment": "caotico",
      "variant": false,
      "access": "partial",
      "description": "  * **Classe de armadura**: possuem CA 11 ou 14 quando usam armadura de couro e escudo.\n\n  * **Infravisão**: 18 metros.",
      "encounters": "2d4",
      "encounters_lair": "1d6x10",
      "xp": "15",
      "treasure": "s",
      "treasure_lair": "b+c",
      "mv": 9,
      "mvc": null,
      "mve": null,
      "mvn": null,
      "mvv": null,
      "mvo": null,
      "dv_bonus": "+1",
      "pv": "6",
      "ca": "11/14",
      "jp": "5",
      "mo": 9,
      "dv": "1",
      "described_attacks": ["1 × arma + 3 (arma + 0)"]
    },
    "links": {
      "self": "https://olddragon.com.br/monstros/orc.json"
    }
  }
}

```
<!-- END monsters_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/monstros/orc.json
```
