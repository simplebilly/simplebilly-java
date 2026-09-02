# AiApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**aiSuggestApi**](AiApi.md#aiSuggestApi) | **POST** /api/v1/support/ai/suggest |  |
| [**createWorkerApi**](AiApi.md#createWorkerApi) | **POST** /api/v1/support/ai/workers |  |
| [**listWorkersApi**](AiApi.md#listWorkersApi) | **GET** /api/v1/support/ai/workers |  |
| [**runWorkerApi**](AiApi.md#runWorkerApi) | **POST** /api/v1/support/ai/workers/{worker_id}/run |  |


<a id="aiSuggestApi"></a>
# **aiSuggestApi**
> AiSuggestion aiSuggestApi(aiSuggestionRequest)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    AiApi apiInstance = new AiApi(defaultClient);
    AiSuggestionRequest aiSuggestionRequest = new AiSuggestionRequest(); // AiSuggestionRequest | 
    try {
      AiSuggestion result = apiInstance.aiSuggestApi(aiSuggestionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#aiSuggestApi");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **aiSuggestionRequest** | [**AiSuggestionRequest**](AiSuggestionRequest.md)|  | |

### Return type

[**AiSuggestion**](AiSuggestion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | AI suggestion |  -  |
| **500** | AI error |  -  |

<a id="createWorkerApi"></a>
# **createWorkerApi**
> AiWorkerConfig createWorkerApi(aiConfigDto)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    AiApi apiInstance = new AiApi(defaultClient);
    AiConfigDto aiConfigDto = new AiConfigDto(); // AiConfigDto | 
    try {
      AiWorkerConfig result = apiInstance.createWorkerApi(aiConfigDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#createWorkerApi");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **aiConfigDto** | [**AiConfigDto**](AiConfigDto.md)|  | |

### Return type

[**AiWorkerConfig**](AiWorkerConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Worker created |  -  |

<a id="listWorkersApi"></a>
# **listWorkersApi**
> List&lt;AiWorkerConfig&gt; listWorkersApi()



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    AiApi apiInstance = new AiApi(defaultClient);
    try {
      List<AiWorkerConfig> result = apiInstance.listWorkersApi();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#listWorkersApi");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List&lt;AiWorkerConfig&gt;**](AiWorkerConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List AI workers |  -  |

<a id="runWorkerApi"></a>
# **runWorkerApi**
> AiSuggestion runWorkerApi(workerId, aiSuggestionRequest)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    AiApi apiInstance = new AiApi(defaultClient);
    UUID workerId = UUID.randomUUID(); // UUID | 
    AiSuggestionRequest aiSuggestionRequest = new AiSuggestionRequest(); // AiSuggestionRequest | 
    try {
      AiSuggestion result = apiInstance.runWorkerApi(workerId, aiSuggestionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#runWorkerApi");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **workerId** | **UUID**|  | |
| **aiSuggestionRequest** | [**AiSuggestionRequest**](AiSuggestionRequest.md)|  | |

### Return type

[**AiSuggestion**](AiSuggestion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Worker executed |  -  |

