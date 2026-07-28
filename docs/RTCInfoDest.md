# RTCInfoDest

Grupo de informações relativas ao Destinatário.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número da inscrição no Cadastro Nacional de Pessoa Jurídica (CNPJ) do Destinatário do serviço. | [optional] 
**cpf** | **str** | Número da inscrição no Cadastro de Pessoa Física (CPF) do Destinatário do serviço. | [optional] 
**nif** | **str** | Número de Identificação Fiscal fornecido por órgão de administração tributária no exterior. | [optional] 
**c_nao_nif** | **int** | Motivo para não informação do NIF:  * 0 - Não informado na nota de origem  * 1 - Dispensado do NIF  * 2 - Não exigência do NIF | [optional] 
**x_nome** | **str** | Nome / Nome Empresarial do do Destinatário do serviço. | 
**end** | [**Endereco**](Endereco.md) |  | [optional] 
**fone** | **str** | Número do telefone do Destinatário do serviço  (Preencher com o Código DDD + número do telefone. Nas operações com exterior é permitido informar o  código do país + código da localidade + número do telefone). | [optional] 
**email** | **str** | * E-mail do Destinatário do serviço | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


