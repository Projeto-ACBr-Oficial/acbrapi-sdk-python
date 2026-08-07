# NfeSefazNFref

Grupo de infromações da NF referenciada.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**ref_nfe** | **str** | Chave de acesso das NF-e referenciadas. Chave de acesso compostas por Código da UF (tabela do IBGE) + AAMM da emissão + CNPJ do Emitente + modelo, série e número da NF-e Referenciada + Código Numérico + DV. | [opcional] 
**ref_nfe_sig** | **str** | Referencia uma NF-e (modelo 55) emitida anteriormente pela sua Chave de Acesso com código numérico zerado, permitindo manter o sigilo da NF-e referenciada. | [opcional] 
**ref_nf** | [**NfeSefazRefNF**](NfeSefazRefNF.md) |  | [opcional] 
**ref_nfp** | [**NfeSefazRefNFP**](NfeSefazRefNFP.md) |  | [opcional] 
**ref_cte** | **str** | Utilizar esta TAG para referenciar um CT-e emitido anteriormente, vinculada a NF-e atual. | [opcional] 
**ref_ecf** | [**NfeSefazRefECF**](NfeSefazRefECF.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


