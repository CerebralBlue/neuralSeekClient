# NeuralSeek.TranslateBody

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **[String]** | An array of input text to be translated | [optional] 
**modelId** | **String** | Convienence input for legacy connections. Define a traget language by setting a source to target relationship using 2-digit language codes, for example en-es to translate into spanish.  The source language is ignored. Either this or the target parameter is required. | [optional] [default to &#x27;&#x27;]
**target** | **String** | The 2-digit language code for the target language.  Either this or the model_id parameter is required. | [optional] [default to &#x27;&#x27;]
**llmId** | **String** | Optional - Pass an llm card id to override the LLM used for translation | [optional] [default to &#x27;&#x27;]
**maxChunk** | **Number** | Optional - Pass a maximum translation chunk token size. This can help speed up translations in the 200-2000 word range when using slower LLM&#x27;s.  Use a setting between 200 and 500 in these scenarios. Setting 0 or omitting this parameter unsets it. | [optional] [default to 0]
**additionalInstructions** | **String** | Optional - Additional prompting to be passed to the LLM. Do not casusally use this field, you will break things. | [optional] [default to &#x27;&#x27;]
