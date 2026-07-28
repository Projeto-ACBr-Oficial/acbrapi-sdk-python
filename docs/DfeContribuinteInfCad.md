# DfeContribuinteInfCad

Informações cadastrais do contribuinte consultado.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ie** | **str** | Número da Inscrição Estadual do contribuinte. | 
**cnpj** | **str** | Número do CNPJ  do contribuinte. | [optional] 
**cpf** | **str** | Número do CPF do contribuinte. | [optional] 
**uf** | **str** | Sigla da UF de localização do contribuinte. Em algumas situações, a UF de localização pode ser diferente da UF consultada. Ex. IE de Substituto Tributário. | 
**situacao_cadastral** | **int** | Situação cadastral do contribuinte:  * 0 - não habilitado  * 1 - habilitado | 
**indicador_nfe** | **int** | Indicador de contribuinte credenciado a emitir NF-e.  * 0 - Não credenciado para emissão da NF-e  * 1 - Credenciado  * 2 - Credenciado com obrigatoriedade para todas operações  * 3 - Credenciado com obrigatoriedade parcial  * 4 - a SEFAZ não fornece a informação  Este indicador significa apenas que o contribuinte é credenciado para emitir NF-e na SEFAZ consultada. | 
**indicador_cte** | **int** | Indicador de contribuinte credenciado a emitir CT-e.  * 0 - Não credenciado para emissão da CT-e  * 1 - Credenciado  * 2 - Credenciado com obrigatoriedade para todas operações  * 3 - Credenciado com obrigatoriedade parcial  * 4 - a SEFAZ não fornece a informação  Este indicador significa apenas que o contribuinte é credenciado para emitir CT-e na SEFAZ consultada. | 
**nome_razao_social** | **str** | Razão Social ou nome do contribuinte. | 
**nome_fantasia** | **str** | Razão Social ou nome do contribuinte. | [optional] 
**regime_apuracao_icms** | **str** | Regime de Apuração do ICMS. | [optional] 
**cnae** | **str** | CNAE Fiscal do contribuinte. | [optional] 
**data_inicio_atividade** | **date** | Data de início de atividades do contribuinte. | [optional] 
**data_situacao_cadastral** | **date** | Data da última modificação da situação cadastral do contribuinte. | [optional] 
**data_fim_atividade** | **date** | Data de ocorrência da baixa do contribuinte. | [optional] 
**ie_unica** | **str** | Inscrição Estadual Única. | [optional] 
**ie_atual** | **str** | Inscrição Estadual atual. | [optional] 
**endereco** | [**DfeContribuinteEndereco**](DfeContribuinteEndereco.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


