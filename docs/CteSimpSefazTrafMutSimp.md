# CteSimpSefazTrafMutSimp

Detalhamento de informações para o tráfego mútuo.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**resp_fat** | **int** | Responsável pelo Faturamento.  Preencher com:  * 1 - Ferrovia de origem  * 2 - Ferrovia de destino | 
**ferr_emi** | **int** | Ferrovia Emitente do CTe.  Preencher com:  * 1 - Ferrovia de origem  * 2 - Ferrovia de destino | 
**v_frete** | **float** | Valor do Frete do Tráfego Mútuo. | 
**ch_cte_ferro_origem** | **str** | Chave de acesso do CT-e emitido pelo ferrovia de origem. | [opcional] 
**ferro_env** | [**list[CteSimpSefazFerroEnvSimp]**](CteSimpSefazFerroEnvSimp.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


