# DfeDebug


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador do documento fiscal. | [optional] 
**tipo** | **str** | Tipo do documento: nfe, nfce, mdfe, nfse, etc. | [optional] 
**created_at** | **datetime** | Data e hora da criação do documento, representada no formato UTC (Tempo Universal Coordenado).  O valor é retornado no padrão ISO 8601, incluindo o deslocamento de fuso horário &#39;Z&#39; no final.    Exemplo: \&quot;2025-04-15T14:16:47.775Z\&quot; | [optional] 
**requisicoes** | [**list[DfeRequisicaoDebug]**](DfeRequisicaoDebug.md) | Lista de requisições feitas ao autorizador durante o processamento. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


