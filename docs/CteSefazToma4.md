# CteSefazToma4

Indicador do \"papel\" do tomador do serviço no CT-e.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**toma** | **int** | Tomador do Serviço.  Preencher com:  * 4 - Outros  Obs: Informar os dados cadastrais do tomador do serviço. | 
**cnpj** | **str** | Número do CNPJ.  Em caso de empresa não estabelecida no Brasil, será informado o CNPJ com zeros.  Informar os zeros não significativos. | [optional] 
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [optional] 
**ie** | **str** | Inscrição Estadual.  Informar a IE do tomador ou ISENTO se tomador é contribuinte do ICMS isento de inscrição no cadastro de contribuintes do ICMS. Caso o tomador não seja contribuinte do ICMS não informar o conteúdo. | [optional] 
**x_nome** | **str** | Razão Social ou Nome. | 
**x_fant** | **str** | Nome Fantasia. | [optional] 
**fone** | **str** | Telefone. | [optional] 
**ender_toma** | [**CteSefazEndereco**](CteSefazEndereco.md) |  | 
**email** | **str** | Endereço de email. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


