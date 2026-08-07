# NfeSefazEmit

Identificação do emitente.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número do CNPJ do emitente.    ***Obrigatório caso o emitente seja pessoa jurídica***. | [opcional] 
**cpf** | **str** | Número do CPF do emitente.    ***Obrigatório caso o emitente seja pessoa física***. | [opcional] 
**x_nome** | **str** | Razão Social ou Nome do emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [opcional] 
**x_fant** | **str** | Nome fantasia.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [opcional] 
**ender_emit** | [**NfeSefazEnderEmi**](NfeSefazEnderEmi.md) |  | [opcional] 
**ie** | **str** | Inscrição Estadual do Emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [opcional] 
**iest** | **str** | Inscricao Estadual do Substituto Tributário.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [opcional] 
**im** | **str** | Inscrição Municipal.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [opcional] 
**cnae** | **str** | CNAE Fiscal.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [opcional] 
**crt** | **int** | Código de Regime Tributário.  Este campo será obrigatoriamente preenchido com:  * 1 - Simples Nacional  * 2 - Simples Nacional - excesso de sublimite de receita bruta  * 3 - Regime Normal  * 4 - Simples Nacional - Microempreendedor individual - MEI    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


