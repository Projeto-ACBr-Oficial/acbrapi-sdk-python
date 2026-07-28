# MdfeSefazAquav

Informações do modal Aquaviário.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**irin** | **str** | Irin do navio sempre deverá ser informado. | 
**tp_emb** | **str** | Código do tipo de embarcação.  Preencher com código da Tabela de Tipo de Embarcação definida no Ministério dos Transportes. | 
**c_embar** | **str** | Código da embarcação. | 
**x_embar** | **str** | Nome da embarcação. | 
**n_viag** | **str** | Número da Viagem. | 
**c_prt_emb** | **str** | Código do Porto de Embarque.  Preencher de acordo com Tabela de Portos definida no Ministério dos Transportes. | 
**c_prt_dest** | **str** | Código do Porto de Destino.  Preencher de acordo com Tabela de Portos definida no Ministério dos Transportes. | 
**prt_trans** | **str** | Porto de Transbordo. | [optional] 
**tp_nav** | **int** | Tipo de Navegação.  Preencher com:  * 0 - Interior  * 1 - Cabotagem | [optional] 
**inf_term_carreg** | [**list[MdfeSefazInfTermCarreg]**](MdfeSefazInfTermCarreg.md) |  | [optional] 
**inf_term_descarreg** | [**list[MdfeSefazInfTermDescarreg]**](MdfeSefazInfTermDescarreg.md) |  | [optional] 
**inf_emb_comb** | [**list[MdfeSefazInfEmbComb]**](MdfeSefazInfEmbComb.md) |  | [optional] 
**inf_unid_carga_vazia** | [**list[MdfeSefazInfUnidCargaVazia]**](MdfeSefazInfUnidCargaVazia.md) |  | [optional] 
**inf_unid_transp_vazia** | [**list[MdfeSefazInfUnidTranspVazia]**](MdfeSefazInfUnidTranspVazia.md) |  | [optional] 
**mmsi** | **str** | Maritime Mobile Service Identify.  Preencher com o MMSI (Maritime Mobile Service Identify) fornecido pela ANATEL ou autoridade de telecomunicações de origem da embarcação. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


