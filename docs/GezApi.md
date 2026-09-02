# GezApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**gezApi**](GezApi.md#gezApi) | **GET** /api/v1/bookkeeping/gez |  |


<a id="gezApi"></a>
# **gezApi**
> GezReport gezApi(jahr, betriebsstaetten, kfz, hotelzimmer, beschaefigte)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.GezApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    GezApi apiInstance = new GezApi(defaultClient);
    Integer jahr = 56; // Integer | 
    String betriebsstaetten = "betriebsstaetten_example"; // String | Liste der Betriebsstätten als JSON, z.B. `[{\"name\":\"Filiale 1\",\"beschaefigte\":12}]`.
    Long kfz = 56L; // Long | Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind).
    Long hotelzimmer = 56L; // Long | Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen.
    Long beschaefigte = 56L; // Long | Gesamtzahl der Beschäftigten (verwendet nur, wenn `betriebsstaetten` fehlt; dann wird eine einzelne Betriebsstätte angenommen).
    try {
      GezReport result = apiInstance.gezApi(jahr, betriebsstaetten, kfz, hotelzimmer, beschaefigte);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GezApi#gezApi");
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
| **jahr** | **Integer**|  | [optional] |
| **betriebsstaetten** | **String**| Liste der Betriebsstätten als JSON, z.B. &#x60;[{\&quot;name\&quot;:\&quot;Filiale 1\&quot;,\&quot;beschaefigte\&quot;:12}]&#x60;. | [optional] |
| **kfz** | **Long**| Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind). | [optional] |
| **hotelzimmer** | **Long**| Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen. | [optional] |
| **beschaefigte** | **Long**| Gesamtzahl der Beschäftigten (verwendet nur, wenn &#x60;betriebsstaetten&#x60; fehlt; dann wird eine einzelne Betriebsstätte angenommen). | [optional] |

### Return type

[**GezReport**](GezReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rundfunkbeitrag (GEZ) Berechnung nach § 5 RBStV |  -  |

