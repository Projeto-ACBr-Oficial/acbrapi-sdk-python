# DfeContribuinteInfCons

Dados do Resultado do Dados do Pedido de Consulta de cadastro de contribuintes.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**codigo_status** | **int** | Código do status da mensagem enviada. | 
**motivo_status** | **str** | Descrição literal do status do serviço solicitado. | 
**uf** | **str** | sigla da UF consultada, utilizar SU para SUFRAMA. | 
**ie** | **str** | Inscrição Estadual do contribuinte. | [optional] 
**cnpj** | **str** | CNPJ do contribuinte. | [optional] 
**cpf** | **str** | CPF do contribuinte. | [optional] 
**data_consulta** | **datetime** | Data da Consulta. | 
**uf_atendimento** | **int** | código da UF de atendimento. | 
**informacoes_cadastrais** | [**list[DfeContribuinteInfCad]**](DfeContribuinteInfCad.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


