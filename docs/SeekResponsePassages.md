# NeuralSeek.SeekResponsePassages

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**passage** | **String** | The passage text, summarized to the length set by sourceResultsSummaryLength | [optional] [default to &#x27;&#x27;]
**id** | **String** | The id of the source document in the KB. | [optional] [default to &#x27;&#x27;]
**score** | **Number** | The score of the passage. | [optional] 
**url** | **String** | The URL (if available) of the source document. | [optional] [default to &#x27;&#x27;]
**document** | **String** | The name of the source document. | [optional] [default to &#x27;&#x27;]
**train** | **String** | The training token for the document. Use this when calling the /train endpoint. | [optional] [default to &#x27;&#x27;]
