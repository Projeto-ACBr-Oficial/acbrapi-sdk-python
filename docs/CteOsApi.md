# acbrapi_sdk.CteOsApi

All URIs are relative to *https://prod.acbr.api.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**baixar_pdf_cancelamento_cte_os**](CteOsApi.md#baixar_pdf_cancelamento_cte_os) | **GET** /cteos/{id}/cancelamento/pdf | Baixar PDF do cancelamento
[**baixar_pdf_carta_correcao_cte_os**](CteOsApi.md#baixar_pdf_carta_correcao_cte_os) | **GET** /cteos/{id}/carta-correcao/pdf | Baixar PDF da carta de correção
[**baixar_pdf_cte_os**](CteOsApi.md#baixar_pdf_cte_os) | **GET** /cteos/{id}/pdf | Baixar PDF do DACTE
[**baixar_pdf_evento_cte_os**](CteOsApi.md#baixar_pdf_evento_cte_os) | **GET** /cteos/eventos/{id}/pdf | Baixar PDF do evento
[**baixar_xml_cancelamento_cte_os**](CteOsApi.md#baixar_xml_cancelamento_cte_os) | **GET** /cteos/{id}/cancelamento/xml | Baixar XML do cancelamento
[**baixar_xml_carta_correcao_cte_os**](CteOsApi.md#baixar_xml_carta_correcao_cte_os) | **GET** /cteos/{id}/carta-correcao/xml | Baixar XML da carta de correção
[**baixar_xml_cte_os**](CteOsApi.md#baixar_xml_cte_os) | **GET** /cteos/{id}/xml | Baixar XML do CT-e OS processado
[**baixar_xml_cte_os_conhecimento**](CteOsApi.md#baixar_xml_cte_os_conhecimento) | **GET** /cteos/{id}/xml/conhecimento | Baixar XML do CT-e OS
[**baixar_xml_cte_os_protocolo**](CteOsApi.md#baixar_xml_cte_os_protocolo) | **GET** /cteos/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
[**baixar_xml_evento_cte_os**](CteOsApi.md#baixar_xml_evento_cte_os) | **GET** /cteos/eventos/{id}/xml | Baixar XML do evento
[**cancelar_cte_os**](CteOsApi.md#cancelar_cte_os) | **POST** /cteos/{id}/cancelamento | Cancelar um CT-e OS autorizado
[**consultar_cancelamento_cte_os**](CteOsApi.md#consultar_cancelamento_cte_os) | **GET** /cteos/{id}/cancelamento | Consultar o cancelamento do CT-e OS
[**consultar_carta_correcao_cte_os**](CteOsApi.md#consultar_carta_correcao_cte_os) | **GET** /cteos/{id}/carta-correcao | Consultar a solicitação de correção do CT-e OS
[**consultar_cte_os**](CteOsApi.md#consultar_cte_os) | **GET** /cteos/{id} | Consultar CT-e OS
[**consultar_evento_cte_os**](CteOsApi.md#consultar_evento_cte_os) | **GET** /cteos/eventos/{id} | Consultar evento
[**consultar_status_sefaz_cte_os**](CteOsApi.md#consultar_status_sefaz_cte_os) | **GET** /cteos/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
[**criar_carta_correcao_cte_os**](CteOsApi.md#criar_carta_correcao_cte_os) | **POST** /cteos/{id}/carta-correcao | Solicitar correção do CT-e OS
[**emitir_cte_os**](CteOsApi.md#emitir_cte_os) | **POST** /cteos | Emitir CT-e OS
[**listar_cte_os**](CteOsApi.md#listar_cte_os) | **GET** /cteos | Listar CT-e OS
[**sincronizar_cte_os**](CteOsApi.md#sincronizar_cte_os) | **POST** /cteos/{id}/sincronizar | Sincroniza dados no CT-e OS a partir da SEFAZ


# **baixar_pdf_cancelamento_cte_os**
> file baixar_pdf_cancelamento_cte_os(id)

Baixar PDF do cancelamento

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do CT-e OS gerado pela API.

    try:
        # Baixar PDF do cancelamento
        api_response = api_instance.baixar_pdf_cancelamento_cte_os(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->baixar_pdf_cancelamento_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e OS gerado pela API. | 

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

# **baixar_pdf_carta_correcao_cte_os**
> file baixar_pdf_carta_correcao_cte_os(id)

Baixar PDF da carta de correção

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do CT-e OS gerado pela API.

    try:
        # Baixar PDF da carta de correção
        api_response = api_instance.baixar_pdf_carta_correcao_cte_os(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->baixar_pdf_carta_correcao_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e OS gerado pela API. | 

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

# **baixar_pdf_cte_os**
> file baixar_pdf_cte_os(id, logotipo=logotipo)

Baixar PDF do DACTE

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do CT-e OS gerado pela API.
logotipo = False # bool | Imprime o documento com logotipo, desde que esteja cadastrado na empresa. (optional) (default to False)

    try:
        # Baixar PDF do DACTE
        api_response = api_instance.baixar_pdf_cte_os(id, logotipo=logotipo)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->baixar_pdf_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e OS gerado pela API. | 
 **logotipo** | **bool**| Imprime o documento com logotipo, desde que esteja cadastrado na empresa. | [optional] [default to False]

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

# **baixar_pdf_evento_cte_os**
> file baixar_pdf_evento_cte_os(id)

Baixar PDF do evento

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Baixar PDF do evento
        api_response = api_instance.baixar_pdf_evento_cte_os(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->baixar_pdf_evento_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do evento gerado pela API. | 

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

# **baixar_xml_cancelamento_cte_os**
> file baixar_xml_cancelamento_cte_os(id)

Baixar XML do cancelamento

**Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do CT-e OS gerado pela API.

    try:
        # Baixar XML do cancelamento
        api_response = api_instance.baixar_xml_cancelamento_cte_os(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->baixar_xml_cancelamento_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e OS gerado pela API. | 

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

# **baixar_xml_carta_correcao_cte_os**
> file baixar_xml_carta_correcao_cte_os(id)

Baixar XML da carta de correção

**Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do CT-e OS gerado pela API.

    try:
        # Baixar XML da carta de correção
        api_response = api_instance.baixar_xml_carta_correcao_cte_os(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->baixar_xml_carta_correcao_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e OS gerado pela API. | 

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

# **baixar_xml_cte_os**
> file baixar_xml_cte_os(id)

Baixar XML do CT-e OS processado

Utilize esse endpoint para obter o XML do conhecimento enviado para a SEFAZ, complementado com a informação do protocolo de autorização de uso (TAG raiz `cteProc`).    O XML só estará disponível nesse endpoint caso o conhecimento tenha sido autorizado pela SEFAZ. Para obter o XML nos demais casos, utilize o endpoint `GET /cteos/{id}/xml/conhecimento`.    **Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do CT-e OS gerado pela API.

    try:
        # Baixar XML do CT-e OS processado
        api_response = api_instance.baixar_xml_cte_os(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->baixar_xml_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e OS gerado pela API. | 

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

# **baixar_xml_cte_os_conhecimento**
> file baixar_xml_cte_os_conhecimento(id)

Baixar XML do CT-e OS

Utilize esse endpoint para obter o XML do conhecimento enviado para a SEFAZ.    O XML estará disponível nesse endpoint mesmo em casos que o conhecimento tenha sido rejeitado.    **Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único da CT-e OS gerado pela API.

    try:
        # Baixar XML do CT-e OS
        api_response = api_instance.baixar_xml_cte_os_conhecimento(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->baixar_xml_cte_os_conhecimento: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da CT-e OS gerado pela API. | 

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

# **baixar_xml_cte_os_protocolo**
> file baixar_xml_cte_os_protocolo(id)

Baixar XML do Protocolo da SEFAZ

**Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único da CT-e OS gerado pela API.

    try:
        # Baixar XML do Protocolo da SEFAZ
        api_response = api_instance.baixar_xml_cte_os_protocolo(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->baixar_xml_cte_os_protocolo: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da CT-e OS gerado pela API. | 

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

# **baixar_xml_evento_cte_os**
> file baixar_xml_evento_cte_os(id)

Baixar XML do evento

**Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Baixar XML do evento
        api_response = api_instance.baixar_xml_evento_cte_os(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->baixar_xml_evento_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do evento gerado pela API. | 

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

# **cancelar_cte_os**
> DfeCancelamento cancelar_cte_os(id, body=body)

Cancelar um CT-e OS autorizado

**Informações adicionais**:  - Consumo: 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do CT-e OS gerado pela API.
body = acbrapi_sdk.CteOsPedidoCancelamento() # CteOsPedidoCancelamento |  (optional)

    try:
        # Cancelar um CT-e OS autorizado
        api_response = api_instance.cancelar_cte_os(id, body=body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->cancelar_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e OS gerado pela API. | 
 **body** | [**CteOsPedidoCancelamento**](CteOsPedidoCancelamento.md)|  | [optional] 

### Return type

[**DfeCancelamento**](DfeCancelamento.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **consultar_cancelamento_cte_os**
> DfeCancelamento consultar_cancelamento_cte_os(id)

Consultar o cancelamento do CT-e OS

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do CT-e OS gerado pela API.

    try:
        # Consultar o cancelamento do CT-e OS
        api_response = api_instance.consultar_cancelamento_cte_os(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->consultar_cancelamento_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e OS gerado pela API. | 

### Return type

[**DfeCancelamento**](DfeCancelamento.md)

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

# **consultar_carta_correcao_cte_os**
> CteOsCartaCorrecao consultar_carta_correcao_cte_os(id)

Consultar a solicitação de correção do CT-e OS

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do CT-e OS gerado pela API.

    try:
        # Consultar a solicitação de correção do CT-e OS
        api_response = api_instance.consultar_carta_correcao_cte_os(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->consultar_carta_correcao_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e OS gerado pela API. | 

### Return type

[**CteOsCartaCorrecao**](CteOsCartaCorrecao.md)

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

# **consultar_cte_os**
> Dfe consultar_cte_os(id)

Consultar CT-e OS

Consulta os detalhes de um CT-e OS já existente. Forneça o ID único obtido de uma requisição de emissão ou de listagem de CT-e OS e a API irá retornar as informações do CT-e OS correspondente.

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do CT-e OS gerado pela API.

    try:
        # Consultar CT-e OS
        api_response = api_instance.consultar_cte_os(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->consultar_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e OS gerado pela API. | 

### Return type

[**Dfe**](Dfe.md)

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

# **consultar_evento_cte_os**
> DfeEvento consultar_evento_cte_os(id)

Consultar evento

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Consultar evento
        api_response = api_instance.consultar_evento_cte_os(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->consultar_evento_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do evento gerado pela API. | 

### Return type

[**DfeEvento**](DfeEvento.md)

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

# **consultar_status_sefaz_cte_os**
> DfeSefazStatus consultar_status_sefaz_cte_os(cpf_cnpj, autorizador=autorizador)

Consulta do Status do Serviço na SEFAZ Autorizadora

Consulta do status do serviço prestado pelo Portal da Secretaria de Fazenda Estadual.    A API mantém a última consulta em cache por 5 minutos, evitando sobrecarregar desnecessariamente os servidores da SEFAZ (conforme orientação do MOC - versão 3.0.0a, item 4.6.3). Dessa forma, você poderá chamar esse endpoint quantas vezes quiser, sem preocupar-se em ter o seu CNPJ bloqueado por consumo indevido (Rejeição 656).

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF/CNPJ do emitente.  Utilize o valor sem máscara.
autorizador = 'autorizador_example' # str | Ambiente Autorizador.    Autorizadores disponíveis: `MT`, `MS`, `MG`, `PR`, `RS`, `SP`, `SVRS`, `SVSP`, `AN`.    *Caso não seja informado, será utilizado o ambiente autorizador da UF do emitente.* (optional)

    try:
        # Consulta do Status do Serviço na SEFAZ Autorizadora
        api_response = api_instance.consultar_status_sefaz_cte_os(cpf_cnpj, autorizador=autorizador)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->consultar_status_sefaz_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF/CNPJ do emitente.  Utilize o valor sem máscara. | 
 **autorizador** | **str**| Ambiente Autorizador.    Autorizadores disponíveis: &#x60;MT&#x60;, &#x60;MS&#x60;, &#x60;MG&#x60;, &#x60;PR&#x60;, &#x60;RS&#x60;, &#x60;SP&#x60;, &#x60;SVRS&#x60;, &#x60;SVSP&#x60;, &#x60;AN&#x60;.    *Caso não seja informado, será utilizado o ambiente autorizador da UF do emitente.* | [optional] 

### Return type

[**DfeSefazStatus**](DfeSefazStatus.md)

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

# **criar_carta_correcao_cte_os**
> CteOsCartaCorrecao criar_carta_correcao_cte_os(id, body)

Solicitar correção do CT-e OS

É possível enviar até 20 correções diferentes, sendo que será válido sempre a última correção enviada.    **Informações adicionais**:  - Consumo: 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do CT-e OS gerado pela API.
body = acbrapi_sdk.CteOsPedidoCartaCorrecao() # CteOsPedidoCartaCorrecao | 

    try:
        # Solicitar correção do CT-e OS
        api_response = api_instance.criar_carta_correcao_cte_os(id, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->criar_carta_correcao_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e OS gerado pela API. | 
 **body** | [**CteOsPedidoCartaCorrecao**](CteOsPedidoCartaCorrecao.md)|  | 

### Return type

[**CteOsCartaCorrecao**](CteOsCartaCorrecao.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emitir_cte_os**
> Dfe emitir_cte_os(body)

Emitir CT-e OS

**Informações adicionais**:  - Consumo: 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    body = acbrapi_sdk.CteOsPedidoEmissao() # CteOsPedidoEmissao | 

    try:
        # Emitir CT-e OS
        api_response = api_instance.emitir_cte_os(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->emitir_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**CteOsPedidoEmissao**](CteOsPedidoEmissao.md)|  | 

### Return type

[**Dfe**](Dfe.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listar_cte_os**
> DfeListagem listar_cte_os(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia, chave=chave, serie=serie)

Listar CT-e OS

Retorna a lista de CT-e OS de acordo com os critérios de busca utilizados. Os CT-e OS são retornados ordenados pela data da criação, com os mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ do emitente.    Utilize o valor sem máscara.
ambiente = 'ambiente_example' # str | Identificação do Ambiente.    Valores aceitos: homologacao, producao
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)
referencia = 'referencia_example' # str | Seu identificador único para o documento. (optional)
chave = 'chave_example' # str | Chave de acesso do DF-e. (optional)
serie = 'serie_example' # str | Série do DF-e. (optional)

    try:
        # Listar CT-e OS
        api_response = api_instance.listar_cte_os(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia, chave=chave, serie=serie)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->listar_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| Filtrar pelo CPF ou CNPJ do emitente.    Utilize o valor sem máscara. | 
 **ambiente** | **str**| Identificação do Ambiente.    Valores aceitos: homologacao, producao | 
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to False]
 **referencia** | **str**| Seu identificador único para o documento. | [optional] 
 **chave** | **str**| Chave de acesso do DF-e. | [optional] 
 **serie** | **str**| Série do DF-e. | [optional] 

### Return type

[**DfeListagem**](DfeListagem.md)

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

# **sincronizar_cte_os**
> DfeSincronizacao sincronizar_cte_os(id)

Sincroniza dados no CT-e OS a partir da SEFAZ

Realiza a sincronização dos dados a partir da consulta da situação atual do CT-e OS na Base de Dados do Portal da Secretaria de Fazenda Estadual.    **Cenários de uso**:  * Sincronizar um CT-e OS que se encontra com o status `erro` na API, mas está autorizado na SEFAZ (útil em casos de erros de transmissão com a SEFAZ, como instabilidades e timeouts).  * Sincronizar um CT-e OS que se encontra com o status `autorizado`na API, mas está cancelado na SEFAZ.  * Sincronizar todos os eventos de Cancelamento e Carta de Correção de um CT-e OS que porventura não tenham sido feitos a partir da API.    **Informações adicionais**:  - Consumo: 1 unidade por evento sincronizado ou requisição.

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
    api_instance = acbrapi_sdk.CteOsApi(api_client)
    id = 'id_example' # str | ID único do CT-e OS gerado pela API.

    try:
        # Sincroniza dados no CT-e OS a partir da SEFAZ
        api_response = api_instance.sincronizar_cte_os(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling CteOsApi->sincronizar_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e OS gerado pela API. | 

### Return type

[**DfeSincronizacao**](DfeSincronizacao.md)

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

