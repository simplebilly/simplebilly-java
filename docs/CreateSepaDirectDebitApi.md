# CreateSepaDirectDebitApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createSepaDirectDebitApi**](CreateSepaDirectDebitApi.md#createSepaDirectDebitApi) | **POST** /api/v1/bookkeeping/sepa-direct-debit |  |


<a id="createSepaDirectDebitApi"></a>
# **createSepaDirectDebitApi**
> SepaDirectDebitResponse createSepaDirectDebitApi(creditorName, creditorIban, creditorId, mandateId, mandateDate, debtorName, debtorIban, amount, collectionDate, creditorBic, debtorBic, description)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CreateSepaDirectDebitApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    CreateSepaDirectDebitApi apiInstance = new CreateSepaDirectDebitApi(defaultClient);
    String creditorName = "creditorName_example"; // String | 
    String creditorIban = "creditorIban_example"; // String | 
    String creditorId = "creditorId_example"; // String | 
    String mandateId = "mandateId_example"; // String | 
    String mandateDate = "mandateDate_example"; // String | 
    String debtorName = "debtorName_example"; // String | 
    String debtorIban = "debtorIban_example"; // String | 
    String amount = "amount_example"; // String | 
    String collectionDate = "collectionDate_example"; // String | 
    String creditorBic = "creditorBic_example"; // String | 
    String debtorBic = "debtorBic_example"; // String | 
    String description = "description_example"; // String | 
    try {
      SepaDirectDebitResponse result = apiInstance.createSepaDirectDebitApi(creditorName, creditorIban, creditorId, mandateId, mandateDate, debtorName, debtorIban, amount, collectionDate, creditorBic, debtorBic, description);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CreateSepaDirectDebitApi#createSepaDirectDebitApi");
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
| **creditorName** | **String**|  | |
| **creditorIban** | **String**|  | |
| **creditorId** | **String**|  | |
| **mandateId** | **String**|  | |
| **mandateDate** | **String**|  | |
| **debtorName** | **String**|  | |
| **debtorIban** | **String**|  | |
| **amount** | **String**|  | |
| **collectionDate** | **String**|  | |
| **creditorBic** | **String**|  | [optional] |
| **debtorBic** | **String**|  | [optional] |
| **description** | **String**|  | [optional] |

### Return type

[**SepaDirectDebitResponse**](SepaDirectDebitResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | SEPA Direct Debit XML |  -  |
| **500** | Internal server error |  -  |

