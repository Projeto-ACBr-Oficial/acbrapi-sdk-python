# acbrapi_sdk.CteApi

Todas as URIs relativas a *https://prod.acbr.api.br*

Método | Endpoint | Descrição
------------- | ------------- | -------------
[**baixar_pdf_cancelamento_cte**](CteApi.md#baixar_pdf_cancelamento_cte) | **GET** /cte/{id}/cancelamento/pdf | Baixar PDF do cancelamento
[**baixar_pdf_carta_correcao_cte**](CteApi.md#baixar_pdf_carta_correcao_cte) | **GET** /cte/{id}/carta-correcao/pdf | Baixar PDF da carta de correção
[**baixar_pdf_cte**](CteApi.md#baixar_pdf_cte) | **GET** /cte/{id}/pdf | Baixar PDF do DACTE
[**baixar_pdf_evento_cte**](CteApi.md#baixar_pdf_evento_cte) | **GET** /cte/eventos/{id}/pdf | Baixar PDF do evento
[**baixar_xml_cancelamento_cte**](CteApi.md#baixar_xml_cancelamento_cte) | **GET** /cte/{id}/cancelamento/xml | Baixar XML do cancelamento
[**baixar_xml_carta_correcao_cte**](CteApi.md#baixar_xml_carta_correcao_cte) | **GET** /cte/{id}/carta-correcao/xml | Baixar XML da carta de correção
[**baixar_xml_cte**](CteApi.md#baixar_xml_cte) | **GET** /cte/{id}/xml | Baixar XML do CT-e processado
[**baixar_xml_cte_conhecimento**](CteApi.md#baixar_xml_cte_conhecimento) | **GET** /cte/{id}/xml/conhecimento | Baixar XML do CT-e
[**baixar_xml_cte_protocolo**](CteApi.md#baixar_xml_cte_protocolo) | **GET** /cte/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
[**baixar_xml_evento_cte**](CteApi.md#baixar_xml_evento_cte) | **GET** /cte/eventos/{id}/xml | Baixar XML do evento
[**cancelar_cte**](CteApi.md#cancelar_cte) | **POST** /cte/{id}/cancelamento | Cancelar um CT-e autorizado
[**consultar_cancelamento_cte**](CteApi.md#consultar_cancelamento_cte) | **GET** /cte/{id}/cancelamento | Consultar o cancelamento do CT-e
[**consultar_carta_correcao_cte**](CteApi.md#consultar_carta_correcao_cte) | **GET** /cte/{id}/carta-correcao | Consultar a solicitação de correção do CT-e
[**consultar_cte**](CteApi.md#consultar_cte) | **GET** /cte/{id} | Consultar CT-e
[**consultar_evento_cte**](CteApi.md#consultar_evento_cte) | **GET** /cte/eventos/{id} | Consultar evento
[**consultar_status_sefaz_cte**](CteApi.md#consultar_status_sefaz_cte) | **GET** /cte/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
[**criar_carta_correcao_cte**](CteApi.md#criar_carta_correcao_cte) | **POST** /cte/{id}/carta-correcao | Solicitar correção do CT-e
[**emitir_cte**](CteApi.md#emitir_cte) | **POST** /cte | Emitir CT-e
[**emitir_cte_simp**](CteApi.md#emitir_cte_simp) | **POST** /cte/simp | Emitir CT-e Simplificado
[**listar_cte**](CteApi.md#listar_cte) | **GET** /cte | Listar CT-e
[**sincronizar_cte**](CteApi.md#sincronizar_cte) | **POST** /cte/{id}/sincronizar | Sincroniza dados no CT-e a partir da SEFAZ


# **baixar_pdf_cancelamento_cte**
> file baixar_pdf_cancelamento_cte(id)

Baixar PDF do cancelamento

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do CT-e gerado pela API.

    try:
        # Baixar PDF do cancelamento
        api_response = api_instance.baixar_pdf_cancelamento_cte(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->baixar_pdf_cancelamento_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e gerado pela API. | 

### Tipo do retorno

**file**

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: */*

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **baixar_pdf_carta_correcao_cte**
> file baixar_pdf_carta_correcao_cte(id)

Baixar PDF da carta de correção

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do CT-e gerado pela API.

    try:
        # Baixar PDF da carta de correção
        api_response = api_instance.baixar_pdf_carta_correcao_cte(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->baixar_pdf_carta_correcao_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e gerado pela API. | 

### Tipo do retorno

**file**

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: */*

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **baixar_pdf_cte**
> file baixar_pdf_cte(id, logotipo=logotipo)

Baixar PDF do DACTE

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do CT-e gerado pela API.
logotipo = False # bool | Imprime o documento com logotipo, desde que esteja cadastrado na empresa. (opcional) (default False)

    try:
        # Baixar PDF do DACTE
        api_response = api_instance.baixar_pdf_cte(id, logotipo=logotipo)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->baixar_pdf_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e gerado pela API. | 
 **logotipo** | **bool**| Imprime o documento com logotipo, desde que esteja cadastrado na empresa. | [opcional] [default False]

### Tipo do retorno

**file**

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: */*

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **baixar_pdf_evento_cte**
> file baixar_pdf_evento_cte(id)

Baixar PDF do evento

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Baixar PDF do evento
        api_response = api_instance.baixar_pdf_evento_cte(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->baixar_pdf_evento_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do evento gerado pela API. | 

### Tipo do retorno

**file**

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: */*

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **baixar_xml_cancelamento_cte**
> file baixar_xml_cancelamento_cte(id)

Baixar XML do cancelamento

**Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do CT-e gerado pela API.

    try:
        # Baixar XML do cancelamento
        api_response = api_instance.baixar_xml_cancelamento_cte(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->baixar_xml_cancelamento_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e gerado pela API. | 

### Tipo do retorno

**file**

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: */*

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **baixar_xml_carta_correcao_cte**
> file baixar_xml_carta_correcao_cte(id)

Baixar XML da carta de correção

**Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do CT-e gerado pela API.

    try:
        # Baixar XML da carta de correção
        api_response = api_instance.baixar_xml_carta_correcao_cte(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->baixar_xml_carta_correcao_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e gerado pela API. | 

### Tipo do retorno

**file**

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: */*

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **baixar_xml_cte**
> file baixar_xml_cte(id)

Baixar XML do CT-e processado

Utilize esse endpoint para obter o XML do conhecimento enviado para a SEFAZ, complementado com a informação do protocolo de autorização de uso (TAG raiz `cteProc`).    O XML só estará disponível nesse endpoint caso o conhecimento tenha sido autorizado pela SEFAZ. Para obter o XML nos demais casos, utilize o endpoint `GET /cte/{id}/xml/conhecimento`.    **Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do CT-e gerado pela API.

    try:
        # Baixar XML do CT-e processado
        api_response = api_instance.baixar_xml_cte(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->baixar_xml_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e gerado pela API. | 

### Tipo do retorno

**file**

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: */*

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **baixar_xml_cte_conhecimento**
> file baixar_xml_cte_conhecimento(id)

Baixar XML do CT-e

Utilize esse endpoint para obter o XML do conhecimento enviado para a SEFAZ.    O XML estará disponível nesse endpoint mesmo em casos que o conhecimento tenha sido rejeitado.    **Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único da CT-e gerado pela API.

    try:
        # Baixar XML do CT-e
        api_response = api_instance.baixar_xml_cte_conhecimento(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->baixar_xml_cte_conhecimento: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da CT-e gerado pela API. | 

### Tipo do retorno

**file**

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: */*

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **baixar_xml_cte_protocolo**
> file baixar_xml_cte_protocolo(id)

Baixar XML do Protocolo da SEFAZ

**Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único da CT-e gerado pela API.

    try:
        # Baixar XML do Protocolo da SEFAZ
        api_response = api_instance.baixar_xml_cte_protocolo(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->baixar_xml_cte_protocolo: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da CT-e gerado pela API. | 

### Tipo do retorno

**file**

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: */*

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **baixar_xml_evento_cte**
> file baixar_xml_evento_cte(id)

Baixar XML do evento

**Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Baixar XML do evento
        api_response = api_instance.baixar_xml_evento_cte(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->baixar_xml_evento_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do evento gerado pela API. | 

### Tipo do retorno

**file**

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: */*

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **cancelar_cte**
> DfeCancelamento cancelar_cte(id, body=body)

Cancelar um CT-e autorizado

**Informações adicionais**:  - Consumo: 1 unidade por requisição.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do CT-e gerado pela API.
body = acbrapi_sdk.CtePedidoCancelamento() # CtePedidoCancelamento |  (opcional)

    try:
        # Cancelar um CT-e autorizado
        api_response = api_instance.cancelar_cte(id, body=body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->cancelar_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e gerado pela API. | 
 **body** | [**CtePedidoCancelamento**](CtePedidoCancelamento.md)|  | [opcional] 

### Tipo do retorno

[**DfeCancelamento**](DfeCancelamento.md)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: application/json
 - **Accept**: application/json

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **consultar_cancelamento_cte**
> DfeCancelamento consultar_cancelamento_cte(id)

Consultar o cancelamento do CT-e

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do CT-e gerado pela API.

    try:
        # Consultar o cancelamento do CT-e
        api_response = api_instance.consultar_cancelamento_cte(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->consultar_cancelamento_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e gerado pela API. | 

### Tipo do retorno

[**DfeCancelamento**](DfeCancelamento.md)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: application/json

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **consultar_carta_correcao_cte**
> CteCartaCorrecao consultar_carta_correcao_cte(id)

Consultar a solicitação de correção do CT-e

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do CT-e gerado pela API.

    try:
        # Consultar a solicitação de correção do CT-e
        api_response = api_instance.consultar_carta_correcao_cte(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->consultar_carta_correcao_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e gerado pela API. | 

### Tipo do retorno

[**CteCartaCorrecao**](CteCartaCorrecao.md)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: application/json

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **consultar_cte**
> Dfe consultar_cte(id)

Consultar CT-e

Consulta os detalhes de um CT-e já existente. Forneça o ID único obtido de uma requisição de emissão ou de listagem de CT-e e a API irá retornar as informações do CT-e correspondente.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do CT-e gerado pela API.

    try:
        # Consultar CT-e
        api_response = api_instance.consultar_cte(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->consultar_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e gerado pela API. | 

### Tipo do retorno

[**Dfe**](Dfe.md)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: application/json

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **consultar_evento_cte**
> DfeEvento consultar_evento_cte(id)

Consultar evento

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do evento gerado pela API.

    try:
        # Consultar evento
        api_response = api_instance.consultar_evento_cte(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->consultar_evento_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do evento gerado pela API. | 

### Tipo do retorno

[**DfeEvento**](DfeEvento.md)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: application/json

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **consultar_status_sefaz_cte**
> DfeSefazStatus consultar_status_sefaz_cte(cpf_cnpj, autorizador=autorizador)

Consulta do Status do Serviço na SEFAZ Autorizadora

Consulta do status do serviço prestado pelo Portal da Secretaria de Fazenda Estadual.    A API mantém a última consulta em cache por 5 minutos, evitando sobrecarregar desnecessariamente os servidores da SEFAZ (conforme orientação do MOC - versão 3.0.0a, item 4.6.3). Dessa forma, você poderá chamar esse endpoint quantas vezes quiser, sem preocupar-se em ter o seu CNPJ bloqueado por consumo indevido (Rejeição 656).

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF/CNPJ do emitente.  Utilize o valor sem máscara.
autorizador = 'autorizador_example' # str | Ambiente Autorizador.    Autorizadores disponíveis: `MT`, `MS`, `MG`, `PR`, `RS`, `SP`, `SVRS`, `SVSP`, `AN`.    *Caso não seja informado, será utilizado o ambiente autorizador da UF do emitente.* (opcional)

    try:
        # Consulta do Status do Serviço na SEFAZ Autorizadora
        api_response = api_instance.consultar_status_sefaz_cte(cpf_cnpj, autorizador=autorizador)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->consultar_status_sefaz_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF/CNPJ do emitente.  Utilize o valor sem máscara. | 
 **autorizador** | **str**| Ambiente Autorizador.    Autorizadores disponíveis: &#x60;MT&#x60;, &#x60;MS&#x60;, &#x60;MG&#x60;, &#x60;PR&#x60;, &#x60;RS&#x60;, &#x60;SP&#x60;, &#x60;SVRS&#x60;, &#x60;SVSP&#x60;, &#x60;AN&#x60;.    *Caso não seja informado, será utilizado o ambiente autorizador da UF do emitente.* | [opcional] 

### Tipo do retorno

[**DfeSefazStatus**](DfeSefazStatus.md)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: application/json

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **criar_carta_correcao_cte**
> CteCartaCorrecao criar_carta_correcao_cte(id, body)

Solicitar correção do CT-e

É possível enviar até 20 correções diferentes, sendo que será válido sempre a última correção enviada.    **Informações adicionais**:  - Consumo: 1 unidade por requisição.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do CT-e gerado pela API.
body = acbrapi_sdk.CtePedidoCartaCorrecao() # CtePedidoCartaCorrecao | 

    try:
        # Solicitar correção do CT-e
        api_response = api_instance.criar_carta_correcao_cte(id, body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->criar_carta_correcao_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e gerado pela API. | 
 **body** | [**CtePedidoCartaCorrecao**](CtePedidoCartaCorrecao.md)|  | 

### Tipo do retorno

[**CteCartaCorrecao**](CteCartaCorrecao.md)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: application/json
 - **Accept**: application/json

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **emitir_cte**
> Dfe emitir_cte(body)

Emitir CT-e

**Informações adicionais**:  - Consumo: 1 unidade por requisição.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    body = acbrapi_sdk.CtePedidoEmissao() # CtePedidoEmissao | 

    try:
        # Emitir CT-e
        api_response = api_instance.emitir_cte(body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->emitir_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **body** | [**CtePedidoEmissao**](CtePedidoEmissao.md)|  | 

### Tipo do retorno

[**Dfe**](Dfe.md)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: application/json
 - **Accept**: application/json

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **emitir_cte_simp**
> Dfe emitir_cte_simp(body)

Emitir CT-e Simplificado

**Informações adicionais**:  - Consumo: 1 unidade por requisição.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    body = acbrapi_sdk.CteSimpPedidoEmissao() # CteSimpPedidoEmissao | 

    try:
        # Emitir CT-e Simplificado
        api_response = api_instance.emitir_cte_simp(body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->emitir_cte_simp: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **body** | [**CteSimpPedidoEmissao**](CteSimpPedidoEmissao.md)|  | 

### Tipo do retorno

[**Dfe**](Dfe.md)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: application/json
 - **Accept**: application/json

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **listar_cte**
> DfeListagem listar_cte(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia, chave=chave, serie=serie)

Listar CT-e

Retorna a lista de CT-e de acordo com os critérios de busca utilizados. Os CT-e são retornados ordenados pela data da criação, com os mais recentes aparecendo primeiro.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ do emitente.    Utilize o valor sem máscara.
ambiente = 'ambiente_example' # str | Identificação do Ambiente.    Valores aceitos: homologacao, producao
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (opcional) (default 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (opcional) (default 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (opcional) (default False)
referencia = 'referencia_example' # str | Seu identificador único para o documento. (opcional)
chave = 'chave_example' # str | Chave de acesso do DF-e. (opcional)
serie = 'serie_example' # str | Série do DF-e. (opcional)

    try:
        # Listar CT-e
        api_response = api_instance.listar_cte(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia, chave=chave, serie=serie)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->listar_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| Filtrar pelo CPF ou CNPJ do emitente.    Utilize o valor sem máscara. | 
 **ambiente** | **str**| Identificação do Ambiente.    Valores aceitos: homologacao, producao | 
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [opcional] [default 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [opcional] [default 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [opcional] [default False]
 **referencia** | **str**| Seu identificador único para o documento. | [opcional] 
 **chave** | **str**| Chave de acesso do DF-e. | [opcional] 
 **serie** | **str**| Série do DF-e. | [opcional] 

### Tipo do retorno

[**DfeListagem**](DfeListagem.md)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: application/json

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **sincronizar_cte**
> DfeSincronizacao sincronizar_cte(id)

Sincroniza dados no CT-e a partir da SEFAZ

Realiza a sincronização dos dados a partir da consulta da situação atual da CT-e na Base de Dados do Portal da Secretaria de Fazenda Estadual.    **Cenários de uso**:  * Sincronizar um CT-e que se encontra com o status `erro` na API, mas está autorizado na SEFAZ (útil em casos de erros de transmissão com a SEFAZ, como instabilidades e timeouts).  * Sincronizar um CT-e que se encontra com o status `autorizado`na API, mas está cancelado na SEFAZ.  * Sincronizar todos os eventos de Cancelamento e Carta de Correção de um CT-e que porventura não tenham sido feitos a partir da API.    **Informações adicionais**:  - Consumo: 1 unidade por evento sincronizado ou requisição.

### Exemplo

* Autenticação OAuth (oauth2):
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

# Abre um contexto com uma instancia do cliente da API
with acbrapi_sdk.ApiClient(configuration) as api_client:
    # Cria uma instancia da classe da API
    api_instance = acbrapi_sdk.CteApi(api_client)
    id = 'id_example' # str | ID único do CT-e gerado pela API.

    try:
        # Sincroniza dados no CT-e a partir da SEFAZ
        api_response = api_instance.sincronizar_cte(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CteApi->sincronizar_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do CT-e gerado pela API. | 

### Tipo do retorno

[**DfeSincronizacao**](DfeSincronizacao.md)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: application/json

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

