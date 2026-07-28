# NfcomSefazGFat

Grupo de informações de controle da Fatura.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**compet_fat** | **str** | Ano e mês referência do faturamento (AAAAMM). | 
**d_venc_fat** | **date** | Data de vencimento da fatura.  Formato AAAA-MM-DD. | 
**d_per_uso_ini** | **date** | Período de uso inicial.  Formato AAAA-MM-DD. | [optional] 
**d_per_uso_fim** | **date** | Período de uso final.  Formato AAAA-MM-DD. | [optional] 
**cod_barras** | **str** | Linha digitável do código de barras. | 
**cod_deb_auto** | **str** | Código de autorização débito em conta. | [optional] 
**cod_banco** | **str** | Número do banco para débito em conta. | [optional] 
**cod_agencia** | **str** | Número da agência bancária para débito em conta. | [optional] 
**ender_corresp** | [**NfcomSefazEndeEmi**](NfcomSefazEndeEmi.md) |  | [optional] 
**g_pix** | [**NfcomSefazGPIX**](NfcomSefazGPIX.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


