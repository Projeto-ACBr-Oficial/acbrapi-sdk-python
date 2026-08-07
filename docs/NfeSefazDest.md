# NfeSefazDest

Identificação do Destinatário.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número do CNPJ. | [opcional] 
**cpf** | **str** | Número do CPF. | [opcional] 
**id_estrangeiro** | **str** | Identificador do destinatário, em caso de comprador estrangeiro. | [opcional] 
**x_nome** | **str** | Razão Social ou nome do destinatário. | [opcional] 
**ender_dest** | [**NfeSefazEndereco**](NfeSefazEndereco.md) |  | [opcional] 
**ind_ie_dest** | **int** | Indicador da IE do destinatário:  * 1 - Contribuinte ICMSpagamento à vista  * 2 - Contribuinte isento de inscrição  * 9 - Não Contribuinte | 
**ie** | **str** | Inscrição Estadual (obrigatório nas operações com contribuintes do ICMS). | [opcional] 
**isuf** | **str** | Inscrição na SUFRAMA (Obrigatório nas operações com as áreas com benefícios de incentivos fiscais sob controle da SUFRAMA) PL_005d - 11/08/09 - alterado para aceitar 8 ou 9 dígitos. | [opcional] 
**im** | **str** | Inscrição Municipal do tomador do serviço. | [opcional] 
**email** | **str** | Informar o e-mail do destinatário. O campo pode ser utilizado para informar o e-mail  de recepção da NF-e indicada pelo destinatário. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


