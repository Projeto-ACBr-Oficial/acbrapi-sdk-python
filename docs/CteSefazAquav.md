# CteSefazAquav

Informações do modal Aquaviário.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**v_prest** | **float** | Valor da Prestação Base de Cálculo do AFRMM. | 
**v_afrmm** | **float** | AFRMM (Adicional de Frete para Renovação da Marinha Mercante). | 
**x_navio** | **str** | Identificação do Navio. | 
**balsa** | [**list[CteSefazBalsa]**](CteSefazBalsa.md) |  | [opcional] 
**n_viag** | **str** | Número da Viagem. | [opcional] 
**direc** | **str** | Direção.  Preencher com: N-Norte, L-Leste, S-Sul, O-Oeste. | 
**irin** | **str** | Irin do navio sempre deverá ser informado. | 
**det_cont** | [**list[CteSefazDetCont]**](CteSefazDetCont.md) |  | [opcional] 
**tp_nav** | **int** | Tipo de Navegação.  Preencher com:  * 0 - Interior  * 1 - Cabotagem | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


