# RTCListaDoc

Grupo relativo aos documentos referenciados nos casos de reembolso, repasse e ressarcimento que serão  considerados na base de cálculo do ISSQN, do IBS e da CBS.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**d_fe_nacional** | [**RTCListaDocDFe**](RTCListaDocDFe.md) |  | [optional] 
**doc_fiscal_outro** | [**RTCListaDocFiscalOutro**](RTCListaDocFiscalOutro.md) |  | [optional] 
**doc_outro** | [**RTCListaDocOutro**](RTCListaDocOutro.md) |  | [optional] 
**fornec** | [**RTCListaDocFornec**](RTCListaDocFornec.md) |  | [optional] 
**dt_emi_doc** | **date** | Data da emissão do documento dedutível  Ano, mês e dia (AAAA-MM-DD). | 
**dt_comp_doc** | **date** | Data da competência do documento dedutível  Ano, mês e dia (AAAA-MM-DD). | 
**tp_ree_rep_res** | **str** | Tipo de valor incluído neste documento, recebido por motivo de estarem relacionadas a operações de terceiros,  objeto de reembolso, repasse ou ressarcimento pelo recebedor, já tributados e aqui referenciados. | 
**x_tp_ree_rep_res** | **str** | Descrição do reembolso ou ressarcimento quando a opção é  \&quot;99 - Outros reembolsos ou ressarcimentos recebidos por valores pagos relativos a operações por conta e ordem de terceiro\&quot;. | [optional] 
**vlr_ree_rep_res** | **float** | Valor monetário (total ou parcial, conforme documento informado) utilizado para não inclusão na base de cálculo  do ISS e do IBS e da CBS da NFS-e que está sendo emitida (R$). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


