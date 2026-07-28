# acbrapi_sdk.DebugApi

All URIs are relative to *https://prod.acbr.api.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**debug_dfe**](DebugApi.md#debug_dfe) | **GET** /debug/{id} | Debug de DF-e
[**debug_dfe_original_payload**](DebugApi.md#debug_dfe_original_payload) | **GET** /debug/{id}/original-payload | Payload original recebido
[**debug_http_request_content**](DebugApi.md#debug_http_request_content) | **GET** /debug/http-requests/{id}/request-content | Corpo da requisição HTTP
[**debug_http_response_content**](DebugApi.md#debug_http_response_content) | **GET** /debug/http-requests/{id}/response-content | Corpo da resposta HTTP


# **debug_dfe**
> DfeDebug debug_dfe(id)

Debug de DF-e

Este endpoint retorna informações detalhadas de debug sobre o processamento de um documento fiscal eletrônico (DFe),  como NF-e, NFC-e, MDF-e, CT-e, NFS-e, dentre outros. Ele permite inspecionar o conteúdo original enviado à API e analisar  todas as interações realizadas com os serviços autorizadores (SEFAZ ou prefeituras) durante o fluxo de emissão.    **Informações retornadas**:  - JSON original recebido no momento da criação do documento.  - Histórico das etapas de envio e consulta.  - Status e mensagens retornadas pelo autorizador.    **Cenários de uso**:  - Diagnóstico de falhas no processamento do documento.  - Verificação da resposta da SEFAZ ou prefeitura.  - Apoio ao suporte técnico e análise de integração.

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
    api_instance = acbrapi_sdk.DebugApi(api_client)
    id = 'id_example' # str | ID único do documento fiscal gerado pela API.

    try:
        # Debug de DF-e
        api_response = api_instance.debug_dfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DebugApi->debug_dfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do documento fiscal gerado pela API. | 

### Return type

[**DfeDebug**](DfeDebug.md)

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

# **debug_dfe_original_payload**
> file debug_dfe_original_payload(id)

Payload original recebido

Este endpoint retorna o conteúdo original recebido pela API no momento da criação do documento fiscal.    **Cenários de uso**:  - Inspeção detalhada dos dados enviados à API.  - Verificação de divergências entre o payload fornecido e o processado.  - Encaminhamento do conteúdo original ao suporte da API.

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
    api_instance = acbrapi_sdk.DebugApi(api_client)
    id = 'id_example' # str | ID do documento fiscal gerado pela API.

    try:
        # Payload original recebido
        api_response = api_instance.debug_dfe_original_payload(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DebugApi->debug_dfe_original_payload: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID do documento fiscal gerado pela API. | 

### Return type

**file**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **debug_http_request_content**
> file debug_http_request_content(id)

Corpo da requisição HTTP

Este endpoint retorna apenas o corpo da requisição HTTP enviada ao autorizador,  preservando o conteúdo exatamente como foi armazenado pela API.    **Informações retornadas**:  - Envelope SOAP da requisição, possivelmente compactado.    **Cenários de uso**:  - Verificação do XML ou SOAP efetivamente enviado.  - Encaminhamento ao suporte da SEFAZ ou prefeitura para análise.  - Diagnóstico técnico do conteúdo de envio.

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
    api_instance = acbrapi_sdk.DebugApi(api_client)
    id = 'id_example' # str | ID da requisição HTTP.

    try:
        # Corpo da requisição HTTP
        api_response = api_instance.debug_http_request_content(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DebugApi->debug_http_request_content: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID da requisição HTTP. | 

### Return type

**file**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **debug_http_response_content**
> file debug_http_response_content(id)

Corpo da resposta HTTP

Este endpoint retorna apenas o corpo da resposta HTTP recebida do autorizador,  permitindo análise técnica da mensagem retornada pela SEFAZ ou prefeitura.    **Informações retornadas**:  - Envelope SOAP da resposta, ou mensagem de erro (ex: HTML, XML), no formato original.    **Cenários de uso**:  - Inspeção da resposta real retornada pelo autorizador.  - Encaminhamento do conteúdo ao suporte técnico.  - Diagnóstico de rejeições, falhas de processamento ou erros de infraestrutura.

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
    api_instance = acbrapi_sdk.DebugApi(api_client)
    id = 'id_example' # str | ID da requisição HTTP.

    try:
        # Corpo da resposta HTTP
        api_response = api_instance.debug_http_response_content(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DebugApi->debug_http_response_content: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID da requisição HTTP. | 

### Return type

**file**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

