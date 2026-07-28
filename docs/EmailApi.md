# acbrapi_sdk.EmailApi

All URIs are relative to *https://prod.acbr.api.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**consultar_email**](EmailApi.md#consultar_email) | **GET** /emails/{id} | Consultar e-mail
[**listar_emails**](EmailApi.md#listar_emails) | **GET** /emails | Listar e-mails


# **consultar_email**
> Email consultar_email(id)

Consultar e-mail

Obtém informações detalhadas sobre o envio de um email. Este endpoint  permite rastrear todos os eventos relacionados ao email, como envio,  entrega, falhas e outros eventos relevantes.    Com este endpoint, é possível ter uma visão completa do ciclo de vida  de um email enviado, permitindo que os usuários acompanhem e analisem  o status e o histórico de eventos do email. Isso é particularmente  útil para identificar problemas de entrega e entender o comportamento  do email ao longo do tempo.

### Example

* OAuth Authentication (oauth2):
```python
from __future__ import print_function
import time
import acbrapi_sdk
from acbrapi_sdk.rest import ApiException
from pprint import pprint
# Definir o host e opcional; o padrao e https://prod.acbr.api.br
# Veja configuration.py para a lista de parametros de configuracao suportados.
configuration = acbrapi_sdk.Configuration(
    host = "https://prod.acbr.api.br"
)

# O cliente deve configurar os parametros de autenticacao e autorizacao
# de acordo com a politica de seguranca do servidor da API.
# Abaixo ha exemplos para cada metodo de autenticacao; use o que
# atende ao seu caso de uso.

# Configura o token de acesso OAuth2 para autorizacao: oauth2
configuration = acbrapi_sdk.Configuration(
    host = "https://prod.acbr.api.br"
)
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# Enter a context with an instance of the API client
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = acbrapi_sdk.EmailApi(api_client)
    id = 'id_example' # str | ID único do e-mail.    Esse parâmetro é obtido após o envio do email por qualquer endpoint da  API que realize disparos de email.    Exemplos:  * <a href=\"#tag/Nfe/operation/EnviarEmailNfe\">Envio de XML e PDF de NF-e</a>.  * <a href=\"#tag/Nfce/operation/EnviarEmailNfce\">Envio de XML e PDF de NFC-e</a>.

    try:
        # Consultar e-mail
        api_response = api_instance.consultar_email(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmailApi->consultar_email: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do e-mail.    Esse parâmetro é obtido após o envio do email por qualquer endpoint da  API que realize disparos de email.    Exemplos:  * &lt;a href&#x3D;\&quot;#tag/Nfe/operation/EnviarEmailNfe\&quot;&gt;Envio de XML e PDF de NF-e&lt;/a&gt;.  * &lt;a href&#x3D;\&quot;#tag/Nfce/operation/EnviarEmailNfce\&quot;&gt;Envio de XML e PDF de NFC-e&lt;/a&gt;. | 

### Return type

[**Email**](Email.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listar_emails**
> EmailListagem listar_emails(cpf_cnpj, top=top, skip=skip, inlinecount=inlinecount, undelivered=undelivered, email=email)

Listar e-mails

Retorna a lista dos emails associadas à sua conta. Os e-emails são  retornados ordenados pela data da criação, com os mais recentes  aparecendo primeiro.

### Example

* OAuth Authentication (oauth2):
```python
from __future__ import print_function
import time
import acbrapi_sdk
from acbrapi_sdk.rest import ApiException
from pprint import pprint
# Definir o host e opcional; o padrao e https://prod.acbr.api.br
# Veja configuration.py para a lista de parametros de configuracao suportados.
configuration = acbrapi_sdk.Configuration(
    host = "https://prod.acbr.api.br"
)

# O cliente deve configurar os parametros de autenticacao e autorizacao
# de acordo com a politica de seguranca do servidor da API.
# Abaixo ha exemplos para cada metodo de autenticacao; use o que
# atende ao seu caso de uso.

# Configura o token de acesso OAuth2 para autorizacao: oauth2
configuration = acbrapi_sdk.Configuration(
    host = "https://prod.acbr.api.br"
)
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# Enter a context with an instance of the API client
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = acbrapi_sdk.EmailApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtra pelo CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*.
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)
undelivered = True # bool | Filtra apenas emails com problemas de entrega. (optional)
email = 'email_example' # str | Filtra pelo endereço de e-mail do destinatário para qual o email foi enviado. (optional)

    try:
        # Listar e-mails
        api_response = api_instance.listar_emails(cpf_cnpj, top=top, skip=skip, inlinecount=inlinecount, undelivered=undelivered, email=email)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmailApi->listar_emails: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| Filtra pelo CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*. | 
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to False]
 **undelivered** | **bool**| Filtra apenas emails com problemas de entrega. | [optional] 
 **email** | **str**| Filtra pelo endereço de e-mail do destinatário para qual o email foi enviado. | [optional] 

### Return type

[**EmailListagem**](EmailListagem.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

