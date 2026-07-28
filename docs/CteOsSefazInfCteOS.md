# CteOsSefazInfCteOS

Informações do CT-e Outros Serviços.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**versao** | **str** | Versão do leiaute.  Ex: \&quot;4.00\&quot;. | 
**id** | **str** | Identificador da tag a ser assinada.  Informar a chave de acesso do CT-e OS e precedida do literal \&quot;CTe\&quot;.    *Geramos automaticamente quando nenhum valor é informado.* | [optional] 
**ide** | [**CteOsSefazIdeOS**](CteOsSefazIdeOS.md) |  | 
**compl** | [**CteOsSefazComplOS**](CteOsSefazComplOS.md) |  | [optional] 
**emit** | [**CteOsSefazEmitOS**](CteOsSefazEmitOS.md) |  | 
**toma** | [**CteOsSefazTomaOS**](CteOsSefazTomaOS.md) |  | [optional] 
**v_prest** | [**CteOsSefazVPrestOS**](CteOsSefazVPrestOS.md) |  | 
**imp** | [**CteOsSefazInfCteImpOS**](CteOsSefazInfCteImpOS.md) |  | 
**pgto_vinc** | [**CteOsSefazPgtoVincOS**](CteOsSefazPgtoVincOS.md) |  | [optional] 
**inf_cte_norm** | [**CteOsSefazInfCTeNormOS**](CteOsSefazInfCTeNormOS.md) |  | [optional] 
**inf_cte_comp** | [**list[CteOsSefazInfCteCompOS]**](CteOsSefazInfCteCompOS.md) |  | [optional] 
**aut_xml** | [**list[CteOsSefazAutXMLOS]**](CteOsSefazAutXMLOS.md) |  | [optional] 
**inf_resp_tec** | [**CteOsSefazRespTecOS**](CteOsSefazRespTecOS.md) |  | [optional] 
**tp_pag_ant** | **int** | Tipo Pagamento ou Pagamento Antecipado.  Informar:  * 1 - Pagamento Antecipado  * 3 - Fornecimento com pagamento realizado anteriormente  Este campo é opcional e apenas deve ser informado quando pagamento que ocorre antes da prestação do serviço e na DFe de fornecimento associada a esses pagamentos, demais hipóteses de prestação de serviço sem antecipação não devem preencher. | [optional] 
**g_pag_antecipado** | [**CteOsSefazGPagAntecipadoOS**](CteOsSefazGPagAntecipadoOS.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


