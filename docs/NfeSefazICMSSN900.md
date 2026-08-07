# NfeSefazICMSSN900

Tributação do ICMS pelo SIMPLES NACIONAL, CRT=1 - Simples Nacional, CRT=4 - MEI e CSOSN=900 (v2.0).

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**orig** | **int** | Origem da mercadoria:  * 0 - Nacional, exceto as indicadas nos códigos 3, 4, 5 e 8;  * 1 - Estrangeira - Importação direta, exceto a indicada no código 6;  * 2 - Estrangeira - Adquirida no mercado interno, exceto a indicada no código 7;  * 3 - Nacional, mercadoria ou bem com Conteúdo de Importação superior a 40%% e inferior ou igual a 70%%;  * 4 - Nacional, cuja produção tenha sido feita em conformidade com os processos produtivos básicos de que tratam as legislações citadas nos Ajustes;  * 5 - Nacional, mercadoria ou bem com Conteúdo de Importação inferior ou igual a 40%%;  * 6 - Estrangeira - Importação direta, sem similar nacional, constante em lista da CAMEX e gás natural;  * 7 - Estrangeira - Adquirida no mercado interno, sem similar nacional, constante lista CAMEX e gás natural;  * 8 - Nacional, mercadoria ou bem com Conteúdo de Importação superior a 70%%. | 
**csosn** | **str** | Tributação pelo ICMS 900 - Outros(v2.0). | 
**mod_bc** | **int** | Modalidade de determinação da BC do ICMS:  * 0 - Margem Valor Agregado (%%)  * 1 - Pauta (valor)  * 2 - Preço Tabelado Máximo (valor)  * 3 - Valor da Operação | [opcional] 
**v_bc** | **float** | Valor da BC do ICMS. | [opcional] 
**p_red_bc** | **float** | Percentual de redução da BC. | [opcional] 
**p_icms** | **float** | Alíquota do ICMS. | [opcional] 
**v_icms** | **float** | Valor do ICMS. | [opcional] 
**mod_bcst** | **int** | Modalidade de determinação da BC do ICMS ST:  * 0 - Preço tabelado ou máximo  sugerido  * 1 - Lista Negativa (valor)  * 2 - Lista Positiva (valor)  * 3 - Lista Neutra (valor)  * 4 - Margem Valor Agregado (%%)  * 5 - Pauta (valor)  * 6 - Valor da Operação | [opcional] 
**p_mvast** | **float** | Percentual da Margem de Valor Adicionado ICMS ST. | [opcional] 
**p_red_bcst** | **float** | Percentual de redução da BC ICMS ST. | [opcional] 
**v_bcst** | **float** | Valor da BC do ICMS ST. | [opcional] 
**p_icmsst** | **float** | Alíquota do ICMS ST. | [opcional] 
**v_icmsst** | **float** | Valor do ICMS ST. | [opcional] 
**v_bcfcpst** | **float** | Valor da Base de cálculo do FCP. | [opcional] 
**p_fcpst** | **float** | Percentual de FCP retido por substituição tributária. | [opcional] 
**v_fcpst** | **float** | Valor do FCP retido por substituição tributária. | [opcional] 
**p_cred_sn** | **float** | Alíquota aplicável de cálculo do crédito (Simples Nacional). (v2.0). | [opcional] 
**v_cred_icmssn** | **float** | Valor crédito do ICMS que pode ser aproveitado nos termos do art. 23 da LC 123 (Simples Nacional) (v2.0). | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


