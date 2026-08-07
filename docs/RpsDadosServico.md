# RpsDadosServico


## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**iss_retido** | **bool** | Reter ISSQN. | [opcional] [default False]
**responsavel_retencao** | **int** | Responsável pela retenção:  * 0 - Prestador;  * 1 - Tomador;  * 2 - Intermediário. | [opcional] 
**item_lista_servico** | **str** | Código do item da lista de serviço, geralmente segue a LC116, podendo variar de acordo com a prefeitura.    Você pode encontrar esse dado no portal da prefeitura, em uma nota emitida ou junto ao contador. | 
**codigo_cnae** | **str** | Código CNAE (Classificação Nacional de Atividades Econômicas). | [opcional] 
**codigo_tributacao_municipio** | **str** | Código de tributação do município. | [opcional] 
**discriminacao** | **str** | Detalhamento do serviço prestado. | 
**codigo_municipio** | **str** | Código IBGE do município de prestação do serviço.  Caso não informado, será considerado o município do prestador. | [opcional] 
**codigo_pais** | **str** | Código do país de prestação do serviço. | [opcional] 
**tipo_tributacao** | **int** | Tipo de Tributação do Serviço:  * 1 - Isento de ISS  * 2 - Imune  * 3 - Não Incidência no Município  * 4 - Não Tributável  * 5 - Retido  * 6 - Tributável Dentro do Município  * 7 - Tributável Fora do Município  * 8 - Tributável Dentro do Município pelo tomador | [opcional] 
**exigibilidade_iss** | **int** | Exigibilidade do ISS:  * 1 - Exigível  * 2 - Não Incidência  * 3 - Isenção  * 4 - Exportação  * 5 - Imunidade  * 6 - Suspenso por Decisão Judicial  * 7 - Suspenso por Processo Administrativo | [opcional] 
**codigo_municipio_incidencia** | **str** | Código IBGE do município de incidência do ISSQN. | [opcional] 
**numero_processo** | **str** | Número do Processo de Suspensão da Exigibilidade. | [opcional] 
**unidade** | **str** | Unidade do serviço prestado. | [opcional] 
**quantidade** | **float** | Quantidade dos serviços prestados. | [opcional] 
**valores** | [**RpsServicoValores**](RpsServicoValores.md) |  | 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


