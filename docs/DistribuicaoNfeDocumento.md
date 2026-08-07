# DistribuicaoNfeDocumento


## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**id** | **str** | ID único gerado pela API para identificar o documento. | 
**created_at** | **datetime** | Data/hora em que o documento foi criado na API. Representado no formato &lt;a href&#x3D;\&quot;https://en.wikipedia.org/wiki/ISO_8601\&quot; target&#x3D;\&quot;blank\&quot;&gt;&#x60;ISO 8601&#x60;&lt;/a&gt;. | [opcional] 
**nsu** | **int** | NSU do documento fiscal. | [opcional] 
**schema** | **str** | Identificação do Schema XML que será utilizado para validar o XML existente no conteúdo da tag docZip. Vai identificar o tipo do documento e sua versão. Exemplos: resNFe_v1.00.xsd, procNFe_v3.10.xsd, resEvento_1.00.xsd, procEventoNFe_v1.00.xsd. | 
**tipo_documento** | **str** | Tipo do documento de interesse da pessoa ou empresa. | [opcional] 
**chave_acesso** | **str** | Chave de Acesso da NF-e. | [opcional] 
**resumo** | **bool** | Indica se o documento distribuído está em sua forma resumida. | [opcional] 
**tipo_evento** | **str** | Tipo do evento. | [opcional] 
**numero_sequencial** | **int** | Número sequencial do evento para o mesmo tipo de evento. | [opcional] 
**data_evento** | **datetime** | Data e hora do evento. | [opcional] 
**data_recebimento** | **datetime** | Data e hora de autorização do evento. | [opcional] 
**numero_protocolo** | **str** | Número do protocolo de autorização. | [opcional] 
**tipo_nfe** | **int** | Tipo da NF-e (0 - entrada; 1 - saída). | [opcional] 
**valor_nfe** | **float** | Valor total da NF-e. | [opcional] 
**digest_value** | **str** | Digest Value da NF-e processada. Utilizado para conferir a integridade da NF-e original. | [opcional] 
**emitente_cpf_cnpj** | **str** | CPF/CNPJ do emitente. | [opcional] 
**emitente_nome_razao_social** | **str** | Nome ou Razão Social do emitente. | [opcional] 
**emitente_inscricao_estadual** | **str** | Inscrição Estadual do emitente. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


