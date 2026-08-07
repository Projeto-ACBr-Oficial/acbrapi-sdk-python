# MdfeSefazInfPag

Informações do Pagamento do Contrato.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**x_nome** | **str** | Razão social ou Nome do respnsável pelo pagamento. | [opcional] 
**cpf** | **str** | Número do CPF do responsável pelo pgto.  Informar os zeros não significativos. | [opcional] 
**cnpj** | **str** | Número do CNPJ do responsável pelo pgto.  Informar os zeros não significativos. | [opcional] 
**id_estrangeiro** | **str** | Identificador do responsável pelo pgto em caso de ser estrangeiro. | [opcional] 
**comp** | [**list[MdfeSefazComp]**](MdfeSefazComp.md) |  | 
**v_contrato** | **float** | Valor Total do Contrato. | 
**ind_alto_desemp** | **int** | Indicador de operação de transporte de alto desempenho.  Operação de transporte com utilização de veículos de frotas dedicadas ou fidelizadas.  Preencher com “1” para indicar operação de transporte de alto desempenho, demais casos não informar a tag. | [opcional] 
**ind_pag** | **int** | Indicador da Forma de Pagamento:0-Pagamento à Vista  * 1 - Pagamento à Prazo | 
**v_adiant** | **float** | Valor do Adiantamento (usar apenas em pagamento à Prazo. | [opcional] 
**ind_antecipa_adiant** | **int** | Indicador para declarar concordância em antecipar o adiantamento.  Informar a tag somente se for autorizado antecipar o adiantamento. | [opcional] 
**inf_prazo** | [**list[MdfeSefazInfPrazo]**](MdfeSefazInfPrazo.md) |  | [opcional] 
**tp_antecip** | **int** | Tipo de Permissão em relação a antecipação das parcelas.  * 0 - Não permite antecipar  * 1 - Permite antecipar as parcelas  * 2 - Permite antecipar as parcelas mediante confirmação | [opcional] 
**inf_banc** | [**MdfeSefazInfBanc**](MdfeSefazInfBanc.md) |  | 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


