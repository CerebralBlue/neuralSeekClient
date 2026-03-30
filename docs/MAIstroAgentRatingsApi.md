# NeuralSeek.MAIstroAgentRatingsApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**maistroRate**](MAIstroAgentRatingsApi.md#maistroRate) | **POST** /maistroRate | Rate an Agent
[**maistroRatings**](MAIstroAgentRatingsApi.md#maistroRatings) | **POST** /maistroRatings | Get the average user ratings for an agent

<a name="maistroRate"></a>
# **maistroRate**
> maistroRate(body)

Rate an Agent

Allow users to give feedback on an Agent run

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.MAIstroAgentRatingsApi();
let body = new NeuralSeek.MaistroRateBody(); // MaistroRateBody | The request object.

apiInstance.maistroRate(body, (error, data, response) => {
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
 **body** | [**MaistroRateBody**](MaistroRateBody.md)| The request object. | 

### Return type

null (empty response body)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

<a name="maistroRatings"></a>
# **maistroRatings**
> InlineResponse2001 maistroRatings(body)

Get the average user ratings for an agent

Get the average user ratings for an agent

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.MAIstroAgentRatingsApi();
let body = new NeuralSeek.MaistroRatingsBody(); // MaistroRatingsBody | The request object.

apiInstance.maistroRatings(body, (error, data, response) => {
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
 **body** | [**MaistroRatingsBody**](MaistroRatingsBody.md)| The request object. | 

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

