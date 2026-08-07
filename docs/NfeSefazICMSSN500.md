# NfeSefazICMSSN500

Tributação do ICMS pelo SIMPLES NACIONAL,CRT=1 - Simples Nacional e CSOSN=500 (v.2.0).

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**orig** | **int** | Origem da mercadoria:  * 0 - Nacional, exceto as indicadas nos códigos 3, 4, 5 e 8;  * 1 - Estrangeira - Importação direta, exceto a indicada no código 6;  * 2 - Estrangeira - Adquirida no mercado interno, exceto a indicada no código 7;  * 3 - Nacional, mercadoria ou bem com Conteúdo de Importação superior a 40%% e inferior ou igual a 70%%;  * 4 - Nacional, cuja produção tenha sido feita em conformidade com os processos produtivos básicos de que tratam as legislações citadas nos Ajustes;  * 5 - Nacional, mercadoria ou bem com Conteúdo de Importação inferior ou igual a 40%%;  * 6 - Estrangeira - Importação direta, sem similar nacional, constante em lista da CAMEX e gás natural;  * 7 - Estrangeira - Adquirida no mercado interno, sem similar nacional, constante lista CAMEX e gás natural;  * 8 - Nacional, mercadoria ou bem com Conteúdo de Importação superior a 70%%. | 
**csosn** | **str** | * 500 - ICMS cobrado anterirmente por substituição tributária (substituído) ou por antecipação  (v.2.0). | 
**v_bcst_ret** | **float** | Valor da BC do ICMS ST retido anteriormente (v2.0). | [opcional] 
**p_st** | **float** | Aliquota suportada pelo consumidor final. | [opcional] 
**v_icms_substituto** | **float** | Valor do ICMS próprio do substituto. | [opcional] 
**v_icmsst_ret** | **float** | Valor do ICMS ST retido anteriormente  (v2.0). | [opcional] 
**v_bcfcpst_ret** | **float** | Valor da Base de cálculo do FCP retido anteriormente. | [opcional] 
**p_fcpst_ret** | **float** | Percentual de FCP retido anteriormente por substituição tributária. | [opcional] 
**v_fcpst_ret** | **float** | Valor do FCP retido por substituição tributária. | [opcional] 
**p_red_bc_efet** | **float** | Percentual de redução da base de cálculo efetiva. | [opcional] 
**v_bc_efet** | **float** | Valor da base de cálculo efetiva. | [opcional] 
**p_icms_efet** | **float** | Alíquota do ICMS efetiva. | [opcional] 
**v_icms_efet** | **float** | Valor do ICMS efetivo. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


