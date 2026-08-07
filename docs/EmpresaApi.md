# acbrapi_sdk.EmpresaApi

Todas as URIs relativas a *https://prod.acbr.api.br*

Método | Endpoint | Descrição
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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigCte() # EmpresaConfigCte | 

    try:
        # Alterar configuração de CT-e
        api_response = api_instance.alterar_config_cte(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->alterar_config_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigCte**](EmpresaConfigCte.md)|  | 

### Tipo do retorno

[**EmpresaConfigCte**](EmpresaConfigCte.md)

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

# **alterar_config_cte_os**
> EmpresaConfigCteOs alterar_config_cte_os(cpf_cnpj, body)

Alterar configuração de CT-e OS

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigCteOs() # EmpresaConfigCteOs | 

    try:
        # Alterar configuração de CT-e OS
        api_response = api_instance.alterar_config_cte_os(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->alterar_config_cte_os: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigCteOs**](EmpresaConfigCteOs.md)|  | 

### Tipo do retorno

[**EmpresaConfigCteOs**](EmpresaConfigCteOs.md)

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

# **alterar_config_dce**
> EmpresaConfigDce alterar_config_dce(cpf_cnpj, body)

Alterar configuração de DC-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigDce() # EmpresaConfigDce | 

    try:
        # Alterar configuração de DC-e
        api_response = api_instance.alterar_config_dce(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->alterar_config_dce: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigDce**](EmpresaConfigDce.md)|  | 

### Tipo do retorno

[**EmpresaConfigDce**](EmpresaConfigDce.md)

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

# **alterar_config_distribuicao_nfe**
> EmpresaConfigDistribuicaoNfe alterar_config_distribuicao_nfe(cpf_cnpj, body)

Alterar configuração de Distribuição de NF-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigDistribuicaoNfe() # EmpresaConfigDistribuicaoNfe | 

    try:
        # Alterar configuração de Distribuição de NF-e
        api_response = api_instance.alterar_config_distribuicao_nfe(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->alterar_config_distribuicao_nfe: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigDistribuicaoNfe**](EmpresaConfigDistribuicaoNfe.md)|  | 

### Tipo do retorno

[**EmpresaConfigDistribuicaoNfe**](EmpresaConfigDistribuicaoNfe.md)

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

# **alterar_config_mdfe**
> EmpresaConfigMdfe alterar_config_mdfe(cpf_cnpj, body)

Alterar configuração de MDF-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigMdfe() # EmpresaConfigMdfe | 

    try:
        # Alterar configuração de MDF-e
        api_response = api_instance.alterar_config_mdfe(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->alterar_config_mdfe: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigMdfe**](EmpresaConfigMdfe.md)|  | 

### Tipo do retorno

[**EmpresaConfigMdfe**](EmpresaConfigMdfe.md)

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

# **alterar_config_nfce**
> EmpresaConfigNfce alterar_config_nfce(cpf_cnpj, body)

Alterar configuração de NFC-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigNfce() # EmpresaConfigNfce | 

    try:
        # Alterar configuração de NFC-e
        api_response = api_instance.alterar_config_nfce(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->alterar_config_nfce: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigNfce**](EmpresaConfigNfce.md)|  | 

### Tipo do retorno

[**EmpresaConfigNfce**](EmpresaConfigNfce.md)

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

# **alterar_config_nfcom**
> EmpresaConfigNfcom alterar_config_nfcom(cpf_cnpj, body)

Alterar configuração de NFCom

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigNfcom() # EmpresaConfigNfcom | 

    try:
        # Alterar configuração de NFCom
        api_response = api_instance.alterar_config_nfcom(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->alterar_config_nfcom: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigNfcom**](EmpresaConfigNfcom.md)|  | 

### Tipo do retorno

[**EmpresaConfigNfcom**](EmpresaConfigNfcom.md)

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

# **alterar_config_nfe**
> EmpresaConfigNfe alterar_config_nfe(cpf_cnpj, body)

Alterar configuração de NF-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigNfe() # EmpresaConfigNfe | 

    try:
        # Alterar configuração de NF-e
        api_response = api_instance.alterar_config_nfe(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->alterar_config_nfe: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigNfe**](EmpresaConfigNfe.md)|  | 

### Tipo do retorno

[**EmpresaConfigNfe**](EmpresaConfigNfe.md)

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

# **alterar_config_nfse**
> EmpresaConfigNfse alterar_config_nfse(cpf_cnpj, body)

Alterar configuração de NFS-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaConfigNfse() # EmpresaConfigNfse | 

    try:
        # Alterar configuração de NFS-e
        api_response = api_instance.alterar_config_nfse(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->alterar_config_nfse: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaConfigNfse**](EmpresaConfigNfse.md)|  | 

### Tipo do retorno

[**EmpresaConfigNfse**](EmpresaConfigNfse.md)

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

# **atualizar_empresa**
> Empresa atualizar_empresa(cpf_cnpj, body)

Alterar empresa

Altera o cadastro de uma empresa (emitente/prestador) que esteja associada a sua conta.  Nesse método, por tratar-se de um PUT, caso algum campo não seja informado, o valor dele será apagado.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.Empresa() # Empresa | 

    try:
        # Alterar empresa
        api_response = api_instance.atualizar_empresa(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->atualizar_empresa: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**Empresa**](Empresa.md)|  | 

### Tipo do retorno

[**Empresa**](Empresa.md)

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

# **baixar_logotipo_empresa**
> file baixar_logotipo_empresa(cpf_cnpj)

Baixar logotipo

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Baixar logotipo
        api_response = api_instance.baixar_logotipo_empresa(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->baixar_logotipo_empresa: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

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

# **cadastrar_certificado_empresa**
> EmpresaCertificado cadastrar_certificado_empresa(cpf_cnpj, body)

Cadastrar certificado

Cadastre ou atualize um certificado digital e vincule a sua empresa, para que possa iniciar a emissão de notas.  * No parâmetro `certificado`, envie o binário do certificado digital (.pfx ou .p12) codificado em **base64**.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
body = acbrapi_sdk.EmpresaPedidoCadastroCertificado() # EmpresaPedidoCadastroCertificado | 

    try:
        # Cadastrar certificado
        api_response = api_instance.cadastrar_certificado_empresa(cpf_cnpj, body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->cadastrar_certificado_empresa: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **body** | [**EmpresaPedidoCadastroCertificado**](EmpresaPedidoCadastroCertificado.md)|  | 

### Tipo do retorno

[**EmpresaCertificado**](EmpresaCertificado.md)

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

# **consultar_certificado_empresa**
> EmpresaCertificado consultar_certificado_empresa(cpf_cnpj)

Consultar certificado

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar certificado
        api_response = api_instance.consultar_certificado_empresa(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->consultar_certificado_empresa: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

[**EmpresaCertificado**](EmpresaCertificado.md)

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

# **consultar_config_cte**
> EmpresaConfigCte consultar_config_cte(cpf_cnpj)

Consultar configuração de CT-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de CT-e
        api_response = api_instance.consultar_config_cte(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->consultar_config_cte: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

[**EmpresaConfigCte**](EmpresaConfigCte.md)

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

# **consultar_config_cte_os**
> EmpresaConfigCteOs consultar_config_cte_os(cpf_cnpj)

Consultar configuração de CT-e OS

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de CT-e OS
        api_response = api_instance.consultar_config_cte_os(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->consultar_config_cte_os: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

[**EmpresaConfigCteOs**](EmpresaConfigCteOs.md)

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

# **consultar_config_dce**
> EmpresaConfigDce consultar_config_dce(cpf_cnpj)

Consultar configuração de DC-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de DC-e
        api_response = api_instance.consultar_config_dce(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->consultar_config_dce: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

[**EmpresaConfigDce**](EmpresaConfigDce.md)

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

# **consultar_config_distribuicao_nfe**
> EmpresaConfigDistribuicaoNfe consultar_config_distribuicao_nfe(cpf_cnpj)

Consultar configuração de Distribuição de NF-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de Distribuição de NF-e
        api_response = api_instance.consultar_config_distribuicao_nfe(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->consultar_config_distribuicao_nfe: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

[**EmpresaConfigDistribuicaoNfe**](EmpresaConfigDistribuicaoNfe.md)

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

# **consultar_config_mdfe**
> EmpresaConfigMdfe consultar_config_mdfe(cpf_cnpj)

Consultar configuração de MDF-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de MDF-e
        api_response = api_instance.consultar_config_mdfe(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->consultar_config_mdfe: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

[**EmpresaConfigMdfe**](EmpresaConfigMdfe.md)

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

# **consultar_config_nfce**
> EmpresaConfigNfce consultar_config_nfce(cpf_cnpj)

Consultar configuração de NFC-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de NFC-e
        api_response = api_instance.consultar_config_nfce(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->consultar_config_nfce: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

[**EmpresaConfigNfce**](EmpresaConfigNfce.md)

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

# **consultar_config_nfcom**
> EmpresaConfigNfcom consultar_config_nfcom(cpf_cnpj)

Consultar configuração de NFCom

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de NFCom
        api_response = api_instance.consultar_config_nfcom(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->consultar_config_nfcom: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

[**EmpresaConfigNfcom**](EmpresaConfigNfcom.md)

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

# **consultar_config_nfe**
> EmpresaConfigNfe consultar_config_nfe(cpf_cnpj)

Consultar configuração de NF-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de NF-e
        api_response = api_instance.consultar_config_nfe(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->consultar_config_nfe: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

[**EmpresaConfigNfe**](EmpresaConfigNfe.md)

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

# **consultar_config_nfse**
> EmpresaConfigNfse consultar_config_nfse(cpf_cnpj)

Consultar configuração de NFS-e

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar configuração de NFS-e
        api_response = api_instance.consultar_config_nfse(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->consultar_config_nfse: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

[**EmpresaConfigNfse**](EmpresaConfigNfse.md)

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

# **consultar_empresa**
> Empresa consultar_empresa(cpf_cnpj)

Consultar empresa

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Consultar empresa
        api_response = api_instance.consultar_empresa(cpf_cnpj)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->consultar_empresa: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

[**Empresa**](Empresa.md)

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

# **criar_empresa**
> Empresa criar_empresa(body)

Cadastrar empresa

Cadastre uma nova empresa (emitente ou prestador) à sua conta.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    body = acbrapi_sdk.Empresa() # Empresa | 

    try:
        # Cadastrar empresa
        api_response = api_instance.criar_empresa(body)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->criar_empresa: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **body** | [**Empresa**](Empresa.md)|  | 

### Tipo do retorno

[**Empresa**](Empresa.md)

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

# **enviar_certificado_empresa**
> EmpresaCertificado enviar_certificado_empresa(cpf_cnpj, input=input)

Upload de certificado

Cadastre ou atualize um certificado digital e vincule a sua empresa, para que possa iniciar a emissão de notas.  * Utilize o `content-type` igual a `multipart/form-data`.  * No parâmetro `file`, envie o binário do arquivo (.pfx ou .p12) do certificado digital.  * No parâmetro `password`, envie a senha do certificado.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
input = '/path/to/file' # file |  (opcional)

    try:
        # Upload de certificado
        api_response = api_instance.enviar_certificado_empresa(cpf_cnpj, input=input)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->enviar_certificado_empresa: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **input** | **file**|  | [opcional] 

### Tipo do retorno

[**EmpresaCertificado**](EmpresaCertificado.md)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **enviar_logotipo_empresa**
> enviar_logotipo_empresa(cpf_cnpj, input=input)

Enviar logotipo

Cadastre ou atualize um logotipo e vincule a sua empresa.    **Restrições:**  * Tipos de mídia (MIME) suportados: `image/png` e `image/jpeg`  * Tamanho máximo do arquivo: 200 KB    **Cenários de uso:**  * Quero que minhas notas sejam impressas com esse logotipo.  * Quero trocar o logotipo utilizado em minhas impressões.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
input = '/path/to/file' # file |  (opcional)

    try:
        # Enviar logotipo
        api_instance.enviar_logotipo_empresa(cpf_cnpj, input=input)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->enviar_logotipo_empresa: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 
 **input** | **file**|  | [opcional] 

### Tipo do retorno

void (corpo de resposta vazio)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: multipart/form-data
 - **Accept**: Não definido

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**204** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **excluir_certificado_empresa**
> excluir_certificado_empresa(cpf_cnpj)

Deletar certificado

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Deletar certificado
        api_instance.excluir_certificado_empresa(cpf_cnpj)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->excluir_certificado_empresa: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

void (corpo de resposta vazio)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: Não definido

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**204** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **excluir_empresa**
> excluir_empresa(cpf_cnpj)

Deletar empresa

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Deletar empresa
        api_instance.excluir_empresa(cpf_cnpj)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->excluir_empresa: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

void (corpo de resposta vazio)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: Não definido

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**204** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **excluir_logotipo_empresa**
> excluir_logotipo_empresa(cpf_cnpj)

Deletar logotipo

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

    try:
        # Deletar logotipo
        api_instance.excluir_logotipo_empresa(cpf_cnpj)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->excluir_logotipo_empresa: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | 

### Tipo do retorno

void (corpo de resposta vazio)

### Autorização

[oauth2](../README.md#oauth2)

### Headers HTTP da requisição

 - **Content-Type**: Não definido
 - **Accept**: Não definido

### Respostas HTTP
| Código | Descrição | Headers da resposta |
|-------------|-------------|------------------|
**204** | Successful response |  -  |

[[Voltar ao topo]](#) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar ao README]](../README.md)

# **listar_certificados**
> EmpresaCertificadoListagem listar_certificados(top=top, skip=skip, inlinecount=inlinecount, expires_in=expires_in, include_expired=include_expired)

Listar certificados

Retorna a lista dos certificados associadas à sua conta. Os certificados são retornados ordenados pela data da criação, com as mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (opcional) (default 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (opcional) (default 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (opcional) (default False)
expires_in = 56 # int | Filtrar certificados que expiram dentro de X dias.    Informe um número inteiro correspondente à quantidade de dias até o vencimento.  Exemplos:   - expires_in=30 -&gt; certificados que vencem nos próximos 30 dias.   - expires_in=7  -&gt; certificados que vencem nos próximos 7 dias. (opcional)
include_expired = True # bool | Indicar se os certificados já vencidos devem ser incluídos no resultado.    Valores aceitos:   - `true`: incluir certificados vencidos.   - `false`: exibir apenas certificados válidos. (opcional) (default True)

    try:
        # Listar certificados
        api_response = api_instance.listar_certificados(top=top, skip=skip, inlinecount=inlinecount, expires_in=expires_in, include_expired=include_expired)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->listar_certificados: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [opcional] [default 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [opcional] [default 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [opcional] [default False]
 **expires_in** | **int**| Filtrar certificados que expiram dentro de X dias.    Informe um número inteiro correspondente à quantidade de dias até o vencimento.  Exemplos:   - expires_in&#x3D;30 -&amp;gt; certificados que vencem nos próximos 30 dias.   - expires_in&#x3D;7  -&amp;gt; certificados que vencem nos próximos 7 dias. | [opcional] 
 **include_expired** | **bool**| Indicar se os certificados já vencidos devem ser incluídos no resultado.    Valores aceitos:   - &#x60;true&#x60;: incluir certificados vencidos.   - &#x60;false&#x60;: exibir apenas certificados válidos. | [opcional] [default True]

### Tipo do retorno

[**EmpresaCertificadoListagem**](EmpresaCertificadoListagem.md)

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

# **listar_empresas**
> EmpresaListagem listar_empresas(top=top, skip=skip, inlinecount=inlinecount, cpf_cnpj=cpf_cnpj, nome_razao_social=nome_razao_social)

Listar empresas

Retorna a lista das empresas associadas à sua conta. As empresas são retornadas ordenadas pela data da criação, com as mais recentes aparecendo primeiro.

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
    api_instance = acbrapi_sdk.EmpresaApi(api_client)
    top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (opcional) (default 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (opcional) (default 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (opcional) (default False)
cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*. (opcional)
nome_razao_social = 'nome_razao_social_example' # str | Filtrar pelo nome ou razão social da empresa.    Esse filtro realiza uma correspondência pelo início do texto,  retornando apenas empresas cujo nome ou razão social começam com  o valor informado.    *Caso o filtro pelo CPF ou CNPJ também seja informado na requisição,  este filtro é ignorado*. (opcional)

    try:
        # Listar empresas
        api_response = api_instance.listar_empresas(top=top, skip=skip, inlinecount=inlinecount, cpf_cnpj=cpf_cnpj, nome_razao_social=nome_razao_social)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmpresaApi->listar_empresas: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [opcional] [default 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [opcional] [default 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [opcional] [default False]
 **cpf_cnpj** | **str**| Filtrar pelo CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*. | [opcional] 
 **nome_razao_social** | **str**| Filtrar pelo nome ou razão social da empresa.    Esse filtro realiza uma correspondência pelo início do texto,  retornando apenas empresas cujo nome ou razão social começam com  o valor informado.    *Caso o filtro pelo CPF ou CNPJ também seja informado na requisição,  este filtro é ignorado*. | [opcional] 

### Tipo do retorno

[**EmpresaListagem**](EmpresaListagem.md)

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

