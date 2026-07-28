# acbrapi_sdk.NfcomApi

All URIs are relative to *https://prod.acbr.api.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**baixar_pdf_nfcom**](NfcomApi.md#baixar_pdf_nfcom) | **GET** /nfcom/{id}/pdf | Baixar PDF do DANFE-COM
[**baixar_xml_cancelamento_nfcom**](NfcomApi.md#baixar_xml_cancelamento_nfcom) | **GET** /nfcom/{id}/cancelamento/xml | Baixar XML do cancelamento
[**baixar_xml_nfcom**](NfcomApi.md#baixar_xml_nfcom) | **GET** /nfcom/{id}/xml | Baixar XML da NFCom processada
[**baixar_xml_nfcom_nota**](NfcomApi.md#baixar_xml_nfcom_nota) | **GET** /nfcom/{id}/xml/nota | Baixar XML da NFCom
[**baixar_xml_nfcom_protocolo**](NfcomApi.md#baixar_xml_nfcom_protocolo) | **GET** /nfcom/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
[**cancelar_nfcom**](NfcomApi.md#cancelar_nfcom) | **POST** /nfcom/{id}/cancelamento | Cancelar uma NFCom autorizada
[**consultar_cancelamento_nfcom**](NfcomApi.md#consultar_cancelamento_nfcom) | **GET** /nfcom/{id}/cancelamento | Consultar o cancelamento da NFCom
[**consultar_nfcom**](NfcomApi.md#consultar_nfcom) | **GET** /nfcom/{id} | Consultar NFCom
[**consultar_status_sefaz_nfcom**](NfcomApi.md#consultar_status_sefaz_nfcom) | **GET** /nfcom/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
[**emitir_nfcom**](NfcomApi.md#emitir_nfcom) | **POST** /nfcom | Emitir NFCom
[**listar_nfcom**](NfcomApi.md#listar_nfcom) | **GET** /nfcom | Listar NFCom


# **baixar_pdf_nfcom**
> file baixar_pdf_nfcom(id, logotipo=logotipo)

Baixar PDF do DANFE-COM

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
    api_instance = acbrapi_sdk.NfcomApi(api_client)
    id = 'id_example' # str | ID único da NFCom gerado pela API.
logotipo = False # bool | Imprime o documento com logotipo, desde que esteja cadastrado na empresa. (optional) (default to False)

    try:
        # Baixar PDF do DANFE-COM
        api_response = api_instance.baixar_pdf_nfcom(id, logotipo=logotipo)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfcomApi->baixar_pdf_nfcom: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFCom gerado pela API. | 
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

# **baixar_xml_cancelamento_nfcom**
> file baixar_xml_cancelamento_nfcom(id)

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
    api_instance = acbrapi_sdk.NfcomApi(api_client)
    id = 'id_example' # str | ID único da NFCom gerada pela API.

    try:
        # Baixar XML do cancelamento
        api_response = api_instance.baixar_xml_cancelamento_nfcom(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfcomApi->baixar_xml_cancelamento_nfcom: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFCom gerada pela API. | 

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

# **baixar_xml_nfcom**
> file baixar_xml_nfcom(id)

Baixar XML da NFCom processada

Utilize esse endpoint para obter o XML da nota enviada para a SEFAZ, complementado com a informação do protocolo de autorização de uso (TAG raiz `nfcomProc`).    O XML só estará disponível nesse endpoint caso a nota tenha sido autorizada pela SEFAZ. Para obter o XML nos demais casos, utilize o endpoint `GET /nfcom/{id}/xml/nota`.    **Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.NfcomApi(api_client)
    id = 'id_example' # str | ID único da NFCom gerada pela API.

    try:
        # Baixar XML da NFCom processada
        api_response = api_instance.baixar_xml_nfcom(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfcomApi->baixar_xml_nfcom: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFCom gerada pela API. | 

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

# **baixar_xml_nfcom_nota**
> file baixar_xml_nfcom_nota(id)

Baixar XML da NFCom

Utilize esse endpoint para obter o XML da nota enviada para a SEFAZ.    O XML estará disponível nesse endpoint mesmo em casos que a nota tenha sido rejeitada.    **Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.NfcomApi(api_client)
    id = 'id_example' # str | ID único da NFCom gerada pela API.

    try:
        # Baixar XML da NFCom
        api_response = api_instance.baixar_xml_nfcom_nota(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfcomApi->baixar_xml_nfcom_nota: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFCom gerada pela API. | 

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

# **baixar_xml_nfcom_protocolo**
> file baixar_xml_nfcom_protocolo(id)

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
    api_instance = acbrapi_sdk.NfcomApi(api_client)
    id = 'id_example' # str | ID único da NFCom gerada pela API.

    try:
        # Baixar XML do Protocolo da SEFAZ
        api_response = api_instance.baixar_xml_nfcom_protocolo(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfcomApi->baixar_xml_nfcom_protocolo: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFCom gerada pela API. | 

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

# **cancelar_nfcom**
> DfeCancelamento cancelar_nfcom(id, body=body)

Cancelar uma NFCom autorizada

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
    api_instance = acbrapi_sdk.NfcomApi(api_client)
    id = 'id_example' # str | ID único da NFCom gerada pela API.
body = acbrapi_sdk.NfcomPedidoCancelamento() # NfcomPedidoCancelamento |  (optional)

    try:
        # Cancelar uma NFCom autorizada
        api_response = api_instance.cancelar_nfcom(id, body=body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfcomApi->cancelar_nfcom: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFCom gerada pela API. | 
 **body** | [**NfcomPedidoCancelamento**](NfcomPedidoCancelamento.md)|  | [optional] 

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

# **consultar_cancelamento_nfcom**
> DfeCancelamento consultar_cancelamento_nfcom(id)

Consultar o cancelamento da NFCom

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
    api_instance = acbrapi_sdk.NfcomApi(api_client)
    id = 'id_example' # str | ID único da NFCom gerada pela API.

    try:
        # Consultar o cancelamento da NFCom
        api_response = api_instance.consultar_cancelamento_nfcom(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfcomApi->consultar_cancelamento_nfcom: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFCom gerada pela API. | 

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

# **consultar_nfcom**
> Dfe consultar_nfcom(id)

Consultar NFCom

Consulta os detalhes de uma NFCom já existente. Forneça o ID único obtido de uma requisição de emissão ou de listagem de NFCom e a API irá retornar as informações da NFCom correspondente.

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
    api_instance = acbrapi_sdk.NfcomApi(api_client)
    id = 'id_example' # str | ID único da NFCom gerada pela API.

    try:
        # Consultar NFCom
        api_response = api_instance.consultar_nfcom(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfcomApi->consultar_nfcom: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFCom gerada pela API. | 

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

# **consultar_status_sefaz_nfcom**
> DfeSefazStatus consultar_status_sefaz_nfcom(cpf_cnpj, autorizador=autorizador)

Consulta do Status do Serviço na SEFAZ Autorizadora

Consulta do status do serviço prestado pelo Portal da Secretaria de Fazenda Estadual.    A API mantém a última consulta em cache por 5 minutos, evitando sobrecarregar desnecessariamente os servidores da SEFAZ.

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
    api_instance = acbrapi_sdk.NfcomApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF/CNPJ do emitente.  Utilize o valor sem máscara.
autorizador = 'autorizador_example' # str | Ambiente Autorizador.    Autorizadores disponíveis: `SVRS`.    *Caso não seja informado, será utilizado o ambiente autorizador da UF do emitente.* (optional)

    try:
        # Consulta do Status do Serviço na SEFAZ Autorizadora
        api_response = api_instance.consultar_status_sefaz_nfcom(cpf_cnpj, autorizador=autorizador)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfcomApi->consultar_status_sefaz_nfcom: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF/CNPJ do emitente.  Utilize o valor sem máscara. | 
 **autorizador** | **str**| Ambiente Autorizador.    Autorizadores disponíveis: &#x60;SVRS&#x60;.    *Caso não seja informado, será utilizado o ambiente autorizador da UF do emitente.* | [optional] 

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

# **emitir_nfcom**
> Dfe emitir_nfcom(body)

Emitir NFCom

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
    api_instance = acbrapi_sdk.NfcomApi(api_client)
    body = acbrapi_sdk.NfcomPedidoEmissao() # NfcomPedidoEmissao | 

    try:
        # Emitir NFCom
        api_response = api_instance.emitir_nfcom(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfcomApi->emitir_nfcom: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NfcomPedidoEmissao**](NfcomPedidoEmissao.md)|  | 

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

# **listar_nfcom**
> DfeListagem listar_nfcom(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia, chave=chave, serie=serie)

Listar NFCom

Retorna a lista de NFCom de acordo com os critérios de busca utilizados. As NFCom são retornadas ordenadas pela data da criação, com as mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.NfcomApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ do emitente.    Utilize o valor sem máscara.
ambiente = 'ambiente_example' # str | Identificação do Ambiente.    Valores aceitos: homologacao, producao
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)
referencia = 'referencia_example' # str | Seu identificador único para o documento. (optional)
chave = 'chave_example' # str | Chave de acesso do DF-e. (optional)
serie = 'serie_example' # str | Série do DF-e. (optional)

    try:
        # Listar NFCom
        api_response = api_instance.listar_nfcom(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia, chave=chave, serie=serie)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfcomApi->listar_nfcom: %s\n" % e)
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

