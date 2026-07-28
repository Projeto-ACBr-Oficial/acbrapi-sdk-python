# CteSefazExped

Informações do Expedidor da Carga.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número do CNPJ.  Em caso de empresa não estabelecida no Brasil, será informado o CNPJ com zeros.  Informar os zeros não significativos. | [optional] 
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [optional] 
**ie** | **str** | Inscrição Estadual.  Informar a IE do expedidor ou ISENTO se expedidor é contribuinte do ICMS isento de inscrição no cadastro de contribuintes do ICMS. Caso o expedidor não seja contribuinte do ICMS não informar a tag. | [optional] 
**x_nome** | **str** | Razão Social ou Nome. | 
**fone** | **str** | Telefone. | [optional] 
**ender_exped** | [**CteSefazEndereco**](CteSefazEndereco.md) |  | 
**email** | **str** | Endereço de email. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


