# NfeSefazDet

Dados dos detalhes da NF-e.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**n_item** | **int** | Número do item do NF. | 
**prod** | [**NfeSefazProd**](NfeSefazProd.md) |  | 
**imposto** | [**NfeSefazImposto**](NfeSefazImposto.md) |  | 
**imposto_devol** | [**NfeSefazImpostoDevol**](NfeSefazImpostoDevol.md) |  | [opcional] 
**inf_ad_prod** | **str** | Informações adicionais do produto (norma referenciada, informações complementares, etc). | [opcional] 
**obs_item** | [**NfeSefazObsItem**](NfeSefazObsItem.md) |  | [opcional] 
**v_item** | **float** | Valor total do Item, correspondente à sua participação no total da nota. A soma dos itens deverá corresponder ao total da nota. | [opcional] 
**dfe_referenciado** | [**NfeSefazDFeReferenciado**](NfeSefazDFeReferenciado.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


