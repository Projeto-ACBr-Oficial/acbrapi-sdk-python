# CteSefazInfOutros

Informações dos demais documentos.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**tp_doc** | **str** | Tipo de documento originário.  Preencher com:  * 00 - Declaração  * 10 - Dutoviário  * 59 - CF-e SAT  * 65 - NFC-e  * 99 - Outros | 
**desc_outros** | **str** | Descrição do documento. | [opcional] 
**n_doc** | **str** | Número. | [opcional] 
**d_emi** | **date** | Data de Emissão.  Formato AAAA-MM-DD. | [opcional] 
**v_doc_fisc** | **float** | Valor do documento. | [opcional] 
**d_prev** | **date** | Data prevista de entrega.  Formato AAAA-MM-DD. | [opcional] 
**inf_unid_carga** | [**list[CteSefazUnidCarga]**](CteSefazUnidCarga.md) |  | [opcional] 
**inf_unid_transp** | [**list[CteSefazUnidadeTransp]**](CteSefazUnidadeTransp.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


