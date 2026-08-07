# DocDedRed

Grupo de informações de documento utilizado para Dedução/Redução do valor do serviço.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**ch_nfse** | **str** | Chave de Acesso da NFS-e (Padrão Nacional). | [opcional] 
**ch_nfe** | **str** | Chave de Acesso da NF-e. | [opcional] 
**nfse_mun** | [**DocOutNFSe**](DocOutNFSe.md) |  | [opcional] 
**nfnfs** | [**DocNFNFS**](DocNFNFS.md) |  | [opcional] 
**n_doc_fisc** | **str** | Número de documento fiscal. | [opcional] 
**n_doc** | **str** | Número de documento não fiscal. | [opcional] 
**tp_ded_red** | **int** | Identificação da Dedução/Redução:  * 1 - Alimentação e bebidas/frigobar  * 2 - Materiais  * 3 - Produção Externa  * 4 - Reembolso de despesas  * 5 - Repasse consorciado  * 6 - Repasse plano de saúde  * 7 - Serviços  * 8 - Subempreitada de mão de obra  * 9 - Profissional parceiro  * 99 - Outras deduções | 
**x_desc_out_ded** | **str** | Descrição da Dedução/Redução quando a opção é \&quot;99 - Outras Deduções\&quot;. | [opcional] 
**dt_emi_doc** | **date** | Data da emissão do documento dedutível. Ano, mês e dia (AAAA-MM-DD). | 
**v_dedutivel_redutivel** | **float** | Valor monetário total dedutível/redutível no documento informado (R$).  Este é o valor total no documento informado que é passível de dedução/redução. | 
**v_deducao_reducao** | **float** | Valor monetário utilizado para dedução/redução do valor do serviço da NFS-e que está sendo emitida (R$).  Deve ser menor ou igual ao valor deduzível/redutível (vDedutivelRedutivel). | 
**fornec** | [**InfoFornecDocDedRed**](InfoFornecDocDedRed.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


