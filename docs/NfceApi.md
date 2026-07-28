# acbrapi_sdk.NfceApi

All URIs are relative to *https://prod.acbr.api.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**baixar_esc_pos_nfce**](NfceApi.md#baixar_esc_pos_nfce) | **GET** /nfce/{id}/escpos | Comandos ESC/POS para impressão do DANFCE
[**baixar_pdf_cancelamento_nfce**](NfceApi.md#baixar_pdf_cancelamento_nfce) | **GET** /nfce/{id}/cancelamento/pdf | Baixar PDF do cancelamento
[**baixar_pdf_evento_nfce**](NfceApi.md#baixar_pdf_evento_nfce) | **GET** /nfce/eventos/{id}/pdf | Baixar PDF do evento
[**baixar_pdf_inutilizacao_nfce**](NfceApi.md#baixar_pdf_inutilizacao_nfce) | **GET** /nfce/inutilizacoes/{id}/pdf | Baixar PDF da inutilização
[**baixar_pdf_nfce**](NfceApi.md#baixar_pdf_nfce) | **GET** /nfce/{id}/pdf | Baixar PDF do DANFCE
[**baixar_previa_pdf_nfce**](NfceApi.md#baixar_previa_pdf_nfce) | **POST** /nfce/previa/pdf | Prévia do PDF do DANFCE
[**baixar_previa_xml_nfce**](NfceApi.md#baixar_previa_xml_nfce) | **POST** /nfce/previa/xml | Prévia do XML da NFC-e
[**baixar_xml_cancelamento_nfce**](NfceApi.md#baixar_xml_cancelamento_nfce) | **GET** /nfce/{id}/cancelamento/xml | Baixar XML do cancelamento
[**baixar_xml_evento_nfce**](NfceApi.md#baixar_xml_evento_nfce) | **GET** /nfce/eventos/{id}/xml | Baixar XML do evento
[**baixar_xml_inutilizacao_nfce**](NfceApi.md#baixar_xml_inutilizacao_nfce) | **GET** /nfce/inutilizacoes/{id}/xml | Baixar XML da inutilização
[**baixar_xml_nfce**](NfceApi.md#baixar_xml_nfce) | **GET** /nfce/{id}/xml | Baixar XML da NFC-e processada
[**baixar_xml_nfce_nota**](NfceApi.md#baixar_xml_nfce_nota) | **GET** /nfce/{id}/xml/nota | Baixar XML da NFC-e
[**baixar_xml_nfce_protocolo**](NfceApi.md#baixar_xml_nfce_protocolo) | **GET** /nfce/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
[**cancelar_nfce**](NfceApi.md#cancelar_nfce) | **POST** /nfce/{id}/cancelamento | Cancelar uma NFC-e autorizada
[**consultar_cancelamento_nfce**](NfceApi.md#consultar_cancelamento_nfce) | **GET** /nfce/{id}/cancelamento | Consultar o cancelamento da NFC-e
[**consultar_evento_nfce**](NfceApi.md#consultar_evento_nfce) | **GET** /nfce/eventos/{id} | Consultar evento
[**consultar_inutilizacao_nfce**](NfceApi.md#consultar_inutilizacao_nfce) | **GET** /nfce/inutilizacoes/{id} | Consultar a inutilização de sequência de numeração
[**consultar_lote_nfce**](NfceApi.md#consultar_lote_nfce) | **GET** /nfce/lotes/{id} | Consultar lote de NFC-e
[**consultar_nfce**](NfceApi.md#consultar_nfce) | **GET** /nfce/{id} | Consultar NFC-e
[**consultar_status_sefaz_nfce**](NfceApi.md#consultar_status_sefaz_nfce) | **GET** /nfce/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
[**emitir_lote_nfce**](NfceApi.md#emitir_lote_nfce) | **POST** /nfce/lotes | Emitir lote de NFC-e
[**emitir_nfce**](NfceApi.md#emitir_nfce) | **POST** /nfce | Emitir NFC-e
[**enviar_email_nfce**](NfceApi.md#enviar_email_nfce) | **POST** /nfce/{id}/email | Enviar e-mail
[**inutilizar_numeracao_nfce**](NfceApi.md#inutilizar_numeracao_nfce) | **POST** /nfce/inutilizacoes | Inutilizar uma sequência de numeração de NFC-e
[**listar_eventos_nfce**](NfceApi.md#listar_eventos_nfce) | **GET** /nfce/eventos | Listar eventos
[**listar_lotes_nfce**](NfceApi.md#listar_lotes_nfce) | **GET** /nfce/lotes | Listar lotes de NFC-e
[**listar_nfce**](NfceApi.md#listar_nfce) | **GET** /nfce | Listar NFC-e
[**sincronizar_nfce**](NfceApi.md#sincronizar_nfce) | **POST** /nfce/{id}/sincronizar | Sincroniza dados na NFC-e a partir da SEFAZ


# **baixar_esc_pos_nfce**
> file baixar_esc_pos_nfce(id, modelo=modelo, colunas=colunas, qrcode_lateral=qrcode_lateral)

Comandos ESC/POS para impressão do DANFCE

ESC/POS é um sistema de comando criado pela Epson usado em diversos sistemas de impressoras POS.    Com o formato ESC/POS, você poderá imprimir nativamente em uma vasta quantidade de modelos de impressora térmicas utilizadas no Brasil e no mundo. Com ela, você consegue fazer o envio de comandos em ESC/POS direto para a porta da impressora.

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único da NFC-e gerado pela API.
modelo = 1 # int | Modelo da impressora:  * `0` - Texto  * `1` - Epson  * `2` - Bematech  * `3` - Daruma  * `4` - Vox  * `5` - Diebold  * `6` - Epson P2  * `7` - CustomPos  * `8` - Star  * `9` - Zjiang  * `10` - GPrinter  * `11` - Datecs  * `12` - Sunmi  * `13` - Externo (optional) (default to 1)
colunas = 48 # int | Define o máximo de caracteres, em uma linha, usando a fonte normal.    Ex: 40, 42, 48, 58, 80. (optional) (default to 48)
qrcode_lateral = False # bool | Imprime o QRCode na lateral do DANFCe.    OBS: não suportado por alguns modelos de impressora. (optional) (default to False)

    try:
        # Comandos ESC/POS para impressão do DANFCE
        api_response = api_instance.baixar_esc_pos_nfce(id, modelo=modelo, colunas=colunas, qrcode_lateral=qrcode_lateral)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_esc_pos_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFC-e gerado pela API. | 
 **modelo** | **int**| Modelo da impressora:  * &#x60;0&#x60; - Texto  * &#x60;1&#x60; - Epson  * &#x60;2&#x60; - Bematech  * &#x60;3&#x60; - Daruma  * &#x60;4&#x60; - Vox  * &#x60;5&#x60; - Diebold  * &#x60;6&#x60; - Epson P2  * &#x60;7&#x60; - CustomPos  * &#x60;8&#x60; - Star  * &#x60;9&#x60; - Zjiang  * &#x60;10&#x60; - GPrinter  * &#x60;11&#x60; - Datecs  * &#x60;12&#x60; - Sunmi  * &#x60;13&#x60; - Externo | [optional] [default to 1]
 **colunas** | **int**| Define o máximo de caracteres, em uma linha, usando a fonte normal.    Ex: 40, 42, 48, 58, 80. | [optional] [default to 48]
 **qrcode_lateral** | **bool**| Imprime o QRCode na lateral do DANFCe.    OBS: não suportado por alguns modelos de impressora. | [optional] [default to False]

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

# **baixar_pdf_cancelamento_nfce**
> file baixar_pdf_cancelamento_nfce(id)

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único da NFC-e gerado pela API.

    try:
        # Baixar PDF do cancelamento
        api_response = api_instance.baixar_pdf_cancelamento_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_pdf_cancelamento_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFC-e gerado pela API. | 

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

# **baixar_pdf_evento_nfce**
> file baixar_pdf_evento_nfce(id)

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Baixar PDF do evento
        api_response = api_instance.baixar_pdf_evento_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_pdf_evento_nfce: %s\n" % e)
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

# **baixar_pdf_inutilizacao_nfce**
> file baixar_pdf_inutilizacao_nfce(id)

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Baixar PDF da inutilização
        api_response = api_instance.baixar_pdf_inutilizacao_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_pdf_inutilizacao_nfce: %s\n" % e)
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

# **baixar_pdf_nfce**
> file baixar_pdf_nfce(id, logotipo=logotipo, nome_fantasia=nome_fantasia, mensagem_rodape=mensagem_rodape, resumido=resumido, qrcode_lateral=qrcode_lateral, largura=largura, margem=margem)

Baixar PDF do DANFCE

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único da NFC-e gerado pela API.
logotipo = False # bool | Imprime o documento com logotipo, desde que esteja cadastrado na empresa. (optional) (default to False)
nome_fantasia = False # bool | Exibe o nome fantasia do emitente, desde que esteja presente no XML da nota. (optional) (default to False)
mensagem_rodape = 'mensagem_rodape_example' # str | Imprime mensagem no rodapé do documento.    O caractere `|` (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * `\"esquerda\"`  * `\"esquerda|centro\"`  * `\"esquerda|centro|direita\"`  * `\"|centro\"`, `\"|centro|\"`  * `\"|centro|direita\"`  * `\"||direita\"`  * `\"esquerda||direita\"` (optional)
resumido = False # bool | Poderá ser impresso apenas o DANFE NFC-e resumido ou ecológico, sem o detalhamento dos itens da venda, desde que a Unidade Federada permita esta opção em sua legislação e o consumidor assim o solicite. (optional) (default to False)
qrcode_lateral = False # bool | Imprime o QRCode na lateral do DANFE NFC-e.    *Disponível apenas para DANFE com 80 milímetros de largura*. (optional) (default to False)
largura = 80 # int | Largura do DANFE NFC-e (em milímetros). (optional) (default to 80)
margem = '2' # str | Define as margens do DANFE NFC-e (em milímetros).    Essa propriedade pode ser especificada usando um, dois, três ou quatro valores (separados por vírgulas). Cada valor deve ser um número entre `0` e `9`.  * Quando **um** valor é especificado, a mesma margem é aplicada para **todos os quatro lados**.  * Quando **dois** valores são especificados, a primeira margem é aplicada aos **lados esquerdo e direito**, e a segunda aos **lados superior e inferior**.  * Quando **três** valores são especificados, a primeira margem é aplicada ao **lado esquerdo**, a segunda aos **lados superior e inferior**, e a terceira ao **lado direito**.  * Quando **quatro** valores são especificados, as margens são aplicadas aos lados **esquerdo**, **superior**, **direito** e **inferior**, nesta ordem (sentido horário).    **Exemplos de uso**:  * `margem=1`    - Margem esquerda: 1mm    - Margem superior: 1mm    - Margem direita: 1mm    - Margem inferior: 1mm  * `margem=1,2`    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 1mm    - Margem inferior: 2mm  * `margem=1,2,3`    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 3mm    - Margem inferior: 2mm  * `margem=1,2,3,4`    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 3mm    - Margem inferior: 4mm (optional) (default to '2')

    try:
        # Baixar PDF do DANFCE
        api_response = api_instance.baixar_pdf_nfce(id, logotipo=logotipo, nome_fantasia=nome_fantasia, mensagem_rodape=mensagem_rodape, resumido=resumido, qrcode_lateral=qrcode_lateral, largura=largura, margem=margem)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_pdf_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFC-e gerado pela API. | 
 **logotipo** | **bool**| Imprime o documento com logotipo, desde que esteja cadastrado na empresa. | [optional] [default to False]
 **nome_fantasia** | **bool**| Exibe o nome fantasia do emitente, desde que esteja presente no XML da nota. | [optional] [default to False]
 **mensagem_rodape** | **str**| Imprime mensagem no rodapé do documento.    O caractere &#x60;|&#x60; (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * &#x60;\&quot;esquerda\&quot;&#x60;  * &#x60;\&quot;esquerda|centro\&quot;&#x60;  * &#x60;\&quot;esquerda|centro|direita\&quot;&#x60;  * &#x60;\&quot;|centro\&quot;&#x60;, &#x60;\&quot;|centro|\&quot;&#x60;  * &#x60;\&quot;|centro|direita\&quot;&#x60;  * &#x60;\&quot;||direita\&quot;&#x60;  * &#x60;\&quot;esquerda||direita\&quot;&#x60; | [optional] 
 **resumido** | **bool**| Poderá ser impresso apenas o DANFE NFC-e resumido ou ecológico, sem o detalhamento dos itens da venda, desde que a Unidade Federada permita esta opção em sua legislação e o consumidor assim o solicite. | [optional] [default to False]
 **qrcode_lateral** | **bool**| Imprime o QRCode na lateral do DANFE NFC-e.    *Disponível apenas para DANFE com 80 milímetros de largura*. | [optional] [default to False]
 **largura** | **int**| Largura do DANFE NFC-e (em milímetros). | [optional] [default to 80]
 **margem** | **str**| Define as margens do DANFE NFC-e (em milímetros).    Essa propriedade pode ser especificada usando um, dois, três ou quatro valores (separados por vírgulas). Cada valor deve ser um número entre &#x60;0&#x60; e &#x60;9&#x60;.  * Quando **um** valor é especificado, a mesma margem é aplicada para **todos os quatro lados**.  * Quando **dois** valores são especificados, a primeira margem é aplicada aos **lados esquerdo e direito**, e a segunda aos **lados superior e inferior**.  * Quando **três** valores são especificados, a primeira margem é aplicada ao **lado esquerdo**, a segunda aos **lados superior e inferior**, e a terceira ao **lado direito**.  * Quando **quatro** valores são especificados, as margens são aplicadas aos lados **esquerdo**, **superior**, **direito** e **inferior**, nesta ordem (sentido horário).    **Exemplos de uso**:  * &#x60;margem&#x3D;1&#x60;    - Margem esquerda: 1mm    - Margem superior: 1mm    - Margem direita: 1mm    - Margem inferior: 1mm  * &#x60;margem&#x3D;1,2&#x60;    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 1mm    - Margem inferior: 2mm  * &#x60;margem&#x3D;1,2,3&#x60;    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 3mm    - Margem inferior: 2mm  * &#x60;margem&#x3D;1,2,3,4&#x60;    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 3mm    - Margem inferior: 4mm | [optional] [default to &#39;2&#39;]

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

# **baixar_previa_pdf_nfce**
> file baixar_previa_pdf_nfce(body, logotipo=logotipo, nome_fantasia=nome_fantasia, mensagem_rodape=mensagem_rodape, resumido=resumido, qrcode_lateral=qrcode_lateral, largura=largura, margem=margem)

Prévia do PDF do DANFCE

Através desse endpoint, é possível enviar os dados de uma NFC-e e gerar uma prévia do DANFCE.    Os dados de entrada são os mesmos do endpoint de emissão de NFC-e (`POST /nfce`).    **Atenção**: O DANFE gerado por este endpoint é apenas para fins de visualização e não possui valor fiscal. Para a emissão de uma NF-e com valor fiscal, utilize o processo de emissão padrão descrito na documentação.    **Informações adicionais**:  - Consumo: 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    body = acbrapi_sdk.NfePedidoEmissao() # NfePedidoEmissao | 
logotipo = False # bool | Imprime o documento com logotipo, desde que esteja cadastrado na empresa. (optional) (default to False)
nome_fantasia = False # bool | Exibe o nome fantasia do emitente, desde que esteja presente no XML da nota. (optional) (default to False)
mensagem_rodape = 'mensagem_rodape_example' # str | Imprime mensagem no rodapé do documento.    O caractere `|` (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * `\"esquerda\"`  * `\"esquerda|centro\"`  * `\"esquerda|centro|direita\"`  * `\"|centro\"`, `\"|centro|\"`  * `\"|centro|direita\"`  * `\"||direita\"`  * `\"esquerda||direita\"` (optional)
resumido = False # bool | Poderá ser impresso apenas o DANFE NFC-e resumido ou ecológico, sem o detalhamento dos itens da venda, desde que a Unidade Federada permita esta opção em sua legislação e o consumidor assim o solicite. (optional) (default to False)
qrcode_lateral = False # bool | Imprime o QRCode na lateral do DANFE NFC-e.    *Disponível apenas para DANFE com 80 milímetros de largura*. (optional) (default to False)
largura = 80 # int | Largura do DANFE NFC-e (em milímetros). (optional) (default to 80)
margem = '2' # str | Define as margens do DANFE NFC-e (em milímetros).    Essa propriedade pode ser especificada usando um, dois, três ou quatro valores (separados por vírgulas). Cada valor deve ser um número entre `0` e `9`.  * Quando **um** valor é especificado, a mesma margem é aplicada para **todos os quatro lados**.  * Quando **dois** valores são especificados, a primeira margem é aplicada aos **lados esquerdo e direito**, e a segunda aos **lados superior e inferior**.  * Quando **três** valores são especificados, a primeira margem é aplicada ao **lado esquerdo**, a segunda aos **lados superior e inferior**, e a terceira ao **lado direito**.  * Quando **quatro** valores são especificados, as margens são aplicadas aos lados **esquerdo**, **superior**, **direito** e **inferior**, nesta ordem (sentido horário).    **Exemplos de uso**:  * `margem=1`    - Margem esquerda: 1mm    - Margem superior: 1mm    - Margem direita: 1mm    - Margem inferior: 1mm  * `margem=1,2`    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 1mm    - Margem inferior: 2mm  * `margem=1,2,3`    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 3mm    - Margem inferior: 2mm  * `margem=1,2,3,4`    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 3mm    - Margem inferior: 4mm (optional) (default to '2')

    try:
        # Prévia do PDF do DANFCE
        api_response = api_instance.baixar_previa_pdf_nfce(body, logotipo=logotipo, nome_fantasia=nome_fantasia, mensagem_rodape=mensagem_rodape, resumido=resumido, qrcode_lateral=qrcode_lateral, largura=largura, margem=margem)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_previa_pdf_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NfePedidoEmissao**](NfePedidoEmissao.md)|  | 
 **logotipo** | **bool**| Imprime o documento com logotipo, desde que esteja cadastrado na empresa. | [optional] [default to False]
 **nome_fantasia** | **bool**| Exibe o nome fantasia do emitente, desde que esteja presente no XML da nota. | [optional] [default to False]
 **mensagem_rodape** | **str**| Imprime mensagem no rodapé do documento.    O caractere &#x60;|&#x60; (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * &#x60;\&quot;esquerda\&quot;&#x60;  * &#x60;\&quot;esquerda|centro\&quot;&#x60;  * &#x60;\&quot;esquerda|centro|direita\&quot;&#x60;  * &#x60;\&quot;|centro\&quot;&#x60;, &#x60;\&quot;|centro|\&quot;&#x60;  * &#x60;\&quot;|centro|direita\&quot;&#x60;  * &#x60;\&quot;||direita\&quot;&#x60;  * &#x60;\&quot;esquerda||direita\&quot;&#x60; | [optional] 
 **resumido** | **bool**| Poderá ser impresso apenas o DANFE NFC-e resumido ou ecológico, sem o detalhamento dos itens da venda, desde que a Unidade Federada permita esta opção em sua legislação e o consumidor assim o solicite. | [optional] [default to False]
 **qrcode_lateral** | **bool**| Imprime o QRCode na lateral do DANFE NFC-e.    *Disponível apenas para DANFE com 80 milímetros de largura*. | [optional] [default to False]
 **largura** | **int**| Largura do DANFE NFC-e (em milímetros). | [optional] [default to 80]
 **margem** | **str**| Define as margens do DANFE NFC-e (em milímetros).    Essa propriedade pode ser especificada usando um, dois, três ou quatro valores (separados por vírgulas). Cada valor deve ser um número entre &#x60;0&#x60; e &#x60;9&#x60;.  * Quando **um** valor é especificado, a mesma margem é aplicada para **todos os quatro lados**.  * Quando **dois** valores são especificados, a primeira margem é aplicada aos **lados esquerdo e direito**, e a segunda aos **lados superior e inferior**.  * Quando **três** valores são especificados, a primeira margem é aplicada ao **lado esquerdo**, a segunda aos **lados superior e inferior**, e a terceira ao **lado direito**.  * Quando **quatro** valores são especificados, as margens são aplicadas aos lados **esquerdo**, **superior**, **direito** e **inferior**, nesta ordem (sentido horário).    **Exemplos de uso**:  * &#x60;margem&#x3D;1&#x60;    - Margem esquerda: 1mm    - Margem superior: 1mm    - Margem direita: 1mm    - Margem inferior: 1mm  * &#x60;margem&#x3D;1,2&#x60;    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 1mm    - Margem inferior: 2mm  * &#x60;margem&#x3D;1,2,3&#x60;    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 3mm    - Margem inferior: 2mm  * &#x60;margem&#x3D;1,2,3,4&#x60;    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 3mm    - Margem inferior: 4mm | [optional] [default to &#39;2&#39;]

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

# **baixar_previa_xml_nfce**
> file baixar_previa_xml_nfce(body)

Prévia do XML da NFC-e

Através desse endpoint, é possível enviar os dados de uma NFC-e e gerar uma prévia do XML, sem a assinatura digital.    Os dados de entrada são os mesmos do endpoint de emissão de NFC-e (`POST /nfce`).    **Atenção**: O XML gerado por este endpoint é apenas para fins de visualização e não possui valor fiscal. Para a emissão de uma NF-e com valor fiscal, utilize o processo de emissão padrão descrito na documentação.    **Informações adicionais**:  - Consumo: 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    body = acbrapi_sdk.NfePedidoEmissao() # NfePedidoEmissao | 

    try:
        # Prévia do XML da NFC-e
        api_response = api_instance.baixar_previa_xml_nfce(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_previa_xml_nfce: %s\n" % e)
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

# **baixar_xml_cancelamento_nfce**
> file baixar_xml_cancelamento_nfce(id)

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único da NFC-e gerado pela API.

    try:
        # Baixar XML do cancelamento
        api_response = api_instance.baixar_xml_cancelamento_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_xml_cancelamento_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFC-e gerado pela API. | 

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

# **baixar_xml_evento_nfce**
> file baixar_xml_evento_nfce(id)

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Baixar XML do evento
        api_response = api_instance.baixar_xml_evento_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_xml_evento_nfce: %s\n" % e)
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

# **baixar_xml_inutilizacao_nfce**
> file baixar_xml_inutilizacao_nfce(id)

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Baixar XML da inutilização
        api_response = api_instance.baixar_xml_inutilizacao_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_xml_inutilizacao_nfce: %s\n" % e)
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

# **baixar_xml_nfce**
> file baixar_xml_nfce(id)

Baixar XML da NFC-e processada

Utilize esse endpoint para obter o XML da nota enviado para a SEFAZ, complementado com a informação do protocolo de autorização ou denegação de uso (TAG raiz `nfeProc`).    O XML só estará disponível nesse endpoint caso a nota tenha sido autorizada ou denegada pela SEFAZ. Para obter o XML nos demais casos, utilize o endpoint `GET /nfce/{id}/xml/nota`.    **Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único da NFC-e gerado pela API.

    try:
        # Baixar XML da NFC-e processada
        api_response = api_instance.baixar_xml_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_xml_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFC-e gerado pela API. | 

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

# **baixar_xml_nfce_nota**
> file baixar_xml_nfce_nota(id)

Baixar XML da NFC-e

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único da NFC-e gerado pela API.

    try:
        # Baixar XML da NFC-e
        api_response = api_instance.baixar_xml_nfce_nota(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_xml_nfce_nota: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFC-e gerado pela API. | 

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

# **baixar_xml_nfce_protocolo**
> file baixar_xml_nfce_protocolo(id)

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único da NFC-e gerado pela API.

    try:
        # Baixar XML do Protocolo da SEFAZ
        api_response = api_instance.baixar_xml_nfce_protocolo(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->baixar_xml_nfce_protocolo: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFC-e gerado pela API. | 

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

# **cancelar_nfce**
> DfeCancelamento cancelar_nfce(id, body=body)

Cancelar uma NFC-e autorizada

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único da NFC-e gerado pela API.
body = acbrapi_sdk.NfePedidoCancelamento() # NfePedidoCancelamento |  (optional)

    try:
        # Cancelar uma NFC-e autorizada
        api_response = api_instance.cancelar_nfce(id, body=body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->cancelar_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFC-e gerado pela API. | 
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

# **consultar_cancelamento_nfce**
> DfeCancelamento consultar_cancelamento_nfce(id)

Consultar o cancelamento da NFC-e

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único da NFC-e gerado pela API.

    try:
        # Consultar o cancelamento da NFC-e
        api_response = api_instance.consultar_cancelamento_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->consultar_cancelamento_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFC-e gerado pela API. | 

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

# **consultar_evento_nfce**
> DfeEvento consultar_evento_nfce(id)

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Consultar evento
        api_response = api_instance.consultar_evento_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->consultar_evento_nfce: %s\n" % e)
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

# **consultar_inutilizacao_nfce**
> DfeInutilizacao consultar_inutilizacao_nfce(id)

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Consultar a inutilização de sequência de numeração
        api_response = api_instance.consultar_inutilizacao_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->consultar_inutilizacao_nfce: %s\n" % e)
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

# **consultar_lote_nfce**
> DfeLote consultar_lote_nfce(id)

Consultar lote de NFC-e

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único do lote gerado pela API.

    try:
        # Consultar lote de NFC-e
        api_response = api_instance.consultar_lote_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->consultar_lote_nfce: %s\n" % e)
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

# **consultar_nfce**
> Dfe consultar_nfce(id)

Consultar NFC-e

Consulta os detalhes de uma NFC-e já existente. Forneça o ID único obtido de uma requisição de emissão ou de listagem de notas e a API irá retornar as informações da nota correspondente.

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único da NFC-e gerado pela API.

    try:
        # Consultar NFC-e
        api_response = api_instance.consultar_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->consultar_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFC-e gerado pela API. | 

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

# **consultar_status_sefaz_nfce**
> DfeSefazStatus consultar_status_sefaz_nfce(cpf_cnpj, autorizador=autorizador)

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF/CNPJ do emitente.  Utilize o valor sem máscara.
autorizador = 'autorizador_example' # str | Ambiente Autorizador.    Autorizadores disponíveis: `AM`, `BA`, `CE`, `GO`, `MG`, `MS`, `MT`, `PE`, `PR`, `RS`, `SP`, `SVRS`.    *Caso não seja informado, será utilizado o ambiente autorizador da UF do emitente.* (optional)

    try:
        # Consulta do Status do Serviço na SEFAZ Autorizadora
        api_response = api_instance.consultar_status_sefaz_nfce(cpf_cnpj, autorizador=autorizador)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->consultar_status_sefaz_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF/CNPJ do emitente.  Utilize o valor sem máscara. | 
 **autorizador** | **str**| Ambiente Autorizador.    Autorizadores disponíveis: &#x60;AM&#x60;, &#x60;BA&#x60;, &#x60;CE&#x60;, &#x60;GO&#x60;, &#x60;MG&#x60;, &#x60;MS&#x60;, &#x60;MT&#x60;, &#x60;PE&#x60;, &#x60;PR&#x60;, &#x60;RS&#x60;, &#x60;SP&#x60;, &#x60;SVRS&#x60;.    *Caso não seja informado, será utilizado o ambiente autorizador da UF do emitente.* | [optional] 

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

# **emitir_lote_nfce**
> DfeLote emitir_lote_nfce(body)

Emitir lote de NFC-e

**Informações adicionais**:  - Consumo: 1 unidade por NFC-e.

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    body = acbrapi_sdk.NfePedidoEmissaoLote() # NfePedidoEmissaoLote | 

    try:
        # Emitir lote de NFC-e
        api_response = api_instance.emitir_lote_nfce(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->emitir_lote_nfce: %s\n" % e)
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

# **emitir_nfce**
> Dfe emitir_nfce(body)

Emitir NFC-e

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    body = acbrapi_sdk.NfePedidoEmissao() # NfePedidoEmissao | 

    try:
        # Emitir NFC-e
        api_response = api_instance.emitir_nfce(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->emitir_nfce: %s\n" % e)
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

# **enviar_email_nfce**
> EmailStatusResponse enviar_email_nfce(id, logotipo=logotipo, nome_fantasia=nome_fantasia, mensagem_rodape=mensagem_rodape, resumido=resumido, qrcode_lateral=qrcode_lateral, largura=largura, margem=margem, body=body)

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único da NFC-e gerado pela API.
logotipo = False # bool | Imprime o documento com logotipo, desde que esteja cadastrado na empresa. (optional) (default to False)
nome_fantasia = False # bool | Exibe o nome fantasia do emitente, desde que esteja presente no XML da nota. (optional) (default to False)
mensagem_rodape = 'mensagem_rodape_example' # str | Imprime mensagem no rodapé do documento.    O caractere `|` (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * `\"esquerda\"`  * `\"esquerda|centro\"`  * `\"esquerda|centro|direita\"`  * `\"|centro\"`, `\"|centro|\"`  * `\"|centro|direita\"`  * `\"||direita\"`  * `\"esquerda||direita\"` (optional)
resumido = False # bool | Poderá ser impresso apenas o DANFE NFC-e resumido ou ecológico, sem o detalhamento dos itens da venda, desde que a Unidade Federada permita esta opção em sua legislação e o consumidor assim o solicite. (optional) (default to False)
qrcode_lateral = False # bool | Imprime o QRCode na lateral do DANFE NFC-e.    *Disponível apenas para DANFE com 80 milímetros de largura*. (optional) (default to False)
largura = 80 # int | Largura do DANFE NFC-e (em milímetros). (optional) (default to 80)
margem = '2' # str | Define as margens do DANFE NFC-e (em milímetros).    Essa propriedade pode ser especificada usando um, dois, três ou quatro valores (separados por vírgulas). Cada valor deve ser um número entre `0` e `9`.  * Quando **um** valor é especificado, a mesma margem é aplicada para **todos os quatro lados**.  * Quando **dois** valores são especificados, a primeira margem é aplicada aos **lados esquerdo e direito**, e a segunda aos **lados superior e inferior**.  * Quando **três** valores são especificados, a primeira margem é aplicada ao **lado esquerdo**, a segunda aos **lados superior e inferior**, e a terceira ao **lado direito**.  * Quando **quatro** valores são especificados, as margens são aplicadas aos lados **esquerdo**, **superior**, **direito** e **inferior**, nesta ordem (sentido horário).    **Exemplos de uso**:  * `margem=1`    - Margem esquerda: 1mm    - Margem superior: 1mm    - Margem direita: 1mm    - Margem inferior: 1mm  * `margem=1,2`    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 1mm    - Margem inferior: 2mm  * `margem=1,2,3`    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 3mm    - Margem inferior: 2mm  * `margem=1,2,3,4`    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 3mm    - Margem inferior: 4mm (optional) (default to '2')
body = acbrapi_sdk.DfePedidoEnvioEmail() # DfePedidoEnvioEmail |  (optional)

    try:
        # Enviar e-mail
        api_response = api_instance.enviar_email_nfce(id, logotipo=logotipo, nome_fantasia=nome_fantasia, mensagem_rodape=mensagem_rodape, resumido=resumido, qrcode_lateral=qrcode_lateral, largura=largura, margem=margem, body=body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->enviar_email_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFC-e gerado pela API. | 
 **logotipo** | **bool**| Imprime o documento com logotipo, desde que esteja cadastrado na empresa. | [optional] [default to False]
 **nome_fantasia** | **bool**| Exibe o nome fantasia do emitente, desde que esteja presente no XML da nota. | [optional] [default to False]
 **mensagem_rodape** | **str**| Imprime mensagem no rodapé do documento.    O caractere &#x60;|&#x60; (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * &#x60;\&quot;esquerda\&quot;&#x60;  * &#x60;\&quot;esquerda|centro\&quot;&#x60;  * &#x60;\&quot;esquerda|centro|direita\&quot;&#x60;  * &#x60;\&quot;|centro\&quot;&#x60;, &#x60;\&quot;|centro|\&quot;&#x60;  * &#x60;\&quot;|centro|direita\&quot;&#x60;  * &#x60;\&quot;||direita\&quot;&#x60;  * &#x60;\&quot;esquerda||direita\&quot;&#x60; | [optional] 
 **resumido** | **bool**| Poderá ser impresso apenas o DANFE NFC-e resumido ou ecológico, sem o detalhamento dos itens da venda, desde que a Unidade Federada permita esta opção em sua legislação e o consumidor assim o solicite. | [optional] [default to False]
 **qrcode_lateral** | **bool**| Imprime o QRCode na lateral do DANFE NFC-e.    *Disponível apenas para DANFE com 80 milímetros de largura*. | [optional] [default to False]
 **largura** | **int**| Largura do DANFE NFC-e (em milímetros). | [optional] [default to 80]
 **margem** | **str**| Define as margens do DANFE NFC-e (em milímetros).    Essa propriedade pode ser especificada usando um, dois, três ou quatro valores (separados por vírgulas). Cada valor deve ser um número entre &#x60;0&#x60; e &#x60;9&#x60;.  * Quando **um** valor é especificado, a mesma margem é aplicada para **todos os quatro lados**.  * Quando **dois** valores são especificados, a primeira margem é aplicada aos **lados esquerdo e direito**, e a segunda aos **lados superior e inferior**.  * Quando **três** valores são especificados, a primeira margem é aplicada ao **lado esquerdo**, a segunda aos **lados superior e inferior**, e a terceira ao **lado direito**.  * Quando **quatro** valores são especificados, as margens são aplicadas aos lados **esquerdo**, **superior**, **direito** e **inferior**, nesta ordem (sentido horário).    **Exemplos de uso**:  * &#x60;margem&#x3D;1&#x60;    - Margem esquerda: 1mm    - Margem superior: 1mm    - Margem direita: 1mm    - Margem inferior: 1mm  * &#x60;margem&#x3D;1,2&#x60;    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 1mm    - Margem inferior: 2mm  * &#x60;margem&#x3D;1,2,3&#x60;    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 3mm    - Margem inferior: 2mm  * &#x60;margem&#x3D;1,2,3,4&#x60;    - Margem esquerda: 1mm    - Margem superior: 2mm    - Margem direita: 3mm    - Margem inferior: 4mm | [optional] [default to &#39;2&#39;]
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

# **inutilizar_numeracao_nfce**
> DfeInutilizacao inutilizar_numeracao_nfce(body)

Inutilizar uma sequência de numeração de NFC-e

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    body = acbrapi_sdk.DfePedidoInutilizacao() # DfePedidoInutilizacao | 

    try:
        # Inutilizar uma sequência de numeração de NFC-e
        api_response = api_instance.inutilizar_numeracao_nfce(body)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->inutilizar_numeracao_nfce: %s\n" % e)
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

# **listar_eventos_nfce**
> DfeEventoListagem listar_eventos_nfce(dfe_id, top=top, skip=skip, inlinecount=inlinecount)

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    dfe_id = 'dfe_id_example' # str | ID único gerado pela API para o documento fiscal.
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)

    try:
        # Listar eventos
        api_response = api_instance.listar_eventos_nfce(dfe_id, top=top, skip=skip, inlinecount=inlinecount)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->listar_eventos_nfce: %s\n" % e)
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

# **listar_lotes_nfce**
> DfeLoteListagem listar_lotes_nfce(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia)

Listar lotes de NFC-e

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ do emitente.  Utilize o valor sem máscara.
ambiente = 'ambiente_example' # str | Identificação do Ambiente.    Valores aceitos: homologacao, producao
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)
referencia = 'referencia_example' # str |  (optional)

    try:
        # Listar lotes de NFC-e
        api_response = api_instance.listar_lotes_nfce(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->listar_lotes_nfce: %s\n" % e)
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

# **listar_nfce**
> DfeListagem listar_nfce(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia, chave=chave, serie=serie)

Listar NFC-e

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ do emitente.    Utilize o valor sem máscara.
ambiente = 'ambiente_example' # str | Identificação do Ambiente.    Valores aceitos: homologacao, producao
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (optional) (default to 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (optional) (default to 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (optional) (default to False)
referencia = 'referencia_example' # str | Seu identificador único para o documento. (optional)
chave = 'chave_example' # str | Chave de acesso do DF-e. (optional)
serie = 'serie_example' # str | Série do DF-e. (optional)

    try:
        # Listar NFC-e
        api_response = api_instance.listar_nfce(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia, chave=chave, serie=serie)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->listar_nfce: %s\n" % e)
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

# **sincronizar_nfce**
> DfeSincronizacao sincronizar_nfce(id)

Sincroniza dados na NFC-e a partir da SEFAZ

Realiza a sincronização dos dados a partir da consulta da situação atual da NFC-e na Base de Dados do Portal da Secretaria de Fazenda Estadual.    **Cenários de uso**:  * Sincronizar uma nota que se encontra com o status `erro` na API, mas está autorizada na SEFAZ (útil em casos de erros de transmissão com a SEFAZ, como instabilidades e timeouts).  * Sincronizar uma nota que se encontra com o status `autorizado`na API, mas está cancelada na SEFAZ.  * Sincronizar todos os eventos de Cancelamento, Carta de Correção e EPEC de uma nota que porventura não tenham sido feitos a partir da API.    **Informações adicionais**:  - Consumo: 1 unidade por evento sincronizado ou requisição.

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
    api_instance = acbrapi_sdk.NfceApi(api_client)
    id = 'id_example' # str | ID único da NFC-e gerado pela API.

    try:
        # Sincroniza dados na NFC-e a partir da SEFAZ
        api_response = api_instance.sincronizar_nfce(id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling NfceApi->sincronizar_nfce: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da NFC-e gerado pela API. | 

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

