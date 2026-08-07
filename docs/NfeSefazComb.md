# NfeSefazComb

Informar apenas para operações com combustíveis líquidos.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**c_prod_anp** | **int** | Código de produto da ANP. codificação de produtos do SIMP (http://www.anp.gov.br). | 
**desc_anp** | **str** | Descrição do Produto conforme ANP. Utilizar a descrição de produtos do Sistema de Informações de Movimentação de Produtos - SIMP (http://www.anp.gov.br/simp/). | 
**p_glp** | **float** | Percentual do GLP derivado do petróleo no produto GLP (cProdANP&#x3D;210203001). Informar em número decimal o percentual do GLP derivado de petróleo no produto GLP. Valores 0 a 100. | [opcional] 
**p_gnn** | **float** | Percentual de gás natural nacional - GLGNn para o produto GLP (cProdANP&#x3D;210203001). Informar em número decimal o percentual do Gás Natural Nacional - GLGNn para o produto GLP. Valores de 0 a 100. | [opcional] 
**p_gni** | **float** | Percentual de gás natural importado GLGNi para o produto GLP (cProdANP&#x3D;210203001). Informar em número deciaml o percentual do Gás Natural Importado - GLGNi para o produto GLP. Valores de 0 a 100. | [opcional] 
**v_part** | **float** | Valor de partida (cProdANP&#x3D;210203001). Deve ser informado neste campo o valor por quilograma sem ICMS. | [opcional] 
**codif** | **str** | Código de autorização / registro do CODIF. Informar apenas quando a UF utilizar o CODIF (Sistema de Controle do    Diferimento do Imposto nas Operações com AEAC - Álcool Etílico Anidro Combustível). | [opcional] 
**q_temp** | **float** | Quantidade de combustível  faturada à temperatura ambiente.  Informar quando a quantidade  faturada informada no campo  qCom (I10) tiver sido ajustada para  uma temperatura diferente da  ambiente. | [opcional] 
**uf_cons** | **str** | Sigla da UF de Consumo. | 
**cide** | [**NfeSefazCIDE**](NfeSefazCIDE.md) |  | [opcional] 
**encerrante** | [**NfeSefazEncerrante**](NfeSefazEncerrante.md) |  | [opcional] 
**p_bio** | **float** | Percentual do índice de mistura do Biodiesel (B100) no Óleo Diesel B instituído pelo órgão regulamentador. | [opcional] 
**orig_comb** | [**list[NfeSefazOrigComb]**](NfeSefazOrigComb.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


