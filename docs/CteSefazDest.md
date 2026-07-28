# CteSefazDest

Informações do Destinatário do CT-e.  Poderá não ser informado para os CT-e de redespacho intermediário e serviço vinculado a multimodal. Nos demais casos deverá sempre ser informado.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número do CNPJ.  Em caso de empresa não estabelecida no Brasil, será informado o CNPJ com zeros.  Informar os zeros não significativos. | [optional] 
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [optional] 
**ie** | **str** | Inscrição Estadual.  Informar a IE do destinatário ou ISENTO se destinatário é contribuinte do ICMS isento de inscrição no cadastro de contribuintes do ICMS. Caso o destinatário não seja contribuinte do ICMS não informar o conteúdo. | [optional] 
**x_nome** | **str** | Razão Social ou Nome do destinatário. | 
**fone** | **str** | Telefone. | [optional] 
**isuf** | **str** | Inscrição na SUFRAMA.  (Obrigatório nas operações com as áreas com benefícios de incentivos fiscais sob controle da SUFRAMA). | [optional] 
**ender_dest** | [**CteSefazEndereco**](CteSefazEndereco.md) |  | 
**email** | **str** | Endereço de email. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


