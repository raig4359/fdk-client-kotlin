



### Class and Methods

* ## [User](#User)
  * Methods
    * [getCustomers](#getcustomers)
    * [searchUsers](#searchusers)
    * [createUser](#createuser)
    * [updateUser](#updateuser)
    * [createUserSession](#createusersession)
    * [getPlatformConfig](#getplatformconfig)
    * [updatePlatformConfig](#updateplatformconfig)
    
---

## User


#### getCustomers
Get a list of customers




```kotlin
client.application("<APPLICATION_ID>").user.getCustomers(q: q, pageSize: pageSize, pageNo: pageNo).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Numeric ID allotted to a business account on Fynd Platform. |   
| applicationId | String | yes | Alphanumeric ID allotted to an application created within a business account. |   
| q | String? | no | The search query. Mobile number or email ID of a customer. |   
| pageSize | Int? | no | The number of items to retrieve in each page. Default value is 10. |   
| pageNo | Int? | no | The page number to navigate through the given set of results. Default value is 1.  |  



Use this API to retrieve a list of customers who have registered in the application.

*Returned Response*




[CustomerListResponseSchema](#CustomerListResponseSchema)

Success. Refer `CustomerListResponseSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/CustomersListResponse"
}
```
</details>

</details>









---


#### searchUsers
Search an existing user.




```kotlin
client.application("<APPLICATION_ID>").user.searchUsers(q: q).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Numeric ID allotted to a business account on Fynd Platform. |   
| applicationId | String | yes | Alphanumeric ID allotted to an application created within a business account. |   
| q | String? | no | The search query. Mobile number or email ID of a customer. |  



Use this API to retrieve an existing user from a list.

*Returned Response*




[UserSearchResponseSchema](#UserSearchResponseSchema)

Success. Returns first name, last name, emails, phone number and gender of the user. Refer `UserSearchResponseSchema` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "users": [
    {
      "_id": "5e68af49cfa09bf7233022f1",
      "gender": "male",
      "active": true,
      "emails": [
        {
          "active": true,
          "primary": true,
          "verified": true,
          "email": "akashmane@gofynd.com"
        },
        {
          "active": true,
          "primary": false,
          "verified": true,
          "email": "akashmane@fynd.com"
        },
        {
          "active": true,
          "primary": false,
          "verified": true,
          "email": "akashmane@uniket.store"
        }
      ],
      "uid": "61",
      "account_type": "user",
      "first_name": "Akash",
      "last_name": "Mane",
      "phone_numbers": [
        {
          "active": true,
          "primary": true,
          "verified": true,
          "phone": "8652523958",
          "country_code": 91
        }
      ],
      "created_at": "2020-03-11T09:28:41.982Z",
      "updated_at": "2020-03-11T09:28:41.982Z"
    }
  ]
}
```
</details>









---


#### createUser
Create user




```kotlin
client.application("<APPLICATION_ID>").user.createUser(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company ID |   
| applicationId | String | yes | Application ID |  
| body | [CreateUserRequestSchema](#CreateUserRequestSchema) | yes | Request body |


Create user

*Returned Response*




[CreateUserResponseSchema](#CreateUserResponseSchema)

User create




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "user": {
    "_id": "5e68af49cfa09bf7233022f1",
    "gender": "male",
    "active": true,
    "emails": [
      {
        "active": true,
        "primary": true,
        "verified": true,
        "email": "akashmane@gofynd.com"
      },
      {
        "active": true,
        "primary": false,
        "verified": true,
        "email": "akashmane@fynd.com"
      },
      {
        "active": true,
        "primary": false,
        "verified": true,
        "email": "akashmane@uniket.store"
      }
    ],
    "uid": "61",
    "account_type": "user",
    "first_name": "Akash",
    "last_name": "Mane",
    "phone_numbers": [
      {
        "active": true,
        "primary": true,
        "verified": true,
        "phone": "8652523958",
        "country_code": 91
      }
    ],
    "meta": {},
    "created_at": "2020-03-11T09:28:41.982Z",
    "updated_at": "2020-03-11T09:28:41.982Z"
  }
}
```
</details>









---


#### updateUser
Update user




```kotlin
client.application("<APPLICATION_ID>").user.updateUser(userId: userId, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company ID |   
| applicationId | String | yes | Application ID |   
| userId | String | yes | User ID |  
| body | [UpdateUserRequestSchema](#UpdateUserRequestSchema) | yes | Request body |


Update user

*Returned Response*




[CreateUserResponseSchema](#CreateUserResponseSchema)

User update




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "user": {
    "_id": "5e68af49cfa09bf7233022f1",
    "gender": "male",
    "active": true,
    "emails": [
      {
        "active": true,
        "primary": true,
        "verified": true,
        "email": "akashmane@gofynd.com"
      },
      {
        "active": true,
        "primary": false,
        "verified": true,
        "email": "akashmane@fynd.com"
      },
      {
        "active": true,
        "primary": false,
        "verified": true,
        "email": "akashmane@uniket.store"
      }
    ],
    "uid": "61",
    "account_type": "user",
    "first_name": "Akash",
    "last_name": "Mane",
    "phone_numbers": [
      {
        "active": true,
        "primary": true,
        "verified": true,
        "phone": "8652523958",
        "country_code": 91
      }
    ],
    "meta": {},
    "created_at": "2020-03-11T09:28:41.982Z",
    "updated_at": "2020-03-11T09:28:41.982Z"
  }
}
```
</details>









---


#### createUserSession
Create user session




```kotlin
client.application("<APPLICATION_ID>").user.createUserSession(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company ID |   
| applicationId | String | yes | Application ID |  
| body | [CreateUserSessionRequestSchema](#CreateUserSessionRequestSchema) | yes | Request body |


Create user session

*Returned Response*




[CreateUserSessionResponseSchema](#CreateUserSessionResponseSchema)

Create user session




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "domain": "vinit.com",
  "max_age": 4555555,
  "secure": true,
  "http_only": true,
  "cookie": {
    "f.session": "s%3A-LrEF5FVR8jrT5DCtCHSbAy7JFyX-f9T.uXOQwzje8nOfx4ODANrLi4yNX5fW2W5kLQ2rkBdO2xE"
  }
}
```
</details>









---


#### getPlatformConfig
Get platform configurations




```kotlin
client.application("<APPLICATION_ID>").user.getPlatformConfig().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Numeric ID allotted to a business account on Fynd Platform. |   
| applicationId | String | yes | Alphanumeric ID allotted to an application created within a business account. |  



Use this API to get all the platform configurations such as mobile image, desktop image, social logins, and all other text.

*Returned Response*




[PlatformSchema](#PlatformSchema)

Success. Returns a JSON object containing the all the platform configurations. Refer `PlatformSchema` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "active": true,
  "mobile_image": "",
  "desktop_image": "",
  "social": {
    "facebook": true,
    "google": true,
    "account_kit": true
  },
  "flash_card": {
    "text": "",
    "text_color": "#FFFFFF",
    "background_color": "#EF5350"
  },
  "register": true,
  "forgot_password": true,
  "login": {
    "password": true,
    "otp": true
  },
  "skip_captcha": false,
  "display": "Fynd",
  "subtext": "Login to Fynd",
  "name": "Fynd",
  "meta": {},
  "required_fields": {
    "email": {
      "is_required": false,
      "level": "hard"
    },
    "mobile": {
      "is_required": true,
      "level": "hard"
    }
  },
  "register_required_fields": {
    "email": {
      "is_required": false,
      "level": "hard"
    },
    "mobile": {
      "is_required": true,
      "level": "hard"
    }
  },
  "skip_login": false,
  "look_and_feel": {
    "background_color": "#F5F5F5",
    "card_position": "center"
  },
  "social_tokens": {
    "google": {
      "appId": "token_123"
    },
    "facebook": {
      "appId": "token_123"
    },
    "account_kit": {
      "appId": "token_123"
    }
  },
  "_id": "5e04a5e5220bc15839ad9bc0",
  "created_at": "2019-12-26T12:21:57.878Z",
  "updated_at": "2020-08-13T14:31:09.878Z",
  "__v": 0
}
```
</details>









---


#### updatePlatformConfig
Update platform configurations




```kotlin
client.application("<APPLICATION_ID>").user.updatePlatformConfig(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Numeric ID allotted to a business account on Fynd Platform. |   
| applicationId | String | yes | Alphanumeric ID allotted to an application created within a business account. |  
| body | [PlatformSchema](#PlatformSchema) | yes | Request body |


Use this API to edit the existing platform configurations such as mobile image, desktop image, social logins, and all other text.

*Returned Response*




[PlatformSchema](#PlatformSchema)

Success. Returns a JSON object with the updated platform configurations. Refer `PlatformSchema` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "active": true,
  "mobile_image": "",
  "desktop_image": "",
  "social": {
    "facebook": true,
    "google": true,
    "account_kit": true
  },
  "flash_card": {
    "text": "",
    "text_color": "#FFFFFF",
    "background_color": "#EF5350"
  },
  "register": true,
  "forgot_password": true,
  "login": {
    "password": true,
    "otp": true
  },
  "skip_captcha": false,
  "display": "Fynd",
  "subtext": "Login to Fynd",
  "name": "Fynd",
  "meta": {},
  "required_fields": {
    "email": {
      "is_required": false,
      "level": "hard"
    },
    "mobile": {
      "is_required": true,
      "level": "hard"
    }
  },
  "register_required_fields": {
    "email": {
      "is_required": false,
      "level": "hard"
    },
    "mobile": {
      "is_required": true,
      "level": "hard"
    }
  },
  "skip_login": false,
  "look_and_feel": {
    "background_color": "#F5F5F5",
    "card_position": "center"
  },
  "social_tokens": {
    "google": {
      "appId": "token_123"
    },
    "facebook": {
      "appId": "token_123"
    },
    "account_kit": {
      "appId": "token_123"
    }
  },
  "_id": "5e04a5e5220bc15839ad9bc0",
  "created_at": "2019-12-26T12:21:57.878Z",
  "updated_at": "2020-08-13T14:31:09.878Z",
  "__v": 0
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




