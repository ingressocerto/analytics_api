##### **INGRESSO CERTO**
# **SKU (Tipos de Ingresso)**

Lista os tipos de ingresso do evento informado.

```
http://{base_url}/sku
```

#### PARÂMETROS

Parâmetro | Tipo   | Padrão     | Descrição
----------|--------|------------|-----------
product   | int    | null       | (requerido) ID do evento
id        | int    | null       | (opcional) ID do tipo de ingresso
status    | int    | null       | (opcional) Filtra tipos de ingresso pela situação, '1' (ativo), '0' (Inativo)
search    | string | null       | (opcional) Busca por palavra-chave
page      | int    | 1          | (opcional) Número da página exibida
limit     | int    | 10         | (opcional) Quantidade de registros listados por página
order     | string | title      | (opcional) Atributo utilizado para ordenação dos resultados, 'title', 'price'
sort      | string | asc        | (opcional) Tipo de ordenação, 'asc' (ascendente), 'desc' (descendente)

#### REQUISIÇÃO HTTP

Método                                     | Descrição
------------------------------------------ | ---------
[GET](get.md) | Retorna a lista de registros

*Clique no método para ver o exemplo.*