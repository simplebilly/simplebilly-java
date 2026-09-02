# ReorderProposalApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**applyReorderProposal**](ReorderProposalApi.md#applyReorderProposal) | **POST** /api/v1/reorder-proposals/apply | Convert a reorder proposal into a draft purchase order. |
| [**getReorderProposal**](ReorderProposalApi.md#getReorderProposal) | **GET** /api/v1/reorder-proposals |  |


<a id="applyReorderProposal"></a>
# **applyReorderProposal**
> Object applyReorderProposal(configuredOnly, warehouseId)

Convert a reorder proposal into a draft purchase order.

Returns the created purchase order id. Suggested line items are generated with the current reorder quantity per product.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ReorderProposalApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    ReorderProposalApi apiInstance = new ReorderProposalApi(defaultClient);
    Boolean configuredOnly = true; // Boolean | Only include products with a reorder point configured (`min_stock`).
    String warehouseId = "warehouseId_example"; // String | Limit to a single warehouse id.
    try {
      Object result = apiInstance.applyReorderProposal(configuredOnly, warehouseId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReorderProposalApi#applyReorderProposal");
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
| **configuredOnly** | **Boolean**| Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional] |
| **warehouseId** | **String**| Limit to a single warehouse id. | [optional] |

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

<a id="getReorderProposal"></a>
# **getReorderProposal**
> ReorderProposalResponse getReorderProposal(configuredOnly, warehouseId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ReorderProposalApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    ReorderProposalApi apiInstance = new ReorderProposalApi(defaultClient);
    Boolean configuredOnly = true; // Boolean | Only include products with a reorder point configured (`min_stock`).
    String warehouseId = "warehouseId_example"; // String | Limit to a single warehouse id.
    try {
      ReorderProposalResponse result = apiInstance.getReorderProposal(configuredOnly, warehouseId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReorderProposalApi#getReorderProposal");
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
| **configuredOnly** | **Boolean**| Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional] |
| **warehouseId** | **String**| Limit to a single warehouse id. | [optional] |

### Return type

[**ReorderProposalResponse**](ReorderProposalResponse.md)

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

