

# PlanLimits

Per-plan numeric limits. `-1` in any field means unlimited.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**maxConnectors** | **Integer** |  |  |
|**maxInvoicesPerMonth** | **Long** |  |  |
|**maxUsers** | **Integer** |  |  |
|**metered** | **Map&lt;String, Long&gt;** |  |  [optional] |
|**paidConnectors** | **List&lt;String&gt;** | Connectors that are *not* included in this plan (require a higher tier). Empty &#x3D; all connectors included on this plan. |  |



