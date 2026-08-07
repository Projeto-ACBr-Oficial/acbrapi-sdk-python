# MdfeSefazEmit

Identificação do Emitente do Manifesto.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | CNPJ do emitente.  Informar zeros não significativos.    ***Obrigatório caso o emitente seja pessoa jurídica***. | [opcional] 
**cpf** | **str** | CPF do emitente.  Informar zeros não significativos.  Usar com série específica 920-969 para emitente pessoa física com inscrição estadual.  Poderá ser usado também para emissão do Regime Especial da Nota Fiscal Fácil.    ***Obrigatório caso o emitente seja pessoa física***. | [opcional] 
**ie** | **str** | Inscrição Estadual do emitemte.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [opcional] 
**x_nome** | **str** | Razão social ou Nome do emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [opcional] 
**x_fant** | **str** | Nome fantasia do emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [opcional] 
**ender_emit** | [**MdfeSefazEndeEmi**](MdfeSefazEndeEmi.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


