# DistribuicaoNfePedido


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cpf_cnpj** | **str** | CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*. | 
**ambiente** | **str** | Identificação do Ambiente. | 
**uf_autor** | **str** | Sigla da UF do autor. | [optional] 
**tipo_consulta** | **str** | Tipo de consulta.   Valores possíveis: * &#x60;dist-nsu&#x60; - Consulta pelo último NSU recebido. * &#x60;cons-nsu&#x60; - Consulta por um NSU específico. * &#x60;cons-chave&#x60; - Consulta pela chave de acesso da NF-e. | 
**dist_nsu** | **int** | Distribuição de conjunto de DF-e a partir do NSU informado.    *Obrigatório quando \&quot;tipo_consulta\&quot; for \&quot;dist-nsu\&quot;.* | [optional] 
**cons_nsu** | **int** | Consulta DF-e vinculado ao NSU informado.    *Obrigatório quando \&quot;tipo_consulta\&quot; for \&quot;cons-nsu\&quot;.* | [optional] 
**cons_chave** | **str** | Consulta de NF-e por chave de acesso informada.    *Obrigatório quando \&quot;tipo_consulta\&quot; for \&quot;cons-chave\&quot;.* | [optional] 
**ignorar_tempo_espera** | **bool** | Deve ser utilizado em situações em que o cliente  deseja ignorar o intervalo mínimo de 1 hora entre pedidos de distribuição  de NF-e. Quando habilitado, o cliente reconhece os riscos associados,  incluindo o bloqueio do CNPJ no Ambiente Nacional da SEFAZ, caso seja  caracterizado consumo indevido.    Valores:  * &#x60;false&#x60;: Respeita a regra de intervalo mínimo de 1 hora entre consultas    quando não há mais documentos disponíveis.    * &#x60;true&#x60;: Ignora o tempo de espera e força a requisição. | [optional] [default to False]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


