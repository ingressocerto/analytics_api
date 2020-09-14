[HOME](Home) / [ANALYTICS API](IngressoCerto-Analytics-API) / [SKU](IngressoCerto-Analytics-API-Sku) / GET

*****
##### **INGRESSO CERTO**
# **SKU (Tipos de Ingresso)**

#### REQUISIÇÃO (GET)

```
#!php
<?php

// LIST SKU'S

$curl = curl_init('http://{base_url}/sku/product/{product_id}');

// EXAMPLE WITH PARAMS
// $curl = curl_init('http://{base_url}/sku/product/{product_id}/page/2/limit/50/status/0'); 

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
    "skus": [
      {
        "id": "59572",
        "title": "Combo Teste",
        "event_notice": "Combo Teste",
        "price": "10.00",
        "category": {
          "id": "11",
          "name": "kit"
        },
        "status": {
          "id": "1",
          "name": "Ativo"
        }
      },
      {
        "id": "54254",
        "title": "Ingresso Pista Feminino Web - Inteira",
        "event_notice": "",
        "price": "0.60",
        "category": {
          "id": "27",
          "name": "Desconto"
        },
        "status": {
          "id": "1",
          "name": "Ativo"
        }
      }
    ],
    "page": {
      "number": 1,
      "limit": "2",
      "count": 7,
      "order": "title",
      "sort": "asc"
    }
  }
}
````