Personagens
===========

Endpoints:

- [Obter personagem específico](#obter-personagem-específico)

Obter personagem específico
---------------------------

* `GET /personagens/972f362c-76ad-4a9b-8f08-749d9e3c09f4.json` retorna o personagem específica para a ID informada.

###### Exemplo de resposta JSON
<!-- START GET /personagens/example.json -->
```json
{
  "data": {
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
  }
}
```
<!-- END GET /personagens/example.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/personagens/972f362c-76ad-4a9b-8f08-749d9e3c09f4.json
```
