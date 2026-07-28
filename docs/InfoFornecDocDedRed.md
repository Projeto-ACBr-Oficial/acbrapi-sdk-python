# InfoFornecDocDedRed

Grupo de informações do Fornecedor em Deduções de Serviços.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número do CNPJ. | [optional] 
**cpf** | **str** | Número do CPF. | [optional] 
**nif** | **str** | Número de Identificação Fiscal fornecido por órgão de administração tributária no exterior. | [optional] 
**c_nao_nif** | **int** | Motivo para não informação do NIF:  * 0 - Não informado na nota de origem  * 1 - Dispensado do NIF  * 2 - Não exigência do NIF | [optional] 
**caepf** | **str** | Número do Cadastro de Atividade Econômica da Pessoa Física (CAEPF). | [optional] 
**im** | **str** | Número da inscrição municipal. | [optional] 
**ie** | **str** | Número da inscrição estadual.    **Atenção**: Para emissões pelo Sistema Nacional NFS-e, esse campo é ignorado. | [optional] 
**x_nome** | **str** | Nome/Nome Empresarial. | 
**end** | [**Endereco**](Endereco.md) |  | [optional] 
**fone** | **str** | Número do telefone do prestador:  Preencher com o Código DDD + número do telefone.  Nas operações com exterior é permitido informar o código do país + código da localidade + número do telefone). | [optional] 
**email** | **str** | * E-mail | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


