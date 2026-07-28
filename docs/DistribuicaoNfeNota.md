# DistribuicaoNfeNota


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**chave_acesso** | **str** | Chave de Acesso da NF-e. | [optional] 
**numero_protocolo** | **str** | Número do protocolo de autorização. | [optional] 
**tipo_nfe** | **int** | Tipo da NF-e (0 - entrada; 1 - saída). | [optional] 
**data_emissao** | **datetime** | Data e hora da emissão do documento fiscal. | [optional] 
**valor_nfe** | **float** | Valor total da NF-e. | [optional] 
**digest_value** | **str** | Digest Value da NF-e processada. Utilizado para conferir a integridade da NF-e original. | [optional] 
**emitente_cpf_cnpj** | **str** | CPF/CNPJ do emitente. | [optional] 
**emitente_nome_razao_social** | **str** | Nome ou Razão Social do emitente. | [optional] 
**emitente_inscricao_estadual** | **str** | Inscrição Estadual do emitente. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


