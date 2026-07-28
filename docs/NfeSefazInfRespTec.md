# NfeSefazInfRespTec

Informações do Responsável Técnico pela emissão do DF-e.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | CNPJ. | 
**x_contato** | **str** | Informar o nome da pessoa a ser contatada na empresa desenvolvedora do sistema utilizado na emissão do documento fiscal eletrônico. | 
**email** | **str** | Informar o e-mail da pessoa a ser contatada na empresa desenvolvedora do sistema. | 
**fone** | **str** | Informar o telefone da pessoa a ser contatada na empresa desenvolvedora do sistema. Preencher com o Código DDD + número do telefone. | 
**id_csrt** | **int** | Identificador do CSRT utilizado para montar o hash do CSRT. | [optional] 
**csrt** | **str** | Código de Segurança do Responsável Técnico utilizado para montar o hash do CSRT. | [optional] 
**hash_csrt** | **str** | O hashCSRT é o resultado da função hash (SHA-1 - Base64) do CSRT fornecido pelo fisco mais a Chave de Acesso da NFe.    *Se não informado, será calculado automaticamente, desde que os campos &#x60;idCSRT&#x60; e &#x60;CSRT&#x60; sejam fornecidos.* | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


