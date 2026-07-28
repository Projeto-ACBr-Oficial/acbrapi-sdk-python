# InfDPS

Grupo de informações da DPS relativas ao serviço prestado.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tp_amb** | **int** | Identificação do Ambiente:  * 1 - Produção  * 2 - Homologação | [optional] 
**dh_emi** | **datetime** | Data e hora da emissão do DPS. Data e hora no formato UTC (Universal Coordinated Time): AAAA-MM-DDThh:mm:ssTZD. | 
**ver_aplic** | **str** | Versão do aplicativo que gerou o DPS. | [optional] 
**d_compet** | **date** | Data em que se iniciou a prestação do serviço: Dia, mês e ano (AAAAMMDD). (AAAA-MM-DDThh:mm:ssTZD).      *Geramos automaticamente quando nenhum valor é informado.* | [optional] 
**c_motivo_emis_ti** | **int** | Motivo da Emissão da DPS pelo Tomador/Intermediário:  * 1 - Importação de Serviço  * 2 - Tomador/Intermediário obrigado a emitir NFS-e por legislação municipal  * 3 - Tomador/Intermediário emitindo NFS-e por recusa de emissão pelo prestador  * 4 - Tomador/Intermediário emitindo por rejeitar a NFS-e emitida pelo prestador | [optional] 
**ch_nfse_rej** | **str** | Chave de Acesso da NFS-e rejeitada pelo Tomador/Intermediário. | [optional] 
**subst** | [**Substituicao**](Substituicao.md) |  | [optional] 
**prest** | [**InfoPrestador**](InfoPrestador.md) |  | 
**toma** | [**InfoTomador**](InfoTomador.md) |  | [optional] 
**interm** | [**InfoIntermediario**](InfoIntermediario.md) |  | [optional] 
**serv** | [**Serv**](Serv.md) |  | 
**valores** | [**InfoValores**](InfoValores.md) |  | 
**ibscbs** | [**RTCInfoIBSCBS**](RTCInfoIBSCBS.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


