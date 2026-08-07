# NfcomSefazDest

Identificação do destinatário / assinante.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**x_nome** | **str** | Razão social ou Nome do destinatário. | 
**cnpj** | **str** | Número do CNPJ.  Informar os zeros não significativos. | [opcional] 
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [opcional] 
**id_outros** | **str** | Identificação do destinatário outros.  Identificação do destinatário não obrigado a inscrição do CPF tais como estrangeiro, indígena e quilombola  Em caso de não contar CPF do assinante, informar o RG. | [opcional] 
**ind_ie_dest** | **int** | Indicador da IE do Destinatário.  * 1 - Contribuinte ICMS (informar a IE do destinatário)  * 2 - Contribuinte isento de Inscrição no cadastro de Contribuintes do ICMS  * 9 - Não Contribuinte, que pode ou não possuir Inscrição Estadual no Cadastro de Contribuintes do ICMS  Nota: No caso de Contribuinte Isento de Inscrição (indIEDest&#x3D;2) informar a tag IE do destinatário com o literal ISENTO. | 
**ie** | **str** | Inscrição Estadual do destinatário. | [opcional] 
**im** | **str** | Inscrição Municipal. | [opcional] 
**ender_dest** | [**NfcomSefazEndeDest**](NfcomSefazEndeDest.md) |  | 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


