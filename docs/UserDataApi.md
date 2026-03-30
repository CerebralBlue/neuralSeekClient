# NeuralSeek.UserDataApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteUserData**](UserDataApi.md#deleteUserData) | **DELETE** /user_data | Delete all user data

<a name="deleteUserData"></a>
# **deleteUserData**
> deleteUserData(opts)

Delete all user data

This endpoint deletes all user data

### Example
```javascript
import {NeuralSeek} from 'neural_seek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.UserDataApi();
let opts = { 
  'intent': ["intent_example"] // [String] | The intents to delete. If left blank all intents will be deleted.
};
apiInstance.deleteUserData(opts, (error, data, response) => {
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
 **intent** | [**[String]**](String.md)| The intents to delete. If left blank all intents will be deleted. | [optional] 

### Return type

null (empty response body)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

