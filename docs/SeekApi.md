# NeuralSeek.SeekApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**seek**](SeekApi.md#seek) | **POST** /seek | Seek an answer from NeuralSeek
[**seekStream**](SeekApi.md#seekStream) | **POST** /seek_stream | Stream a Seek an answer from NeuralSeek

<a name="seek"></a>
# **seek**
> SeekResponse seek(body)

Seek an answer from NeuralSeek

This endpoint takes an input object with a user question, context and options and returns a response object

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

// Configure API key authorization: embedcode
let embedcode = defaultClient.authentications['embedcode'];
embedcode.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//embedcode.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.SeekApi();
let body = new NeuralSeek.Seek(); // Seek | The request object.  Must include the question and a context.

apiInstance.seek(body, (error, data, response) => {
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
 **body** | [**Seek**](Seek.md)| The request object.  Must include the question and a context. | 

### Return type

[**SeekResponse**](SeekResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [embedcode](../README.md#embedcode)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="seekStream"></a>
# **seekStream**
> InlineResponse200 seekStream(body)

Stream a Seek an answer from NeuralSeek

This endpoint takes an input object with a user question, context and options and returns a response object

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

// Configure API key authorization: embedcode
let embedcode = defaultClient.authentications['embedcode'];
embedcode.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//embedcode.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.SeekApi();
let body = new NeuralSeek.SeekStreamBody(); // SeekStreamBody | The request object.  Must include the question and a context.

apiInstance.seekStream(body, (error, data, response) => {
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
 **body** | [**SeekStreamBody**](SeekStreamBody.md)| The request object.  Must include the question and a context. | 

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[apiKey](../README.md#apiKey), [embedcode](../README.md#embedcode)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/event-stream

