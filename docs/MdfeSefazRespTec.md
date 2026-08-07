# MdfeSefazRespTec

Informações do Responsável Técnico pela emissão do DF-e.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | CNPJ da pessoa jurídica responsável técnica pelo sistema utilizado na emissão do documento fiscal eletrônico.  Informar o CNPJ da pessoa jurídica desenvolvedora do sistema utilizado na emissão do documento fiscal eletrônico. | 
**x_contato** | **str** | Nome da pessoa a ser contatada.  Informar o nome da pessoa a ser contatada na empresa desenvolvedora do sistema utilizado na emissão do documento fiscal eletrônico. No caso de pessoa física, informar o respectivo nome. | 
**email** | **str** | Email da pessoa jurídica a ser contatada. | 
**fone** | **str** | Telefone da pessoa jurídica a ser contatada.  Preencher com o Código DDD + número do telefone. | 
**id_csrt** | **int** | Identificador do código de segurança do responsável técnico.  Identificador do CSRT utilizado para geração do hash. | [opcional] 
**csrt** | **str** | Código de Segurança do Responsável Técnico utilizado para montar o hash do CSRT. | [opcional] 
**hash_csrt** | **str** | Hash do token do código de segurança do responsável técnico.  O hashCSRT é o resultado das funções SHA-1 e base64 do token CSRT fornecido pelo fisco + chave de acesso do DF-e. (Implementação em futura NT)  Observação: 28 caracteres são representados no schema como 20 bytes do tipo base64Binary.    *Se não informado, será calculado automaticamente, desde que os campos &#x60;idCSRT&#x60; e &#x60;CSRT&#x60; sejam fornecidos.* | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


