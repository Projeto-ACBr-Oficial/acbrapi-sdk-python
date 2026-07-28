# NfeSefazICMS53

Tributação monofásica sobre combustíveis com recolhimento diferido.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**orig** | **int** | Origem da mercadoria:  * 0 - Nacional, exceto as indicadas nos códigos 3, 4, 5 e 8;  * 1 - Estrangeira - Importação direta, exceto a indicada no código 6;  * 2 - Estrangeira - Adquirida no mercado interno, exceto a indicada no código 7;  * 3 - Nacional, mercadoria ou bem com Conteúdo de Importação superior a 40%% e inferior ou igual a 70%%;  * 4 - Nacional, cuja produção tenha sido feita em conformidade com os processos produtivos básicos de que tratam as legislações citadas nos Ajustes;  * 5 - Nacional, mercadoria ou bem com Conteúdo de Importação inferior ou igual a 40%%;  * 6 - Estrangeira - Importação direta, sem similar nacional, constante em lista da CAMEX e gás natural;  * 7 - Estrangeira - Adquirida no mercado interno, sem similar nacional, constante lista CAMEX e gás natural;  * 8 - Nacional, mercadoria ou bem com Conteúdo de Importação superior a 70%%. | 
**cst** | **str** | Tributção pelo ICMS  * 53 - Tributação monofásica sobre combustíveis com recolhimento diferido | 
**q_bc_mono** | **float** | Quantidade tributada. | [optional] 
**ad_rem_icms** | **float** | Alíquota ad rem do imposto. | [optional] 
**v_icms_mono_op** | **float** | Valor do ICMS da operação. | [optional] 
**p_dif** | **float** | Percentual do diferemento. | [optional] 
**v_icms_mono_dif** | **float** | Valor do ICMS diferido. | [optional] 
**v_icms_mono** | **float** | Valor do ICMS próprio devido. | [optional] 
**q_bc_mono_dif** | **float** | Quantidade tributada diferida.  OBS: Campo revogado pela NT2023.001v1.20 | [optional] 
**ad_rem_icms_dif** | **float** | Alíquota ad rem do imposto diferido.  OBS: Campo revogado pela NT2023.001v1.20 | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


