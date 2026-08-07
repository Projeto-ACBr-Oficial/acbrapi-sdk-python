# CteOsSefazPropOS

Proprietário ou possuidor do Veículo.  Só preenchido quando o veículo não pertencer à empresa emitente do CT-e OS.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [opcional] 
**cnpj** | **str** | Número do CNPJ.  Informar os zeros não significativos. | [opcional] 
**taf** | **str** | Termo de Autorização de Fretamento - TAF.  De acordo com a Resolução ANTT nº 4.777/2015. | [opcional] 
**nro_reg_estadual** | **str** | Número do Registro Estadual.  Registro obrigatório do emitente do CT-e OS junto à Agência Reguladora  Estadual. | [opcional] 
**x_nome** | **str** | Razão Social ou Nome do proprietário. | 
**ie** | **str** | Inscrição Estadual. | [opcional] 
**uf** | **str** | UF. | [opcional] 
**tp_prop** | **int** | Tipo Proprietário ou possuidor.  Preencher com:  * 0 - TAC - Agregado  * 1 - TAC Independente  ou  * 2 - Outros | 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


