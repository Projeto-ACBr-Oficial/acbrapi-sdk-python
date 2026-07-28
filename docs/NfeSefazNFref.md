# NfeSefazNFref

Grupo de infromações da NF referenciada.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ref_nfe** | **str** | Chave de acesso das NF-e referenciadas. Chave de acesso compostas por Código da UF (tabela do IBGE) + AAMM da emissão + CNPJ do Emitente + modelo, série e número da NF-e Referenciada + Código Numérico + DV. | [optional] 
**ref_nfe_sig** | **str** | Referencia uma NF-e (modelo 55) emitida anteriormente pela sua Chave de Acesso com código numérico zerado, permitindo manter o sigilo da NF-e referenciada. | [optional] 
**ref_nf** | [**NfeSefazRefNF**](NfeSefazRefNF.md) |  | [optional] 
**ref_nfp** | [**NfeSefazRefNFP**](NfeSefazRefNFP.md) |  | [optional] 
**ref_cte** | **str** | Utilizar esta TAG para referenciar um CT-e emitido anteriormente, vinculada a NF-e atual. | [optional] 
**ref_ecf** | [**NfeSefazRefECF**](NfeSefazRefECF.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


