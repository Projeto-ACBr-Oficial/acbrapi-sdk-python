# acbrapi_sdk.NfeApi

All URIs are relative to *https://prod.acbr.api.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**baixar_pdf_cancelamento_nfe**](NfeApi.md#baixar_pdf_cancelamento_nfe) | **GET** /nfe/{id}/cancelamento/pdf | Baixar PDF do cancelamento
[**baixar_pdf_carta_correcao_nfe**](NfeApi.md#baixar_pdf_carta_correcao_nfe) | **GET** /nfe/{id}/carta-correcao/pdf | Baixar PDF da carta de correção
[**baixar_pdf_evento_nfe**](NfeApi.md#baixar_pdf_evento_nfe) | **GET** /nfe/eventos/{id}/pdf | Baixar PDF do evento
[**baixar_pdf_inutilizacao_nfe**](NfeApi.md#baixar_pdf_inutilizacao_nfe) | **GET** /nfe/inutilizacoes/{id}/pdf | Baixar PDF da inutilização
[**baixar_pdf_nfe**](NfeApi.md#baixar_pdf_nfe) | **GET** /nfe/{id}/pdf | Baixar PDF do DANFE
[**baixar_previa_pdf_nfe**](NfeApi.md#baixar_previa_pdf_nfe) | **POST** /nfe/previa/pdf | Prévia do PDF do DANFE
[**baixar_previa_xml_nfe**](NfeApi.md#baixar_previa_xml_nfe) | **POST** /nfe/previa/xml | Prévia do XML da NF-e
[**baixar_xml_cancelamento_nfe**](NfeApi.md#baixar_xml_cancelamento_nfe) | **GET** /nfe/{id}/cancelamento/xml | Baixar XML do cancelamento
[**baixar_xml_carta_correcao_nfe**](NfeApi.md#baixar_xml_carta_correcao_nfe) | **GET** /nfe/{id}/carta-correcao/xml | Baixar XML da carta de correção
[**baixar_xml_evento_nfe**](NfeApi.md#baixar_xml_evento_nfe) | **GET** /nfe/eventos/{id}/xml | Baixar XML do evento
[**baixar_xml_inutilizacao_nfe**](NfeApi.md#baixar_xml_inutilizacao_nfe) | **GET** /nfe/inutilizacoes/{id}/xml | Baixar XML da inutilização
[**baixar_xml_nfe**](NfeApi.md#baixar_xml_nfe) | **GET** /nfe/{id}/xml | Baixar XML da NF-e processada
[**baixar_xml_nfe_nota**](NfeApi.md#baixar_xml_nfe_nota) | **GET** /nfe/{id}/xml/nota | Baixar XML da NF-e
[**baixar_xml_nfe_protocolo**](NfeApi.md#baixar_xml_nfe_protocolo) | **GET** /nfe/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
[**cancelar_nfe**](NfeApi.md#cancelar_nfe) | **POST** /nfe/{id}/cancelamento | Cancelar uma NF-e autorizada
[**consultar_cancelamento_nfe**](NfeApi.md#consultar_cancelamento_nfe) | **GET** /nfe/{id}/cancelamento | Consultar o cancelamento da NF-e
[**consultar_carta_correcao_nfe**](NfeApi.md#consultar_carta_correcao_nfe) | **GET** /nfe/{id}/carta-correcao | Consultar a solicitação de correção da NF-e
[**consultar_contribuinte_nfe**](NfeApi.md#consultar_contribuinte_nfe) | **GET** /nfe/cadastro-contribuinte | Consultar contribuinte
[**consultar_evento_nfe**](NfeApi.md#consultar_evento_nfe) | **GET** /nfe/eventos/{id} | Consultar evento
[**consultar_inutilizacao_nfe**](NfeApi.md#consultar_inutilizacao_nfe) | **GET** /nfe/inutilizacoes/{id} | Consultar a inutilização de sequência de numeração
[**consultar_lote_nfe**](NfeApi.md#consultar_lote_nfe) | **GET** /nfe/lotes/{id} | Consultar lote de NF-e
[**consultar_nfe**](NfeApi.md#consultar_nfe) | **GET** /nfe/{id} | Consultar NF-e
[**consultar_status_sefaz_nfe**](NfeApi.md#consultar_status_sefaz_nfe) | **GET** /nfe/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
[**criar_carta_correcao_nfe**](NfeApi.md#criar_carta_correcao_nfe) | **POST** /nfe/{id}/carta-correcao | Solicitar correção da NF-e
[**emitir_lote_nfe**](NfeApi.md#emitir_lote_nfe) | **POST** /nfe/lotes | Emitir lote de NF-e
[**emitir_nfe**](NfeApi.md#emitir_nfe) | **POST** /nfe | Emitir NF-e
[**enviar_email_nfe**](NfeApi.md#enviar_email_nfe) | **POST** /nfe/{id}/email | Enviar e-mail
[**inutilizar_numeracao_nfe**](NfeApi.md#inutilizar_numeracao_nfe) | **POST** /nfe/inutilizacoes | Inutilizar uma sequência de numeração de NF-e
[**listar_eventos_nfe**](NfeApi.md#listar_eventos_nfe) | **GET** /nfe/eventos | Listar eventos
[**listar_lotes_nfe**](NfeApi.md#listar_lotes_nfe) | **GET** /nfe/lotes | Listar lotes de NF-e
[**listar_nfe**](NfeApi.md#listar_nfe) | **GET** /nfe | Listar NF-e
[**sincronizar_nfe**](NfeApi.md#sincronizar_nfe) | **POST** /nfe/{id}/sincronizar | Sincroniza dados na NF-e a partir da SEFAZ


# **baixar_pdf_cancelamento_nfe**
> file baixar_pdf_cancelamento_nfe(id)

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.

    try:
        # Baixar PDF do cancelamento
        api_response = api_instance.baixar_pdf_cancelamento_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_pdf_cancelamento_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 

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

# **baixar_pdf_carta_correcao_nfe**
> file baixar_pdf_carta_correcao_nfe(id)

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.

    try:
        # Baixar PDF da carta de correção
        api_response = api_instance.baixar_pdf_carta_correcao_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_pdf_carta_correcao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 

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

# **baixar_pdf_evento_nfe**
> file baixar_pdf_evento_nfe(id)

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Baixar PDF do evento
        api_response = api_instance.baixar_pdf_evento_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_pdf_evento_nfe: %s\n" % e)
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

# **baixar_pdf_inutilizacao_nfe**
> file baixar_pdf_inutilizacao_nfe(id)

Baixar PDF da inutilização

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Baixar PDF da inutilização
        api_response = api_instance.baixar_pdf_inutilizacao_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_pdf_inutilizacao_nfe: %s\n" % e)
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

# **baixar_pdf_nfe**
> file baixar_pdf_nfe(id, logotipo=logotipo, nome_fantasia=nome_fantasia, formato=formato, mensagem_rodape=mensagem_rodape, canhoto=canhoto)

Baixar PDF do DANFE

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.
logotipo = False # bool | Imprime o documento com logotipo, desde que esteja cadastrado na empresa. (optional) (default to False)
nome_fantasia = False # bool | Exibe o nome fantasia do emitente, desde que esteja presente no XML da nota. (optional) (default to False)
formato = 'padrao' # str | Formato de impressão do DANFE.    Valores disponíveis:  - `padrao`: será utilizado o formato definido no XML da NF-e (tag \"tpImp\");  - `retrato`: tamanho A4 em modo retrato;  - `paisagem`: tamanho A4 em modo paisagem;  - `simplificado`: formato simplificado utilizado nas operações realizadas fora do estabelecimento (Anexo II do MOC, item 3.11);  - `etiqueta`: formato simplificado utilizado nas operações em comércio eletrônico (Anexo II do MOC, item 3.12 e NT 2020.004). (optional) (default to 'padrao')
mensagem_rodape = 'mensagem_rodape_example' # str | Imprime mensagem no rodapé do documento.    O caractere `|` (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * `\"esquerda\"`  * `\"esquerda|centro\"`  * `\"esquerda|centro|direita\"`  * `\"|centro\"`, `\"|centro|\"`  * `\"|centro|direita\"`  * `\"||direita\"`  * `\"esquerda||direita\"` (optional)
canhoto = True # bool | Imprime o documento com o bloco de canhoto. (optional) (default to True)

    try:
        # Baixar PDF do DANFE
        api_response = api_instance.baixar_pdf_nfe(id, logotipo=logotipo, nome_fantasia=nome_fantasia, formato=formato, mensagem_rodape=mensagem_rodape, canhoto=canhoto)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_pdf_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 
 **logotipo** | **bool**| Imprime o documento com logotipo, desde que esteja cadastrado na empresa. | [optional] [default to False]
 **nome_fantasia** | **bool**| Exibe o nome fantasia do emitente, desde que esteja presente no XML da nota. | [optional] [default to False]
 **formato** | **str**| Formato de impressão do DANFE.    Valores disponíveis:  - &#x60;padrao&#x60;: será utilizado o formato definido no XML da NF-e (tag \&quot;tpImp\&quot;);  - &#x60;retrato&#x60;: tamanho A4 em modo retrato;  - &#x60;paisagem&#x60;: tamanho A4 em modo paisagem;  - &#x60;simplificado&#x60;: formato simplificado utilizado nas operações realizadas fora do estabelecimento (Anexo II do MOC, item 3.11);  - &#x60;etiqueta&#x60;: formato simplificado utilizado nas operações em comércio eletrônico (Anexo II do MOC, item 3.12 e NT 2020.004). | [optional] [default to &#39;padrao&#39;]
 **mensagem_rodape** | **str**| Imprime mensagem no rodapé do documento.    O caractere &#x60;|&#x60; (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * &#x60;\&quot;esquerda\&quot;&#x60;  * &#x60;\&quot;esquerda|centro\&quot;&#x60;  * &#x60;\&quot;esquerda|centro|direita\&quot;&#x60;  * &#x60;\&quot;|centro\&quot;&#x60;, &#x60;\&quot;|centro|\&quot;&#x60;  * &#x60;\&quot;|centro|direita\&quot;&#x60;  * &#x60;\&quot;||direita\&quot;&#x60;  * &#x60;\&quot;esquerda||direita\&quot;&#x60; | [optional] 
 **canhoto** | **bool**| Imprime o documento com o bloco de canhoto. | [optional] [default to True]

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

# **baixar_previa_pdf_nfe**
> file baixar_previa_pdf_nfe(body, logotipo=logotipo, nome_fantasia=nome_fantasia, formato=formato, mensagem_rodape=mensagem_rodape, canhoto=canhoto)

Prévia do PDF do DANFE

Através desse endpoint, é possível enviar os dados de uma NF-e e gerar uma prévia do DANFE.    Os dados de entrada são os mesmos do endpoint de emissão de NF-e (`POST /nfe`).    **Atenção**: O DANFE gerado por este endpoint é apenas para fins de visualização e não possui valor fiscal. Para a emissão de uma NF-e com valor fiscal, utilize o processo de emissão padrão descrito na documentação.    **Informações adicionais**:  - Consumo: 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    body = acbrapi_sdk.NfePedidoEmissao() # NfePedidoEmissao | 
logotipo = False # bool | Imprime o documento com logotipo, desde que esteja cadastrado na empresa. (optional) (default to False)
nome_fantasia = False # bool | Exibe o nome fantasia do emitente, desde que esteja presente no XML da nota. (optional) (default to False)
formato = 'padrao' # str | Formato de impressão do DANFE.    Valores disponíveis:  - `padrao`: será utilizado o formato definido no XML da NF-e (tag \"tpImp\");  - `retrato`: tamanho A4 em modo retrato;  - `paisagem`: tamanho A4 em modo paisagem;  - `simplificado`: formato simplificado utilizado nas operações realizadas fora do estabelecimento (Anexo II do MOC, item 3.11);  - `etiqueta`: formato simplificado utilizado nas operações em comércio eletrônico (Anexo II do MOC, item 3.12 e NT 2020.004). (optional) (default to 'padrao')
mensagem_rodape = 'mensagem_rodape_example' # str | Imprime mensagem no rodapé do documento.    O caractere `|` (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * `\"esquerda\"`  * `\"esquerda|centro\"`  * `\"esquerda|centro|direita\"`  * `\"|centro\"`, `\"|centro|\"`  * `\"|centro|direita\"`  * `\"||direita\"`  * `\"esquerda||direita\"` (optional)
canhoto = True # bool | Imprime o documento com o bloco de canhoto. (optional) (default to True)

    try:
        # Prévia do PDF do DANFE
        api_response = api_instance.baixar_previa_pdf_nfe(body, logotipo=logotipo, nome_fantasia=nome_fantasia, formato=formato, mensagem_rodape=mensagem_rodape, canhoto=canhoto)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_previa_pdf_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NfePedidoEmissao**](NfePedidoEmissao.md)|  | 
 **logotipo** | **bool**| Imprime o documento com logotipo, desde que esteja cadastrado na empresa. | [optional] [default to False]
 **nome_fantasia** | **bool**| Exibe o nome fantasia do emitente, desde que esteja presente no XML da nota. | [optional] [default to False]
 **formato** | **str**| Formato de impressão do DANFE.    Valores disponíveis:  - &#x60;padrao&#x60;: será utilizado o formato definido no XML da NF-e (tag \&quot;tpImp\&quot;);  - &#x60;retrato&#x60;: tamanho A4 em modo retrato;  - &#x60;paisagem&#x60;: tamanho A4 em modo paisagem;  - &#x60;simplificado&#x60;: formato simplificado utilizado nas operações realizadas fora do estabelecimento (Anexo II do MOC, item 3.11);  - &#x60;etiqueta&#x60;: formato simplificado utilizado nas operações em comércio eletrônico (Anexo II do MOC, item 3.12 e NT 2020.004). | [optional] [default to &#39;padrao&#39;]
 **mensagem_rodape** | **str**| Imprime mensagem no rodapé do documento.    O caractere &#x60;|&#x60; (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * &#x60;\&quot;esquerda\&quot;&#x60;  * &#x60;\&quot;esquerda|centro\&quot;&#x60;  * &#x60;\&quot;esquerda|centro|direita\&quot;&#x60;  * &#x60;\&quot;|centro\&quot;&#x60;, &#x60;\&quot;|centro|\&quot;&#x60;  * &#x60;\&quot;|centro|direita\&quot;&#x60;  * &#x60;\&quot;||direita\&quot;&#x60;  * &#x60;\&quot;esquerda||direita\&quot;&#x60; | [optional] 
 **canhoto** | **bool**| Imprime o documento com o bloco de canhoto. | [optional] [default to True]

### Return type

**file**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **baixar_previa_xml_nfe**
> file baixar_previa_xml_nfe(body)

Prévia do XML da NF-e

Através desse endpoint, é possível enviar os dados de uma NF-e e gerar uma prévia do XML, sem a assinatura digital.    Os dados de entrada são os mesmos do endpoint de emissão de NF-e (`POST /nfe`).    **Atenção**: O XML gerado por este endpoint é apenas para fins de visualização e não possui valor fiscal. Para a emissão de uma NF-e com valor fiscal, utilize o processo de emissão padrão descrito na documentação.    **Informações adicionais**:  - Consumo: 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    body = acbrapi_sdk.NfePedidoEmissao() # NfePedidoEmissao | 

    try:
        # Prévia do XML da NF-e
        api_response = api_instance.baixar_previa_xml_nfe(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_previa_xml_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NfePedidoEmissao**](NfePedidoEmissao.md)|  | 

### Return type

**file**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **baixar_xml_cancelamento_nfe**
> file baixar_xml_cancelamento_nfe(id)

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.

    try:
        # Baixar XML do cancelamento
        api_response = api_instance.baixar_xml_cancelamento_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_xml_cancelamento_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 

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

# **baixar_xml_carta_correcao_nfe**
> file baixar_xml_carta_correcao_nfe(id)

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.

    try:
        # Baixar XML da carta de correção
        api_response = api_instance.baixar_xml_carta_correcao_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_xml_carta_correcao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 

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

# **baixar_xml_evento_nfe**
> file baixar_xml_evento_nfe(id)

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Baixar XML do evento
        api_response = api_instance.baixar_xml_evento_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_xml_evento_nfe: %s\n" % e)
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

# **baixar_xml_inutilizacao_nfe**
> file baixar_xml_inutilizacao_nfe(id)

Baixar XML da inutilização

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Baixar XML da inutilização
        api_response = api_instance.baixar_xml_inutilizacao_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_xml_inutilizacao_nfe: %s\n" % e)
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

# **baixar_xml_nfe**
> file baixar_xml_nfe(id)

Baixar XML da NF-e processada

Utilize esse endpoint para obter o XML da nota enviado para a SEFAZ, complementado com a informação do protocolo de autorização ou denegação de uso (TAG raiz `nfeProc`).    O XML só estará disponível nesse endpoint caso a nota tenha sido autorizada ou denegada pela SEFAZ. Para obter o XML nos demais casos, utilize o endpoint `GET /nfe/{id}/xml/nota`.    **Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.

    try:
        # Baixar XML da NF-e processada
        api_response = api_instance.baixar_xml_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_xml_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 

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

# **baixar_xml_nfe_nota**
> file baixar_xml_nfe_nota(id)

Baixar XML da NF-e

Utilize esse endpoint para obter o XML da nota enviado para a SEFAZ.    O XML estará disponível nesse endpoint mesmo em casos que a nota tenha sido rejeitada.    **Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.

    try:
        # Baixar XML da NF-e
        api_response = api_instance.baixar_xml_nfe_nota(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_xml_nfe_nota: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 

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

# **baixar_xml_nfe_protocolo**
> file baixar_xml_nfe_protocolo(id)

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.

    try:
        # Baixar XML do Protocolo da SEFAZ
        api_response = api_instance.baixar_xml_nfe_protocolo(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->baixar_xml_nfe_protocolo: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 

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

# **cancelar_nfe**
> DfeCancelamento cancelar_nfe(id, body=body)

Cancelar uma NF-e autorizada

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.
body = acbrapi_sdk.NfePedidoCancelamento() # NfePedidoCancelamento |  (optional)

    try:
        # Cancelar uma NF-e autorizada
        api_response = api_instance.cancelar_nfe(id, body=body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->cancelar_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 
 **body** | [**NfePedidoCancelamento**](NfePedidoCancelamento.md)|  | [optional] 

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

# **consultar_cancelamento_nfe**
> DfeCancelamento consultar_cancelamento_nfe(id)

Consultar o cancelamento da NF-e

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.

    try:
        # Consultar o cancelamento da NF-e
        api_response = api_instance.consultar_cancelamento_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->consultar_cancelamento_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 

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

# **consultar_carta_correcao_nfe**
> DfeCartaCorrecao consultar_carta_correcao_nfe(id)

Consultar a solicitação de correção da NF-e

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.

    try:
        # Consultar a solicitação de correção da NF-e
        api_response = api_instance.consultar_carta_correcao_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->consultar_carta_correcao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 

### Return type

[**DfeCartaCorrecao**](DfeCartaCorrecao.md)

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

# **consultar_contribuinte_nfe**
> DfeContribuinteInfCons consultar_contribuinte_nfe(cpf_cnpj, argumento, documento, uf=uf)

Consultar contribuinte

Consulta o Cadastro Centralizado de Contribuintes (CCC) do ICMS da unidade federada.    **Informações adicionais**:  - Consumo: 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*.
argumento = 'argumento_example' # str | Argumento de pesquisa.    Valores válidos:  * `CNPJ`  * `CPF`  * `IE`
documento = 'documento_example' # str | Documento a ser consultado (CNPJ, CPF ou Inscrição Estadual).
uf = 'uf_example' # str | Sigla da UF consultada.     Utilize `SU` para SUFRAMA.    *Caso não seja informada, será utilizada a UF da empresa.* (optional)

    try:
        # Consultar contribuinte
        api_response = api_instance.consultar_contribuinte_nfe(cpf_cnpj, argumento, documento, uf=uf)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->consultar_contribuinte_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*. | 
 **argumento** | **str**| Argumento de pesquisa.    Valores válidos:  * &#x60;CNPJ&#x60;  * &#x60;CPF&#x60;  * &#x60;IE&#x60; | 
 **documento** | **str**| Documento a ser consultado (CNPJ, CPF ou Inscrição Estadual). | 
 **uf** | **str**| Sigla da UF consultada.     Utilize &#x60;SU&#x60; para SUFRAMA.    *Caso não seja informada, será utilizada a UF da empresa.* | [optional] 

### Return type

[**DfeContribuinteInfCons**](DfeContribuinteInfCons.md)

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

# **consultar_evento_nfe**
> DfeEvento consultar_evento_nfe(id)

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Consultar evento
        api_response = api_instance.consultar_evento_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->consultar_evento_nfe: %s\n" % e)
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

# **consultar_inutilizacao_nfe**
> DfeInutilizacao consultar_inutilizacao_nfe(id)

Consultar a inutilização de sequência de numeração

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Consultar a inutilização de sequência de numeração
        api_response = api_instance.consultar_inutilizacao_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->consultar_inutilizacao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do evento gerado pela API. | 

### Return type

[**DfeInutilizacao**](DfeInutilizacao.md)

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

# **consultar_lote_nfe**
> DfeLote consultar_lote_nfe(id)

Consultar lote de NF-e

Consulta os detalhes de um lote já existente. Forneça o ID único obtido de uma requisição de emissão ou de listagem de lotes e a API irá retornar as informações do lote correspondente.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único do lote gerado pela API.

    try:
        # Consultar lote de NF-e
        api_response = api_instance.consultar_lote_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->consultar_lote_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do lote gerado pela API. | 

### Return type

[**DfeLote**](DfeLote.md)

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

# **consultar_nfe**
> Dfe consultar_nfe(id)

Consultar NF-e

Consulta os detalhes de uma NF-e já existente. Forneça o ID único obtido de uma requisição de emissão ou de listagem de notas e a API irá retornar as informações da nota correspondente.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.

    try:
        # Consultar NF-e
        api_response = api_instance.consultar_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->consultar_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 

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

# **consultar_status_sefaz_nfe**
> DfeSefazStatus consultar_status_sefaz_nfe(cpf_cnpj, autorizador=autorizador)

Consulta do Status do Serviço na SEFAZ Autorizadora

Consulta do status do serviço prestado pelo Portal da Secretaria de Fazenda Estadual.    A API mantém a última consulta em cache por 5 minutos, evitando sobrecarregar desnecessariamente os servidores da SEFAZ (conforme orientação do MOC - versão 7.0, item 5.5.3). Dessa forma, você poderá chamar esse endpoint quantas vezes quiser, sem preocupar-se em ter o seu CNPJ bloqueado por consumo indevido (Rejeição 656).

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF/CNPJ do emitente.  Utilize o valor sem máscara.
autorizador = 'autorizador_example' # str | Ambiente Autorizador.    Autorizadores disponíveis: `AM`, `BA`, `GO`, `MG`, `MS`, `MT`, `PE`, `PR`, `RS`, `SP`, `SVAN`, `SVRS`, `SVCAN`, `SVCRS`, `AN`.    *Caso não seja informado, será utilizado o ambiente autorizador da UF do emitente.* (optional)

    try:
        # Consulta do Status do Serviço na SEFAZ Autorizadora
        api_response = api_instance.consultar_status_sefaz_nfe(cpf_cnpj, autorizador=autorizador)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->consultar_status_sefaz_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF/CNPJ do emitente.  Utilize o valor sem máscara. | 
 **autorizador** | **str**| Ambiente Autorizador.    Autorizadores disponíveis: &#x60;AM&#x60;, &#x60;BA&#x60;, &#x60;GO&#x60;, &#x60;MG&#x60;, &#x60;MS&#x60;, &#x60;MT&#x60;, &#x60;PE&#x60;, &#x60;PR&#x60;, &#x60;RS&#x60;, &#x60;SP&#x60;, &#x60;SVAN&#x60;, &#x60;SVRS&#x60;, &#x60;SVCAN&#x60;, &#x60;SVCRS&#x60;, &#x60;AN&#x60;.    *Caso não seja informado, será utilizado o ambiente autorizador da UF do emitente.* | [optional] 

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

# **criar_carta_correcao_nfe**
> DfeCartaCorrecao criar_carta_correcao_nfe(id, body)

Solicitar correção da NF-e

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.
body = acbrapi_sdk.NfePedidoCartaCorrecao() # NfePedidoCartaCorrecao | Contém os dados do pedido para carta de correção.

    try:
        # Solicitar correção da NF-e
        api_response = api_instance.criar_carta_correcao_nfe(id, body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->criar_carta_correcao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 
 **body** | [**NfePedidoCartaCorrecao**](NfePedidoCartaCorrecao.md)| Contém os dados do pedido para carta de correção. | 

### Return type

[**DfeCartaCorrecao**](DfeCartaCorrecao.md)

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

# **emitir_lote_nfe**
> DfeLote emitir_lote_nfe(body)

Emitir lote de NF-e

**Informações adicionais**:  - Consumo: 1 unidade por NF-e.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    body = acbrapi_sdk.NfePedidoEmissaoLote() # NfePedidoEmissaoLote | 

    try:
        # Emitir lote de NF-e
        api_response = api_instance.emitir_lote_nfe(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->emitir_lote_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NfePedidoEmissaoLote**](NfePedidoEmissaoLote.md)|  | 

### Return type

[**DfeLote**](DfeLote.md)

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

# **emitir_nfe**
> Dfe emitir_nfe(body)

Emitir NF-e

Este endpoint permite a emissão de Notas Fiscais Eletrônicas (NF-e).  A solicitação deve ser feita enviando os dados necessários para a  emissão de uma NF-e.     A estrutura do JSON utilizado na solicitação segue a hierarquia e  nomenclatura de campos definidos no <a href=\"https://www.nfe.fazenda.gov.br/portal/principal.aspx\" target=\"_blank\">  Manual de Orientação ao Contribuinte (MOC)</a>.  Esta conformidade visa facilitar a integração de novos usuários que já  possuem familiaridade com o padrão, além de permitir a resolução de  dúvidas diretamente no MOC, com um profissional de contabilidade  habilitado ou em outras fontes confiáveis que tratam do mesmo assunto.    **Comportamento Assíncrono**    A resposta desse endpoint inclui a propriedade *status* no JSON.  Caso o valor retornado seja *pendente*, significa que a solicitação está  sendo realizada de forma assíncrona pela API. Nesse caso, o usuário deverá  adotar um fluxo que consiste em requisitar periodicamente o endpoint  <a href=\"#tag/Nfe/operation/ConsultarNfe\">Consultar NF-e</a> até que  seja retornado um status indicando o fim da emissão.    **Informações adicionais**:  - Consumo: 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    body = acbrapi_sdk.NfePedidoEmissao() # NfePedidoEmissao | 

    try:
        # Emitir NF-e
        api_response = api_instance.emitir_nfe(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->emitir_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NfePedidoEmissao**](NfePedidoEmissao.md)|  | 

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

# **enviar_email_nfe**
> EmailStatusResponse enviar_email_nfe(id, logotipo=logotipo, nome_fantasia=nome_fantasia, formato=formato, mensagem_rodape=mensagem_rodape, canhoto=canhoto, body=body)

Enviar e-mail

Envia o XML e PDF da nota via email.    **Informações adicionais**:  - Consumo: 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.
logotipo = False # bool | Imprime o documento com logotipo, desde que esteja cadastrado na empresa. (optional) (default to False)
nome_fantasia = False # bool | Exibe o nome fantasia do emitente, desde que esteja presente no XML da nota. (optional) (default to False)
formato = 'padrao' # str | Formato de impressão do DANFE.    Valores disponíveis:  - `padrao`: será utilizado o formato definido no XML da NF-e (tag \"tpImp\");  - `retrato`: tamanho A4 em modo retrato;  - `paisagem`: tamanho A4 em modo paisagem;  - `simplificado`: formato simplificado utilizado nas operações realizadas fora do estabelecimento (Anexo II do MOC, item 3.11);  - `etiqueta`: formato simplificado utilizado nas operações em comércio eletrônico (Anexo II do MOC, item 3.12 e NT 2020.004). (optional) (default to 'padrao')
mensagem_rodape = 'mensagem_rodape_example' # str | Imprime mensagem no rodapé do documento.    O caractere `|` (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * `\"esquerda\"`  * `\"esquerda|centro\"`  * `\"esquerda|centro|direita\"`  * `\"|centro\"`, `\"|centro|\"`  * `\"|centro|direita\"`  * `\"||direita\"`  * `\"esquerda||direita\"` (optional)
canhoto = True # bool | Imprime o documento com o bloco de canhoto. (optional) (default to True)
body = acbrapi_sdk.DfePedidoEnvioEmail() # DfePedidoEnvioEmail |  (optional)

    try:
        # Enviar e-mail
        api_response = api_instance.enviar_email_nfe(id, logotipo=logotipo, nome_fantasia=nome_fantasia, formato=formato, mensagem_rodape=mensagem_rodape, canhoto=canhoto, body=body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->enviar_email_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 
 **logotipo** | **bool**| Imprime o documento com logotipo, desde que esteja cadastrado na empresa. | [optional] [default to False]
 **nome_fantasia** | **bool**| Exibe o nome fantasia do emitente, desde que esteja presente no XML da nota. | [optional] [default to False]
 **formato** | **str**| Formato de impressão do DANFE.    Valores disponíveis:  - &#x60;padrao&#x60;: será utilizado o formato definido no XML da NF-e (tag \&quot;tpImp\&quot;);  - &#x60;retrato&#x60;: tamanho A4 em modo retrato;  - &#x60;paisagem&#x60;: tamanho A4 em modo paisagem;  - &#x60;simplificado&#x60;: formato simplificado utilizado nas operações realizadas fora do estabelecimento (Anexo II do MOC, item 3.11);  - &#x60;etiqueta&#x60;: formato simplificado utilizado nas operações em comércio eletrônico (Anexo II do MOC, item 3.12 e NT 2020.004). | [optional] [default to &#39;padrao&#39;]
 **mensagem_rodape** | **str**| Imprime mensagem no rodapé do documento.    O caractere &#x60;|&#x60; (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * &#x60;\&quot;esquerda\&quot;&#x60;  * &#x60;\&quot;esquerda|centro\&quot;&#x60;  * &#x60;\&quot;esquerda|centro|direita\&quot;&#x60;  * &#x60;\&quot;|centro\&quot;&#x60;, &#x60;\&quot;|centro|\&quot;&#x60;  * &#x60;\&quot;|centro|direita\&quot;&#x60;  * &#x60;\&quot;||direita\&quot;&#x60;  * &#x60;\&quot;esquerda||direita\&quot;&#x60; | [optional] 
 **canhoto** | **bool**| Imprime o documento com o bloco de canhoto. | [optional] [default to True]
 **body** | [**DfePedidoEnvioEmail**](DfePedidoEnvioEmail.md)|  | [optional] 

### Return type

[**EmailStatusResponse**](EmailStatusResponse.md)

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

# **inutilizar_numeracao_nfe**
> DfeInutilizacao inutilizar_numeracao_nfe(body)

Inutilizar uma sequência de numeração de NF-e

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    body = acbrapi_sdk.DfePedidoInutilizacao() # DfePedidoInutilizacao | 

    try:
        # Inutilizar uma sequência de numeração de NF-e
        api_response = api_instance.inutilizar_numeracao_nfe(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->inutilizar_numeracao_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DfePedidoInutilizacao**](DfePedidoInutilizacao.md)|  | 

### Return type

[**DfeInutilizacao**](DfeInutilizacao.md)

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

# **listar_eventos_nfe**
> DfeEventoListagem listar_eventos_nfe(dfe_id, top=top, skip=skip, inlinecount=inlinecount)

Listar eventos

Retorna a lista de eventos vinculados a um documento fiscal de acordo com os critérios de busca utilizados. Os eventos são retornados ordenados pela data da criação, com as mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    dfe_id = 'dfe_id_example' # str | ID único gerado pela API para o documento fiscal.
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)

    try:
        # Listar eventos
        api_response = api_instance.listar_eventos_nfe(dfe_id, top=top, skip=skip, inlinecount=inlinecount)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->listar_eventos_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dfe_id** | **str**| ID único gerado pela API para o documento fiscal. | 
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to False]

### Return type

[**DfeEventoListagem**](DfeEventoListagem.md)

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

# **listar_lotes_nfe**
> DfeLoteListagem listar_lotes_nfe(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia)

Listar lotes de NF-e

Retorna a lista dos lotes de acordo com os critérios de busca utilizados. Os lotes são retornados ordenados pela data da criação, com os mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ do emitente.  Utilize o valor sem máscara.
ambiente = 'ambiente_example' # str | Identificação do Ambiente.    Valores aceitos: homologacao, producao
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)
referencia = 'referencia_example' # str |  (optional)

    try:
        # Listar lotes de NF-e
        api_response = api_instance.listar_lotes_nfe(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->listar_lotes_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| Filtrar pelo CPF ou CNPJ do emitente.  Utilize o valor sem máscara. | 
 **ambiente** | **str**| Identificação do Ambiente.    Valores aceitos: homologacao, producao | 
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to False]
 **referencia** | **str**|  | [optional] 

### Return type

[**DfeLoteListagem**](DfeLoteListagem.md)

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

# **listar_nfe**
> DfeListagem listar_nfe(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia, chave=chave, serie=serie)

Listar NF-e

Retorna a lista de notas de acordo com os critérios de busca utilizados. As notas são retornadas ordenadas pela data da criação, com as mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ do emitente.    Utilize o valor sem máscara.
ambiente = 'ambiente_example' # str | Identificação do Ambiente.    Valores aceitos: homologacao, producao
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)
referencia = 'referencia_example' # str | Seu identificador único para o documento. (optional)
chave = 'chave_example' # str | Chave de acesso do DF-e. (optional)
serie = 'serie_example' # str | Série do DF-e. (optional)

    try:
        # Listar NF-e
        api_response = api_instance.listar_nfe(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia, chave=chave, serie=serie)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->listar_nfe: %s\n" % e)
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

# **sincronizar_nfe**
> DfeSincronizacao sincronizar_nfe(id)

Sincroniza dados na NF-e a partir da SEFAZ

Realiza a sincronização dos dados a partir da consulta da situação atual da NF-e na Base de Dados do Portal da Secretaria de Fazenda Estadual.    **Cenários de uso**:  * Sincronizar uma nota que se encontra com o status `erro` na API, mas está autorizada na SEFAZ (útil em casos de erros de transmissão com a SEFAZ, como instabilidades e timeouts).  * Sincronizar uma nota que se encontra com o status `autorizado`na API, mas está cancelada na SEFAZ.  * Sincronizar todos os eventos de Cancelamento, Carta de Correção e EPEC de uma nota que porventura não tenham sido feitos a partir da API.    **Informações adicionais**:  - Consumo: 1 unidade por evento sincronizado ou requisição.

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
    api_instance = acbrapi_sdk.NfeApi(api_client)
    id = 'id_example' # str | ID único da NF-e gerado pela API.

    try:
        # Sincroniza dados na NF-e a partir da SEFAZ
        api_response = api_instance.sincronizar_nfe(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfeApi->sincronizar_nfe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NF-e gerado pela API. | 

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

