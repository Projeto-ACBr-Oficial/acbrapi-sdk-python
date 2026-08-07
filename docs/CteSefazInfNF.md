# CteSefazInfNF

Informações das NF.  Este grupo deve ser informado quando o documento originário for NF.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**n_roma** | **str** | Número do Romaneio da NF. | [opcional] 
**n_ped** | **str** | Número do Pedido da NF. | [opcional] 
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
**n_peso** | **float** | Peso total em Kg. | [opcional] 
**pin** | **str** | PIN SUFRAMA.  PIN atribuído pela SUFRAMA para a operação. | [opcional] 
**d_prev** | **date** | Data prevista de entrega.  Formato AAAA-MM-DD. | [opcional] 
**inf_unid_carga** | [**list[CteSefazUnidCarga]**](CteSefazUnidCarga.md) |  | [opcional] 
**inf_unid_transp** | [**list[CteSefazUnidadeTransp]**](CteSefazUnidadeTransp.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


