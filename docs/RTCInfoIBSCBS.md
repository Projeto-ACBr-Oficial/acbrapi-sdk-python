# RTCInfoIBSCBS

Grupo de informações declaradas pelo emitente referentes ao IBS e à CBS.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**fin_nfse** | **int** | Indicador da finalidade da emissão de NFS-e:  * 0 - NFS-e regular. | 
**ind_final** | **int** | Indica operação de uso ou consumo pessoal (art. 57):  * 0 - Não;  * 1 - Sim. | 
**c_ind_op** | **str** | Código indicador da operação de fornecimento, conforme tabela \&quot;código indicador de operação\&quot;. | 
**tp_oper** | **int** | Tipo de Operação com Entes Governamentais ou outros serviços sobre bens imóveis:  * 1 - Fornecimento com pagamento posterior;  * 2 - Recebimento do pagamento com fornecimento já realizado;  * 3 - Fornecimento com pagamento já realizado;  * 4 - Recebimento do pagamento com fornecimento posterior;  * 5 - Fornecimento e recebimento do pagamento concomitantes. | [opcional] 
**g_ref_nfse** | [**InfoRefNFSe**](InfoRefNFSe.md) |  | [opcional] 
**tp_ente_gov** | **int** | Tipo de ente governamental  Para administração pública direta e suas autarquias e fundações:  * 1 - União;  * 2 - Estado;  * 3 - Distrito Federal;  * 4 - Município. | [opcional] 
**ind_dest** | **int** | A respeito do Destinatário dos serviços:  * 0 - O destinatário - o próprio tomador/adquirente identificado na NFS-e (tomador &#x3D; adquirente &#x3D; destinatário);  * 1 - O destinatário não - o próprio adquirente, podendo ser outra pessoa, física ou jurídica (ou equiparada), ou um estabelecimento diferente do indicado como tomador (tomador &#x3D; adquirente !&#x3D; destinatário). | 
**dest** | [**RTCInfoDest**](RTCInfoDest.md) |  | [opcional] 
**imovel** | [**RTCInfoImovel**](RTCInfoImovel.md) |  | [opcional] 
**valores** | [**RTCInfoValoresIBSCBS**](RTCInfoValoresIBSCBS.md) |  | 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


