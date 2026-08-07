# DfeContribuinteInfCad

Informações cadastrais do contribuinte consultado.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**ie** | **str** | Número da Inscrição Estadual do contribuinte. | 
**cnpj** | **str** | Número do CNPJ  do contribuinte. | [opcional] 
**cpf** | **str** | Número do CPF do contribuinte. | [opcional] 
**uf** | **str** | Sigla da UF de localização do contribuinte. Em algumas situações, a UF de localização pode ser diferente da UF consultada. Ex. IE de Substituto Tributário. | 
**situacao_cadastral** | **int** | Situação cadastral do contribuinte:  * 0 - não habilitado  * 1 - habilitado | 
**indicador_nfe** | **int** | Indicador de contribuinte credenciado a emitir NF-e.  * 0 - Não credenciado para emissão da NF-e  * 1 - Credenciado  * 2 - Credenciado com obrigatoriedade para todas operações  * 3 - Credenciado com obrigatoriedade parcial  * 4 - a SEFAZ não fornece a informação  Este indicador significa apenas que o contribuinte é credenciado para emitir NF-e na SEFAZ consultada. | 
**indicador_cte** | **int** | Indicador de contribuinte credenciado a emitir CT-e.  * 0 - Não credenciado para emissão da CT-e  * 1 - Credenciado  * 2 - Credenciado com obrigatoriedade para todas operações  * 3 - Credenciado com obrigatoriedade parcial  * 4 - a SEFAZ não fornece a informação  Este indicador significa apenas que o contribuinte é credenciado para emitir CT-e na SEFAZ consultada. | 
**nome_razao_social** | **str** | Razão Social ou nome do contribuinte. | 
**nome_fantasia** | **str** | Razão Social ou nome do contribuinte. | [opcional] 
**regime_apuracao_icms** | **str** | Regime de Apuração do ICMS. | [opcional] 
**cnae** | **str** | CNAE Fiscal do contribuinte. | [opcional] 
**data_inicio_atividade** | **date** | Data de início de atividades do contribuinte. | [opcional] 
**data_situacao_cadastral** | **date** | Data da última modificação da situação cadastral do contribuinte. | [opcional] 
**data_fim_atividade** | **date** | Data de ocorrência da baixa do contribuinte. | [opcional] 
**ie_unica** | **str** | Inscrição Estadual Única. | [opcional] 
**ie_atual** | **str** | Inscrição Estadual atual. | [opcional] 
**endereco** | [**DfeContribuinteEndereco**](DfeContribuinteEndereco.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


