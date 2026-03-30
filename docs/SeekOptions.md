# NeuralSeek.SeekOptions

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**personalize** | [**SeekStreamOptionsPersonalize**](SeekStreamOptionsPersonalize.md) |  | [optional] 
**proposalID** | **String** | Override all settings by passing a NeuralSeek Proposal ID. | [optional] [default to &#x27;&#x27;]
**streaming** | **Boolean** | Return the response via SSE streaming.  This is not compatible with most Virtual Agent platforms, and is intentded for direct website use. | [optional] [default to false]
**seekLLM** | **String** | Override the LLM load balancer and force seek to use a specific LLM.  Input the LLM code here.  You must have a valid model card set up on the configure tab for the code you input. | [optional] [default to &#x27;&#x27;]
**language** | **String** | Valid values are: en, es, de, it, fr, ja, ar | [optional] [default to &#x27;&#x27;]
**filter** | **String** | Text to use as a filter against the filter field set in the KnowledgeBase configuration. Use commas to separate multiple strings for an &#x27;or&#x27; filter. You can use the filter to isolate a certain subset of documents in the knowledgebase. | [optional] [default to &#x27;&#x27;]
**lastTurn** | [**[SeekStreamOptionsLastTurn]**](SeekStreamOptionsLastTurn.md) | lastTurn is a flexible object. It is backwards compatible with the original single turn object, as well as compatible with the Watson Assistant session history format. | [optional] 
**promptEngineering** | **String** | Enable Prompt engineering.  Valid values are the strings &#x27;true&#x27; and &#x27;false&#x27; | [optional] [default to &#x27;&#x27;]
**promptEngineeringPhrase** | **String** | Prepend a phrase to cleansed user input. Must enable Prompt Engineering inside the NeuralSeek \&quot;Configure\&quot; page | [optional] [default to &#x27;&#x27;]
**answerLength** | **Number** | The verbosity of the answer. A whole number 1-4 | [optional] 
**url** | **String** | URL of the current page when using with a web-based Virtual Agent | [optional] [default to &#x27;&#x27;]
**stump** | **String** | Stump Speech text. Fallback for when all else fails. | [optional] [default to &#x27;&#x27;]
**includeSourceResults** | **Boolean** | Include generation source results. Defaults to false. | [optional] [default to false]
**includeHighlights** | **Boolean** | Include highlights from source results. Defaults to false. | [optional] [default to false]
**includeSourceResultsFormatted** | **Boolean** | Include generation source results, and output them into a formatted string.  Defaults to false. | [optional] [default to false]
**sourceResultsNumber** | **Number** | When including source results, how many to include.&#x27; | [optional] [default to 3]
**sourceResultsSummaryLength** | **Number** | When including source results, how long of a summary to include.&#x27; | [optional] [default to 100]
**returnVariables** | **Boolean** | Return the final state of all variables in a dense object | [optional] [default to false]
**returnVariablesExpanded** | **Boolean** | Return the final state of all variables in the same format as the input params | [optional] [default to false]
