# NeuralSeek.InlineResponse2006

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**extractedEntities** | [**[InlineResponse2006ExtractedEntities]**](InlineResponse2006ExtractedEntities.md) |  | [optional] 
**complete** | **Boolean** | If slots are passed, complete will be set to true when all slots are filled | [optional] [default to false]
**promptEntity** | **String** | A message to display to the user asking them to provide input for the next group of unfilled slots. | [optional] 
**slots** | **Object** | If the slots parameter is filled on the input, NeuralSeek will return it and begin filling the value fields. Continue to send this entire filed back as input thru the multiple turns of the conversation, untill Complete is set to true.  Complete will be set to true when all slots are filled | [optional] 
