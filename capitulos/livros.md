Livros
======

Endpoints:

- [Listar livros](#listar-livros)
- [Listar meus livros](#listar-meus-livros)
- [Obter livro específico](#obter-livro-específico)

Listar livros
-------------

- `GET /livros.json` retorna todos os livros.

_Parâmetros opcionais de URL_:

* `ids[]` - Lista de IDs de livros. Exemplo: `ids[]=lb1&ids[]=lb2`.

###### Exemplo de resposta JSON
<!-- START digital_items_index.json -->
```json
[
  {
    "id": "lb1",
    "type": "DigitalItem",
    "title": "Livro I: Regras Básicas",
    "url": "https://olddragon.com.br/livros/lb1.json"
  },
  {
    "id": "lb2",
    "type": "DigitalItem",
    "title": "Livro II: Regras Expandidas",
    "url": "https://olddragon.com.br/livros/lb2.json"
  },
  {
    "id": "lb3",
    "type": "DigitalItem",
    "title": "Livro III: Monstros & Inimigos",
    "url": "https://olddragon.com.br/livros/lb3.json"
  },
  {
    "id": "srd",
    "type": "DigitalItem",
    "title": "SRD: Documento de Referência",
    "url": "https://olddragon.com.br/livros/srd.json"
  },
  {
    "id": "cl1",
    "type": "DigitalItem",
    "title": "CL1: O Forte das Terras Marginais",
    "url": "https://olddragon.com.br/livros/cl1.json"
  }
]
```
<!-- END digital_items_index.json -->
###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/livros.json
```

###### Copiar como HTTPie

``` shell
http https://olddragon.com.br/livros.json
```

Listar meus livros
------------------

**Autenticação obrigatória**: Este endpoint requer autenticação OAuth.

* `GET /livros/meus.json` retorna todos os livros do usuário autenticado.

_Parâmetros opcionais de URL_:

* `category` - Filtrar por categoria. Exemplo: `category=core_book`.

###### Exemplo de resposta JSON
<!-- START digital_items_my.json -->
```json
[
  {
    "id": "lb1",
    "type": "DigitalItem",
    "title": "Livro I: Regras Básicas",
    "url": "https://olddragon.com.br/livros/lb1.json"
  }
]
```
<!-- END digital_items_my.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/livros/meus.json -H "Authorization: Bearer <token>"
```

###### Copiar como HTTPie

``` shell
http https://olddragon.com.br/livros/meus.json Authorization:"Bearer <token>"
```

Obter livro específico
----------------------

- `GET /livros/lb1.json` retorna a livro específica para a ID informada (neste exemplo, a ID é `lb1`).

###### Exemplo de resposta JSON
<!-- START digital_items_show.json -->
```json
{
  "id": "lb1",
  "type": "DigitalItem",
  "title": "Livro I: Regras Básicas",
  "url": "https://olddragon.com.br/livros/lb1.json"
}
```
<!-- END digital_items_show.json -->

###### Copiar como cURL

``` shell
curl -s https://olddragon.com.br/livros/ajuda.json
```

###### Copiar como HTTPie

``` shell
http https://olddragon.com.br/livros/ajuda.json
```
