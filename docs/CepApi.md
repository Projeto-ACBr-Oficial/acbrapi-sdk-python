# acbrapi_sdk.CepApi

All URIs are relative to *https://prod.acbr.api.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**consultar_cep**](CepApi.md#consultar_cep) | **GET** /cep/{Cep} | Consultar endereço através do CEP


# **consultar_cep**
> CepEndereco consultar_cep(cep)

Consultar endereço através do CEP

**Informações adicionais**:  - Consumo: 0,1 unidade requisição.  - Em sandbox, a consulta é permitida somente para os seguintes CEP:    `18270000` Tatuí/SP    `01310300` São Paulo/SP    `22010000` Rio de Janeiro/RJ    `80020130` Curitiba/PR

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
    api_instance = acbrapi_sdk.CepApi(api_client)
    cep = 'cep_example' # str | CEP sem máscara.

    try:
        # Consultar endereço através do CEP
        api_response = api_instance.consultar_cep(cep)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CepApi->consultar_cep: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cep** | **str**| CEP sem máscara. | 

### Return type

[**CepEndereco**](CepEndereco.md)

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

