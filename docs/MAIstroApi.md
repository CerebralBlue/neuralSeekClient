# NeuralSeek.MAIstroApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chat**](MAIstroApi.md#chat) | **POST** /chat/completions | Chat Completions - compatible mAIStro endpoint
[**maistro**](MAIstroApi.md#maistro) | **POST** /maistro | Run mAistro NTL or agent
[**maistroAgentGet**](MAIstroApi.md#maistroAgentGet) | **GET** /maistro/{agent} | Run a mAIstro agent via GET
[**maistroBatch**](MAIstroApi.md#maistroBatch) | **POST** /maistro_batch | Call mAIstro NTL or an agent via batch
[**maistroBatchDelete**](MAIstroApi.md#maistroBatchDelete) | **DELETE** /maistro_batch | Cancel current mAIstro batch run
[**maistroBatchGet**](MAIstroApi.md#maistroBatchGet) | **GET** /maistro_batch | Get mAIstro batch results
[**maistroStream**](MAIstroApi.md#maistroStream) | **POST** /maistro_stream | Stream mAIstro NTL or an agent

<a name="chat"></a>
# **chat**
> InlineResponse2004 chat(opts)

Chat Completions - compatible mAIStro endpoint

Call a mAIstro agent using the openAI chat completions schema.

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.MAIstroApi();
let opts = { 
  'body': new NeuralSeek.ChatCompletionsBody(), // ChatCompletionsBody | 
  'runid': "runid_example" // String | Optional header to specify the run ID
};
apiInstance.chat(opts, (error, data, response) => {
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
 **body** | [**ChatCompletionsBody**](ChatCompletionsBody.md)|  | [optional] 
 **runid** | **String**| Optional header to specify the run ID | [optional] 

### Return type

[**InlineResponse2004**](InlineResponse2004.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, text/event-stream

<a name="maistro"></a>
# **maistro**
> InlineResponse2002 maistro(body, opts)

Run mAistro NTL or agent

Freeform prompting using NeuralSeek Template Language or a saved agent

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

let apiInstance = new NeuralSeek.MAIstroApi();
let body = new NeuralSeek.MaistroBody(); // MaistroBody | The request object.
let opts = { 
  'overrideschema': "", // String | Find variables based on post body.  Return all variables as the base presponse body, overriding the normal NS schema. All POST options will be ignored. Set this to a string value of 'true' to activate
  'overrideagent': "", // String | If using overrideSchema you must pass your agent name here. All other POST options will be ignored.
  'debug': "" // String | Include NS debug information in a field named 'neuralseek'. Set this to a string value of 'true' to activate
};
apiInstance.maistro(body, opts, (error, data, response) => {
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
 **body** | [**MaistroBody**](MaistroBody.md)| The request object. | 
 **overrideschema** | **String**| Find variables based on post body.  Return all variables as the base presponse body, overriding the normal NS schema. All POST options will be ignored. Set this to a string value of &#x27;true&#x27; to activate | [optional] 
 **overrideagent** | **String**| If using overrideSchema you must pass your agent name here. All other POST options will be ignored. | [optional] 
 **debug** | **String**| Include NS debug information in a field named &#x27;neuralseek&#x27;. Set this to a string value of &#x27;true&#x27; to activate | [optional] 

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[apiKey](../README.md#apiKey), [embedcode](../README.md#embedcode)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="maistroAgentGet"></a>
# **maistroAgentGet**
> InlineResponse2002 maistroAgentGet(agent, opts)

Run a mAIstro agent via GET

Run a mAIstro agent via GET

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.MAIstroApi();
let agent = "agent_example"; // String | The saved mAIstro agent to run
let opts = { 
  'params': "params_example" // String | Pass your mAIstro params as query parameters in simple name=value format
};
apiInstance.maistroAgentGet(agent, opts, (error, data, response) => {
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
 **agent** | **String**| The saved mAIstro agent to run | 
 **params** | **String**| Pass your mAIstro params as query parameters in simple name&#x3D;value format | [optional] 

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="maistroBatch"></a>
# **maistroBatch**
> maistroBatch(body)

Call mAIstro NTL or an agent via batch

Freeform prompting using NeuralSeek Template Language or a saved agent run in batch mode

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.MAIstroApi();
let body = new NeuralSeek.MaistroBatchBody(); // MaistroBatchBody | The request object.

apiInstance.maistroBatch(body, (error, data, response) => {
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
 **body** | [**MaistroBatchBody**](MaistroBatchBody.md)| The request object. | 

### Return type

null (empty response body)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

<a name="maistroBatchDelete"></a>
# **maistroBatchDelete**
> maistroBatchDelete()

Cancel current mAIstro batch run

Cancel current mAIstro batch run

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.MAIstroApi();
apiInstance.maistroBatchDelete((error, data, response) => {
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

<a name="maistroBatchGet"></a>
# **maistroBatchGet**
> InlineResponse2002 maistroBatchGet()

Get mAIstro batch results

Retrieve results from a mAIstro batch run

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';
let defaultClient = NeuralSeek.ApiClient.instance;

// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new NeuralSeek.MAIstroApi();
apiInstance.maistroBatchGet((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="maistroStream"></a>
# **maistroStream**
> InlineResponse2003 maistroStream(body)

Stream mAIstro NTL or an agent

Freeform prompting using NeuralSeek Template Language or a saved agent

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

let apiInstance = new NeuralSeek.MAIstroApi();
let body = new NeuralSeek.MaistroStreamBody(); // MaistroStreamBody | The request object.

apiInstance.maistroStream(body, (error, data, response) => {
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
 **body** | [**MaistroStreamBody**](MaistroStreamBody.md)| The request object. | 

### Return type

[**InlineResponse2003**](InlineResponse2003.md)

### Authorization

[apiKey](../README.md#apiKey), [embedcode](../README.md#embedcode)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/event-stream

