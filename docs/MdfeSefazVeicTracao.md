# MdfeSefazVeicTracao

Dados do Veículo com a Tração.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**c_int** | **str** | Código interno do veículo. | [optional] 
**placa** | **str** | Placa do veículo. | 
**renavam** | **str** | RENAVAM do veículo. | [optional] 
**tara** | **int** | Tara em KG. | 
**cap_kg** | **int** | Capacidade em KG. | [optional] 
**cap_m3** | **int** | Capacidade em M3. | [optional] 
**prop** | [**MdfeSefazProp**](MdfeSefazProp.md) |  | [optional] 
**condutor** | [**list[MdfeSefazCondutor]**](MdfeSefazCondutor.md) |  | 
**tp_rod** | **str** | Tipo de Rodado.  Preencher com:  * 01 - Truck  * 02 - Toco  * 03 - Cavalo Mecânico  * 04 - VAN  * 05 - Utilitário  * 06 - Outros | 
**tp_car** | **str** | Tipo de Carroceria.  Preencher com:  * 00 - não aplicável  * 01 - Aberta  * 02 - Fechada/Baú  * 03 - Granelera  * 04 - Porta Container  * 05 - Sider | 
**uf** | **str** | UF em que veículo está licenciado.  Sigla da UF de licenciamento do veículo. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


