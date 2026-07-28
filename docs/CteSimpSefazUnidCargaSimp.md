# CteSimpSefazUnidCargaSimp

Informações das Unidades de Carga (Containeres/ULD/Outros).  Dispositivo de carga utilizada (Unit Load Device - ULD) significa todo tipo de contêiner de carga, vagão, contêiner de avião, palete de aeronave com rede ou palete de aeronave com rede sobre um iglu.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tp_unid_carga** | **int** | Tipo da Unidade de Carga.  * 1 - Container  * 2 - ULD  * 3 - Pallet  * 4 - Outros | 
**id_unid_carga** | **str** | Identificação da Unidade de Carga.  Informar a identificação da unidade de carga, por exemplo: número do container. | 
**lac_unid_carga** | [**list[CteSimpSefazLacUnidCargaSimp]**](CteSimpSefazLacUnidCargaSimp.md) |  | [optional] 
**qtd_rat** | **float** | Quantidade rateada (Peso,Volume). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


