# CnpjEmpresa


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número de inscrição do CNPJ. | [optional] 
**razao_social** | **str** | Nome empresarial da pessoa jurídica. | [optional] 
**nome_fantasia** | **str** | Corresponde ao nome fantasia. | [optional] 
**data_inicio_atividade** | **date** | Data de início da atividade. | [optional] 
**matriz** | **bool** | Indicador de matriz/filial:  * &#x60;true&#x60; - É matriz  * &#x60;false&#x60; - É filial | [optional] 
**natureza_juridica** | [**CnpjNaturezaJuridica**](CnpjNaturezaJuridica.md) |  | [optional] 
**capital_social** | **float** | Capital social da empresa. | [optional] 
**porte** | [**CnpjPorteEmpresa**](CnpjPorteEmpresa.md) |  | [optional] 
**ente_federativo_responsavel** | **str** | O ente federativo responsável é preenchido para os casos de órgãos e  entidades do grupo de natureza jurídica 1XXX. Para as demais naturezas,  este atributo fica em branco. | [optional] 
**situacao_cadastral** | [**CnpjSituacaoCadastral**](CnpjSituacaoCadastral.md) |  | [optional] 
**motivo_situacao_cadastral** | [**CnpjMotivoSituacaoCadastral**](CnpjMotivoSituacaoCadastral.md) |  | [optional] 
**nome_da_cidade_no_exterior** | **str** | Nome da cidade no exterior. | [optional] 
**pais** | [**CnpjPais**](CnpjPais.md) |  | [optional] 
**atividade_principal** | [**CnpjCnae**](CnpjCnae.md) |  | [optional] 
**atividades_secundarias** | [**list[CnpjCnaeSecundario]**](CnpjCnaeSecundario.md) |  | [optional] 
**endereco** | [**CnpjEndereco**](CnpjEndereco.md) |  | [optional] 
**telefones** | [**list[CnpjTelefone]**](CnpjTelefone.md) |  | [optional] 
**email** | **str** | E-mail do contribuinte. | [optional] 
**situacao_especial** | [**CnpjSituacaoEspecial**](CnpjSituacaoEspecial.md) |  | [optional] 
**simples** | [**CnpjOpcaoSimples**](CnpjOpcaoSimples.md) |  | [optional] 
**simei** | [**CnpjOpcaoSimei**](CnpjOpcaoSimei.md) |  | [optional] 
**socios** | [**list[CnpjSocio]**](CnpjSocio.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


