# CustomerCommunicationApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createCommunication**](CustomerCommunicationApi.md#createCommunication) | **POST** /api/v1/communications |  |
| [**customercommunicationRestore**](CustomerCommunicationApi.md#customercommunicationRestore) | **POST** /api/v1/communications/{communication_id}/restore |  |
| [**deleteCommunication**](CustomerCommunicationApi.md#deleteCommunication) | **DELETE** /api/v1/communications/{communication_id} |  |
| [**getCommunication**](CustomerCommunicationApi.md#getCommunication) | **GET** /api/v1/communications/{communication_id} |  |
| [**getContactHistory**](CustomerCommunicationApi.md#getContactHistory) | **GET** /api/v1/contacts/{contact_id}/communications |  |
| [**listCommunications**](CustomerCommunicationApi.md#listCommunications) | **GET** /api/v1/communications/ |  |
| [**updateCommunication**](CustomerCommunicationApi.md#updateCommunication) | **PUT** /api/v1/communications/{communication_id} |  |


<a id="createCommunication"></a>
# **createCommunication**
> CustomerCommunication createCommunication(customerCommunicationCreate)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CustomerCommunicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    CustomerCommunicationApi apiInstance = new CustomerCommunicationApi(defaultClient);
    CustomerCommunicationCreate customerCommunicationCreate = new CustomerCommunicationCreate(); // CustomerCommunicationCreate | 
    try {
      CustomerCommunication result = apiInstance.createCommunication(customerCommunicationCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomerCommunicationApi#createCommunication");
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
| **customerCommunicationCreate** | [**CustomerCommunicationCreate**](CustomerCommunicationCreate.md)|  | |

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

<a id="customercommunicationRestore"></a>
# **customercommunicationRestore**
> CustomerCommunication customercommunicationRestore(communicationId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CustomerCommunicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    CustomerCommunicationApi apiInstance = new CustomerCommunicationApi(defaultClient);
    String communicationId = "communicationId_example"; // String | 
    try {
      CustomerCommunication result = apiInstance.customercommunicationRestore(communicationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomerCommunicationApi#customercommunicationRestore");
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
| **communicationId** | **String**|  | |

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Restored |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

<a id="deleteCommunication"></a>
# **deleteCommunication**
> deleteCommunication(communicationId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CustomerCommunicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    CustomerCommunicationApi apiInstance = new CustomerCommunicationApi(defaultClient);
    String communicationId = "communicationId_example"; // String | 
    try {
      apiInstance.deleteCommunication(communicationId);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomerCommunicationApi#deleteCommunication");
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
| **communicationId** | **String**|  | |

### Return type

null (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | No Content |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

<a id="getCommunication"></a>
# **getCommunication**
> CustomerCommunication getCommunication(communicationId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CustomerCommunicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    CustomerCommunicationApi apiInstance = new CustomerCommunicationApi(defaultClient);
    String communicationId = "communicationId_example"; // String | 
    try {
      CustomerCommunication result = apiInstance.getCommunication(communicationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomerCommunicationApi#getCommunication");
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
| **communicationId** | **String**|  | |

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

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

<a id="getContactHistory"></a>
# **getContactHistory**
> ContactHistoryResponse getContactHistory(contactId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CustomerCommunicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    CustomerCommunicationApi apiInstance = new CustomerCommunicationApi(defaultClient);
    String contactId = "contactId_example"; // String | 
    try {
      ContactHistoryResponse result = apiInstance.getContactHistory(contactId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomerCommunicationApi#getContactHistory");
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
| **contactId** | **String**|  | |

### Return type

[**ContactHistoryResponse**](ContactHistoryResponse.md)

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

<a id="listCommunications"></a>
# **listCommunications**
> List&lt;CustomerCommunication&gt; listCommunications(page, pageSize, contactId, channel, direction, from, to)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CustomerCommunicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    CustomerCommunicationApi apiInstance = new CustomerCommunicationApi(defaultClient);
    Integer page = 56; // Integer | 
    Integer pageSize = 56; // Integer | 
    String contactId = "contactId_example"; // String | Filter history to a single contact.
    CommunicationChannel channel = CommunicationChannel.fromValue("email"); // CommunicationChannel | 
    CommunicationDirection direction = CommunicationDirection.fromValue("inbound"); // CommunicationDirection | 
    LocalDate from = LocalDate.now(); // LocalDate | Only include communications after this ISO date (inclusive).
    LocalDate to = LocalDate.now(); // LocalDate | Only include communications before this ISO date (inclusive).
    try {
      List<CustomerCommunication> result = apiInstance.listCommunications(page, pageSize, contactId, channel, direction, from, to);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomerCommunicationApi#listCommunications");
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
| **page** | **Integer**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **contactId** | **String**| Filter history to a single contact. | [optional] |
| **channel** | [**CommunicationChannel**](.md)|  | [optional] [enum: email, call, meeting, chat, note] |
| **direction** | [**CommunicationDirection**](.md)|  | [optional] [enum: inbound, outbound] |
| **from** | **LocalDate**| Only include communications after this ISO date (inclusive). | [optional] |
| **to** | **LocalDate**| Only include communications before this ISO date (inclusive). | [optional] |

### Return type

[**List&lt;CustomerCommunication&gt;**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **500** | Internal server error |  -  |

<a id="updateCommunication"></a>
# **updateCommunication**
> CustomerCommunication updateCommunication(communicationId, customerCommunicationUpdate)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CustomerCommunicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    CustomerCommunicationApi apiInstance = new CustomerCommunicationApi(defaultClient);
    String communicationId = "communicationId_example"; // String | 
    CustomerCommunicationUpdate customerCommunicationUpdate = new CustomerCommunicationUpdate(); // CustomerCommunicationUpdate | 
    try {
      CustomerCommunication result = apiInstance.updateCommunication(communicationId, customerCommunicationUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomerCommunicationApi#updateCommunication");
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
| **communicationId** | **String**|  | |
| **customerCommunicationUpdate** | [**CustomerCommunicationUpdate**](CustomerCommunicationUpdate.md)|  | |

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad request |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

