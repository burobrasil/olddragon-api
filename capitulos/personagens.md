Personagens
===========

Endpoints:

- [Obter personagem específico](#obter-personagem-específico)

Obter personagem específico
---------------------------

- `GET /personagens/59a2adaf-96e6-4569-827b-a172982cf13c.json` retorna o personagem específica para a ID informada (neste exemplo, a ID é `59a2adaf-96e6-4569-827b-a172982cf13c`).

###### Exemplo de resposta JSON
<!-- START characters_show.json -->
```json
{
  "id": "59a2adaf-96e6-4569-827b-a172982cf13c",
  "name": "Guert",
  "level": 1,
  "created_at": "2023-01-01T00:00:00.000",
  "updated_at": "2023-01-01T00:00:00.000",
  "health_points": 10,
  "max_hp": 10,
  "forca": 10,
  "destreza": 10,
  "constituicao": 10,
  "inteligencia": 10,
  "sabedoria": 10,
  "carisma": 10,
  "mod_forca": 0,
  "mod_destreza": 0,
  "mod_constituicao": 0,
  "mod_inteligencia": 0,
  "mod_sabedoria": 0,
  "mod_carisma": 0,
  "ac": 10,
  "bac": 1,
  "bad": 1,
  "jpd": 5,
  "jpc": 6,
  "jps": 5,
  "current_movement": 9,
  "movement_run": 18,
  "movement_climb": 7,
  "movement_swim": 4,
  "race": "humano",
  "class": "guerreiro",
  "campanha_url": "https://olddragon.com.br/campanhas/261ac8f6-6fbc-4b1e-be4a-6e5ee7d8e4b4.json",
  "url": "https://olddragon.com.br/personagens/59a2adaf-96e6-4569-827b-a172982cf13c.json"
}
```
<!-- END characters_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/personagens/59a2adaf-96e6-4569-827b-a172982cf13c.json
```
