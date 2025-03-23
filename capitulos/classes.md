Classes
========

Endpoints:

- [Listar classes](#listar-classes)
- [Obter classe específica](#obter-classe-específica)

Listar classes
--------------

* `GET /classes.json` retorna todos as classes.

###### Exemplo de resposta JSON
<!-- START character_classes_index.json -->
```json
[
  {
    "id": "guerreiro",
    "type": "CharacterClass",
    "name": "Guerreiro",
    "flavor": "Aventureiros especializados em combate, estão sempre na linha de frente e são mortais quando desembainham suas armas.",
    "armors_description": "Pode usar todas as armaduras.",
    "weapons_description": "Pode usar todas as armas.",
    "magic_items_description": "Não pode usar cajados, varinhas e pergaminhos mágicos com exceção dos pergaminhos de proteção.",
    "hp": 10,
    "high_level_hp_bonus": 2,
    "restrictions": {},
    "levels": {
      "1": {
        "ba": 1,
        "jp": 5
      },
      "2": {
        "ba": 2,
        "jp": 5,
        "xp": 2000
      },
      "3": {
        "ba": 3,
        "jp": 6,
        "xp": 4000
      },
      "4": {
        "ba": 4,
        "jp": 6,
        "xp": 7000
      },
      "5": {
        "ba": 5,
        "jp": 8,
        "xp": 10000
      },
      "6": {
        "ba": 6,
        "jp": 8,
        "xp": 20000
      },
      "7": {
        "ba": 7,
        "jp": 10,
        "xp": 30000
      },
      "8": {
        "ba": 8,
        "jp": 10,
        "xp": 40000
      },
      "9": {
        "ba": 9,
        "jp": 11,
        "xp": 50000
      },
      "10": {
        "ba": 10,
        "jp": 11,
        "xp": 100000
      },
      "11": {
        "ba": 11,
        "jp": 13,
        "xp": 200000
      },
      "12": {
        "ba": 12,
        "jp": 13,
        "xp": 300000
      },
      "13": {
        "ba": 13,
        "jp": 14,
        "xp": 400000
      },
      "14": {
        "ba": 14,
        "jp": 14,
        "xp": 500000
      },
      "15": {
        "ba": 15,
        "jp": 16,
        "xp": 600000
      }
    },
    "abilities": [
      {
        "level": 1,
        "name": "Aparar",
        "description": "Um Guerreiro pode, após receber um ataque físico que o atinja e antes da jogada de dano desse ataque, escolher sacrificar seu escudo ou uma arma que esteja portando para absorver todo o dano do ataque recebido.\n\nArmas e Escudos usados em um aparar ficarão inutilizados e danificados. Armas e Escudos mágicos possuem uma chance de 1-2 em 1d6 de se danificarem, reduzindo seus bônus (de ataque/defesa) em 1 de modo que um escudo +3 ao ser usado em um aparar, e se danificado, passa ter como bônus de defesa +2 e assim sucessivamente.\n\nUm item mágico que perder todos os bônus estará permanentemente destruído. Apenas ataques provenientes de inimigos grandes ou menores poderão ser aparados."
      },
      {
        "level": 1,
        "name": "Maestria em Arma",
        "description": "O Guerreiro se torna Mestre em uma arma à sua escolha, recebendo um bônus de +1 no dano daquela arma.",
        "level3": "O Guerreiro evolui sua maestria para uma segunda arma à sua escolha e melhora o bônus no dano de ambas as armas para +2.",
        "level10": "O Guerreiro evolui sua maestria para todas as armas semelhantes àquelas que ele já possui maestria, recebendo bônus em todas as armas pertencentes a estes grupos.\n\nOs grupos de armas disponíveis são: cortantes, perfurante, impactantes, disparos, hastes ou arremesso. Todas as armas desses grupos melhoram seus bônus de dano para +3.\n"
      },
      {
        "level": 6,
        "name": "Ataque Extra",
        "description": "Um Guerreiro no 6º nível adquire um segundo ataque, corpo a corpo ou à distância, com uma mesma arma na qual possua maestria.\n\nEste segundo ataque é realizado após o primeiro ataque, logo em sequência, antes da ação do próximo jogador na ordem da iniciativa com a mesma BA usada no primeiro ataque."
      },
      {
        "level": 11,
        "name": "Reputação",
        "description": "O Guerreiro de alto nível atinge um grau superior de reconhecimento pelos seus feitos, obtendo Reputação 1 em 1d6. O valor de Reputação evolui em 1 até o máximo de 1-5 em 1d6 no 15º nível."
      }
    ],
    "fontes": [
      {
        "page": 28,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      },
      {
        "page": null,
        "compact": true,
        "digital_item_url": "https://olddragon.com.br/livros/srd.json"
      }
    ],
    "url": "https://olddragon.com.br/classes/guerreiro.json"
  },
  {
    "id": "mago",
    "type": "CharacterClass",
    "name": "Mago",
    "flavor": "Aventureiro estudioso, especializado nas artes arcanas, dedicado a conjurar magias escritas em grimórios e pergaminhos.",
    "armors_description": "Nenhuma. Usar escudos ou armaduras impede a conjuração de magias e protegem apenas metade da CA normal.",
    "weapons_description": "Apenas pequenas. Armas grandes ou médias geram ataques difíceis para Magos.",
    "magic_items_description": "Podem usar todos os tipos.",
    "hp": 4,
    "high_level_hp_bonus": 1,
    "restrictions": {},
    "levels": {
      "1": {
        "ba": 0,
        "jp": 5
      },
      "2": {
        "ba": 1,
        "jp": 5,
        "xp": 2500
      },
      "3": {
        "ba": 1,
        "jp": 5,
        "xp": 5000
      },
      "4": {
        "ba": 1,
        "jp": 5,
        "xp": 8500
      },
      "5": {
        "ba": 2,
        "jp": 7,
        "xp": 11500
      },
      "6": {
        "ba": 2,
        "jp": 7,
        "xp": 23000
      },
      "7": {
        "ba": 2,
        "jp": 7,
        "xp": 33000
      },
      "8": {
        "ba": 3,
        "jp": 7,
        "xp": 43000
      },
      "9": {
        "ba": 3,
        "jp": 7,
        "xp": 53000
      },
      "10": {
        "ba": 3,
        "jp": 10,
        "xp": 106000
      },
      "11": {
        "ba": 4,
        "jp": 10,
        "xp": 210000
      },
      "12": {
        "ba": 4,
        "jp": 10,
        "xp": 320000
      },
      "13": {
        "ba": 4,
        "jp": 10,
        "xp": 430000
      },
      "14": {
        "ba": 5,
        "jp": 13,
        "xp": 540000
      },
      "15": {
        "ba": 5,
        "jp": 13,
        "xp": 650000
      }
    },
    "abilities": [
      {
        "level": 1,
        "name": "Magias Arcanas",
        "description": "Um Mago é capaz de lançar magias arcanas diariamente. Para memorizá-las, o Mago deve estudar seu livro de magias, o grimório, e decidir quais magias serão memorizadas naquele dia.\n\n**Grimório**: Livro no qual o Mago escreve sua coleção de magias, como um grande livro de receitas arcanas. Sem ele, um Mago perde a capacidade de memorizar novas magias. Por isso, um Mago zeloso guardará seu grimório como se fosse a própria vida.\n\n**Magias Iniciais**: No 1º nível, o grimório do Mago contém três magias de 1º círculo à escolha do Mago e uma magia escolhida aleatoriamente da sua lista de magias de 1º círculo.\n\n**Novas Magias**: Um Mago pode acrescentar livremente novas magias ao seu grimório copiando de outros grimórios ou de pergaminhos.\n\n**Círculos Superiores**: Um Mago pode escrever no grimório magias de círculos acima de sua capacidade, mas não pode memorizá-las até atingir o nível necessário."
      },
      {
        "level": 1,
        "name": "Ler Magias",
        "description": "Um Mago é capaz de uma vez ao dia por nível decifrar e ler inscrições mágicas em qualquer lugar, mesmo que não entenda a mensagem a qual elas querem passar.\n\nEsta habilidade não permite identificar as propriedades mágicas de um item mágico, nem é necessária para lançar magias escritas, mas permitirá identificar qual magia está escrita ali."
      },
      {
        "level": 1,
        "name": "Detectar Magias",
        "description": "Um Mago é capaz de uma vez ao dia por nível perceber em lugares, pessoas ou coisas em uma área de até 9m + 3m por nível, a presença de magia, desde que esteja concentrado e procurando ativamente por isso.\n\nO Mago percebe uma tênue aura mágica ao redor dos lugares, pessoas ou coisas encantadas, mas não é capaz de identificar a magia, o nível de poder do conjurador ou o efeito presente no alvo.\n\nUm Mago precisa se concentrar 1d8 rodadas na área desejada para conseguir detectar, caso haja, alguma presença mágica. Esse tempo cai para 1d4 rodadas no 6º nível e para 1 rodada no 10º nível."
      },
      {
        "level": 11,
        "name": "Reputação",
        "description": "O Mago de alto nível atinge um grau superior de reconhecimento pelos seus feitos, obtendo Reputação 1 em 1d6. O valor de Reputação evolui em 1 até o máximo de 1-5 em 1d6 no 15º nível."
      }
    ],
    "fontes": [
      {
        "page": 42,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      },
      {
        "page": null,
        "compact": true,
        "digital_item_url": "https://olddragon.com.br/livros/srd.json"
      }
    ],
    "url": "https://olddragon.com.br/classes/mago.json"
  },
  {
    "id": "necromante",
    "type": "CharacterClass",
    "name": "Necromante",
    "flavor": "O Necromante é um estudioso dos fatos obscuros os quais cercam a vida e a morte, estudando as energias místicas que interferem nos efeitos destes conceitos sobre os seres vivos ou não.",
    "armors_description": "Nenhuma. Usar escudos ou armaduras impede a conjuração de magias e protegem apenas metade da CA normal.",
    "weapons_description": "Apenas pequenas. Armas grandes ou médias geram ataques difíceis para Necromantes.",
    "magic_items_description": "Podem usar todos os tipos.",
    "hp": 4,
    "high_level_hp_bonus": 1,
    "restrictions": {},
    "levels": {
      "1": {
        "ba": 0,
        "jp": 5
      },
      "2": {
        "ba": 1,
        "jp": 5,
        "xp": 3000
      },
      "3": {
        "ba": 1,
        "jp": 5,
        "xp": 6000
      },
      "4": {
        "ba": 1,
        "jp": 5,
        "xp": 10000
      },
      "5": {
        "ba": 2,
        "jp": 7,
        "xp": 13000
      },
      "6": {
        "ba": 2,
        "jp": 7,
        "xp": 26000
      },
      "7": {
        "ba": 2,
        "jp": 7,
        "xp": 36000
      },
      "8": {
        "ba": 3,
        "jp": 7,
        "xp": 46000
      },
      "9": {
        "ba": 3,
        "jp": 7,
        "xp": 56000
      },
      "10": {
        "ba": 3,
        "jp": 10,
        "xp": 112000
      },
      "11": {
        "ba": 4,
        "jp": 10,
        "xp": 220000
      },
      "12": {
        "ba": 4,
        "jp": 10,
        "xp": 340000
      },
      "13": {
        "ba": 4,
        "jp": 10,
        "xp": 460000
      },
      "14": {
        "ba": 5,
        "jp": 13,
        "xp": 580000
      },
      "15": {
        "ba": 5,
        "jp": 13,
        "xp": 700000
      }
    },
    "abilities": [
      {
        "level": 1,
        "name": "Magias Arcanas",
        "description": "Um Necromante é capaz de lançar magias arcanas diariamente. Para memorizá-las, o Necromante deve estudar seu livro de magias, o grimório, e decidir quais magias serão memorizadas naquele dia.\n\n**Grimório**: Livro no qual o Necromante escreve sua coleção de magias, como um grande livro de receitas arcanas. Sem ele, um Necromante perde a capacidade de memorizar novas magias. Por isso, um Necromante zeloso guardará seu grimório como se fosse a própria vida.\n\n**Magias Iniciais**: No 1º nível, o grimório do Necromante contém três magias de 1º círculo à escolha do Mago e uma magia escolhida aleatoriamente da sua lista de magias de 1º círculo.\n\n**Novas Magias**: Um Necromante pode acrescentar livremente novas magias ao seu grimório copiando de outros grimórios ou de pergaminhos.\n\n**Círculos Superiores**: Um Necromante pode escrever no grimório magias de círculos acima de sua capacidade, mas não pode memorizá-las até atingir o nível necessário."
      },
      {
        "level": 1,
        "name": "Ler Magias",
        "description": "Um Necromante é capaz de uma vez ao dia por nível decifrar e ler inscrições mágicas em qualquer lugar, mesmo que não entenda a mensagem a qual elas querem passar.\n\nEsta habilidade não permite identificar as propriedades mágicas de um item mágico, nem é necessária para lançar magias escritas, mas permitirá identificar qual magia está escrita ali."
      },
      {
        "level": 1,
        "name": "Detectar Magias",
        "description": "Um Necromante é capaz de uma vez ao dia por nível perceber em lugares, pessoas ou coisas em uma área de até 9m + 3m por nível, a presença de magia, desde que esteja concentrado e procurando ativamente por isso.\n\nO Necromante percebe uma tênue aura mágica ao redor dos lugares, pessoas ou coisas encantadas, mas não é capaz de identificar a magia, o nível de poder do conjurador ou o efeito presente no alvo.\n\nUm Necromante precisa se concentrar 1d8 rodadas na área desejada para conseguir detectar, caso haja, alguma presença mágica. Esse tempo cai para 1d4 rodadas no 6º nível e para 1 rodada no 10º nível."
      },
      {
        "level": 1,
        "name": "Magias Exclusivas",
        "description": "O Necromante escreve em seu grimório, Toque Sombrio e Aterrorizar, exclusivas para Necromantes.\n\n- **Sem Memorizar**: Magias exclusivas não precisam ser memorizadas para serem conjuradas pelo Necromante.\n- **Usos por dia**: Cada magia exclusiva do Necromante em seu grimório pode ser usada até uma vez ao dia, adicionalmente às magias diárias do Necromante.\n- **Usos Adicionais**: Caso outros usos sejam realizados, a magia exclusiva consumirá o espaço ocupado na memória do Necromante por outra magia já previamente memorizada.\n- **Jogada de Proteção**: Todas as Jogadas de Proteção contra as magias exclusivas são realizadas com um teste difícil."
      },
      {
        "level": 3,
        "name": "Criar Mortos-Vivos",
        "description": "O Necromante escreve esta magia exclusiva em seu grimório."
      },
      {
        "level": 6,
        "name": "Drenar Vida",
        "description": "O Necromante escreve esta magia exclusiva em seu grimório."
      },
      {
        "level": 10,
        "name": "Magia da Morte",
        "description": "O Necromante escreve esta magia exclusiva em seu grimório."
      },
      {
        "level": 11,
        "name": "Reputação",
        "description": "O Necromante de alto nível atinge um grau superior de reconhecimento pelos seus feitos, obtendo Reputação 1 em 1d6. O valor de Reputação evolui em 1 até o máximo de 1-5 em 1d6 no 15º nível."
      }
    ],
    "fontes": [
      {
        "page": 45,
        "compact": false,
        "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
      },
      {
        "page": null,
        "compact": true,
        "digital_item_url": "https://olddragon.com.br/livros/srd.json"
      }
    ],
    "parent_class_url": "https://olddragon.com.br/classes/mago.json",
    "url": "https://olddragon.com.br/classes/necromante.json"
  }
]
```
<!-- END character_classes_index.json -->
###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/classes.json
```

Obter classe específica
------------------------

- `GET /classes/necromante.json` retorna a classe específica para a ID informada (neste exemplo, a ID é `necromante`).

###### Exemplo de resposta JSON
<!-- START character_classes_show.json -->
```json
{
  "id": "necromante",
  "type": "CharacterClass",
  "name": "Necromante",
  "flavor": "O Necromante é um estudioso dos fatos obscuros os quais cercam a vida e a morte, estudando as energias místicas que interferem nos efeitos destes conceitos sobre os seres vivos ou não.",
  "armors_description": "Nenhuma. Usar escudos ou armaduras impede a conjuração de magias e protegem apenas metade da CA normal.",
  "weapons_description": "Apenas pequenas. Armas grandes ou médias geram ataques difíceis para Necromantes.",
  "magic_items_description": "Podem usar todos os tipos.",
  "hp": 4,
  "high_level_hp_bonus": 1,
  "restrictions": {},
  "levels": {
    "1": {
      "ba": 0,
      "jp": 5
    },
    "2": {
      "ba": 1,
      "jp": 5,
      "xp": 3000
    },
    "3": {
      "ba": 1,
      "jp": 5,
      "xp": 6000
    },
    "4": {
      "ba": 1,
      "jp": 5,
      "xp": 10000
    },
    "5": {
      "ba": 2,
      "jp": 7,
      "xp": 13000
    },
    "6": {
      "ba": 2,
      "jp": 7,
      "xp": 26000
    },
    "7": {
      "ba": 2,
      "jp": 7,
      "xp": 36000
    },
    "8": {
      "ba": 3,
      "jp": 7,
      "xp": 46000
    },
    "9": {
      "ba": 3,
      "jp": 7,
      "xp": 56000
    },
    "10": {
      "ba": 3,
      "jp": 10,
      "xp": 112000
    },
    "11": {
      "ba": 4,
      "jp": 10,
      "xp": 220000
    },
    "12": {
      "ba": 4,
      "jp": 10,
      "xp": 340000
    },
    "13": {
      "ba": 4,
      "jp": 10,
      "xp": 460000
    },
    "14": {
      "ba": 5,
      "jp": 13,
      "xp": 580000
    },
    "15": {
      "ba": 5,
      "jp": 13,
      "xp": 700000
    }
  },
  "abilities": [
    {
      "level": 1,
      "name": "Magias Arcanas",
      "description": "Um Necromante é capaz de lançar magias arcanas diariamente. Para memorizá-las, o Necromante deve estudar seu livro de magias, o grimório, e decidir quais magias serão memorizadas naquele dia.\n\n**Grimório**: Livro no qual o Necromante escreve sua coleção de magias, como um grande livro de receitas arcanas. Sem ele, um Necromante perde a capacidade de memorizar novas magias. Por isso, um Necromante zeloso guardará seu grimório como se fosse a própria vida.\n\n**Magias Iniciais**: No 1º nível, o grimório do Necromante contém três magias de 1º círculo à escolha do Mago e uma magia escolhida aleatoriamente da sua lista de magias de 1º círculo.\n\n**Novas Magias**: Um Necromante pode acrescentar livremente novas magias ao seu grimório copiando de outros grimórios ou de pergaminhos.\n\n**Círculos Superiores**: Um Necromante pode escrever no grimório magias de círculos acima de sua capacidade, mas não pode memorizá-las até atingir o nível necessário."
    },
    {
      "level": 1,
      "name": "Ler Magias",
      "description": "Um Necromante é capaz de uma vez ao dia por nível decifrar e ler inscrições mágicas em qualquer lugar, mesmo que não entenda a mensagem a qual elas querem passar.\n\nEsta habilidade não permite identificar as propriedades mágicas de um item mágico, nem é necessária para lançar magias escritas, mas permitirá identificar qual magia está escrita ali."
    },
    {
      "level": 1,
      "name": "Detectar Magias",
      "description": "Um Necromante é capaz de uma vez ao dia por nível perceber em lugares, pessoas ou coisas em uma área de até 9m + 3m por nível, a presença de magia, desde que esteja concentrado e procurando ativamente por isso.\n\nO Necromante percebe uma tênue aura mágica ao redor dos lugares, pessoas ou coisas encantadas, mas não é capaz de identificar a magia, o nível de poder do conjurador ou o efeito presente no alvo.\n\nUm Necromante precisa se concentrar 1d8 rodadas na área desejada para conseguir detectar, caso haja, alguma presença mágica. Esse tempo cai para 1d4 rodadas no 6º nível e para 1 rodada no 10º nível."
    },
    {
      "level": 1,
      "name": "Magias Exclusivas",
      "description": "O Necromante escreve em seu grimório, Toque Sombrio e Aterrorizar, exclusivas para Necromantes.\n\n- **Sem Memorizar**: Magias exclusivas não precisam ser memorizadas para serem conjuradas pelo Necromante.\n- **Usos por dia**: Cada magia exclusiva do Necromante em seu grimório pode ser usada até uma vez ao dia, adicionalmente às magias diárias do Necromante.\n- **Usos Adicionais**: Caso outros usos sejam realizados, a magia exclusiva consumirá o espaço ocupado na memória do Necromante por outra magia já previamente memorizada.\n- **Jogada de Proteção**: Todas as Jogadas de Proteção contra as magias exclusivas são realizadas com um teste difícil."
    },
    {
      "level": 3,
      "name": "Criar Mortos-Vivos",
      "description": "O Necromante escreve esta magia exclusiva em seu grimório."
    },
    {
      "level": 6,
      "name": "Drenar Vida",
      "description": "O Necromante escreve esta magia exclusiva em seu grimório."
    },
    {
      "level": 10,
      "name": "Magia da Morte",
      "description": "O Necromante escreve esta magia exclusiva em seu grimório."
    },
    {
      "level": 11,
      "name": "Reputação",
      "description": "O Necromante de alto nível atinge um grau superior de reconhecimento pelos seus feitos, obtendo Reputação 1 em 1d6. O valor de Reputação evolui em 1 até o máximo de 1-5 em 1d6 no 15º nível."
    }
  ],
  "fontes": [
    {
      "page": 45,
      "compact": false,
      "digital_item_url": "https://olddragon.com.br/livros/lb1.json"
    },
    {
      "page": null,
      "compact": true,
      "digital_item_url": "https://olddragon.com.br/livros/srd.json"
    }
  ],
  "parent_class_url": "https://olddragon.com.br/classes/mago.json",
  "url": "https://olddragon.com.br/classes/necromante.json"
}
```
<!-- END character_classes_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/classes/necromante.json
```
