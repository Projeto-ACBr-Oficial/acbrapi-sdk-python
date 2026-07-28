# DfeRequisicaoDebug


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **datetime** | Data e hora da criação da requisição, representada no formato UTC (Tempo Universal Coordenado).  O valor é retornado no padrão ISO 8601, incluindo o deslocamento de fuso horário &#39;Z&#39; no final.    Exemplo: \&quot;2025-04-15T14:16:47.775Z\&quot; | [optional] 
**tipo** | **str** | Tipo da operação realizada na requisição para o autorizador.  Pode assumir um dos seguintes valores:  - &#39;envio_lote&#39;      : envio do lote de documentos fiscais para autorização;  - &#39;consulta_lote&#39;   : consulta do processamento do lote;  - &#39;cons_sit_dfe&#39;    : consulta de situação individual de um DFe.    Esse campo indica a natureza da interação com a SEFAZ ou prefeitura,  e é útil para fins de rastreamento e diagnóstico do fluxo. | [optional] 
**lote_id** | **str** | Identificador do lote vinculado à requisição. | [optional] 
**codigo_status** | **int** | Código de status retornado pela SEFAZ/prefeitura. | [optional] 
**motivo_status** | **str** | Motivo associado ao status retornado. | [optional] 
**http_request** | [**HttpRequestDebug**](HttpRequestDebug.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


