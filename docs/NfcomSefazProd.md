# NfcomSefazProd

Dados do Produto ou Serviço.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**c_prod** | **str** | Código do produto ou serviço. | 
**x_prod** | **str** | Descrição do produto ou serviço. | 
**c_class** | **str** | Código de classificação.  Tabela de Classificação de Item da NFCom (validar por RV). | 
**cfop** | **str** | CFOP.  Utilizar Tabela de CFOP. | [optional] 
**cnpjld** | **str** | CNPJ da operadora LD.  Informar o CNPJ da operadora LD que irá lançar o item de cofaturamento em nota do tipo faturamento 2. | [optional] 
**u_med** | **int** | Unidade Básica de Medida.  * 1 - Minuto  * 2 - MB  * 3 - GB  * 4 - UN | 
**q_faturada** | **float** | Quantidade Faturada.  Informar a quantidade de comercialização do produto . | 
**v_item** | **float** | Valor unitário do item. | 
**v_desc** | **float** | Valor do Desconto. | [optional] 
**v_outro** | **float** | Outras despesas acessórias. | [optional] 
**v_prod** | **float** | Valor total do item. | 
**d_expiracao** | **date** | Data de expiração de crédito.  Formato AAAA-MM-DD. | [optional] 
**ind_devolucao** | **int** | Indicador de devolução do valor do item.  * 1 - Devolução do valor do item | [optional] 
**cnpj_cobr_terc** | **str** | CNPJ de cobrança de terceiro.  Informar quando cClass do grupo 110 - Cobrança de terceiros. | [optional] 
**g_pag_antecipado** | [**NfcomSefazGPagAntecipado**](NfcomSefazGPagAntecipado.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


