# NeuralSeek.TestQuestionsApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTestResults**](TestQuestionsApi.md#getTestResults) | **GET** /getTestResults | Get Test Results
[**test**](TestQuestionsApi.md#test) | **POST** /test | Test questions via batch upload

<a name="getTestResults"></a>
# **getTestResults**
> getTestResults()

Get Test Results

Retrieve an results from the test endpoint

### Example
```javascript
import {NeuralSeek} from 'neural_seek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.TestQuestionsApi();
apiInstance.getTestResults((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a name="test"></a>
# **test**
> test(opts)

Test questions via batch upload

Test questions via batch upload

### Example
```javascript
import {NeuralSeek} from 'neural_seek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.TestQuestionsApi();
let opts = { 
  'file': "file_example", // Blob | 
  'body': new NeuralSeek.TestBody1() // TestBody1 | The questions csv.  Must adhere to the template https://api.neuralseek.com/q.csv After upload you will receive a 202 response and the server will begin processing.  Check for your completed results on the getTestResults endpoint.
};
apiInstance.test(opts, (error, data, response) => {
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
 **file** | **Blob**|  | [optional] 
 **body** | [**TestBody1**](TestBody1.md)| The questions csv.  Must adhere to the template https://api.neuralseek.com/q.csv After upload you will receive a 202 response and the server will begin processing.  Check for your completed results on the getTestResults endpoint. | [optional] 

### Return type

null (empty response body)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data, application/json
 - **Accept**: Not defined

