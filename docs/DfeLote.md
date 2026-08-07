# DfeLote


## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**id** | **str** | ID único gerado pela API para este documento. | [opcional] 
**created_at** | **datetime** |  | [opcional] 
**status** | **str** |  | [opcional] 
**ambiente** | **str** |  | [opcional] 
**referencia** | **str** | Seu identificador único para este documento. Opcional, ajuda a evitar o envio duplicado de um mesmo documento. | [opcional] 
**id_lote** | **str** |  | [opcional] 
**recibo** | [**DfeRecibo**](DfeRecibo.md) |  | [opcional] 
**documentos** | [**list[Dfe]**](Dfe.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


