# ACBr API: SDK para Python

Biblioteca para uso da [ACBr API](https://www.acbr.api.br) com [Python](https://www.python.org).
Consultar também a [documentação oficial da ACBr API](https://dev.acbr.api.br/docs).

## Requisitos

Python 2.7 e 3.4+

## Instalação

Escolha **uma** das formas abaixo para adicionar o SDK ao seu projeto.

### 1. Via pip direto do GitHub — recomendado

Instala o pacote diretamente do repositório. Rode dentro do ambiente (venv)
do seu projeto:

```sh
pip install "git+https://github.com/projeto-acbr-oficial/acbrapi-sdk-python.git"
```

Fixando a branch `main` (ou troque por uma tag/commit quando disponível):

```sh
pip install "git+https://github.com/projeto-acbr-oficial/acbrapi-sdk-python.git@main"
```

No `requirements.txt` do seu projeto:

```
acbrapi-sdk @ git+https://github.com/projeto-acbr-oficial/acbrapi-sdk-python.git@main
```

(em alguns ambientes o `pip` precisa de permissão de root: use `sudo pip install ...`)

### 2. A partir do código-fonte (setuptools)

Clone o repositório e instale via [Setuptools](http://pypi.python.org/pypi/setuptools):

```sh
python setup.py install --user
```
(ou `sudo python setup.py install` para instalar para todos os usuários)

### Importando o pacote

Depois de instalar por qualquer um dos métodos acima:

```python
import acbrapi_sdk
```

## Primeiros passos

Depois de instalar o pacote (veja a seção **Instalação** acima), rode:

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

## Documentação dos endpoints da API

Todas as URIs são relativas a *https://prod.acbr.api.br*

Classe | Método | Requisição HTTP | Descrição
------------ | ------------- | ------------- | -------------
*CepApi* | [**consultar_cep**](docs/CepApi.md#consultar_cep) | **GET** /cep/{Cep} | Consultar endereço através do CEP
*CnpjApi* | [**consultar_cnpj**](docs/CnpjApi.md#consultar_cnpj) | **GET** /cnpj/{Cnpj} | Consultar dados do CNPJ
*CnpjApi* | [**listar_cnpj**](docs/CnpjApi.md#listar_cnpj) | **GET** /cnpj | Listar estabelecimentos ativos a partir da base de CNPJ
*ContaApi* | [**consultar_cota_conta**](docs/ContaApi.md#consultar_cota_conta) | **GET** /conta/cotas/{nome} | Consultar o limite de uso e o consumo de uma cota específica.
*ContaApi* | [**consultar_cota_pre_pago**](docs/ContaApi.md#consultar_cota_pre_pago) | **GET** /conta/cotas/prepago | Consultar o resumo da cota de créditos pré-pagos.
*ContaApi* | [**listar_cotas_conta**](docs/ContaApi.md#listar_cotas_conta) | **GET** /conta/cotas | Consultar os limites de uso e consumo das cotas disponíveis, exceto a cota de créditos pré-pagos.
*ContaApi* | [**listar_extrato_creditos_conta**](docs/ContaApi.md#listar_extrato_creditos_conta) | **GET** /conta/extrato | Consultar o extrato de movimentação de créditos do tenant atual.
*CteApi* | [**baixar_pdf_cancelamento_cte**](docs/CteApi.md#baixar_pdf_cancelamento_cte) | **GET** /cte/{id}/cancelamento/pdf | Baixar PDF do cancelamento
*CteApi* | [**baixar_pdf_carta_correcao_cte**](docs/CteApi.md#baixar_pdf_carta_correcao_cte) | **GET** /cte/{id}/carta-correcao/pdf | Baixar PDF da carta de correção
*CteApi* | [**baixar_pdf_cte**](docs/CteApi.md#baixar_pdf_cte) | **GET** /cte/{id}/pdf | Baixar PDF do DACTE
*CteApi* | [**baixar_pdf_evento_cte**](docs/CteApi.md#baixar_pdf_evento_cte) | **GET** /cte/eventos/{id}/pdf | Baixar PDF do evento
*CteApi* | [**baixar_xml_cancelamento_cte**](docs/CteApi.md#baixar_xml_cancelamento_cte) | **GET** /cte/{id}/cancelamento/xml | Baixar XML do cancelamento
*CteApi* | [**baixar_xml_carta_correcao_cte**](docs/CteApi.md#baixar_xml_carta_correcao_cte) | **GET** /cte/{id}/carta-correcao/xml | Baixar XML da carta de correção
*CteApi* | [**baixar_xml_cte**](docs/CteApi.md#baixar_xml_cte) | **GET** /cte/{id}/xml | Baixar XML do CT-e processado
*CteApi* | [**baixar_xml_cte_conhecimento**](docs/CteApi.md#baixar_xml_cte_conhecimento) | **GET** /cte/{id}/xml/conhecimento | Baixar XML do CT-e
*CteApi* | [**baixar_xml_cte_protocolo**](docs/CteApi.md#baixar_xml_cte_protocolo) | **GET** /cte/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
*CteApi* | [**baixar_xml_evento_cte**](docs/CteApi.md#baixar_xml_evento_cte) | **GET** /cte/eventos/{id}/xml | Baixar XML do evento
*CteApi* | [**cancelar_cte**](docs/CteApi.md#cancelar_cte) | **POST** /cte/{id}/cancelamento | Cancelar um CT-e autorizado
*CteApi* | [**consultar_cancelamento_cte**](docs/CteApi.md#consultar_cancelamento_cte) | **GET** /cte/{id}/cancelamento | Consultar o cancelamento do CT-e
*CteApi* | [**consultar_carta_correcao_cte**](docs/CteApi.md#consultar_carta_correcao_cte) | **GET** /cte/{id}/carta-correcao | Consultar a solicitação de correção do CT-e
*CteApi* | [**consultar_cte**](docs/CteApi.md#consultar_cte) | **GET** /cte/{id} | Consultar CT-e
*CteApi* | [**consultar_evento_cte**](docs/CteApi.md#consultar_evento_cte) | **GET** /cte/eventos/{id} | Consultar evento
*CteApi* | [**consultar_status_sefaz_cte**](docs/CteApi.md#consultar_status_sefaz_cte) | **GET** /cte/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
*CteApi* | [**criar_carta_correcao_cte**](docs/CteApi.md#criar_carta_correcao_cte) | **POST** /cte/{id}/carta-correcao | Solicitar correção do CT-e
*CteApi* | [**emitir_cte**](docs/CteApi.md#emitir_cte) | **POST** /cte | Emitir CT-e
*CteApi* | [**emitir_cte_simp**](docs/CteApi.md#emitir_cte_simp) | **POST** /cte/simp | Emitir CT-e Simplificado
*CteApi* | [**listar_cte**](docs/CteApi.md#listar_cte) | **GET** /cte | Listar CT-e
*CteApi* | [**sincronizar_cte**](docs/CteApi.md#sincronizar_cte) | **POST** /cte/{id}/sincronizar | Sincroniza dados no CT-e a partir da SEFAZ
*CteOsApi* | [**baixar_pdf_cancelamento_cte_os**](docs/CteOsApi.md#baixar_pdf_cancelamento_cte_os) | **GET** /cteos/{id}/cancelamento/pdf | Baixar PDF do cancelamento
*CteOsApi* | [**baixar_pdf_carta_correcao_cte_os**](docs/CteOsApi.md#baixar_pdf_carta_correcao_cte_os) | **GET** /cteos/{id}/carta-correcao/pdf | Baixar PDF da carta de correção
*CteOsApi* | [**baixar_pdf_cte_os**](docs/CteOsApi.md#baixar_pdf_cte_os) | **GET** /cteos/{id}/pdf | Baixar PDF do DACTE
*CteOsApi* | [**baixar_pdf_evento_cte_os**](docs/CteOsApi.md#baixar_pdf_evento_cte_os) | **GET** /cteos/eventos/{id}/pdf | Baixar PDF do evento
*CteOsApi* | [**baixar_xml_cancelamento_cte_os**](docs/CteOsApi.md#baixar_xml_cancelamento_cte_os) | **GET** /cteos/{id}/cancelamento/xml | Baixar XML do cancelamento
*CteOsApi* | [**baixar_xml_carta_correcao_cte_os**](docs/CteOsApi.md#baixar_xml_carta_correcao_cte_os) | **GET** /cteos/{id}/carta-correcao/xml | Baixar XML da carta de correção
*CteOsApi* | [**baixar_xml_cte_os**](docs/CteOsApi.md#baixar_xml_cte_os) | **GET** /cteos/{id}/xml | Baixar XML do CT-e OS processado
*CteOsApi* | [**baixar_xml_cte_os_conhecimento**](docs/CteOsApi.md#baixar_xml_cte_os_conhecimento) | **GET** /cteos/{id}/xml/conhecimento | Baixar XML do CT-e OS
*CteOsApi* | [**baixar_xml_cte_os_protocolo**](docs/CteOsApi.md#baixar_xml_cte_os_protocolo) | **GET** /cteos/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
*CteOsApi* | [**baixar_xml_evento_cte_os**](docs/CteOsApi.md#baixar_xml_evento_cte_os) | **GET** /cteos/eventos/{id}/xml | Baixar XML do evento
*CteOsApi* | [**cancelar_cte_os**](docs/CteOsApi.md#cancelar_cte_os) | **POST** /cteos/{id}/cancelamento | Cancelar um CT-e OS autorizado
*CteOsApi* | [**consultar_cancelamento_cte_os**](docs/CteOsApi.md#consultar_cancelamento_cte_os) | **GET** /cteos/{id}/cancelamento | Consultar o cancelamento do CT-e OS
*CteOsApi* | [**consultar_carta_correcao_cte_os**](docs/CteOsApi.md#consultar_carta_correcao_cte_os) | **GET** /cteos/{id}/carta-correcao | Consultar a solicitação de correção do CT-e OS
*CteOsApi* | [**consultar_cte_os**](docs/CteOsApi.md#consultar_cte_os) | **GET** /cteos/{id} | Consultar CT-e OS
*CteOsApi* | [**consultar_evento_cte_os**](docs/CteOsApi.md#consultar_evento_cte_os) | **GET** /cteos/eventos/{id} | Consultar evento
*CteOsApi* | [**consultar_status_sefaz_cte_os**](docs/CteOsApi.md#consultar_status_sefaz_cte_os) | **GET** /cteos/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
*CteOsApi* | [**criar_carta_correcao_cte_os**](docs/CteOsApi.md#criar_carta_correcao_cte_os) | **POST** /cteos/{id}/carta-correcao | Solicitar correção do CT-e OS
*CteOsApi* | [**emitir_cte_os**](docs/CteOsApi.md#emitir_cte_os) | **POST** /cteos | Emitir CT-e OS
*CteOsApi* | [**listar_cte_os**](docs/CteOsApi.md#listar_cte_os) | **GET** /cteos | Listar CT-e OS
*CteOsApi* | [**sincronizar_cte_os**](docs/CteOsApi.md#sincronizar_cte_os) | **POST** /cteos/{id}/sincronizar | Sincroniza dados no CT-e OS a partir da SEFAZ
*DceApi* | [**baixar_pdf_dce**](docs/DceApi.md#baixar_pdf_dce) | **GET** /dce/{id}/pdf | Baixar PDF do DACE
*DceApi* | [**baixar_xml_cancelamento_dce**](docs/DceApi.md#baixar_xml_cancelamento_dce) | **GET** /dce/{id}/cancelamento/xml | Baixar XML do cancelamento
*DceApi* | [**baixar_xml_dce**](docs/DceApi.md#baixar_xml_dce) | **GET** /dce/{id}/xml | Baixar XML da DC-e processada
*DceApi* | [**baixar_xml_dce_declaracao**](docs/DceApi.md#baixar_xml_dce_declaracao) | **GET** /dce/{id}/xml/declaracao | Baixar XML da DC-e
*DceApi* | [**baixar_xml_dce_protocolo**](docs/DceApi.md#baixar_xml_dce_protocolo) | **GET** /dce/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
*DceApi* | [**cancelar_dce**](docs/DceApi.md#cancelar_dce) | **POST** /dce/{id}/cancelamento | Cancelar uma DC-e autorizada
*DceApi* | [**consultar_cancelamento_dce**](docs/DceApi.md#consultar_cancelamento_dce) | **GET** /dce/{id}/cancelamento | Consultar o cancelamento da DC-e
*DceApi* | [**consultar_dce**](docs/DceApi.md#consultar_dce) | **GET** /dce/{id} | Consultar DC-e
*DceApi* | [**consultar_status_sefaz_dce**](docs/DceApi.md#consultar_status_sefaz_dce) | **GET** /dce/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
*DceApi* | [**emitir_dce**](docs/DceApi.md#emitir_dce) | **POST** /dce | Emitir DC-e
*DceApi* | [**listar_dce**](docs/DceApi.md#listar_dce) | **GET** /dce | Listar DC-e
*DebugApi* | [**debug_dfe**](docs/DebugApi.md#debug_dfe) | **GET** /debug/{id} | Debug de DF-e
*DebugApi* | [**debug_dfe_original_payload**](docs/DebugApi.md#debug_dfe_original_payload) | **GET** /debug/{id}/original-payload | Payload original recebido
*DebugApi* | [**debug_http_request_content**](docs/DebugApi.md#debug_http_request_content) | **GET** /debug/http-requests/{id}/request-content | Corpo da requisição HTTP
*DebugApi* | [**debug_http_response_content**](docs/DebugApi.md#debug_http_response_content) | **GET** /debug/http-requests/{id}/response-content | Corpo da resposta HTTP
*DistribuioNFEApi* | [**baixar_pdf_documento_distribuicao_nfe**](docs/DistribuioNFEApi.md#baixar_pdf_documento_distribuicao_nfe) | **GET** /distribuicao/nfe/documentos/{id}/pdf | Baixar PDF do documento
*DistribuioNFEApi* | [**baixar_xml_documento_distribuicao_nfe**](docs/DistribuioNFEApi.md#baixar_xml_documento_distribuicao_nfe) | **GET** /distribuicao/nfe/documentos/{id}/xml | Baixar XML do documento
*DistribuioNFEApi* | [**consultar_distribuicao_nfe**](docs/DistribuioNFEApi.md#consultar_distribuicao_nfe) | **GET** /distribuicao/nfe/{id} | Consultar distribuição
*DistribuioNFEApi* | [**consultar_documento_distribuicao_nfe**](docs/DistribuioNFEApi.md#consultar_documento_distribuicao_nfe) | **GET** /distribuicao/nfe/documentos/{id} | Consultar documento
*DistribuioNFEApi* | [**consultar_manifestacao_nfe**](docs/DistribuioNFEApi.md#consultar_manifestacao_nfe) | **GET** /distribuicao/nfe/manifestacoes/{id} | Consultar manifestação
*DistribuioNFEApi* | [**gerar_distribuicao_nfe**](docs/DistribuioNFEApi.md#gerar_distribuicao_nfe) | **POST** /distribuicao/nfe | Distribuir documentos
*DistribuioNFEApi* | [**listar_distribuicao_nfe**](docs/DistribuioNFEApi.md#listar_distribuicao_nfe) | **GET** /distribuicao/nfe | Listar distribuições
*DistribuioNFEApi* | [**listar_documento_distribuicao_nfe**](docs/DistribuioNFEApi.md#listar_documento_distribuicao_nfe) | **GET** /distribuicao/nfe/documentos | Listar documentos
*DistribuioNFEApi* | [**listar_manifestacao_nfe**](docs/DistribuioNFEApi.md#listar_manifestacao_nfe) | **GET** /distribuicao/nfe/manifestacoes | Listar Manifestações
*DistribuioNFEApi* | [**listar_nfe_sem_manifestacao**](docs/DistribuioNFEApi.md#listar_nfe_sem_manifestacao) | **GET** /distribuicao/nfe/notas-sem-manifestacao | Listar notas sem manifestação
*DistribuioNFEApi* | [**manifestar_nfe**](docs/DistribuioNFEApi.md#manifestar_nfe) | **POST** /distribuicao/nfe/manifestacoes | Manifestar nota
*EmailApi* | [**consultar_email**](docs/EmailApi.md#consultar_email) | **GET** /emails/{id} | Consultar e-mail
*EmailApi* | [**listar_emails**](docs/EmailApi.md#listar_emails) | **GET** /emails | Listar e-mails
*EmpresaApi* | [**alterar_config_cte**](docs/EmpresaApi.md#alterar_config_cte) | **PUT** /empresas/{cpf_cnpj}/cte | Alterar configuração de CT-e
*EmpresaApi* | [**alterar_config_cte_os**](docs/EmpresaApi.md#alterar_config_cte_os) | **PUT** /empresas/{cpf_cnpj}/cteos | Alterar configuração de CT-e OS
*EmpresaApi* | [**alterar_config_dce**](docs/EmpresaApi.md#alterar_config_dce) | **PUT** /empresas/{cpf_cnpj}/dce | Alterar configuração de DC-e
*EmpresaApi* | [**alterar_config_distribuicao_nfe**](docs/EmpresaApi.md#alterar_config_distribuicao_nfe) | **PUT** /empresas/{cpf_cnpj}/distnfe | Alterar configuração de Distribuição de NF-e
*EmpresaApi* | [**alterar_config_mdfe**](docs/EmpresaApi.md#alterar_config_mdfe) | **PUT** /empresas/{cpf_cnpj}/mdfe | Alterar configuração de MDF-e
*EmpresaApi* | [**alterar_config_nfce**](docs/EmpresaApi.md#alterar_config_nfce) | **PUT** /empresas/{cpf_cnpj}/nfce | Alterar configuração de NFC-e
*EmpresaApi* | [**alterar_config_nfcom**](docs/EmpresaApi.md#alterar_config_nfcom) | **PUT** /empresas/{cpf_cnpj}/nfcom | Alterar configuração de NFCom
*EmpresaApi* | [**alterar_config_nfe**](docs/EmpresaApi.md#alterar_config_nfe) | **PUT** /empresas/{cpf_cnpj}/nfe | Alterar configuração de NF-e
*EmpresaApi* | [**alterar_config_nfse**](docs/EmpresaApi.md#alterar_config_nfse) | **PUT** /empresas/{cpf_cnpj}/nfse | Alterar configuração de NFS-e
*EmpresaApi* | [**atualizar_empresa**](docs/EmpresaApi.md#atualizar_empresa) | **PUT** /empresas/{cpf_cnpj} | Alterar empresa
*EmpresaApi* | [**baixar_logotipo_empresa**](docs/EmpresaApi.md#baixar_logotipo_empresa) | **GET** /empresas/{cpf_cnpj}/logotipo | Baixar logotipo
*EmpresaApi* | [**cadastrar_certificado_empresa**](docs/EmpresaApi.md#cadastrar_certificado_empresa) | **PUT** /empresas/{cpf_cnpj}/certificado | Cadastrar certificado
*EmpresaApi* | [**consultar_certificado_empresa**](docs/EmpresaApi.md#consultar_certificado_empresa) | **GET** /empresas/{cpf_cnpj}/certificado | Consultar certificado
*EmpresaApi* | [**consultar_config_cte**](docs/EmpresaApi.md#consultar_config_cte) | **GET** /empresas/{cpf_cnpj}/cte | Consultar configuração de CT-e
*EmpresaApi* | [**consultar_config_cte_os**](docs/EmpresaApi.md#consultar_config_cte_os) | **GET** /empresas/{cpf_cnpj}/cteos | Consultar configuração de CT-e OS
*EmpresaApi* | [**consultar_config_dce**](docs/EmpresaApi.md#consultar_config_dce) | **GET** /empresas/{cpf_cnpj}/dce | Consultar configuração de DC-e
*EmpresaApi* | [**consultar_config_distribuicao_nfe**](docs/EmpresaApi.md#consultar_config_distribuicao_nfe) | **GET** /empresas/{cpf_cnpj}/distnfe | Consultar configuração de Distribuição de NF-e
*EmpresaApi* | [**consultar_config_mdfe**](docs/EmpresaApi.md#consultar_config_mdfe) | **GET** /empresas/{cpf_cnpj}/mdfe | Consultar configuração de MDF-e
*EmpresaApi* | [**consultar_config_nfce**](docs/EmpresaApi.md#consultar_config_nfce) | **GET** /empresas/{cpf_cnpj}/nfce | Consultar configuração de NFC-e
*EmpresaApi* | [**consultar_config_nfcom**](docs/EmpresaApi.md#consultar_config_nfcom) | **GET** /empresas/{cpf_cnpj}/nfcom | Consultar configuração de NFCom
*EmpresaApi* | [**consultar_config_nfe**](docs/EmpresaApi.md#consultar_config_nfe) | **GET** /empresas/{cpf_cnpj}/nfe | Consultar configuração de NF-e
*EmpresaApi* | [**consultar_config_nfse**](docs/EmpresaApi.md#consultar_config_nfse) | **GET** /empresas/{cpf_cnpj}/nfse | Consultar configuração de NFS-e
*EmpresaApi* | [**consultar_empresa**](docs/EmpresaApi.md#consultar_empresa) | **GET** /empresas/{cpf_cnpj} | Consultar empresa
*EmpresaApi* | [**criar_empresa**](docs/EmpresaApi.md#criar_empresa) | **POST** /empresas | Cadastrar empresa
*EmpresaApi* | [**enviar_certificado_empresa**](docs/EmpresaApi.md#enviar_certificado_empresa) | **PUT** /empresas/{cpf_cnpj}/certificado/upload | Upload de certificado
*EmpresaApi* | [**enviar_logotipo_empresa**](docs/EmpresaApi.md#enviar_logotipo_empresa) | **PUT** /empresas/{cpf_cnpj}/logotipo | Enviar logotipo
*EmpresaApi* | [**excluir_certificado_empresa**](docs/EmpresaApi.md#excluir_certificado_empresa) | **DELETE** /empresas/{cpf_cnpj}/certificado | Deletar certificado
*EmpresaApi* | [**excluir_empresa**](docs/EmpresaApi.md#excluir_empresa) | **DELETE** /empresas/{cpf_cnpj} | Deletar empresa
*EmpresaApi* | [**excluir_logotipo_empresa**](docs/EmpresaApi.md#excluir_logotipo_empresa) | **DELETE** /empresas/{cpf_cnpj}/logotipo | Deletar logotipo
*EmpresaApi* | [**listar_certificados**](docs/EmpresaApi.md#listar_certificados) | **GET** /empresas/certificados | Listar certificados
*EmpresaApi* | [**listar_empresas**](docs/EmpresaApi.md#listar_empresas) | **GET** /empresas | Listar empresas
*MdfeApi* | [**baixar_pdf_cancelamento_mdfe**](docs/MdfeApi.md#baixar_pdf_cancelamento_mdfe) | **GET** /mdfe/{id}/cancelamento/pdf | Baixar PDF do cancelamento
*MdfeApi* | [**baixar_pdf_encerramento_mdfe**](docs/MdfeApi.md#baixar_pdf_encerramento_mdfe) | **GET** /mdfe/{id}/encerramento/pdf | Baixar PDF do encerramento
*MdfeApi* | [**baixar_pdf_evento_mdfe**](docs/MdfeApi.md#baixar_pdf_evento_mdfe) | **GET** /mdfe/eventos/{id}/pdf | Baixar PDF do evento
*MdfeApi* | [**baixar_pdf_mdfe**](docs/MdfeApi.md#baixar_pdf_mdfe) | **GET** /mdfe/{id}/pdf | Baixar PDF do DAMDFE
*MdfeApi* | [**baixar_xml_cancelamento_mdfe**](docs/MdfeApi.md#baixar_xml_cancelamento_mdfe) | **GET** /mdfe/{id}/cancelamento/xml | Baixar XML do cancelamento
*MdfeApi* | [**baixar_xml_encerramento_mdfe**](docs/MdfeApi.md#baixar_xml_encerramento_mdfe) | **GET** /mdfe/{id}/encerramento/xml | Baixar XML do encerramento
*MdfeApi* | [**baixar_xml_evento_mdfe**](docs/MdfeApi.md#baixar_xml_evento_mdfe) | **GET** /mdfe/eventos/{id}/xml | Baixar XML do evento
*MdfeApi* | [**baixar_xml_mdfe**](docs/MdfeApi.md#baixar_xml_mdfe) | **GET** /mdfe/{id}/xml | Baixar XML do MDF-e processado
*MdfeApi* | [**baixar_xml_mdfe_manifesto**](docs/MdfeApi.md#baixar_xml_mdfe_manifesto) | **GET** /mdfe/{id}/xml/manifesto | Baixar XML do MDF-e
*MdfeApi* | [**baixar_xml_mdfe_protocolo**](docs/MdfeApi.md#baixar_xml_mdfe_protocolo) | **GET** /mdfe/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
*MdfeApi* | [**cancelar_mdfe**](docs/MdfeApi.md#cancelar_mdfe) | **POST** /mdfe/{id}/cancelamento | Cancelar um MDF-e autorizado
*MdfeApi* | [**consultar_cancelamento_mdfe**](docs/MdfeApi.md#consultar_cancelamento_mdfe) | **GET** /mdfe/{id}/cancelamento | Consultar o cancelamento do MDF-e
*MdfeApi* | [**consultar_encerramento_mdfe**](docs/MdfeApi.md#consultar_encerramento_mdfe) | **GET** /mdfe/{id}/encerramento | Consultar encerramento do MDF-e
*MdfeApi* | [**consultar_evento_mdfe**](docs/MdfeApi.md#consultar_evento_mdfe) | **GET** /mdfe/eventos/{id} | Consultar evento do MDF-e
*MdfeApi* | [**consultar_lote_mdfe**](docs/MdfeApi.md#consultar_lote_mdfe) | **GET** /mdfe/lotes/{id} | Consultar lote de MDF-e
*MdfeApi* | [**consultar_mdfe**](docs/MdfeApi.md#consultar_mdfe) | **GET** /mdfe/{id} | Consultar manifesto
*MdfeApi* | [**consultar_mdfe_nao_encerrados**](docs/MdfeApi.md#consultar_mdfe_nao_encerrados) | **GET** /mdfe/nao-encerrados | Consulta MDF-e não encerrados
*MdfeApi* | [**consultar_status_sefaz_mdfe**](docs/MdfeApi.md#consultar_status_sefaz_mdfe) | **GET** /mdfe/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
*MdfeApi* | [**emitir_lote_mdfe**](docs/MdfeApi.md#emitir_lote_mdfe) | **POST** /mdfe/lotes | Emitir lote de MDF-e
*MdfeApi* | [**emitir_mdfe**](docs/MdfeApi.md#emitir_mdfe) | **POST** /mdfe | Emitir MDF-e
*MdfeApi* | [**encerrar_mdfe**](docs/MdfeApi.md#encerrar_mdfe) | **POST** /mdfe/{id}/encerramento | Encerrar um MDF-e autorizado
*MdfeApi* | [**incluir_condutor_mdfe**](docs/MdfeApi.md#incluir_condutor_mdfe) | **POST** /mdfe/{id}/inclusao-condutor | Incluir um condutor em um MDF-e autorizado
*MdfeApi* | [**incluir_dfe_mdfe**](docs/MdfeApi.md#incluir_dfe_mdfe) | **POST** /mdfe/{id}/inclusao-dfe | Incluir um DF-e em um MDF-e autorizado
*MdfeApi* | [**listar_lotes_mdfe**](docs/MdfeApi.md#listar_lotes_mdfe) | **GET** /mdfe/lotes | Listar lotes de MDF-e
*MdfeApi* | [**listar_mdfe**](docs/MdfeApi.md#listar_mdfe) | **GET** /mdfe | Listar MDF-e
*MdfeApi* | [**sincronizar_mdfe**](docs/MdfeApi.md#sincronizar_mdfe) | **POST** /mdfe/{id}/sincronizar | Sincroniza dados no MDF-e a partir da SEFAZ
*NfceApi* | [**baixar_esc_pos_nfce**](docs/NfceApi.md#baixar_esc_pos_nfce) | **GET** /nfce/{id}/escpos | Comandos ESC/POS para impressão do DANFCE
*NfceApi* | [**baixar_pdf_cancelamento_nfce**](docs/NfceApi.md#baixar_pdf_cancelamento_nfce) | **GET** /nfce/{id}/cancelamento/pdf | Baixar PDF do cancelamento
*NfceApi* | [**baixar_pdf_evento_nfce**](docs/NfceApi.md#baixar_pdf_evento_nfce) | **GET** /nfce/eventos/{id}/pdf | Baixar PDF do evento
*NfceApi* | [**baixar_pdf_inutilizacao_nfce**](docs/NfceApi.md#baixar_pdf_inutilizacao_nfce) | **GET** /nfce/inutilizacoes/{id}/pdf | Baixar PDF da inutilização
*NfceApi* | [**baixar_pdf_nfce**](docs/NfceApi.md#baixar_pdf_nfce) | **GET** /nfce/{id}/pdf | Baixar PDF do DANFCE
*NfceApi* | [**baixar_previa_pdf_nfce**](docs/NfceApi.md#baixar_previa_pdf_nfce) | **POST** /nfce/previa/pdf | Prévia do PDF do DANFCE
*NfceApi* | [**baixar_previa_xml_nfce**](docs/NfceApi.md#baixar_previa_xml_nfce) | **POST** /nfce/previa/xml | Prévia do XML da NFC-e
*NfceApi* | [**baixar_xml_cancelamento_nfce**](docs/NfceApi.md#baixar_xml_cancelamento_nfce) | **GET** /nfce/{id}/cancelamento/xml | Baixar XML do cancelamento
*NfceApi* | [**baixar_xml_evento_nfce**](docs/NfceApi.md#baixar_xml_evento_nfce) | **GET** /nfce/eventos/{id}/xml | Baixar XML do evento
*NfceApi* | [**baixar_xml_inutilizacao_nfce**](docs/NfceApi.md#baixar_xml_inutilizacao_nfce) | **GET** /nfce/inutilizacoes/{id}/xml | Baixar XML da inutilização
*NfceApi* | [**baixar_xml_nfce**](docs/NfceApi.md#baixar_xml_nfce) | **GET** /nfce/{id}/xml | Baixar XML da NFC-e processada
*NfceApi* | [**baixar_xml_nfce_nota**](docs/NfceApi.md#baixar_xml_nfce_nota) | **GET** /nfce/{id}/xml/nota | Baixar XML da NFC-e
*NfceApi* | [**baixar_xml_nfce_protocolo**](docs/NfceApi.md#baixar_xml_nfce_protocolo) | **GET** /nfce/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
*NfceApi* | [**cancelar_nfce**](docs/NfceApi.md#cancelar_nfce) | **POST** /nfce/{id}/cancelamento | Cancelar uma NFC-e autorizada
*NfceApi* | [**consultar_cancelamento_nfce**](docs/NfceApi.md#consultar_cancelamento_nfce) | **GET** /nfce/{id}/cancelamento | Consultar o cancelamento da NFC-e
*NfceApi* | [**consultar_evento_nfce**](docs/NfceApi.md#consultar_evento_nfce) | **GET** /nfce/eventos/{id} | Consultar evento
*NfceApi* | [**consultar_inutilizacao_nfce**](docs/NfceApi.md#consultar_inutilizacao_nfce) | **GET** /nfce/inutilizacoes/{id} | Consultar a inutilização de sequência de numeração
*NfceApi* | [**consultar_lote_nfce**](docs/NfceApi.md#consultar_lote_nfce) | **GET** /nfce/lotes/{id} | Consultar lote de NFC-e
*NfceApi* | [**consultar_nfce**](docs/NfceApi.md#consultar_nfce) | **GET** /nfce/{id} | Consultar NFC-e
*NfceApi* | [**consultar_status_sefaz_nfce**](docs/NfceApi.md#consultar_status_sefaz_nfce) | **GET** /nfce/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
*NfceApi* | [**emitir_lote_nfce**](docs/NfceApi.md#emitir_lote_nfce) | **POST** /nfce/lotes | Emitir lote de NFC-e
*NfceApi* | [**emitir_nfce**](docs/NfceApi.md#emitir_nfce) | **POST** /nfce | Emitir NFC-e
*NfceApi* | [**enviar_email_nfce**](docs/NfceApi.md#enviar_email_nfce) | **POST** /nfce/{id}/email | Enviar e-mail
*NfceApi* | [**inutilizar_numeracao_nfce**](docs/NfceApi.md#inutilizar_numeracao_nfce) | **POST** /nfce/inutilizacoes | Inutilizar uma sequência de numeração de NFC-e
*NfceApi* | [**listar_eventos_nfce**](docs/NfceApi.md#listar_eventos_nfce) | **GET** /nfce/eventos | Listar eventos
*NfceApi* | [**listar_lotes_nfce**](docs/NfceApi.md#listar_lotes_nfce) | **GET** /nfce/lotes | Listar lotes de NFC-e
*NfceApi* | [**listar_nfce**](docs/NfceApi.md#listar_nfce) | **GET** /nfce | Listar NFC-e
*NfceApi* | [**sincronizar_nfce**](docs/NfceApi.md#sincronizar_nfce) | **POST** /nfce/{id}/sincronizar | Sincroniza dados na NFC-e a partir da SEFAZ
*NfcomApi* | [**baixar_pdf_nfcom**](docs/NfcomApi.md#baixar_pdf_nfcom) | **GET** /nfcom/{id}/pdf | Baixar PDF do DANFE-COM
*NfcomApi* | [**baixar_xml_cancelamento_nfcom**](docs/NfcomApi.md#baixar_xml_cancelamento_nfcom) | **GET** /nfcom/{id}/cancelamento/xml | Baixar XML do cancelamento
*NfcomApi* | [**baixar_xml_nfcom**](docs/NfcomApi.md#baixar_xml_nfcom) | **GET** /nfcom/{id}/xml | Baixar XML da NFCom processada
*NfcomApi* | [**baixar_xml_nfcom_nota**](docs/NfcomApi.md#baixar_xml_nfcom_nota) | **GET** /nfcom/{id}/xml/nota | Baixar XML da NFCom
*NfcomApi* | [**baixar_xml_nfcom_protocolo**](docs/NfcomApi.md#baixar_xml_nfcom_protocolo) | **GET** /nfcom/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
*NfcomApi* | [**cancelar_nfcom**](docs/NfcomApi.md#cancelar_nfcom) | **POST** /nfcom/{id}/cancelamento | Cancelar uma NFCom autorizada
*NfcomApi* | [**consultar_cancelamento_nfcom**](docs/NfcomApi.md#consultar_cancelamento_nfcom) | **GET** /nfcom/{id}/cancelamento | Consultar o cancelamento da NFCom
*NfcomApi* | [**consultar_nfcom**](docs/NfcomApi.md#consultar_nfcom) | **GET** /nfcom/{id} | Consultar NFCom
*NfcomApi* | [**consultar_status_sefaz_nfcom**](docs/NfcomApi.md#consultar_status_sefaz_nfcom) | **GET** /nfcom/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
*NfcomApi* | [**emitir_nfcom**](docs/NfcomApi.md#emitir_nfcom) | **POST** /nfcom | Emitir NFCom
*NfcomApi* | [**listar_nfcom**](docs/NfcomApi.md#listar_nfcom) | **GET** /nfcom | Listar NFCom
*NfeApi* | [**baixar_pdf_cancelamento_nfe**](docs/NfeApi.md#baixar_pdf_cancelamento_nfe) | **GET** /nfe/{id}/cancelamento/pdf | Baixar PDF do cancelamento
*NfeApi* | [**baixar_pdf_carta_correcao_nfe**](docs/NfeApi.md#baixar_pdf_carta_correcao_nfe) | **GET** /nfe/{id}/carta-correcao/pdf | Baixar PDF da carta de correção
*NfeApi* | [**baixar_pdf_evento_nfe**](docs/NfeApi.md#baixar_pdf_evento_nfe) | **GET** /nfe/eventos/{id}/pdf | Baixar PDF do evento
*NfeApi* | [**baixar_pdf_inutilizacao_nfe**](docs/NfeApi.md#baixar_pdf_inutilizacao_nfe) | **GET** /nfe/inutilizacoes/{id}/pdf | Baixar PDF da inutilização
*NfeApi* | [**baixar_pdf_nfe**](docs/NfeApi.md#baixar_pdf_nfe) | **GET** /nfe/{id}/pdf | Baixar PDF do DANFE
*NfeApi* | [**baixar_previa_pdf_nfe**](docs/NfeApi.md#baixar_previa_pdf_nfe) | **POST** /nfe/previa/pdf | Prévia do PDF do DANFE
*NfeApi* | [**baixar_previa_xml_nfe**](docs/NfeApi.md#baixar_previa_xml_nfe) | **POST** /nfe/previa/xml | Prévia do XML da NF-e
*NfeApi* | [**baixar_xml_cancelamento_nfe**](docs/NfeApi.md#baixar_xml_cancelamento_nfe) | **GET** /nfe/{id}/cancelamento/xml | Baixar XML do cancelamento
*NfeApi* | [**baixar_xml_carta_correcao_nfe**](docs/NfeApi.md#baixar_xml_carta_correcao_nfe) | **GET** /nfe/{id}/carta-correcao/xml | Baixar XML da carta de correção
*NfeApi* | [**baixar_xml_evento_nfe**](docs/NfeApi.md#baixar_xml_evento_nfe) | **GET** /nfe/eventos/{id}/xml | Baixar XML do evento
*NfeApi* | [**baixar_xml_inutilizacao_nfe**](docs/NfeApi.md#baixar_xml_inutilizacao_nfe) | **GET** /nfe/inutilizacoes/{id}/xml | Baixar XML da inutilização
*NfeApi* | [**baixar_xml_nfe**](docs/NfeApi.md#baixar_xml_nfe) | **GET** /nfe/{id}/xml | Baixar XML da NF-e processada
*NfeApi* | [**baixar_xml_nfe_nota**](docs/NfeApi.md#baixar_xml_nfe_nota) | **GET** /nfe/{id}/xml/nota | Baixar XML da NF-e
*NfeApi* | [**baixar_xml_nfe_protocolo**](docs/NfeApi.md#baixar_xml_nfe_protocolo) | **GET** /nfe/{id}/xml/protocolo | Baixar XML do Protocolo da SEFAZ
*NfeApi* | [**cancelar_nfe**](docs/NfeApi.md#cancelar_nfe) | **POST** /nfe/{id}/cancelamento | Cancelar uma NF-e autorizada
*NfeApi* | [**consultar_cancelamento_nfe**](docs/NfeApi.md#consultar_cancelamento_nfe) | **GET** /nfe/{id}/cancelamento | Consultar o cancelamento da NF-e
*NfeApi* | [**consultar_carta_correcao_nfe**](docs/NfeApi.md#consultar_carta_correcao_nfe) | **GET** /nfe/{id}/carta-correcao | Consultar a solicitação de correção da NF-e
*NfeApi* | [**consultar_contribuinte_nfe**](docs/NfeApi.md#consultar_contribuinte_nfe) | **GET** /nfe/cadastro-contribuinte | Consultar contribuinte
*NfeApi* | [**consultar_evento_nfe**](docs/NfeApi.md#consultar_evento_nfe) | **GET** /nfe/eventos/{id} | Consultar evento
*NfeApi* | [**consultar_inutilizacao_nfe**](docs/NfeApi.md#consultar_inutilizacao_nfe) | **GET** /nfe/inutilizacoes/{id} | Consultar a inutilização de sequência de numeração
*NfeApi* | [**consultar_lote_nfe**](docs/NfeApi.md#consultar_lote_nfe) | **GET** /nfe/lotes/{id} | Consultar lote de NF-e
*NfeApi* | [**consultar_nfe**](docs/NfeApi.md#consultar_nfe) | **GET** /nfe/{id} | Consultar NF-e
*NfeApi* | [**consultar_status_sefaz_nfe**](docs/NfeApi.md#consultar_status_sefaz_nfe) | **GET** /nfe/sefaz/status | Consulta do Status do Serviço na SEFAZ Autorizadora
*NfeApi* | [**criar_carta_correcao_nfe**](docs/NfeApi.md#criar_carta_correcao_nfe) | **POST** /nfe/{id}/carta-correcao | Solicitar correção da NF-e
*NfeApi* | [**emitir_lote_nfe**](docs/NfeApi.md#emitir_lote_nfe) | **POST** /nfe/lotes | Emitir lote de NF-e
*NfeApi* | [**emitir_nfe**](docs/NfeApi.md#emitir_nfe) | **POST** /nfe | Emitir NF-e
*NfeApi* | [**enviar_email_nfe**](docs/NfeApi.md#enviar_email_nfe) | **POST** /nfe/{id}/email | Enviar e-mail
*NfeApi* | [**inutilizar_numeracao_nfe**](docs/NfeApi.md#inutilizar_numeracao_nfe) | **POST** /nfe/inutilizacoes | Inutilizar uma sequência de numeração de NF-e
*NfeApi* | [**listar_eventos_nfe**](docs/NfeApi.md#listar_eventos_nfe) | **GET** /nfe/eventos | Listar eventos
*NfeApi* | [**listar_lotes_nfe**](docs/NfeApi.md#listar_lotes_nfe) | **GET** /nfe/lotes | Listar lotes de NF-e
*NfeApi* | [**listar_nfe**](docs/NfeApi.md#listar_nfe) | **GET** /nfe | Listar NF-e
*NfeApi* | [**sincronizar_nfe**](docs/NfeApi.md#sincronizar_nfe) | **POST** /nfe/{id}/sincronizar | Sincroniza dados na NF-e a partir da SEFAZ
*NfseApi* | [**baixar_pdf_nfse**](docs/NfseApi.md#baixar_pdf_nfse) | **GET** /nfse/{id}/pdf | Baixar PDF do DANFSE
*NfseApi* | [**baixar_xml_cancelamento_nfse**](docs/NfseApi.md#baixar_xml_cancelamento_nfse) | **GET** /nfse/{Id}/cancelamento/xml | Baixar XML do evento de cancelamento
*NfseApi* | [**baixar_xml_dps**](docs/NfseApi.md#baixar_xml_dps) | **GET** /nfse/{id}/xml/dps | Baixar XML da DPS
*NfseApi* | [**baixar_xml_nfse**](docs/NfseApi.md#baixar_xml_nfse) | **GET** /nfse/{id}/xml | Baixar XML da NFS-e processada
*NfseApi* | [**cancelar_nfse**](docs/NfseApi.md#cancelar_nfse) | **POST** /nfse/{id}/cancelamento | Cancelar uma NFS-e autorizada
*NfseApi* | [**cidades_atendidas**](docs/NfseApi.md#cidades_atendidas) | **GET** /nfse/cidades | Cidades atendidas
*NfseApi* | [**consultar_cancelamento_nfse**](docs/NfseApi.md#consultar_cancelamento_nfse) | **GET** /nfse/{id}/cancelamento | Consultar o cancelamento da NFS-e
*NfseApi* | [**consultar_lote_nfse**](docs/NfseApi.md#consultar_lote_nfse) | **GET** /nfse/lotes/{id} | Consultar lote de NFS-e
*NfseApi* | [**consultar_metadados**](docs/NfseApi.md#consultar_metadados) | **GET** /nfse/cidades/{codigo_ibge} | Consultar metadados
*NfseApi* | [**consultar_nfse**](docs/NfseApi.md#consultar_nfse) | **GET** /nfse/{id} | Consultar NFS-e
*NfseApi* | [**emitir_lote_nfse**](docs/NfseApi.md#emitir_lote_nfse) | **POST** /nfse/lotes | Emitir lote de NFS-e
*NfseApi* | [**emitir_lote_nfse_dps**](docs/NfseApi.md#emitir_lote_nfse_dps) | **POST** /nfse/dps/lotes | Emitir lote de NFS-e
*NfseApi* | [**emitir_nfse**](docs/NfseApi.md#emitir_nfse) | **POST** /nfse | Emitir NFS-e
*NfseApi* | [**emitir_nfse_dps**](docs/NfseApi.md#emitir_nfse_dps) | **POST** /nfse/dps | Emitir NFS-e
*NfseApi* | [**listar_lotes_nfse**](docs/NfseApi.md#listar_lotes_nfse) | **GET** /nfse/lotes | Listar lotes de NFS-e
*NfseApi* | [**listar_nfse**](docs/NfseApi.md#listar_nfse) | **GET** /nfse | Listar NFS-e
*NfseApi* | [**sincronizar_nfse**](docs/NfseApi.md#sincronizar_nfse) | **POST** /nfse/{id}/sincronizar | Sincroniza dados na NFS-e a partir da Prefeitura


## Documentação dos modelos

 - [AtvEvento](docs/AtvEvento.md)
 - [BeneficioMunicipal](docs/BeneficioMunicipal.md)
 - [CServ](docs/CServ.md)
 - [CepEndereco](docs/CepEndereco.md)
 - [CnpjCnae](docs/CnpjCnae.md)
 - [CnpjCnaeSecundario](docs/CnpjCnaeSecundario.md)
 - [CnpjEmpresa](docs/CnpjEmpresa.md)
 - [CnpjEndereco](docs/CnpjEndereco.md)
 - [CnpjFaixaEtaria](docs/CnpjFaixaEtaria.md)
 - [CnpjIdentificadorSocio](docs/CnpjIdentificadorSocio.md)
 - [CnpjListagem](docs/CnpjListagem.md)
 - [CnpjMotivoSituacaoCadastral](docs/CnpjMotivoSituacaoCadastral.md)
 - [CnpjMunicipio](docs/CnpjMunicipio.md)
 - [CnpjNaturezaJuridica](docs/CnpjNaturezaJuridica.md)
 - [CnpjOpcaoSimei](docs/CnpjOpcaoSimei.md)
 - [CnpjOpcaoSimples](docs/CnpjOpcaoSimples.md)
 - [CnpjPais](docs/CnpjPais.md)
 - [CnpjPorteEmpresa](docs/CnpjPorteEmpresa.md)
 - [CnpjQualificacaoSocio](docs/CnpjQualificacaoSocio.md)
 - [CnpjRepresentanteLegal](docs/CnpjRepresentanteLegal.md)
 - [CnpjSituacaoCadastral](docs/CnpjSituacaoCadastral.md)
 - [CnpjSituacaoEspecial](docs/CnpjSituacaoEspecial.md)
 - [CnpjSocio](docs/CnpjSocio.md)
 - [CnpjTelefone](docs/CnpjTelefone.md)
 - [ComExterior](docs/ComExterior.md)
 - [ContaCota](docs/ContaCota.md)
 - [ContaCotaListagem](docs/ContaCotaListagem.md)
 - [ContaCotaPrePago](docs/ContaCotaPrePago.md)
 - [ContaExtratoCredito](docs/ContaExtratoCredito.md)
 - [ContaExtratoCreditoListagem](docs/ContaExtratoCreditoListagem.md)
 - [CteCartaCorrecao](docs/CteCartaCorrecao.md)
 - [CteInfCorrecao](docs/CteInfCorrecao.md)
 - [CteOsCartaCorrecao](docs/CteOsCartaCorrecao.md)
 - [CteOsInfCorrecao](docs/CteOsInfCorrecao.md)
 - [CteOsPedidoCancelamento](docs/CteOsPedidoCancelamento.md)
 - [CteOsPedidoCartaCorrecao](docs/CteOsPedidoCartaCorrecao.md)
 - [CteOsPedidoEmissao](docs/CteOsPedidoEmissao.md)
 - [CteOsSefazALCZFMCBSOS](docs/CteOsSefazALCZFMCBSOS.md)
 - [CteOsSefazAutXMLOS](docs/CteOsSefazAutXMLOS.md)
 - [CteOsSefazCIBSOS](docs/CteOsSefazCIBSOS.md)
 - [CteOsSefazCobrOS](docs/CteOsSefazCobrOS.md)
 - [CteOsSefazCompOS](docs/CteOsSefazCompOS.md)
 - [CteOsSefazComplOS](docs/CteOsSefazComplOS.md)
 - [CteOsSefazCompraGovReduzidoOS](docs/CteOsSefazCompraGovReduzidoOS.md)
 - [CteOsSefazDevTribOS](docs/CteOsSefazDevTribOS.md)
 - [CteOsSefazDifOS](docs/CteOsSefazDifOS.md)
 - [CteOsSefazDupOS](docs/CteOsSefazDupOS.md)
 - [CteOsSefazEmitOS](docs/CteOsSefazEmitOS.md)
 - [CteOsSefazEndeEmiOS](docs/CteOsSefazEndeEmiOS.md)
 - [CteOsSefazEnderecoOS](docs/CteOsSefazEnderecoOS.md)
 - [CteOsSefazEstornoCredOS](docs/CteOsSefazEstornoCredOS.md)
 - [CteOsSefazFatOS](docs/CteOsSefazFatOS.md)
 - [CteOsSefazGCBSOS](docs/CteOsSefazGCBSOS.md)
 - [CteOsSefazGIBSMunOS](docs/CteOsSefazGIBSMunOS.md)
 - [CteOsSefazGIBSUFOS](docs/CteOsSefazGIBSUFOS.md)
 - [CteOsSefazGPagAntecipadoOS](docs/CteOsSefazGPagAntecipadoOS.md)
 - [CteOsSefazICMS00OS](docs/CteOsSefazICMS00OS.md)
 - [CteOsSefazICMS20OS](docs/CteOsSefazICMS20OS.md)
 - [CteOsSefazICMS45OS](docs/CteOsSefazICMS45OS.md)
 - [CteOsSefazICMS90OS](docs/CteOsSefazICMS90OS.md)
 - [CteOsSefazICMSOutraUFOS](docs/CteOsSefazICMSOutraUFOS.md)
 - [CteOsSefazICMSSNOS](docs/CteOsSefazICMSSNOS.md)
 - [CteOsSefazICMSUFFimOS](docs/CteOsSefazICMSUFFimOS.md)
 - [CteOsSefazIdeOS](docs/CteOsSefazIdeOS.md)
 - [CteOsSefazImpOS](docs/CteOsSefazImpOS.md)
 - [CteOsSefazInfCTeNormOS](docs/CteOsSefazInfCTeNormOS.md)
 - [CteOsSefazInfCTeSuplOS](docs/CteOsSefazInfCTeSuplOS.md)
 - [CteOsSefazInfCteCompOS](docs/CteOsSefazInfCteCompOS.md)
 - [CteOsSefazInfCteImpOS](docs/CteOsSefazInfCteImpOS.md)
 - [CteOsSefazInfCteOS](docs/CteOsSefazInfCteOS.md)
 - [CteOsSefazInfCteSubOS](docs/CteOsSefazInfCteSubOS.md)
 - [CteOsSefazInfDocRefOS](docs/CteOsSefazInfDocRefOS.md)
 - [CteOsSefazInfFretamentoOS](docs/CteOsSefazInfFretamentoOS.md)
 - [CteOsSefazInfGTVeCompOS](docs/CteOsSefazInfGTVeCompOS.md)
 - [CteOsSefazInfGTVeOS](docs/CteOsSefazInfGTVeOS.md)
 - [CteOsSefazInfModalOS](docs/CteOsSefazInfModalOS.md)
 - [CteOsSefazInfPercursoOS](docs/CteOsSefazInfPercursoOS.md)
 - [CteOsSefazInfQOS](docs/CteOsSefazInfQOS.md)
 - [CteOsSefazInfServicoOS](docs/CteOsSefazInfServicoOS.md)
 - [CteOsSefazInfTribFedOS](docs/CteOsSefazInfTribFedOS.md)
 - [CteOsSefazObsContOS](docs/CteOsSefazObsContOS.md)
 - [CteOsSefazObsFiscoOS](docs/CteOsSefazObsFiscoOS.md)
 - [CteOsSefazPagamentoRTCOS](docs/CteOsSefazPagamentoRTCOS.md)
 - [CteOsSefazPgtoVincOS](docs/CteOsSefazPgtoVincOS.md)
 - [CteOsSefazPropOS](docs/CteOsSefazPropOS.md)
 - [CteOsSefazRedOS](docs/CteOsSefazRedOS.md)
 - [CteOsSefazRespTecOS](docs/CteOsSefazRespTecOS.md)
 - [CteOsSefazRodoOS](docs/CteOsSefazRodoOS.md)
 - [CteOsSefazSegOS](docs/CteOsSefazSegOS.md)
 - [CteOsSefazTomaOS](docs/CteOsSefazTomaOS.md)
 - [CteOsSefazTribCTeOS](docs/CteOsSefazTribCTeOS.md)
 - [CteOsSefazTribCompraGovOS](docs/CteOsSefazTribCompraGovOS.md)
 - [CteOsSefazTribRegularOS](docs/CteOsSefazTribRegularOS.md)
 - [CteOsSefazVPrestOS](docs/CteOsSefazVPrestOS.md)
 - [CteOsSefazVeicOS](docs/CteOsSefazVeicOS.md)
 - [CtePedidoCancelamento](docs/CtePedidoCancelamento.md)
 - [CtePedidoCartaCorrecao](docs/CtePedidoCartaCorrecao.md)
 - [CtePedidoEmissao](docs/CtePedidoEmissao.md)
 - [CteSefazALCZFMCBS](docs/CteSefazALCZFMCBS.md)
 - [CteSefazAereo](docs/CteSefazAereo.md)
 - [CteSefazAquav](docs/CteSefazAquav.md)
 - [CteSefazAutXML](docs/CteSefazAutXML.md)
 - [CteSefazBalsa](docs/CteSefazBalsa.md)
 - [CteSefazCIBS](docs/CteSefazCIBS.md)
 - [CteSefazCobr](docs/CteSefazCobr.md)
 - [CteSefazComData](docs/CteSefazComData.md)
 - [CteSefazComHora](docs/CteSefazComHora.md)
 - [CteSefazComp](docs/CteSefazComp.md)
 - [CteSefazCompl](docs/CteSefazCompl.md)
 - [CteSefazCompraGovReduzido](docs/CteSefazCompraGovReduzido.md)
 - [CteSefazDest](docs/CteSefazDest.md)
 - [CteSefazDetCont](docs/CteSefazDetCont.md)
 - [CteSefazDetContInfDoc](docs/CteSefazDetContInfDoc.md)
 - [CteSefazDetContInfDocInfNF](docs/CteSefazDetContInfDocInfNF.md)
 - [CteSefazDetContInfDocInfNFe](docs/CteSefazDetContInfDocInfNFe.md)
 - [CteSefazDevTrib](docs/CteSefazDevTrib.md)
 - [CteSefazDif](docs/CteSefazDif.md)
 - [CteSefazDocAnt](docs/CteSefazDocAnt.md)
 - [CteSefazDup](docs/CteSefazDup.md)
 - [CteSefazDuto](docs/CteSefazDuto.md)
 - [CteSefazEmiDocAnt](docs/CteSefazEmiDocAnt.md)
 - [CteSefazEmiOcc](docs/CteSefazEmiOcc.md)
 - [CteSefazEmit](docs/CteSefazEmit.md)
 - [CteSefazEndeEmi](docs/CteSefazEndeEmi.md)
 - [CteSefazEnderFer](docs/CteSefazEnderFer.md)
 - [CteSefazEndereco](docs/CteSefazEndereco.md)
 - [CteSefazEntrega](docs/CteSefazEntrega.md)
 - [CteSefazEstornoCred](docs/CteSefazEstornoCred.md)
 - [CteSefazExped](docs/CteSefazExped.md)
 - [CteSefazFat](docs/CteSefazFat.md)
 - [CteSefazFerroEnv](docs/CteSefazFerroEnv.md)
 - [CteSefazFerrov](docs/CteSefazFerrov.md)
 - [CteSefazFluxo](docs/CteSefazFluxo.md)
 - [CteSefazGCBS](docs/CteSefazGCBS.md)
 - [CteSefazGIBSMun](docs/CteSefazGIBSMun.md)
 - [CteSefazGIBSUF](docs/CteSefazGIBSUF.md)
 - [CteSefazGPagAntecipado](docs/CteSefazGPagAntecipado.md)
 - [CteSefazICMS00](docs/CteSefazICMS00.md)
 - [CteSefazICMS20](docs/CteSefazICMS20.md)
 - [CteSefazICMS45](docs/CteSefazICMS45.md)
 - [CteSefazICMS60](docs/CteSefazICMS60.md)
 - [CteSefazICMS90](docs/CteSefazICMS90.md)
 - [CteSefazICMSOutraUF](docs/CteSefazICMSOutraUF.md)
 - [CteSefazICMSSN](docs/CteSefazICMSSN.md)
 - [CteSefazICMSUFFim](docs/CteSefazICMSUFFim.md)
 - [CteSefazIdDocAnt](docs/CteSefazIdDocAnt.md)
 - [CteSefazIdDocAntEle](docs/CteSefazIdDocAntEle.md)
 - [CteSefazIdDocAntPap](docs/CteSefazIdDocAntPap.md)
 - [CteSefazIde](docs/CteSefazIde.md)
 - [CteSefazImp](docs/CteSefazImp.md)
 - [CteSefazInfCTeMultimodal](docs/CteSefazInfCTeMultimodal.md)
 - [CteSefazInfCTeNorm](docs/CteSefazInfCTeNorm.md)
 - [CteSefazInfCTeSupl](docs/CteSefazInfCTeSupl.md)
 - [CteSefazInfCarga](docs/CteSefazInfCarga.md)
 - [CteSefazInfCte](docs/CteSefazInfCte.md)
 - [CteSefazInfCteComp](docs/CteSefazInfCteComp.md)
 - [CteSefazInfCteImp](docs/CteSefazInfCteImp.md)
 - [CteSefazInfCteSub](docs/CteSefazInfCteSub.md)
 - [CteSefazInfDCe](docs/CteSefazInfDCe.md)
 - [CteSefazInfDoc](docs/CteSefazInfDoc.md)
 - [CteSefazInfGlobalizado](docs/CteSefazInfGlobalizado.md)
 - [CteSefazInfModal](docs/CteSefazInfModal.md)
 - [CteSefazInfNF](docs/CteSefazInfNF.md)
 - [CteSefazInfNFe](docs/CteSefazInfNFe.md)
 - [CteSefazInfOutros](docs/CteSefazInfOutros.md)
 - [CteSefazInfQ](docs/CteSefazInfQ.md)
 - [CteSefazInfSeg](docs/CteSefazInfSeg.md)
 - [CteSefazInfServVinc](docs/CteSefazInfServVinc.md)
 - [CteSefazInfSolicNFF](docs/CteSefazInfSolicNFF.md)
 - [CteSefazInfTotAP](docs/CteSefazInfTotAP.md)
 - [CteSefazLacUnidCarga](docs/CteSefazLacUnidCarga.md)
 - [CteSefazLacUnidTransp](docs/CteSefazLacUnidTransp.md)
 - [CteSefazLacre](docs/CteSefazLacre.md)
 - [CteSefazMultimodal](docs/CteSefazMultimodal.md)
 - [CteSefazNatCarga](docs/CteSefazNatCarga.md)
 - [CteSefazNoInter](docs/CteSefazNoInter.md)
 - [CteSefazNoPeriodo](docs/CteSefazNoPeriodo.md)
 - [CteSefazObsCont](docs/CteSefazObsCont.md)
 - [CteSefazObsFisco](docs/CteSefazObsFisco.md)
 - [CteSefazOcc](docs/CteSefazOcc.md)
 - [CteSefazPagamentoRTC](docs/CteSefazPagamentoRTC.md)
 - [CteSefazPass](docs/CteSefazPass.md)
 - [CteSefazPeri](docs/CteSefazPeri.md)
 - [CteSefazPgtoVinc](docs/CteSefazPgtoVinc.md)
 - [CteSefazReceb](docs/CteSefazReceb.md)
 - [CteSefazRed](docs/CteSefazRed.md)
 - [CteSefazRem](docs/CteSefazRem.md)
 - [CteSefazRespTec](docs/CteSefazRespTec.md)
 - [CteSefazRodo](docs/CteSefazRodo.md)
 - [CteSefazSeg](docs/CteSefazSeg.md)
 - [CteSefazSemData](docs/CteSefazSemData.md)
 - [CteSefazSemHora](docs/CteSefazSemHora.md)
 - [CteSefazTarifa](docs/CteSefazTarifa.md)
 - [CteSefazToma3](docs/CteSefazToma3.md)
 - [CteSefazToma4](docs/CteSefazToma4.md)
 - [CteSefazTrafMut](docs/CteSefazTrafMut.md)
 - [CteSefazTribCTe](docs/CteSefazTribCTe.md)
 - [CteSefazTribCompraGov](docs/CteSefazTribCompraGov.md)
 - [CteSefazTribRegular](docs/CteSefazTribRegular.md)
 - [CteSefazUnidCarga](docs/CteSefazUnidCarga.md)
 - [CteSefazUnidadeTransp](docs/CteSefazUnidadeTransp.md)
 - [CteSefazVPrest](docs/CteSefazVPrest.md)
 - [CteSefazVeicNovos](docs/CteSefazVeicNovos.md)
 - [CteSimpPedidoEmissao](docs/CteSimpPedidoEmissao.md)
 - [CteSimpSefazALCZFMCBSSimp](docs/CteSimpSefazALCZFMCBSSimp.md)
 - [CteSimpSefazAereoSimp](docs/CteSimpSefazAereoSimp.md)
 - [CteSimpSefazAquavSimp](docs/CteSimpSefazAquavSimp.md)
 - [CteSimpSefazAutXMLSimp](docs/CteSimpSefazAutXMLSimp.md)
 - [CteSimpSefazBalsaSimp](docs/CteSimpSefazBalsaSimp.md)
 - [CteSimpSefazCIBSSimp](docs/CteSimpSefazCIBSSimp.md)
 - [CteSimpSefazCobrSimp](docs/CteSimpSefazCobrSimp.md)
 - [CteSimpSefazCompSimp](docs/CteSimpSefazCompSimp.md)
 - [CteSimpSefazComplSimp](docs/CteSimpSefazComplSimp.md)
 - [CteSimpSefazCompraGovReduzidoSimp](docs/CteSimpSefazCompraGovReduzidoSimp.md)
 - [CteSimpSefazDetContSimp](docs/CteSimpSefazDetContSimp.md)
 - [CteSimpSefazDetSimp](docs/CteSimpSefazDetSimp.md)
 - [CteSimpSefazDevTribSimp](docs/CteSimpSefazDevTribSimp.md)
 - [CteSimpSefazDifSimp](docs/CteSimpSefazDifSimp.md)
 - [CteSimpSefazDupSimp](docs/CteSimpSefazDupSimp.md)
 - [CteSimpSefazDutoSimp](docs/CteSimpSefazDutoSimp.md)
 - [CteSimpSefazEmiOccSimp](docs/CteSimpSefazEmiOccSimp.md)
 - [CteSimpSefazEmitSimp](docs/CteSimpSefazEmitSimp.md)
 - [CteSimpSefazEndeEmiSimp](docs/CteSimpSefazEndeEmiSimp.md)
 - [CteSimpSefazEnderFerSimp](docs/CteSimpSefazEnderFerSimp.md)
 - [CteSimpSefazEnderecoSimp](docs/CteSimpSefazEnderecoSimp.md)
 - [CteSimpSefazEstornoCredSimp](docs/CteSimpSefazEstornoCredSimp.md)
 - [CteSimpSefazFatSimp](docs/CteSimpSefazFatSimp.md)
 - [CteSimpSefazFerroEnvSimp](docs/CteSimpSefazFerroEnvSimp.md)
 - [CteSimpSefazFerrovSimp](docs/CteSimpSefazFerrovSimp.md)
 - [CteSimpSefazFluxoSimp](docs/CteSimpSefazFluxoSimp.md)
 - [CteSimpSefazGCBSSimp](docs/CteSimpSefazGCBSSimp.md)
 - [CteSimpSefazGIBSMunSimp](docs/CteSimpSefazGIBSMunSimp.md)
 - [CteSimpSefazGIBSUFSimp](docs/CteSimpSefazGIBSUFSimp.md)
 - [CteSimpSefazGPagAntecipadoSimp](docs/CteSimpSefazGPagAntecipadoSimp.md)
 - [CteSimpSefazICMS00Simp](docs/CteSimpSefazICMS00Simp.md)
 - [CteSimpSefazICMS20Simp](docs/CteSimpSefazICMS20Simp.md)
 - [CteSimpSefazICMS45Simp](docs/CteSimpSefazICMS45Simp.md)
 - [CteSimpSefazICMS60Simp](docs/CteSimpSefazICMS60Simp.md)
 - [CteSimpSefazICMS90Simp](docs/CteSimpSefazICMS90Simp.md)
 - [CteSimpSefazICMSOutraUFSimp](docs/CteSimpSefazICMSOutraUFSimp.md)
 - [CteSimpSefazICMSSNSimp](docs/CteSimpSefazICMSSNSimp.md)
 - [CteSimpSefazICMSUFFimSimp](docs/CteSimpSefazICMSUFFimSimp.md)
 - [CteSimpSefazIdeSimp](docs/CteSimpSefazIdeSimp.md)
 - [CteSimpSefazImpSimp](docs/CteSimpSefazImpSimp.md)
 - [CteSimpSefazInfCTeSuplSimp](docs/CteSimpSefazInfCTeSuplSimp.md)
 - [CteSimpSefazInfCargaSimp](docs/CteSimpSefazInfCargaSimp.md)
 - [CteSimpSefazInfCteImpSimp](docs/CteSimpSefazInfCteImpSimp.md)
 - [CteSimpSefazInfCteSimp](docs/CteSimpSefazInfCteSimp.md)
 - [CteSimpSefazInfCteSubSimp](docs/CteSimpSefazInfCteSubSimp.md)
 - [CteSimpSefazInfDocAntSimp](docs/CteSimpSefazInfDocAntSimp.md)
 - [CteSimpSefazInfDocInfNFeSimp](docs/CteSimpSefazInfDocInfNFeSimp.md)
 - [CteSimpSefazInfDocSimp](docs/CteSimpSefazInfDocSimp.md)
 - [CteSimpSefazInfModalSimp](docs/CteSimpSefazInfModalSimp.md)
 - [CteSimpSefazInfNFSimp](docs/CteSimpSefazInfNFSimp.md)
 - [CteSimpSefazInfNFeSimp](docs/CteSimpSefazInfNFeSimp.md)
 - [CteSimpSefazInfNFeTranspParcialSimp](docs/CteSimpSefazInfNFeTranspParcialSimp.md)
 - [CteSimpSefazInfQSimp](docs/CteSimpSefazInfQSimp.md)
 - [CteSimpSefazInfSegSimp](docs/CteSimpSefazInfSegSimp.md)
 - [CteSimpSefazInfSolicNFFSimp](docs/CteSimpSefazInfSolicNFFSimp.md)
 - [CteSimpSefazInfTotAPSimp](docs/CteSimpSefazInfTotAPSimp.md)
 - [CteSimpSefazLacUnidCargaSimp](docs/CteSimpSefazLacUnidCargaSimp.md)
 - [CteSimpSefazLacUnidTranspSimp](docs/CteSimpSefazLacUnidTranspSimp.md)
 - [CteSimpSefazLacreSimp](docs/CteSimpSefazLacreSimp.md)
 - [CteSimpSefazMultimodalSimp](docs/CteSimpSefazMultimodalSimp.md)
 - [CteSimpSefazNatCargaSimp](docs/CteSimpSefazNatCargaSimp.md)
 - [CteSimpSefazObsContSimp](docs/CteSimpSefazObsContSimp.md)
 - [CteSimpSefazObsFiscoSimp](docs/CteSimpSefazObsFiscoSimp.md)
 - [CteSimpSefazOccSimp](docs/CteSimpSefazOccSimp.md)
 - [CteSimpSefazPagamentoRTCSimp](docs/CteSimpSefazPagamentoRTCSimp.md)
 - [CteSimpSefazPassSimp](docs/CteSimpSefazPassSimp.md)
 - [CteSimpSefazPeriSimp](docs/CteSimpSefazPeriSimp.md)
 - [CteSimpSefazPgtoVincSimp](docs/CteSimpSefazPgtoVincSimp.md)
 - [CteSimpSefazRedSimp](docs/CteSimpSefazRedSimp.md)
 - [CteSimpSefazRespTecSimp](docs/CteSimpSefazRespTecSimp.md)
 - [CteSimpSefazRodoSimp](docs/CteSimpSefazRodoSimp.md)
 - [CteSimpSefazSegSimp](docs/CteSimpSefazSegSimp.md)
 - [CteSimpSefazTarifaSimp](docs/CteSimpSefazTarifaSimp.md)
 - [CteSimpSefazTomaSimp](docs/CteSimpSefazTomaSimp.md)
 - [CteSimpSefazTotalSimp](docs/CteSimpSefazTotalSimp.md)
 - [CteSimpSefazTrafMutSimp](docs/CteSimpSefazTrafMutSimp.md)
 - [CteSimpSefazTribCTeSimp](docs/CteSimpSefazTribCTeSimp.md)
 - [CteSimpSefazTribCompraGovSimp](docs/CteSimpSefazTribCompraGovSimp.md)
 - [CteSimpSefazTribRegularSimp](docs/CteSimpSefazTribRegularSimp.md)
 - [CteSimpSefazUnidCargaSimp](docs/CteSimpSefazUnidCargaSimp.md)
 - [CteSimpSefazUnidadeTranspSimp](docs/CteSimpSefazUnidadeTranspSimp.md)
 - [DPS](docs/DPS.md)
 - [DcePedidoCancelamento](docs/DcePedidoCancelamento.md)
 - [DcePedidoEmissao](docs/DcePedidoEmissao.md)
 - [DceSefazAutXML](docs/DceSefazAutXML.md)
 - [DceSefazDest](docs/DceSefazDest.md)
 - [DceSefazDet](docs/DceSefazDet.md)
 - [DceSefazECT](docs/DceSefazECT.md)
 - [DceSefazEmit](docs/DceSefazEmit.md)
 - [DceSefazEndeDest](docs/DceSefazEndeDest.md)
 - [DceSefazEndeEmi](docs/DceSefazEndeEmi.md)
 - [DceSefazFisco](docs/DceSefazFisco.md)
 - [DceSefazIde](docs/DceSefazIde.md)
 - [DceSefazInfAdic](docs/DceSefazInfAdic.md)
 - [DceSefazInfDCe](docs/DceSefazInfDCe.md)
 - [DceSefazInfDec](docs/DceSefazInfDec.md)
 - [DceSefazInfSolicDCe](docs/DceSefazInfSolicDCe.md)
 - [DceSefazMarketplace](docs/DceSefazMarketplace.md)
 - [DceSefazObsECT](docs/DceSefazObsECT.md)
 - [DceSefazObsEmit](docs/DceSefazObsEmit.md)
 - [DceSefazObsFisco](docs/DceSefazObsFisco.md)
 - [DceSefazObsMarketplace](docs/DceSefazObsMarketplace.md)
 - [DceSefazProd](docs/DceSefazProd.md)
 - [DceSefazTotal](docs/DceSefazTotal.md)
 - [DceSefazTransp](docs/DceSefazTransp.md)
 - [DceSefazTransportadora](docs/DceSefazTransportadora.md)
 - [Dfe](docs/Dfe.md)
 - [DfeAutorEvento](docs/DfeAutorEvento.md)
 - [DfeAutorizacao](docs/DfeAutorizacao.md)
 - [DfeCancelamento](docs/DfeCancelamento.md)
 - [DfeCartaCorrecao](docs/DfeCartaCorrecao.md)
 - [DfeContribuinteEndereco](docs/DfeContribuinteEndereco.md)
 - [DfeContribuinteInfCad](docs/DfeContribuinteInfCad.md)
 - [DfeContribuinteInfCons](docs/DfeContribuinteInfCons.md)
 - [DfeDebug](docs/DfeDebug.md)
 - [DfeEvento](docs/DfeEvento.md)
 - [DfeEventoListagem](docs/DfeEventoListagem.md)
 - [DfeInutilizacao](docs/DfeInutilizacao.md)
 - [DfeListagem](docs/DfeListagem.md)
 - [DfeLote](docs/DfeLote.md)
 - [DfeLoteListagem](docs/DfeLoteListagem.md)
 - [DfePedidoEnvioEmail](docs/DfePedidoEnvioEmail.md)
 - [DfePedidoInutilizacao](docs/DfePedidoInutilizacao.md)
 - [DfeRecibo](docs/DfeRecibo.md)
 - [DfeRequisicaoDebug](docs/DfeRequisicaoDebug.md)
 - [DfeSefazStatus](docs/DfeSefazStatus.md)
 - [DfeSincronizacao](docs/DfeSincronizacao.md)
 - [DistribuicaoNfe](docs/DistribuicaoNfe.md)
 - [DistribuicaoNfeDocumento](docs/DistribuicaoNfeDocumento.md)
 - [DistribuicaoNfeDocumentoListagem](docs/DistribuicaoNfeDocumentoListagem.md)
 - [DistribuicaoNfeEvento](docs/DistribuicaoNfeEvento.md)
 - [DistribuicaoNfeListagem](docs/DistribuicaoNfeListagem.md)
 - [DistribuicaoNfeNota](docs/DistribuicaoNfeNota.md)
 - [DistribuicaoNfeNotaListagem](docs/DistribuicaoNfeNotaListagem.md)
 - [DistribuicaoNfePedido](docs/DistribuicaoNfePedido.md)
 - [DistribuicaoNfePedidoManifestacao](docs/DistribuicaoNfePedidoManifestacao.md)
 - [DocDedRed](docs/DocDedRed.md)
 - [DocNFNFS](docs/DocNFNFS.md)
 - [DocOutNFSe](docs/DocOutNFSe.md)
 - [Email](docs/Email.md)
 - [EmailAttachment](docs/EmailAttachment.md)
 - [EmailEvent](docs/EmailEvent.md)
 - [EmailListagem](docs/EmailListagem.md)
 - [EmailResumo](docs/EmailResumo.md)
 - [EmailStatusResponse](docs/EmailStatusResponse.md)
 - [Empresa](docs/Empresa.md)
 - [EmpresaCertificado](docs/EmpresaCertificado.md)
 - [EmpresaCertificadoListagem](docs/EmpresaCertificadoListagem.md)
 - [EmpresaConfigCte](docs/EmpresaConfigCte.md)
 - [EmpresaConfigCteOs](docs/EmpresaConfigCteOs.md)
 - [EmpresaConfigDce](docs/EmpresaConfigDce.md)
 - [EmpresaConfigDistribuicaoNfe](docs/EmpresaConfigDistribuicaoNfe.md)
 - [EmpresaConfigMdfe](docs/EmpresaConfigMdfe.md)
 - [EmpresaConfigNfce](docs/EmpresaConfigNfce.md)
 - [EmpresaConfigNfceSefaz](docs/EmpresaConfigNfceSefaz.md)
 - [EmpresaConfigNfcom](docs/EmpresaConfigNfcom.md)
 - [EmpresaConfigNfe](docs/EmpresaConfigNfe.md)
 - [EmpresaConfigNfse](docs/EmpresaConfigNfse.md)
 - [EmpresaConfigNfseRegTrib](docs/EmpresaConfigNfseRegTrib.md)
 - [EmpresaConfigPrefeitura](docs/EmpresaConfigPrefeitura.md)
 - [EmpresaConfigRps](docs/EmpresaConfigRps.md)
 - [EmpresaEndereco](docs/EmpresaEndereco.md)
 - [EmpresaListagem](docs/EmpresaListagem.md)
 - [EmpresaPedidoCadastroCertificado](docs/EmpresaPedidoCadastroCertificado.md)
 - [EnderExt](docs/EnderExt.md)
 - [EnderExtSimples](docs/EnderExtSimples.md)
 - [EnderNac](docs/EnderNac.md)
 - [EnderObraEvento](docs/EnderObraEvento.md)
 - [Endereco](docs/Endereco.md)
 - [EnderecoEmail](docs/EnderecoEmail.md)
 - [EnderecoSimples](docs/EnderecoSimples.md)
 - [ExigSuspensa](docs/ExigSuspensa.md)
 - [HttpRequestDebug](docs/HttpRequestDebug.md)
 - [InfDPS](docs/InfDPS.md)
 - [InfoCompl](docs/InfoCompl.md)
 - [InfoDedRed](docs/InfoDedRed.md)
 - [InfoFornecDocDedRed](docs/InfoFornecDocDedRed.md)
 - [InfoIntermediario](docs/InfoIntermediario.md)
 - [InfoItemPed](docs/InfoItemPed.md)
 - [InfoObra](docs/InfoObra.md)
 - [InfoPrestador](docs/InfoPrestador.md)
 - [InfoRefNFSe](docs/InfoRefNFSe.md)
 - [InfoTomador](docs/InfoTomador.md)
 - [InfoTributacao](docs/InfoTributacao.md)
 - [InfoValores](docs/InfoValores.md)
 - [ListaDocDedRed](docs/ListaDocDedRed.md)
 - [LocPrest](docs/LocPrest.md)
 - [ManifestacaoNfeListagem](docs/ManifestacaoNfeListagem.md)
 - [MdfeDocumentoVinculado](docs/MdfeDocumentoVinculado.md)
 - [MdfeEncerramento](docs/MdfeEncerramento.md)
 - [MdfeInclusaoCondutor](docs/MdfeInclusaoCondutor.md)
 - [MdfeInclusaoDfe](docs/MdfeInclusaoDfe.md)
 - [MdfeNaoEncerrado](docs/MdfeNaoEncerrado.md)
 - [MdfeNaoEncerrados](docs/MdfeNaoEncerrados.md)
 - [MdfePedidoCancelamento](docs/MdfePedidoCancelamento.md)
 - [MdfePedidoEmissao](docs/MdfePedidoEmissao.md)
 - [MdfePedidoEmissaoLote](docs/MdfePedidoEmissaoLote.md)
 - [MdfePedidoEncerramento](docs/MdfePedidoEncerramento.md)
 - [MdfePedidoInclusaoCondutor](docs/MdfePedidoInclusaoCondutor.md)
 - [MdfePedidoInclusaoDfe](docs/MdfePedidoInclusaoDfe.md)
 - [MdfeSefazAereo](docs/MdfeSefazAereo.md)
 - [MdfeSefazAquav](docs/MdfeSefazAquav.md)
 - [MdfeSefazAutXML](docs/MdfeSefazAutXML.md)
 - [MdfeSefazComp](docs/MdfeSefazComp.md)
 - [MdfeSefazCondutor](docs/MdfeSefazCondutor.md)
 - [MdfeSefazDisp](docs/MdfeSefazDisp.md)
 - [MdfeSefazEmit](docs/MdfeSefazEmit.md)
 - [MdfeSefazEndeEmi](docs/MdfeSefazEndeEmi.md)
 - [MdfeSefazFerrov](docs/MdfeSefazFerrov.md)
 - [MdfeSefazIde](docs/MdfeSefazIde.md)
 - [MdfeSefazInfANTT](docs/MdfeSefazInfANTT.md)
 - [MdfeSefazInfAdic](docs/MdfeSefazInfAdic.md)
 - [MdfeSefazInfBanc](docs/MdfeSefazInfBanc.md)
 - [MdfeSefazInfCIOT](docs/MdfeSefazInfCIOT.md)
 - [MdfeSefazInfCTe](docs/MdfeSefazInfCTe.md)
 - [MdfeSefazInfContratante](docs/MdfeSefazInfContratante.md)
 - [MdfeSefazInfContrato](docs/MdfeSefazInfContrato.md)
 - [MdfeSefazInfDoc](docs/MdfeSefazInfDoc.md)
 - [MdfeSefazInfEmbComb](docs/MdfeSefazInfEmbComb.md)
 - [MdfeSefazInfEntregaParcial](docs/MdfeSefazInfEntregaParcial.md)
 - [MdfeSefazInfLocalCarrega](docs/MdfeSefazInfLocalCarrega.md)
 - [MdfeSefazInfLocalDescarrega](docs/MdfeSefazInfLocalDescarrega.md)
 - [MdfeSefazInfLotacao](docs/MdfeSefazInfLotacao.md)
 - [MdfeSefazInfMDFe](docs/MdfeSefazInfMDFe.md)
 - [MdfeSefazInfMDFeSupl](docs/MdfeSefazInfMDFeSupl.md)
 - [MdfeSefazInfMDFeTransp](docs/MdfeSefazInfMDFeTransp.md)
 - [MdfeSefazInfMDFeTranspPeri](docs/MdfeSefazInfMDFeTranspPeri.md)
 - [MdfeSefazInfModal](docs/MdfeSefazInfModal.md)
 - [MdfeSefazInfMunCarrega](docs/MdfeSefazInfMunCarrega.md)
 - [MdfeSefazInfMunDescarga](docs/MdfeSefazInfMunDescarga.md)
 - [MdfeSefazInfNFe](docs/MdfeSefazInfNFe.md)
 - [MdfeSefazInfNFePeri](docs/MdfeSefazInfNFePeri.md)
 - [MdfeSefazInfNFePrestParcial](docs/MdfeSefazInfNFePrestParcial.md)
 - [MdfeSefazInfPag](docs/MdfeSefazInfPag.md)
 - [MdfeSefazInfPercurso](docs/MdfeSefazInfPercurso.md)
 - [MdfeSefazInfPrazo](docs/MdfeSefazInfPrazo.md)
 - [MdfeSefazInfResp](docs/MdfeSefazInfResp.md)
 - [MdfeSefazInfSeg](docs/MdfeSefazInfSeg.md)
 - [MdfeSefazInfSolicNFF](docs/MdfeSefazInfSolicNFF.md)
 - [MdfeSefazInfTermCarreg](docs/MdfeSefazInfTermCarreg.md)
 - [MdfeSefazInfTermDescarreg](docs/MdfeSefazInfTermDescarreg.md)
 - [MdfeSefazInfUnidCargaVazia](docs/MdfeSefazInfUnidCargaVazia.md)
 - [MdfeSefazInfUnidTranspVazia](docs/MdfeSefazInfUnidTranspVazia.md)
 - [MdfeSefazLacRodo](docs/MdfeSefazLacRodo.md)
 - [MdfeSefazLacUnidCarga](docs/MdfeSefazLacUnidCarga.md)
 - [MdfeSefazLacUnidTransp](docs/MdfeSefazLacUnidTransp.md)
 - [MdfeSefazLacres](docs/MdfeSefazLacres.md)
 - [MdfeSefazPeri](docs/MdfeSefazPeri.md)
 - [MdfeSefazProdPred](docs/MdfeSefazProdPred.md)
 - [MdfeSefazProp](docs/MdfeSefazProp.md)
 - [MdfeSefazRespTec](docs/MdfeSefazRespTec.md)
 - [MdfeSefazRodo](docs/MdfeSefazRodo.md)
 - [MdfeSefazSeg](docs/MdfeSefazSeg.md)
 - [MdfeSefazTot](docs/MdfeSefazTot.md)
 - [MdfeSefazTrem](docs/MdfeSefazTrem.md)
 - [MdfeSefazUnidCarga](docs/MdfeSefazUnidCarga.md)
 - [MdfeSefazUnidadeTransp](docs/MdfeSefazUnidadeTransp.md)
 - [MdfeSefazVag](docs/MdfeSefazVag.md)
 - [MdfeSefazValePed](docs/MdfeSefazValePed.md)
 - [MdfeSefazVeicReboque](docs/MdfeSefazVeicReboque.md)
 - [MdfeSefazVeicReboqueProp](docs/MdfeSefazVeicReboqueProp.md)
 - [MdfeSefazVeicTracao](docs/MdfeSefazVeicTracao.md)
 - [NfcomPedidoCancelamento](docs/NfcomPedidoCancelamento.md)
 - [NfcomPedidoEmissao](docs/NfcomPedidoEmissao.md)
 - [NfcomSefazALCZFMCBS](docs/NfcomSefazALCZFMCBS.md)
 - [NfcomSefazAssinante](docs/NfcomSefazAssinante.md)
 - [NfcomSefazAutXML](docs/NfcomSefazAutXML.md)
 - [NfcomSefazCIBS](docs/NfcomSefazCIBS.md)
 - [NfcomSefazCOFINS](docs/NfcomSefazCOFINS.md)
 - [NfcomSefazCompraGovReduzido](docs/NfcomSefazCompraGovReduzido.md)
 - [NfcomSefazDest](docs/NfcomSefazDest.md)
 - [NfcomSefazDet](docs/NfcomSefazDet.md)
 - [NfcomSefazDevTrib](docs/NfcomSefazDevTrib.md)
 - [NfcomSefazDif](docs/NfcomSefazDif.md)
 - [NfcomSefazEmit](docs/NfcomSefazEmit.md)
 - [NfcomSefazEndeDest](docs/NfcomSefazEndeDest.md)
 - [NfcomSefazEndeEmi](docs/NfcomSefazEndeEmi.md)
 - [NfcomSefazEstornoCred](docs/NfcomSefazEstornoCred.md)
 - [NfcomSefazFUNTTEL](docs/NfcomSefazFUNTTEL.md)
 - [NfcomSefazFUST](docs/NfcomSefazFUST.md)
 - [NfcomSefazGCBS](docs/NfcomSefazGCBS.md)
 - [NfcomSefazGCofat](docs/NfcomSefazGCofat.md)
 - [NfcomSefazGCofatGNF](docs/NfcomSefazGCofatGNF.md)
 - [NfcomSefazGEstornoCred](docs/NfcomSefazGEstornoCred.md)
 - [NfcomSefazGFat](docs/NfcomSefazGFat.md)
 - [NfcomSefazGFatCentral](docs/NfcomSefazGFatCentral.md)
 - [NfcomSefazGFidelidade](docs/NfcomSefazGFidelidade.md)
 - [NfcomSefazGIBS](docs/NfcomSefazGIBS.md)
 - [NfcomSefazGIBSGIBSMun](docs/NfcomSefazGIBSGIBSMun.md)
 - [NfcomSefazGIBSGIBSUF](docs/NfcomSefazGIBSGIBSUF.md)
 - [NfcomSefazGIBSMun](docs/NfcomSefazGIBSMun.md)
 - [NfcomSefazGIBSUF](docs/NfcomSefazGIBSUF.md)
 - [NfcomSefazGNF](docs/NfcomSefazGNF.md)
 - [NfcomSefazGPIX](docs/NfcomSefazGPIX.md)
 - [NfcomSefazGPagAntecipado](docs/NfcomSefazGPagAntecipado.md)
 - [NfcomSefazGProc](docs/NfcomSefazGProc.md)
 - [NfcomSefazGProcRef](docs/NfcomSefazGProcRef.md)
 - [NfcomSefazGRessarc](docs/NfcomSefazGRessarc.md)
 - [NfcomSefazGSub](docs/NfcomSefazGSub.md)
 - [NfcomSefazIBSCBSTot](docs/NfcomSefazIBSCBSTot.md)
 - [NfcomSefazIBSCBSTotGCBS](docs/NfcomSefazIBSCBSTotGCBS.md)
 - [NfcomSefazICMS00](docs/NfcomSefazICMS00.md)
 - [NfcomSefazICMS20](docs/NfcomSefazICMS20.md)
 - [NfcomSefazICMS40](docs/NfcomSefazICMS40.md)
 - [NfcomSefazICMS51](docs/NfcomSefazICMS51.md)
 - [NfcomSefazICMS90](docs/NfcomSefazICMS90.md)
 - [NfcomSefazICMSSN](docs/NfcomSefazICMSSN.md)
 - [NfcomSefazICMSTot](docs/NfcomSefazICMSTot.md)
 - [NfcomSefazICMSUFDest](docs/NfcomSefazICMSUFDest.md)
 - [NfcomSefazIde](docs/NfcomSefazIde.md)
 - [NfcomSefazImposto](docs/NfcomSefazImposto.md)
 - [NfcomSefazInfAdic](docs/NfcomSefazInfAdic.md)
 - [NfcomSefazInfNFCom](docs/NfcomSefazInfNFCom.md)
 - [NfcomSefazPIS](docs/NfcomSefazPIS.md)
 - [NfcomSefazPagamentoRTC](docs/NfcomSefazPagamentoRTC.md)
 - [NfcomSefazPgtoVinc](docs/NfcomSefazPgtoVinc.md)
 - [NfcomSefazProd](docs/NfcomSefazProd.md)
 - [NfcomSefazRed](docs/NfcomSefazRed.md)
 - [NfcomSefazRespTec](docs/NfcomSefazRespTec.md)
 - [NfcomSefazRetTrib](docs/NfcomSefazRetTrib.md)
 - [NfcomSefazTotal](docs/NfcomSefazTotal.md)
 - [NfcomSefazTribCompraGov](docs/NfcomSefazTribCompraGov.md)
 - [NfcomSefazTribNFCom](docs/NfcomSefazTribNFCom.md)
 - [NfcomSefazTribRegular](docs/NfcomSefazTribRegular.md)
 - [NfcomSefazVRetTribTot](docs/NfcomSefazVRetTribTot.md)
 - [NfePedidoCancelamento](docs/NfePedidoCancelamento.md)
 - [NfePedidoCartaCorrecao](docs/NfePedidoCartaCorrecao.md)
 - [NfePedidoEmissao](docs/NfePedidoEmissao.md)
 - [NfePedidoEmissaoLote](docs/NfePedidoEmissaoLote.md)
 - [NfeSefazALCZFMCBSNFe](docs/NfeSefazALCZFMCBSNFe.md)
 - [NfeSefazAdi](docs/NfeSefazAdi.md)
 - [NfeSefazAgropecuario](docs/NfeSefazAgropecuario.md)
 - [NfeSefazAjusteCompet](docs/NfeSefazAjusteCompet.md)
 - [NfeSefazArma](docs/NfeSefazArma.md)
 - [NfeSefazAutXML](docs/NfeSefazAutXML.md)
 - [NfeSefazAvulsa](docs/NfeSefazAvulsa.md)
 - [NfeSefazCIBSNFe](docs/NfeSefazCIBSNFe.md)
 - [NfeSefazCIDE](docs/NfeSefazCIDE.md)
 - [NfeSefazCOFINS](docs/NfeSefazCOFINS.md)
 - [NfeSefazCOFINSAliq](docs/NfeSefazCOFINSAliq.md)
 - [NfeSefazCOFINSNT](docs/NfeSefazCOFINSNT.md)
 - [NfeSefazCOFINSOutr](docs/NfeSefazCOFINSOutr.md)
 - [NfeSefazCOFINSQtde](docs/NfeSefazCOFINSQtde.md)
 - [NfeSefazCOFINSST](docs/NfeSefazCOFINSST.md)
 - [NfeSefazCana](docs/NfeSefazCana.md)
 - [NfeSefazCard](docs/NfeSefazCard.md)
 - [NfeSefazCobr](docs/NfeSefazCobr.md)
 - [NfeSefazComb](docs/NfeSefazComb.md)
 - [NfeSefazCompra](docs/NfeSefazCompra.md)
 - [NfeSefazCompraGov](docs/NfeSefazCompraGov.md)
 - [NfeSefazCredPres](docs/NfeSefazCredPres.md)
 - [NfeSefazCredPresIBSZFM](docs/NfeSefazCredPresIBSZFM.md)
 - [NfeSefazCredPresOper](docs/NfeSefazCredPresOper.md)
 - [NfeSefazDFeReferenciado](docs/NfeSefazDFeReferenciado.md)
 - [NfeSefazDI](docs/NfeSefazDI.md)
 - [NfeSefazDeduc](docs/NfeSefazDeduc.md)
 - [NfeSefazDefensivo](docs/NfeSefazDefensivo.md)
 - [NfeSefazDest](docs/NfeSefazDest.md)
 - [NfeSefazDet](docs/NfeSefazDet.md)
 - [NfeSefazDetExport](docs/NfeSefazDetExport.md)
 - [NfeSefazDetPag](docs/NfeSefazDetPag.md)
 - [NfeSefazDevTrib](docs/NfeSefazDevTrib.md)
 - [NfeSefazDif](docs/NfeSefazDif.md)
 - [NfeSefazDup](docs/NfeSefazDup.md)
 - [NfeSefazEmit](docs/NfeSefazEmit.md)
 - [NfeSefazEncerrante](docs/NfeSefazEncerrante.md)
 - [NfeSefazEnderEmi](docs/NfeSefazEnderEmi.md)
 - [NfeSefazEndereco](docs/NfeSefazEndereco.md)
 - [NfeSefazEstornoCred](docs/NfeSefazEstornoCred.md)
 - [NfeSefazExportInd](docs/NfeSefazExportInd.md)
 - [NfeSefazExporta](docs/NfeSefazExporta.md)
 - [NfeSefazFat](docs/NfeSefazFat.md)
 - [NfeSefazForDia](docs/NfeSefazForDia.md)
 - [NfeSefazGCBS](docs/NfeSefazGCBS.md)
 - [NfeSefazGCred](docs/NfeSefazGCred.md)
 - [NfeSefazGEstornoCred](docs/NfeSefazGEstornoCred.md)
 - [NfeSefazGIBS](docs/NfeSefazGIBS.md)
 - [NfeSefazGIBSGIBSMun](docs/NfeSefazGIBSGIBSMun.md)
 - [NfeSefazGIBSGIBSUF](docs/NfeSefazGIBSGIBSUF.md)
 - [NfeSefazGIBSMun](docs/NfeSefazGIBSMun.md)
 - [NfeSefazGIBSUF](docs/NfeSefazGIBSUF.md)
 - [NfeSefazGMono](docs/NfeSefazGMono.md)
 - [NfeSefazGMonoDif](docs/NfeSefazGMonoDif.md)
 - [NfeSefazGMonoPadrao](docs/NfeSefazGMonoPadrao.md)
 - [NfeSefazGMonoRet](docs/NfeSefazGMonoRet.md)
 - [NfeSefazGMonoReten](docs/NfeSefazGMonoReten.md)
 - [NfeSefazGPagAntecipado](docs/NfeSefazGPagAntecipado.md)
 - [NfeSefazGuiaTransito](docs/NfeSefazGuiaTransito.md)
 - [NfeSefazIBSCBSMonoTot](docs/NfeSefazIBSCBSMonoTot.md)
 - [NfeSefazIBSCBSMonoTotGCBS](docs/NfeSefazIBSCBSMonoTotGCBS.md)
 - [NfeSefazICMS](docs/NfeSefazICMS.md)
 - [NfeSefazICMS00](docs/NfeSefazICMS00.md)
 - [NfeSefazICMS02](docs/NfeSefazICMS02.md)
 - [NfeSefazICMS10](docs/NfeSefazICMS10.md)
 - [NfeSefazICMS15](docs/NfeSefazICMS15.md)
 - [NfeSefazICMS20](docs/NfeSefazICMS20.md)
 - [NfeSefazICMS30](docs/NfeSefazICMS30.md)
 - [NfeSefazICMS40](docs/NfeSefazICMS40.md)
 - [NfeSefazICMS51](docs/NfeSefazICMS51.md)
 - [NfeSefazICMS53](docs/NfeSefazICMS53.md)
 - [NfeSefazICMS60](docs/NfeSefazICMS60.md)
 - [NfeSefazICMS61](docs/NfeSefazICMS61.md)
 - [NfeSefazICMS70](docs/NfeSefazICMS70.md)
 - [NfeSefazICMS90](docs/NfeSefazICMS90.md)
 - [NfeSefazICMSPart](docs/NfeSefazICMSPart.md)
 - [NfeSefazICMSSN101](docs/NfeSefazICMSSN101.md)
 - [NfeSefazICMSSN102](docs/NfeSefazICMSSN102.md)
 - [NfeSefazICMSSN201](docs/NfeSefazICMSSN201.md)
 - [NfeSefazICMSSN202](docs/NfeSefazICMSSN202.md)
 - [NfeSefazICMSSN500](docs/NfeSefazICMSSN500.md)
 - [NfeSefazICMSSN900](docs/NfeSefazICMSSN900.md)
 - [NfeSefazICMSST](docs/NfeSefazICMSST.md)
 - [NfeSefazICMSTot](docs/NfeSefazICMSTot.md)
 - [NfeSefazICMSUFDest](docs/NfeSefazICMSUFDest.md)
 - [NfeSefazII](docs/NfeSefazII.md)
 - [NfeSefazIPINT](docs/NfeSefazIPINT.md)
 - [NfeSefazIPITrib](docs/NfeSefazIPITrib.md)
 - [NfeSefazIS](docs/NfeSefazIS.md)
 - [NfeSefazISSQN](docs/NfeSefazISSQN.md)
 - [NfeSefazISSQNtot](docs/NfeSefazISSQNtot.md)
 - [NfeSefazISTot](docs/NfeSefazISTot.md)
 - [NfeSefazIde](docs/NfeSefazIde.md)
 - [NfeSefazImposto](docs/NfeSefazImposto.md)
 - [NfeSefazImpostoDevol](docs/NfeSefazImpostoDevol.md)
 - [NfeSefazImpostoDevolIPI](docs/NfeSefazImpostoDevolIPI.md)
 - [NfeSefazInfAdic](docs/NfeSefazInfAdic.md)
 - [NfeSefazInfAdicObsCont](docs/NfeSefazInfAdicObsCont.md)
 - [NfeSefazInfAdicObsFisco](docs/NfeSefazInfAdicObsFisco.md)
 - [NfeSefazInfIntermed](docs/NfeSefazInfIntermed.md)
 - [NfeSefazInfNFe](docs/NfeSefazInfNFe.md)
 - [NfeSefazInfNFeSupl](docs/NfeSefazInfNFeSupl.md)
 - [NfeSefazInfPAA](docs/NfeSefazInfPAA.md)
 - [NfeSefazInfProdEmb](docs/NfeSefazInfProdEmb.md)
 - [NfeSefazInfProdNFF](docs/NfeSefazInfProdNFF.md)
 - [NfeSefazInfRespTec](docs/NfeSefazInfRespTec.md)
 - [NfeSefazInfSolicNFF](docs/NfeSefazInfSolicNFF.md)
 - [NfeSefazIpi](docs/NfeSefazIpi.md)
 - [NfeSefazLacres](docs/NfeSefazLacres.md)
 - [NfeSefazLocal](docs/NfeSefazLocal.md)
 - [NfeSefazMed](docs/NfeSefazMed.md)
 - [NfeSefazMonofasia](docs/NfeSefazMonofasia.md)
 - [NfeSefazNFref](docs/NfeSefazNFref.md)
 - [NfeSefazObsCont](docs/NfeSefazObsCont.md)
 - [NfeSefazObsFisco](docs/NfeSefazObsFisco.md)
 - [NfeSefazObsItem](docs/NfeSefazObsItem.md)
 - [NfeSefazOrigComb](docs/NfeSefazOrigComb.md)
 - [NfeSefazPAASignature](docs/NfeSefazPAASignature.md)
 - [NfeSefazPIS](docs/NfeSefazPIS.md)
 - [NfeSefazPISAliq](docs/NfeSefazPISAliq.md)
 - [NfeSefazPISNT](docs/NfeSefazPISNT.md)
 - [NfeSefazPISOutr](docs/NfeSefazPISOutr.md)
 - [NfeSefazPISQtde](docs/NfeSefazPISQtde.md)
 - [NfeSefazPISST](docs/NfeSefazPISST.md)
 - [NfeSefazPag](docs/NfeSefazPag.md)
 - [NfeSefazProcRef](docs/NfeSefazProcRef.md)
 - [NfeSefazProd](docs/NfeSefazProd.md)
 - [NfeSefazRSAKeyValueType](docs/NfeSefazRSAKeyValueType.md)
 - [NfeSefazRastro](docs/NfeSefazRastro.md)
 - [NfeSefazRed](docs/NfeSefazRed.md)
 - [NfeSefazRefECF](docs/NfeSefazRefECF.md)
 - [NfeSefazRefNF](docs/NfeSefazRefNF.md)
 - [NfeSefazRefNFP](docs/NfeSefazRefNFP.md)
 - [NfeSefazRetTransp](docs/NfeSefazRetTransp.md)
 - [NfeSefazRetTrib](docs/NfeSefazRetTrib.md)
 - [NfeSefazTotal](docs/NfeSefazTotal.md)
 - [NfeSefazTransfCred](docs/NfeSefazTransfCred.md)
 - [NfeSefazTransp](docs/NfeSefazTransp.md)
 - [NfeSefazTransporta](docs/NfeSefazTransporta.md)
 - [NfeSefazTribCompraGov](docs/NfeSefazTribCompraGov.md)
 - [NfeSefazTribNFe](docs/NfeSefazTribNFe.md)
 - [NfeSefazTribRegular](docs/NfeSefazTribRegular.md)
 - [NfeSefazVeicProd](docs/NfeSefazVeicProd.md)
 - [NfeSefazVeiculo](docs/NfeSefazVeiculo.md)
 - [NfeSefazVol](docs/NfeSefazVol.md)
 - [Nfse](docs/Nfse.md)
 - [NfseCancelamento](docs/NfseCancelamento.md)
 - [NfseCidadeMetadados](docs/NfseCidadeMetadados.md)
 - [NfseCidadesAtendidas](docs/NfseCidadesAtendidas.md)
 - [NfseDpsPedidoEmissao](docs/NfseDpsPedidoEmissao.md)
 - [NfseListagem](docs/NfseListagem.md)
 - [NfseLoteDpsPedidoEmissao](docs/NfseLoteDpsPedidoEmissao.md)
 - [NfseMensagemRetorno](docs/NfseMensagemRetorno.md)
 - [NfsePedidoCancelamento](docs/NfsePedidoCancelamento.md)
 - [NfsePedidoEmissao](docs/NfsePedidoEmissao.md)
 - [NfsePedidoSincronizacao](docs/NfsePedidoSincronizacao.md)
 - [NfseSincronizacao](docs/NfseSincronizacao.md)
 - [RTCInfoDest](docs/RTCInfoDest.md)
 - [RTCInfoIBSCBS](docs/RTCInfoIBSCBS.md)
 - [RTCInfoImovel](docs/RTCInfoImovel.md)
 - [RTCInfoReeRepRes](docs/RTCInfoReeRepRes.md)
 - [RTCInfoTributosDif](docs/RTCInfoTributosDif.md)
 - [RTCInfoTributosIBSCBS](docs/RTCInfoTributosIBSCBS.md)
 - [RTCInfoTributosSitClas](docs/RTCInfoTributosSitClas.md)
 - [RTCInfoTributosTribRegular](docs/RTCInfoTributosTribRegular.md)
 - [RTCInfoValoresIBSCBS](docs/RTCInfoValoresIBSCBS.md)
 - [RTCListaDoc](docs/RTCListaDoc.md)
 - [RTCListaDocDFe](docs/RTCListaDocDFe.md)
 - [RTCListaDocFiscalOutro](docs/RTCListaDocFiscalOutro.md)
 - [RTCListaDocFornec](docs/RTCListaDocFornec.md)
 - [RTCListaDocOutro](docs/RTCListaDocOutro.md)
 - [RegTrib](docs/RegTrib.md)
 - [Rps](docs/Rps.md)
 - [RpsDados](docs/RpsDados.md)
 - [RpsDadosConstrucaoCivil](docs/RpsDadosConstrucaoCivil.md)
 - [RpsDadosIntermediario](docs/RpsDadosIntermediario.md)
 - [RpsDadosPrestador](docs/RpsDadosPrestador.md)
 - [RpsDadosServico](docs/RpsDadosServico.md)
 - [RpsDadosTomador](docs/RpsDadosTomador.md)
 - [RpsDadosTomadorEndereco](docs/RpsDadosTomadorEndereco.md)
 - [RpsIdentificacao](docs/RpsIdentificacao.md)
 - [RpsIdentificacaoPrestador](docs/RpsIdentificacaoPrestador.md)
 - [RpsLote](docs/RpsLote.md)
 - [RpsLoteListagem](docs/RpsLoteListagem.md)
 - [RpsPedidoEmissao](docs/RpsPedidoEmissao.md)
 - [RpsPedidoEmissaoLote](docs/RpsPedidoEmissaoLote.md)
 - [RpsServicoValores](docs/RpsServicoValores.md)
 - [Serv](docs/Serv.md)
 - [Substituicao](docs/Substituicao.md)
 - [TribFederal](docs/TribFederal.md)
 - [TribMunicipal](docs/TribMunicipal.md)
 - [TribOutrosPisCofins](docs/TribOutrosPisCofins.md)
 - [TribTotal](docs/TribTotal.md)
 - [TribTotalMonet](docs/TribTotalMonet.md)
 - [TribTotalPercent](docs/TribTotalPercent.md)
 - [VDescCondIncond](docs/VDescCondIncond.md)
 - [VServPrest](docs/VServPrest.md)


## Documentação de autorização


## oauth2

- **Tipo**: OAuth
- **Fluxo**: application
- **URL de autorização**: 
- **Escopos**: 
 - **conta**: 
 - **empresa**: 
 - **cep**: 
 - **cnpj**: 
 - **mdfe**: 
 - **cte**: 
 - **nfse**: 
 - **nfe**: 


## Autor




