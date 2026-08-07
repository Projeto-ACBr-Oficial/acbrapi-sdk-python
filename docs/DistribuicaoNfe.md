# DistribuicaoNfe


## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**id** | **str** | ID único gerado pela API para o pedido de distribuição. | 
**created_at** | **datetime** | Data/hora em que o pedido foi criado na API. Representado no formato &lt;a href&#x3D;\&quot;https://en.wikipedia.org/wiki/ISO_8601\&quot; target&#x3D;\&quot;blank\&quot;&gt;&#x60;ISO 8601&#x60;&lt;/a&gt;. | [opcional] 
**status** | **str** | Indica o status da distribuição. | 
**ambiente** | **str** | Identificação do Ambiente. | 
**uf_autor** | **str** | Sigla da UF do autor. | [opcional] 
**tipo_consulta** | **str** |  | 
**dist_nsu** | **int** | Distribuição de conjunto de DF-e a partir do NSU informado.    *Obrigatório quando &#x60;tipo_consulta&#x60; for &#x60;distNSU&#x60;.* | [opcional] 
**cons_nsu** | **int** | Consulta DF-e vinculado ao NSU informado.    *Obrigatório quando &#x60;tipo_consulta&#x60; for &#x60;consNSU&#x60;.* | [opcional] 
**cons_chave** | **str** | Consulta de NF-e por chave de acesso informada.    *Obrigatório quando &#x60;tipo_consulta&#x60; for &#x60;consChNFe&#x60;.* | [opcional] 
**codigo_status** | **int** | Código do status de processamento da requisição. | 
**motivo_status** | **str** | Descrição do status de processamento da requisição. | [opcional] 
**data_hora_resposta** | **datetime** | Data e Hora de processamento da requisição. | 
**ultimo_nsu** | **int** | Último NSU pesquisado no Ambiente Nacional. Se for o caso, o solicitante pode continuar a consulta a partir deste NSU para obter novos resultados. | 
**max_nsu** | **int** | Maior NSU existente no Ambiente Nacional para o CNPJ/CPF informado. | 
**documentos** | [**list[DistribuicaoNfeDocumento]**](DistribuicaoNfeDocumento.md) | Conjunto de informações resumidas e documentos fiscais eletrônicos de interesse da pessoa ou empresa. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


