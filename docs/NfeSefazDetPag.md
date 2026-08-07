# NfeSefazDetPag

Grupo de detalhamento da forma de pagamento.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**ind_pag** | **int** | Indicador da Forma de Pagamento:0-Pagamento à Vista  * 1 - Pagamento à Prazo | [opcional] 
**t_pag** | **str** | Forma de Pagamento:. | 
**x_pag** | **str** | Descrição do Meio de Pagamento. | [opcional] 
**v_pag** | **float** | Valor do Pagamento. Esta tag poderá ser omitida quando a tag tPag&#x3D;90 (Sem Pagamento), caso contrário deverá ser preenchida. | 
**d_pag** | **date** | Data do Pagamento. | [opcional] 
**cnpj_pag** | **str** | CNPJ transacional do pagamento - Preencher informando o CNPJ do estabelecimento onde o pagamento foi processado/transacionado/recebido quando a emissão do documento fiscal ocorrer em estabelecimento distinto. | [opcional] 
**uf_pag** | **str** | UF do CNPJ do estabelecimento onde o pagamento foi processado/transacionado/recebido. | [opcional] 
**card** | [**NfeSefazCard**](NfeSefazCard.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


