# DocAjusteBC

Grupo de informações de documento utilizado para ajuste dos valores de base de cálculo (ISSQN e/ou IBS/CBS).

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**tp_ajuste_bc** | **int** | Tipo de Ajuste. | 
**x_tp_ajuste_bc** | **str** | Descrição do ajuste quando o tipo informado exige detalhamento. | [opcional] 
**v_tot_doc** | **float** | Valor monetário total do documento informado (R$). | 
**v_ajuste_aplic** | **float** | Valor monetário efetivamente utilizado para ajuste de base(s) de cálculo do valor do serviço da NFS-e que está sendo emitida (R$). | 
**dt_emi_doc** | **date** | Data da emissão do documento dedutível. Ano, mês e dia (AAAA-MM-DD). | [opcional] 
**dt_comp_doc** | **date** | Data da competência do documento dedutível. Ano, mês e dia (AAAA-MM-DD). | [opcional] 
**d_fe_nacional** | [**RTCListaDocDFe**](RTCListaDocDFe.md) |  | [opcional] 
**doc_fiscal_outro** | [**RTCListaDocFiscalOutro**](RTCListaDocFiscalOutro.md) |  | [opcional] 
**doc_outro** | [**RTCListaDocOutro**](RTCListaDocOutro.md) |  | [opcional] 
**fornec** | [**InfoFornecDocDedRed**](InfoFornecDocDedRed.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


