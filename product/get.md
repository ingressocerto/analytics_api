[HOME](Home) / [ANALYTICS API](IngressoCerto-Analytics-API) / [PRODUCT](IngressoCerto-Analytics-API-Product) / GET

*****
##### **INGRESSO CERTO**
# **PRODUCT (Eventos)**

#### REQUSIÇÃO (GET)
```
#!php
<?php

// LIST PRODUCTS

$curl = curl_init('http://{base_url}/product');

// EXAMPLE WITH PARAMS
// $curl = curl_init('http://{base_url}/product/event_date/2017-02-15/page/2/limit/50/order/title/sort/desc'); 

curl_setopt($curl, CURLOPT_USERPWD, 'username:password');
curl_setopt($curl, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);
curl_setopt($curl, CURLOPT_RETURNTRANSFER, 1);

$reponse = curl_exec($curl);

curl_close($curl);

print_r($reponse);

?>
```

#### RETORNO (GET)

````
#!json
{
  "status": true,
  "response": {
    "products": [
      {
        "id": "5780",
        "title": "Produto de Teste (Não Comprar)",
        "event_date": "2020-12-31",
        "event_place": "Indefinido",
        "event_city": "Rio de Janeiro",
        "event_notice": "Este é um produto criado para teste, favor não comprar.",
        "status": {
          "id": "1",
          "name": "Ativo"
        }
      },
      {
        "id": "9976",
        "title": "Produto de Teste",
        "event_date": "2099-09-18",
        "event_place": "Rio de Janeiro",
        "event_city": "Porto Alegre",
        "event_notice": "Classificação:18 anos. Obrigatória apresentação de carteira de identidade original ou CNH.Evento monitorado.",
        "status": {
          "id": "1",
          "name": "Ativo"
        }
      }
    ],
    "page": {
      "number": "1",
      "limit": 10,
      "count": 25,
      "order": "event_date",
      "sort": "asc"
    }
  }
}
````