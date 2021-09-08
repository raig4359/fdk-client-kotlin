



### Class and Methods

* ## [FileStorage](#FileStorage)
  * Methods
    * [startUpload](#startupload)
    * [completeUpload](#completeupload)
    * [appStartUpload](#appstartupload)
    * [appCompleteUpload](#appcompleteupload)
    * [getSignUrls](#getsignurls)
    * [copyFiles](#copyfiles)
    * [appCopyFiles](#appcopyfiles)
    * [browse](#browse)
    * [browse](#browse)
    * [proxy](#proxy)
    
---

## FileStorage


#### startUpload
This operation initiates upload and returns storage link which is valid for 30 Minutes. You can use that storage link to make subsequent upload request with file buffer or blob.




```kotlin
client.filestorage.startUpload(namespace: namespace, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| namespace | String | yes | bucket name |   
| companyId | Int | yes | company_id |  
| body | [StartRequest](#StartRequest) | yes | Request body |


Uploads an arbitrarily sized buffer or blob.

It has three Major Steps:
* Start
* Upload
* Complete

### Start
Initiates the assets upload using `startUpload`.
It returns the storage link in response.

### Upload
Use the storage link to upload a file (Buffer or Blob) to the File Storage.
Make a `PUT` request on storage link received from `startUpload` api with file (Buffer or Blob) as a request body.

### Complete
After successfully upload, call `completeUpload` api to complete the upload process.
This operation will return the url for the uploaded file.


*Returned Response*




[StartResponse](#StartResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### completeUpload
This will complete the upload process. After successfully uploading file, you can call this operation to complete the upload process.




```kotlin
client.filestorage.completeUpload(namespace: namespace, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| namespace | String | yes | bucket name |   
| companyId | Int | yes | company_id |  
| body | [StartResponse](#StartResponse) | yes | Request body |


Uploads an arbitrarily sized buffer or blob.

It has three Major Steps:
* Start
* Upload
* Complete

### Start
Initiates the assets upload using `startUpload`.
It returns the storage link in response.

### Upload
Use the storage link to upload a file (Buffer or Blob) to the File Storage.
Make a `PUT` request on storage link received from `startUpload` api with file (Buffer or Blob) as a request body.

### Complete
After successfully upload, call `completeUpload` api to complete the upload process.
This operation will return the url for the uploaded file.


*Returned Response*




[CompleteResponse](#CompleteResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### appStartUpload
This operation initiates upload and returns storage link which is valid for 30 Minutes. You can use that storage link to make subsequent upload request with file buffer or blob.




```kotlin
client.application("<APPLICATION_ID>").filestorage.appStartUpload(namespace: namespace, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| namespace | String | yes | bucket name |   
| companyId | Int | yes | company_id |   
| applicationId | String | yes | application id |  
| body | [StartRequest](#StartRequest) | yes | Request body |


Uploads an arbitrarily sized buffer or blob.

It has three Major Steps:
* Start
* Upload
* Complete

### Start
Initiates the assets upload using `appStartUpload`.
It returns the storage link in response.

### Upload
Use the storage link to upload a file (Buffer or Blob) to the File Storage.
Make a `PUT` request on storage link received from `appStartUpload` api with file (Buffer or Blob) as a request body.

### Complete
After successfully upload, call `appCompleteUpload` api to complete the upload process.
This operation will return the url for the uploaded file.


*Returned Response*




[StartResponse](#StartResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### appCompleteUpload
This will complete the upload process. After successfully uploading file, you can call this operation to complete the upload process.




```kotlin
client.application("<APPLICATION_ID>").filestorage.appCompleteUpload(namespace: namespace, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| namespace | String | yes | bucket name |   
| companyId | Int | yes | company_id |   
| applicationId | String | yes | application id |  
| body | [StartResponse](#StartResponse) | yes | Request body |


Uploads an arbitrarily sized buffer or blob.

It has three Major Steps:
* Start
* Upload
* Complete

### Start
Initiates the assets upload using `appStartUpload`.
It returns the storage link in response.

### Upload
Use the storage link to upload a file (Buffer or Blob) to the File Storage.
Make a `PUT` request on storage link received from `appStartUpload` api with file (Buffer or Blob) as a request body.

### Complete
After successfully upload, call `appCompleteUpload` api to complete the upload process.
This operation will return the url for the uploaded file.


*Returned Response*




[CompleteResponse](#CompleteResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getSignUrls
Explain here




```kotlin
client.filestorage.getSignUrls(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | company_id |  
| body | [SignUrlRequest](#SignUrlRequest) | yes | Request body |


Describe here

*Returned Response*




[SignUrlResponse](#SignUrlResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### copyFiles
Copy Files




```kotlin
client.filestorage.copyFiles(sync: sync, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| sync | Boolean? | no | sync |   
| companyId | Int | yes | company_id |  
| body | [BulkRequest](#BulkRequest) | yes | Request body |


Copy Files

*Returned Response*




[BulkResponse](#BulkResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "tracking_url": "https://xxx.xxx.xxx/2",
  "task": {
    "id": "2",
    "name": "__default__",
    "data": {
      "urls": [
        "https://xxx.xxx.xxx/files.csv"
      ],
      "destination": {
        "namespace": "/domaine/path",
        "rewrite": "{{namespace}}/bar/{{dest.path}}"
      }
    },
    "opts": {
      "attempts": 1,
      "delay": 0,
      "timestamp": 1613534206645
    },
    "progress": 0,
    "delay": 0,
    "timestamp": 1613534206645,
    "attempts_made": 0,
    "stacktrace": [],
    "finished_on": 1613534206645,
    "processed_on": 1613534206645
  }
}
```
</details>









---


#### appCopyFiles
Copy Files




```kotlin
client.application("<APPLICATION_ID>").filestorage.appCopyFiles(sync: sync, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| sync | Boolean? | no | sync |   
| companyId | Int | yes | company_id |   
| applicationId | Int | yes | application_id |  
| body | [BulkRequest](#BulkRequest) | yes | Request body |


Copy Files

*Returned Response*




[BulkResponse](#BulkResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "tracking_url": "https://xxx.xxx.xxx/2",
  "task": {
    "id": "2",
    "name": "__default__",
    "data": {
      "urls": [
        "https://xxx.xxx.xxx/files.csv"
      ],
      "destination": {
        "namespace": "/domaine/path",
        "rewrite": "{{namespace}}/bar/{{dest.path}}"
      }
    },
    "opts": {
      "attempts": 1,
      "delay": 0,
      "timestamp": 1613534206645
    },
    "progress": 0,
    "delay": 0,
    "timestamp": 1613534206645,
    "attempts_made": 0,
    "stacktrace": [],
    "finished_on": 1613534206645,
    "processed_on": 1613534206645
  }
}
```
</details>









---


#### browse
Browse Files




```kotlin
client.filestorage.browse(namespace: namespace, pageNo: pageNo).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| namespace | String | yes | bucket name |   
| companyId | Int | yes | company_id |   
| pageNo | Int? | no | page no |  



Browse Files

*Returned Response*




[BrowseResponse](#BrowseResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### browse
Browse Files




```kotlin
client.application("<APPLICATION_ID>").filestorage.browse(namespace: namespace, pageNo: pageNo).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| namespace | String | yes | bucket name |   
| companyId | Int | yes | company_id |   
| applicationId | Int | yes | application_id |   
| pageNo | Int? | no | page no |  



Browse Files

*Returned Response*




[BrowseResponse](#BrowseResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### proxy
Proxy




```kotlin
client.filestorage.proxy(url: url).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | company_id |   
| url | String | yes | url |  



Proxy

*Returned Response*




[String](#String)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

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




