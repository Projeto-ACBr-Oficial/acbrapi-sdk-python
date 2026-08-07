# NfcomSefazGFat

Grupo de informações de controle da Fatura.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**compet_fat** | **str** | Ano e mês referência do faturamento (AAAAMM). | 
**d_venc_fat** | **date** | Data de vencimento da fatura.  Formato AAAA-MM-DD. | 
**d_per_uso_ini** | **date** | Período de uso inicial.  Formato AAAA-MM-DD. | [opcional] 
**d_per_uso_fim** | **date** | Período de uso final.  Formato AAAA-MM-DD. | [opcional] 
**cod_barras** | **str** | Linha digitável do código de barras. | 
**cod_deb_auto** | **str** | Código de autorização débito em conta. | [opcional] 
**cod_banco** | **str** | Número do banco para débito em conta. | [opcional] 
**cod_agencia** | **str** | Número da agência bancária para débito em conta. | [opcional] 
**ender_corresp** | [**NfcomSefazEndeEmi**](NfcomSefazEndeEmi.md) |  | [opcional] 
**g_pix** | [**NfcomSefazGPIX**](NfcomSefazGPIX.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


