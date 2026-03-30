# NeuralSeek.ExtractEntitiesApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**extractEntities**](ExtractEntitiesApi.md#extractEntities) | **POST** /extract | Extract entitites from text

<a name="extractEntities"></a>
# **extractEntities**
> InlineResponse2006 extractEntities(body)

Extract entitites from text

Extract entitites from text

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.ExtractEntitiesApi();
let body = new NeuralSeek.ExtractBody(); // ExtractBody | The request object.

apiInstance.extractEntities(body, (error, data, response) => {
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
 **body** | [**ExtractBody**](ExtractBody.md)| The request object. | 

### Return type

[**InlineResponse2006**](InlineResponse2006.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

