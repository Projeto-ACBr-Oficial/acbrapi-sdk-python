# NfeSefazISSQN

ISSQN.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**v_bc** | **float** | Valor da BC do ISSQN. | 
**v_aliq** | **float** | Alíquota do ISSQN. | 
**v_issqn** | **float** | Valor da do ISSQN. | 
**c_mun_fg** | **str** | Informar o município de ocorrência do fato gerador do ISSQN. Utilizar a Tabela do IBGE (Anexo VII - Tabela de UF, Município e País). “Atenção, não vincular com os campos B12, C10 ou E10” v2.0. | 
**c_list_serv** | **str** | Informar o Item da lista de serviços da LC 116/03 em que se classifica o serviço. | 
**v_deducao** | **float** | Valor dedução para redução da base de cálculo. | [opcional] 
**v_outro** | **float** | Valor outras retenções. | [opcional] 
**v_desc_incond** | **float** | Valor desconto incondicionado. | [opcional] 
**v_desc_cond** | **float** | Valor desconto condicionado. | [opcional] 
**v_iss_ret** | **float** | Valor Retenção ISS. | [opcional] 
**ind_iss** | **int** | Exibilidade do ISS:1-Exigível  * 2 - Não incidente  * 3 - Isenção  * 4 - Exportação  * 5 - Imunidade  * 6 - Exig.Susp. Judicial  * 7 - Exig.Susp. ADM | 
**c_servico** | **str** | Código do serviço prestado dentro do município. | [opcional] 
**c_mun** | **str** | Código do Município de Incidência do Imposto. | [opcional] 
**c_pais** | **str** | Código de Pais. | [opcional] 
**n_processo** | **str** | Número do Processo administrativo ou judicial de suspenção do processo. | [opcional] 
**ind_incentivo** | **int** | Indicador de Incentivo Fiscal. 1&#x3D;Sim  * 2 - Não | 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


