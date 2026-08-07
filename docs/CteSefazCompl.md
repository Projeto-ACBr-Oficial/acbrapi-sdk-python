# CteSefazCompl

Dados complementares do CT-e para fins operacionais ou comerciais.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**x_carac_ad** | **str** | Característica adicional do transporte.  Texto livre:  REENTREGA  DEVOLUÇÃO  REFATURAMENTO  etc. | [opcional] 
**x_carac_ser** | **str** | Característica adicional do serviço.  Texto livre:  ENTREGA EXPRESSA  LOGÍSTICA REVERSA  CONVENCIONAL  EMERGENCIAL  etc. | [opcional] 
**x_emi** | **str** | Funcionário emissor do CTe. | [opcional] 
**fluxo** | [**CteSefazFluxo**](CteSefazFluxo.md) |  | [opcional] 
**entrega** | [**CteSefazEntrega**](CteSefazEntrega.md) |  | [opcional] 
**orig_calc** | **str** | Município de origem para efeito de cálculo do frete. | [opcional] 
**dest_calc** | **str** | Município de destino para efeito de cálculo do frete. | [opcional] 
**x_obs** | **str** | Observações Gerais. | [opcional] 
**obs_cont** | [**list[CteSefazObsCont]**](CteSefazObsCont.md) |  | [opcional] 
**obs_fisco** | [**list[CteSefazObsFisco]**](CteSefazObsFisco.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


