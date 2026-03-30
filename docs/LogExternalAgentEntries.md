# NeuralSeek.LogExternalAgentEntries

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **String** |  | [optional] 
**llmtime** | **Number** | The LLM time in ms | [optional] 
**inputtokencount** | **Number** | Number of input tokens | [optional] 
**generatedtokencount** | **Number** | Number of generated tokens | [optional] 
**llm** | **String** | LLM model identifier | [optional] 
**llmcode** | **String** | LLM specific code | [optional] 
**kbtime** | **Number** | Knowledge base processing time in ms | [optional] 
**kb** | **String** | Knowledge base identifier | [optional] 
**kbScore** | **Number** | Knowledge base relevance score | [optional] 
**kbCoverage** | **Number** | Knowledge base coverage percentage | [optional] 
**elementTime** | **Number** | Time taken for element processing in ms | [optional] 
**element** | **String** | Type of element being timed | [optional] 

<a name="TypeEnum"></a>
## Enum: TypeEnum

* `lLMTime` (value: `"LLMTime"`)
* `lLMCacheTime` (value: `"LLMCacheTime"`)
* `kBTime` (value: `"KBTime"`)
* `elementTime` (value: `"ElementTime"`)


<a name="ElementEnum"></a>
## Enum: ElementEnum

* `model` (value: `"model"`)
* `rest` (value: `"rest"`)
* `database` (value: `"database"`)

