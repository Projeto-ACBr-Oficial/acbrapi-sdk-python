# NfcomSefazDet

Detalhamento de Produtos e Serviços.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**n_item** | **int** | Número do item da NFCom. | 
**ch_nf_com_ant** | **str** | Chave de Acesso da NFCom anterior.  Informar chave de acesso de referencia anterior  TAG OPCIONAL, DEVE SER INFORMADA APENAS NOS CASOS PREVISTOS DE NOTA ANTERIOR REFERENCIADA. | [optional] 
**n_item_ant** | **str** | Número do item da NFCom anterior.  Informar nro do item da chave de acesso de referencia anterior  TAG OPCIONAL, DEVE SER INFORMADA APENAS NOS CASOS PREVISTOS DE NOTA ANTERIOR REFERENCIADA. | [optional] 
**ind_nf_com_ant_papel_fat_central** | **int** | Indicador de Nota anterior em papel no faturamento centralizado.  Informa que a NFCom Anterior de Faturamento centralizado não é eletrônica. | [optional] 
**prod** | [**NfcomSefazProd**](NfcomSefazProd.md) |  | 
**imposto** | [**NfcomSefazImposto**](NfcomSefazImposto.md) |  | 
**g_proc_ref** | [**NfcomSefazGProcRef**](NfcomSefazGProcRef.md) |  | [optional] 
**g_ressarc** | [**NfcomSefazGRessarc**](NfcomSefazGRessarc.md) |  | [optional] 
**inf_ad_prod** | **str** | Informações adicionais do produto (norma referenciada, informações complementares, etc). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


