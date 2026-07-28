# CteOsSefazTomaOS

Informações do Tomador/Usuário do Serviço.  Opcional para Excesso de Bagagem.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número do CNPJ.  Em caso de empresa não estabelecida no Brasil, será informado o CNPJ com zeros.  Informar os zeros não significativos. | [optional] 
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [optional] 
**ie** | **str** | Inscrição Estadual.  Informar a IE do tomador ou ISENTO se tomador é contribuinte do ICMS isento de inscrição no cadastro de contribuintes do ICMS. Caso o tomador não seja contribuinte do ICMS não informar o conteúdo. | [optional] 
**x_nome** | **str** | Razão social ou nome do tomador. | 
**x_fant** | **str** | Nome fantasia. | [optional] 
**fone** | **str** | Telefone. | [optional] 
**ender_toma** | [**CteOsSefazEnderecoOS**](CteOsSefazEnderecoOS.md) |  | 
**email** | **str** | Endereço de email. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


