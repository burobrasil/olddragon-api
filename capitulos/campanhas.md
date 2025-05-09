Campanhas
=========

Endpoints:

- [Listar campanhas](#listar-campanhas)
- [Obter campanha específica](#obter-campanha-específica)
- [Listar personagens em uma campanha](#listar-personagens-em-uma-campanha)

Listar classes
--------------

* `GET /campanhas.json` retorna todas as campanhas do usuário autenticado.

_Parâmetros opcionais de URL_:

* `ids[]` - Lista de IDs de campanhas. Exemplo: `ids[]=261ac8f6-6fbc-4b1e-be4a-6e5ee7d8e4b4&ids[]=261ac8f6-6fbc-4b1e-be4a-6e5ee7d8e4b5`.

###### Exemplo de resposta JSON
<!-- START campaigns_index.json -->
```json
[
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
]
```
<!-- END campaigns_index.json -->
###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/campanhas.json
```

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

Listar personagens em uma campanha
----------------------------------

- `GET /campanhas/261ac8f6-6fbc-4b1e-be4a-6e5ee7d8e4b4/personagens.json` retorna todos os personagens em uma campanha específica para a ID informada (neste exemplo, a ID é `261ac8f6-6fbc-4b1e-be4a-6e5ee7d8e4b4`).

###### Exemplo de resposta JSON
<!-- START campaigns_characters_index.json -->
```json
[
  {
    "id": "59a2adaf-96e6-4569-827b-a172982cf13c",
    "name": "Evendur",
    "level": 5,
    "created_at": "2023-01-01T00:00:00.000",
    "updated_at": "2023-01-01T00:00:00.000",
    "health_points": 30,
    "max_hp": 30,
    "injuries": 0,
    "forca": 15,
    "destreza": 14,
    "constituicao": 12,
    "inteligencia": 10,
    "sabedoria": 9,
    "carisma": 9,
    "mod_forca": 2,
    "mod_destreza": 1,
    "mod_constituicao": 0,
    "mod_inteligencia": 0,
    "mod_sabedoria": 0,
    "mod_carisma": 0,
    "ac": 15,
    "bac": 7,
    "bad": 6,
    "jpd": 9,
    "jpc": 8,
    "jps": 8,
    "current_movement": 9,
    "movement_run": 18,
    "movement_climb": 7,
    "movement_swim": 4,
    "infravision": 0,
    "experience_points": 11520,
    "race_jp": "none",
    "money_gp": 0,
    "money_sp": 0,
    "money_cp": 0,
    "alignment": "neutro",
    "languages": [
      "Comum",
      "Anão"
    ],
    "appearance": "Bonito (Corpo); Cabelos curtos (Cabelos); Barba fechada (Geral)",
    "personality": "Humilde (Sobre todo o resto); Calmo (Sobre si mesmo); Extrovertido (Sobre outras pessoas)",
    "background": "Filho de um ferreiro das montanhas do norte de Valansia, Evendur aprendeu desde cedo o valor da honra e força em batalha.Depois de perder seu grupo de amigos, vagou até conhecer Dorgauth, o anão guerreiro, que se tornou seu irmão-em-armas e o incentivou a viver e ganhar glórias para honrar seus amigos mortos.",
    "notes": "",
    "inventory_items": [
      {
        "position": 0,
        "quantity": 2,
        "equipped": false,
        "equippable?": false,
        "name": "Tocha",
        "concept": "misc",
        "cost": 100,
        "total_cost": 200,
        "weight_in_load": null,
        "weight_in_grams": 500,
        "sum_weight_in_grams": 1000,
        "description": "5 unidades.",
        "magic_item": false,
        "damage_type": "none",
        "damage": null,
        "bonus_ca": null,
        "bonus_damage": null,
        "increases_load_by": null,
        "shoot_range": null,
        "throw_range": null,
        "arrow": false,
        "bolt": false,
        "bolt_small": false,
        "counter_attack": false,
        "mounted": false,
        "polearm": false,
        "recharge": false,
        "two_handed": false,
        "versatile": false,
        "wooden": false,
        "bonus_ba": null
      },
      {
        "position": 1,
        "quantity": 1,
        "equipped": true,
        "equippable?": true,
        "name": "Espada Longa",
        "concept": "weapon",
        "cost": 1000,
        "total_cost": 1000,
        "weight_in_load": 2,
        "weight_in_grams": null,
        "sum_weight_in_grams": 2000,
        "description": "Média, Cortante.",
        "magic_item": false,
        "damage_type": "slashing",
        "damage": "1d8",
        "bonus_ca": null,
        "bonus_damage": null,
        "increases_load_by": null,
        "shoot_range": null,
        "throw_range": null,
        "arrow": false,
        "bolt": false,
        "bolt_small": false,
        "counter_attack": false,
        "mounted": false,
        "polearm": false,
        "recharge": false,
        "two_handed": false,
        "versatile": false,
        "wooden": false,
        "bonus_ba": null
      },
      {
        "position": 2,
        "quantity": 1,
        "equipped": true,
        "equippable?": true,
        "name": "Espada Curta",
        "concept": "weapon",
        "cost": 600,
        "total_cost": 600,
        "weight_in_load": 1,
        "weight_in_grams": null,
        "sum_weight_in_grams": 1000,
        "description": "Pequena, Cortante.",
        "magic_item": false,
        "damage_type": "slashing",
        "damage": "1d6",
        "bonus_ca": null,
        "bonus_damage": null,
        "increases_load_by": null,
        "shoot_range": null,
        "throw_range": null,
        "arrow": false,
        "bolt": false,
        "bolt_small": false,
        "counter_attack": false,
        "mounted": false,
        "polearm": false,
        "recharge": false,
        "two_handed": false,
        "versatile": false,
        "wooden": false,
        "bonus_ba": null
      },
      {
        "position": 3,
        "quantity": 1,
        "equipped": true,
        "equippable?": true,
        "name": "Cota de Malha",
        "concept": "armor",
        "cost": 6000,
        "total_cost": 6000,
        "weight_in_load": 2,
        "weight_in_grams": null,
        "sum_weight_in_grams": 2000,
        "description": "Média, Metal.",
        "magic_item": false,
        "damage_type": "none",
        "damage": null,
        "bonus_ca": 4,
        "bonus_damage": null,
        "increases_load_by": null,
        "shoot_range": null,
        "throw_range": null,
        "arrow": false,
        "bolt": false,
        "bolt_small": false,
        "counter_attack": false,
        "mounted": false,
        "polearm": false,
        "recharge": false,
        "two_handed": false,
        "versatile": false,
        "wooden": false,
        "bonus_ba": null
      },
      {
        "position": 4,
        "quantity": 1,
        "equipped": false,
        "equippable?": false,
        "name": "Mochila",
        "concept": "container",
        "cost": 200,
        "total_cost": 200,
        "weight_in_load": null,
        "weight_in_grams": null,
        "sum_weight_in_grams": 0,
        "description": "De couro, com compartimentos para exploradores e reforço para peso. Adiciona 5 ao valor de carga do personagem. Comporta até 400 moedas.",
        "magic_item": false,
        "damage_type": "none",
        "damage": null,
        "bonus_ca": null,
        "bonus_damage": null,
        "increases_load_by": 5,
        "shoot_range": null,
        "throw_range": null,
        "arrow": false,
        "bolt": false,
        "bolt_small": false,
        "counter_attack": false,
        "mounted": false,
        "polearm": false,
        "recharge": false,
        "two_handed": false,
        "versatile": false,
        "wooden": false,
        "bonus_ba": null
      },
      {
        "position": 5,
        "quantity": 1,
        "equipped": false,
        "equippable?": false,
        "name": "Corda de Cânhamo",
        "concept": "misc",
        "cost": 100,
        "total_cost": 100,
        "weight_in_load": null,
        "weight_in_grams": 2000,
        "sum_weight_in_grams": 2000,
        "description": "15 metros. Suporta erguer até 250 kg.",
        "magic_item": false,
        "damage_type": "none",
        "damage": null,
        "bonus_ca": null,
        "bonus_damage": null,
        "increases_load_by": null,
        "shoot_range": null,
        "throw_range": null,
        "arrow": false,
        "bolt": false,
        "bolt_small": false,
        "counter_attack": false,
        "mounted": false,
        "polearm": false,
        "recharge": false,
        "two_handed": false,
        "versatile": false,
        "wooden": false,
        "bonus_ba": null
      },
      {
        "position": 6,
        "quantity": 1,
        "equipped": false,
        "equippable?": false,
        "name": "Pederneira",
        "concept": "misc",
        "cost": 5,
        "total_cost": 5,
        "weight_in_load": null,
        "weight_in_grams": null,
        "sum_weight_in_grams": 0,
        "description": "Gera faíscas para acender pavios, lanternas ou fogueiras.",
        "magic_item": false,
        "damage_type": "none",
        "damage": null,
        "bonus_ca": null,
        "bonus_damage": null,
        "increases_load_by": null,
        "shoot_range": null,
        "throw_range": null,
        "arrow": false,
        "bolt": false,
        "bolt_small": false,
        "counter_attack": false,
        "mounted": false,
        "polearm": false,
        "recharge": false,
        "two_handed": false,
        "versatile": false,
        "wooden": false,
        "bonus_ba": null
      },
      {
        "position": 8,
        "quantity": 3,
        "equipped": false,
        "equippable?": false,
        "name": "Ração de viagem",
        "concept": "misc",
        "cost": 100,
        "total_cost": 300,
        "weight_in_load": null,
        "weight_in_grams": 500,
        "sum_weight_in_grams": 1500,
        "description": "Ração diária de comida para viagem para uma pessoa.",
        "magic_item": false,
        "damage_type": "none",
        "damage": null,
        "bonus_ca": null,
        "bonus_damage": null,
        "increases_load_by": null,
        "shoot_range": null,
        "throw_range": null,
        "arrow": false,
        "bolt": false,
        "bolt_small": false,
        "counter_attack": false,
        "mounted": false,
        "polearm": false,
        "recharge": false,
        "two_handed": false,
        "versatile": false,
        "wooden": false,
        "bonus_ba": null
      }
    ],
    "character_race_name": "Humano",
    "character_race_url": "https://olddragon.com.br/racas/humano.json",
    "character_class_name": "Guerreiro",
    "character_class_url": "https://olddragon.com.br/classes/guerreiro.json",
    "campaign_name": "Bandeirantes de Valansia",
    "campaign_url": "https://olddragon.com.br/campanhas/261ac8f6-6fbc-4b1e-be4a-6e5ee7d8e4b4.json",
    "url": "https://olddragon.com.br/personagens/59a2adaf-96e6-4569-827b-a172982cf13c.json"
  }
]
```
<!-- END campaigns_characters_index.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/campanhas/261ac8f6-6fbc-4b1e-be4a-6e5ee7d8e4b4/personagens.json
```
