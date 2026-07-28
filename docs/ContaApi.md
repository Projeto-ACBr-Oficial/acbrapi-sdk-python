# acbrapi_sdk.ContaApi

All URIs are relative to *https://prod.acbr.api.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**consultar_cota_conta**](ContaApi.md#consultar_cota_conta) | **GET** /conta/cotas/{nome} | Consultar o limite de uso e o consumo de uma cota específica.
[**consultar_cota_pre_pago**](ContaApi.md#consultar_cota_pre_pago) | **GET** /conta/cotas/prepago | Consultar o resumo da cota de créditos pré-pagos.
[**listar_cotas_conta**](ContaApi.md#listar_cotas_conta) | **GET** /conta/cotas | Consultar os limites de uso e consumo das cotas disponíveis, exceto a cota de créditos pré-pagos.
[**listar_extrato_creditos_conta**](ContaApi.md#listar_extrato_creditos_conta) | **GET** /conta/extrato | Consultar o extrato de movimentação de créditos do tenant atual.


# **consultar_cota_conta**
> ContaCota consultar_cota_conta(nome)

Consultar o limite de uso e o consumo de uma cota específica.

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
    api_instance = acbrapi_sdk.ContaApi(api_client)
    nome = 'nome_example' # str | Nome da cota a ser consultada.

    try:
        # Consultar o limite de uso e o consumo de uma cota específica.
        api_response = api_instance.consultar_cota_conta(nome)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ContaApi->consultar_cota_conta: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **nome** | **str**| Nome da cota a ser consultada. | 

### Return type

[**ContaCota**](ContaCota.md)

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

# **consultar_cota_pre_pago**
> ContaCotaPrePago consultar_cota_pre_pago()

Consultar o resumo da cota de créditos pré-pagos.

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
    api_instance = acbrapi_sdk.ContaApi(api_client)
    
    try:
        # Consultar o resumo da cota de créditos pré-pagos.
        api_response = api_instance.consultar_cota_pre_pago()
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ContaApi->consultar_cota_pre_pago: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ContaCotaPrePago**](ContaCotaPrePago.md)

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

# **listar_cotas_conta**
> ContaCotaListagem listar_cotas_conta()

Consultar os limites de uso e consumo das cotas disponíveis, exceto a cota de créditos pré-pagos.

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
    api_instance = acbrapi_sdk.ContaApi(api_client)
    
    try:
        # Consultar os limites de uso e consumo das cotas disponíveis, exceto a cota de créditos pré-pagos.
        api_response = api_instance.listar_cotas_conta()
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ContaApi->listar_cotas_conta: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ContaCotaListagem**](ContaCotaListagem.md)

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

# **listar_extrato_creditos_conta**
> ContaExtratoCreditoListagem listar_extrato_creditos_conta(data_inicial=data_inicial, data_final=data_final, top=top, skip=skip, limit=limit)

Consultar o extrato de movimentação de créditos do tenant atual.

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
    api_instance = acbrapi_sdk.ContaApi(api_client)
    data_inicial = 'data_inicial_example' # str |  (optional)
data_final = 'data_final_example' # str |  (optional)
top = 56 # int |  (optional)
skip = 56 # int |  (optional)
limit = 56 # int |  (optional)

    try:
        # Consultar o extrato de movimentação de créditos do tenant atual.
        api_response = api_instance.listar_extrato_creditos_conta(data_inicial=data_inicial, data_final=data_final, top=top, skip=skip, limit=limit)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ContaApi->listar_extrato_creditos_conta: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data_inicial** | **str**|  | [optional] 
 **data_final** | **str**|  | [optional] 
 **top** | **int**|  | [optional] 
 **skip** | **int**|  | [optional] 
 **limit** | **int**|  | [optional] 

### Return type

[**ContaExtratoCreditoListagem**](ContaExtratoCreditoListagem.md)

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

