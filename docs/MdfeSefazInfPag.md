# MdfeSefazInfPag

Informações do Pagamento do Contrato.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**x_nome** | **str** | Razão social ou Nome do respnsável pelo pagamento. | [optional] 
**cpf** | **str** | Número do CPF do responsável pelo pgto.  Informar os zeros não significativos. | [optional] 
**cnpj** | **str** | Número do CNPJ do responsável pelo pgto.  Informar os zeros não significativos. | [optional] 
**id_estrangeiro** | **str** | Identificador do responsável pelo pgto em caso de ser estrangeiro. | [optional] 
**comp** | [**list[MdfeSefazComp]**](MdfeSefazComp.md) |  | 
**v_contrato** | **float** | Valor Total do Contrato. | 
**ind_alto_desemp** | **int** | Indicador de operação de transporte de alto desempenho.  Operação de transporte com utilização de veículos de frotas dedicadas ou fidelizadas.  Preencher com “1” para indicar operação de transporte de alto desempenho, demais casos não informar a tag. | [optional] 
**ind_pag** | **int** | Indicador da Forma de Pagamento:0-Pagamento à Vista  * 1 - Pagamento à Prazo | 
**v_adiant** | **float** | Valor do Adiantamento (usar apenas em pagamento à Prazo. | [optional] 
**ind_antecipa_adiant** | **int** | Indicador para declarar concordância em antecipar o adiantamento.  Informar a tag somente se for autorizado antecipar o adiantamento. | [optional] 
**inf_prazo** | [**list[MdfeSefazInfPrazo]**](MdfeSefazInfPrazo.md) |  | [optional] 
**tp_antecip** | **int** | Tipo de Permissão em relação a antecipação das parcelas.  * 0 - Não permite antecipar  * 1 - Permite antecipar as parcelas  * 2 - Permite antecipar as parcelas mediante confirmação | [optional] 
**inf_banc** | [**MdfeSefazInfBanc**](MdfeSefazInfBanc.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


