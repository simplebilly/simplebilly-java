# TimeEntriesApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**clockInTimeEntry**](TimeEntriesApi.md#clockInTimeEntry) | **POST** /api/v1/time-entries | Clock in for the authenticated user (resolved via their employee profile). |
| [**clockOutTimeEntry**](TimeEntriesApi.md#clockOutTimeEntry) | **PATCH** /api/v1/time-entries/{id} | Clock out an entry: the entry&#39;s owner, or anyone with &#x60;time_entries:write&#x60;. |
| [**getLaborCosts**](TimeEntriesApi.md#getLaborCosts) | **GET** /api/v1/labor-costs | Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee&#39;s hourly cost rate. |
| [**listTimeEntries**](TimeEntriesApi.md#listTimeEntries) | **GET** /api/v1/time-entries | List time entries with optional date-range / active / employee filters. |


<a id="clockInTimeEntry"></a>
# **clockInTimeEntry**
> TimeEntryDto clockInTimeEntry(timeEntryClockIn)

Clock in for the authenticated user (resolved via their employee profile).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TimeEntriesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    TimeEntriesApi apiInstance = new TimeEntriesApi(defaultClient);
    TimeEntryClockIn timeEntryClockIn = new TimeEntryClockIn(); // TimeEntryClockIn | 
    try {
      TimeEntryDto result = apiInstance.clockInTimeEntry(timeEntryClockIn);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TimeEntriesApi#clockInTimeEntry");
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
| **timeEntryClockIn** | [**TimeEntryClockIn**](TimeEntryClockIn.md)|  | |

### Return type

[**TimeEntryDto**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | No employee profile for this user |  -  |
| **500** | Internal server error |  -  |

<a id="clockOutTimeEntry"></a>
# **clockOutTimeEntry**
> TimeEntryDto clockOutTimeEntry(id, timeEntryClockOut)

Clock out an entry: the entry&#39;s owner, or anyone with &#x60;time_entries:write&#x60;.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TimeEntriesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    TimeEntriesApi apiInstance = new TimeEntriesApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    TimeEntryClockOut timeEntryClockOut = new TimeEntryClockOut(); // TimeEntryClockOut | 
    try {
      TimeEntryDto result = apiInstance.clockOutTimeEntry(id, timeEntryClockOut);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TimeEntriesApi#clockOutTimeEntry");
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
| **id** | **UUID**|  | |
| **timeEntryClockOut** | [**TimeEntryClockOut**](TimeEntryClockOut.md)|  | |

### Return type

[**TimeEntryDto**](TimeEntryDto.md)

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
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

<a id="getLaborCosts"></a>
# **getLaborCosts**
> List&lt;LaborCostRow&gt; getLaborCosts(from, to, groupBy)

Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee&#39;s hourly cost rate.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TimeEntriesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    TimeEntriesApi apiInstance = new TimeEntriesApi(defaultClient);
    LocalDate from = LocalDate.now(); // LocalDate | 
    LocalDate to = LocalDate.now(); // LocalDate | 
    String groupBy = "groupBy_example"; // String | One of \"employee\", \"order\" or \"day\".
    try {
      List<LaborCostRow> result = apiInstance.getLaborCosts(from, to, groupBy);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TimeEntriesApi#getLaborCosts");
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
| **from** | **LocalDate**|  | |
| **to** | **LocalDate**|  | |
| **groupBy** | **String**| One of \&quot;employee\&quot;, \&quot;order\&quot; or \&quot;day\&quot;. | |

### Return type

[**List&lt;LaborCostRow&gt;**](LaborCostRow.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

<a id="listTimeEntries"></a>
# **listTimeEntries**
> List&lt;TimeEntryDto&gt; listTimeEntries(from, to, active, employeeId)

List time entries with optional date-range / active / employee filters.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TimeEntriesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://demo.simplebilly.com");
    
    // Configure HTTP bearer authorization: bearer_token
    HttpBearerAuth bearer_token = (HttpBearerAuth) defaultClient.getAuthentication("bearer_token");
    bearer_token.setBearerToken("BEARER TOKEN");

    TimeEntriesApi apiInstance = new TimeEntriesApi(defaultClient);
    LocalDate from = LocalDate.now(); // LocalDate | 
    LocalDate to = LocalDate.now(); // LocalDate | 
    Boolean active = true; // Boolean | Only currently running shifts (clock_in set, clock_out null).
    UUID employeeId = UUID.randomUUID(); // UUID | 
    try {
      List<TimeEntryDto> result = apiInstance.listTimeEntries(from, to, active, employeeId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TimeEntriesApi#listTimeEntries");
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
| **from** | **LocalDate**|  | [optional] |
| **to** | **LocalDate**|  | [optional] |
| **active** | **Boolean**| Only currently running shifts (clock_in set, clock_out null). | [optional] |
| **employeeId** | **UUID**|  | [optional] |

### Return type

[**List&lt;TimeEntryDto&gt;**](TimeEntryDto.md)

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

