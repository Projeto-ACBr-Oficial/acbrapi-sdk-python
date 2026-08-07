# DfeContribuinteInfCons

Dados do Resultado do Dados do Pedido de Consulta de cadastro de contribuintes.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**codigo_status** | **int** | Código do status da mensagem enviada. | 
**motivo_status** | **str** | Descrição literal do status do serviço solicitado. | 
**uf** | **str** | sigla da UF consultada, utilizar SU para SUFRAMA. | 
**ie** | **str** | Inscrição Estadual do contribuinte. | [opcional] 
**cnpj** | **str** | CNPJ do contribuinte. | [opcional] 
**cpf** | **str** | CPF do contribuinte. | [opcional] 
**data_consulta** | **datetime** | Data da Consulta. | 
**uf_atendimento** | **int** | código da UF de atendimento. | 
**informacoes_cadastrais** | [**list[DfeContribuinteInfCad]**](DfeContribuinteInfCad.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


