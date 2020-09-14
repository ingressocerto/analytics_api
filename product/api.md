##### **INGRESSO CERTO**
# **PRODUCT (Eventos)**

Lista os produtos associados ao usuário informado na autenticação.

```
http://{base_url}/product
```

#### PARÂMETROS

Parâmetro  | Tipo   | Padrão     | Descrição
-----------|--------|------------|-----------
id         | int    | null       | (opcional) ID do evento
event_date | date   | null       | (opcional) Filtra eventos pela data, formato americano
status     | int    | null       | (opcional) Filtra eventos pela situação, '1' (ativo)
search     | string | null       | (opcional) Busca por palavra-chave
page       | int    | 1          | (opcional) Número da página exibida
limit      | int    | 10         | (opcional) Quantidade de registros listados por página
order      | string | title      | (opcional) Atributo utilizado para ordenação dos resultados, 'id', 'title', 'event_date'
sort       | string | asc        | (opcional) Tipo de ordenação, 'asc' (ascendente), 'desc' (descendente)

#### REQUISIÇÂO HTTP

Método                                         | Descrição
---------------------------------------------- | ---------
[GET](get.md) | Retorna a lista de registros

*Clique no método para ver o exemplo.*