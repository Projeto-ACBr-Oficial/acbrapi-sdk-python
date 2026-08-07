# CteSefazAereo

Informações do modal Aéreo.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**n_minu** | **int** | Número da Minuta.  Documento que precede o CT-e, assinado pelo expedidor, espécie de pedido de serviço. | [opcional] 
**n_oca** | **str** | Número Operacional do Conhecimento Aéreo.  Representa o número de controle comumente utilizado pelo conhecimento aéreo composto por uma sequência numérica de onze dígitos. Os três primeiros dígitos representam um código que os operadores de transporte aéreo associados à IATA possuem. Em seguida um número de série de sete dígitos determinados pelo operador de transporte aéreo. Para finalizar, um dígito verificador, que é um sistema de módulo sete imponderado o qual divide o número de série do conhecimento aéreo por sete e usa o resto como dígito de verificação. | [opcional] 
**d_prev_aereo** | **date** | Data prevista da entrega.  Formato AAAA-MM-DD. | 
**nat_carga** | [**CteSefazNatCarga**](CteSefazNatCarga.md) |  | 
**tarifa** | [**CteSefazTarifa**](CteSefazTarifa.md) |  | 
**peri** | [**list[CteSefazPeri]**](CteSefazPeri.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


