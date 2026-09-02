# SuitabilityApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**shippingSuitabilityApi**](SuitabilityApi.md#shippingSuitabilityApi) | **POST** /api/v1/shipping/suitability |  |


<a id="shippingSuitabilityApi"></a>
# **shippingSuitabilityApi**
> SuitabilityResult shippingSuitabilityApi(suitabilityRequest)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SuitabilityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    SuitabilityApi apiInstance = new SuitabilityApi(defaultClient);
    SuitabilityRequest suitabilityRequest = new SuitabilityRequest(); // SuitabilityRequest | 
    try {
      SuitabilityResult result = apiInstance.shippingSuitabilityApi(suitabilityRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SuitabilityApi#shippingSuitabilityApi");
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
| **suitabilityRequest** | [**SuitabilityRequest**](SuitabilityRequest.md)|  | |

### Return type

[**SuitabilityResult**](SuitabilityResult.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Shipping suitability results |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

