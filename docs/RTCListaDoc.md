# RTCListaDoc

Grupo relativo aos documentos referenciados nos casos de reembolso, repasse e ressarcimento que serão  considerados na base de cálculo do ISSQN, do IBS e da CBS.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**d_fe_nacional** | [**RTCListaDocDFe**](RTCListaDocDFe.md) |  | [opcional] 
**doc_fiscal_outro** | [**RTCListaDocFiscalOutro**](RTCListaDocFiscalOutro.md) |  | [opcional] 
**doc_outro** | [**RTCListaDocOutro**](RTCListaDocOutro.md) |  | [opcional] 
**fornec** | [**RTCListaDocFornec**](RTCListaDocFornec.md) |  | [opcional] 
**dt_emi_doc** | **date** | Data da emissão do documento dedutível  Ano, mês e dia (AAAA-MM-DD). | 
**dt_comp_doc** | **date** | Data da competência do documento dedutível  Ano, mês e dia (AAAA-MM-DD). | 
**tp_ree_rep_res** | **str** | Tipo de valor incluído neste documento, recebido por motivo de estarem relacionadas a operações de terceiros,  objeto de reembolso, repasse ou ressarcimento pelo recebedor, já tributados e aqui referenciados. | 
**x_tp_ree_rep_res** | **str** | Descrição do reembolso ou ressarcimento quando a opção é  \&quot;99 - Outros reembolsos ou ressarcimentos recebidos por valores pagos relativos a operações por conta e ordem de terceiro\&quot;. | [opcional] 
**vlr_ree_rep_res** | **float** | Valor monetário (total ou parcial, conforme documento informado) utilizado para não inclusão na base de cálculo  do ISS e do IBS e da CBS da NFS-e que está sendo emitida (R$). | 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


