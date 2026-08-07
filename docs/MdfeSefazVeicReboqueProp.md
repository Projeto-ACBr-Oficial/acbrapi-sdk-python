# MdfeSefazVeicReboqueProp

Proprietários ou possuidor do Veículo.  Só preenchido quando o veículo não pertencer à empresa emitente do MDF-e.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [opcional] 
**cnpj** | **str** | Número do CNPJ.  Informar os zeros não significativos. | [opcional] 
**rntrc** | **str** | Registro Nacional dos Transportadores Rodoviários de Carga.  Registro obrigatório do proprietário, co-proprietário ou arrendatário do veículo junto à ANTT para exercer a atividade de transportador rodoviário de cargas por conta de terceiros e mediante remuneração. | 
**x_nome** | **str** | Razão Social ou Nome do proprietário. | 
**ie** | **str** | Inscrição Estadual. | [opcional] 
**uf** | **str** | UF. | [opcional] 
**tp_prop** | **int** | Tipo Proprietário ou possuidor.  Preencher com:  * 0 - TAC Agregado  * 1 - TAC Independente  * 2 - Outros | 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


