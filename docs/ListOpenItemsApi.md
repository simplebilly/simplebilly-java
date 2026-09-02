# ListOpenItemsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listOpenItemsApi**](ListOpenItemsApi.md#listOpenItemsApi) | **GET** /api/v1/bookkeeping/open-items |  |


<a id="listOpenItemsApi"></a>
# **listOpenItemsApi**
> List&lt;OpenItem&gt; listOpenItemsApi(reminderLevel1Days, reminderLevel2Days, reminderLevel3Days, customerId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListOpenItemsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    ListOpenItemsApi apiInstance = new ListOpenItemsApi(defaultClient);
    Long reminderLevel1Days = 56L; // Long | 
    Long reminderLevel2Days = 56L; // Long | 
    Long reminderLevel3Days = 56L; // Long | 
    String customerId = "customerId_example"; // String | 
    try {
      List<OpenItem> result = apiInstance.listOpenItemsApi(reminderLevel1Days, reminderLevel2Days, reminderLevel3Days, customerId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListOpenItemsApi#listOpenItemsApi");
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
| **reminderLevel1Days** | **Long**|  | [optional] |
| **reminderLevel2Days** | **Long**|  | [optional] |
| **reminderLevel3Days** | **Long**|  | [optional] |
| **customerId** | **String**|  | [optional] |

### Return type

[**List&lt;OpenItem&gt;**](OpenItem.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of open invoices |  -  |
| **500** | Internal server error |  -  |

