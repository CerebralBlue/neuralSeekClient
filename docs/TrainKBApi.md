# NeuralSeek.TrainKBApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**train**](TrainKBApi.md#train) | **POST** /train | Submit KnowledgeBase Training

<a name="train"></a>
# **train**
> train(body)

Submit KnowledgeBase Training

Submit KnowledgeBase Training

### Example
```javascript
import {NeuralSeek} from 'neural_seek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.TrainKBApi();
let body = new NeuralSeek.TrainBody(); // TrainBody | The request object.  Must include the question and a context.

apiInstance.train(body, (error, data, response) => {
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
 **body** | [**TrainBody**](TrainBody.md)| The request object.  Must include the question and a context. | 

### Return type

null (empty response body)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

