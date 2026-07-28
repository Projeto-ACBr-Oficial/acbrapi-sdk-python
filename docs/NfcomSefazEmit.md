# NfcomSefazEmit

Identificação do Emitente do documento fiscal.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | CNPJ do emitente.  Informar zeros não significativos. | 
**ie** | **str** | Inscrição Estadual do emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**ieuf_dest** | **str** | Inscrição Estadual Virtual do emitente na UF de Destino da partilha (IE Virtual). | [optional] 
**crt** | **int** | Código do Regime Tributário. Informar:  * 1 - Simples Nacional;  * 2 - Simples Nacional, excesso sublimite de receita bruta;  * 3 - Regime Normal.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**x_nome** | **str** | Razão social ou Nome do emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**x_fant** | **str** | Nome fantasia do emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**ender_emit** | [**NfcomSefazEndeEmi**](NfcomSefazEndeEmi.md) |  | [optional] 
**isuf_emit** | **str** | Inscrição do emitente da Suframa.  Informar o número do Cadastro do emitente na Suframa. Campo obrigatório nas operações que se beneficiam de incentivos fiscais existentes nas áreas sob controle da SUFRAMA com alíquota zero da CBS referente aos arts. 451 e 466 da LC 214/25. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


