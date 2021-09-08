



### Class and Methods

* ## [Rewards](#Rewards)
  * Methods
    * [getGiveaways](#getgiveaways)
    * [createGiveaway](#creategiveaway)
    * [getGiveawayByID](#getgiveawaybyid)
    * [updateGiveaway](#updategiveaway)
    * [getOffers](#getoffers)
    * [getOfferByName](#getofferbyname)
    * [updateOfferByName](#updateofferbyname)
    * [getUserAvailablePoints](#getuseravailablepoints)
    * [updateUserStatus](#updateuserstatus)
    * [getUserPointsHistory](#getuserpointshistory)
    
---

## Rewards


#### getGiveaways
List of giveaways of the current application.




```kotlin
client.application("<APPLICATION_ID>").rewards.getGiveaways(pageId: pageId, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | company id |   
| applicationId | String | yes | application id |   
| pageId | String? | no | pagination page id |   
| pageSize | Int? | no | pagination page size |  



List of giveaways of the current application.

*Returned Response*




[GiveawayResponse](#GiveawayResponse)

ok




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### createGiveaway
Adds a new giveaway.




```kotlin
client.application("<APPLICATION_ID>").rewards.createGiveaway(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | company id |   
| applicationId | String | yes | application id |  
| body | [Giveaway](#Giveaway) | yes | Request body |


Adds a new giveaway.

*Returned Response*




[Giveaway](#Giveaway)

ok




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getGiveawayByID
Get giveaway by ID.




```kotlin
client.application("<APPLICATION_ID>").rewards.getGiveawayByID(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | company id |   
| applicationId | String | yes | application id |   
| id | String | yes | Giveaway ID |  



Get giveaway by ID.

*Returned Response*




[Giveaway](#Giveaway)

ok




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### updateGiveaway
Updates the giveaway by it's ID.




```kotlin
client.application("<APPLICATION_ID>").rewards.updateGiveaway(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | company id |   
| applicationId | String | yes | application id |   
| id | String | yes | Giveaway ID |  
| body | [Giveaway](#Giveaway) | yes | Request body |


Updates the giveaway by it's ID.

*Returned Response*




[Giveaway](#Giveaway)

ok




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getOffers
List of offer of the current application.




```kotlin
client.application("<APPLICATION_ID>").rewards.getOffers().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | company id |   
| applicationId | String | yes | application id |  



List of offer of the current application.

*Returned Response*




[ArrayList<Offer>](#ArrayList<Offer>)

ok




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getOfferByName
Get offer by name.




```kotlin
client.application("<APPLICATION_ID>").rewards.getOfferByName(cookie: cookie, name: name).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | company id |   
| applicationId | String | yes | application id |   
| cookie | String | yes | User's session cookie. This cookie is set in browser cookie when logged-in to fynd's authentication system i.e. `Grimlock` or by using grimlock-backend SDK for backend implementation. |   
| name | String | yes | Offer name |  



Get offer by name.

*Returned Response*




[Offer](#Offer)

ok




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### updateOfferByName
Updates the offer by name.




```kotlin
client.application("<APPLICATION_ID>").rewards.updateOfferByName(name: name, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | company id |   
| applicationId | String | yes | application id |   
| name | String | yes | Offer name |  
| body | [Offer](#Offer) | yes | Request body |


Updates the offer by name.

*Returned Response*




[Offer](#Offer)

ok




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getUserAvailablePoints
User's reward details.




```kotlin
client.application("<APPLICATION_ID>").rewards.getUserAvailablePoints(userId: userId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | company id |   
| applicationId | String | yes | application id |   
| userId | String | yes | user id |  



User's reward details.

*Returned Response*




[UserRes](#UserRes)

ok




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### updateUserStatus
Update User status




```kotlin
client.application("<APPLICATION_ID>").rewards.updateUserStatus(userId: userId, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | company id |   
| applicationId | String | yes | application id |   
| userId | String | yes | user id |  
| body | [AppUser](#AppUser) | yes | Request body |


Update user status, active/archive

*Returned Response*




[AppUser](#AppUser)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getUserPointsHistory
Get list of points transactions.




```kotlin
client.application("<APPLICATION_ID>").rewards.getUserPointsHistory(userId: userId, pageId: pageId, pageLimit: pageLimit, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | company id |   
| applicationId | String | yes | application id |   
| userId | String | yes | user id |   
| pageId | String? | no | PageID is the ID of the requested page. For first request it should be kept empty. |   
| pageLimit | Int? | no | PageLimit is the number of requested items in response. |   
| pageSize | Int? | no | PageSize is the number of requested items in response. |  



Get list of points transactions.
The list of points history is paginated.

*Returned Response*




[HistoryRes](#HistoryRes)

ok




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




