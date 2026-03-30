# NeuralSeek.SeekResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**answer** | **String** | The generated answer | [default to &#x27;&#x27;]
**ufa** | **String** | The raw answer from the LLM before guardrails are applied. | [optional] [default to &#x27;&#x27;]
**answerId** | **String** | The id of the answer. Use this to refer to it from other endpoints, such as the Rating endpoint | [optional] [default to &#x27;&#x27;]
**thumbs** | **String** | The URL of a rating HTML page with an SVG to embed with the answer to allow easy rating. | [optional] [default to &#x27;&#x27;]
**thumbsSVG** | **String** | The URL of a rating SVG to display with the answer to allow easy rating. | [optional] [default to &#x27;&#x27;]
**intent** | **String** | The intent of the answer. | [optional] [default to &#x27;&#x27;]
**category** | **Number** | The category id of the answer. | [optional] 
**categoryName** | **String** | The category name of the answer. | [optional] [default to &#x27;&#x27;]
**score** | **Number** | The final confidence score of the answer (0-100) | 
**kBscore** | **Number** | The KnowledgeBase confidence of the answer&#x27;s source documentation  (0-100) | [optional] 
**semanticAnalysis** | **String** | Semantic Analysis | [optional] [default to &#x27;&#x27;]
**cachedResult** | **String** | If the result came from cache, will be set to the string &#x27;true&#x27; | [optional] [default to &#x27;&#x27;]
**langCode** | **String** | The language code of the answer. If you set the input language code to &#x27;xx&#x27; to identify the language, this is useful to condition of the found language and response. | [optional] [default to &#x27;&#x27;]
**url** | **String** | The top scoring URL (if available) used to train the answer. Set the field you want returned here in on the Configure tab. The field must contain a URL, or it will be ignored. | [optional] [default to &#x27;&#x27;]
**document** | **String** | The top document (if available) used to train the answer. Set the field you want returned here in on the Configure tab | [optional] [default to &#x27;&#x27;]
**time** | **Number** | Total processing time in milliseconds | [optional] 
**kbTime** | **Number** | KnowledgeBase response time in milliseconds | [optional] 
**protectTime** | **Number** | PI time in milliseconds | [optional] 
**categorySelectionTime** | **Number** | Category Selection time in milliseconds | [optional] 
**promptInjection** | **Number** | Prompt injection value | [optional] 
**sourceResultsFormatted** | **String** | A listing of the passages used for answer summarization. This will only return if includeSourceResultsFormatted is set to true on the request | [optional] [default to &#x27;&#x27;]
**passages** | [**[SeekResponsePassages]**](SeekResponsePassages.md) | A listing of the passages used for answer summarization. This will only return if includeSourceResults is set to true on the request | [optional] 
**kbCoverage** | **Number** | KnowledgeBase coverage score. How much content was returned from the KnowledgeBase on the subject asked as compared to benchmarks. Low coverage is not necessarily indicitive of bad content. | [optional] 
**sentiment** | **Number** | Sentiment score | [optional] 
**semanticScore** | **Number** | Semantic score (if enabled) | [optional] 
**variables** | **Object** | The returned variable. | [optional] 
**variablesExpanded** | [**[SeekResponseVariablesExpanded]**](SeekResponseVariablesExpanded.md) | The returned variable, in the format of the input params | [optional] 
