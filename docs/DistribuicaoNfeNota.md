# DistribuicaoNfeNota


## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**chave_acesso** | **str** | Chave de Acesso da NF-e. | [opcional] 
**numero_protocolo** | **str** | Número do protocolo de autorização. | [opcional] 
**tipo_nfe** | **int** | Tipo da NF-e (0 - entrada; 1 - saída). | [opcional] 
**data_emissao** | **datetime** | Data e hora da emissão do documento fiscal. | [opcional] 
**valor_nfe** | **float** | Valor total da NF-e. | [opcional] 
**digest_value** | **str** | Digest Value da NF-e processada. Utilizado para conferir a integridade da NF-e original. | [opcional] 
**emitente_cpf_cnpj** | **str** | CPF/CNPJ do emitente. | [opcional] 
**emitente_nome_razao_social** | **str** | Nome ou Razão Social do emitente. | [opcional] 
**emitente_inscricao_estadual** | **str** | Inscrição Estadual do emitente. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


