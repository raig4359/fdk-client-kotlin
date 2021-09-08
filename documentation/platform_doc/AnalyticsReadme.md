



### Class and Methods

* ## [Analytics](#Analytics)
  * Methods
    * [getStatiscticsGroups](#getstatiscticsgroups)
    * [getStatiscticsGroupComponents](#getstatiscticsgroupcomponents)
    * [getComponentStatsCSV](#getcomponentstatscsv)
    * [getComponentStatsPDF](#getcomponentstatspdf)
    * [getComponentStats](#getcomponentstats)
    * [getAbandonCartList](#getabandoncartlist)
    * [getAbandonCartsCSV](#getabandoncartscsv)
    * [getAbandonCartDetail](#getabandoncartdetail)
    * [createExportJob](#createexportjob)
    * [getExportJobStatus](#getexportjobstatus)
    * [getLogsList](#getlogslist)
    * [searchLogs](#searchlogs)
    
---

## Analytics


#### getStatiscticsGroups
Get statistics groups




```kotlin
client.application("<APPLICATION_ID>").analytics.getStatiscticsGroups().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id |   
| applicationId | String | yes | Application Id |  



Get statistics groups

*Returned Response*




[StatsGroups](#StatsGroups)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "groups": [
    {
      "key": "general",
      "url": "/v1/group/general",
      "title": "General"
    }
  ]
}
```
</details>









---


#### getStatiscticsGroupComponents
Get statistics group components




```kotlin
client.application("<APPLICATION_ID>").analytics.getStatiscticsGroupComponents(groupName: groupName).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id |   
| applicationId | String | yes | Application Id |   
| groupName | String | yes | Group name |  



Get statistics group components

*Returned Response*




[StatsGroupComponents](#StatsGroupComponents)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "title": "Catalogue & Inventory",
  "components": [
    {
      "key": "catalogue-basic",
      "title": "Catalogue Basic",
      "type": "text-blocks",
      "url": "/stats/component/catalogue-basic",
      "filters": {}
    }
  ]
}
```
</details>









---


#### getComponentStatsCSV
Get component statistics csv




```kotlin
client.application("<APPLICATION_ID>").analytics.getComponentStatsCSV(componentName: componentName).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id |   
| applicationId | String | yes | Application Id |   
| componentName | String | yes | Component name |  



Get component statistics csv

*Returned Response*




[String](#String)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getComponentStatsPDF
Get component statistics pdf




```kotlin
client.application("<APPLICATION_ID>").analytics.getComponentStatsPDF(componentName: componentName).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id |   
| applicationId | String | yes | Application Id |   
| componentName | String | yes | Component name |  



Get component statistics pdf

*Returned Response*




[String](#String)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getComponentStats
Get component statistics




```kotlin
client.application("<APPLICATION_ID>").analytics.getComponentStats(componentName: componentName).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id |   
| applicationId | String | yes | Application Id |   
| componentName | String | yes | Component name |  



Get component statistics

*Returned Response*




[StatsRes](#StatsRes)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "key": "article-distribution",
  "title": "Inventory Distribution",
  "type": "chart.pie",
  "data": {
    "raw": [
      {
        "name": "Fatimah Logero",
        "available_articles": 8,
        "total_articles": 9,
        "available_sizes": 3,
        "total_sizes": 3,
        "article_freshness": 9,
        "count": 0,
        "percent": "NaN"
      }
    ],
    "type": "pie",
    "data": {
      "datasets": [
        {
          "label": "# of products",
          "backgroundColor": [
            "#7986CB",
            "#3F51B5"
          ],
          "data": [
            8,
            1
          ],
          "percent": [
            "88.89",
            "11.11"
          ]
        }
      ],
      "labels": [
        "Available Articles",
        "Articles Out Of Stock"
      ]
    },
    "options": {
      "responsive": true,
      "display": false
    },
    "cache_hit": false
  }
}
```
</details>









---


#### getAbandonCartList
Get abandon carts list




```kotlin
client.application("<APPLICATION_ID>").analytics.getAbandonCartList(fromDate: fromDate, toDate: toDate, pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id |   
| applicationId | String | yes | Application Id |   
| fromDate | String | yes | From date |   
| toDate | String | yes | To date |   
| pageNo | Int? | no | Current page number |   
| pageSize | Int? | no | Current page size |  



Get abandon carts list

*Returned Response*




[AbandonCartsList](#AbandonCartsList)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": {
    "properties_cart_id": 11517,
    "context_traits_first_name": "Ahmed",
    "context_traits_last_name": "Sakri",
    "context_traits_phone_number": "8433859662",
    "context_traits_email": "ahmedsakri@gofynd.com",
    "context_app_application_id": "000000000000000000000001",
    "properties_breakup_values_raw_total": 4020,
    "received_at": {
      "value": "2021-03-09T05:09:06.840Z"
    }
  },
  "page": {
    "type": "number",
    "size": 10,
    "current": 1,
    "has_next": true,
    "item_total": 15
  }
}
```
</details>









---


#### getAbandonCartsCSV
Get abandon carts csv




```kotlin
client.application("<APPLICATION_ID>").analytics.getAbandonCartsCSV(fromDate: fromDate, toDate: toDate).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id |   
| applicationId | String | yes | Application Id |   
| fromDate | String | yes | From date |   
| toDate | String | yes | To date |  



Get abandon carts csv

*Returned Response*




[String](#String)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getAbandonCartDetail
Get abandon carts details




```kotlin
client.application("<APPLICATION_ID>").analytics.getAbandonCartDetail(cartId: cartId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id |   
| applicationId | String | yes | Application Id |   
| cartId | String | yes | Cart Id |  



Get abandon cart details

*Returned Response*




[AbandonCartDetail](#AbandonCartDetail)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### createExportJob
Create data export job in required format




```kotlin
client.analytics.createExportJob(exportType: exportType, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id |   
| exportType | String | yes | Export type / format |  
| body | [ExportJobReq](#ExportJobReq) | yes | Request body |


Create data export job in required format

*Returned Response*




[ExportJobRes](#ExportJobRes)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "status": "queued",
  "job_id": "6047c67060ad8241a948ee42"
}
```
</details>









---


#### getExportJobStatus
Get data export job status




```kotlin
client.analytics.getExportJobStatus(exportType: exportType, jobId: jobId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id |   
| exportType | String | yes | Export type / format |   
| jobId | String | yes | Export job id |  



Get data export job status

*Returned Response*




[ExportJobStatusRes](#ExportJobStatusRes)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "download_url": "https://marketplace-sync-logs-production.s3.ap-south-1.amazonaws.com/inv-log-37-flipkartAssured-Full_Inventory_Update.csv",
  "status": "success",
  "job_id": "6047c67060ad8241a948ee42"
}
```
</details>









---


#### getLogsList
Get logs list




```kotlin
client.analytics.getLogsList(logType: logType, pageNo: pageNo, pageSize: pageSize, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id |   
| logType | String | yes | Log type |   
| pageNo | Int? | no | Current page number |   
| pageSize | Int? | no | Current page size |  
| body | [GetLogsListReq](#GetLogsListReq) | yes | Request body |


Get logs list

*Returned Response*




[GetLogsListRes](#GetLogsListRes)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "start_time_iso": "2021-04-06T19:00:17.013Z",
      "end_time_iso": "2021-04-06T19:00:17.015Z",
      "event_type": "FULL_PRICE_UPDATE",
      "trace_id": "marketplaces.aa18fa48-b3e8-4e1e-8396-69488e254ace",
      "count": 17,
      "status": "failed"
    }
  ],
  "page": {
    "type": "number",
    "size": 10,
    "current": 1,
    "has_next": true,
    "item_total": 88
  }
}
```
</details>









---


#### searchLogs
Search logs




```kotlin
client.analytics.searchLogs(pageNo: pageNo, pageSize: pageSize, logType: logType, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id |   
| pageNo | Int? | no | Current page number |   
| pageSize | Int? | no | Current page size |   
| logType | String | yes | Log type |  
| body | [SearchLogReq](#SearchLogReq) | yes | Request body |


Search logs

*Returned Response*




[SearchLogRes](#SearchLogRes)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "_id": "606cafc19c2c466b24098437",
      "status": "failed",
      "event_type": "FULL_PRICE_UPDATE",
      "marketplace_name": "myntra",
      "event": "APPLICATION_FULL_INVENTORY",
      "trace_id": "marketplaces.aa18fa48-b3e8-4e1e-8396-69488e254ace",
      "company_id": 28,
      "brand_id": 44,
      "store_id": 57,
      "item_id": 882857,
      "article_id": "57_sku_102831159-TBUCKBEIGE_301066XL",
      "seller_identifier": "SKU_102831159-TBUCKBEIGE_392826XL"
    }
  ],
  "page": {
    "type": "number",
    "size": 10,
    "current": 1,
    "has_next": true,
    "item_total": 88
  }
}
```
</details>









---



### Schemas


### Enums







 #### [PriorityEnum](#PriorityEnum)
 Type : string

 | Name | Value | Description |
 | ---- | ----- | ----------- |
 | low | low | This means ticket is low priority |
 | medium | medium | This means ticket is medium priority |
 | high | high | This means ticket is high priority |
 | urgent | urgent | This means ticket is of urgent priority |

---



 #### [HistoryTypeEnum](#HistoryTypeEnum)
 Type : string

 | Name | Value | Description |
 | ---- | ----- | ----------- |
 | rating | rating | This means history event is a rating |
 | log | log | This means history event is a changelog |
 | comment | comment | This means history event is a comment |

---



 #### [TicketAssetType](#TicketAssetType)
 Type : string

 | Name | Value | Description |
 | ---- | ----- | ----------- |
 | image | image | Denotes asset is of image type |
 | video | video | Denotes asset is of video type |
 | file | file | Denotes asset is of file type |
 | youtube | youtube | Denotes asset is an youtube link |
 | product | product | Denotes asset is of product type |
 | collection | collection | Denotes asset is of collection type |
 | brand | brand | Denotes asset is of brand type |
 | shipment | shipment | Denotes asset is of shipment type |
 | order | order | Denotes asset is of order type |

---



 #### [TicketSourceEnum](#TicketSourceEnum)
 Type : string

 | Name | Value | Description |
 | ---- | ----- | ----------- |
 | platformPanel | platform_panel | This means it is company level ticket |
 | salesChannel | sales_channel | This means it is a application/sales channel level ticket |

---











































 #### [SubscriberStatus](#SubscriberStatus)
 Type : string

 | Name | Value | Description |
 | ---- | ----- | ----------- |
 | active | active | Status is active |
 | inactive | inactive | Status is inactive |

---




