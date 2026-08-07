# Nfse


## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**id** | **str** | ID único da nota gerado automaticamente pela API. | [opcional] 
**created_at** | **datetime** |  | [opcional] 
**status** | **str** |  | [opcional] 
**numero** | **str** |  | [opcional] 
**codigo_verificacao** | **str** |  | [opcional] 
**link_url** | **str** |  | [opcional] 
**data_emissao** | **datetime** |  | [opcional] 
**ambiente** | **str** |  | [opcional] 
**referencia** | **str** |  | [opcional] 
**dps** | [**DPS**](DPS.md) |  | [opcional] 
**cancelamento** | [**NfseCancelamento**](NfseCancelamento.md) |  | [opcional] 
**mensagens** | [**list[NfseMensagemRetorno]**](NfseMensagemRetorno.md) |  | [opcional] 
**declaracao_prestacao_servico** | [**Rps**](Rps.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


