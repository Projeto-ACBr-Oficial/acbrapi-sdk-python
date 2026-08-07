# HttpRequestDebug

Detalhes técnicos da requisição HTTP realizada ao autorizador.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador interno da requisição HTTP.    Esse identificador pode ser utilizado no endpoint  &lt;a href&#x3D;\&quot;#tag/Debug/operation/DebugHttpRequestContent\&quot;&gt;Corpo da Requisição HTTP&lt;/a&gt; ou &lt;a href&#x3D;\&quot;#tag/Debug/operation/DebugHttpResponseContent\&quot;&gt;Corpo da Resposta HTTP&lt;/a&gt;  para obter o conteúdo enviado ou recebido na comunicação com o autorizador. | [opcional] 
**method** | **str** | Método HTTP utilizado (ex: &#39;POST&#39;). | [opcional] 
**uri** | **str** | URI do serviço externo (SEFAZ, prefeitura, etc.). | [opcional] 
**headers** | **str** | Cabeçalhos HTTP enviados na requisição, no formato bruto. | [opcional] 
**response_status_code** | **int** | Código de status HTTP retornado (ex: 200, 403). | [opcional] 
**response_status_reason** | **str** | Motivo ou descrição do status HTTP retornado. | [opcional] 
**response_headers** | **str** | Cabeçalhos retornados na resposta, no formato bruto. | [opcional] 
**response_time** | **int** | Tempo de resposta do serviço externo, em milissegundos. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


