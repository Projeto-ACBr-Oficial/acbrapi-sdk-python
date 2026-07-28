# CteSimpSefazUnidadeTranspSimp

Informações das Unidades de Transporte (Carreta/Reboque/Vagão).  Deve ser preenchido com as informações das unidades de transporte utilizadas.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tp_unid_transp** | **int** | Tipo da Unidade de Transporte.  * 1 - Rodoviário Tração  * 2 - Rodoviário Reboque  * 3 - Navio  * 4 - Balsa  * 5 - Aeronave  * 6 - Vagão  * 7 - Outros | 
**id_unid_transp** | **str** | Identificação da Unidade de Transporte.  Informar a identificação conforme o tipo de unidade de transporte.  Por exemplo: para rodoviário tração ou reboque deverá preencher com a placa do veículo. | 
**lac_unid_transp** | [**list[CteSimpSefazLacUnidTranspSimp]**](CteSimpSefazLacUnidTranspSimp.md) |  | [optional] 
**inf_unid_carga** | [**list[CteSimpSefazUnidCargaSimp]**](CteSimpSefazUnidCargaSimp.md) |  | [optional] 
**qtd_rat** | **float** | Quantidade rateada (Peso,Volume). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


