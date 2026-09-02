# ShippingApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getCredentialsApi**](ShippingApi.md#getCredentialsApi) | **GET** /api/v1/shipping/credentials |  |
| [**getRatesApi**](ShippingApi.md#getRatesApi) | **POST** /api/v1/shipping/rates |  |
| [**listProvidersApi**](ShippingApi.md#listProvidersApi) | **GET** /api/v1/shipping/providers |  |
| [**saveCredentialsApi**](ShippingApi.md#saveCredentialsApi) | **PUT** /api/v1/shipping/credentials |  |


<a id="getCredentialsApi"></a>
# **getCredentialsApi**
> ShippingCredentials getCredentialsApi()



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ShippingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    ShippingApi apiInstance = new ShippingApi(defaultClient);
    try {
      ShippingCredentials result = apiInstance.getCredentialsApi();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ShippingApi#getCredentialsApi");
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

[**ShippingCredentials**](ShippingCredentials.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Configured shipping provider credentials |  -  |
| **500** | Internal server error |  -  |

<a id="getRatesApi"></a>
# **getRatesApi**
> RateResponse getRatesApi(rateRequest)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ShippingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    ShippingApi apiInstance = new ShippingApi(defaultClient);
    RateRequest rateRequest = new RateRequest(); // RateRequest | 
    try {
      RateResponse result = apiInstance.getRatesApi(rateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ShippingApi#getRatesApi");
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
| **rateRequest** | [**RateRequest**](RateRequest.md)|  | |

### Return type

[**RateResponse**](RateResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Shipping rates from configured providers |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

<a id="listProvidersApi"></a>
# **listProvidersApi**
> List&lt;ProviderInfo&gt; listProvidersApi()



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ShippingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    ShippingApi apiInstance = new ShippingApi(defaultClient);
    try {
      List<ProviderInfo> result = apiInstance.listProvidersApi();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ShippingApi#listProvidersApi");
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

[**List&lt;ProviderInfo&gt;**](ProviderInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of shipping providers |  -  |
| **500** | Internal server error |  -  |

<a id="saveCredentialsApi"></a>
# **saveCredentialsApi**
> ShippingCredentials saveCredentialsApi(shippingCredentials)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ShippingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    ShippingApi apiInstance = new ShippingApi(defaultClient);
    ShippingCredentials shippingCredentials = new ShippingCredentials(); // ShippingCredentials | 
    try {
      ShippingCredentials result = apiInstance.saveCredentialsApi(shippingCredentials);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ShippingApi#saveCredentialsApi");
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
| **shippingCredentials** | [**ShippingCredentials**](ShippingCredentials.md)|  | |

### Return type

[**ShippingCredentials**](ShippingCredentials.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Saved shipping provider credentials |  -  |
| **500** | Internal server error |  -  |

