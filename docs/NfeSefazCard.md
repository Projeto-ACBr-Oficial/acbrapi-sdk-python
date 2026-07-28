# NfeSefazCard

Grupo de Cartões, PIX, Boletos e outros Pagamentos Eletrônicos.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tp_integra** | **int** | Tipo de Integração do processo de pagamento com o sistema de automação da empresa:  * 1 - Pagamento integrado com o sistema de automação da empresa (Ex.: equipamento TEF, Comércio Eletrônico, POS Integrado)  * 2 - Pagamento não integrado com o sistema de automação da empresa (Ex.: equipamento POS Simples) | 
**cnpj** | **str** | CNPJ da instituição de pagamento. | [optional] 
**t_band** | **str** | Bandeira da operadora de cartão. | [optional] 
**c_aut** | **str** | Número de autorização da operação com cartões, PIX, boletos e outros pagamentos eletrônicos. | [optional] 
**cnpj_receb** | **str** | CNPJ do beneficiário do pagamento. | [optional] 
**id_term_pag** | **str** | Identificador do terminal de pagamento. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


