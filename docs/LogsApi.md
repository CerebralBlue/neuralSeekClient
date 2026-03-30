# NeuralSeek.LogsApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**logExternalAgent**](LogsApi.md#logExternalAgent) | **POST** /logExternalAgent | Log external agent execution details
[**logs**](LogsApi.md#logs) | **POST** /logs | Instance Logs

<a name="logExternalAgent"></a>
# **logExternalAgent**
> InlineResponse20012 logExternalAgent(body)

Log external agent execution details

Records various timing and performance metrics for external agent execution

### Example
```javascript
import {NeuralSeek} from 'neural_seek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.LogsApi();
let body = new NeuralSeek.LogExternalAgentBody(); // LogExternalAgentBody | 

apiInstance.logExternalAgent(body, (error, data, response) => {
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
 **body** | [**LogExternalAgentBody**](LogExternalAgentBody.md)|  | 

### Return type

[**InlineResponse20012**](InlineResponse20012.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="logs"></a>
# **logs**
> [InlineResponse20011] logs(opts)

Instance Logs

Retrieve logs for your instance

### Example
```javascript
import {NeuralSeek} from 'neural_seek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.LogsApi();
let opts = { 
  'body': new NeuralSeek.LogsBody() // LogsBody | The request object.
};
apiInstance.logs(opts, (error, data, response) => {
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
 **body** | [**LogsBody**](LogsBody.md)| The request object. | [optional] 

### Return type

[**[InlineResponse20011]**](InlineResponse20011.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

