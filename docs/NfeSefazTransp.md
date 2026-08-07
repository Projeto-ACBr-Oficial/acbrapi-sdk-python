# NfeSefazTransp

Dados dos transportes da NF-e.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**mod_frete** | **int** | Modalidade do frete  * 0 - Contratação do Frete por conta do Remetente (CIF)  * 1 - Contratação do Frete por conta do destinatário/remetente (FOB)  * 2 - Contratação do Frete por conta de terceiros  * 3 - Transporte próprio por conta do remetente  * 4 - Transporte próprio por conta do destinatário  * 9 - Sem Ocorrência de transporte | 
**transporta** | [**NfeSefazTransporta**](NfeSefazTransporta.md) |  | [opcional] 
**ret_transp** | [**NfeSefazRetTransp**](NfeSefazRetTransp.md) |  | [opcional] 
**veic_transp** | [**NfeSefazVeiculo**](NfeSefazVeiculo.md) |  | [opcional] 
**reboque** | [**list[NfeSefazVeiculo]**](NfeSefazVeiculo.md) |  | [opcional] 
**vagao** | **str** | Identificação do vagão (v2.0). | [opcional] 
**balsa** | **str** | Identificação da balsa (v2.0). | [opcional] 
**vol** | [**list[NfeSefazVol]**](NfeSefazVol.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


