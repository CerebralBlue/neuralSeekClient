# NeuralSeek.GuardrailsApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**pii**](GuardrailsApi.md#pii) | **POST** /pii | Find PII in a user utterance
[**score**](GuardrailsApi.md#score) | **POST** /score | Run the Semantic Scoring model on text against an array of passages

<a name="pii"></a>
# **pii**
> [InlineResponse20010] pii(body)

Find PII in a user utterance

Find PII in a user utterance

### Example
```javascript
import {NeuralSeek} from 'neural_seek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.GuardrailsApi();
let body = new NeuralSeek.PiiBody(); // PiiBody | The request object.

apiInstance.pii(body, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PiiBody**](PiiBody.md)| The request object. | 

### Return type

[**[InlineResponse20010]**](InlineResponse20010.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="score"></a>
# **score**
> score(body)

Run the Semantic Scoring model on text against an array of passages

Run the Semantic Scoring model on text against an array of passages

### Example
```javascript
import {NeuralSeek} from 'neural_seek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.GuardrailsApi();
let body = new NeuralSeek.ScoreBody(); // ScoreBody | The request object.  Must include the question and a context.

apiInstance.score(body, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ScoreBody**](ScoreBody.md)| The request object.  Must include the question and a context. | 

### Return type

null (empty response body)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

