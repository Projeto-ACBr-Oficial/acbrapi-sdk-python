# CteSefazAquav

Informações do modal Aquaviário.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**v_prest** | **float** | Valor da Prestação Base de Cálculo do AFRMM. | 
**v_afrmm** | **float** | AFRMM (Adicional de Frete para Renovação da Marinha Mercante). | 
**x_navio** | **str** | Identificação do Navio. | 
**balsa** | [**list[CteSefazBalsa]**](CteSefazBalsa.md) |  | [optional] 
**n_viag** | **str** | Número da Viagem. | [optional] 
**direc** | **str** | Direção.  Preencher com: N-Norte, L-Leste, S-Sul, O-Oeste. | 
**irin** | **str** | Irin do navio sempre deverá ser informado. | 
**det_cont** | [**list[CteSefazDetCont]**](CteSefazDetCont.md) |  | [optional] 
**tp_nav** | **int** | Tipo de Navegação.  Preencher com:  * 0 - Interior  * 1 - Cabotagem | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


