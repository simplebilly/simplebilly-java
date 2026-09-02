# AttachmentVersionApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createAttachmentVersion**](AttachmentVersionApi.md#createAttachmentVersion) | **POST** /api/v1/attachments/{attachment_id}/versions |  |
| [**listAttachmentVersions**](AttachmentVersionApi.md#listAttachmentVersions) | **GET** /api/v1/attachments/{attachment_id}/versions |  |
| [**restoreAttachmentVersion**](AttachmentVersionApi.md#restoreAttachmentVersion) | **POST** /api/v1/attachments/{attachment_id}/versions/{version_id}/restore |  |


<a id="createAttachmentVersion"></a>
# **createAttachmentVersion**
> AttachmentVersion createAttachmentVersion(attachmentId, newVersionRequest)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AttachmentVersionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    AttachmentVersionApi apiInstance = new AttachmentVersionApi(defaultClient);
    UUID attachmentId = UUID.randomUUID(); // UUID | 
    NewVersionRequest newVersionRequest = new NewVersionRequest(); // NewVersionRequest | 
    try {
      AttachmentVersion result = apiInstance.createAttachmentVersion(attachmentId, newVersionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AttachmentVersionApi#createAttachmentVersion");
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
| **attachmentId** | **UUID**|  | |
| **newVersionRequest** | [**NewVersionRequest**](NewVersionRequest.md)|  | |

### Return type

[**AttachmentVersion**](AttachmentVersion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | New current version recorded |  -  |
| **400** | Bad request |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

<a id="listAttachmentVersions"></a>
# **listAttachmentVersions**
> List&lt;AttachmentVersion&gt; listAttachmentVersions(attachmentId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AttachmentVersionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    AttachmentVersionApi apiInstance = new AttachmentVersionApi(defaultClient);
    UUID attachmentId = UUID.randomUUID(); // UUID | 
    try {
      List<AttachmentVersion> result = apiInstance.listAttachmentVersions(attachmentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AttachmentVersionApi#listAttachmentVersions");
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
| **attachmentId** | **UUID**|  | |

### Return type

[**List&lt;AttachmentVersion&gt;**](AttachmentVersion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

<a id="restoreAttachmentVersion"></a>
# **restoreAttachmentVersion**
> Attachment restoreAttachmentVersion(attachmentId, versionId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AttachmentVersionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    AttachmentVersionApi apiInstance = new AttachmentVersionApi(defaultClient);
    UUID attachmentId = UUID.randomUUID(); // UUID | 
    UUID versionId = UUID.randomUUID(); // UUID | 
    try {
      Attachment result = apiInstance.restoreAttachmentVersion(attachmentId, versionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AttachmentVersionApi#restoreAttachmentVersion");
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
| **attachmentId** | **UUID**|  | |
| **versionId** | **UUID**|  | |

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Attachment restored |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

