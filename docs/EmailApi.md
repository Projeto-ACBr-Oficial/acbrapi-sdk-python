# acbrapi_sdk.EmailApi

Todas as URIs relativas a *https://prod.acbr.api.br*

Método | Endpoint | Descrição
------------- | ------------- | -------------
[**consultar_email**](EmailApi.md#consultar_email) | **GET** /emails/{id} | Consultar e-mail
[**listar_emails**](EmailApi.md#listar_emails) | **GET** /emails | Listar e-mails


# **consultar_email**
> Email consultar_email(id)

Consultar e-mail

Obtém informações detalhadas sobre o envio de um email. Este endpoint  permite rastrear todos os eventos relacionados ao email, como envio,  entrega, falhas e outros eventos relevantes.    Com este endpoint, é possível ter uma visão completa do ciclo de vida  de um email enviado, permitindo que os usuários acompanhem e analisem  o status e o histórico de eventos do email. Isso é particularmente  útil para identificar problemas de entrega e entender o comportamento  do email ao longo do tempo.

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
    api_instance = acbrapi_sdk.EmailApi(api_client)
    id = 'id_example' # str | ID único do e-mail.    Esse parâmetro é obtido após o envio do email por qualquer endpoint da  API que realize disparos de email.    Exemplos:  * <a href=\"#tag/Nfe/operation/EnviarEmailNfe\">Envio de XML e PDF de NF-e</a>.  * <a href=\"#tag/Nfce/operation/EnviarEmailNfce\">Envio de XML e PDF de NFC-e</a>.

    try:
        # Consultar e-mail
        api_response = api_instance.consultar_email(id)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmailApi->consultar_email: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID único do e-mail.    Esse parâmetro é obtido após o envio do email por qualquer endpoint da  API que realize disparos de email.    Exemplos:  * &lt;a href&#x3D;\&quot;#tag/Nfe/operation/EnviarEmailNfe\&quot;&gt;Envio de XML e PDF de NF-e&lt;/a&gt;.  * &lt;a href&#x3D;\&quot;#tag/Nfce/operation/EnviarEmailNfce\&quot;&gt;Envio de XML e PDF de NFC-e&lt;/a&gt;. | 

### Tipo do retorno

[**Email**](Email.md)

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

# **listar_emails**
> EmailListagem listar_emails(cpf_cnpj, top=top, skip=skip, inlinecount=inlinecount, undelivered=undelivered, email=email)

Listar e-mails

Retorna a lista dos emails associadas à sua conta. Os e-emails são  retornados ordenados pela data da criação, com os mais recentes  aparecendo primeiro.

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
    api_instance = acbrapi_sdk.EmailApi(api_client)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtra pelo CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*.
top = 10 # int | Limite no número de objetos a serem retornados pela API, entre 1 e 100. (opcional) (default 10)
skip = 0 # int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. (opcional) (default 0)
inlinecount = False # bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação. (opcional) (default False)
undelivered = True # bool | Filtra apenas emails com problemas de entrega. (opcional)
email = 'email_example' # str | Filtra pelo endereço de e-mail do destinatário para qual o email foi enviado. (opcional)

    try:
        # Listar e-mails
        api_response = api_instance.listar_emails(cpf_cnpj, top=top, skip=skip, inlinecount=inlinecount, undelivered=undelivered, email=email)
        pprint(api_response)
    except ApiException as e:
        print("Excecao ao chamar EmailApi->listar_emails: %s\n" % e)
```

### Parâmetros

Nome | Tipo | Descrição  | Comentários
------------- | ------------- | ------------- | -------------
 **cpf_cnpj** | **str**| Filtra pelo CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*. | 
 **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [opcional] [default 10]
 **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [opcional] [default 0]
 **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [opcional] [default False]
 **undelivered** | **bool**| Filtra apenas emails com problemas de entrega. | [opcional] 
 **email** | **str**| Filtra pelo endereço de e-mail do destinatário para qual o email foi enviado. | [opcional] 

### Tipo do retorno

[**EmailListagem**](EmailListagem.md)

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

