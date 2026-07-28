# CteSefazInfOutros

Informações dos demais documentos.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tp_doc** | **str** | Tipo de documento originário.  Preencher com:  * 00 - Declaração  * 10 - Dutoviário  * 59 - CF-e SAT  * 65 - NFC-e  * 99 - Outros | 
**desc_outros** | **str** | Descrição do documento. | [optional] 
**n_doc** | **str** | Número. | [optional] 
**d_emi** | **date** | Data de Emissão.  Formato AAAA-MM-DD. | [optional] 
**v_doc_fisc** | **float** | Valor do documento. | [optional] 
**d_prev** | **date** | Data prevista de entrega.  Formato AAAA-MM-DD. | [optional] 
**inf_unid_carga** | [**list[CteSefazUnidCarga]**](CteSefazUnidCarga.md) |  | [optional] 
**inf_unid_transp** | [**list[CteSefazUnidadeTransp]**](CteSefazUnidadeTransp.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


