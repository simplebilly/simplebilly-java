# ProposeAssignmentsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**proposeAssignmentsApi**](ProposeAssignmentsApi.md#proposeAssignmentsApi) | **GET** /api/v1/bookkeeping/propose-assignments |  |


<a id="proposeAssignmentsApi"></a>
# **proposeAssignmentsApi**
> List&lt;ProposedAssignment&gt; proposeAssignmentsApi(minConfidence, customerId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProposeAssignmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    ProposeAssignmentsApi apiInstance = new ProposeAssignmentsApi(defaultClient);
    Double minConfidence = 3.4D; // Double | 
    String customerId = "customerId_example"; // String | 
    try {
      List<ProposedAssignment> result = apiInstance.proposeAssignmentsApi(minConfidence, customerId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProposeAssignmentsApi#proposeAssignmentsApi");
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
| **minConfidence** | **Double**|  | [optional] |
| **customerId** | **String**|  | [optional] |

### Return type

[**List&lt;ProposedAssignment&gt;**](ProposedAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Proposed payment to invoice assignments |  -  |
| **500** | Internal server error |  -  |

