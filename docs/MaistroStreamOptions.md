# NeuralSeek.MaistroStreamOptions

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**llm** | **String** | Override the LLM load balancer and force seek to use a specific LLM.  Input the LLM code here.  You must have a valid model card set up on the configure tab for the code you input. | [optional] [default to &#x27;&#x27;]
**userId** | **String** | Set the user_id. Useful and required if you have a corporate document filter set | [optional] [default to &#x27;&#x27;]
**timeout** | **Number** | Timeout in miliseconds. (optional) | [optional] 
**temperatureMod** | **Number** | Shift the model&#x27;s baseline temperature weighting by a percentage | [optional] 
**toppMod** | **Number** | Shift the model&#x27;s baseline probability weighting by a percentage | [optional] 
**freqpenaltyMod** | **Number** | Shift the model&#x27;s baseline frequency penalty weighting by a percentage | [optional] 
**minTokens** | **Number** | Set the minimum tokens you  want the model to produce | [optional] 
**maxTokens** | **Number** | Set the maximum tokens you  want the model to produce | [optional] 
**lastTurn** | [**[SeekStreamOptionsLastTurn]**](SeekStreamOptionsLastTurn.md) | lastTurn is a flexible object. It is backwards compatible with the original single turn object, as well as compatible with the Watson Assistant session history format. | [optional] 
**returnVariables** | **Boolean** | Return the final state of all variables in a dense object | [optional] [default to false]
**returnVariablesExpanded** | **Boolean** | Return the final state of all variables in the same format as the input params | [optional] [default to false]
**returnRender** | **Boolean** | Return the midstate renders | [optional] [default to false]
**returnSource** | **Boolean** | Return the source parts | [optional] [default to false]
**maxRecursion** | **Number** | The maximum number of recursive calls to Explore.  Use caution that you have not created an endless loop as you increase the maximum, as each Explore is charged. | [optional] [default to 10]
