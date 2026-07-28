# RpsPedidoEmissao


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**referencia** | **str** | Seu identificador único para este documento. Opcional, ajuda a evitar o envio duplicado de um mesmo documento. | [optional] 
**data_emissao** | **datetime** | Data e Hora de Emissão do RPS, no formato AAAA-MM-DDTHH:MM:SSTZD.  Caso não informado, será considerada a data/hora da requisição à API. | [optional] 
**competencia** | **datetime** | Competência do RPS, no formato AAAA-MM-DD.  Caso não informado, será considerada a data da requisição à API. | [optional] 
**natureza_tributacao** | **int** | Natureza da tributação:  * 1 - Simples Nacional;  * 2 - Fixo;  * 3 - Depósito em juízo;  * 4 - Exigibilidade suspensa por decisão judicial;  * 5 - Exigibilidade suspensa por procedimento administrativo;  * 6 - Isenção parcial. | [optional] 
**prestador** | [**RpsIdentificacaoPrestador**](RpsIdentificacaoPrestador.md) |  | 
**tomador** | [**RpsDadosTomador**](RpsDadosTomador.md) |  | 
**intermediario** | [**RpsDadosIntermediario**](RpsDadosIntermediario.md) |  | [optional] 
**construcao_civil** | [**RpsDadosConstrucaoCivil**](RpsDadosConstrucaoCivil.md) |  | [optional] 
**servicos** | [**list[RpsDadosServico]**](RpsDadosServico.md) |  | 
**outras_informacoes** | **str** | Informações adicionais ao documento. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


