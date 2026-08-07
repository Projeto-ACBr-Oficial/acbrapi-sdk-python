# Rps

*Propriedade obsoleta. Não é mais retornada pela API.*

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**rps** | [**RpsDados**](RpsDados.md) |  | [opcional] 
**competencia** | **datetime** |  | [opcional] 
**natureza_tributacao** | **int** | Natureza da tributação  1 - Simples Nacional;  2 - Fixo;  3 - Depósito em juízo;  4 - Exigibilidade suspensa por decisão judicial;  5 - Exigibilidade suspensa por procedimento administrativo;  6 - Isenção parcial. | [opcional] 
**prestador** | [**RpsDadosPrestador**](RpsDadosPrestador.md) |  | [opcional] 
**tomador** | [**RpsDadosTomador**](RpsDadosTomador.md) |  | [opcional] 
**intermediario** | [**RpsDadosIntermediario**](RpsDadosIntermediario.md) |  | [opcional] 
**construcao_civil** | [**RpsDadosConstrucaoCivil**](RpsDadosConstrucaoCivil.md) |  | [opcional] 
**servicos** | [**list[RpsDadosServico]**](RpsDadosServico.md) |  | 
**outras_informacoes** | **str** | Informações adicionais ao documento. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


