# CteOsSefazTomaOS

Informações do Tomador/Usuário do Serviço.  Opcional para Excesso de Bagagem.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número do CNPJ.  Em caso de empresa não estabelecida no Brasil, será informado o CNPJ com zeros.  Informar os zeros não significativos. | [opcional] 
**cpf** | **str** | Número do CPF.  Informar os zeros não significativos. | [opcional] 
**ie** | **str** | Inscrição Estadual.  Informar a IE do tomador ou ISENTO se tomador é contribuinte do ICMS isento de inscrição no cadastro de contribuintes do ICMS. Caso o tomador não seja contribuinte do ICMS não informar o conteúdo. | [opcional] 
**x_nome** | **str** | Razão social ou nome do tomador. | 
**x_fant** | **str** | Nome fantasia. | [opcional] 
**fone** | **str** | Telefone. | [opcional] 
**ender_toma** | [**CteOsSefazEnderecoOS**](CteOsSefazEnderecoOS.md) |  | 
**email** | **str** | Endereço de email. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


