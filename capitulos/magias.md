Magias
======

Endpoints:

- [Listar magias](#listar-magias)
- [Obter magia específico](#obter-magia-específico)

Listar magias
-------------

- `GET /magias.json` retorna todos os magias.

_Parâmetros opcionais de URL_:

- `circles[]` - filtragem com lista (_array_) dos círculos da magia. Caso a magia possua mais de um círculo (como "Ampliar Plantas", que é Arcana de 4o cículo e Divina de 3o círculo), será considerado o círculo menor das magias filtradas no parâmetro `schools[]` (ou de todas caso não esteja presente). Opções são `1o`, `2o`, `3o`, `4o`, `5o`, `6o`, `7o`, `8o`, `9o`. Vários podem ser informados para retornar de mais de um círculo de magia ao mesmo tempo.
- `ids[]` - Lista de IDs de magias. Exemplo: `ids[]=ajuda&ids[]=luz`.
- `name` - filtragem parcial pelo nome. Por exemplo, se for passado `abe`, serão retornadas as magias "Abençoar" e "Arma Abençoada".
- `order` - ordena a lista. Opções são `name` (padrão), `reverse_name`, `circle`, `reverse_circle`.
- `schools[]` - filtragem com lista (_array_) das escolas de magias. Opções são `arcane` (Arcana), `divine` (Divina), `necromancer` (Necromante), e `illusionist` (Ilusionista). Deixe em branco ou sem este parâmetro para retornar de todas as escolas de magia. Várias podem ser informadas para retornar de mais de uma escola ao mesmo tempo.
- `sources[]` - filtragem com lista (_array_) das fontes das magias. O ID do livro (como `c520caa7-e1de-4919-b273-190be862f4eb` para o LB1) deve ser informado para referenciar o livro. Vários podem ser informados para retornar de mais de um livro ao mesmo tempo.

###### Exemplo de resposta JSON
<!-- START spells_index.json -->
```json
[
  {
    "id": "ajuda",
    "type": "Spell",
    "name": "Ajuda",
    "arcane": null,
    "divine": 2,
    "necromancer": null,
    "illusionist": null,
    "updated_at": "2023-01-01T00:00:00.000",
    "reverse": false,
    "access": "complete",
    "range": "toque",
    "duration": "2 turnos",
    "jp": "nenhuma",
    "description": "Esta magia concede uma ajuda de sua divindade, anulando a perda de até 1d4 pontos de vida +1 a cada 2 níveis do conjurador, do próximo dano sofrido pelo conjurador. Pontos de vida anulados que sobram após o próximo dano recebido pelo conjurador, devem ser descartados.\n",
    "fontes": [
      {
        "page": 105,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      }
    ],
    "url": "https://olddragon.com.br/magias/ajuda.json"
  },
  {
    "id": "escuridao",
    "type": "Spell",
    "name": "Escuridão",
    "arcane": 1,
    "divine": null,
    "necromancer": null,
    "illusionist": null,
    "updated_at": "2023-01-01T00:00:00.000",
    "reverse": true,
    "access": "complete",
    "range": "especial",
    "duration": "12 turnos",
    "jp": "JPS nega",
    "description": "O objeto alvo tocado produz luz tão brilhante quanto uma tocha, iluminando uma área com raio de 6 metros.\n\nSe conjurada nos olhos de um alvo a até 3m + 1,5m/nível do conjurador, a vítima que não passar em uma JPS fica cega até o final da duração da magia. Neste caso, a luz mágica se apaga e não causa nenhum outro efeito.\n\n[Escuridão] é a versão reversa que permite interromper qualquer fonte de luz, apagando tochas, velas, lâmpadas ou até mesmo dissipando uma magia Luz lançada anteriormente e criando uma área de 4,5 metros de raio de escuridão mágica, deixando todos dentro da área cegos (mesmo se possuírem Infravisão).\n\nSe conjurada nos olhos de um alvo tocado pelo conjurador, a vítima que não passar em uma JPS fica cega até o final da duração da magia.  Neste caso, a escuridão mágica some e não causa nenhum outro efeito.\n",
    "reverse_spell": {
      "id": "luz",
      "name": "Luz",
      "reverse_spell_url": "https://olddragon.com.br/magias/luz.json"
    },
    "fontes": [
      {
        "page": 119,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      }
    ],
    "url": "https://olddragon.com.br/magias/escuridao.json"
  },
  {
    "id": "ilusao",
    "type": "Spell",
    "name": "Ilusão",
    "arcane": null,
    "divine": null,
    "necromancer": null,
    "illusionist": 1,
    "updated_at": "2023-01-01T00:00:00.000",
    "reverse": false,
    "access": "complete",
    "range": "especial",
    "duration": "especial",
    "jp": "JPS nega",
    "description": "Enquanto concentrado, o conjurador cria a ilusão de uma criatura, objeto ou cena, desde que já tenha a visto anteriormente. A Ilusão é apenas visual e, apesar de possuir movimentos, não emite sons, não possui cheiro e não irradia temperatura.\n\nSe não for usada para criar um falso ataque, a ilusão desaparecerá ao ser tocada. Se usada para atacar ou simular um ataque, o alvo poderá realizar uma JPS para negar os efeitos da ilusão.\n\nA Ilusão criada possui CA 11, o mesmo BA do conjurador e desaparece após a concentração do conjurador ser interrompida ou ao ser atingida com sucesso em combate.\n\nUma ilusão nunca causa dano real. Ao ser “morto” por uma ilusão, o oponente ficará inconsciente por 1d4 rodadas.\n",
    "fontes": [
      {
        "page": 117,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      }
    ],
    "url": "https://olddragon.com.br/magias/ilusao.json"
  },
  {
    "id": "luz",
    "type": "Spell",
    "name": "Luz",
    "arcane": 1,
    "divine": 1,
    "necromancer": null,
    "illusionist": null,
    "updated_at": "2023-01-01T00:00:00.000",
    "reverse": true,
    "access": "complete",
    "range": "especial",
    "duration": "12 turnos",
    "jp": "JPS nega",
    "description": "O objeto alvo tocado produz luz tão brilhante quanto uma tocha, iluminando uma área com raio de 6 metros.\n\nSe conjurada nos olhos de um alvo a até 3m + 1,5m/nível do conjurador, a vítima que não passar em uma JPS fica cega até o final da duração da magia. Neste caso, a luz mágica se apaga e não causa nenhum outro efeito.\n\n[Escuridão] é a versão reversa que permite interromper qualquer fonte de luz, apagando tochas, velas, lâmpadas ou até mesmo dissipando uma magia Luz lançada anteriormente e criando uma área de 4,5 metros de raio de escuridão mágica, deixando todos dentro da área cegos (mesmo se possuírem Infravisão).\n\nSe conjurada nos olhos de um alvo tocado pelo conjurador, a vítima que não passar em uma JPS fica cega até o final da duração da magia.  Neste caso, a escuridão mágica some e não causa nenhum outro efeito.\n",
    "reverse_spell": {
      "id": "escuridao",
      "name": "Escuridão",
      "reverse_spell_url": "https://olddragon.com.br/magias/escuridao.json"
    },
    "fontes": [
      {
        "page": 119,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      }
    ],
    "url": "https://olddragon.com.br/magias/luz.json"
  }
]
```
<!-- END spells_index.json -->
###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/magias.json
```

###### Copiar como HTTPie

``` shell
http https://olddragon.com.br/magias.json
```

Obter magia específica
----------------------

- `GET /magias/luz.json` retorna a magia específica para a ID informada (neste exemplo, a ID é `luz`).

###### Exemplo de resposta JSON
<!-- START spells_show.json -->
```json
{
  "id": "luz",
  "type": "Spell",
  "name": "Luz",
  "arcane": 1,
  "divine": 1,
  "necromancer": null,
  "illusionist": null,
  "updated_at": "2023-01-01T00:00:00.000",
  "reverse": true,
  "access": "complete",
  "range": "especial",
  "duration": "12 turnos",
  "jp": "JPS nega",
  "description": "O objeto alvo tocado produz luz tão brilhante quanto uma tocha, iluminando uma área com raio de 6 metros.\n\nSe conjurada nos olhos de um alvo a até 3m + 1,5m/nível do conjurador, a vítima que não passar em uma JPS fica cega até o final da duração da magia. Neste caso, a luz mágica se apaga e não causa nenhum outro efeito.\n\n[Escuridão] é a versão reversa que permite interromper qualquer fonte de luz, apagando tochas, velas, lâmpadas ou até mesmo dissipando uma magia Luz lançada anteriormente e criando uma área de 4,5 metros de raio de escuridão mágica, deixando todos dentro da área cegos (mesmo se possuírem Infravisão).\n\nSe conjurada nos olhos de um alvo tocado pelo conjurador, a vítima que não passar em uma JPS fica cega até o final da duração da magia.  Neste caso, a escuridão mágica some e não causa nenhum outro efeito.\n",
  "reverse_spell": {
    "id": "escuridao",
    "name": "Escuridão",
    "reverse_spell_url": "https://olddragon.com.br/magias/escuridao.json"
  },
  "fontes": [
    {
      "page": 119,
      "compact": false,
      "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
    }
  ],
  "url": "https://olddragon.com.br/magias/luz.json"
}
```
<!-- END spells_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/magias/luz.json
```

###### Copiar como HTTPie

``` shell
http https://olddragon.com.br/magias/luz.json
```

### Observações sobre atributos

Os atributos `reverse` e `reverse_spell` denotam que esta magia possui uma versão reversa. Por exemplo, a magia [Luz](https://olddragon.com.br/magias/luz) retorna `reverse: true` e com `reverse_spell` apontando para a sua magia reversa [Escuridão](https://olddragon.com.br/magias/escuridao).

O atributo `access` é explicado em [Acesso](https://github.com/burobrasil/olddragon-api/blob/master/capitulos/acesso.md#acesso).
