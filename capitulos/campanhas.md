Campanhas
=========

Endpoints:

- [Obter campanha específica](#obter-campanha-específica)

Obter campanha específica
------------------------

- `GET /campanhas/261ac8f6-6fbc-4b1e-be4a-6e5ee7d8e4b4.json` retorna a campanha específica para a ID informada (neste exemplo, a ID é `261ac8f6-6fbc-4b1e-be4a-6e5ee7d8e4b4`).

###### Exemplo de resposta JSON
<!-- START campaigns_show.json -->
```json
{
  "id": "261ac8f6-6fbc-4b1e-be4a-6e5ee7d8e4b4",
  "type": "Campaign",
  "title": "Bandeirantes de Valansia",
  "intro": "Em um mundo inexplorado, apenas os bravos se aventuram. Descubra os segredos de Valansia e torne-se um herói!\n",
  "created_at": "2023-01-01T00:00:00.000",
  "updated_at": "2023-01-01T00:00:00.000",
  "personagens": [
    {
      "id": "59a2adaf-96e6-4569-827b-a172982cf13c",
      "name": "Evendur",
      "level": 5,
      "health_points": 30,
      "max_hp": 30,
      "forca": 15,
      "destreza": 14,
      "constituicao": 12,
      "inteligencia": 10,
      "sabedoria": 9,
      "carisma": 9,
      "ac": 15,
      "created_at": "2023-01-01T00:00:00.000",
      "updated_at": "2023-01-01T00:00:00.000",
      "race": "humano",
      "class": "guerreiro",
      "url": "https://olddragon.com.br/personagens/59a2adaf-96e6-4569-827b-a172982cf13c.json"
    }
  ],
  "url": "https://olddragon.com.br/campanhas/261ac8f6-6fbc-4b1e-be4a-6e5ee7d8e4b4.json"
}
```
<!-- END campaigns_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/campanhas/261ac8f6-6fbc-4b1e-be4a-6e5ee7d8e4b4.json
```
