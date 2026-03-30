# NeuralSeek.SeekAnswerRatingsApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**answerRatings**](SeekAnswerRatingsApi.md#answerRatings) | **POST** /answerRatings | Get the average user ratings for an answer
[**rate**](SeekAnswerRatingsApi.md#rate) | **POST** /rate | Rate an answer

<a name="answerRatings"></a>
# **answerRatings**
> InlineResponse2001 answerRatings(body)

Get the average user ratings for an answer

Get the average user ratings for an answer

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.SeekAnswerRatingsApi();
let body = new NeuralSeek.AnswerRatingsBody(); // AnswerRatingsBody | The request object.

apiInstance.answerRatings(body, (error, data, response) => {
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
 **body** | [**AnswerRatingsBody**](AnswerRatingsBody.md)| The request object. | 

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="rate"></a>
# **rate**
> rate(body)

Rate an answer

Allow users to give feedback in on answers generated

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.SeekAnswerRatingsApi();
let body = new NeuralSeek.RateBody(); // RateBody | The request object.

apiInstance.rate(body, (error, data, response) => {
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
 **body** | [**RateBody**](RateBody.md)| The request object. | 

### Return type

null (empty response body)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

