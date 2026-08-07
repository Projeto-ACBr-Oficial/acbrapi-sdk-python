# CteOsSefazInfCteOS

Informações do CT-e Outros Serviços.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**versao** | **str** | Versão do leiaute.  Ex: \&quot;4.00\&quot;. | 
**id** | **str** | Identificador da tag a ser assinada.  Informar a chave de acesso do CT-e OS e precedida do literal \&quot;CTe\&quot;.    *Geramos automaticamente quando nenhum valor é informado.* | [opcional] 
**ide** | [**CteOsSefazIdeOS**](CteOsSefazIdeOS.md) |  | 
**compl** | [**CteOsSefazComplOS**](CteOsSefazComplOS.md) |  | [opcional] 
**emit** | [**CteOsSefazEmitOS**](CteOsSefazEmitOS.md) |  | 
**toma** | [**CteOsSefazTomaOS**](CteOsSefazTomaOS.md) |  | [opcional] 
**v_prest** | [**CteOsSefazVPrestOS**](CteOsSefazVPrestOS.md) |  | 
**imp** | [**CteOsSefazInfCteImpOS**](CteOsSefazInfCteImpOS.md) |  | 
**pgto_vinc** | [**CteOsSefazPgtoVincOS**](CteOsSefazPgtoVincOS.md) |  | [opcional] 
**inf_cte_norm** | [**CteOsSefazInfCTeNormOS**](CteOsSefazInfCTeNormOS.md) |  | [opcional] 
**inf_cte_comp** | [**list[CteOsSefazInfCteCompOS]**](CteOsSefazInfCteCompOS.md) |  | [opcional] 
**aut_xml** | [**list[CteOsSefazAutXMLOS]**](CteOsSefazAutXMLOS.md) |  | [opcional] 
**inf_resp_tec** | [**CteOsSefazRespTecOS**](CteOsSefazRespTecOS.md) |  | [opcional] 
**tp_pag_ant** | **int** | Tipo Pagamento ou Pagamento Antecipado.  Informar:  * 1 - Pagamento Antecipado  * 3 - Fornecimento com pagamento realizado anteriormente  Este campo é opcional e apenas deve ser informado quando pagamento que ocorre antes da prestação do serviço e na DFe de fornecimento associada a esses pagamentos, demais hipóteses de prestação de serviço sem antecipação não devem preencher. | [opcional] 
**g_pag_antecipado** | [**CteOsSefazGPagAntecipadoOS**](CteOsSefazGPagAntecipadoOS.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


