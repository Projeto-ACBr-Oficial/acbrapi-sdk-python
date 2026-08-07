# CteSimpSefazDetSimp

Detalhamento das entregas / prestações do CTe Simplificado.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**n_item** | **int** | Número identificador do item agrupador da prestação. | 
**c_mun_ini** | **str** | Código do Município de início da prestação.  Utilizar a tabela do IBGE. Informar 9999999 para operações com o exterior. | 
**x_mun_ini** | **str** | Nome do Município do início da prestação.  Informar &#39;EXTERIOR&#39; para operações com o exterior. | 
**c_mun_fim** | **str** | Código do Município de término da prestação.  Utilizar a tabela do IBGE. Informar 9999999 para operações com o exterior. | 
**x_mun_fim** | **str** | Nome do Município do término da prestação.  Informar &#39;EXTERIOR&#39; para operações com o exterior. | 
**v_prest** | **float** | Valorl da Prestação do Serviço.  Pode conter zeros quando o CT-e for de complemento de ICMS. | 
**v_rec** | **float** | Valor a Receber. | 
**comp** | [**list[CteSimpSefazCompSimp]**](CteSimpSefazCompSimp.md) |  | [opcional] 
**inf_nfe** | [**list[CteSimpSefazInfNFeSimp]**](CteSimpSefazInfNFeSimp.md) |  | [opcional] 
**inf_doc_ant** | [**list[CteSimpSefazInfDocAntSimp]**](CteSimpSefazInfDocAntSimp.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


