# DfeCancelamento


## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**justificativa** | **str** | Justificativa do cancelamento. | [opcional] 
**chave_substituta** | **str** | Chave de acesso da NFC-e substituta. Preenchida apenas no cancelamento  por substituição (evento 110112). | [opcional] 
**id** | **str** | ID único gerado pela API para este evento. | [opcional] 
**ambiente** | **str** | Identificação do ambiente. | [opcional] 
**status** | **str** | Status do Evento. | [opcional] 
**autor** | [**DfeAutorEvento**](DfeAutorEvento.md) |  | [opcional] 
**chave_acesso** | **str** | Chave de Acesso do documento vinculado ao evento. | [opcional] 
**data_evento** | **datetime** | Data e hora do Evento. | [opcional] 
**numero_sequencial** | **int** | Sequencial do evento para o mesmo tipo de evento. | [opcional] 
**data_recebimento** | **datetime** | Data e hora do recebimento do Evento pela SEFAZ. | [opcional] 
**codigo_status** | **int** | Código do status de registro do Evento. | [opcional] 
**motivo_status** | **str** | Descrição literal do status do registro do Evento. | [opcional] 
**numero_protocolo** | **str** | Número do Protocolo de registro do Evento. | [opcional] 
**codigo_mensagem** | **int** | Código da Mensagem. | [opcional] 
**mensagem** | **str** | Mensagem da SEFAZ para o emissor. | [opcional] 
**tipo_evento** | **str** |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


