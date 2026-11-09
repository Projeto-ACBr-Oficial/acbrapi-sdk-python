# RTCLocacaoImovel

Grupo de informações relativas às operações de locação, cessão onerosa ou arrendamento de bens imóveis.  *Disponível a partir da NT 009 (leiaute 009.1.01).*

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**p_copropriedade** | **float** | Percentual de Copropriedade (Caso só haja um locador, cedente ou arrendador, informar o Percentual de Copropriedade de 100%%). | 
**v_tot_oper** | **float** | Valor total da operação com bem imóvel (Informar o valor total da operação de locação, cessão onerosa ou arrendamento de bens imóveis, associado ao aluguel, renda ou equivalente, conforme art. 255 da LC 214/2025). Não deverá ser inserido neste campo o valor proporcional do coproprietário. | 
**v_desc_incond_tot** | **float** | Valor total do Desconto Incondicionado (Informar o valor total do desconto incondicionado na operação de locação, cessão onerosa ou arrendamento de bens imóveis). | [opcional] 
**v_desc_cond_tot** | **float** | Valor total do Desconto Condicionado (Informar o valor total do desconto incondicionado na operação de locação, cessão onerosa ou arrendamento de bens imóveis). | [opcional] 
**d_venc_orig** | **date** | Data de vencimento original Ano, Mês e Dia (AAAA-MM-DD) (Informar data de vencimento original do aluguel, renda ou equivalente na operação de locação, cessão onerosa ou arrendamento de bens imóveis). | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


