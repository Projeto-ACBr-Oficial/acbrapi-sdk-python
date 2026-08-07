# CteSefazExped

Informações do Expedidor da Carga.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número do CNPJ.  Em caso de empresa não estabelecida no Brasil, será informado o CNPJ com zeros.  Informar os zeros não significativos. | [opcional] 
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [opcional] 
**ie** | **str** | Inscrição Estadual.  Informar a IE do expedidor ou ISENTO se expedidor é contribuinte do ICMS isento de inscrição no cadastro de contribuintes do ICMS. Caso o expedidor não seja contribuinte do ICMS não informar a tag. | [opcional] 
**x_nome** | **str** | Razão Social ou Nome. | 
**fone** | **str** | Telefone. | [opcional] 
**ender_exped** | [**CteSefazEndereco**](CteSefazEndereco.md) |  | 
**email** | **str** | Endereço de email. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


