# CServ

Grupo de informações relativas ao código do serviço prestado.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**c_trib_nac** | **str** | Código de tributação nacional do ISSQN.  **Ambiente Nacional**: O código deve conter exatamente 6 dígitos numéricos, sendo 2 para Item (LC 116/2003), 2 para Subitem (LC 116/2003) e 2 para Desdobro Nacional. Exemplo: &#x60;010701&#x60;.  **Envio direto para a Prefeitura**: Em muitos municípios, continua sendo exigido apenas o código conforme a LC 116/2003, totalizando 4 dígitos numéricos (2 para Item e 2 para Subitem). Exemplo: &#x60;0107&#x60;. | 
**c_trib_mun** | **str** | Código de tributação municipal do ISSQN. | [opcional] 
**cnae** | **str** | Código CNAE (Classificação Nacional de Atividades Econômicas). | [opcional] 
**x_desc_serv** | **str** | Descrição completa do serviço prestado.    Os caracteres acentuados poderão ser alterados para caracteres sem acentuação. | 
**c_nbs** | **str** | Código NBS correspondente ao serviço prestado, seguindo a versão 2.0, conforme Anexo B. | [opcional] 
**c_nat_op** | **str** | Código de natureza da operação.    **Atenção**: Para emissões pelo Sistema Nacional NFS-e, esse campo é ignorado. | [opcional] 
**c_sit_trib** | **str** | Código de situação tributária.    **Atenção**: Para emissões pelo Sistema Nacional NFS-e, esse campo é ignorado. | [opcional] 
**c_int_contrib** | **str** | Código interno do contribuinte. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


