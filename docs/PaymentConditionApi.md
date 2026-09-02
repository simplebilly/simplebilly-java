# PaymentConditionApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listPaymentConditionsApi**](PaymentConditionApi.md#listPaymentConditionsApi) | **GET** /api/v1/payment-conditions |  |


<a id="listPaymentConditionsApi"></a>
# **listPaymentConditionsApi**
> List&lt;PaymentCondition&gt; listPaymentConditionsApi()



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PaymentConditionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    PaymentConditionApi apiInstance = new PaymentConditionApi(defaultClient);
    try {
      List<PaymentCondition> result = apiInstance.listPaymentConditionsApi();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentConditionApi#listPaymentConditionsApi");
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

[**List&lt;PaymentCondition&gt;**](PaymentCondition.md)

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

