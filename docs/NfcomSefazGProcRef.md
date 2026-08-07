# NfcomSefazGProcRef

Grupo Processo referenciado.  Este grupo somente deverá ser preenchido quando houver processo judicial ou administrativo que altere valores.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**v_item** | **float** | Valor unitário do item.  Informar o valor sem a influência da decisão judicial/administrativa. | 
**q_faturada** | **float** | Quantidade Faturada.  Informar a quantidade de comercialização do produto . | 
**v_prod** | **float** | Valor total do item. | 
**v_desc** | **float** | Valor do Desconto. | [opcional] 
**v_outro** | **float** | Outras despesas acessórias. | [opcional] 
**ind_devolucao** | **int** | Indicador de devolução do valor do item.  * 1 - Devolução do valor do item | [opcional] 
**v_bc** | **float** | Valor da BC do ICMS. | [opcional] 
**p_icms** | **float** | Alíquota do ICMS. | [opcional] 
**v_icms** | **float** | Valor do ICMS. | [opcional] 
**v_pis** | **float** | Valor do PIS. | [opcional] 
**v_cofins** | **float** | Valor do COFINS. | [opcional] 
**v_fcp** | **float** | Valor do Fundo de Combate à Pobreza (FCP). | [opcional] 
**g_proc** | [**list[NfcomSefazGProc]**](NfcomSefazGProc.md) |  | 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


