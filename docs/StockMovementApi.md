# StockMovementApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getStockMovement**](StockMovementApi.md#getStockMovement) | **GET** /api/v1/stock-movements/{movement_id} |  |
| [**listStockMovements**](StockMovementApi.md#listStockMovements) | **GET** /api/v1/stock-movements/ |  |


<a id="getStockMovement"></a>
# **getStockMovement**
> StockMovement getStockMovement(movementId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.StockMovementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    StockMovementApi apiInstance = new StockMovementApi(defaultClient);
    String movementId = "movementId_example"; // String | 
    try {
      StockMovement result = apiInstance.getStockMovement(movementId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StockMovementApi#getStockMovement");
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
| **movementId** | **String**|  | |

### Return type

[**StockMovement**](StockMovement.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

<a id="listStockMovements"></a>
# **listStockMovements**
> List&lt;StockMovement&gt; listStockMovements(page, pageSize, productId, warehouseId, movementType, from, to)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.StockMovementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    StockMovementApi apiInstance = new StockMovementApi(defaultClient);
    Integer page = 56; // Integer | 
    Integer pageSize = 56; // Integer | 
    UUID productId = UUID.randomUUID(); // UUID | 
    String warehouseId = "warehouseId_example"; // String | 
    String movementType = "movementType_example"; // String | 
    LocalDate from = LocalDate.now(); // LocalDate | Only movements on or after this date (inclusive).
    LocalDate to = LocalDate.now(); // LocalDate | Only movements on or before this date (inclusive).
    try {
      List<StockMovement> result = apiInstance.listStockMovements(page, pageSize, productId, warehouseId, movementType, from, to);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StockMovementApi#listStockMovements");
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
| **page** | **Integer**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **productId** | **UUID**|  | [optional] |
| **warehouseId** | **String**|  | [optional] |
| **movementType** | **String**|  | [optional] |
| **from** | **LocalDate**| Only movements on or after this date (inclusive). | [optional] |
| **to** | **LocalDate**| Only movements on or before this date (inclusive). | [optional] |

### Return type

[**List&lt;StockMovement&gt;**](StockMovement.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **500** | Internal server error |  -  |

