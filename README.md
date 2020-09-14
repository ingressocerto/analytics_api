##### **INGRESSO CERTO**
# **ANALYTICS API**

Esta documentação tem a finalidade de auxiliar e ensinar como consumir as APIs de integração do Ingresso Certo Analytics.

[Documentação](https://github.com/ingressocerto/analytics_api/wiki)

Todas as APIs devem ser acessadas a partir da URL base `{base_url}` a seguir:

```
https://analytics.ingressocerto.com/api/v1
```

As requisições para API devem ser feitas passando usuário e senha usando "basic authentication". 

#### EXEMPLO

```
#!php
<?php

$curl = curl_init('http://{base_url}/{api_name}');

curl_setopt($curl, CURLOPT_USERPWD, 'username:password');
curl_setopt($curl, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);

?>
```

*****

## **API'S DISPONÍVEIS** 

[API Product](product/api.md) (Atualizado em 08/03/2017)

[API Sku](sku/api.md) (Atualizado em 08/03/2017)

[API Ticket](ticket/api.md) (Atualizado em 19/06/2017)