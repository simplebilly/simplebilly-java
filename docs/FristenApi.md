# FristenApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**fristenApi**](FristenApi.md#fristenApi) | **GET** /api/v1/bookkeeping/fristen |  |


<a id="fristenApi"></a>
# **fristenApi**
> FristenErgebnis fristenApi(bundesland, voranmeldungsrhythmus, dauerfristverlaengerung, estAktiv, gewstAktiv, monate)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.FristenApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    FristenApi apiInstance = new FristenApi(defaultClient);
    String bundesland = "bundesland_example"; // String | 
    String voranmeldungsrhythmus = "voranmeldungsrhythmus_example"; // String | 
    Boolean dauerfristverlaengerung = true; // Boolean | 
    Boolean estAktiv = true; // Boolean | 
    Boolean gewstAktiv = true; // Boolean | 
    Integer monate = 56; // Integer | 
    try {
      FristenErgebnis result = apiInstance.fristenApi(bundesland, voranmeldungsrhythmus, dauerfristverlaengerung, estAktiv, gewstAktiv, monate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FristenApi#fristenApi");
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
| **bundesland** | **String**|  | [optional] |
| **voranmeldungsrhythmus** | **String**|  | [optional] |
| **dauerfristverlaengerung** | **Boolean**|  | [optional] |
| **estAktiv** | **Boolean**|  | [optional] |
| **gewstAktiv** | **Boolean**|  | [optional] |
| **monate** | **Integer**|  | [optional] |

### Return type

[**FristenErgebnis**](FristenErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Steuerliche Fristen |  -  |

