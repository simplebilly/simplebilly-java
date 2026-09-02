# TenantSettingsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getTenantSettings**](TenantSettingsApi.md#getTenantSettings) | **GET** /api/v1/settings/tenant |  |
| [**updateTenantSettings**](TenantSettingsApi.md#updateTenantSettings) | **PUT** /api/v1/settings/tenant |  |


<a id="getTenantSettings"></a>
# **getTenantSettings**
> TenantSettings getTenantSettings()



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TenantSettingsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    TenantSettingsApi apiInstance = new TenantSettingsApi(defaultClient);
    try {
      TenantSettings result = apiInstance.getTenantSettings();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TenantSettingsApi#getTenantSettings");
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

[**TenantSettings**](TenantSettings.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tenant settings |  -  |
| **500** | Internal server error |  -  |

<a id="updateTenantSettings"></a>
# **updateTenantSettings**
> TenantSettings updateTenantSettings(updateTenantSettings)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TenantSettingsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    TenantSettingsApi apiInstance = new TenantSettingsApi(defaultClient);
    UpdateTenantSettings updateTenantSettings = new UpdateTenantSettings(); // UpdateTenantSettings | 
    try {
      TenantSettings result = apiInstance.updateTenantSettings(updateTenantSettings);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TenantSettingsApi#updateTenantSettings");
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
| **updateTenantSettings** | [**UpdateTenantSettings**](UpdateTenantSettings.md)|  | |

### Return type

[**TenantSettings**](TenantSettings.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated tenant settings |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

