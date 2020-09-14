[HOME](Home) / [ANALYTICS API](IngressoCerto-Analytics-API) / [TICKET](IngressoCerto-Analytics-API-Ticket) / POST

*****
##### **INGRESSO CERTO**
# **TICKET (Ingresso)**

#### REQUSIÇÃO (POST)

```
#!php
<?php

// REGISTER TICKET AS READ

$curl = curl_init('http://{base_url}/ticket');

curl_setopt($curl, CURLOPT_USERPWD, 'username:password');
curl_setopt($curl, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);
curl_setopt($curl, CURLOPT_RETURNTRANSFER, 1);
curl_setopt($curl, CURLOPT_POST, 1);
curl_setopt($curl, CURLOPT_POSTFIELDS, 'id={id}');

// EXAMPLE WITH 'code'
// curl_setopt($curl, CURLOPT_POSTFIELDS, 'code={code}');

$reponse = curl_exec($curl);

curl_close($curl);

print_r($reponse);

?>
```

#### RETORNO (POST)

````
#!json
{
    "status": true,
    "response": {
        "message": "Conferência registrada!"
    }
}
````