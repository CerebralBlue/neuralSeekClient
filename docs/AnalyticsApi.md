# NeuralSeek.AnalyticsApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**analytics**](AnalyticsApi.md#analytics) | **POST** /analytics | Instance Analytics

<a name="analytics"></a>
# **analytics**
> analytics(opts)

Instance Analytics

Retrieve an analytics dataset for your instance

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.AnalyticsApi();
let opts = { 
  'body': new NeuralSeek.AnalyticsBody() // AnalyticsBody | The request object.  You may optionally limit the result set using \"count\"
};
apiInstance.analytics(opts, (error, data, response) => {
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
 **body** | [**AnalyticsBody**](AnalyticsBody.md)| The request object.  You may optionally limit the result set using \&quot;count\&quot; | [optional] 

### Return type

null (empty response body)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

