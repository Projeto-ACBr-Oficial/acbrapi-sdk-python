# MdfeSefazEmit

Identificação do Emitente do Manifesto.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | CNPJ do emitente.  Informar zeros não significativos.    ***Obrigatório caso o emitente seja pessoa jurídica***. | [optional] 
**cpf** | **str** | CPF do emitente.  Informar zeros não significativos.  Usar com série específica 920-969 para emitente pessoa física com inscrição estadual.  Poderá ser usado também para emissão do Regime Especial da Nota Fiscal Fácil.    ***Obrigatório caso o emitente seja pessoa física***. | [optional] 
**ie** | **str** | Inscrição Estadual do emitemte.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**x_nome** | **str** | Razão social ou Nome do emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**x_fant** | **str** | Nome fantasia do emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**ender_emit** | [**MdfeSefazEndeEmi**](MdfeSefazEndeEmi.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


