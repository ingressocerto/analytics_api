##### **INGRESSO CERTO**
# **TICKET (Ingresso)**

#### REQUISIÇÃO (GET)

```
#!php
<?php

// GET TICKET

$curl = curl_init('http://{base_url}/ticket/id/{id}');

// EXAMPLE WITH 'code'
// $curl = curl_init('http://{base_url}/ticket/code/{code}');

// EXAMPLE WITH 'product'
// $curl = curl_init('http://{base_url}/ticket/product/{product_id}/limit/{limit}');

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
        "tickets": [
            {
                "access": {
                    "status": {
                        "id": 0,
                        "name": "Não liberado",
                        "message": "O ingresso já foi conferido!"
                    }
                },
                "ticket": {
                    "id": "11094631",
                    "code": "11094631",
                    "creation_date": "2014-09-12 13:05:15",
                    "printing_date": "2014-09-12 13:05:24",
                    "reading_date": "2017-02-14 20:34:02",
                    "status": {
                        "id": "1",
                        "name": "Ativo"
                    },
                    "data": {
                        "name": null,
                        "email": null,
                        "cell_phone": null
                    }
                },
                "product": {
                    "id": "531",
                    "title": "Evento Teste - Permissão POS",
                    "event_date": "2020-12-31",
                    "event_place": "Rua Guilhermina Guinle",
                    "event_city": "Rio de Janeiro",
                    "event_notice": "Proibida a entrada de menores de 18 anos. Obrigatória a apresentação de carteira de identidade original ou CNH. Evento monitorado.",
                    "status": {
                        "id": "1",
                        "name": "Ativo"
                    }
                },
                "sku": {
                    "id": "59573",
                    "title": "Combo Teste",
                    "event_notice": "Combo Teste",
                    "price": "10.00",
                    "status": {
                        "id": "1",
                        "name": "Ativo"
                    }
                },
                "order": {
                    "id": "8361861",
                    "creation_date": "2014-09-12 13:05:13",
                    "note": "VENDA ONLINE (NOVO)",
                    "status": {
                        "id": "2",
                        "name": "Aprovado"
                    },
                    "shipping_method": {
                        "id": null,
                        "name": null
                    },
                    "pos": {
                        "id": "127",
                        "name": "TESTE"
                    },
                    "customer": {
                        "id": null,
                        "name": null,
                        "email": null,
                        "phone": null,
                        "cell_phone": null,
                        "address": {
                            "zip_code": null
                        }
                    }
                }
            }
        ],
        "page": {
            "number": 1,
            "limit": "1",
            "count": 4705,
            "order": "t.id",
            "sort": "asc"
        }
    }
}
````