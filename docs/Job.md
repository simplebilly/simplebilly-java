

# Job


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**attempts** | **Integer** |  |  [optional] |
|**jobType** | **String** | Discriminator the worker dispatches on (e.g. \&quot;webhook.deliver\&quot;). |  |
|**maxAttempts** | **Integer** |  |  |
|**payload** | **Object** |  |  [optional] |
|**runAt** | **OffsetDateTime** | Earliest execution time; None &#x3D; run now. |  [optional] |
|**status** | **JobStatus** | pending | running | done | failed |  |



