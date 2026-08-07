# MdfeSefazInfNFePeri

Preenchido quando for  transporte de produtos classificados pela ONU como perigosos.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**n_onu** | **str** | Número ONU/UN.  Ver a legislação de transporte de produtos perigosos aplicadas ao modal. | 
**x_nome_ae** | **str** | Nome apropriado para embarque do produto.  Ver a legislação de transporte de produtos perigosos aplicada ao modo de transporte. | [opcional] 
**x_cla_risco** | **str** | Classe ou subclasse/divisão, e risco subsidiário/risco secundário.  Ver a legislação de transporte de produtos perigosos aplicadas ao modal. | [opcional] 
**gr_emb** | **str** | Grupo de Embalagem.  Ver a legislação de transporte de produtos perigosos aplicadas ao modal  Preenchimento obrigatório para o modal aéreo.  A legislação para o modal rodoviário e ferroviário não atribui grupo de embalagem para todos os produtos, portanto haverá casos de não preenchimento desse campo. | [opcional] 
**q_tot_prod** | **str** | Quantidade total por produto.  Preencher conforme a legislação de transporte de produtos perigosos aplicada ao modal. | 
**q_vol_tipo** | **str** | Quantidade e Tipo de volumes.  Preencher conforme a legislação de transporte de produtos perigosos aplicada ao modal. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


