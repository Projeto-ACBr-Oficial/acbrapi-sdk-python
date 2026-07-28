# acbrapi_sdk.DistribuioNFEApi

All URIs are relative to *https://prod.acbr.api.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**baixar_pdf_documento_distribuicao_nfe**](DistribuioNFEApi.md#baixar_pdf_documento_distribuicao_nfe) | **GET** /distribuicao/nfe/documentos/{id}/pdf | Baixar PDF do documento
[**baixar_xml_documento_distribuicao_nfe**](DistribuioNFEApi.md#baixar_xml_documento_distribuicao_nfe) | **GET** /distribuicao/nfe/documentos/{id}/xml | Baixar XML do documento
[**consultar_distribuicao_nfe**](DistribuioNFEApi.md#consultar_distribuicao_nfe) | **GET** /distribuicao/nfe/{id} | Consultar distribuição
[**consultar_documento_distribuicao_nfe**](DistribuioNFEApi.md#consultar_documento_distribuicao_nfe) | **GET** /distribuicao/nfe/documentos/{id} | Consultar documento
[**consultar_manifestacao_nfe**](DistribuioNFEApi.md#consultar_manifestacao_nfe) | **GET** /distribuicao/nfe/manifestacoes/{id} | Consultar manifestação
[**gerar_distribuicao_nfe**](DistribuioNFEApi.md#gerar_distribuicao_nfe) | **POST** /distribuicao/nfe | Distribuir documentos
[**listar_distribuicao_nfe**](DistribuioNFEApi.md#listar_distribuicao_nfe) | **GET** /distribuicao/nfe | Listar distribuições
[**listar_documento_distribuicao_nfe**](DistribuioNFEApi.md#listar_documento_distribuicao_nfe) | **GET** /distribuicao/nfe/documentos | Listar documentos
[**listar_manifestacao_nfe**](DistribuioNFEApi.md#listar_manifestacao_nfe) | **GET** /distribuicao/nfe/manifestacoes | Listar Manifestações
[**listar_nfe_sem_manifestacao**](DistribuioNFEApi.md#listar_nfe_sem_manifestacao) | **GET** /distribuicao/nfe/notas-sem-manifestacao | Listar notas sem manifestação
[**manifestar_nfe**](DistribuioNFEApi.md#manifestar_nfe) | **POST** /distribuicao/nfe/manifestacoes | Manifestar nota


# **baixar_pdf_documento_distribuicao_nfe**
> file baixar_pdf_documento_distribuicao_nfe(id)

Baixar PDF do documento

Utilize esse endpoint para obter o PDF do documento.    Schemas suportados:  * procNFe_v4.00.xsd

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
    api_instance = acbrapi_sdk.DistribuioNFEApi(api_client)
    id = 'id_example' # str | ID único do documento gerado pela API.

    try:
        # Baixar PDF do documento
        api_response = api_instance.baixar_pdf_documento_distribuicao_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DistribuioNFEApi->baixar_pdf_documento_distribuicao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do documento gerado pela API. | 

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

# **baixar_xml_documento_distribuicao_nfe**
> file baixar_xml_documento_distribuicao_nfe(id)

Baixar XML do documento

Utilize esse endpoint para obter o XML das informações resumidas ou documento fiscal de interesse da pessoa ou empresa interessada.    **Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.DistribuioNFEApi(api_client)
    id = 'id_example' # str | ID único do documento gerado pela API.

    try:
        # Baixar XML do documento
        api_response = api_instance.baixar_xml_documento_distribuicao_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DistribuioNFEApi->baixar_xml_documento_distribuicao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do documento gerado pela API. | 

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

# **consultar_distribuicao_nfe**
> DistribuicaoNfe consultar_distribuicao_nfe(id)

Consultar distribuição

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
    api_instance = acbrapi_sdk.DistribuioNFEApi(api_client)
    id = 'id_example' # str | ID único da distribuição de NF-e gerada pela API.

    try:
        # Consultar distribuição
        api_response = api_instance.consultar_distribuicao_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DistribuioNFEApi->consultar_distribuicao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da distribuição de NF-e gerada pela API. | 

### Return type

[**DistribuicaoNfe**](DistribuicaoNfe.md)

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

# **consultar_documento_distribuicao_nfe**
> DistribuicaoNfeDocumento consultar_documento_distribuicao_nfe(id)

Consultar documento

Utilize esse endpoint para obter as informações resumidas ou documento fiscal de interesse da pessoa ou empresa interessada.

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
    api_instance = acbrapi_sdk.DistribuioNFEApi(api_client)
    id = 'id_example' # str | ID único do documento gerado pela API.

    try:
        # Consultar documento
        api_response = api_instance.consultar_documento_distribuicao_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DistribuioNFEApi->consultar_documento_distribuicao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do documento gerado pela API. | 

### Return type

[**DistribuicaoNfeDocumento**](DistribuicaoNfeDocumento.md)

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

# **consultar_manifestacao_nfe**
> DistribuicaoNfeEvento consultar_manifestacao_nfe(id)

Consultar manifestação

Consulta os detalhes de uma manifestação de NF-e já existente. Forneça o ID único obtido de uma requisição de manifestação ou de listagem de manifestações e a API irá retornar as informações da manifestação correspondente.

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
    api_instance = acbrapi_sdk.DistribuioNFEApi(api_client)
    id = 'id_example' # str | ID único da manifestação gerado pela API.

    try:
        # Consultar manifestação
        api_response = api_instance.consultar_manifestacao_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DistribuioNFEApi->consultar_manifestacao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da manifestação gerado pela API. | 

### Return type

[**DistribuicaoNfeEvento**](DistribuicaoNfeEvento.md)

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

# **gerar_distribuicao_nfe**
> DistribuicaoNfe gerar_distribuicao_nfe(body)

Distribuir documentos

Este endpoint permite que o destinatário obtenha Documentos Fiscais  Eletrônicos (DF-e) emitidos contra o seu CNPJ ou CPF ou que seja de  seu interesse. A distribuição pode ser feita de três formas:  *dist-nsu*, *cons-nsu* e *cons-chave*.    **Formas de Consulta**:  - *dist-nsu*: Consulta pelo último NSU recebido.  - *cons-nsu*: Consulta por um NSU específico.  - *cons-chave*: Consulta pela chave de acesso da NF-e.    **Retorno da Solicitação**    A resposta da solicitação inclui a propriedade *status* no JSON, que  pode ter os seguintes valores:  - *processando*: A solicitação está em andamento.  - *concluido*: A solicitação foi processada com sucesso.  - *erro*: Ocorreu um erro no processamento da solicitação.    Se o status retornado for *processando*, significa que a solicitação está  sendo realizada de forma assíncrona pela API. Nesse caso, o usuário deverá  adotar um fluxo que consiste em requisitar periodicamente o endpoint  <a href=\"#tag/Distribuicao-NF-e/operation/ConsultarDistribuicaoNfe\">consultar distribuição</a> até que  a API retorne o pedido com um status indicando o fim do  processamento (concluido ou erro).    **Informações adicionais**:  - Consumo: 1 unidade por documento distribuído (retornado) ou requisição.

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
    api_instance = acbrapi_sdk.DistribuioNFEApi(api_client)
    body = acbrapi_sdk.DistribuicaoNfePedido() # DistribuicaoNfePedido | 

    try:
        # Distribuir documentos
        api_response = api_instance.gerar_distribuicao_nfe(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DistribuioNFEApi->gerar_distribuicao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DistribuicaoNfePedido**](DistribuicaoNfePedido.md)|  | 

### Return type

[**DistribuicaoNfe**](DistribuicaoNfe.md)

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

# **listar_distribuicao_nfe**
> DistribuicaoNfeListagem listar_distribuicao_nfe(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount)

Listar distribuições

Retorna a lista de distribuições de NF-e de acordo com os critérios de busca utilizados. As distribuições são retornadas ordenadas pela data da criação, com as mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.DistribuioNFEApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ da pessoa ou empresa interessada.    Utilize o valor sem máscara.
ambiente = 'ambiente_example' # str | Identificação do Ambiente.    Valores aceitos: homologacao, producao
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)

    try:
        # Listar distribuições
        api_response = api_instance.listar_distribuicao_nfe(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DistribuioNFEApi->listar_distribuicao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| Filtrar pelo CPF ou CNPJ da pessoa ou empresa interessada.    Utilize o valor sem máscara. | 
 **ambiente** | **str**| Identificação do Ambiente.    Valores aceitos: homologacao, producao | 
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to False]

### Return type

[**DistribuicaoNfeListagem**](DistribuicaoNfeListagem.md)

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

# **listar_documento_distribuicao_nfe**
> DistribuicaoNfeDocumentoListagem listar_documento_distribuicao_nfe(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, dist_nsu=dist_nsu, tipo_documento=tipo_documento, forma_distribuicao=forma_distribuicao, chave_acesso=chave_acesso)

Listar documentos

Retorna a lista de documentos fiscais eletrônicos de interesse da pessoa ou empresa de acordo com os critérios de busca utilizados. Os documentos são retornadas ordenados pela data da criação, com os mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.DistribuioNFEApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ da pessoa ou empresa interessada.    Utilize o valor sem máscara.
ambiente = 'ambiente_example' # str | Identificação do Ambiente.    Valores aceitos: homologacao, producao
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)
dist_nsu = 56 # int | Filtrar por documentos a partir do NSU informado. (optional)
tipo_documento = 'tipo_documento_example' # str | Filtrar pelo tipo do documento de interesse da pessoa ou empresa.    Valores aceitos: `nota`, `evento` (optional)
forma_distribuicao = 'forma_distribuicao_example' # str | Filtrar por documentos que foram distribuídos em sua forma resumida ou completa.    Valores aceitos: `resumida`, `completa` (optional)
chave_acesso = 'chave_acesso_example' # str | Filtrar pela chave de acesso da NF-e. (optional)

    try:
        # Listar documentos
        api_response = api_instance.listar_documento_distribuicao_nfe(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, dist_nsu=dist_nsu, tipo_documento=tipo_documento, forma_distribuicao=forma_distribuicao, chave_acesso=chave_acesso)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DistribuioNFEApi->listar_documento_distribuicao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| Filtrar pelo CPF ou CNPJ da pessoa ou empresa interessada.    Utilize o valor sem máscara. | 
 **ambiente** | **str**| Identificação do Ambiente.    Valores aceitos: homologacao, producao | 
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to False]
 **dist_nsu** | **int**| Filtrar por documentos a partir do NSU informado. | [optional] 
 **tipo_documento** | **str**| Filtrar pelo tipo do documento de interesse da pessoa ou empresa.    Valores aceitos: &#x60;nota&#x60;, &#x60;evento&#x60; | [optional] 
 **forma_distribuicao** | **str**| Filtrar por documentos que foram distribuídos em sua forma resumida ou completa.    Valores aceitos: &#x60;resumida&#x60;, &#x60;completa&#x60; | [optional] 
 **chave_acesso** | **str**| Filtrar pela chave de acesso da NF-e. | [optional] 

### Return type

[**DistribuicaoNfeDocumentoListagem**](DistribuicaoNfeDocumentoListagem.md)

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

# **listar_manifestacao_nfe**
> ManifestacaoNfeListagem listar_manifestacao_nfe(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount)

Listar Manifestações

Retorna a lista de manifestações de NF-e de acordo com os critérios de busca utilizados. As manifestações são retornadas ordenadas pela data da criação, com as mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.DistribuioNFEApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ do autor do evento.    Utilize o valor sem máscara.
ambiente = 'ambiente_example' # str | Identificação do Ambiente.    Valores aceitos: homologacao, producao
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)

    try:
        # Listar Manifestações
        api_response = api_instance.listar_manifestacao_nfe(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DistribuioNFEApi->listar_manifestacao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| Filtrar pelo CPF ou CNPJ do autor do evento.    Utilize o valor sem máscara. | 
 **ambiente** | **str**| Identificação do Ambiente.    Valores aceitos: homologacao, producao | 
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to False]

### Return type

[**ManifestacaoNfeListagem**](ManifestacaoNfeListagem.md)

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

# **listar_nfe_sem_manifestacao**
> DistribuicaoNfeNotaListagem listar_nfe_sem_manifestacao(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, conclusiva=conclusiva)

Listar notas sem manifestação

No processo de distribuição de DF-e, as notas fiscais eletrônicas (NF-e)  são inicialmente disponibilizadas de forma resumida. Para obter o XML  completo, o destinatário deve manifestar a ciência da operação e,  posteriormente, uma manifestação conclusiva dentro de um prazo legal.    Para facilitar essa gestão e o cumprimento dos prazos legais de manifestação,  a API permite listar as notas que ainda não  possuem manifestação, ajudando os usuários a identificar rapidamente as  notas que necessitam de ação.    O usuário pode optar por listar apenas as notas que não possuem manifestação  conclusiva ou que não possuem qualquer tipo de manifestação. Essa flexibilidade  permite um controle mais preciso e adequado às necessidades operacionais  de cada empresa.    Os documentos são retornados ordenados decrescentemente pela data de  distribuição, permitindo uma visualização clara e organizada das notas  mais recentes.    **Cenários de uso:**  * Identificar rapidamente as notas que ainda precisam de manifestação para obter o XML completo.  * Listar todas as notas fiscais eletrônicas que foram registradas com ciência da operação, mas ainda não possuem uma manifestação conclusiva (confirmação da operação, desconhecimento da operação ou operação não realizada).  * Listar todas as notas fiscais eletrônicas que não possuem nenhum tipo de manifestação registrada (nem ciência da operação, nem manifestação conclusiva).

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
    api_instance = acbrapi_sdk.DistribuioNFEApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ da pessoa ou empresa interessada.    Utilize o valor sem máscara.
ambiente = 'ambiente_example' # str | Identificação do Ambiente.    Valores aceitos: homologacao, producao
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)
conclusiva = False # bool | Indica se serão consideradas apenas as manifestações conclusivas.    Valores:  * `false`: serão retornadas notas que não possuírem qualquer tipo de    manifestação.    * `true`: apenas as notas que não possuírem manifestação conclusiva    serão retornadas. Ou seja, notas que tenham sido manifestadas apenas    com Ciência da Operação (210210) continuarão sendo retornadas por    esse endpoint até que recebam uma manifestação conclusiva. (optional) (default to False)

    try:
        # Listar notas sem manifestação
        api_response = api_instance.listar_nfe_sem_manifestacao(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, conclusiva=conclusiva)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DistribuioNFEApi->listar_nfe_sem_manifestacao: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| Filtrar pelo CPF ou CNPJ da pessoa ou empresa interessada.    Utilize o valor sem máscara. | 
 **ambiente** | **str**| Identificação do Ambiente.    Valores aceitos: homologacao, producao | 
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to False]
 **conclusiva** | **bool**| Indica se serão consideradas apenas as manifestações conclusivas.    Valores:  * &#x60;false&#x60;: serão retornadas notas que não possuírem qualquer tipo de    manifestação.    * &#x60;true&#x60;: apenas as notas que não possuírem manifestação conclusiva    serão retornadas. Ou seja, notas que tenham sido manifestadas apenas    com Ciência da Operação (210210) continuarão sendo retornadas por    esse endpoint até que recebam uma manifestação conclusiva. | [optional] [default to False]

### Return type

[**DistribuicaoNfeNotaListagem**](DistribuicaoNfeNotaListagem.md)

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

# **manifestar_nfe**
> DistribuicaoNfeEvento manifestar_nfe(body)

Manifestar nota

O processo de manifestação do destinatário permite que os destinatários  de Notas Fiscais Eletrônicas (NF-e) registrem formalmente sua posição em  relação às operações descritas nesses documentos fiscais. Ele envolve  eventos que indicam se a operação foi confirmada, desconhecida ou  não realizada.    Os seguintes tipos de manifestação são suportados pela NF-e:  * **Confirmação da Operação (210200)**: Manifestação do destinatário confirmando que a operação descrita na NF-e ocorreu exatamente como informado na NF-e. Esse evento libera a possibilidade de download da NF-e pelo destinatário e impede que a empresa emitente cancele a NF-e após a confirmação.  * **Ciência da Operação (210210)**: Declara que o destinatário tem ciência da existência da NF-e, mas ainda não possui elementos suficientes para manifestar-se conclusivamente. Este é um evento opcional que pode ser usado pelo destinatário para indicar que está ciente da NF-e enquanto coleta mais informações. Esse evento libera a possibilidade de download da NF-e pelo destinatário.  * **Desconhecimento da Operação (210220)**: Manifestação do destinatário declarando que a operação descrita da NF-e não foi por ele solicitada.  * **Operação não Realizada (210240)**: Manifestação do destinatário reconhecendo sua participação na operação descrita na NF-e, mas declarando que a operação não ocorreu ou não se efetivou como informado nesta NF-e.    **Informações adicionais**:  - Consumo: 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.DistribuioNFEApi(api_client)
    body = acbrapi_sdk.DistribuicaoNfePedidoManifestacao() # DistribuicaoNfePedidoManifestacao | Contém os dados do pedido para manifestação do destinatário.

    try:
        # Manifestar nota
        api_response = api_instance.manifestar_nfe(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DistribuioNFEApi->manifestar_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DistribuicaoNfePedidoManifestacao**](DistribuicaoNfePedidoManifestacao.md)| Contém os dados do pedido para manifestação do destinatário. | 

### Return type

[**DistribuicaoNfeEvento**](DistribuicaoNfeEvento.md)

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

