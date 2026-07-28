# NfeSefazDetPag

Grupo de detalhamento da forma de pagamento.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ind_pag** | **int** | Indicador da Forma de Pagamento:0-Pagamento à Vista  * 1 - Pagamento à Prazo | [optional] 
**t_pag** | **str** | Forma de Pagamento:. | 
**x_pag** | **str** | Descrição do Meio de Pagamento. | [optional] 
**v_pag** | **float** | Valor do Pagamento. Esta tag poderá ser omitida quando a tag tPag&#x3D;90 (Sem Pagamento), caso contrário deverá ser preenchida. | 
**d_pag** | **date** | Data do Pagamento. | [optional] 
**cnpj_pag** | **str** | CNPJ transacional do pagamento - Preencher informando o CNPJ do estabelecimento onde o pagamento foi processado/transacionado/recebido quando a emissão do documento fiscal ocorrer em estabelecimento distinto. | [optional] 
**uf_pag** | **str** | UF do CNPJ do estabelecimento onde o pagamento foi processado/transacionado/recebido. | [optional] 
**card** | [**NfeSefazCard**](NfeSefazCard.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


