# CteSefazRem

Informações do Remetente das mercadorias transportadas pelo CT-e.  Poderá não ser informado para os CT-e de redespacho intermediário e serviço vinculado a multimodal. Nos demais casos deverá sempre ser informado.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número do CNPJ.  Em caso de empresa não estabelecida no Brasil, será informado o CNPJ com zeros.  Informar os zeros não significativos. | [opcional] 
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [opcional] 
**ie** | **str** | Inscrição Estadual.  Informar a IE do remetente ou ISENTO se remetente é contribuinte do ICMS isento de inscrição no cadastro de contribuintes do ICMS. Caso o remetente não seja contribuinte do ICMS não informar a tag. | [opcional] 
**x_nome** | **str** | Razão social ou nome do remetente. | 
**x_fant** | **str** | Nome fantasia. | [opcional] 
**fone** | **str** | Telefone. | [opcional] 
**ender_reme** | [**CteSefazEndereco**](CteSefazEndereco.md) |  | 
**email** | **str** | Endereço de email. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


