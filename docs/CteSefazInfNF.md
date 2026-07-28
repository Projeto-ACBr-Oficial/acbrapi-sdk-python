# CteSefazInfNF

Informações das NF.  Este grupo deve ser informado quando o documento originário for NF.

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**n_roma** | **str** | Número do Romaneio da NF. | [optional] 
**n_ped** | **str** | Número do Pedido da NF. | [optional] 
**mod** | **str** | Modelo da Nota Fiscal.  Preencher com:  * 01 - NF Modelo 01/1A e Avulsa  * 04 - NF de Produtor | 
**serie** | **str** | Série. | 
**n_doc** | **str** | Número. | 
**d_emi** | **date** | Data de Emissão.  Formato AAAA-MM-DD. | 
**v_bc** | **float** | Valor da Base de Cálculo do ICMS. | 
**v_icms** | **float** | Valor Total do ICMS. | 
**v_bcst** | **float** | Valor da Base de Cálculo do ICMS ST. | 
**v_st** | **float** | Valor Total do ICMS ST. | 
**v_prod** | **float** | Valor Total dos Produtos. | 
**v_nf** | **float** | Valor Total da NF. | 
**n_cfop** | **str** | CFOP Predominante.  CFOP da NF ou, na existência de mais de um, predominância pelo critério de valor econômico. | 
**n_peso** | **float** | Peso total em Kg. | [optional] 
**pin** | **str** | PIN SUFRAMA.  PIN atribuído pela SUFRAMA para a operação. | [optional] 
**d_prev** | **date** | Data prevista de entrega.  Formato AAAA-MM-DD. | [optional] 
**inf_unid_carga** | [**list[CteSefazUnidCarga]**](CteSefazUnidCarga.md) |  | [optional] 
**inf_unid_transp** | [**list[CteSefazUnidadeTransp]**](CteSefazUnidadeTransp.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


