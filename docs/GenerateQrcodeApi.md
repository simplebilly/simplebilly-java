# GenerateQrcodeApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**generateQrcodeApi**](GenerateQrcodeApi.md#generateQrcodeApi) | **GET** /api/v1/invoices/{id}/qrcode |  |


<a id="generateQrcodeApi"></a>
# **generateQrcodeApi**
> QRCodeResponse generateQrcodeApi(iban, id, holderName, bic, amount, reference, purpose)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.GenerateQrcodeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    GenerateQrcodeApi apiInstance = new GenerateQrcodeApi(defaultClient);
    String iban = "iban_example"; // String | 
    String id = "id_example"; // String | 
    String holderName = "holderName_example"; // String | 
    String bic = "bic_example"; // String | 
    String amount = "amount_example"; // String | 
    String reference = "reference_example"; // String | 
    String purpose = "purpose_example"; // String | 
    try {
      QRCodeResponse result = apiInstance.generateQrcodeApi(iban, id, holderName, bic, amount, reference, purpose);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GenerateQrcodeApi#generateQrcodeApi");
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
| **iban** | **String**|  | |
| **id** | **String**|  | |
| **holderName** | **String**|  | [optional] |
| **bic** | **String**|  | [optional] |
| **amount** | **String**|  | [optional] |
| **reference** | **String**|  | [optional] |
| **purpose** | **String**|  | [optional] |

### Return type

[**QRCodeResponse**](QRCodeResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | QR Code for invoice payment |  -  |
| **404** | Invoice not found |  -  |
| **500** | Internal server error |  -  |

