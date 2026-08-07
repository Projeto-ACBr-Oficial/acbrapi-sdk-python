# acbrapi_sdk.CnpjApi

Todas as URIs relativas a *https://prod.acbr.api.br*

Método | Endpoint | Descrição
------------- | ------------- | -------------
[**consultar_cnpj**](CnpjApi.md#consultar_cnpj) | **GET** /cnpj/{Cnpj} | Consultar dados do CNPJ
[**listar_cnpj**](CnpjApi.md#listar_cnpj) | **GET** /cnpj | Listar estabelecimentos ativos a partir da base de CNPJ


# **consultar_cnpj**
> CnpjEmpresa consultar_cnpj(cnpj)

Consultar dados do CNPJ

**Informações adicionais**:  - Consumo: 0,1 unidade por requisição.  - Em sandbox, a consulta é permitida somente para os seguintes CNPJ:    `18760540000139`    `00038166000105`    `00394460000141`    `29979036000140`

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
    api_instance = acbrapi_sdk.CnpjApi(api_client)
    cnpj = 'cnpj_example' # str | CNPJ sem máscara.

    try:
        # Consultar dados do CNPJ
        api_response = api_instance.consultar_cnpj(cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CnpjApi->consultar_cnpj: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cnpj** | **str**| CNPJ sem máscara. | 

### Tipo do retorno

[**CnpjEmpresa**](CnpjEmpresa.md)

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

# **listar_cnpj**
> CnpjListagem listar_cnpj(cnae_principal, municipio, natureza_juridica, top=top, skip=skip, inlinecount=inlinecount)

Listar estabelecimentos ativos a partir da base de CNPJ

Retorna uma lista de estabelecimentos de acordo com os critérios de busca utilizados.  Somente serão retornados estabelecimentos com situação cadastral \"Ativa\".    **Informações adicionais**:  - Consumo: 0,1 unidade por estabelecimento listado ou requisição.  - Em sandbox, a consulta de listagem de CNPJ não é permitida.

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
    api_instance = acbrapi_sdk.CnpjApi(api_client)
    cnae_principal = 'cnae_principal_example' # str | Filtro pelo código CNAE da atividade principal do estabelecimento.  Utilize o valor sem máscara.
municipio = 'municipio_example' # str | Filtro pelo código IBGE ou TOM (Tabela de Órgãos e Municípios) do município do estabelecimento.  Utilize o valor sem máscara.
natureza_juridica = 'natureza_juridica_example' # str | Filtro pela natureza jurídica do estabelecimento   Utilize o valor de quatro dígitos sem máscara.
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (opcional) (default 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (opcional) (default 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (opcional) (default False)

    try:
        # Listar estabelecimentos ativos a partir da base de CNPJ
        api_response = api_instance.listar_cnpj(cnae_principal, municipio, natureza_juridica, top=top, skip=skip, inlinecount=inlinecount)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar CnpjApi->listar_cnpj: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cnae_principal** | **str**| Filtro pelo código CNAE da atividade principal do estabelecimento.  Utilize o valor sem máscara. | 
 **municipio** | **str**| Filtro pelo código IBGE ou TOM (Tabela de Órgãos e Municípios) do município do estabelecimento.  Utilize o valor sem máscara. | 
 **natureza_juridica** | **str**| Filtro pela natureza jurídica do estabelecimento   Utilize o valor de quatro dígitos sem máscara. | 
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [opcional] [default 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [opcional] [default 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [opcional] [default False]

### Tipo do retorno

[**CnpjListagem**](CnpjListagem.md)

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

