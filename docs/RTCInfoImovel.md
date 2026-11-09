# RTCInfoImovel

Grupo de informações de operações relacionadas a bens imóveis, exceto obras.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**c_mun** | **str** | Código do município do endereço do imóvel (Tabela do IBGE).  *Disponível a partir da NT 009 (leiaute 009.1.01).* | [opcional] 
**g_locacao** | [**RTCLocacaoImovel**](RTCLocacaoImovel.md) |  | [opcional] 
**g_unid_imob** | [**list[RTCUnidadesImobiliarias]**](RTCUnidadesImobiliarias.md) |  | [opcional] 
**insc_imob_fisc** | **str** | &#x60;Deprecated&#x60;    **Propriedade depreciada** a partir da NT 009 (leiaute 009.1.01).    *Utilize &#x60;IBSCBS.imovel.gUnidImob[].inscImobFisc&#x60;*.  Inscrição imobiliária fiscal (código fornecido pela Prefeitura Municipal para a identificação da obra ou para fins de recolhimento do IPTU). | [opcional] 
**c_cib** | **str** | &#x60;Deprecated&#x60;    **Propriedade depreciada** a partir da NT 009 (leiaute 009.1.01).    *Utilize &#x60;IBSCBS.imovel.gUnidImob[].cCIB&#x60;*.  Código do Cadastro Imobiliário Brasileiro - CIB. | [opcional] 
**end** | [**EnderObraEvento**](EnderObraEvento.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


