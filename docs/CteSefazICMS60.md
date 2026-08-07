# CteSefazICMS60

Tributação pelo ICMS60 - ICMS cobrado por substituição tributária.Responsabilidade do recolhimento do ICMS atribuído ao tomador ou 3º por ST.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cst** | **str** | Classificação Tributária do Serviço.  * 60 - ICMS cobrado por substituição tributária | 
**v_bcst_ret** | **float** | Valor da BC do ICMS ST retido.  Valor do frete sobre o qual será calculado o ICMS a ser substituído na Prestação. | 
**v_icmsst_ret** | **float** | Valor do ICMS ST retido.  Resultado da multiplicação do “vBCSTRet” x “pICMSSTRet” - que será valor do ICMS a ser retido pelo Substituto. Podendo o valor do ICMS a ser retido efetivamente, sofrer ajustes conforme a opção tributaria do transportador substituído. | 
**p_icmsst_ret** | **float** | Alíquota do ICMS.  Percentual de Alíquota incidente na prestação de serviço de transporte. | 
**v_cred** | **float** | Valor do Crédito outorgado/Presumido.  Preencher somente quando o transportador substituído, for optante pelo crédito outorgado previsto no Convênio 106/96 e corresponde ao percentual de 20%% do valor do ICMS ST retido. | [opcional] 
**v_icms_deson** | **float** | Valor do ICMS de desoneração. | [opcional] 
**c_benef** | **str** | Código de Benefício Fiscal na UF.  Código de Benefício Fiscal utilizado pela UF. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


