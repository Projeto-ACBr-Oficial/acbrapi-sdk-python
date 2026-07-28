# MdfeSefazInfResp

Informações do responsável pelo seguro da carga.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resp_seg** | **int** | Responsável pelo seguro.  Preencher com:  * 1 - Emitente do MDF-e  * 22 - Responsável pela contratação do serviço de transporte (contratante)  Dados obrigatórios apenas no modal Rodoviário, depois da lei 11.442/07. Para os demais modais esta informação é opcional. | 
**cnpj** | **str** | Número do CNPJ do responsável pelo seguro.  Obrigatório apenas se responsável pelo seguro for (2) responsável pela contratação do transporte - pessoa jurídica. | [optional] 
**cpf** | **str** | Número do CPF do responsável pelo seguro.  Obrigatório apenas se responsável pelo seguro for (2) responsável pela contratação do transporte - pessoa física. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


