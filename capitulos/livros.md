Livros
======

Endpoints:

- [Listar livros](#listar-livros)
- [Obter livro específico](#obter-livro-específico)

Listar livros
-------------

- `GET /livros.json` retorna todos os livros.

###### Exemplo de resposta JSON
<!-- START digital_items_index.json -->
[
  {
    "id": "lb1",
    "title": "Livro I: Regras Básicas",
    "url": "https://olddragon.com.br/livros/lb1.json"
  },
  {
    "id": "lb2",
    "title": "Livro II: Regras Expandidas",
    "url": "https://olddragon.com.br/livros/lb2.json"
  },
  {
    "id": "lb3",
    "title": "Livro III: Monstros & Inimigos",
    "url": "https://olddragon.com.br/livros/lb3.json"
  }
]
<!-- END digital_items_index.json -->
###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/livros.json
```

Obter livro específico
----------------------

- `GET /livros/lb1.json` retorna a livro específica para a ID informada (neste exemplo, a ID é `lb1`).

###### Exemplo de resposta JSON
<!-- START digital_items_show.json -->
{
  "id": "lb1",
  "title": "Livro I: Regras Básicas",
  "url": "https://olddragon.com.br/livros/lb1.json"
}
<!-- END digital_items_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/livros/ajuda.json
```
