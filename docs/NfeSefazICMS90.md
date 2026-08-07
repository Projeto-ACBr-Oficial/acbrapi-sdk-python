# NfeSefazICMS90

Tributação pelo ICMS  * 90 - Outras

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**orig** | **int** | Origem da mercadoria:  * 0 - Nacional, exceto as indicadas nos códigos 3, 4, 5 e 8;  * 1 - Estrangeira - Importação direta, exceto a indicada no código 6;  * 2 - Estrangeira - Adquirida no mercado interno, exceto a indicada no código 7;  * 3 - Nacional, mercadoria ou bem com Conteúdo de Importação superior a 40%% e inferior ou igual a 70%%;  * 4 - Nacional, cuja produção tenha sido feita em conformidade com os processos produtivos básicos de que tratam as legislações citadas nos Ajustes;  * 5 - Nacional, mercadoria ou bem com Conteúdo de Importação inferior ou igual a 40%%;  * 6 - Estrangeira - Importação direta, sem similar nacional, constante em lista da CAMEX e gás natural;  * 7 - Estrangeira - Adquirida no mercado interno, sem similar nacional, constante lista CAMEX e gás natural;  * 8 - Nacional, mercadoria ou bem com Conteúdo de Importação superior a 70%%. | 
**cst** | **str** | Tributção pelo ICMS  * 90 - Outras | 
**mod_bc** | **int** | Modalidade de determinação da BC do ICMS:  * 0 - Margem Valor Agregado (%%)  * 1 - Pauta (valor)  * 2 - Preço Tabelado Máximo (valor)  * 3 - Valor da Operação | [opcional] 
**v_bc** | **float** | Valor da BC do ICMS. | [opcional] 
**p_red_bc** | **float** | Percentual de redução da BC. | [opcional] 
**c_benef_rbc** | **str** | Código de Benefício Fiscal na UF aplicado ao item quando houver RBC. | [opcional] 
**p_icms** | **float** | Alíquota do ICMS. | [opcional] 
**v_icmsop** | **float** | Valor do ICMS da Operação. | [opcional] 
**p_dif** | **float** | Percentual do diferemento. | [opcional] 
**v_icms_dif** | **float** | Valor do ICMS da diferido. | [opcional] 
**v_icms** | **float** | Valor do ICMS. | [opcional] 
**v_bcfcp** | **float** | Valor da Base de cálculo do FCP. | [opcional] 
**p_fcp** | **float** | Percentual de ICMS relativo ao Fundo de Combate à Pobreza (FCP). | [opcional] 
**v_fcp** | **float** | Valor do ICMS relativo ao Fundo de Combate à Pobreza (FCP). | [opcional] 
**p_fcp_dif** | **float** | Percentual do diferimento do ICMS relativo ao Fundo de Combate à Pobreza (FCP). | [opcional] 
**v_fcp_dif** | **float** | Valor do ICMS relativo ao Fundo de Combate à Pobreza (FCP) diferido. | [opcional] 
**v_fcp_efet** | **float** | Valor efetivo do ICMS relativo ao Fundo de Combate à Pobreza (FCP). | [opcional] 
**mod_bcst** | **int** | Modalidade de determinação da BC do ICMS ST:  * 0 - Preço tabelado ou máximo  sugerido  * 1 - Lista Negativa (valor)  * 2 - Lista Positiva (valor)  * 3 - Lista Neutra (valor)  * 4 - Margem Valor Agregado (%%)  * 5 - Pauta (valor)  * 6 - Valor da Operação | [opcional] 
**p_mvast** | **float** | Percentual da Margem de Valor Adicionado ICMS ST. | [opcional] 
**p_red_bcst** | **float** | Percentual de redução da BC ICMS ST. | [opcional] 
**v_bcst** | **float** | Valor da BC do ICMS ST. | [opcional] 
**p_icmsst** | **float** | Alíquota do ICMS ST. | [opcional] 
**v_icmsst** | **float** | Valor do ICMS ST. | [opcional] 
**v_bcfcpst** | **float** | Valor da Base de cálculo do FCP. | [opcional] 
**p_fcpst** | **float** | Percentual de FCP retido por substituição tributária. | [opcional] 
**v_fcpst** | **float** | Valor do FCP retido por substituição tributária. | [opcional] 
**v_icms_deson** | **float** | Valor do ICMS de desoneração. | [opcional] 
**mot_des_icms** | **int** | Motivo da desoneração do ICMS:3-Uso na agropecuária  * 9 - Outros  * 12 - Fomento agropecuário | [opcional] 
**ind_deduz_deson** | **int** | Indica se o valor do ICMS desonerado (vICMSDeson) deduz do valor do item (vProd):  * 0 - Valor do ICMS desonerado (vICMSDeson) não deduz do valor do item (vProd) / total da NF-e  * 1 - Valor do ICMS desonerado (vICMSDeson) deduz do valor do item (vProd) / total da NF-e | [opcional] 
**v_icmsst_deson** | **float** | Valor do ICMS-ST desonerado. | [opcional] 
**mot_des_icmsst** | **int** | Motivo da desoneração do ICMS-ST: 3-Uso na agropecuária  * 9 - Outros  * 12 - Fomento agropecuário | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


