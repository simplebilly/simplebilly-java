# ZugferdApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**generateZugferdApi**](ZugferdApi.md#generateZugferdApi) | **GET** /api/v1/invoices/{id}/zugferd |  |


<a id="generateZugferdApi"></a>
# **generateZugferdApi**
> generateZugferdApi(id, supplierName, supplierStreet, supplierCity, supplierZip, supplierCountry, supplierVatId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ZugferdApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    ZugferdApi apiInstance = new ZugferdApi(defaultClient);
    String id = "id_example"; // String | 
    String supplierName = "supplierName_example"; // String | 
    String supplierStreet = "supplierStreet_example"; // String | 
    String supplierCity = "supplierCity_example"; // String | 
    String supplierZip = "supplierZip_example"; // String | 
    String supplierCountry = "supplierCountry_example"; // String | 
    String supplierVatId = "supplierVatId_example"; // String | 
    try {
      apiInstance.generateZugferdApi(id, supplierName, supplierStreet, supplierCity, supplierZip, supplierCountry, supplierVatId);
    } catch (ApiException e) {
      System.err.println("Exception when calling ZugferdApi#generateZugferdApi");
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
| **id** | **String**|  | |
| **supplierName** | **String**|  | [optional] |
| **supplierStreet** | **String**|  | [optional] |
| **supplierCity** | **String**|  | [optional] |
| **supplierZip** | **String**|  | [optional] |
| **supplierCountry** | **String**|  | [optional] |
| **supplierVatId** | **String**|  | [optional] |

### Return type

null (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | ZUGFeRD/Factur-X hybrid PDF (PDF/A-3 with embedded EN 16931 XML) |  -  |
| **404** | Invoice not found |  -  |
| **500** | Internal server error |  -  |

