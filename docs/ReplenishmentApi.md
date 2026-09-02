# ReplenishmentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**applyReplenishments**](ReplenishmentApi.md#applyReplenishments) | **POST** /api/v1/replenishments/apply | Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair. |
| [**getReplenishments**](ReplenishmentApi.md#getReplenishments) | **GET** /api/v1/replenishments |  |


<a id="applyReplenishments"></a>
# **applyReplenishments**
> Object applyReplenishments(targetWarehouseId, sourceWarehouseId)

Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ReplenishmentApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    ReplenishmentApi apiInstance = new ReplenishmentApi(defaultClient);
    String targetWarehouseId = "targetWarehouseId_example"; // String | Warehouse to be replenished. Defaults to the tenant's default warehouse.
    String sourceWarehouseId = "sourceWarehouseId_example"; // String | Restrict source warehouses to this id.
    try {
      Object result = apiInstance.applyReplenishments(targetWarehouseId, sourceWarehouseId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReplenishmentApi#applyReplenishments");
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
| **targetWarehouseId** | **String**| Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional] |
| **sourceWarehouseId** | **String**| Restrict source warehouses to this id. | [optional] |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

<a id="getReplenishments"></a>
# **getReplenishments**
> ReplenishmentResponse getReplenishments(targetWarehouseId, sourceWarehouseId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ReplenishmentApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    ReplenishmentApi apiInstance = new ReplenishmentApi(defaultClient);
    String targetWarehouseId = "targetWarehouseId_example"; // String | Warehouse to be replenished. Defaults to the tenant's default warehouse.
    String sourceWarehouseId = "sourceWarehouseId_example"; // String | Restrict source warehouses to this id.
    try {
      ReplenishmentResponse result = apiInstance.getReplenishments(targetWarehouseId, sourceWarehouseId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReplenishmentApi#getReplenishments");
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
| **targetWarehouseId** | **String**| Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional] |
| **sourceWarehouseId** | **String**| Restrict source warehouses to this id. | [optional] |

### Return type

[**ReplenishmentResponse**](ReplenishmentResponse.md)

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

