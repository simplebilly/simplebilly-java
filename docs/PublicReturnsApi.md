# PublicReturnsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getPublicReturnStatus**](PublicReturnsApi.md#getPublicReturnStatus) | **GET** /api/v1/public/returns/status | Customer checks the status of a return (public, no auth). The return is only revealed when its linked order&#39;s email matches. |
| [**listPublicReturns**](PublicReturnsApi.md#listPublicReturns) | **GET** /api/v1/public/returns/list | List all returns for an order (public, no auth). |
| [**requestPublicReturn**](PublicReturnsApi.md#requestPublicReturn) | **POST** /api/v1/public/returns/request | Customer requests a return for an order (public, no auth). |


<a id="getPublicReturnStatus"></a>
# **getPublicReturnStatus**
> PublicReturnStatusResponse getPublicReturnStatus(email, returnNumber, returnOrderId, orderNumber)

Customer checks the status of a return (public, no auth). The return is only revealed when its linked order&#39;s email matches.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PublicReturnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    PublicReturnsApi apiInstance = new PublicReturnsApi(defaultClient);
    String email = "email_example"; // String | 
    String returnNumber = "returnNumber_example"; // String | Either return_number or return_order_id must be provided.
    String returnOrderId = "returnOrderId_example"; // String | 
    String orderNumber = "orderNumber_example"; // String | 
    try {
      PublicReturnStatusResponse result = apiInstance.getPublicReturnStatus(email, returnNumber, returnOrderId, orderNumber);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicReturnsApi#getPublicReturnStatus");
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
| **email** | **String**|  | |
| **returnNumber** | **String**| Either return_number or return_order_id must be provided. | [optional] |
| **returnOrderId** | **String**|  | [optional] |
| **orderNumber** | **String**|  | [optional] |

### Return type

[**PublicReturnStatusResponse**](PublicReturnStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return status |  -  |
| **400** | Bad request (missing return identifier) |  -  |
| **404** | Return not found or email mismatch |  -  |
| **500** | Internal server error |  -  |

<a id="listPublicReturns"></a>
# **listPublicReturns**
> List&lt;PublicReturnStatusResponse&gt; listPublicReturns(orderNumber, email)

List all returns for an order (public, no auth).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PublicReturnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    PublicReturnsApi apiInstance = new PublicReturnsApi(defaultClient);
    String orderNumber = "orderNumber_example"; // String | 
    String email = "email_example"; // String | 
    try {
      List<PublicReturnStatusResponse> result = apiInstance.listPublicReturns(orderNumber, email);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicReturnsApi#listPublicReturns");
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
| **orderNumber** | **String**|  | |
| **email** | **String**|  | |

### Return type

[**List&lt;PublicReturnStatusResponse&gt;**](PublicReturnStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Returns for the order |  -  |
| **404** | Order not found or email mismatch |  -  |
| **500** | Internal server error |  -  |

<a id="requestPublicReturn"></a>
# **requestPublicReturn**
> PublicReturnResponse requestPublicReturn(publicReturnRequest)

Customer requests a return for an order (public, no auth).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PublicReturnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    PublicReturnsApi apiInstance = new PublicReturnsApi(defaultClient);
    PublicReturnRequest publicReturnRequest = new PublicReturnRequest(); // PublicReturnRequest | 
    try {
      PublicReturnResponse result = apiInstance.requestPublicReturn(publicReturnRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicReturnsApi#requestPublicReturn");
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
| **publicReturnRequest** | [**PublicReturnRequest**](PublicReturnRequest.md)|  | |

### Return type

[**PublicReturnResponse**](PublicReturnResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Return requested |  -  |
| **400** | Bad request (item not in order / quantity too high) |  -  |
| **404** | Order not found or email mismatch |  -  |
| **500** | Internal server error |  -  |

