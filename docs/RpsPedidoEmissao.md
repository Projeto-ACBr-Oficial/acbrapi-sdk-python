# RpsPedidoEmissao


## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**referencia** | **str** | Seu identificador único para este documento. Opcional, ajuda a evitar o envio duplicado de um mesmo documento. | [opcional] 
**data_emissao** | **datetime** | Data e Hora de Emissão do RPS, no formato AAAA-MM-DDTHH:MM:SSTZD.  Caso não informado, será considerada a data/hora da requisição à API. | [opcional] 
**competencia** | **datetime** | Competência do RPS, no formato AAAA-MM-DD.  Caso não informado, será considerada a data da requisição à API. | [opcional] 
**natureza_tributacao** | **int** | Natureza da tributação:  * 1 - Simples Nacional;  * 2 - Fixo;  * 3 - Depósito em juízo;  * 4 - Exigibilidade suspensa por decisão judicial;  * 5 - Exigibilidade suspensa por procedimento administrativo;  * 6 - Isenção parcial. | [opcional] 
**prestador** | [**RpsIdentificacaoPrestador**](RpsIdentificacaoPrestador.md) |  | 
**tomador** | [**RpsDadosTomador**](RpsDadosTomador.md) |  | 
**intermediario** | [**RpsDadosIntermediario**](RpsDadosIntermediario.md) |  | [opcional] 
**construcao_civil** | [**RpsDadosConstrucaoCivil**](RpsDadosConstrucaoCivil.md) |  | [opcional] 
**servicos** | [**list[RpsDadosServico]**](RpsDadosServico.md) |  | 
**outras_informacoes** | **str** | Informações adicionais ao documento. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


