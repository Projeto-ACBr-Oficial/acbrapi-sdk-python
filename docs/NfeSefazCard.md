# NfeSefazCard

Grupo de Cartões, PIX, Boletos e outros Pagamentos Eletrônicos.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**tp_integra** | **int** | Tipo de Integração do processo de pagamento com o sistema de automação da empresa:  * 1 - Pagamento integrado com o sistema de automação da empresa (Ex.: equipamento TEF, Comércio Eletrônico, POS Integrado)  * 2 - Pagamento não integrado com o sistema de automação da empresa (Ex.: equipamento POS Simples) | 
**cnpj** | **str** | CNPJ da instituição de pagamento. | [opcional] 
**t_band** | **str** | Bandeira da operadora de cartão. | [opcional] 
**c_aut** | **str** | Número de autorização da operação com cartões, PIX, boletos e outros pagamentos eletrônicos. | [opcional] 
**cnpj_receb** | **str** | CNPJ do beneficiário do pagamento. | [opcional] 
**id_term_pag** | **str** | Identificador do terminal de pagamento. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


