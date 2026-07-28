# NfeSefazTransp

Dados dos transportes da NF-e.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mod_frete** | **int** | Modalidade do frete  * 0 - Contratação do Frete por conta do Remetente (CIF)  * 1 - Contratação do Frete por conta do destinatário/remetente (FOB)  * 2 - Contratação do Frete por conta de terceiros  * 3 - Transporte próprio por conta do remetente  * 4 - Transporte próprio por conta do destinatário  * 9 - Sem Ocorrência de transporte | 
**transporta** | [**NfeSefazTransporta**](NfeSefazTransporta.md) |  | [optional] 
**ret_transp** | [**NfeSefazRetTransp**](NfeSefazRetTransp.md) |  | [optional] 
**veic_transp** | [**NfeSefazVeiculo**](NfeSefazVeiculo.md) |  | [optional] 
**reboque** | [**list[NfeSefazVeiculo]**](NfeSefazVeiculo.md) |  | [optional] 
**vagao** | **str** | Identificação do vagão (v2.0). | [optional] 
**balsa** | **str** | Identificação da balsa (v2.0). | [optional] 
**vol** | [**list[NfeSefazVol]**](NfeSefazVol.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


