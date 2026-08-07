# acbrapi_sdk.DceApi

Todas as URIs relativas a *https://prod.acbr.api.br*

Método | Endpoint | Descrição
------------- | ------------- | -------------
[**baixar_pdf_dce**](DceApi.md#baixar_pdf_dce) | **GET** /dce/{id}/pdf | Baixar PDF do DACE
[**baixar_xml_cancelamento_dce**](DceApi.md#baixar_xml_cancelamento_dce) | **GET** /dce/{id}/cancelamento/xml | Baixar XML do cancelamento
[**baixar_xml_dce**](DceApi.md#baixar_xml_dce) | **GET** /dce/{id}/xml | Baixar XML da DC-e processada
[**baixar_xml_dce_declaracao**](DceApi.md#baixar_xml_dce_declaracao) | **GET** /dce/{id}/xml/declaracao | Baixar XML da DC-e
[**baixar_xml_dce_protocolo**](DceApi.md#baixar_xml_dce_protocolo) | **GET** /dce/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
[**cancelar_dce**](DceApi.md#cancelar_dce) | **POST** /dce/{id}/cancelamento | Cancelar uma DC-e autorizada
[**consultar_cancelamento_dce**](DceApi.md#consultar_cancelamento_dce) | **GET** /dce/{id}/cancelamento | Consultar o cancelamento da DC-e
[**consultar_dce**](DceApi.md#consultar_dce) | **GET** /dce/{id} | Consultar DC-e
[**consultar_status_sefaz_dce**](DceApi.md#consultar_status_sefaz_dce) | **GET** /dce/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
[**emitir_dce**](DceApi.md#emitir_dce) | **POST** /dce | Emitir DC-e
[**listar_dce**](DceApi.md#listar_dce) | **GET** /dce | Listar DC-e


# **baixar_pdf_dce**
> file baixar_pdf_dce(id)

Baixar PDF do DACE

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
    api_instance = acbrapi_sdk.DceApi(api_client)
    id = 'id_example' # str | ID único da DC-e gerado pela API.

    try:
        # Baixar PDF do DACE
        api_response = api_instance.baixar_pdf_dce(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar DceApi->baixar_pdf_dce: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da DC-e gerado pela API. | 

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

# **baixar_xml_cancelamento_dce**
> file baixar_xml_cancelamento_dce(id)

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
    api_instance = acbrapi_sdk.DceApi(api_client)
    id = 'id_example' # str | ID único da DC-e gerada pela API.

    try:
        # Baixar XML do cancelamento
        api_response = api_instance.baixar_xml_cancelamento_dce(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar DceApi->baixar_xml_cancelamento_dce: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da DC-e gerada pela API. | 

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

# **baixar_xml_dce**
> file baixar_xml_dce(id)

Baixar XML da DC-e processada

Utilize esse endpoint para obter o XML da DC-e enviada para a SEFAZ, complementado com a informação do protocolo de autorização de uso (TAG raiz `dceProc`).    O XML só estará disponível nesse endpoint caso a DC-e tenha sido autorizada pela SEFAZ. Para obter o XML nos demais casos, utilize o endpoint `GET /dce/{id}/xml/declaracao`.    **Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.DceApi(api_client)
    id = 'id_example' # str | ID único da DC-e gerada pela API.

    try:
        # Baixar XML da DC-e processada
        api_response = api_instance.baixar_xml_dce(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar DceApi->baixar_xml_dce: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da DC-e gerada pela API. | 

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

# **baixar_xml_dce_declaracao**
> file baixar_xml_dce_declaracao(id)

Baixar XML da DC-e

Utilize esse endpoint para obter o XML da DC-e enviada para a SEFAZ.    O XML estará disponível nesse endpoint mesmo em casos que a declaração tenha sido rejeitada.    **Informações adicionais**:  - Consumo: Primeira requisição isenta, posteriores 1 unidade por requisição.

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
    api_instance = acbrapi_sdk.DceApi(api_client)
    id = 'id_example' # str | ID único da DC-e gerada pela API.

    try:
        # Baixar XML da DC-e
        api_response = api_instance.baixar_xml_dce_declaracao(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar DceApi->baixar_xml_dce_declaracao: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da DC-e gerada pela API. | 

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

# **baixar_xml_dce_protocolo**
> file baixar_xml_dce_protocolo(id)

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
    api_instance = acbrapi_sdk.DceApi(api_client)
    id = 'id_example' # str | ID único da DC-e gerada pela API.

    try:
        # Baixar XML do Protocolo da SEFAZ
        api_response = api_instance.baixar_xml_dce_protocolo(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar DceApi->baixar_xml_dce_protocolo: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da DC-e gerada pela API. | 

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

# **cancelar_dce**
> DfeCancelamento cancelar_dce(id, body=body)

Cancelar uma DC-e autorizada

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
    api_instance = acbrapi_sdk.DceApi(api_client)
    id = 'id_example' # str | ID único da DC-e gerada pela API.
body = acbrapi_sdk.DcePedidoCancelamento() # DcePedidoCancelamento |  (opcional)

    try:
        # Cancelar uma DC-e autorizada
        api_response = api_instance.cancelar_dce(id, body=body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar DceApi->cancelar_dce: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da DC-e gerada pela API. | 
 **body** | [**DcePedidoCancelamento**](DcePedidoCancelamento.md)|  | [opcional] 

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

# **consultar_cancelamento_dce**
> DfeCancelamento consultar_cancelamento_dce(id)

Consultar o cancelamento da DC-e

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
    api_instance = acbrapi_sdk.DceApi(api_client)
    id = 'id_example' # str | ID único da DC-e gerada pela API.

    try:
        # Consultar o cancelamento da DC-e
        api_response = api_instance.consultar_cancelamento_dce(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar DceApi->consultar_cancelamento_dce: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da DC-e gerada pela API. | 

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

# **consultar_dce**
> Dfe consultar_dce(id)

Consultar DC-e

Consulta os detalhes de uma DC-e já existente. Forneça o ID único obtido de uma requisição de emissão ou de listagem de DC-e e a API irá retornar as informações da DC-e correspondente.

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
    api_instance = acbrapi_sdk.DceApi(api_client)
    id = 'id_example' # str | ID único da DC-e gerada pela API.

    try:
        # Consultar DC-e
        api_response = api_instance.consultar_dce(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar DceApi->consultar_dce: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único da DC-e gerada pela API. | 

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

# **consultar_status_sefaz_dce**
> DfeSefazStatus consultar_status_sefaz_dce(cpf_cnpj, autorizador=autorizador)

Consulta do Status do Serviço na SEFAZ Autorizadora

Consulta do status do serviço prestado pelo Portal da Secretaria de Fazenda Estadual.    A API mantém a última consulta em cache por 5 minutos, evitando sobrecarregar desnecessariamente os servidores da SEFAZ.

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
    api_instance = acbrapi_sdk.DceApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF/CNPJ do emitente.  Utilize o valor sem máscara.
autorizador = 'autorizador_example' # str | Ambiente Autorizador.    Autorizadores disponíveis: `AN`.    *Caso não seja informado, será utilizado o ambiente autorizador da UF do emitente.* (opcional)

    try:
        # Consulta do Status do Serviço na SEFAZ Autorizadora
        api_response = api_instance.consultar_status_sefaz_dce(cpf_cnpj, autorizador=autorizador)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar DceApi->consultar_status_sefaz_dce: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF/CNPJ do emitente.  Utilize o valor sem máscara. | 
 **autorizador** | **str**| Ambiente Autorizador.    Autorizadores disponíveis: &#x60;AN&#x60;.    *Caso não seja informado, será utilizado o ambiente autorizador da UF do emitente.* | [opcional] 

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

# **emitir_dce**
> Dfe emitir_dce(body)

Emitir DC-e

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
    api_instance = acbrapi_sdk.DceApi(api_client)
    body = acbrapi_sdk.DcePedidoEmissao() # DcePedidoEmissao | 

    try:
        # Emitir DC-e
        api_response = api_instance.emitir_dce(body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar DceApi->emitir_dce: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **body** | [**DcePedidoEmissao**](DcePedidoEmissao.md)|  | 

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

# **listar_dce**
> DfeListagem listar_dce(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia, chave=chave, serie=serie)

Listar DC-e

Retorna a lista de DC-e de acordo com os critérios de busca utilizados. As DC-e são retornadas ordenadas pela data da criação, com as mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.DceApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ do emitente.    Utilize o valor sem máscara.
ambiente = 'ambiente_example' # str | Identificação do Ambiente.    Valores aceitos: homologacao, producao
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (opcional) (default 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (opcional) (default 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (opcional) (default False)
referencia = 'referencia_example' # str | Seu identificador único para o documento. (opcional)
chave = 'chave_example' # str | Chave de acesso do DF-e. (opcional)
serie = 'serie_example' # str | Série do DF-e. (opcional)

    try:
        # Listar DC-e
        api_response = api_instance.listar_dce(cpf_cnpj, ambiente, top=top, skip=skip, inlinecount=inlinecount, referencia=referencia, chave=chave, serie=serie)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar DceApi->listar_dce: %s\n" % e)
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

