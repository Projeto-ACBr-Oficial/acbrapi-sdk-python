# CteSimpSefazEmitSimp

Identificação do Emitente do CT-e.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | CNPJ do emitente.  Informar zeros não significativos.    ***Obrigatório caso o emitente seja pessoa jurídica***. | [optional] 
**cpf** | **str** | CPF do emitente.  Informar zeros não significativos.  Usar com série específica 920-969 para emitente pessoa física com inscrição estadual.    ***Obrigatório caso o emitente seja pessoa física***. | [optional] 
**ie** | **str** | Inscrição Estadual do Emitente.  A IE do emitente somente ficará sem informação para o caso do Regime Especial da NFF (tpEmis&#x3D;3).    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**iest** | **str** | Inscrição Estadual do Substituto Tributário. | [optional] 
**x_nome** | **str** | Razão social ou Nome do emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**x_fant** | **str** | Nome fantasia.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**ender_emit** | [**CteSimpSefazEndeEmiSimp**](CteSimpSefazEndeEmiSimp.md) |  | [optional] 
**crt** | **int** | Código do Regime Tributário. Informar:  * 1 - Simples Nacional;  * 2 - Simples Nacional, excesso sublimite de receita bruta;  * 3 - Regime Normal;  * 4 - Simples Nacional - Microempreendedor Individual (MEI).    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional] 
**isuf_emit** | **str** | Inscrição do emitente da Suframa.  Informar o número do Cadastro do emitente na Suframa. Campo obrigatório nas operações que se beneficiam de incentivos fiscais existentes nas áreas sob controle da SUFRAMA com alíquota zero da CBS referente aos arts. 451 e 466 da LC 214/25. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


