# CteSefazTrafMut

Detalhamento de informações para o tráfego mútuo.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resp_fat** | **int** | Responsável pelo Faturamento.  Preencher com:  * 1 - Ferrovia de origem  * 2 - Ferrovia de destino | 
**ferr_emi** | **int** | Ferrovia Emitente do CTe.  Preencher com:  * 1 - Ferrovia de origem  * 2 - Ferrovia de destino | 
**v_frete** | **float** | Valor do Frete do Tráfego Mútuo. | 
**ch_cte_ferro_origem** | **str** | Chave de acesso do CT-e emitido pelo ferrovia de origem. | [optional] 
**ferro_env** | [**list[CteSefazFerroEnv]**](CteSefazFerroEnv.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


