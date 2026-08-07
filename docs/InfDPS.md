# InfDPS

Grupo de informações da DPS relativas ao serviço prestado.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**tp_amb** | **int** | Identificação do Ambiente:  * 1 - Produção  * 2 - Homologação | [opcional] 
**dh_emi** | **datetime** | Data e hora da emissão do DPS. Data e hora no formato UTC (Universal Coordinated Time): AAAA-MM-DDThh:mm:ssTZD. | 
**ver_aplic** | **str** | Versão do aplicativo que gerou o DPS. | [opcional] 
**d_compet** | **date** | Data em que se iniciou a prestação do serviço: Dia, mês e ano (AAAAMMDD). (AAAA-MM-DDThh:mm:ssTZD).      *Geramos automaticamente quando nenhum valor é informado.* | [opcional] 
**c_motivo_emis_ti** | **int** | Motivo da Emissão da DPS pelo Tomador/Intermediário:  * 1 - Importação de Serviço  * 2 - Tomador/Intermediário obrigado a emitir NFS-e por legislação municipal  * 3 - Tomador/Intermediário emitindo NFS-e por recusa de emissão pelo prestador  * 4 - Tomador/Intermediário emitindo por rejeitar a NFS-e emitida pelo prestador | [opcional] 
**ch_nfse_rej** | **str** | Chave de Acesso da NFS-e rejeitada pelo Tomador/Intermediário. | [opcional] 
**subst** | [**Substituicao**](Substituicao.md) |  | [opcional] 
**prest** | [**InfoPrestador**](InfoPrestador.md) |  | 
**toma** | [**InfoTomador**](InfoTomador.md) |  | [opcional] 
**interm** | [**InfoIntermediario**](InfoIntermediario.md) |  | [opcional] 
**serv** | [**Serv**](Serv.md) |  | 
**valores** | [**InfoValores**](InfoValores.md) |  | 
**ibscbs** | [**RTCInfoIBSCBS**](RTCInfoIBSCBS.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


