# NfeSefazDI

Declaração de Importação (NT 2011/004).

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**n_di** | **str** | Número do Documento de Importação (DI, DSI, DIRE, DUImp) (NT2011/004). | 
**d_di** | **date** | Data de registro da DI/DSI/DA (AAAA-MM-DD). | 
**x_loc_desemb** | **str** | Local do desembaraço aduaneiro. | 
**uf_desemb** | **str** | UF onde ocorreu o desembaraço aduaneiro. | 
**d_desemb** | **date** | Data do desembaraço aduaneiro (AAAA-MM-DD). | 
**tp_via_transp** | **int** | Via de transporte internacional informada na DI ou na Declaração Única de Importação (DUImp):  * 1 - Maritima  * 2 - Fluvial  * 3 - Lacustre  * 4 - Aerea  * 5 - Postal  * 6 - Ferroviaria  * 7 - Rodoviaria  * 8 - Conduto  * 9 - Meios Proprios  * 10 - Entrada/Saida Ficta  * 11 - Courier  * 12 - Em maos  * 13 - Por reboque | 
**v_afrmm** | **float** | Valor Adicional ao frete para renovação de marinha mercante. | [optional] 
**tp_intermedio** | **int** | Forma de Importação quanto a intermediação  * 1 - por conta propria  * 2 - por conta e ordem  * 3 - encomenda | 
**cnpj** | **str** | CNPJ do adquirente ou do encomendante. | [optional] 
**cpf** | **str** | CPF do adquirente ou do encomendante. | [optional] 
**uf_terceiro** | **str** | Sigla da UF do adquirente ou do encomendante. | [optional] 
**c_exportador** | **str** | Código do exportador (usado nos sistemas internos de informação do emitente da NF-e). | 
**adi** | [**list[NfeSefazAdi]**](NfeSefazAdi.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


