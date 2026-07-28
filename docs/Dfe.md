# Dfe


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | ID único gerado pela API para este documento. | [optional] 
**ambiente** | **str** |  | [optional] 
**created_at** | **datetime** | Data/hora em que o documento foi criado na API. Representado no formato &lt;a href&#x3D;\&quot;https://en.wikipedia.org/wiki/ISO_8601\&quot; target&#x3D;\&quot;blank\&quot;&gt;&#x60;ISO 8601&#x60;&lt;/a&gt;. | [optional] 
**status** | **str** | * &#x60;pendente&#x60;: o pedido de emissão do documento foi recebido pela API e está na fila de processamento.  * &#x60;autorizado&#x60;, &#x60;rejeitado&#x60; ou &#x60;denegado&#x60;: o documento foi transmitido para a SEFAZ, que retornou um desses status.  * &#x60;cancelado&#x60;: um evento de cancelamento foi homologado pela SEFAZ e associado ao documento.  * &#x60;encerrado&#x60;: um evento de encerramento foi homologado pela SEFAZ e associado a um MDF-e.  * &#x60;erro&#x60;: status próprio da API que significa, na maioria das vezes, que houve algum erro que impediu a transmissão do documento para a SEFAZ (erros de validação, erros interno do servidor, timeouts, etc). | [optional] 
**referencia** | **str** | Seu identificador único para este documento. Opcional, ajuda a evitar o envio duplicado de um mesmo documento. | [optional] 
**data_emissao** | **datetime** |  | [optional] 
**modelo** | **int** |  | [optional] 
**serie** | **int** |  | [optional] 
**numero** | **int** |  | [optional] 
**tipo_emissao** | **int** |  | [optional] 
**valor_total** | **float** |  | [optional] 
**chave** | **str** | Chave de acesso do DF-e. | [optional] 
**autorizacao** | [**DfeAutorizacao**](DfeAutorizacao.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


