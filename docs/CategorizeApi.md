# NeuralSeek.CategorizeApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**categorize**](CategorizeApi.md#categorize) | **POST** /categorize | Categorize text into an Intent &amp; Category

<a name="categorize"></a>
# **categorize**
> InlineResponse2005 categorize(body)

Categorize text into an Intent &amp; Category

Categorize text into an Intent &amp; Category

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.CategorizeApi();
let body = new NeuralSeek.CategorizeBody(); // CategorizeBody | The request object.

apiInstance.categorize(body, (error, data, response) => {
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
 **body** | [**CategorizeBody**](CategorizeBody.md)| The request object. | 

### Return type

[**InlineResponse2005**](InlineResponse2005.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

