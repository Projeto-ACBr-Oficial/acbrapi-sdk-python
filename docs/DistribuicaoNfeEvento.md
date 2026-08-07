# DistribuicaoNfeEvento


## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**id** | **str** | ID único gerado pela API para este evento. | [opcional] 
**created_at** | **datetime** | Data/hora em que o evento foi criado na API. Representado no formato &lt;a href&#x3D;\&quot;https://en.wikipedia.org/wiki/ISO_8601\&quot; target&#x3D;\&quot;blank\&quot;&gt;&#x60;ISO 8601&#x60;&lt;/a&gt;. | [opcional] 
**ambiente** | **str** | Identificação do ambiente. | [opcional] 
**status** | **str** | Status do Evento. | [opcional] 
**cpf_cnpj_autor** | **str** | CPF/CNPJ do autor do evento. | [opcional] 
**chave_acesso** | **str** | Chave de Acesso do documento vinculado ao evento. | [opcional] 
**tipo_evento** | **str** | Tipo do evento vinculado. | [opcional] 
**data_evento** | **datetime** | Data e hora do Evento. | [opcional] 
**numero_sequencial** | **int** | Sequencial do evento para o mesmo tipo de evento. | [opcional] 
**justificativa** | **str** | Justificativa para o desconhecimento ou não-realização da operação. | [opcional] 
**data_registro** | **datetime** | Data e hora do registro do evento pela SEFAZ. | [opcional] 
**codigo_status** | **int** | Código do status de registro do evento. | [opcional] 
**motivo_status** | **str** | Descrição literal do status do registro do evento. | [opcional] 
**numero_protocolo** | **str** | Número do Protocolo de registro do evento. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


