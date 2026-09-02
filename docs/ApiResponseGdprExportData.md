

# ApiResponseGdprExportData


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**activityLog** | [**List&lt;GdprActivity&gt;**](GdprActivity.md) |  |  |
|**apiKeys** | [**List&lt;GdprApiKey&gt;**](GdprApiKey.md) | Key identifiers and names only — never a usable credential. |  |
|**billing** | [**List&lt;GdprBillingInfo&gt;**](GdprBillingInfo.md) |  |  |
|**exportedAt** | **OffsetDateTime** |  |  |
|**generatedByAi** | **Boolean** | Honesty field: this document is a plain data dump, never AI-generated. |  |
|**notifications** | [**List&lt;GdprNotification&gt;**](GdprNotification.md) |  |  |
|**refreshTokens** | [**List&lt;GdprRefreshToken&gt;**](GdprRefreshToken.md) | Session records: metadata only, never the token hash. |  |
|**tenants** | [**List&lt;GdprTenant&gt;**](GdprTenant.md) |  |  |
|**usageEvents** | [**List&lt;GdprUsageEvent&gt;**](GdprUsageEvent.md) |  |  |
|**user** | [**GdprUser**](GdprUser.md) |  |  |



