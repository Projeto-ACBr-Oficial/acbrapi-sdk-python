# NfcomSefazDet

Detalhamento de Produtos e Serviços.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**n_item** | **int** | Número do item da NFCom. | 
**ch_nf_com_ant** | **str** | Chave de Acesso da NFCom anterior.  Informar chave de acesso de referencia anterior  TAG OPCIONAL, DEVE SER INFORMADA APENAS NOS CASOS PREVISTOS DE NOTA ANTERIOR REFERENCIADA. | [opcional] 
**n_item_ant** | **str** | Número do item da NFCom anterior.  Informar nro do item da chave de acesso de referencia anterior  TAG OPCIONAL, DEVE SER INFORMADA APENAS NOS CASOS PREVISTOS DE NOTA ANTERIOR REFERENCIADA. | [opcional] 
**ind_nf_com_ant_papel_fat_central** | **int** | Indicador de Nota anterior em papel no faturamento centralizado.  Informa que a NFCom Anterior de Faturamento centralizado não é eletrônica. | [opcional] 
**prod** | [**NfcomSefazProd**](NfcomSefazProd.md) |  | 
**imposto** | [**NfcomSefazImposto**](NfcomSefazImposto.md) |  | 
**g_proc_ref** | [**NfcomSefazGProcRef**](NfcomSefazGProcRef.md) |  | [opcional] 
**g_ressarc** | [**NfcomSefazGRessarc**](NfcomSefazGRessarc.md) |  | [opcional] 
**inf_ad_prod** | **str** | Informações adicionais do produto (norma referenciada, informações complementares, etc). | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


