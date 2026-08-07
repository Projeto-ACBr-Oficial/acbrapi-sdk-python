# acbrapi_sdk.ContaApi

Todas as URIs relativas a *https://prod.acbr.api.br*

Método | Endpoint | Descrição
------------- | ------------- | -------------
[**consultar_cota_conta**](ContaApi.md#consultar_cota_conta) | **GET** /conta/cotas/{nome} | Consultar o limite de uso e o consumo de uma cota específica.
[**consultar_cota_pre_pago**](ContaApi.md#consultar_cota_pre_pago) | **GET** /conta/cotas/prepago | Consultar o resumo da cota de créditos pré-pagos.
[**listar_cotas_conta**](ContaApi.md#listar_cotas_conta) | **GET** /conta/cotas | Consultar os limites de uso e consumo das cotas disponíveis, exceto a cota de créditos pré-pagos.
[**listar_extrato_creditos_conta**](ContaApi.md#listar_extrato_creditos_conta) | **GET** /conta/extrato | Consultar o extrato de movimentação de créditos do tenant atual.


# **consultar_cota_conta**
> ContaCota consultar_cota_conta(nome)

Consultar o limite de uso e o consumo de uma cota específica.

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
    api_instance = acbrapi_sdk.ContaApi(api_client)
    nome = 'nome_example' # str | Nome da cota a ser consultada.

    try:
        # Consultar o limite de uso e o consumo de uma cota específica.
        api_response = api_instance.consultar_cota_conta(nome)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar ContaApi->consultar_cota_conta: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **nome** | **str**| Nome da cota a ser consultada. | 

### Tipo do retorno

[**ContaCota**](ContaCota.md)

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

# **consultar_cota_pre_pago**
> ContaCotaPrePago consultar_cota_pre_pago()

Consultar o resumo da cota de créditos pré-pagos.

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
    api_instance = acbrapi_sdk.ContaApi(api_client)
    
    try:
        # Consultar o resumo da cota de créditos pré-pagos.
        api_response = api_instance.consultar_cota_pre_pago()
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar ContaApi->consultar_cota_pre_pago: %s\n" % e)
```

### Parâmetros
Este endpoint não usa parâmetros.

### Tipo do retorno

[**ContaCotaPrePago**](ContaCotaPrePago.md)

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

# **listar_cotas_conta**
> ContaCotaListagem listar_cotas_conta()

Consultar os limites de uso e consumo das cotas disponíveis, exceto a cota de créditos pré-pagos.

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
    api_instance = acbrapi_sdk.ContaApi(api_client)
    
    try:
        # Consultar os limites de uso e consumo das cotas disponíveis, exceto a cota de créditos pré-pagos.
        api_response = api_instance.listar_cotas_conta()
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar ContaApi->listar_cotas_conta: %s\n" % e)
```

### Parâmetros
Este endpoint não usa parâmetros.

### Tipo do retorno

[**ContaCotaListagem**](ContaCotaListagem.md)

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

# **listar_extrato_creditos_conta**
> ContaExtratoCreditoListagem listar_extrato_creditos_conta(data_inicial=data_inicial, data_final=data_final, top=top, skip=skip, limit=limit)

Consultar o extrato de movimentação de créditos do tenant atual.

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
    api_instance = acbrapi_sdk.ContaApi(api_client)
    data_inicial = 'data_inicial_example' # str |  (opcional)
data_final = 'data_final_example' # str |  (opcional)
top = 56 # int |  (opcional)
skip = 56 # int |  (opcional)
limit = 56 # int |  (opcional)

    try:
        # Consultar o extrato de movimentação de créditos do tenant atual.
        api_response = api_instance.listar_extrato_creditos_conta(data_inicial=data_inicial, data_final=data_final, top=top, skip=skip, limit=limit)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar ContaApi->listar_extrato_creditos_conta: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **data_inicial** | **str**|  | [opcional] 
 **data_final** | **str**|  | [opcional] 
 **top** | **int**|  | [opcional] 
 **skip** | **int**|  | [opcional] 
 **limit** | **int**|  | [opcional] 

### Tipo do retorno

[**ContaExtratoCreditoListagem**](ContaExtratoCreditoListagem.md)

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

