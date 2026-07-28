# HttpRequestDebug

Detalhes técnicos da requisição HTTP realizada ao autorizador.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador interno da requisição HTTP.    Esse identificador pode ser utilizado no endpoint  &lt;a href&#x3D;\&quot;#tag/Debug/operation/DebugHttpRequestContent\&quot;&gt;Corpo da Requisição HTTP&lt;/a&gt; ou &lt;a href&#x3D;\&quot;#tag/Debug/operation/DebugHttpResponseContent\&quot;&gt;Corpo da Resposta HTTP&lt;/a&gt;  para obter o conteúdo enviado ou recebido na comunicação com o autorizador. | [optional] 
**method** | **str** | Método HTTP utilizado (ex: &#39;POST&#39;). | [optional] 
**uri** | **str** | URI do serviço externo (SEFAZ, prefeitura, etc.). | [optional] 
**headers** | **str** | Cabeçalhos HTTP enviados na requisição, no formato bruto. | [optional] 
**response_status_code** | **int** | Código de status HTTP retornado (ex: 200, 403). | [optional] 
**response_status_reason** | **str** | Motivo ou descrição do status HTTP retornado. | [optional] 
**response_headers** | **str** | Cabeçalhos retornados na resposta, no formato bruto. | [optional] 
**response_time** | **int** | Tempo de resposta do serviço externo, em milissegundos. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


