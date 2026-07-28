# acbrapi_sdk.EmpresaApi

All URIs are relative to *https://prod.acbr.api.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**alterar_config_cte**](EmpresaApi.md#alterar_config_cte) | **PUT** /empresas/{cpf_cnpj}/cte | Alterar configuração de CT-e
[**alterar_config_cte_os**](EmpresaApi.md#alterar_config_cte_os) | **PUT** /empresas/{cpf_cnpj}/cteos | Alterar configuração de CT-e OS
[**alterar_config_dce**](EmpresaApi.md#alterar_config_dce) | **PUT** /empresas/{cpf_cnpj}/dce | Alterar configuração de DC-e
[**alterar_config_distribuicao_nfe**](EmpresaApi.md#alterar_config_distribuicao_nfe) | **PUT** /empresas/{cpf_cnpj}/distnfe | Alterar configuração de Distribuição de NF-e
[**alterar_config_mdfe**](EmpresaApi.md#alterar_config_mdfe) | **PUT** /empresas/{cpf_cnpj}/mdfe | Alterar configuração de MDF-e
[**alterar_config_nfce**](EmpresaApi.md#alterar_config_nfce) | **PUT** /empresas/{cpf_cnpj}/nfce | Alterar configuração de NFC-e
[**alterar_config_nfcom**](EmpresaApi.md#alterar_config_nfcom) | **PUT** /empresas/{cpf_cnpj}/nfcom | Alterar configuração de NFCom
[**alterar_config_nfe**](EmpresaApi.md#alterar_config_nfe) | **PUT** /empresas/{cpf_cnpj}/nfe | Alterar configuração de NF-e
[**alterar_config_nfse**](EmpresaApi.md#alterar_config_nfse) | **PUT** /empresas/{cpf_cnpj}/nfse | Alterar configuração de NFS-e
[**atualizar_empresa**](EmpresaApi.md#atualizar_empresa) | **PUT** /empresas/{cpf_cnpj} | Alterar empresa
[**baixar_logotipo_empresa**](EmpresaApi.md#baixar_logotipo_empresa) | **GET** /empresas/{cpf_cnpj}/logotipo | Baixar logotipo
[**cadastrar_certificado_empresa**](EmpresaApi.md#cadastrar_certificado_empresa) | **PUT** /empresas/{cpf_cnpj}/certificado | Cadastrar certificado
[**consultar_certificado_empresa**](EmpresaApi.md#consultar_certificado_empresa) | **GET** /empresas/{cpf_cnpj}/certificado | Consultar certificado
[**consultar_config_cte**](EmpresaApi.md#consultar_config_cte) | **GET** /empresas/{cpf_cnpj}/cte | Consultar configuração de CT-e
[**consultar_config_cte_os**](EmpresaApi.md#consultar_config_cte_os) | **GET** /empresas/{cpf_cnpj}/cteos | Consultar configuração de CT-e OS
[**consultar_config_dce**](EmpresaApi.md#consultar_config_dce) | **GET** /empresas/{cpf_cnpj}/dce | Consultar configuração de DC-e
[**consultar_config_distribuicao_nfe**](EmpresaApi.md#consultar_config_distribuicao_nfe) | **GET** /empresas/{cpf_cnpj}/distnfe | Consultar configuração de Distribuição de NF-e
[**consultar_config_mdfe**](EmpresaApi.md#consultar_config_mdfe) | **GET** /empresas/{cpf_cnpj}/mdfe | Consultar configuração de MDF-e
[**consultar_config_nfce**](EmpresaApi.md#consultar_config_nfce) | **GET** /empresas/{cpf_cnpj}/nfce | Consultar configuração de NFC-e
[**consultar_config_nfcom**](EmpresaApi.md#consultar_config_nfcom) | **GET** /empresas/{cpf_cnpj}/nfcom | Consultar configuração de NFCom
[**consultar_config_nfe**](EmpresaApi.md#consultar_config_nfe) | **GET** /empresas/{cpf_cnpj}/nfe | Consultar configuração de NF-e
[**consultar_config_nfse**](EmpresaApi.md#consultar_config_nfse) | **GET** /empresas/{cpf_cnpj}/nfse | Consultar configuração de NFS-e
[**consultar_empresa**](EmpresaApi.md#consultar_empresa) | **GET** /empresas/{cpf_cnpj} | Consultar empresa
[**criar_empresa**](EmpresaApi.md#criar_empresa) | **POST** /empresas | Cadastrar empresa
[**enviar_certificado_empresa**](EmpresaApi.md#enviar_certificado_empresa) | **PUT** /empresas/{cpf_cnpj}/certificado/upload | Upload de certificado
[**enviar_logotipo_empresa**](EmpresaApi.md#enviar_logotipo_empresa) | **PUT** /empresas/{cpf_cnpj}/logotipo | Enviar logotipo
[**excluir_certificado_empresa**](EmpresaApi.md#excluir_certificado_empresa) | **DELETE** /empresas/{cpf_cnpj}/certificado | Deletar certificado
[**excluir_empresa**](EmpresaApi.md#excluir_empresa) | **DELETE** /empresas/{cpf_cnpj} | Deletar empresa
[**excluir_logotipo_empresa**](EmpresaApi.md#excluir_logotipo_empresa) | **DELETE** /empresas/{cpf_cnpj}/logotipo | Deletar logotipo
[**listar_certificados**](EmpresaApi.md#listar_certificados) | **GET** /empresas/certificados | Listar certificados
[**listar_empresas**](EmpresaApi.md#listar_empresas) | **GET** /empresas | Listar empresas


# **alterar_config_cte**
> EmpresaConfigCte alterar_config_cte(cpf_cnpj, body)

Alterar configuração de CT-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigCte() # EmpresaConfigCte | 

    try:
        # Alterar configuração de CT-e
        api_response = api_instance.alterar_config_cte(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->alterar_config_cte: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigCte**](EmpresaConfigCte.md)|  | 

### Return type

[**EmpresaConfigCte**](EmpresaConfigCte.md)

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

# **alterar_config_cte_os**
> EmpresaConfigCteOs alterar_config_cte_os(cpf_cnpj, body)

Alterar configuração de CT-e OS

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigCteOs() # EmpresaConfigCteOs | 

    try:
        # Alterar configuração de CT-e OS
        api_response = api_instance.alterar_config_cte_os(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->alterar_config_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigCteOs**](EmpresaConfigCteOs.md)|  | 

### Return type

[**EmpresaConfigCteOs**](EmpresaConfigCteOs.md)

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

# **alterar_config_dce**
> EmpresaConfigDce alterar_config_dce(cpf_cnpj, body)

Alterar configuração de DC-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigDce() # EmpresaConfigDce | 

    try:
        # Alterar configuração de DC-e
        api_response = api_instance.alterar_config_dce(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->alterar_config_dce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigDce**](EmpresaConfigDce.md)|  | 

### Return type

[**EmpresaConfigDce**](EmpresaConfigDce.md)

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

# **alterar_config_distribuicao_nfe**
> EmpresaConfigDistribuicaoNfe alterar_config_distribuicao_nfe(cpf_cnpj, body)

Alterar configuração de Distribuição de NF-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigDistribuicaoNfe() # EmpresaConfigDistribuicaoNfe | 

    try:
        # Alterar configuração de Distribuição de NF-e
        api_response = api_instance.alterar_config_distribuicao_nfe(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->alterar_config_distribuicao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigDistribuicaoNfe**](EmpresaConfigDistribuicaoNfe.md)|  | 

### Return type

[**EmpresaConfigDistribuicaoNfe**](EmpresaConfigDistribuicaoNfe.md)

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

# **alterar_config_mdfe**
> EmpresaConfigMdfe alterar_config_mdfe(cpf_cnpj, body)

Alterar configuração de MDF-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigMdfe() # EmpresaConfigMdfe | 

    try:
        # Alterar configuração de MDF-e
        api_response = api_instance.alterar_config_mdfe(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->alterar_config_mdfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigMdfe**](EmpresaConfigMdfe.md)|  | 

### Return type

[**EmpresaConfigMdfe**](EmpresaConfigMdfe.md)

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

# **alterar_config_nfce**
> EmpresaConfigNfce alterar_config_nfce(cpf_cnpj, body)

Alterar configuração de NFC-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigNfce() # EmpresaConfigNfce | 

    try:
        # Alterar configuração de NFC-e
        api_response = api_instance.alterar_config_nfce(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->alterar_config_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigNfce**](EmpresaConfigNfce.md)|  | 

### Return type

[**EmpresaConfigNfce**](EmpresaConfigNfce.md)

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

# **alterar_config_nfcom**
> EmpresaConfigNfcom alterar_config_nfcom(cpf_cnpj, body)

Alterar configuração de NFCom

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigNfcom() # EmpresaConfigNfcom | 

    try:
        # Alterar configuração de NFCom
        api_response = api_instance.alterar_config_nfcom(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->alterar_config_nfcom: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigNfcom**](EmpresaConfigNfcom.md)|  | 

### Return type

[**EmpresaConfigNfcom**](EmpresaConfigNfcom.md)

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

# **alterar_config_nfe**
> EmpresaConfigNfe alterar_config_nfe(cpf_cnpj, body)

Alterar configuração de NF-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigNfe() # EmpresaConfigNfe | 

    try:
        # Alterar configuração de NF-e
        api_response = api_instance.alterar_config_nfe(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->alterar_config_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigNfe**](EmpresaConfigNfe.md)|  | 

### Return type

[**EmpresaConfigNfe**](EmpresaConfigNfe.md)

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

# **alterar_config_nfse**
> EmpresaConfigNfse alterar_config_nfse(cpf_cnpj, body)

Alterar configuração de NFS-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigNfse() # EmpresaConfigNfse | 

    try:
        # Alterar configuração de NFS-e
        api_response = api_instance.alterar_config_nfse(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->alterar_config_nfse: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigNfse**](EmpresaConfigNfse.md)|  | 

### Return type

[**EmpresaConfigNfse**](EmpresaConfigNfse.md)

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

# **atualizar_empresa**
> Empresa atualizar_empresa(cpf_cnpj, body)

Alterar empresa

Altera o cadastro de uma empresa (emitente/prestador) que esteja associada a sua conta.  Nesse método, por tratar-se de um PUT, caso algum campo não seja informado, o valor dele será apagado.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.Empresa() # Empresa | 

    try:
        # Alterar empresa
        api_response = api_instance.atualizar_empresa(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->atualizar_empresa: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**Empresa**](Empresa.md)|  | 

### Return type

[**Empresa**](Empresa.md)

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

# **baixar_logotipo_empresa**
> file baixar_logotipo_empresa(cpf_cnpj)

Baixar logotipo

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Baixar logotipo
        api_response = api_instance.baixar_logotipo_empresa(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->baixar_logotipo_empresa: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

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

# **cadastrar_certificado_empresa**
> EmpresaCertificado cadastrar_certificado_empresa(cpf_cnpj, body)

Cadastrar certificado

Cadastre ou atualize um certificado digital e vincule a sua empresa, para que possa iniciar a emissão de notas.  * No parâmetro `certificado`, envie o binário do certificado digital (.pfx ou .p12) codificado em **base64**.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaPedidoCadastroCertificado() # EmpresaPedidoCadastroCertificado | 

    try:
        # Cadastrar certificado
        api_response = api_instance.cadastrar_certificado_empresa(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->cadastrar_certificado_empresa: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaPedidoCadastroCertificado**](EmpresaPedidoCadastroCertificado.md)|  | 

### Return type

[**EmpresaCertificado**](EmpresaCertificado.md)

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

# **consultar_certificado_empresa**
> EmpresaCertificado consultar_certificado_empresa(cpf_cnpj)

Consultar certificado

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar certificado
        api_response = api_instance.consultar_certificado_empresa(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->consultar_certificado_empresa: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

[**EmpresaCertificado**](EmpresaCertificado.md)

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

# **consultar_config_cte**
> EmpresaConfigCte consultar_config_cte(cpf_cnpj)

Consultar configuração de CT-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de CT-e
        api_response = api_instance.consultar_config_cte(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->consultar_config_cte: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

[**EmpresaConfigCte**](EmpresaConfigCte.md)

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

# **consultar_config_cte_os**
> EmpresaConfigCteOs consultar_config_cte_os(cpf_cnpj)

Consultar configuração de CT-e OS

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de CT-e OS
        api_response = api_instance.consultar_config_cte_os(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->consultar_config_cte_os: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

[**EmpresaConfigCteOs**](EmpresaConfigCteOs.md)

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

# **consultar_config_dce**
> EmpresaConfigDce consultar_config_dce(cpf_cnpj)

Consultar configuração de DC-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de DC-e
        api_response = api_instance.consultar_config_dce(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->consultar_config_dce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

[**EmpresaConfigDce**](EmpresaConfigDce.md)

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

# **consultar_config_distribuicao_nfe**
> EmpresaConfigDistribuicaoNfe consultar_config_distribuicao_nfe(cpf_cnpj)

Consultar configuração de Distribuição de NF-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de Distribuição de NF-e
        api_response = api_instance.consultar_config_distribuicao_nfe(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->consultar_config_distribuicao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

[**EmpresaConfigDistribuicaoNfe**](EmpresaConfigDistribuicaoNfe.md)

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

# **consultar_config_mdfe**
> EmpresaConfigMdfe consultar_config_mdfe(cpf_cnpj)

Consultar configuração de MDF-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de MDF-e
        api_response = api_instance.consultar_config_mdfe(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->consultar_config_mdfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

[**EmpresaConfigMdfe**](EmpresaConfigMdfe.md)

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

# **consultar_config_nfce**
> EmpresaConfigNfce consultar_config_nfce(cpf_cnpj)

Consultar configuração de NFC-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de NFC-e
        api_response = api_instance.consultar_config_nfce(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->consultar_config_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

[**EmpresaConfigNfce**](EmpresaConfigNfce.md)

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

# **consultar_config_nfcom**
> EmpresaConfigNfcom consultar_config_nfcom(cpf_cnpj)

Consultar configuração de NFCom

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de NFCom
        api_response = api_instance.consultar_config_nfcom(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->consultar_config_nfcom: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

[**EmpresaConfigNfcom**](EmpresaConfigNfcom.md)

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

# **consultar_config_nfe**
> EmpresaConfigNfe consultar_config_nfe(cpf_cnpj)

Consultar configuração de NF-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de NF-e
        api_response = api_instance.consultar_config_nfe(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->consultar_config_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

[**EmpresaConfigNfe**](EmpresaConfigNfe.md)

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

# **consultar_config_nfse**
> EmpresaConfigNfse consultar_config_nfse(cpf_cnpj)

Consultar configuração de NFS-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de NFS-e
        api_response = api_instance.consultar_config_nfse(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->consultar_config_nfse: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

[**EmpresaConfigNfse**](EmpresaConfigNfse.md)

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

# **consultar_empresa**
> Empresa consultar_empresa(cpf_cnpj)

Consultar empresa

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar empresa
        api_response = api_instance.consultar_empresa(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->consultar_empresa: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

[**Empresa**](Empresa.md)

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

# **criar_empresa**
> Empresa criar_empresa(body)

Cadastrar empresa

Cadastre uma nova empresa (emitente ou prestador) à sua conta.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    body = acbrapi_sdk.Empresa() # Empresa | 

    try:
        # Cadastrar empresa
        api_response = api_instance.criar_empresa(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->criar_empresa: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Empresa**](Empresa.md)|  | 

### Return type

[**Empresa**](Empresa.md)

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

# **enviar_certificado_empresa**
> EmpresaCertificado enviar_certificado_empresa(cpf_cnpj, input=input)

Upload de certificado

Cadastre ou atualize um certificado digital e vincule a sua empresa, para que possa iniciar a emissão de notas.  * Utilize o `content-type` igual a `multipart/form-data`.  * No parâmetro `file`, envie o binário do arquivo (.pfx ou .p12) do certificado digital.  * No parâmetro `password`, envie a senha do certificado.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
input = '/path/to/file' # file |  (optional)

    try:
        # Upload de certificado
        api_response = api_instance.enviar_certificado_empresa(cpf_cnpj, input=input)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->enviar_certificado_empresa: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **input** | **file**|  | [optional] 

### Return type

[**EmpresaCertificado**](EmpresaCertificado.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enviar_logotipo_empresa**
> enviar_logotipo_empresa(cpf_cnpj, input=input)

Enviar logotipo

Cadastre ou atualize um logotipo e vincule a sua empresa.    **Restrições:**  * Tipos de mídia (MIME) suportados: `image/png` e `image/jpeg`  * Tamanho máximo do arquivo: 200 KB    **Cenários de uso:**  * Quero que minhas notas sejam impressas com esse logotipo.  * Quero trocar o logotipo utilizado em minhas impressões.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
input = '/path/to/file' # file |  (optional)

    try:
        # Enviar logotipo
        api_instance.enviar_logotipo_empresa(cpf_cnpj, input=input)
    except ApiException as e:
        print("Exception when calling EmpresaApi->enviar_logotipo_empresa: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **input** | **file**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **excluir_certificado_empresa**
> excluir_certificado_empresa(cpf_cnpj)

Deletar certificado

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Deletar certificado
        api_instance.excluir_certificado_empresa(cpf_cnpj)
    except ApiException as e:
        print("Exception when calling EmpresaApi->excluir_certificado_empresa: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **excluir_empresa**
> excluir_empresa(cpf_cnpj)

Deletar empresa

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Deletar empresa
        api_instance.excluir_empresa(cpf_cnpj)
    except ApiException as e:
        print("Exception when calling EmpresaApi->excluir_empresa: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **excluir_logotipo_empresa**
> excluir_logotipo_empresa(cpf_cnpj)

Deletar logotipo

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Deletar logotipo
        api_instance.excluir_logotipo_empresa(cpf_cnpj)
    except ApiException as e:
        print("Exception when calling EmpresaApi->excluir_logotipo_empresa: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listar_certificados**
> EmpresaCertificadoListagem listar_certificados(top=top, skip=skip, inlinecount=inlinecount, expires_in=expires_in, include_expired=include_expired)

Listar certificados

Retorna a lista dos certificados associadas à sua conta. Os certificados são retornados ordenados pela data da criação, com as mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)
expires_in = 56 # int | Filtrar certificados que expiram dentro de X dias.    Informe um número inteiro correspondente à quantidade de dias até o vencimento.  Exemplos:   - expires_in=30 -&gt; certificados que vencem nos próximos 30 dias.   - expires_in=7  -&gt; certificados que vencem nos próximos 7 dias. (optional)
include_expired = True # bool | Indicar se os certificados já vencidos devem ser incluídos no resultado.    Valores aceitos:   - `true`: incluir certificados vencidos.   - `false`: exibir apenas certificados válidos. (optional) (default to True)

    try:
        # Listar certificados
        api_response = api_instance.listar_certificados(top=top, skip=skip, inlinecount=inlinecount, expires_in=expires_in, include_expired=include_expired)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->listar_certificados: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to False]
 **expires_in** | **int**| Filtrar certificados que expiram dentro de X dias.    Informe um número inteiro correspondente à quantidade de dias até o vencimento.  Exemplos:   - expires_in&#x3D;30 -&amp;gt; certificados que vencem nos próximos 30 dias.   - expires_in&#x3D;7  -&amp;gt; certificados que vencem nos próximos 7 dias. | [optional] 
 **include_expired** | **bool**| Indicar se os certificados já vencidos devem ser incluídos no resultado.    Valores aceitos:   - &#x60;true&#x60;: incluir certificados vencidos.   - &#x60;false&#x60;: exibir apenas certificados válidos. | [optional] [default to True]

### Return type

[**EmpresaCertificadoListagem**](EmpresaCertificadoListagem.md)

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

# **listar_empresas**
> EmpresaListagem listar_empresas(top=top, skip=skip, inlinecount=inlinecount, cpf_cnpj=cpf_cnpj, nome_razao_social=nome_razao_social)

Listar empresas

Retorna a lista das empresas associadas à sua conta. As empresas são retornadas ordenadas pela data da criação, com as mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)
cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*. (optional)
nome_razao_social = 'nome_razao_social_example' # str | Filtrar pelo nome ou razão social da empresa.    Esse filtro realiza uma correspondência pelo início do texto,  retornando apenas empresas cujo nome ou razão social começam com  o valor informado.    *Caso o filtro pelo CPF ou CNPJ também seja informado na requisição,  este filtro é ignorado*. (optional)

    try:
        # Listar empresas
        api_response = api_instance.listar_empresas(top=top, skip=skip, inlinecount=inlinecount, cpf_cnpj=cpf_cnpj, nome_razao_social=nome_razao_social)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EmpresaApi->listar_empresas: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to False]
 **cpf_cnpj** | **str**| Filtrar pelo CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*. | [optional] 
 **nome_razao_social** | **str**| Filtrar pelo nome ou razão social da empresa.    Esse filtro realiza uma correspondência pelo início do texto,  retornando apenas empresas cujo nome ou razão social começam com  o valor informado.    *Caso o filtro pelo CPF ou CNPJ também seja informado na requisição,  este filtro é ignorado*. | [optional] 

### Return type

[**EmpresaListagem**](EmpresaListagem.md)

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

