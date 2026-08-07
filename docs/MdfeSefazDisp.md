# MdfeSefazDisp

Informações dos dispositivos do Vale Pedágio.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj_forn** | **str** | CNPJ da empresa fornecedora do Vale-Pedágio.  * CNPJ da Empresa Fornecedora do Vale-Pedágio, ou seja, empresa que fornece ao Responsável pelo Pagamento do Vale-Pedágio os dispositivos do Vale-Pedágio.  * Informar os zeros não significativos. | 
**cnpjpg** | **str** | CNPJ do responsável pelo pagamento do Vale-Pedágio.  * responsável pelo pagamento do Vale Pedágio. Informar somente quando o responsável não for o emitente do MDF-e.  * Informar os zeros não significativos. | [opcional] 
**cpfpg** | **str** | CNPJ do responsável pelo pagamento do Vale-Pedágio.  Informar os zeros não significativos. | [opcional] 
**n_compra** | **str** | Identificador do vale pedagio obrigatório - IDVPO. | [opcional] 
**v_vale_ped** | **float** | Valor do Vale-Pedagio.  Valor do Vale-Pedágio obrigatório necessário à livre circulação, desde a origem da operação de transporte até o destino, do transportador contratado. | 
**tp_vale_ped** | **str** | Tipo do Vale Pedagio.  * 01 - TAG; 04 - Leitura de placa (pela placa de identificação veicular) | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


