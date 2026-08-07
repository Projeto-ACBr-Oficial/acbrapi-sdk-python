# RTCInfoDest

Grupo de informações relativas ao Destinatário.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número da inscrição no Cadastro Nacional de Pessoa Jurídica (CNPJ) do Destinatário do serviço. | [opcional] 
**cpf** | **str** | Número da inscrição no Cadastro de Pessoa Física (CPF) do Destinatário do serviço. | [opcional] 
**nif** | **str** | Número de Identificação Fiscal fornecido por órgão de administração tributária no exterior. | [opcional] 
**c_nao_nif** | **int** | Motivo para não informação do NIF:  * 0 - Não informado na nota de origem  * 1 - Dispensado do NIF  * 2 - Não exigência do NIF | [opcional] 
**x_nome** | **str** | Nome / Nome Empresarial do do Destinatário do serviço. | 
**end** | [**Endereco**](Endereco.md) |  | [opcional] 
**fone** | **str** | Número do telefone do Destinatário do serviço  (Preencher com o Código DDD + número do telefone. Nas operações com exterior é permitido informar o  código do país + código da localidade + número do telefone). | [opcional] 
**email** | **str** | * E-mail do Destinatário do serviço | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


