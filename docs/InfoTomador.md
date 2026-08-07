# InfoTomador

Grupo de informações do DPS relativas ao Tomador de Serviços.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**orgao_publico** | **bool** | Indica se o tomador do serviço - um órgão público.    **Atenção**: Para emissões pelo Sistema Nacional NFS-e, esse campo é ignorado. | [opcional] [default False]
**cnpj** | **str** | Número do CNPJ. | [opcional] 
**cpf** | **str** | Número do CPF. | [opcional] 
**nif** | **str** | Número de Identificação Fiscal fornecido por órgão de administração tributária no exterior. | [opcional] 
**c_nao_nif** | **int** | Motivo para não informação do NIF:  * 0 - Não informado na nota de origem  * 1 - Dispensado do NIF  * 2 - Não exigência do NIF | [opcional] 
**caepf** | **str** | Número do Cadastro de Atividade Econômica da Pessoa Física (CAEPF). | [opcional] 
**im** | **str** | Número da inscrição municipal. | [opcional] 
**ie** | **str** | Número da inscrição estadual.    **Atenção**: Para emissões pelo Sistema Nacional NFS-e, esse campo é ignorado. | [opcional] 
**x_nome** | **str** | Nome/Nome Empresarial. | 
**end** | [**Endereco**](Endereco.md) |  | [opcional] 
**fone** | **str** | Número do telefone do prestador:  Preencher com o Código DDD + número do telefone.  Nas operações com exterior é permitido informar o código do país + código da localidade + número do telefone). | [opcional] 
**email** | **str** | * E-mail | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


