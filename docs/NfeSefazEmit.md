# NfeSefazEmit

Identificação do emitente.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número do CNPJ do emitente.    ***Obrigatório caso o emitente seja pessoa jurídica***. | [optional] 
**cpf** | **str** | Número do CPF do emitente.    ***Obrigatório caso o emitente seja pessoa física***. | [optional] 
**x_nome** | **str** | Razão Social ou Nome do emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**x_fant** | **str** | Nome fantasia.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**ender_emit** | [**NfeSefazEnderEmi**](NfeSefazEnderEmi.md) |  | [optional] 
**ie** | **str** | Inscrição Estadual do Emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**iest** | **str** | Inscricao Estadual do Substituto Tributário.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**im** | **str** | Inscrição Municipal.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**cnae** | **str** | CNAE Fiscal.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**crt** | **int** | Código de Regime Tributário.  Este campo será obrigatoriamente preenchido com:  * 1 - Simples Nacional  * 2 - Simples Nacional - excesso de sublimite de receita bruta  * 3 - Regime Normal  * 4 - Simples Nacional - Microempreendedor individual - MEI    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


