# CteSefazToma4

Indicador do \"papel\" do tomador do serviço no CT-e.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**toma** | **int** | Tomador do Serviço.  Preencher com:  * 4 - Outros  Obs: Informar os dados cadastrais do tomador do serviço. | 
**cnpj** | **str** | Número do CNPJ.  Em caso de empresa não estabelecida no Brasil, será informado o CNPJ com zeros.  Informar os zeros não significativos. | [opcional] 
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [opcional] 
**ie** | **str** | Inscrição Estadual.  Informar a IE do tomador ou ISENTO se tomador é contribuinte do ICMS isento de inscrição no cadastro de contribuintes do ICMS. Caso o tomador não seja contribuinte do ICMS não informar o conteúdo. | [opcional] 
**x_nome** | **str** | Razão Social ou Nome. | 
**x_fant** | **str** | Nome Fantasia. | [opcional] 
**fone** | **str** | Telefone. | [opcional] 
**ender_toma** | [**CteSefazEndereco**](CteSefazEndereco.md) |  | 
**email** | **str** | Endereço de email. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


