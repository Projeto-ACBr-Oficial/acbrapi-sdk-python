# acbrapi_sdk.CepApi

Todas as URIs relativas a *https://prod.acbr.api.br*

Método | Endpoint | Descrição
------------- | ------------- | -------------
[**consultar_cep**](CepApi.md#consultar_cep) | **GET** /cep/{Cep} | Consultar endereço através do CEP


# **consultar_cep**
> CepEndereco consultar_cep(cep)

Consultar endereço através do CEP

**Informações adicionais**:  - Consumo: 0,1 unidade requisição.  - Em sandbox, a consulta é permitida somente para os seguintes CEP:    `18270000` Tatuí/SP    `01310300` São Paulo/SP    `22010000` Rio de Janeiro/RJ    `80020130` Curitiba/PR

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
    api_instance = acbrapi_sdk.CepApi(api_client)
    cep = 'cep_example' # str | CEP sem máscara.

    try:
        # Consultar endereço através do CEP
        api_response = api_instance.consultar_cep(cep)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CepApi->consultar_cep: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cep** | **str**| CEP sem máscara. | 

### Tipo do retorno

[**CepEndereco**](CepEndereco.md)

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

