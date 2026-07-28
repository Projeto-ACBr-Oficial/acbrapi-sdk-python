# NfcomSefazDest

Identificação do destinatário / assinante.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**x_nome** | **str** | Razão social ou Nome do destinatário. | 
**cnpj** | **str** | Número do CNPJ.  Informar os zeros não significativos. | [optional] 
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [optional] 
**id_outros** | **str** | Identificação do destinatário outros.  Identificação do destinatário não obrigado a inscrição do CPF tais como estrangeiro, indígena e quilombola  Em caso de não contar CPF do assinante, informar o RG. | [optional] 
**ind_ie_dest** | **int** | Indicador da IE do Destinatário.  * 1 - Contribuinte ICMS (informar a IE do destinatário)  * 2 - Contribuinte isento de Inscrição no cadastro de Contribuintes do ICMS  * 9 - Não Contribuinte, que pode ou não possuir Inscrição Estadual no Cadastro de Contribuintes do ICMS  Nota: No caso de Contribuinte Isento de Inscrição (indIEDest&#x3D;2) informar a tag IE do destinatário com o literal ISENTO. | 
**ie** | **str** | Inscrição Estadual do destinatário. | [optional] 
**im** | **str** | Inscrição Municipal. | [optional] 
**ender_dest** | [**NfcomSefazEndeDest**](NfcomSefazEndeDest.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


