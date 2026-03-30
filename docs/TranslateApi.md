# NeuralSeek.TranslateApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteTranslateGlossary**](TranslateApi.md#deleteTranslateGlossary) | **DELETE** /translateGlossary | Delete the custom translations
[**identifyLanguage**](TranslateApi.md#identifyLanguage) | **POST** /identify | Identify the source language
[**identifyLanguageJSON**](TranslateApi.md#identifyLanguageJSON) | **POST** /identify-single | Identify the source language (JSON)
[**translate**](TranslateApi.md#translate) | **POST** /translate | Translate text into a desired language
[**translateGlossary**](TranslateApi.md#translateGlossary) | **POST** /translateGlossary | Add custom translations

<a name="deleteTranslateGlossary"></a>
# **deleteTranslateGlossary**
> deleteTranslateGlossary()

Delete the custom translations

Delete the custom translations

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.TranslateApi();
apiInstance.deleteTranslateGlossary((error, data, response) => {
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

<a name="identifyLanguage"></a>
# **identifyLanguage**
> [InlineResponse2008] identifyLanguage(body)

Identify the source language

Identify the source language

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.TranslateApi();
let body = "body_example"; // String | The request object.

apiInstance.identifyLanguage(body, (error, data, response) => {
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
 **body** | [**String**](String.md)| The request object. | 

### Return type

[**[InlineResponse2008]**](InlineResponse2008.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: text/plain
 - **Accept**: application/json

<a name="identifyLanguageJSON"></a>
# **identifyLanguageJSON**
> InlineResponse2009 identifyLanguageJSON(body)

Identify the source language (JSON)

Identify the source language (JSON)

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.TranslateApi();
let body = new NeuralSeek.IdentifysingleBody(); // IdentifysingleBody | The request object.

apiInstance.identifyLanguageJSON(body, (error, data, response) => {
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
 **body** | [**IdentifysingleBody**](IdentifysingleBody.md)| The request object. | 

### Return type

[**InlineResponse2009**](InlineResponse2009.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="translate"></a>
# **translate**
> InlineResponse2007 translate(body)

Translate text into a desired language

Translate text into a desired language

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.TranslateApi();
let body = new NeuralSeek.TranslateBody(); // TranslateBody | The request object.

apiInstance.translate(body, (error, data, response) => {
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
 **body** | [**TranslateBody**](TranslateBody.md)| The request object. | 

### Return type

[**InlineResponse2007**](InlineResponse2007.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="translateGlossary"></a>
# **translateGlossary**
> translateGlossary(file, body)

Add custom translations

Add custom translations

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.TranslateApi();
let file = "file_example"; // Blob | 
let body = new NeuralSeek.TranslateGlossaryBody1(); // TranslateGlossaryBody1 | This endpoint will accept either a file upload (TMX or JSON), or a direct JSON payload following IBM's JSON file format https://cloud.ibm.com/docs/language-translator?topic=language-translator-customizing#json.  Only one file may be saved. Subsequent files will overwrite.

apiInstance.translateGlossary(file, body, (error, data, response) => {
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
 **file** | **Blob**|  | 
 **body** | [**TranslateGlossaryBody1**](TranslateGlossaryBody1.md)| This endpoint will accept either a file upload (TMX or JSON), or a direct JSON payload following IBM&#x27;s JSON file format https://cloud.ibm.com/docs/language-translator?topic&#x3D;language-translator-customizing#json.  Only one file may be saved. Subsequent files will overwrite. | 

### Return type

null (empty response body)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data, application/json
 - **Accept**: Not defined

