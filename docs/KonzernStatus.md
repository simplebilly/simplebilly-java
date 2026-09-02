

# KonzernStatus


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**groessenbefreit** | **Boolean** |  |  |
|**kapitalmarktorientiert** | **Boolean** |  |  |
|**konzernabschlusspflicht** | **Boolean** |  |  |
|**missingGroupFigures** | **Boolean** | Keine group_figures-Zeile für das Jahr vorhanden → keine Größenbefreiung. |  |
|**mutterunternehmen** | **Boolean** | Mutterunternehmen: mindestens eine beherrschte Beteiligung (§ 290 Abs. 1 HGB). |  |
|**parentName** | **String** | Mutterunternehmen für die Zwischenholding-Befreiung (§ 291 HGB). |  [optional] |
|**parentSitus** | **String** |  |  [optional] |
|**participations** | [**List&lt;KonzernBeteiligung&gt;**](KonzernBeteiligung.md) |  |  |
|**thresholds** | [**KonzernThresholds**](KonzernThresholds.md) |  |  |
|**year** | **Integer** |  |  |
|**zwischenholdingBefreit** | **Boolean** |  |  |
|**zwischenholdingHinweis** | **String** | Hinweis zu den § 291-Voraussetzungen (EU/EWR-Sitz, geprüfter Konzernabschluss). |  [optional] |



