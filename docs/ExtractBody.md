# NeuralSeek.ExtractBody

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **String** | The text to extract entitites from | [optional] 
**language** | **String** | The 2-char language code to be used when generating a promptEntity response. Only set this if you want to override the configured language in NeuralSeek. | [optional] 
**entities** | **String** | An array of objects, stringified. The properties of the object are name, description, and format | [optional] 
**slots** | **Object** | Provide an object of variable names, with a type property set to an entity type to match to in total across multiple turns of a conversation. NeuralSeek will return a promptEntity to display to the user to continue to fil the slots.  As slots are filled the value field will be populated.  Continue to send this entire filed back as input thru the multiple turns of the conversation, untill Complete is set to true.  Complete will be set to true when all slots are filled | [optional] 
**confirmSlots** | **Boolean** | When using Slots, once all slots have been filled display a summary and ask for a confirmation before setting the &#x27;complete&#x27; flag | [optional] 
**confirmEverySlot** | **Boolean** | When using Slots, on every turn recite the slot that was just previously filled. | [optional] 
