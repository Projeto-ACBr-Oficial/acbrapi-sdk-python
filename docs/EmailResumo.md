# EmailResumo


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | ID único gerado pela API para este email.    Utilize-o no endpoint de &lt;a href&#x3D;\&quot;#tag/Email/operation/ConsultarEmail\&quot;&gt;consulta de email&lt;/a&gt;  para obter informações detalhadas sobre o envio do email e  rastrear todos os eventos relacionados, como envio, entrega, falhas e outros  eventos relevantes. | 
**status** | **str** |  | [optional] 
**sent_at** | **datetime** |  | [optional] 
**recipients** | **list[str]** |  | [optional] 
**subject** | **str** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


