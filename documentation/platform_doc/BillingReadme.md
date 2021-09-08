



### Class and Methods

* ## [Billing](#Billing)
  * Methods
    * [createSubscriptionCharge](#createsubscriptioncharge)
    * [getSubscriptionCharge](#getsubscriptioncharge)
    * [cancelSubscriptionCharge](#cancelsubscriptioncharge)
    * [getInvoices](#getinvoices)
    * [getInvoiceById](#getinvoicebyid)
    * [getCustomerDetail](#getcustomerdetail)
    * [upsertCustomerDetail](#upsertcustomerdetail)
    * [getSubscription](#getsubscription)
    * [getFeatureLimitConfig](#getfeaturelimitconfig)
    * [activateSubscriptionPlan](#activatesubscriptionplan)
    * [cancelSubscriptionPlan](#cancelsubscriptionplan)
    
---

## Billing


#### createSubscriptionCharge
Create subscription charge




```kotlin
client.billing.createSubscriptionCharge(extensionId: extensionId, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Customer unique id. In case of company it will be company id. |   
| extensionId | String | yes | Extension _id |  
| body | [CreateSubscriptionCharge](#CreateSubscriptionCharge) | yes | Request body |


Register subscription charge for a seller of your extension.

*Returned Response*




[CreateSubscriptionResponse](#CreateSubscriptionResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getSubscriptionCharge
Get subscription charge details




```kotlin
client.billing.getSubscriptionCharge(extensionId: extensionId, subscriptionId: subscriptionId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Customer unique id. In case of company it will be company id. |   
| extensionId | String | yes | Extension _id |   
| subscriptionId | String | yes | Subscription charge _id |  



Get created subscription charge details

*Returned Response*




[EntitySubscription](#EntitySubscription)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### cancelSubscriptionCharge
Cancel subscription charge




```kotlin
client.billing.cancelSubscriptionCharge(extensionId: extensionId, subscriptionId: subscriptionId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Customer unique id. In case of company it will be company id. |   
| extensionId | String | yes | Extension _id |   
| subscriptionId | String | yes | Subscription charge _id |  



Cancel subscription and attached charges.

*Returned Response*




[EntitySubscription](#EntitySubscription)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getInvoices
Get invoices




```kotlin
client.billing.getInvoices().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Customer unique id. In case of company it will be company id. |  



Get invoices.

*Returned Response*




[Invoices](#Invoices)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/Invoices"
}
```
</details>

</details>









---


#### getInvoiceById
Get invoice by id




```kotlin
client.billing.getInvoiceById(invoiceId: invoiceId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Customer unique id. In case of company it will be company id. |   
| invoiceId | String | yes | Invoice id |  



Get invoice by id.

*Returned Response*




[Invoice](#Invoice)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/Invoice"
}
```
</details>

</details>









---


#### getCustomerDetail
Get subscription customer detail




```kotlin
client.billing.getCustomerDetail().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Customer unique id. In case of company it will be company id. |  



Get subscription customer detail.

*Returned Response*




[SubscriptionCustomer](#SubscriptionCustomer)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SubscriptionCustomerRes"
}
```
</details>

</details>









---


#### upsertCustomerDetail
Upsert subscription customer detail




```kotlin
client.billing.upsertCustomerDetail(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Customer unique id. In case of company it will be company id. |  
| body | [SubscriptionCustomerCreate](#SubscriptionCustomerCreate) | yes | Request body |


Upsert subscription customer detail.

*Returned Response*




[SubscriptionCustomer](#SubscriptionCustomer)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SubscriptionCustomerRes"
}
```
</details>

</details>









---


#### getSubscription
Get current subscription detail




```kotlin
client.billing.getSubscription().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Customer unique id. In case of company it will be company id. |  



If subscription is active then it will return is_enabled true and return subscription object. If subscription is not active then is_enabled false and message.


*Returned Response*




[SubscriptionStatus](#SubscriptionStatus)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Active subscription</i></summary>

```json
{
  "$ref": "#/components/examples/SubscriptionActiveRes"
}
```
</details>

<details>
<summary><i>&nbsp; Inactive subscription</i></summary>

```json
{
  "$ref": "#/components/examples/SubscriptionInavtiveRes"
}
```
</details>

</details>









---


#### getFeatureLimitConfig
Get subscription subscription limits




```kotlin
client.billing.getFeatureLimitConfig().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Customer unique id. In case of company it will be company id. |  



Get subscription subscription limits.

*Returned Response*




[SubscriptionLimit](#SubscriptionLimit)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/CurrentLimitRes"
}
```
</details>

</details>









---


#### activateSubscriptionPlan
Activate subscription




```kotlin
client.billing.activateSubscriptionPlan(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Customer unique id. In case of company it will be company id. |  
| body | [SubscriptionActivateReq](#SubscriptionActivateReq) | yes | Request body |


It will activate subscription plan for customer

*Returned Response*




[SubscriptionActivateRes](#SubscriptionActivateRes)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/SubscriptionActivateRes"
}
```
</details>

</details>









---


#### cancelSubscriptionPlan
Cancel subscription




```kotlin
client.billing.cancelSubscriptionPlan(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Customer unique id. In case of company it will be company id. |  
| body | [CancelSubscriptionReq](#CancelSubscriptionReq) | yes | Request body |


It will cancel current active subscription.

*Returned Response*




[CancelSubscriptionRes](#CancelSubscriptionRes)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; default</i></summary>

```json
{
  "$ref": "#/components/examples/CancelSubscriptionRes"
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




