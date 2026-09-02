# GewerbesteuerApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**gewerbesteuerApi**](GewerbesteuerApi.md#gewerbesteuerApi) | **GET** /api/v1/bookkeeping/gewerbesteuer |  |


<a id="gewerbesteuerApi"></a>
# **gewerbesteuerApi**
> GewerbesteuerErgebnis gewerbesteuerApi(year, hebesatz, gewerbeertrag, country, gemeindeschluessel)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.GewerbesteuerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    GewerbesteuerApi apiInstance = new GewerbesteuerApi(defaultClient);
    Integer year = 56; // Integer | 
    String hebesatz = "hebesatz_example"; // String | 
    String gewerbeertrag = "gewerbeertrag_example"; // String | 
    String country = "country_example"; // String | 
    String gemeindeschluessel = "gemeindeschluessel_example"; // String | 
    try {
      GewerbesteuerErgebnis result = apiInstance.gewerbesteuerApi(year, hebesatz, gewerbeertrag, country, gemeindeschluessel);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GewerbesteuerApi#gewerbesteuerApi");
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
| **year** | **Integer**|  | |
| **hebesatz** | **String**|  | [optional] |
| **gewerbeertrag** | **String**|  | [optional] |
| **country** | **String**|  | [optional] |
| **gemeindeschluessel** | **String**|  | [optional] |

### Return type

[**GewerbesteuerErgebnis**](GewerbesteuerErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Gewerbesteuer / Trade Tax Ergebnis |  -  |

