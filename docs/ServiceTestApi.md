# NeuralSeek.ServiceTestApi

All URIs are relative to *https://api.neuralseek.com/v1/{instance}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**servicetest**](ServiceTestApi.md#servicetest) | **GET** /test | Service check

<a name="servicetest"></a>
# **servicetest**
> servicetest()

Service check

Responds 200

### Example
```javascript
import {NeuralSeek} from 'neuralSeek';

let apiInstance = new NeuralSeek.ServiceTestApi();
apiInstance.servicetest((error, data, response) => {
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

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

