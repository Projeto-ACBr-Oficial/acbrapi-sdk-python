# CnpjEmpresa


## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número de inscrição do CNPJ. | [opcional] 
**razao_social** | **str** | Nome empresarial da pessoa jurídica. | [opcional] 
**nome_fantasia** | **str** | Corresponde ao nome fantasia. | [opcional] 
**data_inicio_atividade** | **date** | Data de início da atividade. | [opcional] 
**matriz** | **bool** | Indicador de matriz/filial:  * &#x60;true&#x60; - É matriz  * &#x60;false&#x60; - É filial | [opcional] 
**natureza_juridica** | [**CnpjNaturezaJuridica**](CnpjNaturezaJuridica.md) |  | [opcional] 
**capital_social** | **float** | Capital social da empresa. | [opcional] 
**porte** | [**CnpjPorteEmpresa**](CnpjPorteEmpresa.md) |  | [opcional] 
**ente_federativo_responsavel** | **str** | O ente federativo responsável é preenchido para os casos de órgãos e  entidades do grupo de natureza jurídica 1XXX. Para as demais naturezas,  este atributo fica em branco. | [opcional] 
**situacao_cadastral** | [**CnpjSituacaoCadastral**](CnpjSituacaoCadastral.md) |  | [opcional] 
**motivo_situacao_cadastral** | [**CnpjMotivoSituacaoCadastral**](CnpjMotivoSituacaoCadastral.md) |  | [opcional] 
**nome_da_cidade_no_exterior** | **str** | Nome da cidade no exterior. | [opcional] 
**pais** | [**CnpjPais**](CnpjPais.md) |  | [opcional] 
**atividade_principal** | [**CnpjCnae**](CnpjCnae.md) |  | [opcional] 
**atividades_secundarias** | [**list[CnpjCnaeSecundario]**](CnpjCnaeSecundario.md) |  | [opcional] 
**endereco** | [**CnpjEndereco**](CnpjEndereco.md) |  | [opcional] 
**telefones** | [**list[CnpjTelefone]**](CnpjTelefone.md) |  | [opcional] 
**email** | **str** | E-mail do contribuinte. | [opcional] 
**situacao_especial** | [**CnpjSituacaoEspecial**](CnpjSituacaoEspecial.md) |  | [opcional] 
**simples** | [**CnpjOpcaoSimples**](CnpjOpcaoSimples.md) |  | [opcional] 
**simei** | [**CnpjOpcaoSimei**](CnpjOpcaoSimei.md) |  | [opcional] 
**socios** | [**list[CnpjSocio]**](CnpjSocio.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


