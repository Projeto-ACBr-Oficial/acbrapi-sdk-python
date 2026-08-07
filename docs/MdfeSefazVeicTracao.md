# MdfeSefazVeicTracao

Dados do Veículo com a Tração.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**c_int** | **str** | Código interno do veículo. | [opcional] 
**placa** | **str** | Placa do veículo. | 
**renavam** | **str** | RENAVAM do veículo. | [opcional] 
**tara** | **int** | Tara em KG. | 
**cap_kg** | **int** | Capacidade em KG. | [opcional] 
**cap_m3** | **int** | Capacidade em M3. | [opcional] 
**prop** | [**MdfeSefazProp**](MdfeSefazProp.md) |  | [opcional] 
**condutor** | [**list[MdfeSefazCondutor]**](MdfeSefazCondutor.md) |  | 
**tp_rod** | **str** | Tipo de Rodado.  Preencher com:  * 01 - Truck  * 02 - Toco  * 03 - Cavalo Mecânico  * 04 - VAN  * 05 - Utilitário  * 06 - Outros | 
**tp_car** | **str** | Tipo de Carroceria.  Preencher com:  * 00 - não aplicável  * 01 - Aberta  * 02 - Fechada/Baú  * 03 - Granelera  * 04 - Porta Container  * 05 - Sider | 
**uf** | **str** | UF em que veículo está licenciado.  Sigla da UF de licenciamento do veículo. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


