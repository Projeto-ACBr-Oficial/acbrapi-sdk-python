# NfeSefazProd

Dados dos produtos e serviços da NF-e.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**c_prod** | **str** | Código do produto ou serviço. Preencher com CFOP caso se trate de itens não relacionados com mercadorias/produto e que o contribuinte não possua codificação própria  Formato ”CFOP9999”. | 
**c_ean** | **str** | GTIN (Global Trade Item Number) do produto, antigo código EAN ou código de barras. | 
**c_barra** | **str** | Codigo de barras diferente do padrão GTIN. | [opcional] 
**x_prod** | **str** | Descrição do produto ou serviço. | 
**ncm** | **str** | Código NCM (8 posições), será permitida a informação do gênero (posição do capítulo do NCM) quando a operação não for de comércio exterior (importação/exportação) ou o produto não seja tributado pelo IPI. Em caso de item de serviço ou item que não tenham produto (Ex. transferência de crédito, crédito do ativo imobilizado, etc.), informar o código 00 (zeros) (v2.0). | 
**nve** | **list[str]** | Nomenclatura de Valor aduaneio e Estatístico. | [opcional] 
**cest** | **str** | Codigo especificador da Substuicao Tributaria - CEST, que identifica a mercadoria sujeita aos regimes de  substituicao tributária e de antecipação do recolhimento  do imposto. | [opcional] 
**ind_escala** | **str** |  | [opcional] 
**cnpj_fab** | **str** | CNPJ do Fabricante da Mercadoria, obrigatório para produto em escala NÃO relevante. | [opcional] 
**c_benef** | **str** |  | [opcional] 
**g_cred** | [**list[NfeSefazGCred]**](NfeSefazGCred.md) |  | [opcional] 
**tp_cred_pres_ibszfm** | **int** | Classificação para subapuração do IBS na ZFM. | [opcional] 
**extipi** | **str** | Código EX TIPI (3 posições). | [opcional] 
**cfop** | **str** | Cfop. | 
**u_com** | **str** | Unidade comercial. | 
**q_com** | **float** | Quantidade Comercial  do produto, alterado para aceitar de 0 a 4 casas decimais e 11 inteiros. | 
**v_un_com** | **float** | Valor unitário de comercialização  - alterado para aceitar 0 a 10 casas decimais e 11 inteiros. | 
**v_prod** | **float** | Valor bruto do produto ou serviço. | 
**c_ean_trib** | **str** | GTIN (Global Trade Item Number) da unidade tributável, antigo código EAN ou código de barras. | 
**c_barra_trib** | **str** | Código de barras da unidade tributável diferente do padrão GTIN. | [opcional] 
**u_trib** | **str** | Unidade Tributável. | 
**q_trib** | **float** | Quantidade Tributável - alterado para aceitar de 0 a 4 casas decimais e 11 inteiros. | 
**v_un_trib** | **float** | Valor unitário de tributação - alterado para aceitar 0 a 10 casas decimais e 11 inteiros. | 
**v_frete** | **float** | Valor Total do Frete. | [opcional] 
**v_seg** | **float** | Valor Total do Seguro. | [opcional] 
**v_desc** | **float** | Valor do Desconto. | [opcional] 
**v_outro** | **float** | Outras despesas acessórias. | [opcional] 
**ind_tot** | **int** | Este campo deverá ser preenchido com:  * 0 - o valor do item (vProd) não compõe o valor total da NF-e (vProd)  * 1 - o valor do item (vProd) compõe o valor total da NF-e (vProd) | 
**ind_bem_movel_usado** | **int** | Indicador de fornecimento de bem móvel usado: 1-Bem Móvel Usado. | [opcional] 
**di** | [**list[NfeSefazDI]**](NfeSefazDI.md) |  | [opcional] 
**det_export** | [**list[NfeSefazDetExport]**](NfeSefazDetExport.md) |  | [opcional] 
**x_ped** | **str** | pedido de compra - Informação de interesse do emissor para controle do B2B. | [opcional] 
**n_item_ped** | **int** | Número do Item do Pedido de Compra - Identificação do número do item do pedido de Compra. | [opcional] 
**n_fci** | **str** | Número de controle da FCI - Ficha de Conteúdo de Importação. | [opcional] 
**rastro** | [**list[NfeSefazRastro]**](NfeSefazRastro.md) |  | [opcional] 
**inf_prod_nff** | [**NfeSefazInfProdNFF**](NfeSefazInfProdNFF.md) |  | [opcional] 
**inf_prod_emb** | [**NfeSefazInfProdEmb**](NfeSefazInfProdEmb.md) |  | [opcional] 
**veic_prod** | [**NfeSefazVeicProd**](NfeSefazVeicProd.md) |  | [opcional] 
**med** | [**NfeSefazMed**](NfeSefazMed.md) |  | [opcional] 
**arma** | [**list[NfeSefazArma]**](NfeSefazArma.md) |  | [opcional] 
**comb** | [**NfeSefazComb**](NfeSefazComb.md) |  | [opcional] 
**n_recopi** | **str** | Número do RECOPI. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


