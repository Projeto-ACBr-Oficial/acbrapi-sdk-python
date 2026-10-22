# RTCInfoTributosAbrasf

Grupo de informações dos valores do IBS e da CBS utilizado pelos provedores municipais.    **Atenção**: Para emissões pelo Sistema Nacional NFS-e, esse campo é ignorado.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**c_loc_incid_ibscbs** | **str** | Código do município de incidência do IBS/CBS (tabela do IBGE).    Caso não seja informado, é determinado pelo local da operação (LC 214/25, art. 11), conforme o indicador da operação (&#x60;cIndOp&#x60;). Não confundir com o município de incidência do ISSQN (&#x60;tribMun.cLocIncid&#x60;). | [opcional] 
**v_bc** | **float** | Valor da base de cálculo (BC) do IBS/CBS (R$). | [opcional] 
**fed** | [**RTCInfoTributosAbrasfFed**](RTCInfoTributosAbrasfFed.md) |  | [opcional] 
**uf** | [**RTCInfoTributosAbrasfUF**](RTCInfoTributosAbrasfUF.md) |  | [opcional] 
**mun** | [**RTCInfoTributosAbrasfMun**](RTCInfoTributosAbrasfMun.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


