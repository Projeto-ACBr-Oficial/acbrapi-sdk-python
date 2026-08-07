# NfcomSefazProd

Dados do Produto ou Serviço.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**c_prod** | **str** | Código do produto ou serviço. | 
**x_prod** | **str** | Descrição do produto ou serviço. | 
**c_class** | **str** | Código de classificação.  Tabela de Classificação de Item da NFCom (validar por RV). | 
**cfop** | **str** | CFOP.  Utilizar Tabela de CFOP. | [opcional] 
**cnpjld** | **str** | CNPJ da operadora LD.  Informar o CNPJ da operadora LD que irá lançar o item de cofaturamento em nota do tipo faturamento 2. | [opcional] 
**u_med** | **int** | Unidade Básica de Medida.  * 1 - Minuto  * 2 - MB  * 3 - GB  * 4 - UN | 
**q_faturada** | **float** | Quantidade Faturada.  Informar a quantidade de comercialização do produto . | 
**v_item** | **float** | Valor unitário do item. | 
**v_desc** | **float** | Valor do Desconto. | [opcional] 
**v_outro** | **float** | Outras despesas acessórias. | [opcional] 
**v_prod** | **float** | Valor total do item. | 
**d_expiracao** | **date** | Data de expiração de crédito.  Formato AAAA-MM-DD. | [opcional] 
**ind_devolucao** | **int** | Indicador de devolução do valor do item.  * 1 - Devolução do valor do item | [opcional] 
**cnpj_cobr_terc** | **str** | CNPJ de cobrança de terceiro.  Informar quando cClass do grupo 110 - Cobrança de terceiros. | [opcional] 
**g_pag_antecipado** | [**NfcomSefazGPagAntecipado**](NfcomSefazGPagAntecipado.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


