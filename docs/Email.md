# Email


## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**id** | **str** | ID único gerado pela API para este email.    Utilize-o no endpoint de &lt;a href&#x3D;\&quot;#tag/Email/operation/ConsultarEmail\&quot;&gt;consulta de email&lt;/a&gt;  para obter informações detalhadas sobre o envio do email e  rastrear todos os eventos relacionados, como envio, entrega, falhas e outros  eventos relevantes. | 
**status** | **str** |  | [opcional] 
**sent_at** | **datetime** |  | [opcional] 
**to** | **list[str]** |  | [opcional] 
**cc** | **list[str]** |  | [opcional] 
**reply_to** | **str** |  | [opcional] 
**subject** | **str** |  | [opcional] 
**attachments** | [**list[EmailAttachment]**](EmailAttachment.md) |  | [opcional] 
**events** | [**list[EmailEvent]**](EmailEvent.md) |  | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


