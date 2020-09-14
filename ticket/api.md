##### **INGRESSO CERTO**
# **TICKET (Ingresso)**

Permite a consulta de dados ou o registro da conferência do ingresso informado.

```
http://{base_url}/ticket
```

#### PARÂMETROS

Parâmetro | Tipo    | Padrão     | Descrição
----------|---------|------------|-----------
id        | int     | null       | (opcional) ID do ingresso
code      | numeric | null       | (opcional) Código de barras do ingresso
product   | int     | null       | (opcional) ID do produto (evento)
sku       | int     | null       | (opcional) ID do tipo de ingresso
pos       | int     | null       | (opcional) ID do ponto de venda
status    | int     | null       | (opcional) Filtra ingressos pela situação, '1' (ativo), '0' (Inativo)
page      | int     | 1          | (opcional) Número da página exibida
limit     | int     | 10         | (opcional) Quantidade de registros listados por página
order     | string  | id         | (opcional) Atributo utilizado para ordenação dos resultados, 'id'
sort      | string  | asc        | (opcional) Tipo de ordenação, 'asc' (ascendente), 'desc' (descendente)

#### REQUISIÇÃO HTTP

Método                                          | Descrição
----------------------------------------------- | ---------
[GET](get.md)   | Retorna a lista de registros
[POST](post.md) | Registra a conferência do ingresso

*Clique no método para ver o exemplo.*