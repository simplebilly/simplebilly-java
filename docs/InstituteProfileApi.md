# InstituteProfileApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getInstituteProfile**](InstituteProfileApi.md#getInstituteProfile) | **GET** /api/v1/institute-profile | Current institute profile (created with defaults when missing). |
| [**updateInstituteProfile**](InstituteProfileApi.md#updateInstituteProfile) | **PUT** /api/v1/institute-profile | Update the institute profile (institute_type and/or kapitalmarktorientiert). |


<a id="getInstituteProfile"></a>
# **getInstituteProfile**
> InstituteProfile getInstituteProfile()

Current institute profile (created with defaults when missing).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.InstituteProfileApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    InstituteProfileApi apiInstance = new InstituteProfileApi(defaultClient);
    try {
      InstituteProfile result = apiInstance.getInstituteProfile();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstituteProfileApi#getInstituteProfile");
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

[**InstituteProfile**](InstituteProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Institute profile |  -  |
| **500** | Internal server error |  -  |

<a id="updateInstituteProfile"></a>
# **updateInstituteProfile**
> InstituteProfile updateInstituteProfile(instituteProfileUpdate)

Update the institute profile (institute_type and/or kapitalmarktorientiert).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.InstituteProfileApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    InstituteProfileApi apiInstance = new InstituteProfileApi(defaultClient);
    InstituteProfileUpdate instituteProfileUpdate = new InstituteProfileUpdate(); // InstituteProfileUpdate | 
    try {
      InstituteProfile result = apiInstance.updateInstituteProfile(instituteProfileUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstituteProfileApi#updateInstituteProfile");
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
| **instituteProfileUpdate** | [**InstituteProfileUpdate**](InstituteProfileUpdate.md)|  | |

### Return type

[**InstituteProfile**](InstituteProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated institute profile |  -  |
| **400** | Invalid institute_type |  -  |
| **500** | Internal server error |  -  |

