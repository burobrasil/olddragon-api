Campanhas
=========

Endpoints:

- [Obter campanha específica](#obter-campanha-específica)

Obter campanha específica
------------------------

- `GET /campanhas/c958955b-8211-42cf-94a5-8276a1b052d5.json` retorna a campanha específica para a ID informada (neste exemplo, a ID é `c958955b-8211-42cf-94a5-8276a1b052d5`).

###### Exemplo de resposta JSON
<!-- START campaigns_show.json -->
```json
{
  "data": {
    "id": "c958955b-8211-42cf-94a5-8276a1b052d5",
    "type": "campanhas",
    "attributes": {
      "title": "A Fortaleza Sombria",
      "intro": "",
      "created_at": "2023-07-30T23:01:17.108-03:00",
      "updated_at": "2023-07-30T23:01:17.108-03:00"
    },
    "relationships": {
      "personagens": [
        {
          "id": "972f362c-76ad-4a9b-8f08-749d9e3c09f4",
          "type": "personagens",
          "attributes": {
            "name": "Draco",
            "level": 10,
            "health_points": 8,
            "max_hp": 51,
            "forca": 14,
            "destreza": 15,
            "constituicao": 13,
            "inteligencia": 11,
            "sabedoria": 12,
            "carisma": 10,
            "mod_forca": 1,
            "mod_destreza": 2,
            "mod_constituicao": 1,
            "mod_inteligencia": 0,
            "mod_sabedoria": 0,
            "mod_carisma": 0,
            "ac": 14,
            "bac": 6,
            "bad": 7,
            "jpd": 14,
            "jpc": 12,
            "jps": 11,
            "current_movement": 6,
            "movement_run": 12,
            "movement_climb": 4,
            "movement_swim": 3,
            "created_at": "2023-07-26T22:24:54.106-03:00",
            "updated_at": "2023-08-08T10:49:54.894-03:00",
            "race": "elfo",
            "class": "assassino"
          },
          "links": {
            "self": "https://olddragon.com.br/personagens/972f362c-76ad-4a9b-8f08-749d9e3c09f4.json"
          }
        },
        {
          "id": "05f9e7bc-0dde-405b-ab5a-c0837325e30e",
          "type": "personagens",
          "attributes": {
            "name": "Iahel",
            "level": 10,
            "health_points": 10,
            "max_hp": 72,
            "forca": 17,
            "destreza": 11,
            "constituicao": 15,
            "inteligencia": 10,
            "sabedoria": 14,
            "carisma": 6,
            "mod_forca": 3,
            "mod_destreza": 0,
            "mod_constituicao": 2,
            "mod_inteligencia": 0,
            "mod_sabedoria": 1,
            "mod_carisma": -1,
            "ac": 16,
            "bac": 13,
            "bad": 10,
            "jpd": 11,
            "jpc": 14,
            "jps": 12,
            "current_movement": 6,
            "movement_run": 12,
            "movement_climb": 4,
            "movement_swim": 3,
            "created_at": "2023-07-26T22:23:37.900-03:00",
            "updated_at": "2023-08-03T00:44:44.588-03:00",
            "race": "humano",
            "class": "paladino"
          },
          "links": {
            "self": "https://olddragon.com.br/personagens/05f9e7bc-0dde-405b-ab5a-c0837325e30e.json"
          }
        }
      ]
    },
    "links": {
      "self": "https://olddragon.com.br/campanhas/c958955b-8211-42cf-94a5-8276a1b052d5.json"
    }
  }
}
```
<!-- END campaigns_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/campanhas/c958955b-8211-42cf-94a5-8276a1b052d5.json
```
