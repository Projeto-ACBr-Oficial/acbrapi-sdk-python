# NfeSefazDest

Identificação do Destinatário.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cnpj** | **str** | Número do CNPJ. | [optional] 
**cpf** | **str** | Número do CPF. | [optional] 
**id_estrangeiro** | **str** | Identificador do destinatário, em caso de comprador estrangeiro. | [optional] 
**x_nome** | **str** | Razão Social ou nome do destinatário. | [optional] 
**ender_dest** | [**NfeSefazEndereco**](NfeSefazEndereco.md) |  | [optional] 
**ind_ie_dest** | **int** | Indicador da IE do destinatário:  * 1 - Contribuinte ICMSpagamento à vista  * 2 - Contribuinte isento de inscrição  * 9 - Não Contribuinte | 
**ie** | **str** | Inscrição Estadual (obrigatório nas operações com contribuintes do ICMS). | [optional] 
**isuf** | **str** | Inscrição na SUFRAMA (Obrigatório nas operações com as áreas com benefícios de incentivos fiscais sob controle da SUFRAMA) PL_005d - 11/08/09 - alterado para aceitar 8 ou 9 dígitos. | [optional] 
**im** | **str** | Inscrição Municipal do tomador do serviço. | [optional] 
**email** | **str** | Informar o e-mail do destinatário. O campo pode ser utilizado para informar o e-mail  de recepção da NF-e indicada pelo destinatário. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


