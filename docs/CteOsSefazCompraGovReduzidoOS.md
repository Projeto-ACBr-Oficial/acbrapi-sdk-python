# CteOsSefazCompraGovReduzidoOS

Grupo de Compras Governamentais.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tp_ente_gov** | **int** | Para administração pública direta e suas autarquias e fundações:  * 1 - União  * 2 - Estados  * 3 - Distrito Federal  * 4 - Municípios  * 5 - Consórcio Público  * 6 - Comitê Gestor do IBS | 
**p_redutor** | **float** | Percentual de redução de aliquota em compra governamental. | 
**tp_oper_gov** | **int** | Tipo da operação com ente governamental:  * 1 - Fornecimento com pagamento posterior  * 2 - Recebimento do pagamento com fornecimento já realizado  * 3 - Fornecimento com pagamento já realizado  * 4 - Recebimento do pagamento com fornecimento posterior | 
**ref_dfe_ant** | **list[str]** | Chave de acesso do documento fiscal anterior.  Deverá ser informado para tpOperGov 2 e 3 e vedado para os tipos 1 e 4.  No caso do toOperGov 2 aceitará apenas uma chave referenciada, no tipo 3 poderá aceitar múltiplas chaves  Obs: a chave de acesso deverá ser de um emitente com o mesmo CNPJ base. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


