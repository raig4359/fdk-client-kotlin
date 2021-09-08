



### Class and Methods

* ## [Communication](#Communication)
  * Methods
    * [getCampaigns](#getcampaigns)
    * [createCampaign](#createcampaign)
    * [getCampaignById](#getcampaignbyid)
    * [updateCampaignById](#updatecampaignbyid)
    * [getStatsOfCampaignById](#getstatsofcampaignbyid)
    * [getAudiences](#getaudiences)
    * [createAudience](#createaudience)
    * [getBigqueryHeaders](#getbigqueryheaders)
    * [getAudienceById](#getaudiencebyid)
    * [updateAudienceById](#updateaudiencebyid)
    * [getNSampleRecordsFromCsv](#getnsamplerecordsfromcsv)
    * [getEmailProviders](#getemailproviders)
    * [createEmailProvider](#createemailprovider)
    * [getEmailProviderById](#getemailproviderbyid)
    * [updateEmailProviderById](#updateemailproviderbyid)
    * [getEmailTemplates](#getemailtemplates)
    * [createEmailTemplate](#createemailtemplate)
    * [getSystemEmailTemplates](#getsystememailtemplates)
    * [getEmailTemplateById](#getemailtemplatebyid)
    * [updateEmailTemplateById](#updateemailtemplatebyid)
    * [deleteEmailTemplateById](#deleteemailtemplatebyid)
    * [getEventSubscriptions](#geteventsubscriptions)
    * [getJobs](#getjobs)
    * [triggerCampaignJob](#triggercampaignjob)
    * [getJobLogs](#getjoblogs)
    * [getCommunicationLogs](#getcommunicationlogs)
    * [getSystemNotifications](#getsystemnotifications)
    * [getSmsProviders](#getsmsproviders)
    * [createSmsProvider](#createsmsprovider)
    * [getSmsProviderById](#getsmsproviderbyid)
    * [updateSmsProviderById](#updatesmsproviderbyid)
    * [getSmsTemplates](#getsmstemplates)
    * [createSmsTemplate](#createsmstemplate)
    * [getSmsTemplateById](#getsmstemplatebyid)
    * [updateSmsTemplateById](#updatesmstemplatebyid)
    * [deleteSmsTemplateById](#deletesmstemplatebyid)
    * [getSystemSystemTemplates](#getsystemsystemtemplates)
    
---

## Communication


#### getCampaigns
Get campaigns




```kotlin
client.application("<APPLICATION_ID>").communication.getCampaigns(pageNo: pageNo, pageSize: pageSize, sort: sort).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |   
| sort | HashMap<String,Any>? | no | To sort based on created_at |  



Get campaigns

*Returned Response*




[Campaigns](#Campaigns)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/Campaigns"
}
```
</details>

</details>









---


#### createCampaign
Create campaign




```kotlin
client.application("<APPLICATION_ID>").communication.createCampaign(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |  
| body | [CampaignReq](#CampaignReq) | yes | Request body |


Create campaign

*Returned Response*




[Campaign](#Campaign)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/Campaign"
}
```
</details>

</details>









---


#### getCampaignById
Get campaign by id




```kotlin
client.application("<APPLICATION_ID>").communication.getCampaignById(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Campaign id |  



Get campaign by id

*Returned Response*




[Campaign](#Campaign)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/Campaign"
}
```
</details>

</details>









---


#### updateCampaignById
Update campaign by id




```kotlin
client.application("<APPLICATION_ID>").communication.updateCampaignById(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Campaign id |  
| body | [CampaignReq](#CampaignReq) | yes | Request body |


Update campaign by id

*Returned Response*




[Campaign](#Campaign)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/Campaign"
}
```
</details>

</details>









---


#### getStatsOfCampaignById
Get stats of campaign by id




```kotlin
client.application("<APPLICATION_ID>").communication.getStatsOfCampaignById(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Campaign id |  



Get stats of campaign by id

*Returned Response*




[GetStats](#GetStats)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/GetStats"
}
```
</details>

</details>









---


#### getAudiences
Get audiences




```kotlin
client.application("<APPLICATION_ID>").communication.getAudiences(pageNo: pageNo, pageSize: pageSize, sort: sort).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |   
| sort | HashMap<String,Any>? | no | To sort based on created_at |  



Get audiences

*Returned Response*




[Audiences](#Audiences)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/Audiences"
}
```
</details>

</details>









---


#### createAudience
Create audience




```kotlin
client.application("<APPLICATION_ID>").communication.createAudience(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |  
| body | [AudienceReq](#AudienceReq) | yes | Request body |


Create audience

*Returned Response*




[Audience](#Audience)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/Audience"
}
```
</details>

</details>









---


#### getBigqueryHeaders
Get bigquery headers




```kotlin
client.application("<APPLICATION_ID>").communication.getBigqueryHeaders(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |  
| body | [BigqueryHeadersReq](#BigqueryHeadersReq) | yes | Request body |


Get bigquery headers

*Returned Response*




[BigqueryHeadersRes](#BigqueryHeadersRes)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/BigqueryHeadersRes"
}
```
</details>

</details>









---


#### getAudienceById
Get audience by id




```kotlin
client.application("<APPLICATION_ID>").communication.getAudienceById(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Audience id |  



Get audience by id

*Returned Response*




[Audience](#Audience)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/Audience"
}
```
</details>

</details>









---


#### updateAudienceById
Update audience by id




```kotlin
client.application("<APPLICATION_ID>").communication.updateAudienceById(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Audience id |  
| body | [AudienceReq](#AudienceReq) | yes | Request body |


Update audience by id

*Returned Response*




[Audience](#Audience)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/Audience"
}
```
</details>

</details>









---


#### getNSampleRecordsFromCsv
Get n sample records from csv




```kotlin
client.application("<APPLICATION_ID>").communication.getNSampleRecordsFromCsv(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |  
| body | [GetNRecordsCsvReq](#GetNRecordsCsvReq) | yes | Request body |


Get n sample records from csv

*Returned Response*




[GetNRecordsCsvRes](#GetNRecordsCsvRes)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/GetNRecordsCsvRes"
}
```
</details>

</details>









---


#### getEmailProviders
Get email providers




```kotlin
client.application("<APPLICATION_ID>").communication.getEmailProviders(pageNo: pageNo, pageSize: pageSize, sort: sort).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |   
| sort | HashMap<String,Any>? | no | To sort based on created_at |  



Get email providers

*Returned Response*




[EmailProviders](#EmailProviders)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/EmailProviders"
}
```
</details>

</details>









---


#### createEmailProvider
Create email provider




```kotlin
client.application("<APPLICATION_ID>").communication.createEmailProvider(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |  
| body | [EmailProviderReq](#EmailProviderReq) | yes | Request body |


Create email provider

*Returned Response*




[EmailProvider](#EmailProvider)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/EmailProvider"
}
```
</details>

</details>









---


#### getEmailProviderById
Get email provider by id




```kotlin
client.application("<APPLICATION_ID>").communication.getEmailProviderById(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Email provider id |  



Get email provider by id

*Returned Response*




[EmailProvider](#EmailProvider)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/EmailProvider"
}
```
</details>

</details>









---


#### updateEmailProviderById
Update email provider by id




```kotlin
client.application("<APPLICATION_ID>").communication.updateEmailProviderById(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Email provider id |  
| body | [EmailProviderReq](#EmailProviderReq) | yes | Request body |


Update email provider by id

*Returned Response*




[EmailProvider](#EmailProvider)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/EmailProvider"
}
```
</details>

</details>









---


#### getEmailTemplates
Get email templates




```kotlin
client.application("<APPLICATION_ID>").communication.getEmailTemplates(pageNo: pageNo, pageSize: pageSize, sort: sort).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |   
| sort | HashMap<String,Any>? | no | To sort based on created_at |  



Get email templates

*Returned Response*




[EmailTemplates](#EmailTemplates)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/EmailTemplates"
}
```
</details>

</details>









---


#### createEmailTemplate
Create email template




```kotlin
client.application("<APPLICATION_ID>").communication.createEmailTemplate(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |  
| body | [EmailTemplateReq](#EmailTemplateReq) | yes | Request body |


Create email template

*Returned Response*




[EmailTemplateRes](#EmailTemplateRes)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/EmailTemplateRes"
}
```
</details>

</details>









---


#### getSystemEmailTemplates
Get system email templates




```kotlin
client.application("<APPLICATION_ID>").communication.getSystemEmailTemplates(pageNo: pageNo, pageSize: pageSize, sort: sort).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |   
| sort | HashMap<String,Any>? | no | To sort based on created_at |  



Get system email templates

*Returned Response*




[SystemEmailTemplates](#SystemEmailTemplates)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SystemEmailTemplates"
}
```
</details>

</details>









---


#### getEmailTemplateById
Get email template by id




```kotlin
client.application("<APPLICATION_ID>").communication.getEmailTemplateById(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Email template id |  



Get email template by id

*Returned Response*




[EmailTemplate](#EmailTemplate)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/EmailTemplate"
}
```
</details>

</details>









---


#### updateEmailTemplateById
Update email template by id




```kotlin
client.application("<APPLICATION_ID>").communication.updateEmailTemplateById(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Email template id |  
| body | [EmailTemplateReq](#EmailTemplateReq) | yes | Request body |


Update email template by id

*Returned Response*




[EmailTemplateRes](#EmailTemplateRes)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/EmailTemplateRes"
}
```
</details>

</details>









---


#### deleteEmailTemplateById
Delete email template by id




```kotlin
client.application("<APPLICATION_ID>").communication.deleteEmailTemplateById(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Email template id |  



Delete email template by id

*Returned Response*




[EmailTemplateDeleteSuccessRes](#EmailTemplateDeleteSuccessRes)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/EmailTemplateDeleteSuccessRes"
}
```
</details>

</details>









---


#### getEventSubscriptions
Get event subscriptions




```kotlin
client.application("<APPLICATION_ID>").communication.getEventSubscriptions(pageNo: pageNo, pageSize: pageSize, populate: populate).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |   
| populate | String? | no | populate fields |  



Get event subscriptions

*Returned Response*




[EventSubscriptions](#EventSubscriptions)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/EventSubscriptions"
}
```
</details>

</details>









---


#### getJobs
Get jobs




```kotlin
client.application("<APPLICATION_ID>").communication.getJobs(pageNo: pageNo, pageSize: pageSize, sort: sort).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |   
| sort | HashMap<String,Any>? | no | To sort based on created_at |  



Get jobs

*Returned Response*




[Jobs](#Jobs)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/Jobs"
}
```
</details>

</details>









---


#### triggerCampaignJob
Trigger campaign job




```kotlin
client.application("<APPLICATION_ID>").communication.triggerCampaignJob(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |  
| body | [TriggerJobRequest](#TriggerJobRequest) | yes | Request body |


Trigger campaign job

*Returned Response*




[TriggerJobResponse](#TriggerJobResponse)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/TriggerJobResponse"
}
```
</details>

</details>









---


#### getJobLogs
Get job logs




```kotlin
client.application("<APPLICATION_ID>").communication.getJobLogs(pageNo: pageNo, pageSize: pageSize, sort: sort).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |   
| sort | HashMap<String,Any>? | no | To sort based on created_at |  



Get job logs

*Returned Response*




[JobLogs](#JobLogs)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/JobLogs"
}
```
</details>

</details>









---


#### getCommunicationLogs
Get communication logs




```kotlin
client.application("<APPLICATION_ID>").communication.getCommunicationLogs(pageId: pageId, pageSize: pageSize, sort: sort, query: query).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| pageId | String? | no | Current page no |   
| pageSize | Int? | no | Current request items count |   
| sort | HashMap<String,Any>? | no | To sort based on _id |   
| query | HashMap<String,Any>? | no |  |  



Get communication logs

*Returned Response*




[Logs](#Logs)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/Logs"
}
```
</details>

</details>









---


#### getSystemNotifications
Get system notifications




```kotlin
client.communication.getSystemNotifications(pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| pageNo | Int? | no |  |   
| pageSize | Int? | no |  |  



Get system notifications

*Returned Response*




[SystemNotifications](#SystemNotifications)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SystemNotifications"
}
```
</details>

</details>









---


#### getSmsProviders
Get sms providers




```kotlin
client.application("<APPLICATION_ID>").communication.getSmsProviders(pageNo: pageNo, pageSize: pageSize, sort: sort).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |   
| sort | HashMap<String,Any>? | no | To sort based on created_at |  



Get sms providers

*Returned Response*




[SmsProviders](#SmsProviders)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SmsProviders"
}
```
</details>

</details>









---


#### createSmsProvider
Create sms provider




```kotlin
client.application("<APPLICATION_ID>").communication.createSmsProvider(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |  
| body | [SmsProviderReq](#SmsProviderReq) | yes | Request body |


Create sms provider

*Returned Response*




[SmsProvider](#SmsProvider)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SmsProvider"
}
```
</details>

</details>









---


#### getSmsProviderById
Get sms provider by id




```kotlin
client.application("<APPLICATION_ID>").communication.getSmsProviderById(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Sms provider id |  



Get sms provider by id

*Returned Response*




[SmsProvider](#SmsProvider)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SmsProvider"
}
```
</details>

</details>









---


#### updateSmsProviderById
Update sms provider by id




```kotlin
client.application("<APPLICATION_ID>").communication.updateSmsProviderById(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Sms provider id |  
| body | [SmsProviderReq](#SmsProviderReq) | yes | Request body |


Update sms provider by id

*Returned Response*




[SmsProvider](#SmsProvider)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SmsProvider"
}
```
</details>

</details>









---


#### getSmsTemplates
Get sms templates




```kotlin
client.application("<APPLICATION_ID>").communication.getSmsTemplates(pageNo: pageNo, pageSize: pageSize, sort: sort).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |   
| sort | HashMap<String,Any>? | no | To sort based on created_at |  



Get sms templates

*Returned Response*




[SmsTemplates](#SmsTemplates)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SmsTemplates"
}
```
</details>

</details>









---


#### createSmsTemplate
Create sms template




```kotlin
client.application("<APPLICATION_ID>").communication.createSmsTemplate(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |  
| body | [SmsTemplateReq](#SmsTemplateReq) | yes | Request body |


Create sms template

*Returned Response*




[SmsTemplateRes](#SmsTemplateRes)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SmsTemplateRes"
}
```
</details>

</details>









---


#### getSmsTemplateById
Get sms template by id




```kotlin
client.application("<APPLICATION_ID>").communication.getSmsTemplateById(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Sms template id |  



Get sms template by id

*Returned Response*




[SmsTemplate](#SmsTemplate)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SmsTemplate"
}
```
</details>

</details>









---


#### updateSmsTemplateById
Update sms template by id




```kotlin
client.application("<APPLICATION_ID>").communication.updateSmsTemplateById(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Sms template id |  
| body | [SmsTemplateReq](#SmsTemplateReq) | yes | Request body |


Update sms template by id

*Returned Response*




[SmsTemplateRes](#SmsTemplateRes)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SmsTemplateRes"
}
```
</details>

</details>









---


#### deleteSmsTemplateById
Delete sms template by id




```kotlin
client.application("<APPLICATION_ID>").communication.deleteSmsTemplateById(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| id | String | yes | Sms template id |  



Delete sms template by id

*Returned Response*




[SmsTemplateDeleteSuccessRes](#SmsTemplateDeleteSuccessRes)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SmsTemplateDeleteSuccessRes"
}
```
</details>

</details>









---


#### getSystemSystemTemplates
Get system sms templates




```kotlin
client.application("<APPLICATION_ID>").communication.getSystemSystemTemplates(pageNo: pageNo, pageSize: pageSize, sort: sort).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company id |   
| applicationId | String | yes | Application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |   
| sort | HashMap<String,Any>? | no | To sort based on created_at |  



Get system sms templates

*Returned Response*




[SystemSmsTemplates](#SystemSmsTemplates)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SystemSmsTemplates"
}
```
</details>

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




