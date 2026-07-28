# DistribuicaoNfeEvento


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | ID único gerado pela API para este evento. | [optional] 
**created_at** | **datetime** | Data/hora em que o evento foi criado na API. Representado no formato &lt;a href&#x3D;\&quot;https://en.wikipedia.org/wiki/ISO_8601\&quot; target&#x3D;\&quot;blank\&quot;&gt;&#x60;ISO 8601&#x60;&lt;/a&gt;. | [optional] 
**ambiente** | **str** | Identificação do ambiente. | [optional] 
**status** | **str** | Status do Evento. | [optional] 
**cpf_cnpj_autor** | **str** | CPF/CNPJ do autor do evento. | [optional] 
**chave_acesso** | **str** | Chave de Acesso do documento vinculado ao evento. | [optional] 
**tipo_evento** | **str** | Tipo do evento vinculado. | [optional] 
**data_evento** | **datetime** | Data e hora do Evento. | [optional] 
**numero_sequencial** | **int** | Sequencial do evento para o mesmo tipo de evento. | [optional] 
**justificativa** | **str** | Justificativa para o desconhecimento ou não-realização da operação. | [optional] 
**data_registro** | **datetime** | Data e hora do registro do evento pela SEFAZ. | [optional] 
**codigo_status** | **int** | Código do status de registro do evento. | [optional] 
**motivo_status** | **str** | Descrição literal do status do registro do evento. | [optional] 
**numero_protocolo** | **str** | Número do Protocolo de registro do evento. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


