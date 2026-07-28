# CteSefazCompl

Dados complementares do CT-e para fins operacionais ou comerciais.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**x_carac_ad** | **str** | Característica adicional do transporte.  Texto livre:  REENTREGA  DEVOLUÇÃO  REFATURAMENTO  etc. | [optional] 
**x_carac_ser** | **str** | Característica adicional do serviço.  Texto livre:  ENTREGA EXPRESSA  LOGÍSTICA REVERSA  CONVENCIONAL  EMERGENCIAL  etc. | [optional] 
**x_emi** | **str** | Funcionário emissor do CTe. | [optional] 
**fluxo** | [**CteSefazFluxo**](CteSefazFluxo.md) |  | [optional] 
**entrega** | [**CteSefazEntrega**](CteSefazEntrega.md) |  | [optional] 
**orig_calc** | **str** | Município de origem para efeito de cálculo do frete. | [optional] 
**dest_calc** | **str** | Município de destino para efeito de cálculo do frete. | [optional] 
**x_obs** | **str** | Observações Gerais. | [optional] 
**obs_cont** | [**list[CteSefazObsCont]**](CteSefazObsCont.md) |  | [optional] 
**obs_fisco** | [**list[CteSefazObsFisco]**](CteSefazObsFisco.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


