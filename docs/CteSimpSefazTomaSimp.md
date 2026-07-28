# CteSimpSefazTomaSimp

Identificação do tomador do serviço no CT-e.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**toma** | **int** | Tomador do Serviço.  Preencher com:  * 0 - Remetente  * 1 - Expedidor  * 2 - Recebedor  * 3 - Destinatário  * 4 - Terceiro | 
**ind_ie_toma** | **int** | Indicador do papel do tomador na prestação do serviço:  * 1 - Contribuinte ICMS  * 2 - Contribuinte isento de inscrição  * 9 - Não Contribuinte  Aplica-se ao tomador que for indicado no toma. | 
**cnpj** | **str** | Número do CNPJ.  Em caso de empresa não estabelecida no Brasil, será informado o CNPJ com zeros.  Informar os zeros não significativos. | [optional] 
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [optional] 
**ie** | **str** | Inscrição Estadual.  Informar a IE do tomador ou ISENTO se tomador é contribuinte do ICMS isento de inscrição no cadastro de contribuintes do ICMS. Caso o tomador não seja contribuinte do ICMS não informar o conteúdo. | [optional] 
**x_nome** | **str** | Razão Social ou Nome. | 
**isuf** | **str** | Inscrição na SUFRAMA.  (Obrigatório nas operações com as áreas com benefícios de incentivos fiscais sob controle da SUFRAMA). | [optional] 
**fone** | **str** | Telefone. | [optional] 
**ender_toma** | [**CteSimpSefazEnderecoSimp**](CteSimpSefazEnderecoSimp.md) |  | 
**email** | **str** | Endereço de email. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


