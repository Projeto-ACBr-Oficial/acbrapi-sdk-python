# DfeDebug


## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador do documento fiscal. | [opcional] 
**tipo** | **str** | Tipo do documento: nfe, nfce, mdfe, nfse, etc. | [opcional] 
**created_at** | **datetime** | Data e hora da criação do documento, representada no formato UTC (Tempo Universal Coordenado).  O valor é retornado no padrão ISO 8601, incluindo o deslocamento de fuso horário &#39;Z&#39; no final.    Exemplo: \&quot;2025-04-15T14:16:47.775Z\&quot; | [opcional] 
**requisicoes** | [**list[DfeRequisicaoDebug]**](DfeRequisicaoDebug.md) | Lista de requisições feitas ao autorizador durante o processamento. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


