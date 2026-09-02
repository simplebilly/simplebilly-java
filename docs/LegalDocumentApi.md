# LegalDocumentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getLegalDocuments**](LegalDocumentApi.md#getLegalDocuments) | **GET** /api/v1/legal/documents | List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access. |
| [**resetLegalDocuments**](LegalDocumentApi.md#resetLegalDocuments) | **POST** /api/v1/legal/documents/reset | Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list. |
| [**upsertLegalDocuments**](LegalDocumentApi.md#upsertLegalDocuments) | **PUT** /api/v1/legal/documents | Upsert legal documents per (doc_type, lang). Returns the full tenant list. |


<a id="getLegalDocuments"></a>
# **getLegalDocuments**
> List&lt;LegalDocument&gt; getLegalDocuments()

List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.LegalDocumentApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    LegalDocumentApi apiInstance = new LegalDocumentApi(defaultClient);
    try {
      List<LegalDocument> result = apiInstance.getLegalDocuments();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LegalDocumentApi#getLegalDocuments");
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

[**List&lt;LegalDocument&gt;**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | All legal documents of the tenant |  -  |
| **500** | Internal server error |  -  |

<a id="resetLegalDocuments"></a>
# **resetLegalDocuments**
> List&lt;LegalDocument&gt; resetLegalDocuments(legalDocumentReset)

Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.LegalDocumentApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    LegalDocumentApi apiInstance = new LegalDocumentApi(defaultClient);
    LegalDocumentReset legalDocumentReset = new LegalDocumentReset(); // LegalDocumentReset | 
    try {
      List<LegalDocument> result = apiInstance.resetLegalDocuments(legalDocumentReset);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LegalDocumentApi#resetLegalDocuments");
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
| **legalDocumentReset** | [**LegalDocumentReset**](LegalDocumentReset.md)|  | |

### Return type

[**List&lt;LegalDocument&gt;**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reset legal documents |  -  |
| **500** | Internal server error |  -  |

<a id="upsertLegalDocuments"></a>
# **upsertLegalDocuments**
> List&lt;LegalDocument&gt; upsertLegalDocuments(legalDocumentUpsert)

Upsert legal documents per (doc_type, lang). Returns the full tenant list.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.LegalDocumentApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    LegalDocumentApi apiInstance = new LegalDocumentApi(defaultClient);
    List<LegalDocumentUpsert> legalDocumentUpsert = Arrays.asList(); // List<LegalDocumentUpsert> | 
    try {
      List<LegalDocument> result = apiInstance.upsertLegalDocuments(legalDocumentUpsert);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LegalDocumentApi#upsertLegalDocuments");
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
| **legalDocumentUpsert** | [**List&lt;LegalDocumentUpsert&gt;**](LegalDocumentUpsert.md)|  | |

### Return type

[**List&lt;LegalDocument&gt;**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Saved legal documents |  -  |
| **500** | Internal server error |  -  |

