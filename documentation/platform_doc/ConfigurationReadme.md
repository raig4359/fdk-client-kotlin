



## Configuration Methods
Application configuration apis
* [getBuildConfig](#getbuildconfig)
* [updateBuildConfig](#updatebuildconfig)
* [getPreviousVersions](#getpreviousversions)
* [getAppFeatures](#getappfeatures)
* [updateAppFeatures](#updateappfeatures)
* [getAppBasicDetails](#getappbasicdetails)
* [updateAppBasicDetails](#updateappbasicdetails)
* [getAppContactInfo](#getappcontactinfo)
* [updateAppContactInfo](#updateappcontactinfo)
* [getAppApiTokens](#getappapitokens)
* [updateAppApiTokens](#updateappapitokens)
* [getAppCompanies](#getappcompanies)
* [getAppStores](#getappstores)
* [getInventoryConfig](#getinventoryconfig)
* [updateInventoryConfig](#updateinventoryconfig)
* [partiallyUpdateInventoryConfig](#partiallyupdateinventoryconfig)
* [getAppCurrencyConfig](#getappcurrencyconfig)
* [updateAppCurrencyConfig](#updateappcurrencyconfig)
* [getOrderingStoresByFilter](#getorderingstoresbyfilter)
* [updateOrderingStoreConfig](#updateorderingstoreconfig)
* [getDomains](#getdomains)
* [addDomain](#adddomain)
* [removeDomainById](#removedomainbyid)
* [changeDomainType](#changedomaintype)
* [getDomainStatus](#getdomainstatus)
* [createApplication](#createapplication)
* [getApplications](#getapplications)
* [getApplicationById](#getapplicationbyid)
* [getCurrencies](#getcurrencies)
* [getDomainAvailibility](#getdomainavailibility)
* [getIntegrationById](#getintegrationbyid)
* [getAvailableOptIns](#getavailableoptins)
* [getSelectedOptIns](#getselectedoptins)
* [getIntegrationLevelConfig](#getintegrationlevelconfig)
* [getIntegrationByLevelId](#getintegrationbylevelid)
* [getLevelActiveIntegrations](#getlevelactiveintegrations)
* [getBrandsByCompany](#getbrandsbycompany)
* [getCompanyByBrands](#getcompanybybrands)
* [getStoreByBrands](#getstorebybrands)
* [getOtherSellerApplications](#getothersellerapplications)
* [getOtherSellerApplicationById](#getothersellerapplicationbyid)
* [optOutFromApplication](#optoutfromapplication)

---

## Configuration Methods


#### getBuildConfig
Get latest build config




```kotlin
client.application("<APPLICATION_ID>").configuration.getBuildConfig(platformType: platformType).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |   
| platformType | String | yes | Current platform name |  



Get latest build config

*Returned Response*




[MobileAppConfiguration](#MobileAppConfiguration)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "is_active": true,
  "_id": "5ea9b318bc23a343ab6d442f",
  "app_name": "TestUniket",
  "landing_image": {
    "aspect_ratio": "57/51",
    "secure_url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/mobile-build/pictures/free-landing/original/yKnXY1ATx-store-landing-image.png"
  },
  "splash_image": {
    "aspect_ratio": "1/1",
    "secure_url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/mobile-build/pictures/free-splash/original/s6d7oYfY6-store-splash-image.png"
  },
  "application": "000000000000000000000004",
  "platform_type": "android",
  "created_at": "2020-04-29T17:02:16.976Z",
  "modified_at": "2021-02-23T17:10:26.872Z",
  "__v": 0,
  "package_name": "com.fynd.store.x000000000000000000000004"
}
```
</details>









---


#### updateBuildConfig
Update build config for next build




```kotlin
client.application("<APPLICATION_ID>").configuration.updateBuildConfig(platformType: platformType, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |   
| platformType | String | yes | Current platform name |  
| body | [MobileAppConfigRequest](#MobileAppConfigRequest) | yes | Request body |


Update build config for next build

*Returned Response*




[MobileAppConfiguration](#MobileAppConfiguration)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "is_active": true,
  "_id": "5ea9b318bc23a343ab6d442f",
  "app_name": "TestUniket",
  "landing_image": {
    "aspect_ratio": "57/51",
    "secure_url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/mobile-build/pictures/free-landing/original/yKnXY1ATx-store-landing-image.png"
  },
  "splash_image": {
    "aspect_ratio": "1/1",
    "secure_url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/mobile-build/pictures/free-splash/original/s6d7oYfY6-store-splash-image.png"
  },
  "application": "000000000000000000000004",
  "platform_type": "android",
  "created_at": "2020-04-29T17:02:16.976Z",
  "modified_at": "2021-02-23T17:10:26.872Z",
  "__v": 0,
  "package_name": "com.fynd.store.x000000000000000000000004"
}
```
</details>









---


#### getPreviousVersions
Get previous build versions




```kotlin
client.application("<APPLICATION_ID>").configuration.getPreviousVersions(platformType: platformType).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |   
| platformType | String | yes | Current platform name |  



Get previous build versions

*Returned Response*




[BuildVersionHistory](#BuildVersionHistory)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "versions": [
    {
      "_id": "6035376ab937c5f7c5462888",
      "application": "000000000000000000000004",
      "platform_type": "android",
      "build_status": "pending",
      "version_name": "0.5.6",
      "version_code": 1,
      "created_at": "2021-02-23T17:12:10.977Z",
      "modified_at": "2021-02-23T17:12:10.977Z",
      "__v": 0
    }
  ],
  "latest_available_version_name": "0.5.7"
}
```
</details>









---


#### getAppFeatures
Get features of application




```kotlin
client.application("<APPLICATION_ID>").configuration.getAppFeatures().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  



Get features of application

*Returned Response*




[AppFeatureResponse](#AppFeatureResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "feature": {
    "product_detail": {
      "similar": [
        "basic",
        "visual",
        "brand",
        "category",
        "seller",
        "price",
        "specs"
      ],
      "seller_selection": true,
      "update_product_meta": true,
      "request_product": true
    },
    "landing_page": {
      "launch_page": {
        "page_type": "home",
        "params": null,
        "query": null
      },
      "continue_as_guest": true,
      "login_btn_text": "Click here to sign-in",
      "show_domain_textbox": true,
      "show_register_btn": true
    },
    "registration_page": {
      "ask_store_address": false
    },
    "home_page": {
      "order_processing": true
    },
    "common": {
      "communication_optin_dialog": {
        "visibility": true
      },
      "deployment_store_selection": {
        "enabled": true,
        "type": "hard"
      },
      "listing_price": {
        "value": "min",
        "sort": "min"
      },
      "currency": {
        "value": [
          "INR"
        ],
        "type": "explicit",
        "default_currency": "INR"
      },
      "revenue_engine": {
        "enabled": false
      },
      "feedback": {
        "enabled": true
      },
      "compare_products": {
        "enabled": true
      },
      "reward_points": {
        "credit": {
          "enabled": true
        },
        "debit": {
          "enabled": true,
          "auto_apply": false,
          "strategy_channel": "REWARDS"
        }
      }
    },
    "cart": {
      "gst_input": true,
      "staff_selection": true,
      "placing_for_customer": true,
      "google_map": true,
      "revenue_engine_coupon": false
    },
    "qr": {
      "application": true,
      "products": true,
      "collections": true
    },
    "pcr": {
      "staff_selection": true
    },
    "order": {
      "buy_again": true
    },
    "_id": "5e57643c986e4119c973df7d",
    "app": "000000000000000000000004",
    "created_at": "2020-02-27T06:39:56.088Z",
    "modified_at": "2021-02-02T11:04:14.289Z",
    "__v": 1
  }
}
```
</details>









---


#### updateAppFeatures
Update features of application




```kotlin
client.application("<APPLICATION_ID>").configuration.updateAppFeatures(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  
| body | [AppFeatureRequest](#AppFeatureRequest) | yes | Request body |


Update features of application

*Returned Response*




[AppFeature](#AppFeature)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "product_detail": {
    "similar": [
      "basic",
      "visual",
      "brand",
      "category",
      "seller",
      "price",
      "specs"
    ],
    "seller_selection": true,
    "update_product_meta": true,
    "request_product": true
  },
  "landing_page": {
    "launch_page": {
      "page_type": "home",
      "params": null,
      "query": null
    },
    "continue_as_guest": true,
    "login_btn_text": "Click here to sign-in",
    "show_domain_textbox": true,
    "show_register_btn": true
  },
  "registration_page": {
    "ask_store_address": false
  },
  "home_page": {
    "order_processing": true
  },
  "common": {
    "communication_optin_dialog": {
      "visibility": true
    },
    "deployment_store_selection": {
      "enabled": true,
      "type": "hard"
    },
    "listing_price": {
      "value": "min",
      "sort": "min"
    },
    "currency": {
      "value": [
        "INR"
      ],
      "type": "explicit",
      "default_currency": "INR"
    },
    "revenue_engine": {
      "enabled": false
    },
    "feedback": {
      "enabled": true
    },
    "compare_products": {
      "enabled": true
    }
  },
  "cart": {
    "gst_input": true,
    "staff_selection": true,
    "placing_for_customer": true,
    "google_map": true,
    "revenue_engine_coupon": false
  },
  "qr": {
    "application": true,
    "products": true,
    "collections": true
  },
  "pcr": {
    "staff_selection": true
  },
  "order": {
    "buy_again": true
  },
  "_id": "5e57643c986e4119c973df7d",
  "app": "000000000000000000000004",
  "created_at": "2020-02-27T06:39:56.088Z",
  "modified_at": "2021-03-09T15:40:29.188Z",
  "__v": 1
}
```
</details>









---


#### getAppBasicDetails
Get basic application details




```kotlin
client.application("<APPLICATION_ID>").configuration.getAppBasicDetails().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  



Get basic application details like name

*Returned Response*




[ApplicationDetail](#ApplicationDetail)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "name": "Uniket B2B",
  "description": "Uniket B2B - India's Fastest Growing Retail Store - Aapki Badhti Dukaan",
  "logo": {
    "secure_url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/application/pictures/free-logo/original/oEf3SQjda-Uniket-B2B.png"
  },
  "mobile_logo": {
    "secure_url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/application/pictures/free-logo/original/oEf3SQjda-Uniket-B2B.png"
  },
  "favicon": {
    "secure_url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/application/pictures/favicon/original/y3h6SSlY5-Uniket-B2B.png"
  },
  "banner": {
    "secure_url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/application/pictures/landscape-banner/original/uSwlNpygq-Uniket-B2B.png"
  },
  "domain": {
    "verified": true,
    "is_primary": true,
    "is_shortlink": false,
    "_id": "5eb1177748312a3bd55d0f1e",
    "name": "uniket.hostx0.de"
  },
  "domains": [
    {
      "verified": true,
      "is_primary": true,
      "is_shortlink": false,
      "_id": "5eb1177748312a3bd55d0f1e",
      "name": "uniket.hostx0.de"
    },
    {
      "verified": true,
      "is_primary": false,
      "is_shortlink": true,
      "_id": "5f0858c5f86e00cd42dccc8d",
      "name": "jd.hostx0.de"
    }
  ],
  "company_id": 1,
  "_id": "000000000000000000000004"
}
```
</details>









---


#### updateAppBasicDetails
Add or update application's basic details




```kotlin
client.application("<APPLICATION_ID>").configuration.updateAppBasicDetails(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  
| body | [ApplicationDetail](#ApplicationDetail) | yes | Request body |


Add or update application's basic details

*Returned Response*




[ApplicationDetail](#ApplicationDetail)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "name": "Uniket B2B",
  "description": "Uniket B2B - India's Fastest Growing Retail Store - Aapki Badhti Dukaan",
  "logo": {
    "secure_url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/application/pictures/free-logo/original/oEf3SQjda-Uniket-B2B.png"
  },
  "mobile_logo": {
    "secure_url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/application/pictures/free-logo/original/oEf3SQjda-Uniket-B2B.png"
  },
  "favicon": {
    "secure_url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/application/pictures/favicon/original/y3h6SSlY5-Uniket-B2B.png"
  },
  "banner": {
    "secure_url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/application/pictures/landscape-banner/original/uSwlNpygq-Uniket-B2B.png"
  },
  "domain": {
    "verified": true,
    "is_primary": true,
    "is_shortlink": false,
    "_id": "5eb1177748312a3bd55d0f1e",
    "name": "uniket.hostx0.de"
  },
  "domains": [
    {
      "verified": true,
      "is_primary": true,
      "is_shortlink": false,
      "_id": "5eb1177748312a3bd55d0f1e",
      "name": "uniket.hostx0.de"
    },
    {
      "verified": true,
      "is_primary": false,
      "is_shortlink": true,
      "_id": "5f0858c5f86e00cd42dccc8d",
      "name": "jd.hostx0.de"
    }
  ]
}
```
</details>









---


#### getAppContactInfo
Get application information




```kotlin
client.application("<APPLICATION_ID>").configuration.getAppContactInfo().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  



Get Application Current Information. This includes information about social links, address and contact information of company/seller/brand of the application.

*Returned Response*




[ApplicationInformation](#ApplicationInformation)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "value": {
    "address": {
      "loc": null,
      "address_line": [
        "Warehouse 5, Near Industrial Complex",
        "2nd Lane, Andheri"
      ],
      "phone": [
        {
          "code": "+91",
          "number": "9988776654"
        }
      ],
      "city": "Mumbai , Maharashtra , India",
      "country": "India",
      "pincode": 400059
    },
    "support": {
      "phone": [],
      "email": [],
      "timing": "9 AM to 9 PM"
    },
    "social_links": {
      "facebook": {
        "title": "Facebook",
        "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/hQAbAKdvHK-facebookfooteraopcjq.svg",
        "link": ""
      },
      "instagram": {
        "title": "Instagram",
        "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/UZYsGWOqXp-instagramfooterl3utrr.svg",
        "link": ""
      },
      "twitter": {
        "title": "Twitter",
        "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/oT2hW-BJjq-twitterfooternajsyr.svg",
        "link": ""
      },
      "pinterest": {
        "title": "Pinterest",
        "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/v0erlcMk8p-pinterestfooternzmq4b.svg",
        "link": ""
      },
      "google_plus": {
        "title": "Google+",
        "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/lw3Y5S58h4-googleplusysukr1.png",
        "link": ""
      },
      "youtube": {
        "title": "Youtube",
        "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/EYV03PDST_-youtubefootermqhcr7.svg",
        "link": ""
      },
      "linked_in": {
        "title": "LinkedIn",
        "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/qa7gx_bW9O-linkedinfooterrcr0yq.svg",
        "link": ""
      },
      "vimeo": {
        "title": "Vimeo",
        "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/Ttc80b3U78-vimeofooternho4br.svg",
        "link": ""
      },
      "blog_link": {
        "title": "Blog",
        "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/LKpxTk1I3s-mediumfooterdtvrva.svg",
        "link": ""
      }
    },
    "links": [
      {
        "title": "Shipping",
        "link": "www.uniket.store/shipping-details"
      },
      {
        "title": "Returns",
        "link": "www.uniket.store/policy/return-policy"
      },
      {
        "title": "Privacy",
        "link": "www.uniket.store/policy/privacy-policy"
      },
      {
        "title": "Terms",
        "link": "www.uniket.store/policy/terms-conditions"
      }
    ],
    "copyright_text": "#MadeInIndia © 2020 Shopsense Retail Technologies",
    "_id": "5e6627bd0732616083e83750",
    "business_highlights": [
      {
        "_id": "5fc901611dfba6c2e87d1ca9",
        "title": "100% Genuine Products",
        "icon": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/business-highlights/pictures/square-logo/original/bVlx43F2a-H6pvZ9tzp-business-logo-icon.png",
        "sub_title": "Directly from brands"
      },
      {
        "_id": "5fc901611dfba64ce57d1caa",
        "title": "Credit Facility Available",
        "icon": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/business-highlights/pictures/square-logo/original/VMnltS1m3-QuUnEjOsA-business-logo-icon.png",
        "sub_title": "Free 30 Days Credit"
      },
      {
        "_id": "5fc901611dfba64b2e7d1cab",
        "title": "Assured Returns",
        "icon": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/business-highlights/pictures/square-logo/original/cTHzgHJXK-sROtLMalN-business-logo-icon.png",
        "sub_title": "For all damaged/wrong items"
      }
    ],
    "application": "000000000000000000000004",
    "created_at": "2020-03-09T11:25:49.921Z",
    "modified_at": "2020-12-03T15:16:49.087Z",
    "__v": 99
  }
}
```
</details>









---


#### updateAppContactInfo
Get application information




```kotlin
client.application("<APPLICATION_ID>").configuration.updateAppContactInfo(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  
| body | [ApplicationInformation](#ApplicationInformation) | yes | Request body |


Save Application Current Information. This includes information about social links, address and contact information of an application.

*Returned Response*




[ApplicationInformation](#ApplicationInformation)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "_id": "5e6627bd0732616083e83750",
  "address": {
    "address_line": [
      "Warehouse 5, Near Industrial Complex",
      "2nd Lane, Andheri"
    ],
    "phone": [
      {
        "code": "+91",
        "number": "9988776654"
      }
    ],
    "city": "Mumbai , Maharashtra , India",
    "country": "India",
    "pincode": 400059,
    "loc": null
  },
  "social_links": {
    "facebook": {
      "title": "Facebook",
      "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/hQAbAKdvHK-facebookfooteraopcjq.svg",
      "link": ""
    },
    "instagram": {
      "title": "Instagram",
      "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/UZYsGWOqXp-instagramfooterl3utrr.svg",
      "link": ""
    },
    "twitter": {
      "title": "Twitter",
      "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/oT2hW-BJjq-twitterfooternajsyr.svg",
      "link": ""
    },
    "pinterest": {
      "title": "Pinterest",
      "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/v0erlcMk8p-pinterestfooternzmq4b.svg",
      "link": ""
    },
    "google_plus": {
      "title": "Google+",
      "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/lw3Y5S58h4-googleplusysukr1.png",
      "link": ""
    },
    "youtube": {
      "title": "Youtube",
      "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/EYV03PDST_-youtubefootermqhcr7.svg",
      "link": ""
    },
    "linked_in": {
      "title": "LinkedIn",
      "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/qa7gx_bW9O-linkedinfooterrcr0yq.svg",
      "link": ""
    },
    "blog_link": {
      "title": "Blog",
      "icon": "https://hdn-1.fynd.com/system/svg/social-media/icon/original/LKpxTk1I3s-mediumfooterdtvrva.svg",
      "link": ""
    }
  },
  "links": [
    {
      "title": "Shipping",
      "link": "www.uniket.store/shipping-details"
    },
    {
      "title": "Returns",
      "link": "www.uniket.store/policy/return-policy"
    },
    {
      "title": "Privacy",
      "link": "www.uniket.store/policy/privacy-policy"
    },
    {
      "title": "Terms",
      "link": "www.uniket.store/policy/terms-conditions"
    }
  ],
  "copyright_text": "#MadeInIndia © 2020 Shopsense Retail Technologies",
  "support": {
    "timing": "9 AM to 9 PM",
    "phone": [],
    "email": []
  },
  "business_highlights": [
    {
      "_id": "60479413a32f774d754b00ef",
      "title": "100% Genuine Products",
      "icon": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/business-highlights/pictures/square-logo/original/bVlx43F2a-H6pvZ9tzp-business-logo-icon.png",
      "sub_title": "Directly from brands"
    },
    {
      "_id": "60479413a32f7717df4b00f0",
      "title": "Credit Facility Available",
      "icon": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/business-highlights/pictures/square-logo/original/VMnltS1m3-QuUnEjOsA-business-logo-icon.png",
      "sub_title": "Free 30 Days Credit"
    },
    {
      "_id": "60479413a32f77e70b4b00f1",
      "title": "Assured Returns",
      "icon": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000004/business-highlights/pictures/square-logo/original/cTHzgHJXK-sROtLMalN-business-logo-icon.png",
      "sub_title": "For all damaged/wrong items"
    }
  ],
  "application": "000000000000000000000004",
  "created_at": "2020-03-09T11:25:49.921Z",
  "modified_at": "2021-03-09T15:28:19.598Z",
  "__v": 101
}
```
</details>









---


#### getAppApiTokens
Get social tokens




```kotlin
client.application("<APPLICATION_ID>").configuration.getAppApiTokens().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  



Get social tokens.

*Returned Response*




[TokenResponse](#TokenResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "tokens": {
    "firebase": {
      "credentials": {
        "ios": {
          "application_id": "test",
          "api_key": "test"
        },
        "android": {
          "application_id": "test",
          "api_key": "test"
        },
        "project_id": "uniket-d8cdc",
        "gcm_sender_id": "test",
        "application_id": "test",
        "api_key": "test"
      },
      "enabled": true
    },
    "moengage": {
      "credentials": {
        "app_id": "test"
      },
      "enabled": true
    },
    "segment": {
      "credentials": {
        "write_key": "test"
      },
      "enabled": true
    },
    "gtm": {
      "credentials": {
        "api_key": "test"
      },
      "enabled": false
    },
    "freshchat": {
      "credentials": {
        "app_id": "123456",
        "app_key": "123456789",
        "web_token": ""
      },
      "enabled": false
    },
    "safetynet": {
      "credentials": {
        "api_key": "test"
      },
      "enabled": true
    },
    "fynd_rewards": {
      "credentials": {
        "public_key": "test"
      }
    },
    "auth": {
      "google": {
        "appId": "test"
      },
      "facebook": {
        "appId": "test"
      },
      "accountkit": {
        "appId": ""
      }
    },
    "google_map": {
      "credentials": {
        "api_key": "test"
      }
    }
  },
  "_id": "5e66282a073261060ee83751",
  "application": "000000000000000000000004",
  "created_at": "2020-03-09T11:27:38.894Z",
  "modified_at": "2020-12-24T05:39:17.054Z",
  "__v": 0
}
```
</details>









---


#### updateAppApiTokens
Add social tokens




```kotlin
client.application("<APPLICATION_ID>").configuration.updateAppApiTokens(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  
| body | [TokenResponse](#TokenResponse) | yes | Request body |


Add social tokens.

*Returned Response*




[TokenResponse](#TokenResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "tokens": {
    "firebase": {
      "credentials": {
        "ios": {
          "application_id": "test",
          "api_key": "test"
        },
        "android": {
          "application_id": "test",
          "api_key": "test"
        },
        "project_id": "uniket-d8cdc",
        "gcm_sender_id": "test",
        "application_id": "test",
        "api_key": "test"
      },
      "enabled": true
    },
    "moengage": {
      "credentials": {
        "app_id": "test"
      },
      "enabled": true
    },
    "segment": {
      "credentials": {
        "write_key": "test"
      },
      "enabled": true
    },
    "gtm": {
      "credentials": {
        "api_key": "1234567890"
      },
      "enabled": false
    },
    "freshchat": {
      "credentials": {
        "app_id": "123456",
        "app_key": "123456789",
        "web_token": ""
      },
      "enabled": false
    },
    "safetynet": {
      "credentials": {
        "api_key": "test"
      },
      "enabled": true
    },
    "fynd_rewards": {
      "credentials": {
        "public_key": "test"
      }
    },
    "auth": {
      "google": {
        "appId": "test"
      },
      "facebook": {
        "appId": "test"
      },
      "accountkit": {
        "appId": ""
      }
    },
    "google_map": {
      "credentials": {
        "api_key": "test"
      }
    }
  },
  "_id": "5e66282a073261060ee83751",
  "application": "000000000000000000000004",
  "created_at": "2020-03-09T11:27:38.894Z",
  "modified_at": "2020-12-24T05:39:17.054Z",
  "__v": 0
}
```
</details>









---


#### getAppCompanies
Application inventory enabled companies




```kotlin
client.application("<APPLICATION_ID>").configuration.getAppCompanies(pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |  



Application inventory enabled companies.

*Returned Response*




[CompaniesResponse](#CompaniesResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "uid": 108,
      "name": "Sample2 Company",
      "company_type": "mbo"
    },
    {
      "uid": 13,
      "name": "Isabel Mazanec",
      "company_type": "franchisee"
    },
    {
      "uid": 7,
      "name": "Zack Burgdorf",
      "company_type": "distributor"
    }
  ],
  "page": {
    "type": "number",
    "size": 200,
    "current": 1,
    "has_next": false,
    "item_total": 3
  }
}
```
</details>









---


#### getAppStores
Application inventory enabled stores




```kotlin
client.application("<APPLICATION_ID>").configuration.getAppStores(pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |  



Application inventory enabled stores.

*Returned Response*




[StoresResponse](#StoresResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "_id": "5ec2c0b168fc2800017112f5",
      "uid": 1,
      "name": "RRL01",
      "display_name": "RRL01",
      "store_type": "warehouse",
      "store_code": "WH_8513",
      "company_id": 1
    },
    {
      "_id": "5ec3b09a68fc28000171137c",
      "modified_on": "2020-06-30T10:02:41.208Z",
      "uid": 10,
      "name": "Saran Ledonne",
      "display_name": "",
      "store_type": "high_street",
      "store_code": "af6198fe-2c23-4441-bbf4-e694c96e255c",
      "company_id": 1
    },
    {
      "_id": "5f099b2c931b1c0001e7ccb2",
      "display_name": "cbs 2",
      "store_code": "HS-c9bac",
      "name": "cbs 2",
      "company_id": 80,
      "store_type": "high_street",
      "uid": 11014
    }
  ],
  "page": {
    "type": "number",
    "size": 200,
    "current": 1,
    "has_next": true,
    "item_total": 3
  }
}
```
</details>









---


#### getInventoryConfig
Get application configuration




```kotlin
client.application("<APPLICATION_ID>").configuration.getInventoryConfig().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  



Get application configuration for various features and data

*Returned Response*




[ApplicationInventory](#ApplicationInventory)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "inventory": {
    "brand": {
      "criteria": "all",
      "brands": []
    },
    "store": {
      "criteria": "filter",
      "stores": [],
      "rules": [
        {
          "companies": [
            1,
            3,
            4
          ],
          "brands": []
        }
      ]
    },
    "category": {
      "criteria": "all",
      "categories": []
    },
    "price": {
      "min": 1,
      "max": 10000
    },
    "discount": {
      "min": 0,
      "max": 100
    },
    "out_of_stock": true,
    "franchise_enabled": true,
    "exclude_category": [],
    "image": [
      "standard",
      "substandard",
      "default"
    ],
    "company_store": []
  },
  "authentication": {
    "required": true,
    "provider": "fynd"
  },
  "article_assignment": {
    "rules": {
      "store_priority": {
        "enabled": false,
        "storetype_order": []
      }
    },
    "post_order_reassignment": true
  },
  "reward_points": {
    "credit": {
      "enabled": true
    },
    "debit": {
      "enabled": true,
      "auto_apply": false,
      "strategy_channel": "rewards"
    }
  },
  "cart": {
    "delivery_charges": {
      "enabled": true,
      "charges": [
        {
          "threshold": 1000,
          "charges": 49
        },
        {
          "threshold": 200000,
          "charges": 79
        }
      ]
    },
    "enabled": true,
    "max_cart_items": 0,
    "min_cart_value": 120,
    "bulk_coupons": true
  },
  "payment": {
    "callback_url": {
      "app": "",
      "web": ""
    },
    "methods": {
      "pl": {
        "enabled": true
      },
      "card": {
        "enabled": true
      },
      "nb": {
        "enabled": true
      },
      "wl": {
        "enabled": true
      },
      "ps": {
        "enabled": true
      },
      "upi": {
        "enabled": true
      },
      "qr": {
        "enabled": true
      },
      "cod": {
        "enabled": true
      },
      "pp": {
        "enabled": true
      },
      "jp": {
        "enabled": false
      },
      "pac": {
        "enabled": false
      },
      "fc": {
        "enabled": false
      },
      "jiopp": {
        "enabled": false
      },
      "stripepg": {
        "enabled": true
      },
      "juspaypg": {
        "enabled": false
      },
      "payubizpg": {
        "enabled": true
      },
      "payumoneypg": {
        "enabled": true
      },
      "rupifipg": {
        "enabled": false
      },
      "simpl": {
        "enabled": true
      }
    },
    "payment_selection_lock": {
      "enabled": false,
      "default_options": "",
      "payment_identifier": ""
    },
    "mode_of_payment": "uniket_b2b",
    "source": "uniket",
    "enabled": true,
    "cod_amount_limit": 100000,
    "cod_charges": 1500
  },
  "order": {
    "enabled": true,
    "force_reassignment": false
  },
  "logistics": {
    "logistics_by_seller": false,
    "serviceability_check": true,
    "same_day_delivery": true,
    "dp_assignment": true
  },
  "business": "retail",
  "comms_enabled": true,
  "platforms": [
    "uniket_wholesale"
  ],
  "_id": "5e04c76b8dd8c003577fdd0a",
  "loyalty_points": {
    "enabled": true,
    "auto_apply": false
  },
  "app": "000000000000000000000004",
  "created_at": "2019-12-26t14:44:59.835z",
  "modified_at": "2021-03-09t15:40:29.208z",
  "__v": 3,
  "modified_by": "5e199eed98cfe16dc61385de"
}
```
</details>









---


#### updateInventoryConfig
Update application configuration




```kotlin
client.application("<APPLICATION_ID>").configuration.updateInventoryConfig(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  
| body | [ApplicationInventory](#ApplicationInventory) | yes | Request body |


Update application configuration for various features and data

*Returned Response*




[ApplicationInventory](#ApplicationInventory)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "inventory": {
    "brand": {
      "criteria": "all",
      "brands": []
    },
    "store": {
      "criteria": "filter",
      "stores": [],
      "rules": [
        {
          "companies": [
            1,
            3,
            4
          ],
          "brands": []
        }
      ]
    },
    "category": {
      "criteria": "all",
      "categories": []
    },
    "price": {
      "min": 1,
      "max": 10000
    },
    "discount": {
      "min": 0,
      "max": 100
    },
    "out_of_stock": true,
    "franchise_enabled": true,
    "exclude_category": [],
    "image": [
      "standard",
      "substandard",
      "default"
    ],
    "company_store": []
  },
  "authentication": {
    "required": true,
    "provider": "fynd"
  },
  "article_assignment": {
    "rules": {
      "store_priority": {
        "enabled": false,
        "storetype_order": []
      }
    },
    "post_order_reassignment": true
  },
  "reward_points": {
    "credit": {
      "enabled": true
    },
    "debit": {
      "enabled": true,
      "auto_apply": false,
      "strategy_channel": "REWARDS"
    }
  },
  "cart": {
    "delivery_charges": {
      "enabled": true,
      "charges": [
        {
          "threshold": 1000,
          "charges": 49
        },
        {
          "threshold": 200000,
          "charges": 79
        }
      ]
    },
    "enabled": true,
    "max_cart_items": 0,
    "min_cart_value": 120,
    "bulk_coupons": true
  },
  "payment": {
    "callback_url": {
      "app": "",
      "web": ""
    },
    "methods": {
      "PL": {
        "enabled": true
      },
      "CARD": {
        "enabled": true
      },
      "NB": {
        "enabled": true
      },
      "WL": {
        "enabled": true
      },
      "PS": {
        "enabled": true
      },
      "UPI": {
        "enabled": true
      },
      "QR": {
        "enabled": true
      },
      "COD": {
        "enabled": true
      },
      "PP": {
        "enabled": true
      },
      "JP": {
        "enabled": false
      },
      "PAC": {
        "enabled": false
      },
      "FC": {
        "enabled": false
      },
      "JIOPP": {
        "enabled": false
      },
      "STRIPEPG": {
        "enabled": true
      },
      "JUSPAYPG": {
        "enabled": false
      },
      "PAYUBIZPG": {
        "enabled": true
      },
      "PAYUMONEYPG": {
        "enabled": true
      },
      "RUPIFIPG": {
        "enabled": false
      },
      "SIMPL": {
        "enabled": true
      }
    },
    "payment_selection_lock": {
      "enabled": false,
      "default_options": "",
      "payment_identifier": ""
    },
    "mode_of_payment": "UNIKET_B2B",
    "source": "UNIKET",
    "enabled": true,
    "cod_amount_limit": 100000,
    "cod_charges": 1500
  },
  "order": {
    "enabled": true,
    "force_reassignment": false
  },
  "logistics": {
    "logistics_by_seller": false,
    "serviceability_check": true,
    "same_day_delivery": true,
    "dp_assignment": true
  },
  "business": "retail",
  "comms_enabled": true,
  "platforms": [
    "uniket_wholesale"
  ],
  "_id": "5e04c76b8dd8c003577fdd0a",
  "loyalty_points": {
    "enabled": true,
    "auto_apply": false
  },
  "app": "000000000000000000000004",
  "created_at": "2019-12-26T14:44:59.835Z",
  "modified_at": "2021-03-09T15:40:29.208Z",
  "__v": 3,
  "modified_by": "5e199eed98cfe16dc61385de"
}
```
</details>









---


#### partiallyUpdateInventoryConfig
Partially update application configuration




```kotlin
client.application("<APPLICATION_ID>").configuration.partiallyUpdateInventoryConfig(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  
| body | [AppInventoryPartialUpdate](#AppInventoryPartialUpdate) | yes | Request body |


Partially update application configuration for various features and data

*Returned Response*




[ApplicationInventory](#ApplicationInventory)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "inventory": {
    "brand": {
      "criteria": "all",
      "brands": []
    },
    "store": {
      "criteria": "filter",
      "stores": [],
      "rules": [
        {
          "companies": [
            1,
            3,
            4
          ],
          "brands": []
        }
      ]
    },
    "category": {
      "criteria": "all",
      "categories": []
    },
    "price": {
      "min": 1,
      "max": 10000
    },
    "discount": {
      "min": 0,
      "max": 100
    },
    "out_of_stock": true,
    "franchise_enabled": true,
    "exclude_category": [],
    "image": [
      "standard",
      "substandard",
      "default"
    ],
    "company_store": []
  },
  "authentication": {
    "required": true,
    "provider": "fynd"
  },
  "article_assignment": {
    "rules": {
      "store_priority": {
        "enabled": false,
        "storetype_order": []
      }
    },
    "post_order_reassignment": true
  },
  "reward_points": {
    "credit": {
      "enabled": true
    },
    "debit": {
      "enabled": true,
      "auto_apply": false,
      "strategy_channel": "REWARDS"
    }
  },
  "cart": {
    "delivery_charges": {
      "enabled": true,
      "charges": [
        {
          "threshold": 1000,
          "charges": 49
        },
        {
          "threshold": 200000,
          "charges": 79
        }
      ]
    },
    "enabled": true,
    "max_cart_items": 0,
    "min_cart_value": 120,
    "bulk_coupons": true
  },
  "payment": {
    "callback_url": {
      "app": "",
      "web": ""
    },
    "methods": {
      "PL": {
        "enabled": true
      },
      "CARD": {
        "enabled": true
      },
      "NB": {
        "enabled": true
      },
      "WL": {
        "enabled": true
      },
      "PS": {
        "enabled": true
      },
      "UPI": {
        "enabled": true
      },
      "QR": {
        "enabled": true
      },
      "COD": {
        "enabled": true
      },
      "PP": {
        "enabled": true
      },
      "JP": {
        "enabled": false
      },
      "PAC": {
        "enabled": false
      },
      "FC": {
        "enabled": false
      },
      "JIOPP": {
        "enabled": false
      },
      "STRIPEPG": {
        "enabled": true
      },
      "JUSPAYPG": {
        "enabled": false
      },
      "PAYUBIZPG": {
        "enabled": true
      },
      "PAYUMONEYPG": {
        "enabled": true
      },
      "RUPIFIPG": {
        "enabled": false
      },
      "SIMPL": {
        "enabled": true
      }
    },
    "payment_selection_lock": {
      "enabled": false,
      "default_options": "",
      "payment_identifier": ""
    },
    "mode_of_payment": "UNIKET_B2B",
    "source": "UNIKET",
    "enabled": true,
    "cod_amount_limit": 100000,
    "cod_charges": 1500
  },
  "order": {
    "enabled": true,
    "force_reassignment": false
  },
  "logistics": {
    "logistics_by_seller": false,
    "serviceability_check": true,
    "same_day_delivery": true,
    "dp_assignment": true
  },
  "business": "retail",
  "comms_enabled": true,
  "platforms": [
    "uniket_wholesale"
  ],
  "_id": "5e04c76b8dd8c003577fdd0a",
  "loyalty_points": {
    "enabled": true,
    "auto_apply": false
  },
  "app": "000000000000000000000004",
  "created_at": "2019-12-26T14:44:59.835Z",
  "modified_at": "2021-03-09T15:40:29.208Z",
  "__v": 3,
  "modified_by": "5e199eed98cfe16dc61385de"
}
```
</details>









---


#### getAppCurrencyConfig
Get application enabled currency list




```kotlin
client.application("<APPLICATION_ID>").configuration.getAppCurrencyConfig().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  



Get application enabled currency list

*Returned Response*




[AppSupportedCurrency](#AppSupportedCurrency)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "_id": "5ec7a85965c3893857538d93",
  "supported_currency": [
    "5ec75d11f7bfb5a7d38f3524",
    "5ec75d11f7bfb54d798f3516",
    "5ec75d11f7bfb553b88f355f",
    "5ec75d11f7bfb559d08f34d5",
    "5ec75d11f7bfb5d1e98f34da"
  ],
  "application": "000000000000000000000004",
  "default_currency": {
    "ref": "5ec75d11f7bfb54d798f3516",
    "code": "USD"
  },
  "created_at": "2020-05-22T10:24:25.984Z",
  "modified_at": "2021-03-09T10:47:32.664Z"
}
```
</details>









---


#### updateAppCurrencyConfig
Add initial application supported currency




```kotlin
client.application("<APPLICATION_ID>").configuration.updateAppCurrencyConfig(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  
| body | [AppSupportedCurrency](#AppSupportedCurrency) | yes | Request body |


Add initial application supported currency for various features and data. Default INR will be enabled.

*Returned Response*




[AppSupportedCurrency](#AppSupportedCurrency)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "_id": "5ec7a85965c3893857538d93",
  "supported_currency": [
    "5ec75d11f7bfb5a7d38f3524",
    "5ec75d11f7bfb54d798f3516",
    "5ec75d11f7bfb553b88f355f",
    "5ec75d11f7bfb559d08f34d5",
    "5ec75d11f7bfb5d1e98f34da"
  ],
  "application": "000000000000000000000004",
  "default_currency": {
    "ref": "5ec75d11f7bfb54d798f3516",
    "code": "USD"
  },
  "created_at": "2020-05-22T10:24:25.984Z",
  "modified_at": "2021-03-09T10:47:32.664Z"
}
```
</details>









---


#### getOrderingStoresByFilter
Get ordering store by filter




```kotlin
client.application("<APPLICATION_ID>").configuration.getOrderingStoresByFilter(pageNo: pageNo, pageSize: pageSize, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |  
| body | [FilterOrderingStoreRequest](#FilterOrderingStoreRequest) | yes | Request body |


Get ordering store by filter

*Returned Response*




[OrderingStores](#OrderingStores)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {
    "type": "number",
    "size": 10,
    "current": 1,
    "has_next": true,
    "item_total": 583
  },
  "items": [
    {
      "address": {
        "state": "MAHARASHTRA",
        "address1": "SAGAR TECH PLAZA, SAKINAKA",
        "lat_long": {
          "type": "Point",
          "coordinates": [
            1,
            1
          ]
        },
        "pincode": 400070,
        "country": "INDIA",
        "city": "MUMBAI"
      },
      "_id": "5f586563f509dd000145c02d",
      "store_type": "high_street",
      "uid": 11016,
      "store_code": "HS-0c532",
      "display_name": " Brand Company Store 11",
      "name": " Brand Company Store 11",
      "pincode": 400070,
      "code": "HS-0c532"
    },
    {
      "address": {
        "state": "MAHARASHTRA",
        "address1": "UNNAMED ROAD, VASAI EAST SALT PLANT",
        "lat_long": {
          "type": "Point",
          "coordinates": [
            72.84293219999999,
            19.3805675
          ]
        },
        "address2": "VASAI EAST SALT PLANT, VASAI EAST, ",
        "pincode": 401208,
        "country": "INDIA",
        "city": "VIRAR",
        "landmark": ""
      },
      "_id": "5f585934f509dd000145c025",
      "store_type": "high_street",
      "uid": 11567,
      "store_code": "123456",
      "display_name": "2nd Store",
      "name": "2nd Store",
      "pincode": 401208,
      "code": "123456"
    },
    {
      "address": {
        "state": "GUJARAT",
        "address1": "32, AANAND SHOPPING CENTRE ",
        "lat_long": {
          "type": "Point",
          "coordinates": [
            1,
            1
          ]
        },
        "pincode": 380001,
        "country": "INDIA",
        "city": "AHMEDABAD"
      },
      "_id": "5f587b5ef509dd000145c02f",
      "store_type": "high_street",
      "uid": 11568,
      "store_code": "12345",
      "display_name": "3rd ",
      "name": "3rd ",
      "pincode": 380001,
      "code": "12345"
    }
  ]
}
```
</details>









---


#### updateOrderingStoreConfig
Add/Update ordering store config




```kotlin
client.application("<APPLICATION_ID>").configuration.updateOrderingStoreConfig(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  
| body | [OrderingStoreConfig](#OrderingStoreConfig) | yes | Request body |


Add/Update ordering store config.

*Returned Response*




[DeploymentMeta](#DeploymentMeta)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "deployed_stores": [
    1,
    10
  ],
  "all_stores": false,
  "enabled": true,
  "type": "hard",
  "_id": "5e7e5e4d6b5f3b4b54c95f9c",
  "app": "000000000000000000000004",
  "__v": 6
}
```
</details>









---


#### getDomains
Get attached domain list




```kotlin
client.application("<APPLICATION_ID>").configuration.getDomains().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  



Get attached domain list.

*Returned Response*




[DomainsResponse](#DomainsResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "domains": [
    {
      "_id": "5eb1177748312a3bd55d0f1e",
      "verified": true,
      "name": "uniket.hostx0.de",
      "is_primary": true,
      "is_shortlink": false
    },
    {
      "verified": true,
      "is_primary": false,
      "is_shortlink": true,
      "_id": "5f0858c5f86e00cd42dccc8d",
      "name": "jd.hostx0.de"
    },
    {
      "verified": true,
      "is_primary": false,
      "is_shortlink": false,
      "_id": "6048497e87f5730423149190",
      "name": "testdm.hostx0.de"
    }
  ]
}
```
</details>









---


#### addDomain
Add new domain to application




```kotlin
client.application("<APPLICATION_ID>").configuration.addDomain(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  
| body | [DomainAddRequest](#DomainAddRequest) | yes | Request body |


Add new domain to application.

*Returned Response*




[Domain](#Domain)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "name": "testdm.hostx0.de",
  "verified": true,
  "txtRecords": [],
  "message": "New domain added successfully",
  "is_primary": false,
  "is_shortlink": false,
  "_id": "6048497e87f5730423149190"
}
```
</details>









---


#### removeDomainById
Remove attached domain




```kotlin
client.application("<APPLICATION_ID>").configuration.removeDomainById(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |   
| id | String | yes | Domain _id |  



Remove attached domain.

*Returned Response*




[SuccessMessageResponse](#SuccessMessageResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "message": "Domain removed successfully"
}
```
</details>









---


#### changeDomainType
Change domain type




```kotlin
client.application("<APPLICATION_ID>").configuration.changeDomainType(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  
| body | [UpdateDomainTypeRequest](#UpdateDomainTypeRequest) | yes | Request body |


Change a domain to Primary or Shortlink domain

*Returned Response*




[DomainsResponse](#DomainsResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "domains": [
    {
      "_id": "5eb1177748312a3bd55d0f1e",
      "verified": true,
      "name": "uniket.hostx0.de",
      "is_primary": true,
      "is_shortlink": false
    },
    {
      "verified": true,
      "is_primary": false,
      "is_shortlink": true,
      "_id": "5f0858c5f86e00cd42dccc8d",
      "name": "jd.hostx0.de"
    },
    {
      "verified": true,
      "is_primary": false,
      "is_shortlink": false,
      "_id": "6048497e87f5730423149190",
      "name": "testdm.hostx0.de"
    }
  ]
}
```
</details>









---


#### getDomainStatus
Get domain connected status.




```kotlin
client.application("<APPLICATION_ID>").configuration.getDomainStatus(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  
| body | [DomainStatusRequest](#DomainStatusRequest) | yes | Request body |


Get domain connected status. Check if domain is live and mapped to appropriate IP to fynd servers.

*Returned Response*




[DomainStatusResponse](#DomainStatusResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "connected": true,
  "status": [
    {
      "display": "Domain TXT record entry 5d65089e031f9029f8e8dc2f",
      "status": true
    },
    {
      "display": "Domain pointing to 18.217.232.69 A record",
      "status": true
    },
    {
      "display": "Domain pointing to 18.188.115.251 A record",
      "status": true
    }
  ]
}
```
</details>









---


#### createApplication
Create application




```kotlin
client.configuration.createApplication(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |  
| body | [CreateApplicationRequest](#CreateApplicationRequest) | yes | Request body |


Create new application

*Returned Response*




[CreateAppResponse](#CreateAppResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getApplications
Get list of application under company




```kotlin
client.configuration.getApplications(pageNo: pageNo, pageSize: pageSize, q: q).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| pageNo | Int? | no |  |   
| pageSize | Int? | no |  |   
| q | String? | no | Url encoded object used as mongodb query |  



Get list of application under company

*Returned Response*




[ApplicationsResponse](#ApplicationsResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getApplicationById
Get application data from id




```kotlin
client.application("<APPLICATION_ID>").configuration.getApplicationById().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| applicationId | String | yes | Current application id |  



Get application data from id

*Returned Response*




[Application](#Application)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getCurrencies
Get all currencies




```kotlin
client.configuration.getCurrencies().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |  



Get all currencies

*Returned Response*




[CurrenciesResponse](#CurrenciesResponse)

Currencies Success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "_id": "5ec75d11f7bfb54d798f3516",
      "is_active": true,
      "name": "United States Dollar",
      "code": "USD",
      "created_at": "2020-05-22T05:03:13.354Z",
      "modified_at": "2020-06-05T09:12:04.248Z",
      "decimal_digits": 2,
      "symbol": "$"
    }
  ]
}
```
</details>









---


#### getDomainAvailibility
Check domain availibility before linking to application




```kotlin
client.configuration.getDomainAvailibility(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |  
| body | [DomainSuggestionsRequest](#DomainSuggestionsRequest) | yes | Request body |


Check domain availibility before linking to application. Also sends domain suggestions with similar to queried domain. \ Custom domain search is currently powered by GoDaddy provider.

*Returned Response*




[DomainSuggestionsResponse](#DomainSuggestionsResponse)

Success




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Suggestions for fynd domains</i></summary>

```json
{
  "value": {
    "domains": [
      {
        "name": "test.hostx1.de",
        "is_available": false
      },
      {
        "name": "testhive.hostx1.de",
        "is_available": true
      }
    ]
  }
}
```
</details>

<details>
<summary><i>&nbsp; Suggestions for custom domains</i></summary>

```json
{
  "value": {
    "domains": [
      {
        "name": "test25.in",
        "unsupported": false,
        "is_available": false
      },
      {
        "name": "try25.in",
        "unsupported": false,
        "is_available": true,
        "price": 14.99,
        "currency": "USD"
      }
    ]
  }
}
```
</details>

</details>









---


#### getIntegrationById
Get integration data




```kotlin
client.configuration.getIntegrationById(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| id | Int | yes | Integration id |  



Get integration data

*Returned Response*




[Integration](#Integration)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "_id": "5ec376ce848a005189acb312",
  "validators": {
    "company": {
      "browser_script": "",
      "json_schema": {
        "type": "object",
        "required": [
          "ip_address",
          "icode",
          "gds_entity_id",
          "auth_key"
        ],
        "properties": {
          "gds_entity_id": {
            "type": "string",
            "title": "GDS Entity ID",
            "minLength": 3,
            "maxLength": 10,
            "pattern": "^[a-zA-Z0-9]+$",
            "description": "GDS Entity ID is a unique identifier provided by Ginesys to you."
          },
          "ip_address": {
            "type": "string",
            "title": "IP Address",
            "pattern": "(\\d{1,3}\\.){3}\\d{1,3}",
            "description": "Enter IP address provided by Ginesys for your POS server"
          },
          "auth_key": {
            "title": "Auth Key",
            "type": "string",
            "maxLength": 500,
            "description": "Provide authentication token provided by Ginesys to you."
          },
          "icode": {
            "title": "ICODE",
            "type": "string",
            "enum": [
              "ean",
              "upc",
              "alu",
              "sku_code"
            ],
            "description": "Please select the correct SKU identifier that you use to provide inventory to Fynd."
          }
        }
      }
    },
    "store": {
      "browser_script": "",
      "json_schema": {
        "type": "object",
        "properties": {
          "location_id": {
            "type": "string",
            "title": "Location ID",
            "description": "Provide site code as per POS/SAP."
          },
          "ip_address": {
            "type": "string",
            "title": "IP Address",
            "pattern": "(\\d{1,3}\\.){3}\\d{1,3}",
            "description": "Enter IP address provided by Ginesys for your POS server"
          }
        }
      }
    }
  },
  "description": "Sap Integration west ELM brands",
  "constants": {},
  "name": "SAP RBL Integration",
  "meta": [
    {
      "public": true,
      "_id": "5ee3e246129be17ce0b59ef4",
      "name": "price_level",
      "value": "store"
    }
  ],
  "icon": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1589868232/addsale/platform/integrations/icon/z3kj9p8nidx4zzmdutdu.svg",
  "owner": "5e60e43dcd08cf01069eb23e",
  "created_at": "2020-05-19T06:03:58.757Z",
  "modified_at": "2020-06-15T12:00:42.598Z",
  "token": "qk60vXqk-",
  "secret": "Gp0dYInpUV",
  "__v": 13,
  "description_html": ""
}
```
</details>









---


#### getAvailableOptIns
Get all available integration opt-ins




```kotlin
client.configuration.getAvailableOptIns(pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |  



Get all available integration opt-ins

*Returned Response*




[GetIntegrationsOptInsResponse](#GetIntegrationsOptInsResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "validators": {
        "company": {
          "json_schema": [
            {
              "display": "Host",
              "key": "host",
              "type": "text",
              "tooltip": "Enter host address"
            }
          ],
          "browser_script": ""
        },
        "store": {
          "json_schema": [],
          "browser_script": ""
        },
        "inventory": {
          "json_schema": [],
          "browser_script": ""
        },
        "order": {
          "json_schema": [],
          "browser_script": ""
        }
      },
      "description": "awesome integration",
      "description_html": "",
      "constants": "{\"mop_mapping\":{\"FYND\":\"FYND\"}}",
      "companies": [],
      "support": [
        "inventory",
        "order"
      ],
      "_id": "5e56089f4265cf2846d1e58c",
      "name": "x0-1",
      "meta": [
        {
          "public": true,
          "_id": "5e56089f4265cf81e1d1e58e",
          "name": "wow",
          "value": "1"
        }
      ],
      "icon": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1582696589/addsale/platform/integrations/icon/jihgcoibfmdttgiukwg0.png",
      "owner": "5e55fe074bda3c392ed9eab2",
      "created_at": "2020-02-26T05:56:47.214Z",
      "modified_at": "2021-03-02T12:29:03.554Z",
      "token": "fKoHRW5H",
      "secret": "d1E85CTmf",
      "__v": 12
    },
    {
      "validators": {
        "company": {
          "json_schema": [],
          "browser_script": ""
        },
        "store": {
          "json_schema": [],
          "browser_script": ""
        },
        "inventory": {
          "json_schema": [],
          "browser_script": ""
        },
        "order": {
          "json_schema": [],
          "browser_script": ""
        }
      },
      "description": "jabardast",
      "description_html": "",
      "constants": "{\"mop_mapping\":{\"FYND\":\"FYND\"}}",
      "companies": [],
      "support": [
        "inventory",
        "order"
      ],
      "_id": "5e5608bf4265cf7198d1e58f",
      "name": "x0-2",
      "meta": [
        {
          "public": false,
          "_id": "5e5608bf4265cf813fd1e590",
          "name": "wow",
          "value": "1"
        }
      ],
      "icon": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1582696633/addsale/platform/integrations/icon/cstvvkgjgip1ja56gq4x.png",
      "owner": "5e55fe074bda3c392ed9eab2",
      "created_at": "2020-02-26T05:57:19.875Z",
      "modified_at": "2021-02-15T05:23:55.962Z",
      "token": "3h3_mnzp",
      "secret": "dgGHrIlFG",
      "__v": 7
    }
  ],
  "page": {
    "type": "number",
    "current": 1,
    "size": 50,
    "item_total": 24,
    "has_next": false
  }
}
```
</details>









---


#### getSelectedOptIns
Get company/store level integration opt-ins




```kotlin
client.configuration.getSelectedOptIns(level: level, uid: uid, pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| level | String | yes | Integration level |   
| uid | Int | yes | Integration level uid |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |  



Get company/store level integration opt-ins

*Returned Response*




[GetIntegrationsOptInsResponse](#GetIntegrationsOptInsResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "validators": {
        "company": {
          "json_schema": [
            {
              "display": "Host",
              "key": "host",
              "type": "text",
              "tooltip": "Enter host address"
            }
          ],
          "browser_script": ""
        },
        "store": {
          "json_schema": [],
          "browser_script": ""
        },
        "inventory": {
          "json_schema": [],
          "browser_script": ""
        },
        "order": {
          "json_schema": [],
          "browser_script": ""
        }
      },
      "description": "awesome integration",
      "description_html": "",
      "constants": "{\"mop_mapping\":{\"FYND\":\"FYND\"}}",
      "companies": [],
      "support": [
        "inventory",
        "order"
      ],
      "_id": "5e56089f4265cf2846d1e58c",
      "name": "x0-1",
      "meta": [
        {
          "public": true,
          "_id": "5e56089f4265cf81e1d1e58e",
          "name": "wow",
          "value": "1"
        }
      ],
      "icon": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1582696589/addsale/platform/integrations/icon/jihgcoibfmdttgiukwg0.png",
      "owner": "5e55fe074bda3c392ed9eab2",
      "created_at": "2020-02-26T05:56:47.214Z",
      "modified_at": "2021-03-02T12:29:03.554Z",
      "token": "fKoHRW5H",
      "secret": "d1E85CTmf",
      "__v": 12
    },
    {
      "validators": {
        "company": {
          "json_schema": [],
          "browser_script": ""
        },
        "store": {
          "json_schema": [],
          "browser_script": ""
        },
        "inventory": {
          "json_schema": [],
          "browser_script": ""
        },
        "order": {
          "json_schema": [],
          "browser_script": ""
        }
      },
      "description": "jabardast",
      "description_html": "",
      "constants": "{\"mop_mapping\":{\"FYND\":\"FYND\"}}",
      "companies": [],
      "support": [
        "inventory",
        "order"
      ],
      "_id": "5e5608bf4265cf7198d1e58f",
      "name": "x0-2",
      "meta": [
        {
          "public": false,
          "_id": "5e5608bf4265cf813fd1e590",
          "name": "wow",
          "value": "1"
        }
      ],
      "icon": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1582696633/addsale/platform/integrations/icon/cstvvkgjgip1ja56gq4x.png",
      "owner": "5e55fe074bda3c392ed9eab2",
      "created_at": "2020-02-26T05:57:19.875Z",
      "modified_at": "2021-02-15T05:23:55.962Z",
      "token": "3h3_mnzp",
      "secret": "dgGHrIlFG",
      "__v": 7
    }
  ],
  "page": {
    "type": "number",
    "current": 1,
    "size": 50,
    "item_total": 24,
    "has_next": false
  }
}
```
</details>









---


#### getIntegrationLevelConfig
Get integration level config




```kotlin
client.configuration.getIntegrationLevelConfig(id: id, level: level, opted: opted, checkPermission: checkPermission).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| id | String | yes | Integration id |   
| level | String | yes | Integration level |   
| opted | Boolean? | no | Filter on opted stores |   
| checkPermission | Boolean? | no | Filter on if permissions are present |  



Get integration/integration-opt-in level config

*Returned Response*




[IntegrationConfigResponse](#IntegrationConfigResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "opted": false,
      "permissions": [],
      "last_patch": [],
      "_id": "5ec377f2848a0073feacb31b",
      "integration": "5ec376ce848a005189acb312",
      "level": "store",
      "uid": 1,
      "meta": [],
      "token": "1RuGX0Fyp",
      "created_at": "2020-05-19T06:08:50.199Z",
      "modified_at": "2020-08-17T07:54:01.809Z",
      "__v": 14,
      "data": {
        "location_id": "09876",
        "ip_address": "1.2.3.4"
      }
    }
  ]
}
```
</details>









---


#### getIntegrationByLevelId
Get level data for integration




```kotlin
client.configuration.getIntegrationByLevelId(id: id, level: level, uid: uid).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| id | String | yes | Integration id |   
| level | String | yes | Integration level |   
| uid | Int | yes | Integration level uid |  



Get level data for integration

*Returned Response*




[IntegrationLevel](#IntegrationLevel)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "opted": false,
  "permissions": [],
  "last_patch": [],
  "_id": "5ec377f2848a0073feacb31b",
  "integration": "5ec376ce848a005189acb312",
  "level": "store",
  "uid": 1,
  "meta": [],
  "token": "1RuGX0Fyp",
  "created_at": "2020-05-19T06:08:50.199Z",
  "modified_at": "2020-08-17T07:54:01.809Z",
  "__v": 14,
  "data": {
    "location_id": "09876",
    "ip_address": "1.2.3.4"
  }
}
```
</details>









---


#### getLevelActiveIntegrations
Check store has active integration




```kotlin
client.configuration.getLevelActiveIntegrations(id: id, level: level, uid: uid).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| id | String | yes | Integration id |   
| level | String | yes | Integration level |   
| uid | Int | yes | Integration level uid |  



API checks if a store is already opted in any other integrations

*Returned Response*




[OptedStoreIntegration](#OptedStoreIntegration)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "opted": false,
  "permissions": [],
  "last_patch": [],
  "_id": "5ec377f2848a0073feacb31b",
  "integration": "5ec376ce848a005189acb312",
  "level": "store",
  "uid": 1,
  "meta": [],
  "token": "1RuGX0Fyp",
  "created_at": "2020-05-19T06:08:50.199Z",
  "modified_at": "2020-08-17T07:54:01.809Z",
  "__v": 14,
  "data": {
    "location_id": "09876",
    "ip_address": "1.2.3.4"
  }
}
```
</details>









---


#### getBrandsByCompany
Get brands by company




```kotlin
client.configuration.getBrandsByCompany(q: q).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| q | String? | no | Search text for brand name |  



Get brands by company

*Returned Response*




[BrandsByCompanyResponse](#BrandsByCompanyResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "brands": [
    {
      "name": "5th Avenue",
      "value": 476,
      "brand_logo_url": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/--unnamed--/1595615012186.jpeg",
      "brand_banner_url": "https://hdn-1.addsale.com/x0/seller/pictures/landscape-banner/original/--unnamed--/1595615012724.jpeg",
      "brand_banner_portrait_url": "https://hdn-1.addsale.com/x0/seller/pictures/portrait-banner/original/--unnamed--/1595615013203.jpeg"
    },
    {
      "name": "Abhay",
      "value": 47,
      "brand_logo_url": "https://hdn-1.fynd.com/brands/pictures/square-logo/resize-h:200,w:0/9fG6jZUJV-brand-Slamay.png",
      "brand_banner_url": "https://hdn-1.addsale.com/x0/seller/pictures/landscape-banner/original/cpApcg_insta_01.jpg034422ca-b739-4a30-ba9c-87ca32e8c2ef/cpApcg_insta_01.jpg",
      "brand_banner_portrait_url": "https://hdn-1.addsale.com/x0/seller/pictures/portrait-banner/original/mtaSMv_insta_01.jpga088b881-886d-4b5a-b82f-139bd2aa3f35/mtaSMv_insta_01.jpg"
    }
  ]
}
```
</details>









---


#### getCompanyByBrands
Get company by brand uids




```kotlin
client.configuration.getCompanyByBrands(pageNo: pageNo, pageSize: pageSize, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |  
| body | [CompanyByBrandsRequest](#CompanyByBrandsRequest) | yes | Request body |


Get company by brand uids

*Returned Response*




[CompanyByBrandsResponse](#CompanyByBrandsResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "company_name": "RELIANCE RETAIL LTD",
      "company_id": 1
    },
    {
      "company_name": "SARASUOLE PRIVATE LIMITED",
      "company_id": 3
    },
    {
      "company_name": "Lloyd Palek",
      "company_id": 4
    }
  ],
  "page": {
    "type": "number",
    "current": 1,
    "size": 200,
    "item_total": 171,
    "has_next": false
  }
}
```
</details>









---


#### getStoreByBrands
Get stores by brand uids




```kotlin
client.configuration.getStoreByBrands(pageNo: pageNo, pageSize: pageSize, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |  
| body | [StoreByBrandsRequest](#StoreByBrandsRequest) | yes | Request body |


Get stores by brand uids

*Returned Response*




[StoreByBrandsResponse](#StoreByBrandsResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "store_name": "RRL01",
      "store_id": 1,
      "store_type": "warehouse",
      "store_code": "WH_8513",
      "store_address": {
        "state": "MAHARASHTRA",
        "address1": "SHOPSENSE RETAIL TECHNOLOGIES PRIVATE LIMITED 1ST FLOOR WEWORK VIJAY DIAMOND, CROSS RD B, AJIT NAGAR,",
        "lat_long": {
          "type": "Point",
          "coordinates": [
            72.8691788,
            19.1174114
          ]
        },
        "address2": "KONDIVITA, ANDHERI EAST, MUMBAI, MAHARASHTRA 400069",
        "pincode": 400059,
        "country": "INDIA",
        "city": "MUMBAI"
      },
      "company": {
        "uid": 1,
        "name": "RELIANCE RETAIL LTD"
      }
    },
    {
      "store_name": "RUOSH WAREHOUSE",
      "store_id": 2,
      "store_type": "warehouse",
      "store_code": "RUOSH43",
      "store_address": {
        "state": "MAHARASHTRA",
        "address1": "RAUNAK CITY SECTOR 4 D10, SAPAD GAON",
        "lat_long": {
          "type": "Point",
          "coordinates": [
            73.121952,
            19.2645048
          ]
        },
        "address2": "SAPAD GAON, KHADAKPADA, ",
        "pincode": 421301,
        "country": "INDIA",
        "city": "THANE",
        "landmark": "near taj"
      },
      "company": {
        "uid": 3,
        "name": "SARASUOLE PRIVATE LIMITED"
      }
    }
  ],
  "page": {
    "type": "number",
    "current": 1,
    "size": 200,
    "item_total": 762,
    "has_next": true
  }
}
```
</details>









---


#### getOtherSellerApplications
Get other seller applications




```kotlin
client.configuration.getOtherSellerApplications(pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| pageNo | Int? | no | Current page no |   
| pageSize | Int? | no | Current request items count |  



Get other seller applications who has opted current company as inventory

*Returned Response*




[OtherSellerApplications](#OtherSellerApplications)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "name": "intent 2",
      "description": "",
      "_id": "5f030880f019afd636889afc",
      "domain": "intent.hostx0.de",
      "company": {
        "uid": 94,
        "name": "DummyImran"
      },
      "opt_type": "store"
    },
    {
      "name": "new application imran",
      "description": "",
      "_id": "5f03f5d17692029e2d1a50a5",
      "domain": "imranstore.hostx0.de",
      "company": {
        "uid": 94,
        "name": "DummyImran"
      },
      "opt_type": "store"
    },
    {
      "name": "helo",
      "description": "",
      "_id": "5f03f63b769202170c1a50a9",
      "domain": "helo.hostx0.de",
      "company": {
        "uid": 7,
        "name": "Zack Burgdorf"
      },
      "opt_type": "store"
    }
  ],
  "page": {
    "type": "number",
    "current": 1,
    "size": 10,
    "item_total": 20,
    "has_next": true
  }
}
```
</details>









---


#### getOtherSellerApplicationById
Get other seller applications




```kotlin
client.configuration.getOtherSellerApplicationById(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| id | String | yes | Application Id |  



Get other seller application

*Returned Response*




[OptedApplicationResponse](#OptedApplicationResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "name": "intent 2",
  "description": "",
  "_id": "5f030880f019afd636889afc",
  "domain": "intent.hostx0.de",
  "company": {
    "uid": 94,
    "name": "DummyImran"
  },
  "opted_inventory": {
    "opt_type": {
      "key": "store",
      "display": "Store"
    },
    "items": [
      {
        "name": "RRL01",
        "id": 1,
        "store_code": "WH_8513",
        "_id": "5ec2c0b168fc2800017112f5",
        "modified_on": "2020-09-09T04:25:55.843Z",
        "uid": 1,
        "address": {
          "state": "MAHARASHTRA",
          "address1": "SHOPSENSE RETAIL TECHNOLOGIES PRIVATE LIMITED 1ST FLOOR WEWORK VIJAY DIAMOND, CROSS RD B, AJIT NAGAR,",
          "lat_long": {
            "type": "Point",
            "coordinates": [
              72.8691788,
              19.1174114
            ]
          },
          "address2": "KONDIVITA, ANDHERI EAST, MUMBAI, MAHARASHTRA 400069",
          "pincode": 400059,
          "country": "INDIA",
          "city": "MUMBAI"
        },
        "display_name": "RRL01",
        "store_type": "warehouse",
        "company_id": 1
      }
    ]
  },
  "opt_out_inventory": {
    "store": [],
    "company": []
  }
}
```
</details>









---


#### optOutFromApplication
Opt out company or store from other seller application




```kotlin
client.configuration.optOutFromApplication(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Current company id |   
| id | String | yes | Application Id |  
| body | [OptOutInventory](#OptOutInventory) | yes | Request body |


Opt out company or store from other seller application

*Returned Response*




[SuccessMessageResponse](#SuccessMessageResponse)

Success




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "message": "Updated opt out data"
}
```
</details>









---



### Schemas


 
 
 #### [LocationDefaultLanguage](#LocationDefaultLanguage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | code | String? |  yes  |  |

---


 
 
 #### [LocationDefaultCurrency](#LocationDefaultCurrency)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | symbol | String? |  yes  |  |
 | code | String? |  yes  |  |

---


 
 
 #### [LocationCountry](#LocationCountry)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | capital | String? |  yes  |  |
 | currency | String? |  yes  |  |
 | iso2 | String? |  yes  |  |
 | iso3 | String? |  yes  |  |
 | name | String? |  yes  |  |
 | parent | String? |  yes  |  |
 | phoneCode | String? |  yes  |  |
 | type | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | v | Int? |  yes  |  |
 | id | String? |  yes  |  |
 | defaultCurrency | [LocationDefaultCurrency](#LocationDefaultCurrency)? |  yes  |  |
 | defaultLanguage | [LocationDefaultLanguage](#LocationDefaultLanguage)? |  yes  |  |

---


 
 
 #### [Locations](#Locations)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<HashMap<String,Any>>? |  yes  |  |

---




 
 
 #### [TicketList](#TicketList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Ticket](#Ticket)>? |  yes  | List of tickets |
 | filters | [Filter](#Filter)? |  yes  | All the filters available for tickets |
 | page | [Page](#Page)? |  yes  | Describes the pagination state |

---


 
 
 #### [Page](#Page)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | itemTotal | Int? |  yes  |  |
 | nextId | String? |  yes  |  |
 | hasPrevious | Boolean? |  yes  |  |
 | hasNext | Boolean? |  yes  |  |
 | current | Int? |  yes  |  |
 | type | String |  no  |  |
 | size | Int? |  yes  |  |

---


 
 
 #### [TicketHistoryList](#TicketHistoryList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[TicketHistory](#TicketHistory)>? |  yes  | List of ticket history |
 | page | [Page](#Page)? |  yes  | Describes the pagination state |

---


 
 
 #### [CustomFormList](#CustomFormList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[CustomForm](#CustomForm)>? |  yes  | List of forms |
 | page | [Page](#Page)? |  yes  | Describes the pagination state |

---


 
 
 #### [CreateCustomFormPayload](#CreateCustomFormPayload)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | slug | String |  no  | Slug for the form |
 | title | String |  no  | Title for the form |
 | inputs | ArrayList<HashMap<String,Any>> |  no  | List of all the form components |
 | description | String? |  yes  | Description of the form |
 | headerImage | String? |  yes  | Header image that is to be shown for the form |
 | priority | [PriorityEnum](#PriorityEnum) |  no  | Describes the priority of the tickets created by the form |
 | shouldNotify | Boolean? |  yes  | Indicates if staff should be notified when a response is received |
 | successMessage | String? |  yes  | Success message that will be shown on submission |
 | pollForAssignment | [PollForAssignment](#PollForAssignment)? |  yes  | Describes how polling will be done for the tickets createds |

---


 
 
 #### [EditCustomFormPayload](#EditCustomFormPayload)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String |  no  | Title for the form |
 | inputs | ArrayList<HashMap<String,Any>> |  no  | List of all the form components |
 | description | String? |  yes  | Description of the form |
 | priority | [PriorityEnum](#PriorityEnum) |  no  | Describes the priority of the tickets created by the form |
 | headerImage | String? |  yes  | Header image that is to be shown for the form |
 | shouldNotify | Boolean? |  yes  | Indicates if staff should be notified when a response is received |
 | loginRequired | Boolean? |  yes  | Denotes if login is required to make a form response submission |
 | successMessage | String? |  yes  | Success message that will be shown on submission |
 | pollForAssignment | [PollForAssignment](#PollForAssignment)? |  yes  | Describes how polling will be done for the tickets createds |

---


 
 
 #### [EditTicketPayload](#EditTicketPayload)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | content | [TicketContent](#TicketContent)? |  yes  | Ticket conetent details |
 | category | String? |  yes  | Category assigned to the ticket |
 | subCategory | String? |  yes  | Sub-category assigned to the ticket |
 | source | String? |  yes  | Denotes if the ticket was created at company or application level |
 | status | String? |  yes  | Denotes in what state is the ticket |
 | priority | [PriorityEnum](#PriorityEnum)? |  yes  | Denotes the priority of ticket |
 | assignedTo | [AgentChangePayload](#AgentChangePayload)? |  yes  | Details of support staff to whom ticket is assigned |
 | tags | ArrayList<String>? |  yes  | Tags relevant to ticket |

---


 
 
 #### [AgentChangePayload](#AgentChangePayload)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | agentId | String |  no  | Agent's unique ID |

---


 
 
 #### [CreateVideoRoomResponse](#CreateVideoRoomResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uniqueName | String |  no  | Video Room's unique name |

---


 
 
 #### [CloseVideoRoomResponse](#CloseVideoRoomResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean |  no  | Denotes if operation was successfully |

---


 
 
 #### [CreateVideoRoomPayload](#CreateVideoRoomPayload)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uniqueName | String |  no  | Ticket id |
 | notify | ArrayList<[NotifyUser](#NotifyUser)>? |  yes  | List of people to be notified |

---


 
 
 #### [NotifyUser](#NotifyUser)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | countryCode | String |  no  | Country code |
 | phoneNumber | String |  no  | Phone number |

---


 
 
 #### [Filter](#Filter)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | priorities | ArrayList<[Priority](#Priority)> |  no  | List of possible priorities for tickets |
 | categories | ArrayList<[TicketCategory](#TicketCategory)>? |  yes  | List of possible categories for tickets |
 | statuses | ArrayList<[Status](#Status)> |  no  | List of possible statuses for tickets |
 | assignees | ArrayList<HashMap<String,Any>> |  no  | List of support staff availble for tickets assignment |

---


 
 
 #### [TicketHistoryPayload](#TicketHistoryPayload)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | HashMap<String,Any> |  no  | Details of history event |
 | type | [HistoryTypeEnum](#HistoryTypeEnum) |  no  | Type of history event |

---


 
 
 #### [CustomFormSubmissionPayload](#CustomFormSubmissionPayload)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | response | ArrayList<[KeyValue](#KeyValue)> |  no  | Form response |
 | attachments | ArrayList<[TicketAsset](#TicketAsset)>? |  yes  | List of all attachments related to the form |

---


 
 
 #### [KeyValue](#KeyValue)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String |  no  | Parameter for evaluating |
 | value | HashMap<String,Any> |  no  | Response for the parameter |

---


 
 
 #### [GetTokenForVideoRoomResponse](#GetTokenForVideoRoomResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | accessToken | String |  no  | Access token to be used for video room |

---


 
 
 #### [GetParticipantsInsideVideoRoomResponse](#GetParticipantsInsideVideoRoomResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | participants | ArrayList<[Participant](#Participant)> |  no  | List of participants of the video room |

---


 
 
 #### [Participant](#Participant)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  | Details of participant |
 | identity | String? |  yes  | Unique identifier of participant |
 | status | String? |  yes  | Status of participant |

---


 
 
 #### [PhoneNumber](#PhoneNumber)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  | Denotes if the phone number is active |
 | primary | Boolean? |  yes  | Denotes it's the primary phone number for the account |
 | verified | Boolean? |  yes  | Denotes it's a verified phone number |
 | phone | String? |  yes  | Phone number |
 | countryCode | Int? |  yes  | Country code |

---


 
 
 #### [Email](#Email)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | primary | Boolean? |  yes  | Denotes it's the primary email for the account |
 | verified | Boolean? |  yes  | Denotes it's a verified email |
 | email | String? |  yes  | Email Address |
 | active | Boolean? |  yes  | Denotes if the email is active |

---


 
 
 #### [Debug](#Debug)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | source | String? |  yes  | Source of user |
 | platform | String? |  yes  | Platform of user |

---


 
 
 #### [SubmitCustomFormResponse](#SubmitCustomFormResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ticket | [Ticket](#Ticket) |  no  | Ticket created on form submission |

---


 
 
 #### [TicketContext](#TicketContext)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | applicationId | String? |  yes  | Application ID related to the ticket |
 | companyId | String |  no  | Company ID related to the ticket |

---


 
 
 #### [CreatedOn](#CreatedOn)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | userAgent | String |  no  | Useragent details |

---


 
 
 #### [TicketAsset](#TicketAsset)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  | Display text for asset |
 | value | String |  no  | To be used for details |
 | type | Any |  no  | Type of asset |

---


 
 
 #### [TicketContent](#TicketContent)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String |  no  | Title for ticket |
 | description | String? |  yes  | Long description of issue |
 | attachments | ArrayList<[TicketAsset](#TicketAsset)>? |  yes  | List of all attachments related to the ticket |

---


 
 
 #### [AddTicketPayload](#AddTicketPayload)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | createdBy | HashMap<String,Any>? |  yes  | Creator of the ticket |
 | status | String? |  yes  | Status of the ticket |
 | priority | [PriorityEnum](#PriorityEnum)? |  yes  | Priority of the ticket |
 | category | String |  no  | Category of the ticket |
 | content | [TicketContent](#TicketContent) |  no  | Content for the ticket |

---


 
 
 #### [Priority](#Priority)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | [PriorityEnum](#PriorityEnum) |  no  | Key for priority |
 | display | String |  no  | Display text for priority |
 | color | String |  no  | Color for priority |

---


 
 
 #### [Status](#Status)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String |  no  | Key for status |
 | display | String |  no  | Display text for status |
 | color | String |  no  | Color for status |

---


 
 
 #### [TicketCategory](#TicketCategory)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String |  no  | Key for category |
 | display | String |  no  | Display text for category |
 | form | [CustomForm](#CustomForm)? |  yes  | Form related to the category |
 | subCategories | ArrayList<[TicketSubCategory](#TicketSubCategory)>? |  yes  | Sub-category related to the category |
 | feedbackForm | [TicketFeedbackForm](#TicketFeedbackForm)? |  yes  | Feedback form of category used to submit ticket feedback |

---


 
 
 #### [TicketSubCategory](#TicketSubCategory)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String |  no  | Key for sub-category |
 | display | String |  no  | Display text for sub-category |

---


 
 
 #### [TicketFeedbackForm](#TicketFeedbackForm)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String |  no  | Feedback form title that will be shown to the user |
 | display | ArrayList<HashMap<String,Any>>? |  yes  | List of all the form fields |

---


 
 
 #### [TicketFeedbackList](#TicketFeedbackList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[TicketFeedback](#TicketFeedback)>? |  yes  | List of all ticket feedback for the ticket |

---


 
 
 #### [TicketFeedbackPayload](#TicketFeedbackPayload)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | formResponse | HashMap<String,Any>? |  yes  | Key-value pairs of all the form fields and their response |

---


 
 
 #### [SubmitButton](#SubmitButton)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String |  no  | Title for submit button |
 | titleColor | String |  no  | Title color submit button |
 | backgroundColor | String |  no  | Color for submit button |

---


 
 
 #### [PollForAssignment](#PollForAssignment)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | duration | Double |  no  | Duration for polling of staff |
 | message | String |  no  | Message for polling |
 | successMessage | String |  no  | Message for successful polling |
 | failureMessage | String |  no  | Message if polling failed |

---


 
 
 #### [CustomForm](#CustomForm)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | applicationId | String |  no  | Application ID for form |
 | slug | String |  no  | Slug for the form, which is to be used for accessing the form |
 | headerImage | String? |  yes  | Form header image that will be shown to the user |
 | title | String |  no  | Form title that will be shown to the user |
 | description | String? |  yes  | Form description that will be shown to the user |
 | priority | [Priority](#Priority) |  no  | Sets priority of tickets created by form response |
 | loginRequired | Boolean |  no  | Denotes if login is required to make a form response submission |
 | shouldNotify | Boolean |  no  | Denotes if new response submission for the form should be notified to the assignees |
 | successMessage | String? |  yes  | Message that is to be shown on succesfull form response submission |
 | submitButton | [SubmitButton](#SubmitButton)? |  yes  | Details for submit button |
 | inputs | ArrayList<HashMap<String,Any>> |  no  | List of all the form fields |
 | createdOn | [CreatedOn](#CreatedOn)? |  yes  | Gives details of when the form was created |
 | createdBy | HashMap<String,Any>? |  yes  | Gives details of user who created the form |
 | pollForAssignment | [PollForAssignment](#PollForAssignment)? |  yes  | Details of how polling should be done for support |
 | id | String |  no  | Unique identifier for the form |

---


 
 
 #### [FeedbackResponseItem](#FeedbackResponseItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String |  no  | Question/Title of the form field |
 | key | String |  no  | Key of the form field |
 | value | String |  no  | User response value for the form field |

---


 
 
 #### [TicketFeedback](#TicketFeedback)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  | Unique identifier for the feedback |
 | ticketId | String |  no  | Readable ticket number |
 | companyId | String |  no  | Company id for which ticket was raised |
 | response | ArrayList<[FeedbackResponseItem](#FeedbackResponseItem)> |  no  |  |
 | category | String? |  yes  | Category of the ticket |
 | user | HashMap<String,Any>? |  yes  | User who submitted the feedback |
 | updatedAt | String? |  yes  | Time when the feedback was last updated |
 | createdAt | String? |  yes  | Time when the feedback was created |

---


 
 
 #### [TicketHistory](#TicketHistory)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String |  no  | Type of the history event |
 | value | HashMap<String,Any> |  no  | Data of the history event |
 | ticketId | String |  no  | Readable ticket number |
 | createdOn | [CreatedOn](#CreatedOn)? |  yes  | Time of creation of the history event |
 | createdBy | HashMap<String,Any>? |  yes  | User who created the history event |
 | id | String |  no  | Unique identifier of the history event |
 | updatedAt | String? |  yes  | Time of last update of the history event |
 | createdAt | String? |  yes  | Time of creation of the history event |

---


 
 
 #### [Ticket](#Ticket)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | context | [TicketContext](#TicketContext)? |  yes  | Details of company and application realated to the ticket |
 | createdOn | [CreatedOn](#CreatedOn)? |  yes  | Details of company and application realated to the ticket |
 | responseId | String? |  yes  | Details of company and application realated to the ticket |
 | content | [TicketContent](#TicketContent)? |  yes  | Ticket conetent details |
 | ticketId | String |  no  | Readable ticket number |
 | category | [TicketCategory](#TicketCategory) |  no  | Category assigned to the ticket |
 | subCategory | [TicketSubCategory](#TicketSubCategory)? |  yes  | Sub-category assigned to the ticket |
 | source | [TicketSourceEnum](#TicketSourceEnum) |  no  | Denotes if the ticket was created at company or application level |
 | status | [Status](#Status) |  no  | Denotes in what state is the ticket |
 | priority | [Priority](#Priority) |  no  | Denotes the priority of ticket |
 | createdBy | HashMap<String,Any>? |  yes  | User details of ticket creator |
 | assignedTo | HashMap<String,Any>? |  yes  | Details of support staff to whom ticket is assigned |
 | tags | ArrayList<String>? |  yes  | Tags relevant to ticket |
 | customJson | HashMap<String,Any>? |  yes  | custom json relevant to the ticket |
 | isFeedbackPending | Boolean? |  yes  | Denotes if feedback submission is pending for the ticket |
 | id | String |  no  | Unique identifier for the ticket |
 | updatedAt | String? |  yes  | Time when the ticket was last updated |
 | createdAt | String? |  yes  | Time when the ticket was created |

---




 
 
 #### [Activity](#Activity)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | currentState | HashMap<String,Any>? |  yes  |  |
 | documentId | String? |  yes  |  |
 | previousState | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [ActivityDump](#ActivityDump)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | activity | [Activity](#Activity)? |  yes  |  |
 | createdBy | [CreatedBy](#CreatedBy)? |  yes  |  |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | id | String? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [AddMediaListRequest](#AddMediaListRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | entityId | String? |  yes  |  |
 | entityType | String? |  yes  |  |
 | mediaList | ArrayList<[AddMediaRequest](#AddMediaRequest)>? |  yes  |  |
 | refId | String? |  yes  |  |
 | refType | String? |  yes  |  |

---


 
 
 #### [AddMediaRequest](#AddMediaRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cloudId | String? |  yes  |  |
 | cloudName | String? |  yes  |  |
 | cloudProvider | String? |  yes  |  |
 | entityId | String? |  yes  |  |
 | entityType | String? |  yes  |  |
 | mediaUrl | String? |  yes  |  |
 | refId | String? |  yes  |  |
 | refType | String? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | thumbnailUrl | String? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [ApproveRequest](#ApproveRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | approve | Boolean? |  yes  |  |
 | entityType | String? |  yes  |  |
 | id | String |  no  |  |
 | reason | String? |  yes  |  |

---


 
 
 #### [Attribute](#Attribute)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | description | String? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | tags | ArrayList<[TagMeta](#TagMeta)>? |  yes  |  |

---


 
 
 #### [AttributeObject](#AttributeObject)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | name | String |  no  |  |
 | slug | String? |  yes  |  |
 | title | String? |  yes  |  |
 | type | String |  no  |  |
 | value | Double |  no  |  |

---


 
 
 #### [CreatedBy](#CreatedBy)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | tags | ArrayList<[TagMeta](#TagMeta)>? |  yes  |  |

---


 
 
 #### [CursorGetResponse](#CursorGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [DateMeta](#DateMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | createdOn | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |

---


 
 
 #### [DeviceMeta](#DeviceMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | appVersion | String? |  yes  |  |
 | platform | String? |  yes  |  |

---


 
 
 #### [Entity](#Entity)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [EntityRequest](#EntityRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | entityId | String? |  yes  |  |
 | entityType | String? |  yes  |  |

---


 
 
 #### [FeedbackAttributes](#FeedbackAttributes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Attribute](#Attribute)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [FeedbackError](#FeedbackError)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | code | HashMap<String,Any>? |  yes  |  |
 | exception | String? |  yes  |  |
 | info | String? |  yes  |  |
 | message | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | requestId | String? |  yes  |  |
 | stackTrace | String? |  yes  |  |
 | status | Int? |  yes  |  |

---


 
 
 #### [FeedbackState](#FeedbackState)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  |  |
 | archive | Boolean? |  yes  |  |
 | media | String? |  yes  | image, video, any |
 | qna | Boolean? |  yes  |  |
 | rating | Boolean? |  yes  |  |
 | review | Boolean? |  yes  |  |

---


 
 
 #### [GetResponse](#GetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | HashMap<String,Any>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [GetReviewResponse](#GetReviewResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | facets | ArrayList<[ReviewFacet](#ReviewFacet)>? |  yes  |  |
 | items | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |
 | sort | ArrayList<[SortMethod](#SortMethod)>? |  yes  |  |

---


 
 
 #### [InsertResponse](#InsertResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | count | Int? |  yes  |  |

---


 
 
 #### [MediaMeta](#MediaMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | maxCount | Int? |  yes  |  |
 | size | Int? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [MediaMetaRequest](#MediaMetaRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | maxCount | Int |  no  |  |
 | size | Int |  no  |  |

---


 
 
 #### [NumberGetResponse](#NumberGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [PageCursor](#PageCursor)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | current | Int? |  yes  |  |
 | hasNext | Boolean? |  yes  |  |
 | hasPrevious | Boolean? |  yes  |  |
 | itemTotal | Int? |  yes  |  |
 | nextId | String? |  yes  |  |
 | size | Int |  no  |  |
 | type | String |  no  |  |

---


 
 
 #### [PageNumber](#PageNumber)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | current | Int? |  yes  |  |
 | hasNext | Boolean? |  yes  |  |
 | itemTotal | Int? |  yes  |  |
 | size | Int? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [Rating](#Rating)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | attributes | ArrayList<[Attribute](#Attribute)>? |  yes  |  |
 | attributesSlugs | ArrayList<String>? |  yes  |  |
 | ui | [UI](#UI)? |  yes  |  |

---


 
 
 #### [RatingRequest](#RatingRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | attributes | ArrayList<String> |  no  |  |
 | ui | [UI](#UI)? |  yes  |  |

---


 
 
 #### [ReportAbuseRequest](#ReportAbuseRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | entityId | String |  no  |  |
 | entityType | String |  no  |  |

---


 
 
 #### [Review](#Review)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | header | String? |  yes  |  |
 | imageMeta | [MediaMeta](#MediaMeta)? |  yes  |  |
 | title | String? |  yes  |  |
 | videoMeta | [MediaMeta](#MediaMeta)? |  yes  |  |
 | voteAllowed | Boolean? |  yes  |  |

---


 
 
 #### [ReviewFacet](#ReviewFacet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | name | String? |  yes  |  |
 | selected | Boolean? |  yes  |  |
 | slug | String? |  yes  |  |
 | type | String? |  yes  | rating, attributerating |

---


 
 
 #### [ReviewRequest](#ReviewRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String |  no  |  |
 | header | String |  no  |  |
 | imageMeta | [MediaMetaRequest](#MediaMetaRequest) |  no  |  |
 | isVoteAllowed | Boolean |  no  |  |
 | title | String |  no  |  |
 | videoMeta | [MediaMetaRequest](#MediaMetaRequest) |  no  |  |

---


 
 
 #### [SaveAttributeRequest](#SaveAttributeRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | name | String |  no  |  |
 | slug | String |  no  |  |

---


 
 
 #### [SortMethod](#SortMethod)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | selected | Boolean? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [TagMeta](#TagMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | media | ArrayList<[MediaMeta](#MediaMeta)>? |  yes  |  |
 | name | String? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [Template](#Template)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | entity | [Entity](#Entity)? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | rating | [Rating](#Rating)? |  yes  |  |
 | review | [Review](#Review)? |  yes  |  |
 | state | [FeedbackState](#FeedbackState)? |  yes  |  |
 | tags | ArrayList<[TagMeta](#TagMeta)>? |  yes  |  |

---


 
 
 #### [TemplateGetResponse](#TemplateGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Template](#Template)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [TemplateRequest](#TemplateRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean |  no  |  |
 | enableMediaType | String? |  yes  | image | video | any |
 | enableQna | Boolean? |  yes  |  |
 | enableRating | Boolean |  no  |  |
 | enableReview | Boolean |  no  |  |
 | entity | [EntityRequest](#EntityRequest) |  no  |  |
 | rating | [RatingRequest](#RatingRequest) |  no  |  |
 | review | [ReviewRequest](#ReviewRequest) |  no  |  |

---


 
 
 #### [TemplateRequestList](#TemplateRequestList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | templateList | ArrayList<[TemplateRequest](#TemplateRequest)> |  no  |  |

---


 
 
 #### [UI](#UI)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | feedbackQuestion | ArrayList<String>? |  yes  |  |
 | icon | [UIIcon](#UIIcon)? |  yes  |  |
 | text | ArrayList<String>? |  yes  |  |
 | type | String? |  yes  | star | images | gifs | smileys |

---


 
 
 #### [UIIcon](#UIIcon)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | String? |  yes  |  |
 | inactive | String? |  yes  |  |
 | selected | ArrayList<String>? |  yes  |  |

---


 
 
 #### [UpdateAttributeRequest](#UpdateAttributeRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | name | String |  no  |  |
 | slug | String? |  yes  |  |

---


 
 
 #### [UpdateResponse](#UpdateResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | count | Int? |  yes  |  |

---


 
 
 #### [UpdateReviewRequest](#UpdateReviewRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  |  |
 | application | String? |  yes  |  |
 | approve | Boolean? |  yes  |  |
 | archive | Boolean? |  yes  |  |
 | attributesRating | ArrayList<[AttributeObject](#AttributeObject)>? |  yes  |  |
 | description | String? |  yes  |  |
 | deviceMeta | [DeviceMeta](#DeviceMeta)? |  yes  |  |
 | entityId | String? |  yes  |  |
 | entityType | String? |  yes  |  |
 | mediaResource | ArrayList<[MediaMeta](#MediaMeta)>? |  yes  |  |
 | rating | Double? |  yes  |  |
 | reviewId | String? |  yes  |  |
 | templateId | String? |  yes  |  |
 | title | String? |  yes  |  |

---


 
 
 #### [UpdateTemplateRequest](#UpdateTemplateRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean |  no  |  |
 | enableMediaType | String? |  yes  | image | video | any |
 | enableQna | Boolean? |  yes  |  |
 | enableRating | Boolean |  no  |  |
 | enableReview | Boolean |  no  |  |
 | entity | [EntityRequest](#EntityRequest) |  no  |  |
 | rating | [RatingRequest](#RatingRequest) |  no  |  |
 | review | [ReviewRequest](#ReviewRequest) |  no  |  |

---


 
 
 #### [UpdateTemplateStatusRequest](#UpdateTemplateStatusRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  |  |
 | archive | Boolean? |  yes  |  |

---




 
 
 #### [AvailablePageSchema](#AvailablePageSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | String? |  yes  |  |
 | text | String? |  yes  |  |
 | path | String? |  yes  |  |
 | type | String? |  yes  |  |
 | sections | ArrayList<[AvailablePageSchemaSections](#AvailablePageSchemaSections)>? |  yes  |  |
 | sectionsMeta | ArrayList<[AvailablePageSectionMetaAttributes](#AvailablePageSectionMetaAttributes)>? |  yes  |  |
 | theme | String? |  yes  |  |
 | seo | [AvailablePageSeo](#AvailablePageSeo)? |  yes  |  |
 | props | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | id | String? |  yes  |  |

---


 
 
 #### [AvailablePageSectionMetaAttributes](#AvailablePageSectionMetaAttributes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | attributes | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [AvailablePageSeo](#AvailablePageSeo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | description | String? |  yes  |  |
 | id | String? |  yes  |  |

---


 
 
 #### [AvailablePageSchemaSections](#AvailablePageSchemaSections)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | label | String? |  yes  |  |
 | props | HashMap<String,Any>? |  yes  |  |
 | blocks | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | preset | HashMap<String,Any>? |  yes  |  |
 | predicate | [AvailablePagePredicate](#AvailablePagePredicate)? |  yes  |  |

---


 
 
 #### [AvailablePageScreenPredicate](#AvailablePageScreenPredicate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | mobile | Boolean? |  yes  |  |
 | desktop | Boolean? |  yes  |  |
 | tablet | Boolean? |  yes  |  |

---


 
 
 #### [AvailablePageUserPredicate](#AvailablePageUserPredicate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | authenticated | Boolean? |  yes  |  |
 | anonymous | Boolean? |  yes  |  |

---


 
 
 #### [AvailablePageRoutePredicate](#AvailablePageRoutePredicate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | selected | String? |  yes  |  |
 | exactUrl | String? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [AvailablePagePredicate](#AvailablePagePredicate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | screen | [AvailablePageScreenPredicate](#AvailablePageScreenPredicate)? |  yes  |  |
 | user | [AvailablePageUserPredicate](#AvailablePageUserPredicate)? |  yes  |  |
 | route | [AvailablePageRoutePredicate](#AvailablePageRoutePredicate)? |  yes  |  |

---


 
 
 #### [AllAvailablePageSchema](#AllAvailablePageSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pages | ArrayList<[AvailablePageSchema](#AvailablePageSchema)>? |  yes  |  |

---


 
 
 #### [PaginationSchema](#PaginationSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | size | Int? |  yes  |  |
 | itemTotal | Int? |  yes  |  |
 | hasNext | Boolean? |  yes  |  |
 | type | String? |  yes  |  |
 | current | Int? |  yes  |  |

---


 
 
 #### [ThemesListingResponseSchema](#ThemesListingResponseSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[ThemesSchema](#ThemesSchema)>? |  yes  |  |
 | page | [PaginationSchema](#PaginationSchema)? |  yes  |  |

---


 
 
 #### [AddThemeRequestSchema](#AddThemeRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | themeId | String? |  yes  |  |

---


 
 
 #### [UpgradableThemeSchema](#UpgradableThemeSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | parentTheme | String? |  yes  |  |
 | appliedTheme | String? |  yes  |  |
 | upgrade | Boolean? |  yes  |  |

---


 
 
 #### [FontsSchema](#FontsSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | [FontsSchemaItems](#FontsSchemaItems)? |  yes  |  |
 | kind | String? |  yes  |  |

---


 
 
 #### [BlitzkriegApiErrorSchema](#BlitzkriegApiErrorSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [BlitzkriegNotFoundSchema](#BlitzkriegNotFoundSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [BlitzkriegInternalServerErrorSchema](#BlitzkriegInternalServerErrorSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [FontsSchemaItems](#FontsSchemaItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | family | String? |  yes  |  |
 | variants | ArrayList<String>? |  yes  |  |
 | subsets | ArrayList<String>? |  yes  |  |
 | version | String? |  yes  |  |
 | lastModified | String? |  yes  |  |
 | files | [FontsSchemaItemsFiles](#FontsSchemaItemsFiles)? |  yes  |  |
 | category | String? |  yes  |  |
 | kind | String? |  yes  |  |

---


 
 
 #### [FontsSchemaItemsFiles](#FontsSchemaItemsFiles)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | regular | String? |  yes  |  |
 | italic | String? |  yes  |  |
 | bold | String? |  yes  |  |

---


 
 
 #### [ThemesSchema](#ThemesSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | application | String? |  yes  |  |
 | applied | Boolean? |  yes  |  |
 | customized | Boolean? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | archived | Boolean? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | version | String? |  yes  |  |
 | parentThemeVersion | String? |  yes  |  |
 | parentTheme | String? |  yes  |  |
 | information | [Information](#Information)? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | src | [Src](#Src)? |  yes  |  |
 | assets | [AssetsSchema](#AssetsSchema)? |  yes  |  |
 | availableSections | ArrayList<[availableSectionSchema](#availableSectionSchema)>? |  yes  |  |
 | constants | HashMap<String,Any>? |  yes  |  |
 | styles | HashMap<String,Any>? |  yes  |  |
 | config | [Config](#Config)? |  yes  |  |
 | settings | HashMap<String,Any>? |  yes  |  |
 | font | [Font](#Font)? |  yes  |  |
 | id | String? |  yes  |  |
 | v | Int? |  yes  |  |
 | colors | [Colors](#Colors)? |  yes  |  |

---


 
 
 #### [availableSectionSchema](#availableSectionSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | blocks | ArrayList<[Blocks](#Blocks)>? |  yes  |  |
 | name | String? |  yes  |  |
 | label | String? |  yes  |  |
 | props | ArrayList<[BlocksProps](#BlocksProps)>? |  yes  |  |

---


 
 
 #### [Information](#Information)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | images | [Images](#Images)? |  yes  |  |
 | features | ArrayList<String>? |  yes  |  |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |

---


 
 
 #### [Images](#Images)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | desktop | ArrayList<String>? |  yes  |  |
 | android | ArrayList<String>? |  yes  |  |
 | ios | ArrayList<String>? |  yes  |  |
 | thumbnail | ArrayList<String>? |  yes  |  |

---


 
 
 #### [Src](#Src)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | link | String? |  yes  |  |

---


 
 
 #### [AssetsSchema](#AssetsSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | umdJs | [UmdJs](#UmdJs)? |  yes  |  |
 | commonJs | [CommonJs](#CommonJs)? |  yes  |  |
 | css | [Css](#Css)? |  yes  |  |

---


 
 
 #### [UmdJs](#UmdJs)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | link | String? |  yes  |  |

---


 
 
 #### [CommonJs](#CommonJs)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | link | String? |  yes  |  |

---


 
 
 #### [Css](#Css)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | link | String? |  yes  |  |

---


 
 
 #### [Seo](#Seo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | description | String? |  yes  |  |

---


 
 
 #### [Sections](#Sections)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | attributes | String? |  yes  |  |

---


 
 
 #### [Config](#Config)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | preset | [Preset](#Preset)? |  yes  |  |
 | globalSchema | [GlobalSchema](#GlobalSchema)? |  yes  |  |
 | current | String? |  yes  |  |
 | list | ArrayList<[ListSchemaItem](#ListSchemaItem)>? |  yes  |  |

---


 
 
 #### [Preset](#Preset)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pages | ArrayList<[AvailablePageSchema](#AvailablePageSchema)>? |  yes  |  |

---


 
 
 #### [GlobalSchema](#GlobalSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | props | ArrayList<[GlobalSchemaProps](#GlobalSchemaProps)>? |  yes  |  |

---


 
 
 #### [ListSchemaItem](#ListSchemaItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | global | HashMap<String,Any>? |  yes  |  |
 | page | ArrayList<[ConfigPage](#ConfigPage)>? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [Colors](#Colors)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | bgColor | String? |  yes  |  |
 | primaryColor | String? |  yes  |  |
 | secondaryColor | String? |  yes  |  |
 | accentColor | String? |  yes  |  |
 | linkColor | String? |  yes  |  |
 | buttonSecondaryColor | String? |  yes  |  |

---


 
 
 #### [Custom](#Custom)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | props | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [ConfigPage](#ConfigPage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | settings | HashMap<String,Any>? |  yes  |  |
 | page | String? |  yes  |  |

---


 
 
 #### [Font](#Font)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | family | String? |  yes  |  |
 | variants | [Variants](#Variants)? |  yes  |  |

---


 
 
 #### [Variants](#Variants)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | medium | [Medium](#Medium)? |  yes  |  |
 | semiBold | [SemiBold](#SemiBold)? |  yes  |  |
 | bold | [Bold](#Bold)? |  yes  |  |
 | light | [Light](#Light)? |  yes  |  |
 | regular | [Regular](#Regular)? |  yes  |  |

---


 
 
 #### [Medium](#Medium)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | file | String? |  yes  |  |

---


 
 
 #### [SemiBold](#SemiBold)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | file | String? |  yes  |  |

---


 
 
 #### [Bold](#Bold)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | file | String? |  yes  |  |

---


 
 
 #### [Light](#Light)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | file | String? |  yes  |  |

---


 
 
 #### [Regular](#Regular)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | file | String? |  yes  |  |

---


 
 
 #### [Blocks](#Blocks)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | name | String? |  yes  |  |
 | props | ArrayList<[BlocksProps](#BlocksProps)>? |  yes  |  |

---


 
 
 #### [GlobalSchemaProps](#GlobalSchemaProps)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | label | String? |  yes  |  |
 | type | String? |  yes  |  |
 | category | String? |  yes  |  |

---


 
 
 #### [BlocksProps](#BlocksProps)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | label | String? |  yes  |  |
 | type | String? |  yes  |  |

---




 
 
 #### [EditEmailRequestSchema](#EditEmailRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | String? |  yes  |  |

---


 
 
 #### [SendVerificationLinkMobileRequestSchema](#SendVerificationLinkMobileRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | verified | Boolean? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | phone | String? |  yes  |  |
 | primary | Boolean? |  yes  |  |

---


 
 
 #### [EditMobileRequestSchema](#EditMobileRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | countryCode | String? |  yes  |  |
 | phone | String? |  yes  |  |

---


 
 
 #### [EditProfileRequestSchema](#EditProfileRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | firstName | String? |  yes  |  |
 | lastName | String? |  yes  |  |
 | mobile | [EditProfileMobileSchema](#EditProfileMobileSchema)? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | email | String? |  yes  |  |
 | gender | String? |  yes  |  |
 | dob | String? |  yes  |  |
 | profilePicUrl | String? |  yes  |  |
 | androidHash | String? |  yes  |  |
 | sender | String? |  yes  |  |
 | registerToken | String? |  yes  |  |

---


 
 
 #### [EditProfileMobileSchema](#EditProfileMobileSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | phone | String? |  yes  |  |
 | countryCode | String? |  yes  |  |

---


 
 
 #### [SendEmailOtpRequestSchema](#SendEmailOtpRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | String? |  yes  |  |
 | action | String? |  yes  |  |
 | token | String? |  yes  |  |
 | registerToken | String? |  yes  |  |

---


 
 
 #### [VerifyEmailOtpRequestSchema](#VerifyEmailOtpRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | String? |  yes  |  |
 | action | String? |  yes  |  |
 | registerToken | String? |  yes  |  |
 | otp | String? |  yes  |  |

---


 
 
 #### [VerifyOtpRequestSchema](#VerifyOtpRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | requestId | String? |  yes  |  |
 | registerToken | String? |  yes  |  |
 | otp | String? |  yes  |  |

---


 
 
 #### [SendMobileOtpRequestSchema](#SendMobileOtpRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | mobile | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | action | String? |  yes  |  |
 | token | String? |  yes  |  |
 | androidHash | String? |  yes  |  |
 | force | String? |  yes  |  |
 | captchaCode | String? |  yes  |  |

---


 
 
 #### [UpdatePasswordRequestSchema](#UpdatePasswordRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | oldPassword | String? |  yes  |  |
 | newPassword | String? |  yes  |  |

---


 
 
 #### [FormRegisterRequestSchema](#FormRegisterRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | firstName | String? |  yes  |  |
 | lastName | String? |  yes  |  |
 | gender | String? |  yes  |  |
 | email | String? |  yes  |  |
 | password | String? |  yes  |  |
 | phone | [FormRegisterRequestSchemaPhone](#FormRegisterRequestSchemaPhone)? |  yes  |  |
 | registerToken | String? |  yes  |  |

---


 
 
 #### [TokenRequestBodySchema](#TokenRequestBodySchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | token | String? |  yes  |  |

---


 
 
 #### [ForgotPasswordRequestSchema](#ForgotPasswordRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | code | String? |  yes  |  |
 | password | String? |  yes  |  |

---


 
 
 #### [CodeRequestBodySchema](#CodeRequestBodySchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | code | String? |  yes  |  |

---


 
 
 #### [SendResetPasswordEmailRequestSchema](#SendResetPasswordEmailRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | String? |  yes  |  |
 | captchaCode | String? |  yes  |  |

---


 
 
 #### [PasswordLoginRequestSchema](#PasswordLoginRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | captchaCode | String? |  yes  |  |
 | password | String? |  yes  |  |
 | username | String? |  yes  |  |

---


 
 
 #### [SendOtpRequestSchema](#SendOtpRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | countryCode | String? |  yes  |  |
 | captchaCode | String? |  yes  |  |
 | mobile | String? |  yes  |  |

---


 
 
 #### [OAuthRequestSchema](#OAuthRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isSignedIn | Boolean? |  yes  |  |
 | oauth2 | [OAuthRequestSchemaOauth2](#OAuthRequestSchemaOauth2)? |  yes  |  |
 | profile | [OAuthRequestSchemaProfile](#OAuthRequestSchemaProfile)? |  yes  |  |

---


 
 
 #### [UserObjectSchema](#UserObjectSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  |  |

---


 
 
 #### [AuthSuccess](#AuthSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | registerToken | String? |  yes  |  |
 | userExists | Boolean? |  yes  |  |
 | user | [UserSchema](#UserSchema)? |  yes  |  |

---


 
 
 #### [SendOtpResponse](#SendOtpResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | resendTimer | Int? |  yes  |  |
 | resendToken | String? |  yes  |  |
 | success | Boolean? |  yes  |  |
 | requestId | String? |  yes  |  |
 | message | String? |  yes  |  |
 | mobile | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | email | String? |  yes  |  |
 | resendEmailToken | String? |  yes  |  |
 | registerToken | String? |  yes  |  |
 | verifyEmailOtp | Boolean? |  yes  |  |
 | verifyMobileOtp | Boolean? |  yes  |  |
 | userExists | Boolean? |  yes  |  |

---


 
 
 #### [ProfileEditSuccess](#ProfileEditSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  |  |
 | registerToken | String? |  yes  |  |
 | userExists | Boolean? |  yes  |  |
 | verifyEmailLink | Boolean? |  yes  |  |
 | verifyEmailOtp | Boolean? |  yes  |  |
 | verifyMobileOtp | Boolean? |  yes  |  |
 | email | String? |  yes  |  |

---


 
 
 #### [LoginSuccess](#LoginSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  |  |
 | requestId | String? |  yes  |  |
 | registerToken | String? |  yes  |  |

---


 
 
 #### [VerifyOtpSuccess](#VerifyOtpSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  |  |
 | userExists | Boolean? |  yes  |  |
 | registerToken | String? |  yes  |  |

---


 
 
 #### [ResetPasswordSuccess](#ResetPasswordSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | String? |  yes  |  |

---


 
 
 #### [RegisterFormSuccess](#RegisterFormSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | String? |  yes  |  |
 | resendTimer | Int? |  yes  |  |
 | resendToken | String? |  yes  |  |
 | resendEmailToken | String? |  yes  |  |
 | registerToken | String? |  yes  |  |
 | success | Boolean? |  yes  |  |
 | requestId | String? |  yes  |  |
 | message | String? |  yes  |  |
 | mobile | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | verifyEmailOtp | Boolean? |  yes  |  |
 | verifyMobileOtp | Boolean? |  yes  |  |
 | userExists | Boolean? |  yes  |  |

---


 
 
 #### [VerifyEmailSuccess](#VerifyEmailSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [HasPasswordSuccess](#HasPasswordSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | result | Boolean? |  yes  |  |

---


 
 
 #### [LogoutSuccess](#LogoutSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | logout | Boolean? |  yes  |  |

---


 
 
 #### [OtpSuccess](#OtpSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | resendTimer | Int? |  yes  |  |
 | resendToken | String? |  yes  |  |
 | registerToken | String? |  yes  |  |
 | success | Boolean? |  yes  |  |
 | requestId | String? |  yes  |  |
 | message | String? |  yes  |  |
 | mobile | String? |  yes  |  |
 | countryCode | String? |  yes  |  |

---


 
 
 #### [EmailOtpSuccess](#EmailOtpSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |

---


 
 
 #### [SessionListSuccess](#SessionListSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sessions | ArrayList<String>? |  yes  |  |

---


 
 
 #### [VerifyMobileOTPSuccess](#VerifyMobileOTPSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  |  |
 | verifyMobileLink | Boolean? |  yes  |  |

---


 
 
 #### [VerifyEmailOTPSuccess](#VerifyEmailOTPSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  |  |
 | verifyEmailLink | Boolean? |  yes  |  |

---


 
 
 #### [SendMobileVerifyLinkSuccess](#SendMobileVerifyLinkSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | verifyMobileLink | Boolean? |  yes  |  |

---


 
 
 #### [SendEmailVerifyLinkSuccess](#SendEmailVerifyLinkSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | verifyEmailLink | Boolean? |  yes  |  |

---


 
 
 #### [UserSearchResponseSchema](#UserSearchResponseSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | users | ArrayList<[UserSchema](#UserSchema)>? |  yes  |  |

---


 
 
 #### [CustomerListResponseSchema](#CustomerListResponseSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[UserSchema](#UserSchema)>? |  yes  |  |
 | page | [PaginationSchema](#PaginationSchema)? |  yes  |  |

---


 
 
 #### [UnauthorizedSchema](#UnauthorizedSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [UnauthenticatedSchema](#UnauthenticatedSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | authenticated | Boolean? |  yes  |  |

---


 
 
 #### [NotFoundSchema](#NotFoundSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [AuthenticationInternalServerErrorSchema](#AuthenticationInternalServerErrorSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [AuthenticationApiErrorSchema](#AuthenticationApiErrorSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [ProfileEditSuccessSchema](#ProfileEditSuccessSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | String? |  yes  |  |
 | verifyEmailOtp | Boolean? |  yes  |  |
 | verifyEmailLink | Boolean? |  yes  |  |
 | verifyMobileOtp | Boolean? |  yes  |  |
 | user | String? |  yes  |  |
 | registerToken | String? |  yes  |  |
 | userExists | Boolean? |  yes  |  |

---


 
 
 #### [FormRegisterRequestSchemaPhone](#FormRegisterRequestSchemaPhone)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | countryCode | String? |  yes  |  |
 | mobile | String? |  yes  |  |

---


 
 
 #### [OAuthRequestSchemaOauth2](#OAuthRequestSchemaOauth2)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | accessToken | String? |  yes  |  |
 | expiry | Int? |  yes  |  |
 | refreshToken | String? |  yes  |  |

---


 
 
 #### [OAuthRequestSchemaProfile](#OAuthRequestSchemaProfile)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | lastName | String? |  yes  |  |
 | image | String? |  yes  |  |
 | id | String? |  yes  |  |
 | email | String? |  yes  |  |
 | fullName | String? |  yes  |  |
 | firstName | String? |  yes  |  |

---


 
 
 #### [AuthSuccessUser](#AuthSuccessUser)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | firstName | String? |  yes  |  |
 | lastName | String? |  yes  |  |
 | debug | [AuthSuccessUserDebug](#AuthSuccessUserDebug)? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | emails | [AuthSuccessUserEmails](#AuthSuccessUserEmails)? |  yes  |  |

---


 
 
 #### [AuthSuccessUserDebug](#AuthSuccessUserDebug)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | platform | String? |  yes  |  |

---


 
 
 #### [AuthSuccessUserEmails](#AuthSuccessUserEmails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | String? |  yes  |  |
 | verified | Boolean? |  yes  |  |
 | primary | Boolean? |  yes  |  |
 | active | Boolean? |  yes  |  |

---


 
 
 #### [CreateUserRequestSchema](#CreateUserRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | phoneNumber | String |  no  |  |
 | email | String? |  yes  |  |
 | firstName | String? |  yes  |  |
 | lastName | String? |  yes  |  |
 | gender | String? |  yes  |  |
 | username | String |  no  |  |
 | meta | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [CreateUserResponseSchema](#CreateUserResponseSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  |  |

---


 
 
 #### [CreateUserSessionRequestSchema](#CreateUserSessionRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | domain | String? |  yes  |  |
 | maxAge | Double? |  yes  |  |
 | userId | String? |  yes  |  |

---


 
 
 #### [CreateUserSessionResponseSchema](#CreateUserSessionResponseSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | domain | String? |  yes  |  |
 | maxAge | Double? |  yes  |  |
 | secure | Boolean? |  yes  |  |
 | httpOnly | Boolean? |  yes  |  |
 | cookie | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [PlatformSchema](#PlatformSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | lookAndFeel | [LookAndFeel](#LookAndFeel)? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | forgotPassword | Boolean? |  yes  |  |
 | login | [Login](#Login)? |  yes  |  |
 | skipCaptcha | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | meta | [MetaSchema](#MetaSchema)? |  yes  |  |
 | id | String? |  yes  |  |
 | social | [Social](#Social)? |  yes  |  |
 | requiredFields | [RequiredFields](#RequiredFields)? |  yes  |  |
 | registerRequiredFields | [RegisterRequiredFields](#RegisterRequiredFields)? |  yes  |  |
 | skipLogin | Boolean? |  yes  |  |
 | flashCard | [FlashCard](#FlashCard)? |  yes  |  |
 | subtext | String? |  yes  |  |
 | socialTokens | [SocialTokens](#SocialTokens)? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | register | Boolean? |  yes  |  |
 | mobileImage | String? |  yes  |  |
 | desktopImage | String? |  yes  |  |

---


 
 
 #### [LookAndFeel](#LookAndFeel)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cardPosition | String? |  yes  |  |
 | backgroundColor | String? |  yes  |  |

---


 
 
 #### [Login](#Login)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | password | Boolean? |  yes  |  |
 | otp | Boolean? |  yes  |  |

---


 
 
 #### [MetaSchema](#MetaSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | fyndDefault | Boolean? |  yes  |  |

---


 
 
 #### [Social](#Social)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | accountKit | Boolean? |  yes  |  |
 | facebook | Boolean? |  yes  |  |
 | google | Boolean? |  yes  |  |

---


 
 
 #### [RequiredFields](#RequiredFields)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | [PlatformEmail](#PlatformEmail)? |  yes  |  |
 | mobile | [PlatformMobile](#PlatformMobile)? |  yes  |  |

---


 
 
 #### [PlatformEmail](#PlatformEmail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isRequired | Boolean? |  yes  |  |
 | level | String? |  yes  |  |

---


 
 
 #### [PlatformMobile](#PlatformMobile)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isRequired | Boolean? |  yes  |  |
 | level | String? |  yes  |  |

---


 
 
 #### [RegisterRequiredFields](#RegisterRequiredFields)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | [RegisterRequiredFieldsEmail](#RegisterRequiredFieldsEmail)? |  yes  |  |
 | mobile | [RegisterRequiredFieldsMobile](#RegisterRequiredFieldsMobile)? |  yes  |  |

---


 
 
 #### [RegisterRequiredFieldsEmail](#RegisterRequiredFieldsEmail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isRequired | Boolean? |  yes  |  |
 | level | String? |  yes  |  |

---


 
 
 #### [RegisterRequiredFieldsMobile](#RegisterRequiredFieldsMobile)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isRequired | Boolean? |  yes  |  |
 | level | String? |  yes  |  |

---


 
 
 #### [FlashCard](#FlashCard)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | text | String? |  yes  |  |
 | textColor | String? |  yes  |  |
 | backgroundColor | String? |  yes  |  |

---


 
 
 #### [SocialTokens](#SocialTokens)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | facebook | [Facebook](#Facebook)? |  yes  |  |
 | accountKit | [Accountkit](#Accountkit)? |  yes  |  |
 | google | [Google](#Google)? |  yes  |  |

---


 
 
 #### [Facebook](#Facebook)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | appId | String? |  yes  |  |

---


 
 
 #### [Accountkit](#Accountkit)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | appId | String? |  yes  |  |

---


 
 
 #### [Google](#Google)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | appId | String? |  yes  |  |

---


 
 
 #### [UpdateUserRequestSchema](#UpdateUserRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | firstName | String? |  yes  |  |
 | lastName | String? |  yes  |  |
 | gender | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [UserSchema](#UserSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | firstName | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | lastName | String? |  yes  |  |
 | phoneNumbers | ArrayList<[PhoneNumber](#PhoneNumber)>? |  yes  |  |
 | emails | ArrayList<[Email](#Email)>? |  yes  |  |
 | gender | String? |  yes  |  |
 | dob | String? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | profilePicUrl | String? |  yes  |  |
 | username | String? |  yes  |  |
 | accountType | String? |  yes  |  |
 | uid | String? |  yes  |  |
 | debug | [Debug](#Debug)? |  yes  |  |
 | hasOldPasswordHash | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |

---




 
 
 #### [ApplicationLegal](#ApplicationLegal)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | application | String? |  yes  |  |
 | tnc | String? |  yes  |  |
 | policy | String? |  yes  |  |
 | shipping | String? |  yes  |  |
 | faq | ArrayList<[ApplicationLegalFAQ](#ApplicationLegalFAQ)>? |  yes  |  |
 | id | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | createdAt | String? |  yes  |  |

---


 
 
 #### [ApplicationLegalFAQ](#ApplicationLegalFAQ)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | question | String? |  yes  |  |
 | answer | String? |  yes  |  |

---


 
 
 #### [SeoComponent](#SeoComponent)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | seo | [SeoSchema](#SeoSchema)? |  yes  |  |

---


 
 
 #### [SeoSchema](#SeoSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | app | String? |  yes  |  |
 | id | String? |  yes  |  |
 | robotsTxt | String? |  yes  |  |
 | sitemapEnabled | Boolean? |  yes  |  |
 | customMetaTags | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | details | [Detail](#Detail)? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |

---


 
 
 #### [CustomMetaTag](#CustomMetaTag)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | content | String? |  yes  |  |
 | id | String? |  yes  |  |

---


 
 
 #### [Detail](#Detail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | description | String? |  yes  |  |

---


 
 
 #### [AnnouncementPageSchema](#AnnouncementPageSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pageSlug | String? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [EditorMeta](#EditorMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | foregroundColor | String? |  yes  |  |
 | backgroundColor | String? |  yes  |  |
 | contentType | String? |  yes  |  |
 | content | String? |  yes  |  |

---


 
 
 #### [AnnouncementAuthorSchema](#AnnouncementAuthorSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | createdBy | String? |  yes  |  |
 | modifiedBy | String? |  yes  |  |

---


 
 
 #### [AdminAnnouncementSchema](#AdminAnnouncementSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | platforms | ArrayList<String>? |  yes  |  |
 | title | String? |  yes  |  |
 | announcement | String? |  yes  |  |
 | pages | ArrayList<[AnnouncementPageSchema](#AnnouncementPageSchema)>? |  yes  |  |
 | editorMeta | [EditorMeta](#EditorMeta)? |  yes  |  |
 | author | [AnnouncementAuthorSchema](#AnnouncementAuthorSchema)? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | app | String? |  yes  |  |
 | modifiedAt | String? |  yes  |  |
 | schedule | [ScheduleSchema](#ScheduleSchema)? |  yes  |  |

---


 
 
 #### [ScheduleSchema](#ScheduleSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cron | String? |  yes  |  |
 | start | String? |  yes  |  |
 | end | String? |  yes  |  |
 | duration | Double? |  yes  |  |
 | nextSchedule | ArrayList<HashMap<String,Any>>? |  yes  |  |

---


 
 
 #### [NextSchedule](#NextSchedule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | start | String? |  yes  |  |
 | end | String? |  yes  |  |

---


 
 
 #### [AnnouncementSchema](#AnnouncementSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | announcement | String? |  yes  |  |
 | schedule | [ScheduleStartSchema](#ScheduleStartSchema)? |  yes  |  |

---


 
 
 #### [ScheduleStartSchema](#ScheduleStartSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | start | String? |  yes  |  |
 | end | String? |  yes  |  |

---


 
 
 #### [BlogGetResponse](#BlogGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[BlogSchema](#BlogSchema)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [ResourceContent](#ResourceContent)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [Asset](#Asset)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | aspectRatio | String? |  yes  |  |
 | id | String? |  yes  |  |
 | secureUrl | String? |  yes  |  |

---


 
 
 #### [Author](#Author)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | designation | String? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [BlogSchema](#BlogSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | application | String? |  yes  |  |
 | archived | Boolean? |  yes  |  |
 | author | [Author](#Author)? |  yes  |  |
 | content | ArrayList<[ResourceContent](#ResourceContent)>? |  yes  |  |
 | featureImage | [Asset](#Asset)? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | readingTime | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | seo | [SEO](#SEO)? |  yes  |  |
 | schedule | [CronSchedule](#CronSchedule)? |  yes  |  |
 | title | String? |  yes  |  |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |

---


 
 
 #### [SEO](#SEO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | image | [SEOImage](#SEOImage)? |  yes  |  |
 | title | String? |  yes  |  |

---


 
 
 #### [SEOImage](#SEOImage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | url | String? |  yes  |  |

---


 
 
 #### [BlogRequest](#BlogRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | application | String? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | author | [Author](#Author)? |  yes  |  |
 | content | ArrayList<[ResourceContent](#ResourceContent)>? |  yes  |  |
 | featureImage | [Asset](#Asset)? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | readingTime | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | title | String? |  yes  |  |
 | seo | [SEO](#SEO)? |  yes  |  |
 | schedule | [CronSchedule](#CronSchedule)? |  yes  |  |

---


 
 
 #### [GetAnnouncementListSchema](#GetAnnouncementListSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[AdminAnnouncementSchema](#AdminAnnouncementSchema)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [CreateAnnouncementSchema](#CreateAnnouncementSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |
 | data | [AdminAnnouncementSchema](#AdminAnnouncementSchema)? |  yes  |  |

---


 
 
 #### [Navigation](#Navigation)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | orientation | String? |  yes  |  |
 | createdBy | [CreatedBySchema](#CreatedBySchema)? |  yes  |  |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | id | String? |  yes  |  |
 | position | String? |  yes  |  |
 | application | String? |  yes  |  |
 | platform | String? |  yes  |  |
 | navigation | [NavigationReference](#NavigationReference)? |  yes  |  |

---


 
 
 #### [LocaleLanguage](#LocaleLanguage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | hi | [Language](#Language)? |  yes  |  |
 | ar | [Language](#Language)? |  yes  |  |
 | enUs | [Language](#Language)? |  yes  |  |

---


 
 
 #### [Language](#Language)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |

---


 
 
 #### [Action](#Action)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [ActionPage](#ActionPage)? |  yes  |  |
 | popup | [ActionPage](#ActionPage)? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [ActionPage](#ActionPage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | params | HashMap<String,ArrayList<String>>? |  yes  |  |
 | query | HashMap<String,ArrayList<String>>? |  yes  |  |
 | url | String? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [NavigationReference](#NavigationReference)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | acl | ArrayList<String>? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | localeLanguage | [LocaleLanguage](#LocaleLanguage)? |  yes  |  |
 | image | String? |  yes  |  |
 | type | String? |  yes  |  |
 | action | [Action](#Action)? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | display | String? |  yes  |  |
 | sortOrder | Int? |  yes  |  |
 | subNavigation | ArrayList<[NavigationReference](#NavigationReference)>? |  yes  |  |

---


 
 
 #### [LandingPage](#LandingPage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [LandingPageSchema](#LandingPageSchema)? |  yes  |  |
 | success | Boolean? |  yes  |  |

---


 
 
 #### [ConfigurationSchema](#ConfigurationSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sleepTime | Int? |  yes  |  |
 | startOnLaunch | Boolean? |  yes  |  |
 | duration | Int? |  yes  |  |
 | slideDirection | String? |  yes  |  |

---


 
 
 #### [SlideshowMedia](#SlideshowMedia)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | url | String? |  yes  |  |
 | bgColor | String? |  yes  |  |
 | duration | Int? |  yes  |  |
 | autoDecideDuration | Boolean? |  yes  |  |
 | action | [Action](#Action)? |  yes  |  |

---


 
 
 #### [Slideshow](#Slideshow)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [SlideshowSchema](#SlideshowSchema)? |  yes  |  |
 | success | Boolean? |  yes  |  |

---


 
 
 #### [AnnouncementsResponseSchema](#AnnouncementsResponseSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | announcements | HashMap<String,ArrayList<[AnnouncementSchema](#AnnouncementSchema)>>? |  yes  |  |
 | refreshRate | Int? |  yes  | number of seconds after which api should hit again to fetch new announcements |
 | refreshPages | ArrayList<String>? |  yes  | list of page slugs on which announcement should be fetched as soon as they are loaded |

---


 
 
 #### [FaqResponseSchema](#FaqResponseSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | faqs | ArrayList<[FaqSchema](#FaqSchema)>? |  yes  |  |

---


 
 
 #### [UpdateHandpickedSchema](#UpdateHandpickedSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tag | [HandpickedTagSchema](#HandpickedTagSchema)? |  yes  |  |

---


 
 
 #### [HandpickedTagSchema](#HandpickedTagSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | position | String? |  yes  |  |
 | attributes | HashMap<String,Any>? |  yes  |  |
 | name | String? |  yes  |  |
 | url | String? |  yes  |  |
 | type | String? |  yes  |  |
 | subType | String? |  yes  |  |
 | content | String? |  yes  |  |

---


 
 
 #### [RemoveHandpickedSchema](#RemoveHandpickedSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tags | ArrayList<String>? |  yes  |  |

---


 
 
 #### [CreateTagSchema](#CreateTagSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | subType | String? |  yes  |  |
 | id | String? |  yes  |  |
 | type | String? |  yes  |  |
 | url | String? |  yes  |  |
 | position | String? |  yes  |  |
 | attributes | HashMap<String,Any>? |  yes  |  |
 | content | String? |  yes  |  |

---


 
 
 #### [CreateTagRequestSchema](#CreateTagRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tags | ArrayList<[CreateTagSchema](#CreateTagSchema)>? |  yes  |  |

---


 
 
 #### [TagDeleteSuccessResponse](#TagDeleteSuccessResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |

---


 
 
 #### [APIError](#APIError)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |
 | status | Double? |  yes  |  |
 | code | String? |  yes  |  |
 | exception | String? |  yes  |  |
 | info | String? |  yes  |  |
 | requestId | String? |  yes  |  |
 | stackTrace | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [CategorySchema](#CategorySchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | index | Int? |  yes  |  |
 | title | String? |  yes  |  |
 | description | String? |  yes  |  |
 | children | ArrayList<String>? |  yes  |  |
 | id | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | application | String? |  yes  |  |
 | iconUrl | String? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [ChildrenSchema](#ChildrenSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | question | String? |  yes  |  |
 | answer | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | application | String? |  yes  |  |
 | id | String? |  yes  |  |

---


 
 
 #### [CategoryRequestSchema](#CategoryRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | slug | String? |  yes  |  |
 | title | String? |  yes  |  |

---


 
 
 #### [FAQCategorySchema](#FAQCategorySchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | index | Int? |  yes  |  |
 | title | String? |  yes  |  |
 | description | String? |  yes  |  |
 | children | ArrayList<[ChildrenSchema](#ChildrenSchema)>? |  yes  |  |
 | id | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | application | String? |  yes  |  |
 | iconUrl | String? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [FaqSchema](#FaqSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | slug | String? |  yes  |  |
 | application | String? |  yes  |  |
 | id | String? |  yes  |  |
 | question | String? |  yes  |  |
 | answer | String? |  yes  |  |

---


 
 
 #### [FAQ](#FAQ)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | slug | String? |  yes  |  |
 | question | String? |  yes  |  |
 | answer | String? |  yes  |  |

---


 
 
 #### [CreateFaqResponseSchema](#CreateFaqResponseSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | faq | [FaqSchema](#FaqSchema)? |  yes  |  |

---


 
 
 #### [CreateFaqSchema](#CreateFaqSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | faq | [FAQ](#FAQ)? |  yes  |  |

---


 
 
 #### [GetFaqSchema](#GetFaqSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | faqs | ArrayList<HashMap<String,Any>>? |  yes  |  |

---


 
 
 #### [UpdateFaqCategoryRequestSchema](#UpdateFaqCategoryRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | category | [CategorySchema](#CategorySchema)? |  yes  |  |

---


 
 
 #### [CreateFaqCategoryRequestSchema](#CreateFaqCategoryRequestSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | category | [CategoryRequestSchema](#CategoryRequestSchema)? |  yes  |  |

---


 
 
 #### [CreateFaqCategorySchema](#CreateFaqCategorySchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | category | [CategorySchema](#CategorySchema)? |  yes  |  |

---


 
 
 #### [GetFaqCategoriesSchema](#GetFaqCategoriesSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | categories | ArrayList<[CategorySchema](#CategorySchema)>? |  yes  |  |

---


 
 
 #### [GetFaqCategoryBySlugSchema](#GetFaqCategoryBySlugSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | category | [FAQCategorySchema](#FAQCategorySchema)? |  yes  |  |

---


 
 
 #### [LandingPageGetResponse](#LandingPageGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[LandingPageSchema](#LandingPageSchema)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [LandingPageSchema](#LandingPageSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | slug | String? |  yes  |  |
 | action | [Action](#Action)? |  yes  |  |
 | platform | ArrayList<String>? |  yes  |  |
 | createdBy | [CreatedBySchema](#CreatedBySchema)? |  yes  |  |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | id | String? |  yes  |  |
 | application | String? |  yes  |  |
 | archived | Boolean? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [DefaultNavigationResponse](#DefaultNavigationResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[NavigationSchema](#NavigationSchema)>? |  yes  |  |

---


 
 
 #### [NavigationGetResponse](#NavigationGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[NavigationSchema](#NavigationSchema)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [Orientation](#Orientation)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | portrait | ArrayList<String>? |  yes  |  |
 | landscape | ArrayList<String>? |  yes  |  |

---


 
 
 #### [NavigationSchema](#NavigationSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | application | String? |  yes  |  |
 | archived | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | platform | ArrayList<String>? |  yes  |  |
 | createdBy | [CreatedBySchema](#CreatedBySchema)? |  yes  |  |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | orientation | [Orientation](#Orientation)? |  yes  |  |
 | version | Double? |  yes  |  |
 | navigation | ArrayList<[NavigationReference](#NavigationReference)>? |  yes  |  |

---


 
 
 #### [NavigationRequest](#NavigationRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | platform | ArrayList<String>? |  yes  |  |
 | orientation | [Orientation](#Orientation)? |  yes  |  |
 | navigation | ArrayList<[NavigationReference](#NavigationReference)>? |  yes  |  |

---


 
 
 #### [CustomPageSchema](#CustomPageSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | platform | String? |  yes  |  |
 | title | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | type | String? |  yes  |  |
 | orientation | String? |  yes  |  |
 | application | String? |  yes  |  |
 | description | String? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | content | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | createdBy | [CreatedBySchema](#CreatedBySchema)? |  yes  |  |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | schedule | [ScheduleSchema](#ScheduleSchema)? |  yes  |  |

---


 
 
 #### [ContentSchema](#ContentSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | value | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [CustomPage](#CustomPage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [CustomPageSchema](#CustomPageSchema)? |  yes  |  |

---


 
 
 #### [FeatureImage](#FeatureImage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | secureUrl | String? |  yes  |  |

---


 
 
 #### [PageGetResponse](#PageGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[PageSchema](#PageSchema)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [PageSpec](#PageSpec)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | specifications | ArrayList<HashMap<String,Any>>? |  yes  |  |

---


 
 
 #### [PageSpecParam](#PageSpecParam)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String? |  yes  |  |
 | required | Boolean? |  yes  |  |

---


 
 
 #### [PageSpecItem](#PageSpecItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pageType | String? |  yes  |  |
 | displayName | String? |  yes  |  |
 | params | ArrayList<[PageSpecParam](#PageSpecParam)>? |  yes  |  |
 | query | ArrayList<[PageSpecParam](#PageSpecParam)>? |  yes  |  |

---


 
 
 #### [PageSchema](#PageSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | application | String? |  yes  |  |
 | componentIds | ArrayList<String>? |  yes  | Components can be used to store multiple components |
 | content | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | createdBy | [CreatedBySchema](#CreatedBySchema)? |  yes  |  |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | description | String? |  yes  |  |
 | featureImage | [Asset](#Asset)? |  yes  |  |
 | pageMeta | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | schedule | [ScheduleSchema](#ScheduleSchema)? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | orientation | String? |  yes  |  |
 | platform | String? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | slug | String? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | title | String? |  yes  |  |
 | type | String? |  yes  |  |
 | seo | [SEO](#SEO)? |  yes  |  |
 | visibility | HashMap<String,Any>? |  yes  |  |
 | archived | Boolean? |  yes  |  |

---


 
 
 #### [CreatedBySchema](#CreatedBySchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |

---


 
 
 #### [PageContent](#PageContent)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | value | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [PageMeta](#PageMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String? |  yes  |  |
 | value | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [PageRequest](#PageRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | schedule | [CronSchedule](#CronSchedule)? |  yes  |  |
 | application | String? |  yes  |  |
 | author | [Author](#Author)? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | orientation | String? |  yes  |  |
 | content | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | featureImage | [Asset](#Asset)? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | readingTime | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | seo | [SEO](#SEO)? |  yes  |  |
 | title | String? |  yes  |  |

---


 
 
 #### [CronSchedule](#CronSchedule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cron | String? |  yes  |  |
 | start | String? |  yes  |  |
 | end | String? |  yes  |  |
 | duration | Double? |  yes  |  |

---


 
 
 #### [PagePublishRequest](#PagePublishRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | publish | Boolean? |  yes  |  |

---


 
 
 #### [PageMetaSchema](#PageMetaSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | systemPages | ArrayList<[NavigationSchema](#NavigationSchema)>? |  yes  |  |
 | customPages | ArrayList<[PageSchema](#PageSchema)>? |  yes  |  |
 | applicationId | String? |  yes  |  |

---


 
 
 #### [SlideshowGetResponse](#SlideshowGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[SlideshowSchema](#SlideshowSchema)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [SlideshowSchema](#SlideshowSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | application | String? |  yes  |  |
 | platform | String? |  yes  |  |
 | configuration | [ConfigurationSchema](#ConfigurationSchema)? |  yes  |  |
 | media | ArrayList<[SlideshowMedia](#SlideshowMedia)>? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | archived | Boolean? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [SlideshowRequest](#SlideshowRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | slug | String? |  yes  |  |
 | platform | String? |  yes  |  |
 | configuration | [ConfigurationSchema](#ConfigurationSchema)? |  yes  |  |
 | media | [SlideshowMedia](#SlideshowMedia)? |  yes  |  |
 | active | Boolean? |  yes  |  |

---


 
 
 #### [Support](#Support)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | created | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | configType | String? |  yes  |  |
 | application | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | contact | [ContactSchema](#ContactSchema)? |  yes  |  |

---


 
 
 #### [PhoneProperties](#PhoneProperties)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String? |  yes  |  |
 | code | String? |  yes  |  |
 | number | String? |  yes  |  |

---


 
 
 #### [PhoneSchema](#PhoneSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  |  |
 | phone | ArrayList<[PhoneProperties](#PhoneProperties)>? |  yes  |  |

---


 
 
 #### [EmailProperties](#EmailProperties)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [EmailSchema](#EmailSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  |  |
 | email | ArrayList<[EmailProperties](#EmailProperties)>? |  yes  |  |

---


 
 
 #### [ContactSchema](#ContactSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | phone | [PhoneSchema](#PhoneSchema)? |  yes  |  |
 | email | [EmailSchema](#EmailSchema)? |  yes  |  |

---


 
 
 #### [TagsSchema](#TagsSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | application | String? |  yes  |  |
 | id | String? |  yes  |  |
 | tags | ArrayList<[TagSchema](#TagSchema)>? |  yes  |  |

---


 
 
 #### [TagSchema](#TagSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | url | String? |  yes  |  |
 | type | String? |  yes  |  |
 | subType | String? |  yes  |  |
 | id | String? |  yes  |  |
 | position | String? |  yes  |  |
 | attributes | HashMap<String,Any>? |  yes  |  |
 | content | String? |  yes  |  |

---




 
 
 #### [UnauthenticatedUser](#UnauthenticatedUser)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  | Failure message. |

---


 
 
 #### [UnauthenticatedApplication](#UnauthenticatedApplication)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  | Failure message. |

---


 
 
 #### [BadRequest](#BadRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  | Failure message. |

---


 
 
 #### [ResourceNotFound](#ResourceNotFound)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  | Resource not found with {id} |

---


 
 
 #### [InternalServerError](#InternalServerError)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  | Internal server Server error |
 | code | String? |  yes  | Error code |

---


 
 
 #### [PlanRecurring](#PlanRecurring)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | interval | String? |  yes  |  |
 | intervalCount | Double? |  yes  |  |

---


 
 
 #### [Plan](#Plan)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | recurring | [PlanRecurring](#PlanRecurring)? |  yes  |  |
 | isTrialPlan | Boolean? |  yes  |  |
 | planGroup | String? |  yes  |  |
 | tagLines | ArrayList<String>? |  yes  |  |
 | currency | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | isVisible | Boolean? |  yes  |  |
 | trialPeriod | Double? |  yes  |  |
 | addons | ArrayList<String>? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | type | String? |  yes  |  |
 | country | String? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | amount | Double? |  yes  |  |
 | productSuiteId | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | modifiedAt | String? |  yes  |  |

---


 
 
 #### [DetailedPlanComponents](#DetailedPlanComponents)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | description | String? |  yes  |  |
 | group | String? |  yes  |  |
 | icon | String? |  yes  |  |
 | links | HashMap<String,Any>? |  yes  |  |
 | enabled | Boolean? |  yes  |  |
 | displayText | String? |  yes  |  |

---


 
 
 #### [DetailedPlan](#DetailedPlan)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | recurring | [PlanRecurring](#PlanRecurring)? |  yes  |  |
 | isTrialPlan | Boolean? |  yes  |  |
 | planGroup | String? |  yes  |  |
 | tagLines | ArrayList<String>? |  yes  |  |
 | currency | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | isVisible | Boolean? |  yes  |  |
 | trialPeriod | Double? |  yes  |  |
 | addons | ArrayList<String>? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | type | String? |  yes  |  |
 | country | String? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | amount | Double? |  yes  |  |
 | productSuiteId | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | modifiedAt | String? |  yes  |  |
 | components | ArrayList<[DetailedPlanComponents](#DetailedPlanComponents)>? |  yes  |  |

---


 
 
 #### [SubscriptionTrialPeriod](#SubscriptionTrialPeriod)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | startDate | String? |  yes  |  |
 | endDate | String? |  yes  |  |

---


 
 
 #### [EntityChargePrice](#EntityChargePrice)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | Double |  no  | Amount for price. Minimum value 1 |
 | currencyCode | String |  no  |  |

---


 
 
 #### [EntityChargeRecurring](#EntityChargeRecurring)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | interval | String |  no  |  |

---


 
 
 #### [ChargeLineItem](#ChargeLineItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | term | String |  no  |  |
 | pricingType | String |  no  |  |
 | price | [EntityChargePrice](#EntityChargePrice) |  no  |  |
 | recurring | [EntityChargeRecurring](#EntityChargeRecurring)? |  yes  |  |
 | cappedAmount | Double? |  yes  |  |
 | trialDays | Int? |  yes  |  |
 | isTest | Boolean? |  yes  |  |
 | metadata | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [CreateSubscriptionCharge](#CreateSubscriptionCharge)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | trialDays | Int? |  yes  |  |
 | lineItems | ArrayList<[ChargeLineItem](#ChargeLineItem)> |  no  |  |
 | isTest | Boolean? |  yes  |  |
 | returnUrl | String |  no  |  |

---


 
 
 #### [CurrentPeriod](#CurrentPeriod)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | startDate | String? |  yes  |  |
 | endDate | String? |  yes  |  |

---


 
 
 #### [SubscriptionCharge](#SubscriptionCharge)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | term | String? |  yes  |  |
 | pricingType | String? |  yes  |  |
 | price | [EntityChargePrice](#EntityChargePrice)? |  yes  |  |
 | recurring | [EntityChargeRecurring](#EntityChargeRecurring)? |  yes  |  |
 | cappedAmount | Double? |  yes  |  |
 | activatedOn | String? |  yes  |  |
 | cancelledOn | String? |  yes  |  |
 | billingDate | String? |  yes  |  |
 | currentPeriod | [CurrentPeriod](#CurrentPeriod)? |  yes  |  |
 | status | String? |  yes  |  |
 | isTest | Boolean? |  yes  |  |
 | metadata | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [EntitySubscription](#EntitySubscription)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | status | String? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | activatedOn | String? |  yes  |  |
 | cancelledOn | String? |  yes  |  |
 | trialDays | Int? |  yes  |  |
 | trialPeriod | [SubscriptionTrialPeriod](#SubscriptionTrialPeriod)? |  yes  |  |
 | metadata | HashMap<String,Any>? |  yes  |  |
 | lineItems | ArrayList<[SubscriptionCharge](#SubscriptionCharge)>? |  yes  |  |

---


 
 
 #### [CreateSubscriptionResponse](#CreateSubscriptionResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | subscription | [EntitySubscription](#EntitySubscription)? |  yes  |  |
 | confirmUrl | String? |  yes  |  |

---


 
 
 #### [InvoiceDetailsPeriod](#InvoiceDetailsPeriod)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | start | String? |  yes  |  |
 | end | String? |  yes  |  |

---


 
 
 #### [InvoiceDetailsClient](#InvoiceDetailsClient)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | addressLines | ArrayList<String>? |  yes  |  |
 | name | String? |  yes  |  |
 | email | String? |  yes  |  |
 | phone | String? |  yes  |  |

---


 
 
 #### [InvoiceDetailsStatusTrail](#InvoiceDetailsStatusTrail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | value | String? |  yes  |  |
 | timestamp | String? |  yes  |  |

---


 
 
 #### [InvoiceDetailsPaymentMethodsDataChecks](#InvoiceDetailsPaymentMethodsDataChecks)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cvcCheck | String? |  yes  |  |
 | addressLine1Check | String? |  yes  |  |
 | addressPostalCodeCheck | String? |  yes  |  |

---


 
 
 #### [InvoiceDetailsPaymentMethodsDataNetworks](#InvoiceDetailsPaymentMethodsDataNetworks)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | available | ArrayList<String>? |  yes  |  |
 | preferred | String? |  yes  |  |

---


 
 
 #### [InvoiceDetailsPaymentMethodsDataThreeDSecureUsage](#InvoiceDetailsPaymentMethodsDataThreeDSecureUsage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | supported | Boolean? |  yes  |  |

---


 
 
 #### [InvoiceDetailsPaymentMethodsData](#InvoiceDetailsPaymentMethodsData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brand | String? |  yes  |  |
 | last4 | String? |  yes  |  |
 | checks | [InvoiceDetailsPaymentMethodsDataChecks](#InvoiceDetailsPaymentMethodsDataChecks)? |  yes  |  |
 | wallet | String? |  yes  |  |
 | country | String? |  yes  |  |
 | funding | String? |  yes  |  |
 | expYear | Int? |  yes  |  |
 | networks | [InvoiceDetailsPaymentMethodsDataNetworks](#InvoiceDetailsPaymentMethodsDataNetworks)? |  yes  |  |
 | expMonth | Int? |  yes  |  |
 | fingerprint | String? |  yes  |  |
 | generatedFrom | String? |  yes  |  |
 | threeDSecureUsage | [InvoiceDetailsPaymentMethodsDataThreeDSecureUsage](#InvoiceDetailsPaymentMethodsDataThreeDSecureUsage)? |  yes  |  |

---


 
 
 #### [InvoiceDetailsPaymentMethods](#InvoiceDetailsPaymentMethods)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |
 | type | String? |  yes  |  |
 | pgPaymentMethodId | String? |  yes  |  |
 | data | [InvoiceDetailsPaymentMethodsData](#InvoiceDetailsPaymentMethodsData)? |  yes  |  |
 | isDefault | Boolean? |  yes  |  |

---


 
 
 #### [InvoicePaymentMethod](#InvoicePaymentMethod)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pgPaymentMethodId | String? |  yes  |  |

---


 
 
 #### [InvoiceDetails](#InvoiceDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | period | [InvoiceDetailsPeriod](#InvoiceDetailsPeriod)? |  yes  |  |
 | client | [InvoiceDetailsClient](#InvoiceDetailsClient)? |  yes  |  |
 | autoAdvance | Boolean? |  yes  |  |
 | currency | String? |  yes  |  |
 | paid | Boolean? |  yes  |  |
 | attemp | Int? |  yes  |  |
 | id | String? |  yes  |  |
 | collectionMethod | String? |  yes  |  |
 | subscriberId | String? |  yes  |  |
 | invoiceUrl | String? |  yes  |  |
 | number | String? |  yes  |  |
 | pgData | HashMap<String,Any>? |  yes  |  |
 | receiptNumber | String? |  yes  |  |
 | statementDescriptor | String? |  yes  |  |
 | currentStatus | String? |  yes  |  |
 | statusTrail | ArrayList<[InvoiceDetailsStatusTrail](#InvoiceDetailsStatusTrail)>? |  yes  |  |
 | subtotal | Double? |  yes  |  |
 | total | Double? |  yes  |  |
 | subscription | String? |  yes  |  |
 | nextActionTime | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | modifiedAt | String? |  yes  |  |
 | hashIdentifier | String? |  yes  |  |
 | paymentMethod | [InvoicePaymentMethod](#InvoicePaymentMethod)? |  yes  |  |

---


 
 
 #### [InvoiceItemsPlanRecurring](#InvoiceItemsPlanRecurring)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | interval | String? |  yes  |  |
 | intervalCount | Int? |  yes  |  |

---


 
 
 #### [InvoiceItemsPlan](#InvoiceItemsPlan)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | recurring | [InvoiceItemsPlanRecurring](#InvoiceItemsPlanRecurring)? |  yes  |  |
 | isTrialPlan | Boolean? |  yes  |  |
 | planGroup | String? |  yes  |  |
 | tagLines | ArrayList<String>? |  yes  |  |
 | currency | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | isVisible | Boolean? |  yes  |  |
 | trialPeriod | Int? |  yes  |  |
 | addons | ArrayList<String>? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | type | String? |  yes  |  |
 | country | String? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | amount | Int? |  yes  |  |
 | productSuiteId | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | modifiedAt | String? |  yes  |  |

---


 
 
 #### [InvoiceItemsPeriod](#InvoiceItemsPeriod)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | start | String? |  yes  |  |
 | end | String? |  yes  |  |

---


 
 
 #### [InvoiceItems](#InvoiceItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | currency | String? |  yes  |  |
 | plan | [InvoiceItemsPlan](#InvoiceItemsPlan)? |  yes  |  |
 | name | String? |  yes  |  |
 | quantity | Int? |  yes  |  |
 | description | String? |  yes  |  |
 | period | [InvoiceItemsPeriod](#InvoiceItemsPeriod)? |  yes  |  |
 | unitAmount | Double? |  yes  |  |
 | amount | Double? |  yes  |  |
 | type | String? |  yes  |  |
 | invoiceId | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | modifiedAt | String? |  yes  |  |

---


 
 
 #### [Invoice](#Invoice)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | invoice | [InvoiceDetails](#InvoiceDetails)? |  yes  |  |
 | invoiceItems | ArrayList<[InvoiceItems](#InvoiceItems)>? |  yes  |  |

---


 
 
 #### [InvoicesDataClient](#InvoicesDataClient)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | email | String? |  yes  |  |
 | phone | String? |  yes  |  |
 | addressLines | ArrayList<String>? |  yes  |  |

---


 
 
 #### [InvoicesDataPeriod](#InvoicesDataPeriod)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | start | String? |  yes  |  |
 | end | String? |  yes  |  |

---


 
 
 #### [InvoicesDataPaymentMethod](#InvoicesDataPaymentMethod)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pgPaymentMethodId | String? |  yes  |  |

---


 
 
 #### [InvoicesData](#InvoicesData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | client | [InvoicesDataClient](#InvoicesDataClient)? |  yes  |  |
 | autoAdvance | Boolean? |  yes  |  |
 | currency | String? |  yes  |  |
 | paid | Boolean? |  yes  |  |
 | attemp | Int? |  yes  |  |
 | collectionMethod | String? |  yes  |  |
 | subscriberId | String? |  yes  |  |
 | invoiceUrl | String? |  yes  |  |
 | number | String? |  yes  |  |
 | pgData | HashMap<String,Any>? |  yes  |  |
 | period | [InvoicesDataPeriod](#InvoicesDataPeriod)? |  yes  |  |
 | receiptNumber | String? |  yes  |  |
 | statementDescriptor | String? |  yes  |  |
 | currentStatus | String? |  yes  |  |
 | statusTrail | ArrayList<[InvoiceDetailsStatusTrail](#InvoiceDetailsStatusTrail)>? |  yes  |  |
 | subtotal | Double? |  yes  |  |
 | total | Double? |  yes  |  |
 | subscription | String? |  yes  |  |
 | nextActionTime | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | modifiedAt | String? |  yes  |  |
 | hashIdentifier | String? |  yes  |  |
 | paymentMethod | [InvoicesDataPaymentMethod](#InvoicesDataPaymentMethod)? |  yes  |  |
 | invoiceItems | ArrayList<[InvoiceItems](#InvoiceItems)>? |  yes  |  |

---


 
 
 #### [Invoices](#Invoices)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | ArrayList<[InvoicesData](#InvoicesData)>? |  yes  |  |
 | start | Int? |  yes  |  |
 | end | Int? |  yes  |  |
 | limit | Int? |  yes  |  |
 | page | Int? |  yes  |  |
 | total | Int? |  yes  |  |

---


 
 
 #### [Phone](#Phone)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | phoneNumber | String? |  yes  |  |
 | phoneCountryCode | String? |  yes  |  |

---


 
 
 #### [SubscriptionBillingAddress](#SubscriptionBillingAddress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | country | String? |  yes  |  |
 | state | String? |  yes  |  |
 | city | String? |  yes  |  |
 | line1 | String? |  yes  |  |
 | line2 | String? |  yes  |  |
 | postalCode | String? |  yes  |  |

---


 
 
 #### [SubscriptionCustomer](#SubscriptionCustomer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | phone | [Phone](#Phone)? |  yes  |  |
 | billingAddress | [SubscriptionBillingAddress](#SubscriptionBillingAddress)? |  yes  |  |
 | id | String? |  yes  |  |
 | uniqueId | String? |  yes  |  |
 | type | String? |  yes  |  |
 | name | String? |  yes  |  |
 | email | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | modifiedAt | String? |  yes  |  |
 | data | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [SubscriptionCustomerCreate](#SubscriptionCustomerCreate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | phone | [Phone](#Phone)? |  yes  |  |
 | billingAddress | [SubscriptionBillingAddress](#SubscriptionBillingAddress)? |  yes  |  |
 | uniqueId | String? |  yes  |  |
 | type | String? |  yes  |  |
 | name | String? |  yes  |  |
 | email | String? |  yes  |  |

---


 
 
 #### [SubscriptionCurrentPeriod](#SubscriptionCurrentPeriod)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | start | String? |  yes  |  |
 | end | String? |  yes  |  |

---


 
 
 #### [SubscriptionPauseCollection](#SubscriptionPauseCollection)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | behavior | String? |  yes  |  |
 | resumeAt | String? |  yes  |  |

---


 
 
 #### [SubscriptionTrial](#SubscriptionTrial)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | start | String? |  yes  |  |
 | end | String? |  yes  |  |

---


 
 
 #### [SubscriptionInvoiceSettings](#SubscriptionInvoiceSettings)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | generation | Boolean? |  yes  |  |
 | charging | Boolean? |  yes  |  |

---


 
 
 #### [Subscription](#Subscription)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | currentPeriod | [SubscriptionCurrentPeriod](#SubscriptionCurrentPeriod)? |  yes  |  |
 | pauseCollection | [SubscriptionPauseCollection](#SubscriptionPauseCollection)? |  yes  |  |
 | trial | [SubscriptionTrial](#SubscriptionTrial)? |  yes  |  |
 | invoiceSettings | [SubscriptionInvoiceSettings](#SubscriptionInvoiceSettings)? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | cancelAtPeriodEnd | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | subscriberId | String? |  yes  |  |
 | planId | String? |  yes  |  |
 | productSuiteId | String? |  yes  |  |
 | planData | [Plan](#Plan)? |  yes  |  |
 | currentStatus | String? |  yes  |  |
 | collectionMethod | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | modifiedAt | String? |  yes  |  |
 | latestInvoice | String? |  yes  |  |

---


 
 
 #### [SubscriptionStatus](#SubscriptionStatus)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isEnabled | Boolean? |  yes  |  |
 | subscription | [Subscription](#Subscription)? |  yes  |  |

---


 
 
 #### [SubscriptionLimitApplication](#SubscriptionLimitApplication)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |
 | hardLimit | Int? |  yes  |  |
 | softLimit | Int? |  yes  |  |

---


 
 
 #### [SubscriptionLimitMarketplace](#SubscriptionLimitMarketplace)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [SubscriptionLimitOtherPlatform](#SubscriptionLimitOtherPlatform)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [SubscriptionLimitTeam](#SubscriptionLimitTeam)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | limit | Int? |  yes  |  |

---


 
 
 #### [SubscriptionLimitProducts](#SubscriptionLimitProducts)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | bulk | Boolean? |  yes  |  |
 | limit | Int? |  yes  |  |

---


 
 
 #### [SubscriptionLimitExtensions](#SubscriptionLimitExtensions)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |
 | limit | Int? |  yes  |  |

---


 
 
 #### [SubscriptionLimitIntegrations](#SubscriptionLimitIntegrations)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |
 | limit | Int? |  yes  |  |

---


 
 
 #### [SubscriptionLimit](#SubscriptionLimit)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | application | [SubscriptionLimitApplication](#SubscriptionLimitApplication)? |  yes  |  |
 | marketplace | [SubscriptionLimitMarketplace](#SubscriptionLimitMarketplace)? |  yes  |  |
 | otherPlatform | [SubscriptionLimitOtherPlatform](#SubscriptionLimitOtherPlatform)? |  yes  |  |
 | team | [SubscriptionLimitTeam](#SubscriptionLimitTeam)? |  yes  |  |
 | products | [SubscriptionLimitProducts](#SubscriptionLimitProducts)? |  yes  |  |
 | extensions | [SubscriptionLimitExtensions](#SubscriptionLimitExtensions)? |  yes  |  |
 | integrations | [SubscriptionLimitIntegrations](#SubscriptionLimitIntegrations)? |  yes  |  |
 | isTrialPlan | Boolean? |  yes  |  |

---


 
 
 #### [SubscriptionActivateReq](#SubscriptionActivateReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uniqueId | String? |  yes  |  |
 | type | String? |  yes  |  |
 | productSuite | String? |  yes  |  |
 | planId | String? |  yes  |  |
 | paymentMethod | String? |  yes  |  |

---


 
 
 #### [SubscriptionActivateRes](#SubscriptionActivateRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |
 | data | [Subscription](#Subscription)? |  yes  |  |

---


 
 
 #### [CancelSubscriptionReq](#CancelSubscriptionReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uniqueId | String? |  yes  |  |
 | type | String? |  yes  |  |
 | productSuite | String? |  yes  |  |
 | subscriptionId | String? |  yes  |  |

---


 
 
 #### [CancelSubscriptionRes](#CancelSubscriptionRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |
 | data | [Subscription](#Subscription)? |  yes  |  |

---




 
 
 #### [StatsImported](#StatsImported)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | count | Int? |  yes  |  |

---


 
 
 #### [StatsProcessedEmail](#StatsProcessedEmail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Int? |  yes  |  |
 | failed | Int? |  yes  |  |
 | suppressed | Int? |  yes  |  |

---


 
 
 #### [StatsProcessedSms](#StatsProcessedSms)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Int? |  yes  |  |
 | failed | Int? |  yes  |  |
 | suppressed | Int? |  yes  |  |

---


 
 
 #### [StatsProcessed](#StatsProcessed)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | [StatsProcessedEmail](#StatsProcessedEmail)? |  yes  |  |
 | sms | [StatsProcessedSms](#StatsProcessedSms)? |  yes  |  |

---


 
 
 #### [Stats](#Stats)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | imported | Any? |  yes  |  |
 | processed | Any? |  yes  |  |

---


 
 
 #### [GetStats](#GetStats)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Stats](#Stats)>? |  yes  |  |

---


 
 
 #### [CampaignReq](#CampaignReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | headers | ArrayList<String>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | fileUrl | String? |  yes  |  |
 | type | String? |  yes  |  |
 | recordsCount | Int? |  yes  |  |
 | application | String? |  yes  |  |

---


 
 
 #### [RecipientHeaders](#RecipientHeaders)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | String? |  yes  |  |

---


 
 
 #### [CampaignEmailTemplate](#CampaignEmailTemplate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [CampignEmailProvider](#CampignEmailProvider)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | fromName | String? |  yes  |  |
 | fromEmail | String? |  yes  |  |

---


 
 
 #### [CampaignEmail](#CampaignEmail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | template | [CampaignEmailTemplate](#CampaignEmailTemplate)? |  yes  |  |
 | provider | [CampignEmailProvider](#CampignEmailProvider)? |  yes  |  |

---


 
 
 #### [Campaign](#Campaign)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | recipientHeaders | [RecipientHeaders](#RecipientHeaders)? |  yes  |  |
 | email | [CampaignEmail](#CampaignEmail)? |  yes  |  |
 | description | String? |  yes  |  |
 | tags | ArrayList<Any>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | datasource | String? |  yes  |  |
 | type | String? |  yes  |  |
 | name | String? |  yes  |  |
 | application | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [Campaigns](#Campaigns)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Campaign](#Campaign)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [BigqueryHeadersReq](#BigqueryHeadersReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | query | String? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [BigqueryHeadersResHeaders](#BigqueryHeadersResHeaders)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [BigqueryHeadersRes](#BigqueryHeadersRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | headers | ArrayList<[BigqueryHeadersResHeaders](#BigqueryHeadersResHeaders)>? |  yes  |  |

---


 
 
 #### [GetNRecordsCsvReq](#GetNRecordsCsvReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | url | String? |  yes  |  |
 | header | Boolean? |  yes  |  |
 | count | Int? |  yes  |  |

---


 
 
 #### [GetNRecordsCsvResItems](#GetNRecordsCsvResItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | phoneNumber | String? |  yes  |  |
 | email | String? |  yes  |  |
 | firstname | String? |  yes  |  |
 | lastname | String? |  yes  |  |
 | orderid | String? |  yes  |  |

---


 
 
 #### [GetNRecordsCsvRes](#GetNRecordsCsvRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[GetNRecordsCsvResItems](#GetNRecordsCsvResItems)>? |  yes  |  |

---


 
 
 #### [AudienceReq](#AudienceReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | headers | ArrayList<String>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | fileUrl | String? |  yes  |  |
 | type | String? |  yes  |  |
 | recordsCount | Int? |  yes  |  |
 | application | String? |  yes  |  |

---


 
 
 #### [Audience](#Audience)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | headers | ArrayList<String>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | fileUrl | String? |  yes  |  |
 | type | String? |  yes  |  |
 | recordsCount | Int? |  yes  |  |
 | application | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [Audiences](#Audiences)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Audience](#Audience)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [EmailProviderReqFrom](#EmailProviderReqFrom)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | email | String? |  yes  |  |
 | isDefault | Boolean? |  yes  |  |

---


 
 
 #### [EmailProviderReq](#EmailProviderReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | apiKey | String? |  yes  |  |
 | type | String? |  yes  |  |
 | provider | String? |  yes  |  |
 | from | ArrayList<[EmailProviderReqFrom](#EmailProviderReqFrom)>? |  yes  |  |

---


 
 
 #### [EmailProvider](#EmailProvider)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | provider | String? |  yes  |  |
 | from | ArrayList<[EmailProviderReqFrom](#EmailProviderReqFrom)>? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | apiKey | String? |  yes  |  |
 | application | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [EmailProviders](#EmailProviders)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[EmailProvider](#EmailProvider)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [EmailTemplateDeleteSuccessRes](#EmailTemplateDeleteSuccessRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [EmailTemplateDeleteFailureRes](#EmailTemplateDeleteFailureRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [EmailTemplateKeys](#EmailTemplateKeys)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | to | String? |  yes  |  |
 | cc | String? |  yes  |  |
 | bcc | String? |  yes  |  |

---


 
 
 #### [EmailTemplateHeaders](#EmailTemplateHeaders)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [EmailTemplateReq](#EmailTemplateReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | keys | [EmailTemplateKeys](#EmailTemplateKeys)? |  yes  |  |
 | from | String? |  yes  |  |
 | staticTo | ArrayList<String>? |  yes  |  |
 | staticCc | ArrayList<String>? |  yes  |  |
 | staticBcc | ArrayList<String>? |  yes  |  |
 | replyTo | String? |  yes  |  |
 | headers | ArrayList<[EmailTemplateHeaders](#EmailTemplateHeaders)>? |  yes  |  |
 | subject | [TemplateAndType](#TemplateAndType)? |  yes  |  |
 | html | [TemplateAndType](#TemplateAndType)? |  yes  |  |
 | text | [TemplateAndType](#TemplateAndType)? |  yes  |  |
 | attachments | ArrayList<Any>? |  yes  |  |
 | priority | String? |  yes  |  |

---


 
 
 #### [TemplateAndType](#TemplateAndType)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | templateType | String? |  yes  |  |
 | template | String? |  yes  |  |

---


 
 
 #### [EmailTemplateRes](#EmailTemplateRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isSystem | Boolean? |  yes  |  |
 | isInternal | Boolean? |  yes  |  |
 | description | String? |  yes  |  |
 | staticTo | ArrayList<String>? |  yes  |  |
 | staticCc | ArrayList<String>? |  yes  |  |
 | staticBcc | ArrayList<String>? |  yes  |  |
 | tags | ArrayList<Any>? |  yes  |  |
 | priority | String? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | keys | [EmailTemplateKeys](#EmailTemplateKeys)? |  yes  |  |
 | from | String? |  yes  |  |
 | replyTo | String? |  yes  |  |
 | headers | ArrayList<[EmailTemplateHeaders](#EmailTemplateHeaders)>? |  yes  |  |
 | subject | [TemplateAndType](#TemplateAndType)? |  yes  |  |
 | html | [TemplateAndType](#TemplateAndType)? |  yes  |  |
 | text | [TemplateAndType](#TemplateAndType)? |  yes  |  |
 | attachments | ArrayList<Any>? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [EmailTemplate](#EmailTemplate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isSystem | Boolean? |  yes  |  |
 | isInternal | Boolean? |  yes  |  |
 | description | String? |  yes  |  |
 | staticTo | ArrayList<Any>? |  yes  |  |
 | staticCc | ArrayList<Any>? |  yes  |  |
 | staticBcc | ArrayList<Any>? |  yes  |  |
 | tags | ArrayList<Any>? |  yes  |  |
 | priority | String? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | name | String? |  yes  |  |
 | from | String? |  yes  |  |
 | fromName | String? |  yes  |  |
 | subject | [TemplateAndType](#TemplateAndType)? |  yes  |  |
 | html | [TemplateAndType](#TemplateAndType)? |  yes  |  |
 | text | [TemplateAndType](#TemplateAndType)? |  yes  |  |
 | headers | ArrayList<Any>? |  yes  |  |
 | attachments | ArrayList<Any>? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [SystemEmailTemplate](#SystemEmailTemplate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isSystem | Boolean? |  yes  |  |
 | isInternal | Boolean? |  yes  |  |
 | description | String? |  yes  |  |
 | staticTo | ArrayList<Any>? |  yes  |  |
 | staticCc | ArrayList<Any>? |  yes  |  |
 | staticBcc | ArrayList<Any>? |  yes  |  |
 | tags | ArrayList<Any>? |  yes  |  |
 | priority | String? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | name | String? |  yes  |  |
 | from | String? |  yes  |  |
 | fromName | String? |  yes  |  |
 | subject | [TemplateAndType](#TemplateAndType)? |  yes  |  |
 | html | [TemplateAndType](#TemplateAndType)? |  yes  |  |
 | text | [TemplateAndType](#TemplateAndType)? |  yes  |  |
 | headers | ArrayList<Any>? |  yes  |  |
 | attachments | ArrayList<Any>? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [EmailTemplates](#EmailTemplates)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[EmailTemplate](#EmailTemplate)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [SystemEmailTemplates](#SystemEmailTemplates)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[SystemEmailTemplate](#SystemEmailTemplate)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [EventSubscriptionTemplateSms](#EventSubscriptionTemplateSms)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | subscribed | Boolean? |  yes  |  |
 | template | String? |  yes  |  |

---


 
 
 #### [EventSubscriptionTemplateEmail](#EventSubscriptionTemplateEmail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | subscribed | Boolean? |  yes  |  |
 | template | String? |  yes  |  |

---


 
 
 #### [EventSubscriptionTemplate](#EventSubscriptionTemplate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sms | [EventSubscriptionTemplateSms](#EventSubscriptionTemplateSms)? |  yes  |  |
 | email | [EventSubscriptionTemplateEmail](#EventSubscriptionTemplateEmail)? |  yes  |  |

---


 
 
 #### [EventSubscription](#EventSubscription)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | template | [EventSubscriptionTemplate](#EventSubscriptionTemplate)? |  yes  |  |
 | isDefault | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | application | String? |  yes  |  |
 | event | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [EventSubscriptions](#EventSubscriptions)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[EventSubscription](#EventSubscription)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [TriggerJobResponse](#TriggerJobResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | Int? |  yes  |  |

---


 
 
 #### [TriggerJobRequest](#TriggerJobRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | jobId | String? |  yes  |  |

---


 
 
 #### [Job](#Job)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | completed | Boolean? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | campaign | String? |  yes  |  |
 | application | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [Jobs](#Jobs)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Job](#Job)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [JobLog](#JobLog)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | imported | Any? |  yes  |  |
 | processed | Any? |  yes  |  |
 | id | String? |  yes  |  |
 | job | String? |  yes  |  |
 | campaign | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [JobLogs](#JobLogs)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[JobLog](#JobLog)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [LogEmail](#LogEmail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | template | String? |  yes  |  |

---


 
 
 #### [LogPushnotification](#LogPushnotification)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pushtokens | ArrayList<String>? |  yes  |  |

---


 
 
 #### [LogMeta](#LogMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | identifier | String? |  yes  |  |
 | key | String? |  yes  |  |
 | offset | String? |  yes  |  |
 | partition | String? |  yes  |  |
 | topic | String? |  yes  |  |

---


 
 
 #### [Log](#Log)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | [LogEmail](#LogEmail)? |  yes  |  |
 | pushnotification | [LogPushnotification](#LogPushnotification)? |  yes  |  |
 | meta | [LogMeta](#LogMeta)? |  yes  |  |
 | id | String? |  yes  |  |
 | application | String? |  yes  |  |
 | service | String? |  yes  |  |
 | step | String? |  yes  |  |
 | status | String? |  yes  |  |
 | data | Any? |  yes  |  |
 | expireAt | String? |  yes  |  |
 | createdAt | String? |  yes  |  |

---


 
 
 #### [Logs](#Logs)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Log](#Log)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [PushtokenReq](#PushtokenReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | action | String? |  yes  |  |
 | bundleIdentifier | String? |  yes  |  |
 | pushToken | String? |  yes  |  |
 | uniqueDeviceId | String? |  yes  |  |

---


 
 
 #### [PushtokenRes](#PushtokenRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | bundleIdentifier | String? |  yes  |  |
 | pushToken | String? |  yes  |  |
 | uniqueDeviceId | String? |  yes  |  |
 | type | String? |  yes  |  |
 | platform | String? |  yes  |  |
 | applicationId | String? |  yes  |  |
 | userId | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | expiredAt | String? |  yes  |  |

---


 
 
 #### [SmsProviderReq](#SmsProviderReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | sender | String? |  yes  |  |
 | username | String? |  yes  |  |
 | authkey | String? |  yes  |  |
 | type | String? |  yes  |  |
 | provider | String? |  yes  |  |

---


 
 
 #### [SmsProvider](#SmsProvider)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | rpt | Int? |  yes  |  |
 | type | String? |  yes  |  |
 | provider | String? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | sender | String? |  yes  |  |
 | username | String? |  yes  |  |
 | authkey | String? |  yes  |  |
 | application | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [SmsProviders](#SmsProviders)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[SmsProvider](#SmsProvider)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [SmsTemplateDeleteSuccessRes](#SmsTemplateDeleteSuccessRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [SmsTemplateDeleteFailureRes](#SmsTemplateDeleteFailureRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [SmsTemplateMessage](#SmsTemplateMessage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | templateType | String? |  yes  |  |
 | template | String? |  yes  |  |

---


 
 
 #### [SmsTemplateReq](#SmsTemplateReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | message | [SmsTemplateMessage](#SmsTemplateMessage)? |  yes  |  |
 | templateVariables | Any? |  yes  |  |
 | attachments | ArrayList<Any>? |  yes  |  |
 | priority | String? |  yes  |  |

---


 
 
 #### [SmsTemplateRes](#SmsTemplateRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isSystem | Boolean? |  yes  |  |
 | isInternal | Boolean? |  yes  |  |
 | description | String? |  yes  |  |
 | tags | ArrayList<Any>? |  yes  |  |
 | priority | String? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | message | [SmsTemplateMessage](#SmsTemplateMessage)? |  yes  |  |
 | templateVariables | Any? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [SmsTemplate](#SmsTemplate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isSystem | Boolean? |  yes  |  |
 | isInternal | Boolean? |  yes  |  |
 | description | String? |  yes  |  |
 | priority | String? |  yes  |  |
 | tags | ArrayList<Any>? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | name | String? |  yes  |  |
 | message | [SmsTemplateMessage](#SmsTemplateMessage)? |  yes  |  |
 | templateVariables | Any? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [SystemSmsTemplate](#SystemSmsTemplate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isSystem | Boolean? |  yes  |  |
 | isInternal | Boolean? |  yes  |  |
 | description | String? |  yes  |  |
 | tags | ArrayList<Any>? |  yes  |  |
 | priority | String? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | name | String? |  yes  |  |
 | message | [SmsTemplateMessage](#SmsTemplateMessage)? |  yes  |  |
 | templateVariables | Any? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [SmsTemplates](#SmsTemplates)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[SmsTemplate](#SmsTemplate)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [SystemSmsTemplates](#SystemSmsTemplates)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[SystemSmsTemplate](#SystemSmsTemplate)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [Notification](#Notification)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | body | String? |  yes  |  |
 | subtitle | String? |  yes  |  |
 | icon | String? |  yes  |  |
 | deeplink | String? |  yes  |  |
 | clickAction | String? |  yes  |  |

---


 
 
 #### [SystemNotificationUser](#SystemNotificationUser)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [SystemNotificationSettings](#SystemNotificationSettings)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sound | Boolean? |  yes  |  |
 | priority | String? |  yes  |  |
 | timeToLive | String? |  yes  |  |

---


 
 
 #### [SystemNotification](#SystemNotification)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | notification | [Notification](#Notification)? |  yes  |  |
 | user | [SystemNotificationUser](#SystemNotificationUser)? |  yes  |  |
 | settings | [SystemNotificationUser](#SystemNotificationUser)? |  yes  |  |
 | id | String? |  yes  |  |
 | group | String? |  yes  |  |
 | createdAt | String? |  yes  |  |

---


 
 
 #### [SystemNotificationsPage](#SystemNotificationsPage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | current | Int? |  yes  |  |
 | size | Int? |  yes  |  |
 | itemTotal | Int? |  yes  |  |
 | hasNext | Boolean? |  yes  |  |

---


 
 
 #### [SystemNotifications](#SystemNotifications)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[SystemNotification](#SystemNotification)>? |  yes  |  |
 | lastReadAnchor | Int? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---




 
 
 #### [PaymentGatewayConfigResponse](#PaymentGatewayConfigResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | aggregators | ArrayList<HashMap<String,Any>>? |  yes  | List of all speceific Payment options with their Details. |
 | excludedFields | ArrayList<String> |  no  | List of all excluded  options with their Details. |
 | created | Boolean |  no  | Response is created or not |
 | appId | String |  no  | Application Id to which Payment config Mapped |
 | displayFields | ArrayList<String> |  no  | List of all included  options with their Details. |
 | success | Boolean |  no  | Response is successful or not |

---


 
 
 #### [ErrorCodeDescription](#ErrorCodeDescription)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String |  no  | Error human understandable description. |
 | code | String |  no  | Error descrption code. |
 | success | Boolean |  no  | Response is successful or not |

---


 
 
 #### [PaymentGatewayConfig](#PaymentGatewayConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | merchantSalt | String |  no  | Merchant key of the payment aggregator |
 | configType | String |  no  | Config Type of the aggregator |
 | isActive | Boolean? |  yes  | Enable/ Disable Flag |
 | key | String |  no  | Api key of the payment aggregator |
 | secret | String |  no  | Secret Key of the payment aggregator |

---


 
 
 #### [PaymentGatewayConfigRequest](#PaymentGatewayConfigRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isActive | Boolean? |  yes  | Enable/ Disable Flag |
 | aggregatorName | [PaymentGatewayConfig](#PaymentGatewayConfig)? |  yes  |  |
 | appId | String |  no  | Application Id to which Payment config Mapped |

---


 
 
 #### [PaymentGatewayToBeReviewed](#PaymentGatewayToBeReviewed)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | aggregator | ArrayList<String> |  no  | List of added payment gateway |
 | success | Boolean |  no  | Response is successful or not |

---


 
 
 #### [ErrorCodeAndDescription](#ErrorCodeAndDescription)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String |  no  | Error human understandable description. |
 | code | String |  no  | Error descrption code. |

---


 
 
 #### [HttpErrorCodeAndResponse](#HttpErrorCodeAndResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | error | [ErrorCodeAndDescription](#ErrorCodeAndDescription) |  no  |  |
 | success | Boolean |  no  | Response is successful or not |

---


 
 
 #### [PaymentModeLogo](#PaymentModeLogo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | large | String |  no  | large |
 | small | String |  no  | smalll |

---


 
 
 #### [PaymentModeList](#PaymentModeList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cardBrand | String? |  yes  | card_brand |
 | cardNumber | String? |  yes  | card_number |
 | fyndVpa | String? |  yes  | fynd_vpa |
 | timeout | Int? |  yes  | timeout |
 | cardName | String? |  yes  | card_name |
 | displayName | String? |  yes  | display name |
 | expYear | Int? |  yes  | exp_year |
 | cardId | String? |  yes  | card_id |
 | expired | Boolean? |  yes  | expired |
 | nickname | String? |  yes  | nickname |
 | retryCount | Int? |  yes  | retry_count |
 | cardToken | String? |  yes  | card_token |
 | merchantCode | String? |  yes  | merchant code |
 | logoUrl | [PaymentModeLogo](#PaymentModeLogo)? |  yes  | Logo |
 | expMonth | Int? |  yes  | exp_month |
 | code | String? |  yes  | code |
 | cardReference | String? |  yes  | card_reference |
 | name | String? |  yes  | name |
 | intentAppErrorList | ArrayList<String>? |  yes  | intent_app_error_list |
 | cardFingerprint | String? |  yes  | card_fingerprint |
 | cardType | String? |  yes  | card_type |
 | cardBrandImage | String? |  yes  | card_brand_image |
 | cardIsin | String? |  yes  | card_isin |
 | displayPriority | Int? |  yes  | Dispaly Priority |
 | aggregatorName | String |  no  | aggregator_name |
 | cardIssuer | String? |  yes  | card_issuer |
 | intentFlow | String? |  yes  | intent_flow |

---


 
 
 #### [RootPaymentMode](#RootPaymentMode)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | anonymousEnable | Boolean? |  yes  | Annonymous card flag |
 | addCardEnabled | Boolean? |  yes  | Annonymous card flag |
 | displayPriority | Int |  no  | Dispaly Priority |
 | aggregatorName | String? |  yes  | Dispaly Priority |
 | displayName | String |  no  | Payment mode display name |
 | list | ArrayList<[PaymentModeList](#PaymentModeList)>? |  yes  | Payment mode |
 | name | String |  no  | Payment mode name |

---


 
 
 #### [PaymentOptions](#PaymentOptions)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | paymentOption | ArrayList<[RootPaymentMode](#RootPaymentMode)> |  no  | Payment options |

---


 
 
 #### [PaymentOptionsResponse](#PaymentOptionsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | paymentOptions | [PaymentOptions](#PaymentOptions) |  no  | Payment options |
 | success | Boolean |  no  | Response is successful or not |

---


 
 
 #### [PayoutsResponse](#PayoutsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uniqueTransferNo | HashMap<String,Any> |  no  | display priority of the payment mode |
 | transferType | String |  no  | transafer type |
 | moreAttributes | HashMap<String,Any> |  no  | bank details object |
 | customers | HashMap<String,Any> |  no  | customers details object |
 | isActive | Boolean |  no  | Enable/DIsable Flag Payout |
 | isDefault | Boolean |  no  | default or not  |
 | payoutsAggregators | ArrayList<HashMap<String,Any>> |  no  | payout aggregator object |

---


 
 
 #### [PayoutBankDetails](#PayoutBankDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ifscCode | String |  no  |  |
 | pincode | Int? |  yes  |  |
 | accountHolder | String? |  yes  |  |
 | city | String? |  yes  |  |
 | accountType | String |  no  |  |
 | country | String? |  yes  |  |
 | bankName | String? |  yes  |  |
 | state | String? |  yes  |  |
 | branchName | String? |  yes  |  |
 | accountNo | String? |  yes  |  |

---


 
 
 #### [PayoutRequest](#PayoutRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | transferType | String |  no  | transafer type |
 | uniqueExternalId | String |  no  | Unique Id of Payout |
 | aggregator | String |  no  | Aggregator Name |
 | users | HashMap<String,Any> |  no  | payout users object |
 | isActive | Boolean |  no  | Enable/Disable Flag Payout |
 | bankDetails | [PayoutBankDetails](#PayoutBankDetails) |  no  | payout bank details object |

---


 
 
 #### [PayoutResponse](#PayoutResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uniqueTransferNo | String |  no  | unique transfer no |
 | payouts | HashMap<String,Any> |  no  | payout  object |
 | transferType | String |  no  | transfer type |
 | created | Boolean |  no  | created flag |
 | aggregator | String |  no  | Aggregator Name |
 | users | HashMap<String,Any> |  no  | users details object |
 | isActive | Boolean |  no  | Enable/DIsable Flag Payout |
 | paymentStatus | String |  no  | status of payment |
 | bankDetails | HashMap<String,Any> |  no  | payout bank_details object |
 | success | Boolean |  no  | Response is successful or not |

---


 
 
 #### [UpdatePayoutResponse](#UpdatePayoutResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isDefault | Boolean |  no  | Enable/Disable Default Payout |
 | isActive | Boolean |  no  | Enable/DIsable Flag Payout |
 | success | Boolean |  no  | Response is successful or not |

---


 
 
 #### [UpdatePayoutRequest](#UpdatePayoutRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uniqueExternalId | String |  no  | Unique Id of Payout |
 | isDefault | Boolean |  no  | Enable/Disable Default Payout |
 | isActive | Boolean |  no  | Enable/Disable Flag Payout |

---


 
 
 #### [DeletePayoutResponse](#DeletePayoutResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean |  no  | Response is successful or not |

---


 
 
 #### [SubscriptionPaymentMethodResponse](#SubscriptionPaymentMethodResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | ArrayList<HashMap<String,Any>> |  no  | Subscription Payment Method Object |
 | success | Boolean |  no  | Response is successful or not |

---


 
 
 #### [DeleteSubscriptionPaymentMethodResponse](#DeleteSubscriptionPaymentMethodResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean |  no  | Success or failure. |

---


 
 
 #### [SubscriptionConfigResponse](#SubscriptionConfigResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | config | HashMap<String,Any> |  no  | Aggregator Config |
 | aggregator | String |  no  | Aggregator Name |
 | success | Boolean |  no  | Response is successful or not |

---


 
 
 #### [SaveSubscriptionSetupIntentRequest](#SaveSubscriptionSetupIntentRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uniqueExternalId | String |  no  | Unique id i.e company:id |

---


 
 
 #### [SaveSubscriptionSetupIntentResponse](#SaveSubscriptionSetupIntentResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | HashMap<String,Any> |  no  | Subscription Payment Method Object |
 | success | Boolean |  no  | Response is successful or not |

---


 
 
 #### [BeneficiaryModeDetails](#BeneficiaryModeDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ifscCode | String |  no  | Ifsc Code of the Account |
 | email | String |  no  | Email of the Account Holder |
 | accountHolder | String |  no  | Name of the Account Holder |
 | comment | String? |  yes  | Remarks added by The user |
 | mobile | String |  no  | Moblie Number of the User |
 | address | String? |  yes  | Address of the User |
 | bankName | String |  no  | Bank Name of the Account |
 | vpa | String? |  yes  |  |
 | wallet | String? |  yes  |  |
 | branchName | String |  no  | Branch Name of the Account |
 | accountNo | String |  no  | Account NUmber of the Account Holder |

---


 
 
 #### [AddBeneficiaryDetailsRequest](#AddBeneficiaryDetailsRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | otp | String? |  yes  |  |
 | shipmentId | String |  no  | Shipment Id of the respective Merchant Order Id |
 | orderId | String |  no  | Merchant Order Id |
 | delights | Boolean |  no  | True if  beneficiary to be added by delights or False if by User |
 | requestId | String? |  yes  |  |
 | details | [BeneficiaryModeDetails](#BeneficiaryModeDetails) |  no  | Beneficiary bank details |
 | transferMode | String |  no  | Transfer Mode of the Beneficiary to be added |

---


 
 
 #### [RefundAccountResponse](#RefundAccountResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String |  no  | Response message |
 | data | HashMap<String,Any>? |  yes  | Refund account data. |
 | success | Boolean |  no  | Success or failure flag. |

---


 
 
 #### [NotFoundResourceError](#NotFoundResourceError)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String |  no  | Not Found |
 | code | String |  no  | Bad Request Data |
 | success | Boolean |  no  | Response is successful or not |

---


 
 
 #### [IfscCodeResponse](#IfscCodeResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | bankName | String |  no  | Bank Name Of Account |
 | branchName | String |  no  | Branch Name Of Account |
 | success | Boolean? |  yes  | Response is successful or not |

---


 
 
 #### [OrderBeneficiaryDetails](#OrderBeneficiaryDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | createdOn | String |  no  | Creation Date of Beneficiary |
 | accountHolder | String |  no  | Account Holder Name |
 | mobile | Boolean? |  yes  | MObile no of User |
 | modifiedOn | String |  no  | MOdification Date of Beneficiary |
 | displayName | String |  no  | Display Name Of Account |
 | email | String |  no  | EMail of User |
 | comment | Boolean? |  yes  | Remarks |
 | beneficiaryId | String |  no  | Benenficiary Id |
 | isActive | Boolean |  no  | Boolean Flag whether Beneficiary set or not |
 | address | String |  no  | Address of User |
 | subtitle | String |  no  | SHort Title Of Account |
 | transferMode | String |  no  | Transfer Mode Of Account |
 | ifscCode | String |  no  | Ifsc Code Of Account |
 | title | String |  no  | Title Of Account |
 | id | Int |  no  |   |
 | branchName | Boolean? |  yes  | Branch Name Of Account |
 | accountNo | String |  no  | Account Number |
 | delightsUserName | String |  no  | User Id Who filled the Beneficiary  |
 | bankName | String |  no  | Bank Name Of Account |

---


 
 
 #### [OrderBeneficiaryResponse](#OrderBeneficiaryResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | beneficiaries | ArrayList<[OrderBeneficiaryDetails](#OrderBeneficiaryDetails)> |  no  | All Beneficiaries Of An Order |
 | showBeneficiaryDetails | Boolean? |  yes  | Show beneficiary details or not. |

---


 
 
 #### [PaymentConfirmationMode](#PaymentConfirmationMode)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  | Payment mode name |
 | amount | Double |  no  | Payment amount |
 | mode | String |  no  | Payment mode |
 | meta | HashMap<String,Any>? |  yes  | Payment meta i.e payment id, order id, gateway |

---


 
 
 #### [PaymentConfirmationRequest](#PaymentConfirmationRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | paymentMethods | ArrayList<[PaymentConfirmationMode](#PaymentConfirmationMode)> |  no  |  |
 | orderId | String |  no  | Unique order id |

---


 
 
 #### [PaymentConfirmationResponse](#PaymentConfirmationResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String |  no  | Message |
 | orderId | String |  no  | Unique order id |
 | success | Boolean |  no  | Payment confirmation updated or not. |

---




 
 
 #### [GetActivityStatus](#GetActivityStatus)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | activityHistory | [ActivityHistory](#ActivityHistory) |  no  |  |

---


 
 
 #### [ActivityHistory](#ActivityHistory)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | createdat | String? |  yes  |  |
 | message | String? |  yes  |  |
 | type | String? |  yes  |  |
 | user | String? |  yes  |  |

---


 
 
 #### [FailedOrders](#FailedOrders)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | orders | [FailOrder](#FailOrder) |  no  |  |

---


 
 
 #### [FailOrder](#FailOrder)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | updatedAt | String? |  yes  |  |
 | id | String? |  yes  |  |
 | reason | String? |  yes  |  |
 | marketplaceOrder | [MarketplaceOrder](#MarketplaceOrder)? |  yes  |  |
 | marketplaceOrderId | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | appId | String? |  yes  |  |
 | marketplace | String? |  yes  |  |
 | companyId | Int? |  yes  |  |

---


 
 
 #### [MarketplaceOrder](#MarketplaceOrder)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | orderStatusUrl | String? |  yes  |  |
 | adminGraphqlApiId | String? |  yes  |  |
 | email | String? |  yes  |  |
 | test | Boolean? |  yes  |  |
 | note | String? |  yes  |  |
 | totalPrice | String? |  yes  |  |
 | appId | Int? |  yes  |  |
 | totalDiscountsSet | [TotalDiscountsSet](#TotalDiscountsSet)? |  yes  |  |
 | totalPriceSet | [TotalPriceSet](#TotalPriceSet)? |  yes  |  |
 | totalTaxSet | [TotalTaxSet](#TotalTaxSet)? |  yes  |  |
 | gateway | String? |  yes  |  |
 | name | String? |  yes  |  |
 | subtotalPriceSet | [SubtotalPriceSet](#SubtotalPriceSet)? |  yes  |  |
 | number | Int? |  yes  |  |
 | buyerAcceptsMarketing | Boolean? |  yes  |  |
 | contactEmail | String? |  yes  |  |
 | token | String? |  yes  |  |
 | sourceName | String? |  yes  |  |
 | paymentGatewayNames | ArrayList<Any>? |  yes  |  |
 | presentmentCurrency | String? |  yes  |  |
 | subtotalPrice | String? |  yes  |  |
 | processedAt | String? |  yes  |  |
 | orderNumber | Int? |  yes  |  |
 | totalTipReceived | String? |  yes  |  |
 | id | Int? |  yes  |  |
 | confirmed | Boolean? |  yes  |  |
 | currency | String? |  yes  |  |
 | totalLineItemsPrice | String? |  yes  |  |
 | lineItems | [LineItems](#LineItems)? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | totalWeight | Int? |  yes  |  |
 | billingAddress | [BillingAddress](#BillingAddress)? |  yes  |  |
 | totalShippingPriceSet | [TotalShippingPriceSet](#TotalShippingPriceSet)? |  yes  |  |
 | customer | [Customer](#Customer)? |  yes  |  |
 | totalDiscounts | String? |  yes  |  |
 | totalLineItemsPriceSet | [TotalLineItemsPriceSet](#TotalLineItemsPriceSet)? |  yes  |  |
 | tags | String? |  yes  |  |
 | totalPriceUsd | String? |  yes  |  |
 | userId | Int? |  yes  |  |
 | totalTax | String? |  yes  |  |
 | processingMethod | String? |  yes  |  |
 | shippingAddress | [OrderShippingAddress](#OrderShippingAddress)? |  yes  |  |
 | taxesIncluded | Boolean? |  yes  |  |
 | financialStatus | String? |  yes  |  |

---


 
 
 #### [TotalDiscountsSet](#TotalDiscountsSet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | presentmentMoney | [PresentmentMoney](#PresentmentMoney)? |  yes  |  |
 | shopMoney | [ShopMoney](#ShopMoney)? |  yes  |  |

---


 
 
 #### [PresentmentMoney](#PresentmentMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [ShopMoney](#ShopMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [TotalPriceSet](#TotalPriceSet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | shopMoney | [TotalPriceSetShopMoney](#TotalPriceSetShopMoney)? |  yes  |  |
 | presentmentMoney | [TotalPriceSetPresentmentMoney](#TotalPriceSetPresentmentMoney)? |  yes  |  |

---


 
 
 #### [TotalPriceSetShopMoney](#TotalPriceSetShopMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [TotalPriceSetPresentmentMoney](#TotalPriceSetPresentmentMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [TotalTaxSet](#TotalTaxSet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | shopMoney | [TotalTaxSetShopMoney](#TotalTaxSetShopMoney)? |  yes  |  |
 | presentmentMoney | [TotalTaxSetPresentmentMoney](#TotalTaxSetPresentmentMoney)? |  yes  |  |

---


 
 
 #### [TotalTaxSetShopMoney](#TotalTaxSetShopMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [TotalTaxSetPresentmentMoney](#TotalTaxSetPresentmentMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [SubtotalPriceSet](#SubtotalPriceSet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | shopMoney | [SubtotalPriceSetShopMoney](#SubtotalPriceSetShopMoney)? |  yes  |  |
 | presentmentMoney | [SubtotalPriceSetPresentmentMoney](#SubtotalPriceSetPresentmentMoney)? |  yes  |  |

---


 
 
 #### [SubtotalPriceSetShopMoney](#SubtotalPriceSetShopMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [SubtotalPriceSetPresentmentMoney](#SubtotalPriceSetPresentmentMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [LineItems](#LineItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sku | String? |  yes  |  |
 | fulfillableQuantity | Int? |  yes  |  |
 | grams | Int? |  yes  |  |
 | totalDiscount | String? |  yes  |  |
 | article | [LineItemsArticle](#LineItemsArticle)? |  yes  |  |
 | title | String? |  yes  |  |
 | variantInventoryManagement | String? |  yes  |  |
 | id | Int? |  yes  |  |
 | variantId | Int? |  yes  |  |
 | variantTitle | String? |  yes  |  |
 | productExists | Boolean? |  yes  |  |
 | price | String? |  yes  |  |
 | adminGraphqlApiId | String? |  yes  |  |
 | quantity | Int? |  yes  |  |
 | vendor | String? |  yes  |  |
 | fulfillmentService | String? |  yes  |  |
 | taxable | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | productId | Int? |  yes  |  |
 | priceSet | [PriceSet](#PriceSet)? |  yes  |  |
 | taxLines | [TaxLines](#TaxLines)? |  yes  |  |
 | requiresShipping | Boolean? |  yes  |  |
 | giftCard | Boolean? |  yes  |  |
 | totalDiscountSet | [TotalDiscountSet](#TotalDiscountSet)? |  yes  |  |

---


 
 
 #### [LineItemsArticle](#LineItemsArticle)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | quantities | [Quantities](#Quantities)? |  yes  |  |
 | oldArticleUid | String? |  yes  |  |
 | totalQuantity | Int? |  yes  |  |
 | manufacturer | [Manufacturer](#Manufacturer)? |  yes  |  |
 | price | [ArticlePrice](#ArticlePrice)? |  yes  |  |
 | trackInventory | Boolean? |  yes  |  |
 | company | [Company](#Company)? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | dateMeta | [FailOrderDateMeta](#FailOrderDateMeta)? |  yes  |  |
 | fragile | Boolean? |  yes  |  |
 | marketplaceIdentifiers | [MarketplaceIdentifiers](#MarketplaceIdentifiers)? |  yes  |  |
 | size | String? |  yes  |  |
 | isSet | Boolean? |  yes  |  |
 | dimension | [Dimension](#Dimension)? |  yes  |  |
 | weight | [Weight](#Weight)? |  yes  |  |
 | store | [Store](#Store)? |  yes  |  |
 | meta | [ArticleMeta](#ArticleMeta)? |  yes  |  |
 | uid | String? |  yes  |  |
 | brand | [ArticleBrand](#ArticleBrand)? |  yes  |  |
 | itemId | Int? |  yes  |  |
 | fyndArticleCode | String? |  yes  |  |
 | id | String? |  yes  |  |
 | identifier | [LineItemsArticleIdentifier](#LineItemsArticleIdentifier)? |  yes  |  |
 | sellerIdentifier | String? |  yes  |  |
 | fyndItemCode | String? |  yes  |  |
 | countryOfOrigin | String? |  yes  |  |

---


 
 
 #### [Quantities](#Quantities)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | notAvailable | [NotAvailable](#NotAvailable)? |  yes  |  |
 | sellable | [Sellable](#Sellable)? |  yes  |  |
 | orderCommitted | [OrderCommitted](#OrderCommitted)? |  yes  |  |
 | damaged | [Damaged](#Damaged)? |  yes  |  |

---


 
 
 #### [NotAvailable](#NotAvailable)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | count | Int? |  yes  |  |
 | updatedAt | String? |  yes  |  |

---


 
 
 #### [Sellable](#Sellable)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | count | Int? |  yes  |  |
 | updatedAt | String? |  yes  |  |

---


 
 
 #### [OrderCommitted](#OrderCommitted)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | count | Int? |  yes  |  |
 | updatedAt | String? |  yes  |  |

---


 
 
 #### [Damaged](#Damaged)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | updatedAt | String? |  yes  |  |
 | count | Int? |  yes  |  |

---


 
 
 #### [Manufacturer](#Manufacturer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isDefault | Boolean? |  yes  |  |
 | address | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [ArticlePrice](#ArticlePrice)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | marked | Int? |  yes  |  |
 | currency | String? |  yes  |  |
 | effective | Int? |  yes  |  |
 | transfer | Int? |  yes  |  |

---


 
 
 #### [Company](#Company)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |
 | companyType | String? |  yes  |  |
 | businessType | String? |  yes  |  |
 | companyName | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | panNo | String? |  yes  |  |
 | returnAllowed | Boolean? |  yes  |  |
 | meta | String? |  yes  |  |
 | exchangeAllowed | Boolean? |  yes  |  |
 | agreementStartDate | String? |  yes  |  |
 | exchangeWithinDays | Int? |  yes  |  |
 | paymentProcesingCharge | Int? |  yes  |  |
 | fyndAFitAvailable | Boolean? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | returnWithinDays | Int? |  yes  |  |

---


 
 
 #### [FailOrderDateMeta](#FailOrderDateMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | addedOnStore | String? |  yes  |  |
 | inventoryUpdatedOn | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |

---


 
 
 #### [MarketplaceIdentifiers](#MarketplaceIdentifiers)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tatacliqLuxury | [TatacliqLuxury](#TatacliqLuxury)? |  yes  |  |

---


 
 
 #### [TatacliqLuxury](#TatacliqLuxury)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sku | String? |  yes  |  |

---


 
 
 #### [Dimension](#Dimension)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | height | Int? |  yes  |  |
 | width | Int? |  yes  |  |
 | unit | String? |  yes  |  |
 | length | Int? |  yes  |  |
 | isDefault | Boolean? |  yes  |  |

---


 
 
 #### [Weight](#Weight)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isDefault | Boolean? |  yes  |  |
 | unit | String? |  yes  |  |
 | shipping | Int? |  yes  |  |

---


 
 
 #### [Store](#Store)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |

---


 
 
 #### [ArticleMeta](#ArticleMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | service | String? |  yes  |  |

---


 
 
 #### [ArticleBrand](#ArticleBrand)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | id | Int? |  yes  |  |

---


 
 
 #### [LineItemsArticleIdentifier](#LineItemsArticleIdentifier)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | skuCode | String? |  yes  |  |

---


 
 
 #### [PriceSet](#PriceSet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | shopMoney | [PriceSetShopMoney](#PriceSetShopMoney)? |  yes  |  |
 | presentmentMoney | [PriceSetPresentmentMoney](#PriceSetPresentmentMoney)? |  yes  |  |

---


 
 
 #### [PriceSetShopMoney](#PriceSetShopMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [PriceSetPresentmentMoney](#PriceSetPresentmentMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [TaxLines](#TaxLines)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | price | String? |  yes  |  |
 | rate | Int? |  yes  |  |
 | priceSet | [TaxLinesPriceSet](#TaxLinesPriceSet)? |  yes  |  |

---


 
 
 #### [TaxLinesPriceSet](#TaxLinesPriceSet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | shopMoney | [TaxLinesPriceSetShopMoney](#TaxLinesPriceSetShopMoney)? |  yes  |  |
 | presentmentMoney | [TaxLinesPriceSetPresentmentMoney](#TaxLinesPriceSetPresentmentMoney)? |  yes  |  |

---


 
 
 #### [TaxLinesPriceSetShopMoney](#TaxLinesPriceSetShopMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [TaxLinesPriceSetPresentmentMoney](#TaxLinesPriceSetPresentmentMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | currencyCode | String? |  yes  |  |
 | amount | String? |  yes  |  |

---


 
 
 #### [TotalDiscountSet](#TotalDiscountSet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | presentmentMoney | [TotalDiscountSetPresentmentMoney](#TotalDiscountSetPresentmentMoney)? |  yes  |  |
 | shopMoney | [TotalDiscountSetShopMoney](#TotalDiscountSetShopMoney)? |  yes  |  |

---


 
 
 #### [TotalDiscountSetPresentmentMoney](#TotalDiscountSetPresentmentMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [TotalDiscountSetShopMoney](#TotalDiscountSetShopMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [BillingAddress](#BillingAddress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | address1 | String? |  yes  |  |
 | city | String? |  yes  |  |
 | zip | String? |  yes  |  |
 | lastName | String? |  yes  |  |
 | address2 | String? |  yes  |  |
 | longitude | Double? |  yes  |  |
 | provinceCode | String? |  yes  |  |
 | phone | String? |  yes  |  |
 | company | String? |  yes  |  |
 | latitude | Double? |  yes  |  |
 | name | String? |  yes  |  |
 | country | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | firstName | String? |  yes  |  |
 | province | String? |  yes  |  |

---


 
 
 #### [TotalShippingPriceSet](#TotalShippingPriceSet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | shopMoney | [TotalShippingPriceSetShopMoney](#TotalShippingPriceSetShopMoney)? |  yes  |  |
 | presentmentMoney | [TotalShippingPriceSetPresentmentMoney](#TotalShippingPriceSetPresentmentMoney)? |  yes  |  |

---


 
 
 #### [TotalShippingPriceSetShopMoney](#TotalShippingPriceSetShopMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [TotalShippingPriceSetPresentmentMoney](#TotalShippingPriceSetPresentmentMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [Customer](#Customer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | createdAt | String? |  yes  |  |
 | id | Int? |  yes  |  |
 | lastName | String? |  yes  |  |
 | state | String? |  yes  |  |
 | lastOrderId | Int? |  yes  |  |
 | note | String? |  yes  |  |
 | verifiedEmail | Boolean? |  yes  |  |
 | phone | String? |  yes  |  |
 | acceptsMarketing | Boolean? |  yes  |  |
 | firstName | String? |  yes  |  |
 | tags | String? |  yes  |  |
 | lastOrderName | String? |  yes  |  |
 | ordersCount | Int? |  yes  |  |
 | totalSpent | String? |  yes  |  |
 | taxExempt | Boolean? |  yes  |  |
 | currency | String? |  yes  |  |
 | acceptsMarketingUpdatedAt | String? |  yes  |  |
 | email | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | adminGraphqlApiId | String? |  yes  |  |
 | defaultAddress | [DefaultAddress](#DefaultAddress)? |  yes  |  |

---


 
 
 #### [DefaultAddress](#DefaultAddress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | lastName | String? |  yes  |  |
 | name | String? |  yes  |  |
 | provinceCode | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | isDefault | Boolean? |  yes  |  |
 | id | Int? |  yes  |  |
 | customerId | Int? |  yes  |  |
 | firstName | String? |  yes  |  |
 | address1 | String? |  yes  |  |
 | phone | String? |  yes  |  |
 | countryName | String? |  yes  |  |
 | company | String? |  yes  |  |
 | address2 | String? |  yes  |  |
 | city | String? |  yes  |  |
 | province | String? |  yes  |  |
 | country | String? |  yes  |  |
 | zip | String? |  yes  |  |

---


 
 
 #### [TotalLineItemsPriceSet](#TotalLineItemsPriceSet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | shopMoney | [TotalLineItemsPriceSetShopMoney](#TotalLineItemsPriceSetShopMoney)? |  yes  |  |
 | presentmentMoney | [TotalLineItemsPriceSetPresentmentMoney](#TotalLineItemsPriceSetPresentmentMoney)? |  yes  |  |

---


 
 
 #### [TotalLineItemsPriceSetShopMoney](#TotalLineItemsPriceSetShopMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [TotalLineItemsPriceSetPresentmentMoney](#TotalLineItemsPriceSetPresentmentMoney)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [OrderShippingAddress](#OrderShippingAddress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | address1 | String? |  yes  |  |
 | zip | String? |  yes  |  |
 | address2 | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | country | String? |  yes  |  |
 | lastName | String? |  yes  |  |
 | latitude | Double? |  yes  |  |
 | provinceCode | String? |  yes  |  |
 | firstName | String? |  yes  |  |
 | phone | String? |  yes  |  |
 | province | String? |  yes  |  |
 | longitude | Double? |  yes  |  |
 | city | String? |  yes  |  |
 | company | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [OrderListing](#OrderListing)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[OrderItems](#OrderItems)> |  no  |  |
 | filters | [Filters](#Filters) |  no  |  |
 | nextOrderStatus | HashMap<String,Any> |  no  |  |
 | page | [PlatformOrderPage](#PlatformOrderPage) |  no  |  |
 | appliedFilters | [AppliedFilters](#AppliedFilters) |  no  |  |

---


 
 
 #### [OrderItems](#OrderItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [PlatformOrderUserInfo](#PlatformOrderUserInfo)? |  yes  |  |
 | deliveryAddress | [PlatformDeliveryAddress](#PlatformDeliveryAddress)? |  yes  |  |
 | channel | [Channel](#Channel)? |  yes  |  |
 | id | String? |  yes  |  |
 | application | [PlatformApplication](#PlatformApplication)? |  yes  |  |
 | shipments | [PlatformShipment](#PlatformShipment)? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | totalShipmentsInOrder | Int? |  yes  |  |

---


 
 
 #### [PlatformOrderUserInfo](#PlatformOrderUserInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | mobile | String? |  yes  |  |
 | firstName | String? |  yes  |  |
 | gender | String? |  yes  |  |
 | email | String? |  yes  |  |
 | lastName | String? |  yes  |  |
 | isAnonymousUser | Boolean? |  yes  |  |
 | uid | Int? |  yes  |  |
 | avisUserId | String? |  yes  |  |

---


 
 
 #### [PlatformDeliveryAddress](#PlatformDeliveryAddress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | area | String? |  yes  |  |
 | state | String? |  yes  |  |
 | country | String? |  yes  |  |
 | version | String? |  yes  |  |
 | address1 | String? |  yes  |  |
 | latitude | Double? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | city | String? |  yes  |  |
 | landmark | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | name | String? |  yes  |  |
 | address | String? |  yes  |  |
 | phone | String? |  yes  |  |
 | longitude | Double? |  yes  |  |
 | addressType | String? |  yes  |  |
 | email | String? |  yes  |  |
 | pincode | String? |  yes  |  |
 | address2 | String? |  yes  |  |
 | contactPerson | String? |  yes  |  |
 | addressCategory | String? |  yes  |  |

---


 
 
 #### [Channel](#Channel)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | logo | String? |  yes  |  |

---


 
 
 #### [PlatformApplication](#PlatformApplication)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |

---


 
 
 #### [PlatformShipment](#PlatformShipment)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | [PlatformShipmentStatus](#PlatformShipmentStatus)? |  yes  |  |
 | bags | [Bags](#Bags)? |  yes  |  |
 | prices | [ShipmentPrices](#ShipmentPrices)? |  yes  |  |
 | id | String? |  yes  |  |
 | gst | [ShipmentGst](#ShipmentGst)? |  yes  |  |
 | totalShipmentBags | Int? |  yes  |  |

---


 
 
 #### [PlatformShipmentStatus](#PlatformShipmentStatus)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |
 | bagList | ArrayList<Int>? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | status | String? |  yes  |  |
 | name | String? |  yes  |  |
 | progress | Int? |  yes  |  |
 | shipmentId | String? |  yes  |  |
 | currentShipmentStatus | String? |  yes  |  |
 | colorCode | String? |  yes  |  |

---


 
 
 #### [Bags](#Bags)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | item | [BagItem](#BagItem)? |  yes  |  |
 | id | Int? |  yes  |  |

---


 
 
 #### [BagItem](#BagItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |
 | size | String? |  yes  |  |
 | slugKey | String? |  yes  |  |
 | canReturn | Boolean? |  yes  |  |
 | brandId | Int? |  yes  |  |
 | l2Category | ArrayList<String>? |  yes  |  |
 | name | String? |  yes  |  |
 | code | String? |  yes  |  |
 | canCancel | Boolean? |  yes  |  |
 | attributes | [BagItemAttributes](#BagItemAttributes)? |  yes  |  |
 | l3CategoryName | String? |  yes  |  |
 | l3Category | Int? |  yes  |  |
 | l1Category | ArrayList<String>? |  yes  |  |
 | image | ArrayList<String>? |  yes  |  |
 | brand | String? |  yes  |  |
 | lastUpdatedAt | String? |  yes  |  |

---


 
 
 #### [BagItemAttributes](#BagItemAttributes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | itemCode | String? |  yes  |  |
 | brandName | String? |  yes  |  |
 | countryOfOrigin | String? |  yes  |  |

---


 
 
 #### [ShipmentPrices](#ShipmentPrices)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | refundAmount | Double? |  yes  |  |
 | cashbackApplied | Double? |  yes  |  |
 | transferPrice | Double? |  yes  |  |
 | couponValue | Double? |  yes  |  |
 | amountPaid | Double? |  yes  |  |
 | deliveryCharge | Double? |  yes  |  |
 | couponEffectiveDiscount | Double? |  yes  |  |
 | codCharges | Double? |  yes  |  |
 | refundCredit | Double? |  yes  |  |
 | addedToFyndCash | Boolean? |  yes  |  |
 | gstTaxPercentage | Double? |  yes  |  |
 | priceMarked | Double? |  yes  |  |
 | priceEffective | Double? |  yes  |  |
 | discount | Double? |  yes  |  |
 | promotionEffectiveDiscount | Double? |  yes  |  |
 | amountPaidRoundoff | Double? |  yes  |  |
 | fyndCredits | Double? |  yes  |  |
 | brandCalculatedAmount | Double? |  yes  |  |
 | cashback | Double? |  yes  |  |
 | valueOfGood | Double? |  yes  |  |

---


 
 
 #### [Payments](#Payments)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isActive | Boolean? |  yes  |  |
 | displayName | String? |  yes  |  |
 | logo | String? |  yes  |  |
 | source | String? |  yes  |  |
 | sourceNickname | String? |  yes  |  |
 | displayPriority | Int? |  yes  |  |
 | id | Int? |  yes  |  |
 | mode | String? |  yes  |  |
 | paymentIdentifier | String? |  yes  |  |

---


 
 
 #### [Filters](#Filters)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | stage | [Stage](#Stage)? |  yes  |  |
 | stages | [Stages](#Stages)? |  yes  |  |

---


 
 
 #### [Stage](#Stage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | text | String? |  yes  |  |
 | value | String? |  yes  |  |
 | isDefault | Boolean? |  yes  |  |
 | filters | [StagesFilters](#StagesFilters)? |  yes  |  |

---


 
 
 #### [StagesFilters](#StagesFilters)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | text | String? |  yes  |  |
 | value | String? |  yes  |  |
 | type | String? |  yes  |  |
 | options | [Options](#Options)? |  yes  |  |

---


 
 
 #### [Options](#Options)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | text | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [PlatformOrderPage](#PlatformOrderPage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | next | String? |  yes  |  |
 | previous | String? |  yes  |  |
 | type | String? |  yes  |  |
 | size | Int? |  yes  |  |
 | current | Int? |  yes  |  |
 | hasNext | Boolean? |  yes  |  |
 | total | Int? |  yes  |  |
 | itemTotal | [ItemTotal](#ItemTotal)? |  yes  |  |

---


 
 
 #### [AppliedFilters](#AppliedFilters)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | stage | String? |  yes  |  |
 | stores | ArrayList<String>? |  yes  |  |
 | fromDate | String? |  yes  |  |
 | toDate | String? |  yes  |  |

---


 
 
 #### [OrderDetails](#OrderDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[OrderPicklistListing](#OrderPicklistListing)> |  no  |  |
 | page | [PlatformOrderPage](#PlatformOrderPage) |  no  |  |
 | filters | [Filters](#Filters) |  no  |  |
 | nextOrderStatus | HashMap<String,Any> |  no  |  |
 | appliedFilters | [AppliedFilters](#AppliedFilters) |  no  |  |

---


 
 
 #### [OrderDetailsItem](#OrderDetailsItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [PlatformOrderUserInfo](#PlatformOrderUserInfo)? |  yes  |  |
 | deliveryAddress | [PlatformDeliveryAddress](#PlatformDeliveryAddress)? |  yes  |  |
 | channel | [Channel](#Channel)? |  yes  |  |
 | fyndstoreEmp | HashMap<String,Any>? |  yes  |  |
 | orderingStore | HashMap<String,Any>? |  yes  |  |
 | breakupValues | [PlatformBreakupValues](#PlatformBreakupValues)? |  yes  |  |
 | id | String? |  yes  |  |
 | application | [PlatformApplication](#PlatformApplication)? |  yes  |  |
 | shipments | [PlatformShipmentDetails](#PlatformShipmentDetails)? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | totalShipmentsInOrder | Int? |  yes  |  |
 | payments | [ItemsPayments](#ItemsPayments)? |  yes  |  |

---


 
 
 #### [PlatformBreakupValues](#PlatformBreakupValues)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | value | Double? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [ArticleAssignment](#ArticleAssignment)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | strategy | String? |  yes  |  |
 | level | String? |  yes  |  |

---


 
 
 #### [PlatformShipmentDetails](#PlatformShipmentDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | [PlatformShipmentDetailsStatus](#PlatformShipmentDetailsStatus)? |  yes  |  |
 | bags | [BagsDetails](#BagsDetails)? |  yes  |  |
 | prices | [ShipmentPrices](#ShipmentPrices)? |  yes  |  |
 | breakupValues | [ShipmentBreakupValues](#ShipmentBreakupValues)? |  yes  |  |
 | id | String? |  yes  |  |
 | dpDetails | [DpDetails](#DpDetails)? |  yes  |  |
 | invoice | [ShipmentInvoice](#ShipmentInvoice)? |  yes  |  |
 | fulfillingStore | [PlatformFulfillingStore](#PlatformFulfillingStore)? |  yes  |  |
 | payments | [Payments](#Payments)? |  yes  |  |
 | gst | [ShipmentGst](#ShipmentGst)? |  yes  |  |
 | company | [Company](#Company)? |  yes  |  |
 | brand | [PlatformShipmentDetailsBrand](#PlatformShipmentDetailsBrand)? |  yes  |  |
 | coupon | HashMap<String,Any>? |  yes  |  |
 | orderSource | String? |  yes  |  |
 | isNotFyndSource | Boolean? |  yes  |  |
 | comment | String? |  yes  |  |
 | promise | [Promise](#Promise)? |  yes  |  |
 | trackingDetails | [ShipmentTrackingDetails](#ShipmentTrackingDetails)? |  yes  |  |
 | isFyndCoupon | Boolean? |  yes  |  |
 | orderType | String? |  yes  |  |
 | totalShipmentBags | Int? |  yes  |  |
 | pod | HashMap<String,Any>? |  yes  |  |
 | lockStatus | Boolean? |  yes  |  |
 | orderingChannel | String? |  yes  |  |

---


 
 
 #### [PlatformShipmentDetailsStatus](#PlatformShipmentDetailsStatus)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |
 | bagList | ArrayList<Int>? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | status | String? |  yes  |  |
 | name | String? |  yes  |  |
 | progress | Int? |  yes  |  |
 | shipmentId | String? |  yes  |  |
 | currentShipmentStatus | String? |  yes  |  |
 | colorCode | String? |  yes  |  |

---


 
 
 #### [BagsDetails](#BagsDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | financialBreakup | ArrayList<[BagFinancialBreakup](#BagFinancialBreakup)>? |  yes  |  |
 | status | [BagCurrStatus](#BagCurrStatus)? |  yes  |  |
 | item | [BagItem](#BagItem)? |  yes  |  |
 | article | [BagArticle](#BagArticle)? |  yes  |  |
 | id | Int? |  yes  |  |
 | prices | [BagPrices](#BagPrices)? |  yes  |  |
 | gstDetails | [GstDetails](#GstDetails)? |  yes  |  |
 | breakupValues | [BagBreakupValues](#BagBreakupValues)? |  yes  |  |
 | updateTime | Int? |  yes  |  |
 | currentStatus | [BagCurrentStatus](#BagCurrentStatus)? |  yes  |  |
 | bagStatus | [BagStatus](#BagStatus)? |  yes  |  |

---


 
 
 #### [BagFinancialBreakup](#BagFinancialBreakup)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | valueOfGood | Double? |  yes  |  |
 | hsnCode | String? |  yes  |  |
 | priceEffective | Double? |  yes  |  |
 | codCharges | Double? |  yes  |  |
 | gstFee | String? |  yes  |  |
 | fyndCredits | Double? |  yes  |  |
 | refundAmount | Double? |  yes  |  |
 | cashbackApplied | Double? |  yes  |  |
 | transferPrice | Double? |  yes  |  |
 | amountPaidRoundoff | Double? |  yes  |  |
 | couponValue | Double? |  yes  |  |
 | amountPaid | Double? |  yes  |  |
 | gstTaxPercentage | Double? |  yes  |  |
 | size | String? |  yes  |  |
 | totalUnits | Int? |  yes  |  |
 | discount | Double? |  yes  |  |
 | couponEffectiveDiscount | Double? |  yes  |  |
 | cashback | Double? |  yes  |  |
 | promotionEffectiveDiscount | Double? |  yes  |  |
 | gstTag | String? |  yes  |  |
 | deliveryCharge | Double? |  yes  |  |
 | refundCredit | Double? |  yes  |  |
 | priceMarked | Double? |  yes  |  |
 | identifiers | [Identifiers](#Identifiers)? |  yes  |  |
 | itemName | String? |  yes  |  |
 | addedToFyndCash | Boolean? |  yes  |  |
 | brandCalculatedAmount | Double? |  yes  |  |

---


 
 
 #### [Identifiers](#Identifiers)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ean | String? |  yes  |  |

---


 
 
 #### [BagCurrStatus](#BagCurrStatus)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enableTracking | Boolean? |  yes  |  |
 | isCustomerReturnAllowed | Boolean? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | isReturnable | Boolean? |  yes  |  |
 | canBeCancelled | Boolean? |  yes  |  |

---


 
 
 #### [BagArticle](#BagArticle)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | identifiers | [ArticleIdentifiers](#ArticleIdentifiers)? |  yes  |  |
 | espModified | Boolean? |  yes  |  |
 | isSet | Boolean? |  yes  |  |
 | size | String? |  yes  |  |
 | code | String? |  yes  |  |
 | set | [Set](#Set)? |  yes  |  |
 | sellerIdentifier | String? |  yes  |  |
 | returnConfig | [BagArticleReturnConfig](#BagArticleReturnConfig)? |  yes  |  |
 | id | String? |  yes  |  |
 | uid | String? |  yes  |  |
 | childDetails | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [ArticleIdentifiers](#ArticleIdentifiers)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ean | String? |  yes  |  |

---


 
 
 #### [Set](#Set)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | quantity | Int? |  yes  |  |
 | sizeDistribution | [SetSizeDistribution](#SetSizeDistribution)? |  yes  |  |

---


 
 
 #### [SetSizeDistribution](#SetSizeDistribution)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sizes | [Sizes](#Sizes)? |  yes  |  |

---


 
 
 #### [Sizes](#Sizes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | size | String? |  yes  |  |
 | pieces | Int? |  yes  |  |

---


 
 
 #### [BagArticleReturnConfig](#BagArticleReturnConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | time | Int? |  yes  |  |
 | unit | String? |  yes  |  |
 | returnable | Boolean? |  yes  |  |

---


 
 
 #### [GstDetails](#GstDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brandCalculatedAmount | Double? |  yes  |  |
 | gstFee | String? |  yes  |  |
 | gstTag | String? |  yes  |  |
 | hsnCode | String? |  yes  |  |
 | valueOfGood | Double? |  yes  |  |
 | gstTaxPercentage | Double? |  yes  |  |
 | isDefaultHsnCode | Boolean? |  yes  |  |

---


 
 
 #### [BagBreakupValues](#BagBreakupValues)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | display | String? |  yes  |  |
 | value | Double? |  yes  |  |

---


 
 
 #### [BagCurrentStatus](#BagCurrentStatus)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | updatedAt | String? |  yes  |  |
 | bagStateMapper | [BagStateMapper](#BagStateMapper)? |  yes  |  |
 | status | String? |  yes  |  |
 | stateType | String? |  yes  |  |

---


 
 
 #### [BagStateMapper](#BagStateMapper)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | appStateName | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | displayName | String? |  yes  |  |
 | name | String? |  yes  |  |
 | appDisplayName | String? |  yes  |  |

---


 
 
 #### [BagStatus](#BagStatus)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | String? |  yes  |  |
 | stateType | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | bagStateMapper | [BagStatusBagStateMapper](#BagStatusBagStateMapper)? |  yes  |  |

---


 
 
 #### [BagStatusBagStateMapper](#BagStatusBagStateMapper)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isActive | Boolean? |  yes  |  |
 | displayName | String? |  yes  |  |
 | name | String? |  yes  |  |
 | appDisplayName | String? |  yes  |  |
 | appStateName | String? |  yes  |  |

---


 
 
 #### [BagPrices](#BagPrices)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cashback | Double? |  yes  |  |
 | refundCredit | Double? |  yes  |  |
 | couponValue | Double? |  yes  |  |
 | deliveryCharge | Double? |  yes  |  |
 | fyndCredits | Double? |  yes  |  |
 | priceMarked | Double? |  yes  |  |
 | cashbackApplied | Double? |  yes  |  |
 | valueOfGood | Double? |  yes  |  |
 | amountPaidRoundoff | Double? |  yes  |  |
 | amountPaid | Double? |  yes  |  |
 | codCharges | Double? |  yes  |  |
 | priceEffective | Double? |  yes  |  |
 | refundAmount | Double? |  yes  |  |
 | discount | Double? |  yes  |  |

---


 
 
 #### [ShipmentBreakupValues](#ShipmentBreakupValues)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | display | String? |  yes  |  |
 | value | Double? |  yes  |  |

---


 
 
 #### [DpDetails](#DpDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | gstTag | String? |  yes  |  |

---


 
 
 #### [ShipmentInvoice](#ShipmentInvoice)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | paymentType | String? |  yes  |  |
 | updatedDate | String? |  yes  |  |
 | invoiceUrl | String? |  yes  |  |
 | labelUrl | String? |  yes  |  |
 | paymentMode | String? |  yes  |  |
 | amountToCollect | Double? |  yes  |  |
 | rtoAddress | [RtoAddress](#RtoAddress)? |  yes  |  |

---


 
 
 #### [RtoAddress](#RtoAddress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | id | Int? |  yes  |  |
 | phone | String? |  yes  |  |
 | locationType | String? |  yes  |  |
 | storeAddressJson | [StoreAddressJson](#StoreAddressJson)? |  yes  |  |
 | code | String? |  yes  |  |
 | address1 | String? |  yes  |  |
 | city | String? |  yes  |  |
 | country | String? |  yes  |  |
 | pincode | String? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | contactPerson | String? |  yes  |  |
 | state | String? |  yes  |  |
 | storeEmail | String? |  yes  |  |
 | address2 | String? |  yes  |  |

---


 
 
 #### [StoreAddressJson](#StoreAddressJson)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | country | String? |  yes  |  |
 | latitude | Double? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | area | String? |  yes  |  |
 | state | String? |  yes  |  |
 | addressType | String? |  yes  |  |
 | city | String? |  yes  |  |
 | pincode | String? |  yes  |  |
 | address1 | String? |  yes  |  |
 | address2 | String? |  yes  |  |
 | longitude | Double? |  yes  |  |
 | email | String? |  yes  |  |
 | phone | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | contactPerson | String? |  yes  |  |
 | addressCategory | String? |  yes  |  |
 | version | String? |  yes  |  |
 | landmark | String? |  yes  |  |

---


 
 
 #### [PlatformFulfillingStore](#PlatformFulfillingStore)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | packagingMaterialCount | Int? |  yes  |  |
 | locationType | String? |  yes  |  |
 | code | String? |  yes  |  |
 | city | String? |  yes  |  |
 | meta | [FulfillingStoreMeta](#FulfillingStoreMeta)? |  yes  |  |
 | name | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | address1 | String? |  yes  |  |
 | storeEmail | String? |  yes  |  |
 | isArchived | Boolean? |  yes  |  |
 | state | String? |  yes  |  |
 | address2 | String? |  yes  |  |
 | contactPerson | String? |  yes  |  |
 | phone | String? |  yes  |  |
 | isEnabledForRecon | Boolean? |  yes  |  |
 | fulfillmentChannel | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | id | Int? |  yes  |  |
 | pincode | String? |  yes  |  |
 | brandStoreTags | ArrayList<String>? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | storeAddressJson | [FulfillingStoreStoreAddressJson](#FulfillingStoreStoreAddressJson)? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | loginUsername | String? |  yes  |  |
 | country | String? |  yes  |  |

---


 
 
 #### [FulfillingStoreMeta](#FulfillingStoreMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | additionalContactDetails | [AdditionalContactDetails](#AdditionalContactDetails)? |  yes  |  |
 | documents | [Documents](#Documents)? |  yes  |  |
 | gstNumber | String? |  yes  |  |
 | displayName | String? |  yes  |  |
 | productReturnConfig | [ProductReturnConfig](#ProductReturnConfig)? |  yes  |  |
 | allowDpAssignmentFromFynd | Boolean? |  yes  |  |
 | stage | String? |  yes  |  |
 | timing | [Timing](#Timing)? |  yes  |  |

---


 
 
 #### [AdditionalContactDetails](#AdditionalContactDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | number | ArrayList<String>? |  yes  |  |

---


 
 
 #### [Documents](#Documents)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | gst | [Gst](#Gst)? |  yes  |  |

---


 
 
 #### [Gst](#Gst)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | legalName | String? |  yes  |  |
 | type | String? |  yes  |  |
 | value | String? |  yes  |  |
 | verified | Boolean? |  yes  |  |

---


 
 
 #### [ProductReturnConfig](#ProductReturnConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | onSameStore | Boolean? |  yes  |  |

---


 
 
 #### [Timing](#Timing)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | opening | [Opening](#Opening)? |  yes  |  |
 | weekday | String? |  yes  |  |
 | open | Boolean? |  yes  |  |
 | closing | [Closing](#Closing)? |  yes  |  |

---


 
 
 #### [Opening](#Opening)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | minute | Int? |  yes  |  |
 | hour | Int? |  yes  |  |

---


 
 
 #### [Closing](#Closing)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | hour | Int? |  yes  |  |
 | minute | Int? |  yes  |  |

---


 
 
 #### [FulfillingStoreStoreAddressJson](#FulfillingStoreStoreAddressJson)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | address2 | String? |  yes  |  |
 | area | String? |  yes  |  |
 | email | String? |  yes  |  |
 | phone | String? |  yes  |  |
 | state | String? |  yes  |  |
 | contactPerson | String? |  yes  |  |
 | country | String? |  yes  |  |
 | pincode | String? |  yes  |  |
 | version | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | addressType | String? |  yes  |  |
 | city | String? |  yes  |  |
 | address1 | String? |  yes  |  |
 | landmark | String? |  yes  |  |
 | latitude | Double? |  yes  |  |
 | longitude | Double? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | addressCategory | String? |  yes  |  |

---


 
 
 #### [ShipmentGst](#ShipmentGst)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brandCalculatedAmount | Double? |  yes  |  |
 | valueOfGood | Double? |  yes  |  |
 | gstFee | Double? |  yes  |  |

---


 
 
 #### [PlatformShipmentDetailsBrand](#PlatformShipmentDetailsBrand)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | creditNoteAllowed | Boolean? |  yes  |  |
 | brandName | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | id | Int? |  yes  |  |
 | isVirtualInvoice | Boolean? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | logo | String? |  yes  |  |

---


 
 
 #### [Promise](#Promise)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | timestamp | [Timestamp](#Timestamp)? |  yes  |  |

---


 
 
 #### [Timestamp](#Timestamp)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | min | String? |  yes  |  |
 | max | String? |  yes  |  |

---


 
 
 #### [ShipmentTrackingDetails](#ShipmentTrackingDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | String? |  yes  |  |
 | time | String? |  yes  |  |
 | isPassed | Boolean? |  yes  |  |
 | isCurrent | Boolean? |  yes  |  |

---


 
 
 #### [ItemsPayments](#ItemsPayments)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | displayPriority | Int? |  yes  |  |
 | id | Int? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | displayName | String? |  yes  |  |
 | logo | String? |  yes  |  |
 | paymentIdentifier | String? |  yes  |  |
 | sourceNickname | String? |  yes  |  |
 | mode | String? |  yes  |  |
 | source | String? |  yes  |  |

---


 
 
 #### [PlatformOrderDetailsPage](#PlatformOrderDetailsPage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | next | String? |  yes  |  |
 | previous | String? |  yes  |  |

---


 
 
 #### [OrderLanesCount](#OrderLanesCount)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | stages | ArrayList<[StageItem](#StageItem)> |  no  |  |

---


 
 
 #### [StageItem](#StageItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | count | Int? |  yes  |  |
 | text | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [UpdateOrderReprocessResponse](#UpdateOrderReprocessResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | String |  no  |  |

---


 
 
 #### [PlatformOrderTrack](#PlatformOrderTrack)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean |  no  |  |
 | requestId | String |  no  |  |
 | message | String |  no  |  |
 | mobile | String |  no  |  |
 | countryCode | String |  no  |  |
 | resendTimer | Int |  no  |  |
 | resendToken | String? |  yes  |  |

---


 
 
 #### [OrderPicklistListing](#OrderPicklistListing)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [PlatformOrderUserInfo](#PlatformOrderUserInfo)? |  yes  |  |
 | deliveryAddress | [PlatformDeliveryAddress](#PlatformDeliveryAddress)? |  yes  |  |
 | channel | [Channel](#Channel)? |  yes  |  |
 | fyndstoreEmp | HashMap<String,Any>? |  yes  |  |
 | orderingStore | HashMap<String,Any>? |  yes  |  |
 | breakupValues | [PlatformBreakupValues](#PlatformBreakupValues)? |  yes  |  |
 | id | String? |  yes  |  |
 | application | [PlatformApplication](#PlatformApplication)? |  yes  |  |
 | shipments | [PlatformShipmentDetails](#PlatformShipmentDetails)? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | totalShipmentsInOrder | Int? |  yes  |  |
 | payments | [ItemsPayments](#ItemsPayments)? |  yes  |  |

---


 
 
 #### [Stages](#Stages)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | text | String? |  yes  |  |
 | value | String? |  yes  |  |
 | isDefault | Boolean? |  yes  |  |
 | filters | [StagesFilters](#StagesFilters)? |  yes  |  |

---


 
 
 #### [ItemTotal](#ItemTotal)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | new | Int? |  yes  |  |
 | processing | Int? |  yes  |  |
 | returns | Int? |  yes  |  |
 | all | Int? |  yes  |  |

---


 
 
 #### [GetPingResponse](#GetPingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ping | String |  no  |  |

---


 
 
 #### [GetShipmentAddressResponse](#GetShipmentAddressResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String |  no  |  |
 | data | [DataShipmentAddress](#DataShipmentAddress) |  no  |  |
 | success | Boolean |  no  |  |

---


 
 
 #### [DataShipmentAddress](#DataShipmentAddress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | city | String? |  yes  |  |
 | country | String? |  yes  |  |
 | pincode | String? |  yes  |  |
 | phone | String? |  yes  |  |
 | area | String? |  yes  |  |
 | address | String? |  yes  |  |
 | landmark | String? |  yes  |  |
 | state | String? |  yes  |  |
 | addressType | String? |  yes  |  |
 | addressCategory | String? |  yes  |  |
 | email | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [UpdateShipmentAddressRequest](#UpdateShipmentAddressRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | String |  no  |  |
 | address | String |  no  |  |
 | pincode | String |  no  |  |
 | state | String |  no  |  |
 | addressType | String |  no  |  |
 | country | String |  no  |  |
 | name | String |  no  |  |
 | phone | String |  no  |  |
 | area | String |  no  |  |
 | landmark | String |  no  |  |
 | city | String |  no  |  |

---


 
 
 #### [UpdateShipmentAddressResponse](#UpdateShipmentAddressResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean |  no  |  |
 | message | String |  no  |  |

---


 
 
 #### [ShipmentTrackResponse](#ShipmentTrackResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | bagList | ArrayList<[ShipmentTrackResponseBagListItem](#ShipmentTrackResponseBagListItem)> |  no  |  |
 | message | String |  no  |  |
 | orderValue | Int |  no  |  |

---


 
 
 #### [ShipmentTrackResponseBagListItem](#ShipmentTrackResponseBagListItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enableTracking | Boolean? |  yes  |  |
 | price | String? |  yes  |  |
 | timeSlot | String? |  yes  |  |
 | productName | String? |  yes  |  |
 | canReturn | Boolean? |  yes  |  |
 | orderDate | String? |  yes  |  |
 | isTryAtHome | Boolean? |  yes  |  |
 | breakupValues | ArrayList<[ShipmentTrackResponseBagListItemBreakValues](#ShipmentTrackResponseBagListItemBreakValues)>? |  yes  |  |
 | statuses | ArrayList<[ShipmentTrackResponseBagListItemStatuses](#ShipmentTrackResponseBagListItemStatuses)>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | bagId | String? |  yes  |  |
 | orderId | String? |  yes  |  |
 | size | String? |  yes  |  |
 | paymentModeSource | String? |  yes  |  |
 | dpDetails | [ShipmentTrackResponseBagListItemDpDetails](#ShipmentTrackResponseBagListItemDpDetails)? |  yes  |  |
 | productId | Int? |  yes  |  |
 | productImage | [ShipmentTrackResponseBagListItemsProductImage](#ShipmentTrackResponseBagListItemsProductImage)? |  yes  |  |
 | brandName | String? |  yes  |  |
 | priceMarked | String? |  yes  |  |
 | status | String? |  yes  |  |
 | canCancel | Boolean? |  yes  |  |
 | paymentMode | String? |  yes  |  |
 | fyndCashMsg | String? |  yes  |  |
 | deliveryAddress | String? |  yes  |  |

---


 
 
 #### [ShipmentTrackResponseBagListItemBreakValues](#ShipmentTrackResponseBagListItemBreakValues)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | display | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [ShipmentTrackResponseBagListItemStatuses](#ShipmentTrackResponseBagListItemStatuses)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | npsRating | Int? |  yes  |  |
 | npsString | String? |  yes  |  |
 | progressStatus | ArrayList<[ShipmentTrackResponseBagListItemStatusesProgress](#ShipmentTrackResponseBagListItemStatusesProgress)>? |  yes  |  |
 | flowType | String? |  yes  |  |
 | statusProgress | Int? |  yes  |  |
 | isNpsDone | Boolean? |  yes  |  |
 | headerMessage | String? |  yes  |  |
 | isDelayed | String? |  yes  |  |
 | trackingList | ArrayList<[ShipmentTrackResponseBagListItemStatusesTrack](#ShipmentTrackResponseBagListItemStatusesTrack)>? |  yes  |  |

---


 
 
 #### [ShipmentTrackResponseBagListItemStatusesProgress](#ShipmentTrackResponseBagListItemStatusesProgress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | type | String? |  yes  |  |
 | state | Boolean? |  yes  |  |

---


 
 
 #### [ShipmentTrackResponseBagListItemStatusesTrack](#ShipmentTrackResponseBagListItemStatusesTrack)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | String? |  yes  |  |
 | time | String? |  yes  |  |
 | isPassed | Boolean? |  yes  |  |
 | isCurrent | Boolean? |  yes  |  |

---


 
 
 #### [ShipmentTrackResponseBagListItemDpDetails](#ShipmentTrackResponseBagListItemDpDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | trackingNo | String? |  yes  |  |
 | courier | String? |  yes  |  |

---


 
 
 #### [ShipmentTrackResponseBagListItemsProductImage](#ShipmentTrackResponseBagListItemsProductImage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | aspectRatio | String? |  yes  |  |
 | url | String? |  yes  |  |

---


 
 
 #### [UpdateShipmentStatusResponse](#UpdateShipmentStatusResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | shipments | HashMap<String,Any> |  no  |  |
 | errorShipments | ArrayList<Any>? |  yes  |  |

---


 
 
 #### [UpdateShipmentStatusBody](#UpdateShipmentStatusBody)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | shipments | HashMap<String,Any> |  no  |  |
 | forceTransition | Boolean |  no  |  |
 | task | Boolean |  no  |  |

---


 
 
 #### [ShipmentReasonsResponse](#ShipmentReasonsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean |  no  |  |
 | message | String |  no  |  |
 | reasons | ArrayList<[ShipmentResponseReasons](#ShipmentResponseReasons)> |  no  |  |

---


 
 
 #### [ShipmentResponseReasons](#ShipmentResponseReasons)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | reasonId | Double? |  yes  |  |
 | reason | String? |  yes  |  |

---


 
 
 #### [PlatformShipmentTrack](#PlatformShipmentTrack)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | results | [Results](#Results) |  no  |  |

---


 
 
 #### [Results](#Results)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | awb | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | lastLocationRecievedAt | String? |  yes  |  |
 | reason | String? |  yes  |  |
 | shipmentType | String? |  yes  |  |
 | status | String? |  yes  |  |
 | updatedTime | String? |  yes  |  |
 | accountName | String? |  yes  |  |

---


 
 
 #### [ShipmentUpdateRequest](#ShipmentUpdateRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | bags | ArrayList<String> |  no  |  |
 | reason | HashMap<String,Any> |  no  |  |
 | comments | String |  no  |  |
 | action | String |  no  |  |

---


 
 
 #### [ShipmentUpdateResponse](#ShipmentUpdateResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean |  no  |  |
 | message | String |  no  |  |

---


 
 
 #### [UpdateProcessShipmenstRequestBody](#UpdateProcessShipmenstRequestBody)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | shipmentIds | ArrayList<String> |  no  |  |
 | expectedStatus | String |  no  |  |

---


 
 
 #### [UpdateProcessShipmenstRequestResponse](#UpdateProcessShipmenstRequestResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean |  no  |  |
 | message | String |  no  |  |

---


 
 
 #### [GetVoiceCallbackResponse](#GetVoiceCallbackResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String |  no  |  |

---


 
 
 #### [GetClickToCallResponse](#GetClickToCallResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String |  no  |  |

---


 
 
 #### [ApefaceApiError](#ApefaceApiError)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---




 
 
 #### [SearchKeywordResult](#SearchKeywordResult)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | query | HashMap<String,Any> |  no  |  |
 | sortOn | String |  no  |  |

---


 
 
 #### [CreateSearchKeyword](#CreateSearchKeyword)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | appId | String? |  yes  |  |
 | result | [SearchKeywordResult](#SearchKeywordResult) |  no  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | words | ArrayList<String>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [GetSearchWordsData](#GetSearchWordsData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | appId | String? |  yes  |  |
 | result | HashMap<String,Any>? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | uid | String? |  yes  |  |
 | words | ArrayList<String>? |  yes  |  |

---


 
 
 #### [ErrorResponse](#ErrorResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | meta | HashMap<String,Any>? |  yes  |  |
 | code | String? |  yes  |  |
 | status | Int? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [DeleteResponse](#DeleteResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [GetSearchWordsDetailResponse](#GetSearchWordsDetailResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | [GetSearchWordsData](#GetSearchWordsData)? |  yes  |  |

---


 
 
 #### [GetSearchWordsResponse](#GetSearchWordsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[GetSearchWordsData](#GetSearchWordsData)>? |  yes  |  |

---


 
 
 #### [AutocompletePageAction](#AutocompletePageAction)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String |  no  |  |
 | params | HashMap<String,Any>? |  yes  |  |
 | query | HashMap<String,Any> |  no  |  |
 | url | String? |  yes  |  |

---


 
 
 #### [AutocompleteAction](#AutocompleteAction)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | page | [AutocompletePageAction](#AutocompletePageAction)? |  yes  |  |

---


 
 
 #### [Media](#Media)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | url | String? |  yes  |  |

---


 
 
 #### [AutocompleteResult](#AutocompleteResult)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | action | [AutocompleteAction](#AutocompleteAction)? |  yes  |  |
 | logo | [Media](#Media)? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [CreateAutocompleteKeyword](#CreateAutocompleteKeyword)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | results | ArrayList<[AutocompleteResult](#AutocompleteResult)>? |  yes  |  |
 | appId | String? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | words | ArrayList<String>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [GetAutocompleteWordsData](#GetAutocompleteWordsData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | results | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | appId | String? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | uid | String? |  yes  |  |
 | words | ArrayList<String>? |  yes  |  |

---


 
 
 #### [GetAutocompleteWordsResponse](#GetAutocompleteWordsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[GetAutocompleteWordsData](#GetAutocompleteWordsData)>? |  yes  |  |

---


 
 
 #### [CreateAutocompleteWordsResponse](#CreateAutocompleteWordsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | appId | String? |  yes  |  |
 | words | ArrayList<String>? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | results | ArrayList<HashMap<String,Any>>? |  yes  |  |

---


 
 
 #### [ProductBundleItem](#ProductBundleItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | minQuantity | Int |  no  |  |
 | allowRemove | Boolean? |  yes  |  |
 | autoSelect | Boolean? |  yes  |  |
 | maxQuantity | Int |  no  |  |
 | autoAddToCart | Boolean? |  yes  |  |
 | productUid | Int |  no  |  |

---


 
 
 #### [GetProductBundleCreateResponse](#GetProductBundleCreateResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | products | ArrayList<[ProductBundleItem](#ProductBundleItem)> |  no  |  |
 | pageVisibility | ArrayList<String>? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | choice | String |  no  |  |
 | id | String? |  yes  |  |
 | slug | String |  no  |  |
 | sameStoreAssignment | Boolean? |  yes  |  |
 | name | String |  no  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | logo | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [GetProductBundleListingResponse](#GetProductBundleListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[GetProductBundleCreateResponse](#GetProductBundleCreateResponse)>? |  yes  |  |

---


 
 
 #### [ProductBundleRequest](#ProductBundleRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | products | ArrayList<[ProductBundleItem](#ProductBundleItem)> |  no  |  |
 | pageVisibility | ArrayList<String>? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | choice | String |  no  |  |
 | slug | String |  no  |  |
 | sameStoreAssignment | Boolean? |  yes  |  |
 | name | String |  no  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | logo | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [ProductBundleUpdateRequest](#ProductBundleUpdateRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | products | ArrayList<[ProductBundleItem](#ProductBundleItem)> |  no  |  |
 | pageVisibility | ArrayList<String>? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | choice | String |  no  |  |
 | slug | String |  no  |  |
 | sameStoreAssignment | Boolean? |  yes  |  |
 | name | String |  no  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | logo | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [LimitedProductData](#LimitedProductData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | images | ArrayList<String>? |  yes  |  |
 | identifier | HashMap<String,Any>? |  yes  |  |
 | shortDescription | String? |  yes  |  |
 | sizes | ArrayList<String>? |  yes  |  |
 | attributes | HashMap<String,Any>? |  yes  |  |
 | countryOfOrigin | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | price | HashMap<String,Any>? |  yes  |  |
 | name | String? |  yes  |  |
 | quantity | Int? |  yes  |  |
 | itemCode | String? |  yes  |  |
 | uid | Int? |  yes  |  |

---


 
 
 #### [Size](#Size)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | isAvailable | Boolean? |  yes  |  |
 | quantity | Int? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [Price](#Price)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | currency | String? |  yes  |  |
 | minEffective | Double? |  yes  |  |
 | maxMarked | Double? |  yes  |  |
 | minMarked | Double? |  yes  |  |
 | maxEffective | Double? |  yes  |  |

---


 
 
 #### [GetProducts](#GetProducts)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | minQuantity | Int? |  yes  |  |
 | allowRemove | Boolean? |  yes  |  |
 | autoSelect | Boolean? |  yes  |  |
 | maxQuantity | Int? |  yes  |  |
 | productDetails | [LimitedProductData](#LimitedProductData)? |  yes  |  |
 | sizes | ArrayList<[Size](#Size)>? |  yes  |  |
 | autoAddToCart | Boolean? |  yes  |  |
 | price | [Price](#Price)? |  yes  |  |
 | productUid | Int? |  yes  |  |

---


 
 
 #### [GetProductBundleResponse](#GetProductBundleResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pageVisibility | ArrayList<String>? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | products | ArrayList<[GetProducts](#GetProducts)>? |  yes  |  |
 | choice | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | sameStoreAssignment | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | logo | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [ListSizeGuide](#ListSizeGuide)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | HashMap<String,Any>? |  yes  |  |
 | items | ArrayList<HashMap<String,Any>>? |  yes  |  |

---


 
 
 #### [Meta](#Meta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | unit | String? |  yes  |  |
 | values | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | headers | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [Guide](#Guide)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | meta | [Meta](#Meta)? |  yes  |  |

---


 
 
 #### [ValidateSizeGuide](#ValidateSizeGuide)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String |  no  |  |
 | companyId | Int? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | description | String? |  yes  |  |
 | image | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | id | String? |  yes  |  |
 | subtitle | String? |  yes  |  |
 | name | String |  no  |  |
 | brandId | Int? |  yes  |  |
 | tag | String? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | guide | [Guide](#Guide)? |  yes  |  |

---


 
 
 #### [SuccessResponse](#SuccessResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | success | Boolean? |  yes  |  |

---


 
 
 #### [SizeGuideResponse](#SizeGuideResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | brandId | Int? |  yes  |  |
 | subtitle | String? |  yes  |  |
 | tag | String? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | guide | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [GetCatalogConfigurationDetailsProduct](#GetCatalogConfigurationDetailsProduct)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | similar | HashMap<String,Any>? |  yes  |  |
 | compare | HashMap<String,Any>? |  yes  |  |
 | detail | HashMap<String,Any>? |  yes  |  |
 | variant | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [MetaDataListingSortMetaResponse](#MetaDataListingSortMetaResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | key | String? |  yes  |  |

---


 
 
 #### [MetaDataListingSortResponse](#MetaDataListingSortResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | ArrayList<[MetaDataListingSortMetaResponse](#MetaDataListingSortMetaResponse)>? |  yes  |  |

---


 
 
 #### [MetaDataListingFilterMetaResponse](#MetaDataListingFilterMetaResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | key | String? |  yes  |  |
 | units | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | filterTypes | ArrayList<String>? |  yes  |  |

---


 
 
 #### [MetaDataListingFilterResponse](#MetaDataListingFilterResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | ArrayList<[MetaDataListingFilterMetaResponse](#MetaDataListingFilterMetaResponse)>? |  yes  |  |

---


 
 
 #### [MetaDataListingResponse](#MetaDataListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sort | [MetaDataListingSortResponse](#MetaDataListingSortResponse) |  no  |  |
 | filter | [MetaDataListingFilterResponse](#MetaDataListingFilterResponse) |  no  |  |

---


 
 
 #### [GetCatalogConfigurationMetaData](#GetCatalogConfigurationMetaData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | product | [GetCatalogConfigurationDetailsProduct](#GetCatalogConfigurationDetailsProduct)? |  yes  |  |
 | listing | [MetaDataListingResponse](#MetaDataListingResponse)? |  yes  |  |

---


 
 
 #### [ConfigurationListingSortConfig](#ConfigurationListingSortConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String |  no  |  |
 | priority | Int |  no  |  |
 | name | String? |  yes  |  |
 | logo | String? |  yes  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [ConfigurationListingSort](#ConfigurationListingSort)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | defaultKey | String |  no  |  |
 | config | ArrayList<[ConfigurationListingSortConfig](#ConfigurationListingSortConfig)>? |  yes  |  |

---


 
 
 #### [ConfigurationBucketPoints](#ConfigurationBucketPoints)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | end | Double? |  yes  |  |
 | start | Double? |  yes  |  |

---


 
 
 #### [ConfigurationListingFilterValue](#ConfigurationListingFilterValue)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | String? |  yes  |  |
 | sort | String? |  yes  |  |
 | bucketPoints | ArrayList<[ConfigurationBucketPoints](#ConfigurationBucketPoints)>? |  yes  |  |
 | map | HashMap<String,Any>? |  yes  |  |
 | condition | String? |  yes  |  |

---


 
 
 #### [ConfigurationListingFilterConfig](#ConfigurationListingFilterConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String |  no  |  |
 | valueConfig | [ConfigurationListingFilterValue](#ConfigurationListingFilterValue)? |  yes  |  |
 | key | String |  no  |  |
 | priority | Int |  no  |  |
 | name | String? |  yes  |  |
 | logo | String? |  yes  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [ConfigurationListingFilter](#ConfigurationListingFilter)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | attributeConfig | ArrayList<[ConfigurationListingFilterConfig](#ConfigurationListingFilterConfig)>? |  yes  |  |
 | allowSingle | Boolean |  no  |  |

---


 
 
 #### [ConfigurationListing](#ConfigurationListing)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sort | [ConfigurationListingSort](#ConfigurationListingSort) |  no  |  |
 | filter | [ConfigurationListingFilter](#ConfigurationListingFilter) |  no  |  |

---


 
 
 #### [ProductSize](#ProductSize)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | min | Int |  no  |  |
 | max | Int |  no  |  |

---


 
 
 #### [ConfigurationProductConfig](#ConfigurationProductConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | key | String |  no  |  |
 | priority | Int |  no  |  |
 | subtitle | String? |  yes  |  |
 | size | [ProductSize](#ProductSize)? |  yes  |  |
 | logo | String? |  yes  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [ConfigurationProductSimilar](#ConfigurationProductSimilar)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | config | ArrayList<[ConfigurationProductConfig](#ConfigurationProductConfig)>? |  yes  |  |

---


 
 
 #### [ConfigurationProductVariantConfig](#ConfigurationProductVariantConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | displayType | String |  no  |  |
 | key | String |  no  |  |
 | priority | Int |  no  |  |
 | name | String |  no  |  |
 | size | [ProductSize](#ProductSize) |  no  |  |
 | logo | String? |  yes  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [ConfigurationProductVariant](#ConfigurationProductVariant)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | config | ArrayList<[ConfigurationProductVariantConfig](#ConfigurationProductVariantConfig)>? |  yes  |  |

---


 
 
 #### [ConfigurationProduct](#ConfigurationProduct)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | similar | [ConfigurationProductSimilar](#ConfigurationProductSimilar) |  no  |  |
 | variant | [ConfigurationProductVariant](#ConfigurationProductVariant) |  no  |  |

---


 
 
 #### [AppCatalogConfiguration](#AppCatalogConfiguration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | listing | [ConfigurationListing](#ConfigurationListing)? |  yes  |  |
 | configId | String? |  yes  |  |
 | product | [ConfigurationProduct](#ConfigurationProduct)? |  yes  |  |
 | appId | String |  no  |  |
 | configType | String |  no  |  |

---


 
 
 #### [GetAppCatalogConfiguration](#GetAppCatalogConfiguration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [AppCatalogConfiguration](#AppCatalogConfiguration)? |  yes  |  |
 | isDefault | Boolean? |  yes  |  |

---


 
 
 #### [AppConfiguration](#AppConfiguration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | listing | [ConfigurationListing](#ConfigurationListing)? |  yes  |  |
 | configId | String? |  yes  |  |
 | product | [ConfigurationProduct](#ConfigurationProduct)? |  yes  |  |
 | appId | String |  no  |  |
 | configType | String |  no  |  |

---


 
 
 #### [GetCatalogConfigurationDetailsSchemaListing](#GetCatalogConfigurationDetailsSchemaListing)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sort | HashMap<String,Any>? |  yes  |  |
 | filter | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [EntityConfiguration](#EntityConfiguration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | listing | [GetCatalogConfigurationDetailsSchemaListing](#GetCatalogConfigurationDetailsSchemaListing)? |  yes  |  |
 | configId | String? |  yes  |  |
 | product | [GetCatalogConfigurationDetailsProduct](#GetCatalogConfigurationDetailsProduct)? |  yes  |  |
 | appId | String |  no  |  |
 | configType | String |  no  |  |

---


 
 
 #### [GetAppCatalogEntityConfiguration](#GetAppCatalogEntityConfiguration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [EntityConfiguration](#EntityConfiguration)? |  yes  |  |
 | isDefault | Boolean? |  yes  |  |

---


 
 
 #### [ProductFiltersKey](#ProductFiltersKey)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String |  no  |  |
 | logo | String? |  yes  |  |
 | name | String |  no  |  |
 | kind | String? |  yes  |  |

---


 
 
 #### [ProductFiltersValue](#ProductFiltersValue)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | displayFormat | String? |  yes  |  |
 | selectedMax | Int? |  yes  |  |
 | currencySymbol | String? |  yes  |  |
 | display | String |  no  |  |
 | value | String |  no  |  |
 | max | Int? |  yes  |  |
 | min | Int? |  yes  |  |
 | selectedMin | Int? |  yes  |  |
 | isSelected | Boolean |  no  |  |
 | currencyCode | String? |  yes  |  |
 | queryFormat | String? |  yes  |  |
 | count | Int? |  yes  |  |

---


 
 
 #### [ProductFilters](#ProductFilters)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | [ProductFiltersKey](#ProductFiltersKey) |  no  |  |
 | values | ArrayList<[ProductFiltersValue](#ProductFiltersValue)> |  no  |  |

---


 
 
 #### [ProductSortOn](#ProductSortOn)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | String? |  yes  |  |
 | name | String? |  yes  |  |
 | isSelected | Boolean? |  yes  |  |

---


 
 
 #### [GetCollectionQueryOptionResponse](#GetCollectionQueryOptionResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | filters | ArrayList<[ProductFilters](#ProductFilters)>? |  yes  |  |
 | sortOn | ArrayList<[ProductSortOn](#ProductSortOn)>? |  yes  |  |

---


 
 
 #### [CollectionListingFilterType](#CollectionListingFilterType)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | name | String? |  yes  |  |
 | isSelected | Boolean? |  yes  |  |

---


 
 
 #### [CollectionListingFilterTag](#CollectionListingFilterTag)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | name | String? |  yes  |  |
 | isSelected | Boolean? |  yes  |  |

---


 
 
 #### [CollectionListingFilter](#CollectionListingFilter)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | ArrayList<[CollectionListingFilterType](#CollectionListingFilterType)>? |  yes  |  |
 | tags | ArrayList<[CollectionListingFilterTag](#CollectionListingFilterTag)>? |  yes  |  |

---


 
 
 #### [ProductListingActionPage](#ProductListingActionPage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [ProductListingAction](#ProductListingAction)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | page | [ProductListingActionPage](#ProductListingActionPage)? |  yes  |  |

---


 
 
 #### [BannerImage](#BannerImage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | url | String? |  yes  |  |
 | aspectRatio | String? |  yes  |  |

---


 
 
 #### [ImageUrls](#ImageUrls)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | portrait | [BannerImage](#BannerImage)? |  yes  |  |
 | landscape | [BannerImage](#BannerImage)? |  yes  |  |

---


 
 
 #### [Media1](#Media1)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | url | String |  no  |  |

---


 
 
 #### [GetCollectionDetailNest](#GetCollectionDetailNest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | badge | HashMap<String,Any>? |  yes  |  |
 | name | String? |  yes  |  |
 | tag | ArrayList<String>? |  yes  |  |
 | uid | String? |  yes  |  |
 | allowFacets | Boolean? |  yes  |  |
 | visibleFacetsKeys | ArrayList<String>? |  yes  |  |
 | type | String? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |
 | appId | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | allowSort | Boolean? |  yes  |  |
 | description | String? |  yes  |  |
 | schedule | HashMap<String,Any>? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | cron | HashMap<String,Any>? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | logo | [Media1](#Media1)? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [GetCollectionListingResponse](#GetCollectionListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | filters | [CollectionListingFilter](#CollectionListingFilter)? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[GetCollectionDetailNest](#GetCollectionDetailNest)>? |  yes  |  |

---


 
 
 #### [CollectionBadge](#CollectionBadge)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | text | String? |  yes  |  |
 | color | String? |  yes  |  |

---


 
 
 #### [Schedule](#Schedule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cron | String? |  yes  |  |
 | end | String? |  yes  |  |
 | duration | Int? |  yes  |  |
 | start | String? |  yes  |  |

---


 
 
 #### [CollectionImage](#CollectionImage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | url | String |  no  |  |
 | aspectRatio | String |  no  |  |

---


 
 
 #### [CollectionBanner](#CollectionBanner)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | portrait | [CollectionImage](#CollectionImage) |  no  |  |
 | landscape | [CollectionImage](#CollectionImage) |  no  |  |

---


 
 
 #### [UserInfo](#UserInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | userId | String? |  yes  |  |
 | uid | String? |  yes  |  |
 | email | String? |  yes  |  |
 | username | String? |  yes  |  |

---


 
 
 #### [SeoDetail](#SeoDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | description | String? |  yes  |  |

---


 
 
 #### [CreateCollection](#CreateCollection)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isActive | Boolean? |  yes  |  |
 | badge | [CollectionBadge](#CollectionBadge)? |  yes  |  |
 | name | String |  no  |  |
 | sortOn | String? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | allowFacets | Boolean? |  yes  |  |
 | visibleFacetsKeys | ArrayList<String>? |  yes  |  |
 | type | String |  no  |  |
 | query | HashMap<String,Any>? |  yes  |  |
 | slug | String |  no  |  |
 | appId | String |  no  |  |
 | allowSort | Boolean? |  yes  |  |
 | description | String? |  yes  |  |
 | schedule | [Schedule](#Schedule)? |  yes  |  |
 | banners | [CollectionBanner](#CollectionBanner) |  no  |  |
 | createdBy | [UserInfo](#UserInfo)? |  yes  |  |
 | seo | [SeoDetail](#SeoDetail)? |  yes  |  |
 | localeLanguage | HashMap<String,Any>? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | modifiedBy | [UserInfo](#UserInfo)? |  yes  |  |
 | logo | [CollectionImage](#CollectionImage) |  no  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | published | Boolean? |  yes  |  |

---


 
 
 #### [CollectionCreateResponse](#CollectionCreateResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | visibleFacetsKeys | ArrayList<String>? |  yes  |  |
 | allowFacets | Boolean? |  yes  |  |
 | type | String? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | description | String? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |
 | schedule | HashMap<String,Any>? |  yes  |  |
 | appId | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | badge | HashMap<String,Any>? |  yes  |  |
 | name | String? |  yes  |  |
 | tag | ArrayList<String>? |  yes  |  |
 | cron | HashMap<String,Any>? |  yes  |  |
 | allowSort | Boolean? |  yes  |  |
 | logo | [BannerImage](#BannerImage)? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [CollectionDetailResponse](#CollectionDetailResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | visibleFacetsKeys | ArrayList<String>? |  yes  |  |
 | allowFacets | Boolean? |  yes  |  |
 | type | String? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | description | String? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |
 | schedule | HashMap<String,Any>? |  yes  |  |
 | appId | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | badge | HashMap<String,Any>? |  yes  |  |
 | name | String? |  yes  |  |
 | tag | ArrayList<String>? |  yes  |  |
 | cron | HashMap<String,Any>? |  yes  |  |
 | allowSort | Boolean? |  yes  |  |
 | logo | [Media1](#Media1)? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [UpdateCollection](#UpdateCollection)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isActive | Boolean? |  yes  |  |
 | badge | [CollectionBadge](#CollectionBadge)? |  yes  |  |
 | name | String? |  yes  |  |
 | sortOn | String? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | allowFacets | Boolean? |  yes  |  |
 | visibleFacetsKeys | ArrayList<String>? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |
 | slug | String? |  yes  |  |
 | allowSort | Boolean? |  yes  |  |
 | modifiedBy | [UserInfo](#UserInfo)? |  yes  |  |
 | description | String? |  yes  |  |
 | schedule | [Schedule](#Schedule)? |  yes  |  |
 | banners | [CollectionBanner](#CollectionBanner)? |  yes  |  |
 | seo | [SeoDetail](#SeoDetail)? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | localeLanguage | HashMap<String,Any>? |  yes  |  |
 | logo | [CollectionImage](#CollectionImage)? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | published | Boolean? |  yes  |  |

---


 
 
 #### [ProductBrand](#ProductBrand)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | logo | [Media1](#Media1)? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [Price1](#Price1)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | min | Double? |  yes  |  |
 | currencySymbol | String? |  yes  |  |
 | max | Double? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [ProductListingPrice](#ProductListingPrice)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | marked | [Price1](#Price1)? |  yes  |  |
 | effective | [Price1](#Price1)? |  yes  |  |

---


 
 
 #### [ProductDetailAttribute](#ProductDetailAttribute)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | key | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [ProductDetailGroupedAttribute](#ProductDetailGroupedAttribute)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | details | ArrayList<[ProductDetailAttribute](#ProductDetailAttribute)>? |  yes  |  |

---


 
 
 #### [ProductListingDetail](#ProductListingDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | imageNature | String? |  yes  |  |
 | similars | ArrayList<String>? |  yes  |  |
 | medias | ArrayList<[Media1](#Media1)>? |  yes  |  |
 | hasVariant | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | brand | [ProductBrand](#ProductBrand)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | color | String? |  yes  |  |
 | type | String? |  yes  |  |
 | attributes | HashMap<String,Any>? |  yes  |  |
 | slug | String |  no  |  |
 | price | [ProductListingPrice](#ProductListingPrice)? |  yes  |  |
 | itemCode | String? |  yes  |  |
 | rating | Double? |  yes  |  |
 | tryouts | ArrayList<String>? |  yes  |  |
 | sellable | Boolean? |  yes  |  |
 | description | String? |  yes  |  |
 | highlights | ArrayList<String>? |  yes  |  |
 | teaserTag | HashMap<String,Any>? |  yes  |  |
 | promoMeta | HashMap<String,Any>? |  yes  |  |
 | shortDescription | String? |  yes  |  |
 | groupedAttributes | ArrayList<[ProductDetailGroupedAttribute](#ProductDetailGroupedAttribute)>? |  yes  |  |
 | itemType | String? |  yes  |  |
 | productOnlineDate | String? |  yes  |  |
 | ratingCount | Int? |  yes  |  |
 | discount | String? |  yes  |  |

---


 
 
 #### [GetCollectionItemsResponse](#GetCollectionItemsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | filters | ArrayList<[ProductFilters](#ProductFilters)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |
 | sortOn | ArrayList<[ProductSortOn](#ProductSortOn)>? |  yes  |  |
 | items | ArrayList<[ProductListingDetail](#ProductListingDetail)>? |  yes  |  |

---


 
 
 #### [CollectionItemRequest](#CollectionItemRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pageSize | Int |  no  |  |
 | pageNo | Int |  no  |  |

---


 
 
 #### [UpdatedResponse](#UpdatedResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [CatalogInsightBrand](#CatalogInsightBrand)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | availableArticles | Int? |  yes  |  |
 | articleFreshness | Int? |  yes  |  |
 | totalSizes | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | totalArticles | Int? |  yes  |  |
 | availableSizes | Int? |  yes  |  |

---


 
 
 #### [CatalogInsightItem](#CatalogInsightItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sellableCount | Int? |  yes  |  |
 | outOfStockCount | Int? |  yes  |  |
 | count | Int? |  yes  |  |

---


 
 
 #### [CatalogInsightResponse](#CatalogInsightResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brandDistribution | [CatalogInsightBrand](#CatalogInsightBrand)? |  yes  |  |
 | item | [CatalogInsightItem](#CatalogInsightItem)? |  yes  |  |

---


 
 
 #### [CrossSellingData](#CrossSellingData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | products | Int? |  yes  |  |
 | articles | Int? |  yes  |  |

---


 
 
 #### [CrossSellingResponse](#CrossSellingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [CrossSellingData](#CrossSellingData)? |  yes  |  |
 | brandDistribution | [CatalogInsightBrand](#CatalogInsightBrand)? |  yes  |  |

---


 
 
 #### [OptInPostRequest](#OptInPostRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brandIds | ArrayList<Int>? |  yes  |  |
 | enabled | Boolean? |  yes  |  |
 | optLevel | String |  no  |  |
 | storeIds | ArrayList<Int>? |  yes  |  |

---


 
 
 #### [CompanyOptIn](#CompanyOptIn)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | optLevel | String |  no  |  |
 | platform | String |  no  |  |
 | enabled | Boolean |  no  |  |
 | companyId | Int |  no  |  |
 | createdOn | Int |  no  |  |
 | modifiedOn | Int |  no  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | brandIds | ArrayList<Int> |  no  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | storeIds | ArrayList<Int> |  no  |  |

---


 
 
 #### [GetOptInPlatform](#GetOptInPlatform)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page) |  no  |  |
 | items | ArrayList<[CompanyOptIn](#CompanyOptIn)> |  no  |  |

---


 
 
 #### [OptinCompanyDetail](#OptinCompanyDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companyType | String? |  yes  |  |
 | businessType | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [CompanyBrandDetail](#CompanyBrandDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companyId | Int? |  yes  |  |
 | brandName | String? |  yes  |  |
 | totalArticle | Int? |  yes  |  |
 | brandId | Int? |  yes  |  |

---


 
 
 #### [OptinCompanyBrandDetailsView](#OptinCompanyBrandDetailsView)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[CompanyBrandDetail](#CompanyBrandDetail)>? |  yes  |  |

---


 
 
 #### [OptinCompanyMetrics](#OptinCompanyMetrics)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | company | String? |  yes  |  |
 | store | Int? |  yes  |  |
 | brand | Int? |  yes  |  |

---


 
 
 #### [StoreDetail](#StoreDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | timing | HashMap<String,Any>? |  yes  |  |
 | displayName | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | documents | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | name | String? |  yes  |  |
 | storeType | String? |  yes  |  |
 | storeCode | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | additionalContacts | ArrayList<HashMap<String,Any>>? |  yes  |  |

---


 
 
 #### [OptinStoreDetails](#OptinStoreDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[StoreDetail](#StoreDetail)>? |  yes  |  |

---


 
 
 #### [AttributeMasterFilter](#AttributeMasterFilter)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | priority | Int? |  yes  |  |
 | indexing | Boolean |  no  |  |
 | dependsOn | ArrayList<String>? |  yes  |  |

---


 
 
 #### [AttributeMasterDetails](#AttributeMasterDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | displayType | String |  no  |  |

---


 
 
 #### [AttributeSchemaRange](#AttributeSchemaRange)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | min | Int? |  yes  |  |
 | max | Int? |  yes  |  |

---


 
 
 #### [AttributeMaster](#AttributeMaster)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | mandatory | Boolean? |  yes  |  |
 | type | String |  no  |  |
 | range | [AttributeSchemaRange](#AttributeSchemaRange)? |  yes  |  |
 | format | String? |  yes  |  |
 | multi | Boolean? |  yes  |  |
 | allowedValues | ArrayList<String>? |  yes  |  |

---


 
 
 #### [AttributeMasterMandatoryDetails](#AttributeMasterMandatoryDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | l3Keys | ArrayList<String>? |  yes  |  |

---


 
 
 #### [AttributeMasterMeta](#AttributeMasterMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enriched | Boolean? |  yes  |  |
 | mandatoryDetails | [AttributeMasterMandatoryDetails](#AttributeMasterMandatoryDetails) |  no  |  |

---


 
 
 #### [GenderDetail](#GenderDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabledForEndConsumer | Boolean? |  yes  |  |
 | departments | ArrayList<String>? |  yes  |  |
 | filters | [AttributeMasterFilter](#AttributeMasterFilter)? |  yes  |  |
 | description | String? |  yes  |  |
 | id | String? |  yes  |  |
 | logo | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | details | [AttributeMasterDetails](#AttributeMasterDetails)? |  yes  |  |
 | name | String? |  yes  |  |
 | isNested | Boolean? |  yes  |  |
 | schema | [AttributeMaster](#AttributeMaster)? |  yes  |  |
 | meta | [AttributeMasterMeta](#AttributeMasterMeta)? |  yes  |  |

---


 
 
 #### [ProdcutTemplateCategoriesResponse](#ProdcutTemplateCategoriesResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<HashMap<String,Any>>? |  yes  |  |

---


 
 
 #### [PTErrorResponse](#PTErrorResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | code | String? |  yes  |  |
 | status | Int? |  yes  |  |
 | errors | HashMap<String,Any>? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [UserSerializer](#UserSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | userId | String? |  yes  |  |
 | username | String? |  yes  |  |
 | contact | String? |  yes  |  |

---


 
 
 #### [GetDepartment](#GetDepartment)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | priorityOrder | Int? |  yes  |  |
 | search | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | createdBy | [UserSerializer](#UserSerializer)? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | pageNo | Int? |  yes  |  |
 | itemType | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | name | String? |  yes  |  |
 | synonyms | ArrayList<String>? |  yes  |  |
 | pageSize | Int? |  yes  |  |
 | modifiedBy | [UserSerializer](#UserSerializer)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | logo | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [DepartmentsResponse](#DepartmentsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[GetDepartment](#GetDepartment)>? |  yes  |  |

---


 
 
 #### [DepartmentErrorResponse](#DepartmentErrorResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | code | String? |  yes  |  |
 | status | Int? |  yes  |  |
 | errors | HashMap<String,Any>? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [ProductTemplate](#ProductTemplate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | departments | ArrayList<String>? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | description | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | attributes | ArrayList<String>? |  yes  |  |
 | categories | ArrayList<String>? |  yes  |  |
 | slug | String |  no  |  |
 | name | String? |  yes  |  |
 | isPhysical | Boolean |  no  |  |
 | isArchived | Boolean? |  yes  |  |
 | tag | String? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | logo | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [TemplatesResponse](#TemplatesResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | [ProductTemplate](#ProductTemplate)? |  yes  |  |

---


 
 
 #### [Properties](#Properties)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | command | HashMap<String,Any>? |  yes  |  |
 | sizeGuide | HashMap<String,Any>? |  yes  |  |
 | returnConfig | HashMap<String,Any>? |  yes  |  |
 | name | HashMap<String,Any>? |  yes  |  |
 | variants | HashMap<String,Any>? |  yes  |  |
 | tags | HashMap<String,Any>? |  yes  |  |
 | categorySlug | HashMap<String,Any>? |  yes  |  |
 | trader | HashMap<String,Any>? |  yes  |  |
 | traderType | HashMap<String,Any>? |  yes  |  |
 | countryOfOrigin | HashMap<String,Any>? |  yes  |  |
 | slug | HashMap<String,Any>? |  yes  |  |
 | itemCode | HashMap<String,Any>? |  yes  |  |
 | currency | HashMap<String,Any>? |  yes  |  |
 | hsnCode | HashMap<String,Any>? |  yes  |  |
 | productPublish | HashMap<String,Any>? |  yes  |  |
 | media | HashMap<String,Any>? |  yes  |  |
 | description | HashMap<String,Any>? |  yes  |  |
 | sizes | HashMap<String,Any>? |  yes  |  |
 | noOfBoxes | HashMap<String,Any>? |  yes  |  |
 | customOrder | HashMap<String,Any>? |  yes  |  |
 | multiSize | HashMap<String,Any>? |  yes  |  |
 | highlights | HashMap<String,Any>? |  yes  |  |
 | teaserTag | HashMap<String,Any>? |  yes  |  |
 | moq | HashMap<String,Any>? |  yes  |  |
 | shortDescription | HashMap<String,Any>? |  yes  |  |
 | brandUid | HashMap<String,Any>? |  yes  |  |
 | itemType | HashMap<String,Any>? |  yes  |  |
 | isDependent | HashMap<String,Any>? |  yes  |  |
 | productGroupTag | HashMap<String,Any>? |  yes  |  |
 | isActive | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [GlobalValidation](#GlobalValidation)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | required | ArrayList<String>? |  yes  |  |
 | definitions | HashMap<String,Any>? |  yes  |  |
 | type | String? |  yes  |  |
 | description | String? |  yes  |  |
 | properties | [Properties](#Properties)? |  yes  |  |

---


 
 
 #### [TemplateValidationData](#TemplateValidationData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | templateValidation | HashMap<String,Any>? |  yes  |  |
 | globalValidation | [GlobalValidation](#GlobalValidation)? |  yes  |  |

---


 
 
 #### [TemplateDetails](#TemplateDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | departments | ArrayList<String>? |  yes  |  |
 | description | String? |  yes  |  |
 | id | String? |  yes  |  |
 | attributes | ArrayList<String>? |  yes  |  |
 | categories | ArrayList<String>? |  yes  |  |
 | slug | String |  no  |  |
 | name | String? |  yes  |  |
 | isPhysical | Boolean |  no  |  |
 | isArchived | Boolean? |  yes  |  |
 | tag | String? |  yes  |  |
 | logo | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [TemplatesValidationResponse](#TemplatesValidationResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [TemplateValidationData](#TemplateValidationData)? |  yes  |  |
 | templateDetails | [TemplateDetails](#TemplateDetails)? |  yes  |  |

---


 
 
 #### [InventoryValidationResponse](#InventoryValidationResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | HashMap<String,Any>? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [HSNData](#HSNData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | hsnCode | ArrayList<String>? |  yes  |  |
 | countryOfOrigin | ArrayList<String>? |  yes  |  |

---


 
 
 #### [HSNCodesResponse](#HSNCodesResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [HSNData](#HSNData)? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [ProductDownloadItemsData](#ProductDownloadItemsData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | templates | ArrayList<String>? |  yes  |  |
 | brand | ArrayList<String>? |  yes  |  |

---


 
 
 #### [VerifiedBy](#VerifiedBy)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | userId | String? |  yes  |  |
 | username | String? |  yes  |  |

---


 
 
 #### [ProductDownloadsItems](#ProductDownloadsItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | taskId | String? |  yes  |  |
 | status | String? |  yes  |  |
 | triggerOn | String? |  yes  |  |
 | data | [ProductDownloadItemsData](#ProductDownloadItemsData)? |  yes  |  |
 | templateTags | HashMap<String,Any>? |  yes  |  |
 | createdBy | [VerifiedBy](#VerifiedBy)? |  yes  |  |
 | completedOn | String? |  yes  |  |
 | url | String? |  yes  |  |
 | id | String? |  yes  |  |
 | sellerId | Double? |  yes  |  |

---


 
 
 #### [ProductDownloadsResponse](#ProductDownloadsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | [ProductDownloadsItems](#ProductDownloadsItems)? |  yes  |  |

---


 
 
 #### [ProductConfigurationDownloads](#ProductConfigurationDownloads)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | multivalue | Boolean? |  yes  |  |

---


 
 
 #### [CategoryMappingValues](#CategoryMappingValues)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | catalogId | Int? |  yes  |  |
 | name | String |  no  |  |

---


 
 
 #### [CategoryMapping](#CategoryMapping)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | facebook | [CategoryMappingValues](#CategoryMappingValues)? |  yes  |  |
 | ajio | [CategoryMappingValues](#CategoryMappingValues)? |  yes  |  |
 | google | [CategoryMappingValues](#CategoryMappingValues)? |  yes  |  |

---


 
 
 #### [Media2](#Media2)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | logo | String |  no  |  |
 | portrait | String |  no  |  |
 | landscape | String |  no  |  |

---


 
 
 #### [Hierarchy](#Hierarchy)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | l2 | Int |  no  |  |
 | l1 | Int |  no  |  |
 | department | Int |  no  |  |

---


 
 
 #### [Category](#Category)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | marketplaces | [CategoryMapping](#CategoryMapping)? |  yes  |  |
 | departments | ArrayList<Int> |  no  |  |
 | level | Int |  no  |  |
 | media | [Media2](#Media2)? |  yes  |  |
 | tryouts | ArrayList<String>? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | hierarchy | ArrayList<[Hierarchy](#Hierarchy)>? |  yes  |  |
 | slug | String? |  yes  |  |
 | priority | Int? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String |  no  |  |
 | synonyms | ArrayList<String>? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | uid | Int? |  yes  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [CategoryResponse](#CategoryResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[Category](#Category)>? |  yes  |  |

---


 
 
 #### [CategoryRequestBody](#CategoryRequestBody)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | marketplaces | [CategoryMapping](#CategoryMapping)? |  yes  |  |
 | departments | ArrayList<Int> |  no  |  |
 | media | [Media2](#Media2)? |  yes  |  |
 | level | Int |  no  |  |
 | tryouts | ArrayList<String>? |  yes  |  |
 | hierarchy | ArrayList<[Hierarchy](#Hierarchy)>? |  yes  |  |
 | slug | String? |  yes  |  |
 | priority | Int? |  yes  |  |
 | name | String |  no  |  |
 | synonyms | ArrayList<String>? |  yes  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [CategoryCreateResponse](#CategoryCreateResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [CategoryUpdateResponse](#CategoryUpdateResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [SingleCategoryResponse](#SingleCategoryResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [Category](#Category)? |  yes  |  |

---


 
 
 #### [Logo](#Logo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | secureUrl | String? |  yes  |  |
 | aspectRatioF | Int? |  yes  |  |
 | url | String? |  yes  |  |
 | aspectRatio | String? |  yes  |  |

---


 
 
 #### [Brand](#Brand)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | logo | [Logo](#Logo)? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [Image](#Image)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | secureUrl | String? |  yes  |  |
 | aspectRatioF | Double? |  yes  |  |
 | url | String? |  yes  |  |
 | aspectRatio | String? |  yes  |  |

---


 
 
 #### [ProductPublished](#ProductPublished)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isSet | Boolean? |  yes  |  |
 | productOnlineDate | Int? |  yes  |  |

---


 
 
 #### [Product](#Product)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | imageNature | String? |  yes  |  |
 | departments | ArrayList<Int>? |  yes  |  |
 | isSet | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | sizeGuide | String? |  yes  |  |
 | templateTag | String? |  yes  |  |
 | name | String? |  yes  |  |
 | brand | [Brand](#Brand)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | variants | HashMap<String,Any>? |  yes  |  |
 | categorySlug | String? |  yes  |  |
 | color | String? |  yes  |  |
 | countryOfOrigin | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | categoryUid | Int? |  yes  |  |
 | itemCode | String? |  yes  |  |
 | l3Mapping | ArrayList<String>? |  yes  |  |
 | currency | String? |  yes  |  |
 | images | ArrayList<[Image](#Image)>? |  yes  |  |
 | primaryColor | String? |  yes  |  |
 | hsnCode | String? |  yes  |  |
 | productPublish | [ProductPublished](#ProductPublished)? |  yes  |  |
 | media | ArrayList<[Media1](#Media1)>? |  yes  |  |
 | description | String? |  yes  |  |
 | sizes | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | isPhysical | Boolean? |  yes  |  |
 | customOrder | HashMap<String,Any>? |  yes  |  |
 | multiSize | Boolean? |  yes  |  |
 | highlights | ArrayList<String>? |  yes  |  |
 | moq | HashMap<String,Any>? |  yes  |  |
 | allSizes | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | shortDescription | String? |  yes  |  |
 | brandUid | Int? |  yes  |  |
 | itemType | String? |  yes  |  |
 | isDependent | Boolean? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [ProductListingResponse](#ProductListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[Product](#Product)>? |  yes  |  |

---


 
 
 #### [ReturnConfig](#ReturnConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | returnable | Boolean? |  yes  |  |
 | time | Int? |  yes  |  |
 | unit | String? |  yes  |  |

---


 
 
 #### [Trader](#Trader)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | address | String |  no  |  |

---


 
 
 #### [ProductPublish](#ProductPublish)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isSet | Boolean? |  yes  |  |
 | productOnlineDate | String? |  yes  |  |

---


 
 
 #### [CustomOrder](#CustomOrder)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | manufacturingTimeUnit | String? |  yes  |  |
 | manufacturingTime | Int? |  yes  |  |
 | isCustomOrder | Boolean? |  yes  |  |

---


 
 
 #### [TeaserTag](#TeaserTag)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tag | String? |  yes  |  |
 | url | String? |  yes  |  |

---


 
 
 #### [OrderQuantity](#OrderQuantity)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isSet | Boolean? |  yes  |  |
 | maximum | Int? |  yes  |  |
 | minimum | Int? |  yes  |  |

---


 
 
 #### [ProductCreateUpdate](#ProductCreateUpdate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | departments | ArrayList<Int> |  no  |  |
 | isSet | Boolean? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | sizeGuide | String? |  yes  |  |
 | templateTag | String |  no  |  |
 | returnConfig | [ReturnConfig](#ReturnConfig)? |  yes  |  |
 | name | String |  no  |  |
 | uid | Int? |  yes  |  |
 | variants | HashMap<String,Any>? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | categorySlug | String |  no  |  |
 | trader | [Trader](#Trader)? |  yes  |  |
 | traderType | String? |  yes  |  |
 | requester | String? |  yes  |  |
 | countryOfOrigin | String |  no  |  |
 | slug | String |  no  |  |
 | itemCode | String |  no  |  |
 | isImageLessProduct | Boolean? |  yes  |  |
 | currency | String |  no  |  |
 | hsnCode | String |  no  |  |
 | productPublish | [ProductPublish](#ProductPublish)? |  yes  |  |
 | media | ArrayList<[Media1](#Media1)>? |  yes  |  |
 | companyId | Int |  no  |  |
 | description | String? |  yes  |  |
 | noOfBoxes | Int? |  yes  |  |
 | customOrder | [CustomOrder](#CustomOrder)? |  yes  |  |
 | multiSize | Boolean? |  yes  |  |
 | highlights | ArrayList<String>? |  yes  |  |
 | teaserTag | [TeaserTag](#TeaserTag)? |  yes  |  |
 | moq | [OrderQuantity](#OrderQuantity)? |  yes  |  |
 | shortDescription | String? |  yes  |  |
 | brandUid | Int |  no  |  |
 | itemType | String |  no  |  |
 | isDependent | Boolean? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | productGroupTag | ArrayList<String>? |  yes  |  |
 | changeRequestId | String? |  yes  |  |

---


 
 
 #### [ValidateProduct](#ValidateProduct)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | valid | Boolean? |  yes  |  |

---


 
 
 #### [UserDetail](#UserDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | userId | String? |  yes  |  |
 | username | String? |  yes  |  |
 | fullName | String? |  yes  |  |

---


 
 
 #### [ProductBulkRequest](#ProductBulkRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | failedRecords | ArrayList<String>? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | stage | String? |  yes  |  |
 | failed | Int? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | createdBy | [UserDetail](#UserDetail)? |  yes  |  |
 | total | Int? |  yes  |  |
 | filePath | String? |  yes  |  |
 | templateTag | String? |  yes  |  |
 | cancelled | Int? |  yes  |  |
 | succeed | Int? |  yes  |  |
 | cancelledRecords | ArrayList<String>? |  yes  |  |
 | modifiedBy | [UserDetail](#UserDetail)? |  yes  |  |
 | template | [ProductTemplate](#ProductTemplate)? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [ProductBulkRequestList](#ProductBulkRequestList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | [ProductBulkRequest](#ProductBulkRequest)? |  yes  |  |

---


 
 
 #### [UserInfo1](#UserInfo1)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | userId | String? |  yes  |  |
 | uid | String? |  yes  |  |
 | email | String? |  yes  |  |
 | username | String? |  yes  |  |

---


 
 
 #### [BulkJob](#BulkJob)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | failedRecords | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | createdBy | [UserInfo1](#UserInfo1)? |  yes  |  |
 | createdOn | String |  no  |  |
 | modifiedOn | String? |  yes  |  |
 | companyId | Int |  no  |  |
 | total | Int |  no  |  |
 | cancelled | Int? |  yes  |  |
 | failed | Int? |  yes  |  |
 | stage | String? |  yes  |  |
 | filePath | String? |  yes  |  |
 | templateTag | String? |  yes  |  |
 | succeed | Int? |  yes  |  |
 | cancelledRecords | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | modifiedBy | [UserInfo1](#UserInfo1)? |  yes  |  |
 | customTemplateTag | String? |  yes  |  |
 | trackingUrl | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [BulkProductRequest](#BulkProductRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | ArrayList<HashMap<String,Any>> |  no  |  |
 | batchId | String |  no  |  |
 | companyId | Int |  no  |  |
 | templateTag | String |  no  |  |

---


 
 
 #### [NestedTags](#NestedTags)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tags | ArrayList<String>? |  yes  |  |

---


 
 
 #### [ProductTagsViewResponse](#ProductTagsViewResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | [NestedTags](#NestedTags)? |  yes  |  |

---


 
 
 #### [UserCommon](#UserCommon)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | userId | String? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | username | String? |  yes  |  |

---


 
 
 #### [Items](#Items)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | failedRecords | ArrayList<String>? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | createdBy | [UserCommon](#UserCommon)? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | failed | Int? |  yes  |  |
 | stage | String? |  yes  |  |
 | total | Int? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | filePath | String? |  yes  |  |
 | cancelled | Int? |  yes  |  |
 | id | String? |  yes  |  |
 | retry | Int? |  yes  |  |
 | succeed | Int? |  yes  |  |
 | cancelledRecords | ArrayList<String>? |  yes  |  |
 | modifiedBy | [UserCommon](#UserCommon)? |  yes  |  |
 | trackingUrl | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [BulkAssetResponse](#BulkAssetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[Items](#Items)>? |  yes  |  |

---


 
 
 #### [ProductBulkAssets](#ProductBulkAssets)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companyId | Int? |  yes  |  |
 | url | String |  no  |  |
 | user | HashMap<String,Any> |  no  |  |

---


 
 
 #### [ProductSizeDeleteDataResponse](#ProductSizeDeleteDataResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companyId | Int? |  yes  |  |
 | itemId | Int? |  yes  |  |
 | size | String? |  yes  |  |

---


 
 
 #### [ProductSizeDeleteResponse](#ProductSizeDeleteResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [ProductSizeDeleteDataResponse](#ProductSizeDeleteDataResponse)? |  yes  |  |
 | success | Boolean? |  yes  |  |

---


 
 
 #### [InventoryResponse](#InventoryResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | currency | String? |  yes  |  |
 | priceEffective | Int? |  yes  |  |
 | store | HashMap<String,Any>? |  yes  |  |
 | inventoryUpdatedOn | String? |  yes  |  |
 | sellerIdentifier | Int? |  yes  |  |
 | price | Int? |  yes  |  |
 | identifiers | HashMap<String,Any>? |  yes  |  |
 | itemId | Int? |  yes  |  |
 | uid | String? |  yes  |  |
 | quantity | Int? |  yes  |  |
 | size | String? |  yes  |  |
 | priceTransfer | Int? |  yes  |  |
 | sellableQuantity | Int? |  yes  |  |

---


 
 
 #### [GTIN](#GTIN)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | primary | Boolean? |  yes  |  |
 | gtinValue | String |  no  |  |
 | gtinType | String |  no  |  |

---


 
 
 #### [SetSize](#SetSize)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pieces | Int |  no  |  |
 | size | String |  no  |  |

---


 
 
 #### [SizeDistribution](#SizeDistribution)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sizes | ArrayList<[SetSize](#SetSize)> |  no  |  |

---


 
 
 #### [InventorySet](#InventorySet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sizeDistribution | [SizeDistribution](#SizeDistribution) |  no  |  |
 | quantity | Int? |  yes  |  |

---


 
 
 #### [InvSize](#InvSize)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | currency | String |  no  |  |
 | priceEffective | Double |  no  |  |
 | itemLength | Double? |  yes  |  |
 | isSet | Boolean? |  yes  |  |
 | storeCode | String |  no  |  |
 | itemWidth | Double? |  yes  |  |
 | itemDimensionsUnitOfMeasure | String? |  yes  |  |
 | itemWeightUnitOfMeasure | String? |  yes  |  |
 | price | Double |  no  |  |
 | identifiers | ArrayList<[GTIN](#GTIN)> |  no  |  |
 | itemHeight | Double? |  yes  |  |
 | size | String |  no  |  |
 | priceTransfer | Double? |  yes  |  |
 | quantity | Int |  no  |  |
 | itemWeight | Double? |  yes  |  |
 | set | [InventorySet](#InventorySet)? |  yes  |  |

---


 
 
 #### [ItemQuery](#ItemQuery)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | itemCode | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | brandUid | Int? |  yes  |  |

---


 
 
 #### [InventoryRequest](#InventoryRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companyId | Int |  no  |  |
 | sizes | ArrayList<[InvSize](#InvSize)> |  no  |  |
 | item | [ItemQuery](#ItemQuery) |  no  |  |

---


 
 
 #### [InventoryDeleteData](#InventoryDeleteData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | locationId | Int? |  yes  |  |
 | itemId | Int? |  yes  |  |
 | size | String? |  yes  |  |

---


 
 
 #### [InventoryDelete](#InventoryDelete)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [InventoryDeleteData](#InventoryDeleteData)? |  yes  |  |
 | success | Boolean? |  yes  |  |

---


 
 
 #### [BulkInventoryGetItems](#BulkInventoryGetItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | failedRecords | ArrayList<String>? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | cancelled | Int? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | failed | Int? |  yes  |  |
 | id | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | filePath | String? |  yes  |  |
 | stage | String? |  yes  |  |
 | total | Int? |  yes  |  |
 | succeed | Int? |  yes  |  |
 | cancelledRecords | ArrayList<String>? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [BulkInventoryGet](#BulkInventoryGet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[BulkInventoryGetItems](#BulkInventoryGetItems)>? |  yes  |  |

---


 
 
 #### [CommonResponse](#CommonResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | String? |  yes  |  |

---


 
 
 #### [Size1](#Size1)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | currency | String |  no  |  |
 | priceEffective | Double |  no  |  |
 | itemLength | Double? |  yes  |  |
 | isSet | Boolean? |  yes  |  |
 | storeCode | String |  no  |  |
 | itemWidth | Double? |  yes  |  |
 | itemDimensionsUnitOfMeasure | String? |  yes  |  |
 | itemWeightUnitOfMeasure | String? |  yes  |  |
 | price | Double |  no  |  |
 | identifiers | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | sellerIdentifier | String |  no  |  |
 | itemHeight | Double? |  yes  |  |
 | size | String? |  yes  |  |
 | priceTransfer | Double? |  yes  |  |
 | quantity | Int |  no  |  |
 | itemWeight | Double? |  yes  |  |
 | set | [InventorySet](#InventorySet)? |  yes  |  |

---


 
 
 #### [InventoryBulkRequest](#InventoryBulkRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | batchId | String |  no  |  |
 | companyId | Int |  no  |  |
 | sizes | ArrayList<[Size1](#Size1)> |  no  |  |
 | user | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [InventoryExportJob](#InventoryExportJob)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | taskId | String |  no  |  |
 | status | String? |  yes  |  |
 | url | String? |  yes  |  |
 | triggerOn | String? |  yes  |  |
 | completedOn | String? |  yes  |  |
 | requestParams | HashMap<String,Any>? |  yes  |  |
 | sellerId | Int |  no  |  |

---


 
 
 #### [InventoryExportRequest](#InventoryExportRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | store | ArrayList<Int>? |  yes  |  |
 | brand | ArrayList<Int>? |  yes  |  |

---


 
 
 #### [FilerList](#FilerList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [InventoryConfig](#InventoryConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | ArrayList<[FilerList](#FilerList)>? |  yes  |  |
 | multivalues | Boolean? |  yes  |  |

---


 
 
 #### [PageResponse](#PageResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | hasPrevious | Boolean? |  yes  |  |
 | current | String? |  yes  |  |
 | hasNext | Boolean? |  yes  |  |
 | itemTotal | Int? |  yes  |  |
 | size | Int? |  yes  |  |

---


 
 
 #### [HsnCodesObject](#HsnCodesObject)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tax1 | Double? |  yes  |  |
 | threshold2 | Double? |  yes  |  |
 | taxOnEsp | Boolean? |  yes  |  |
 | hsnCode | String? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | id | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | hs2Code | String? |  yes  |  |
 | taxOnMrp | Boolean? |  yes  |  |
 | threshold1 | Double? |  yes  |  |
 | tax2 | Double? |  yes  |  |

---


 
 
 #### [HsnCodesListingResponse](#HsnCodesListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [PageResponse](#PageResponse)? |  yes  |  |
 | items | ArrayList<[HsnCodesObject](#HsnCodesObject)>? |  yes  |  |

---


 
 
 #### [HsnUpsert](#HsnUpsert)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tax1 | Double |  no  |  |
 | threshold2 | Double? |  yes  |  |
 | taxOnEsp | Boolean? |  yes  |  |
 | hsnCode | String |  no  |  |
 | companyId | Int |  no  |  |
 | hs2Code | String |  no  |  |
 | taxOnMrp | Boolean |  no  |  |
 | uid | Int? |  yes  |  |
 | threshold1 | Double |  no  |  |
 | tax2 | Double? |  yes  |  |

---


 
 
 #### [HsnCode](#HsnCode)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [HsnCodesObject](#HsnCodesObject)? |  yes  |  |

---


 
 
 #### [BulkHsnUpsert](#BulkHsnUpsert)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | ArrayList<[HsnUpsert](#HsnUpsert)> |  no  |  |

---


 
 
 #### [BulkHsnResponse](#BulkHsnResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |

---


 
 
 #### [BrandItem](#BrandItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | departments | ArrayList<String>? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | slug | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | name | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | logo | [Media](#Media)? |  yes  |  |
 | discount | String? |  yes  |  |

---


 
 
 #### [BrandListingResponse](#BrandListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page) |  no  |  |
 | items | ArrayList<[BrandItem](#BrandItem)>? |  yes  |  |

---


 
 
 #### [Department](#Department)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | priorityOrder | Int? |  yes  |  |
 | slug | String? |  yes  |  |
 | name | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | logo | [Media](#Media)? |  yes  |  |

---


 
 
 #### [DepartmentResponse](#DepartmentResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Department](#Department)>? |  yes  |  |

---


 
 
 #### [ThirdLevelChild](#ThirdLevelChild)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | childs | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | slug | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | name | String? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | uid | Int? |  yes  |  |

---


 
 
 #### [SecondLevelChild](#SecondLevelChild)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | childs | ArrayList<[ThirdLevelChild](#ThirdLevelChild)>? |  yes  |  |
 | slug | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | name | String? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | uid | Int? |  yes  |  |

---


 
 
 #### [Child](#Child)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | childs | ArrayList<[SecondLevelChild](#SecondLevelChild)>? |  yes  |  |
 | slug | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | name | String? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | uid | Int? |  yes  |  |

---


 
 
 #### [CategoryItems](#CategoryItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | childs | ArrayList<[Child](#Child)>? |  yes  |  |
 | slug | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | name | String? |  yes  |  |
 | uid | Int? |  yes  |  |

---


 
 
 #### [DepartmentCategoryTree](#DepartmentCategoryTree)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | department | String? |  yes  |  |
 | items | ArrayList<[CategoryItems](#CategoryItems)>? |  yes  |  |

---


 
 
 #### [DepartmentIdentifier](#DepartmentIdentifier)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | slug | String? |  yes  |  |
 | uid | Int? |  yes  |  |

---


 
 
 #### [CategoryListingResponse](#CategoryListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | ArrayList<[DepartmentCategoryTree](#DepartmentCategoryTree)>? |  yes  |  |
 | departments | ArrayList<[DepartmentIdentifier](#DepartmentIdentifier)>? |  yes  |  |

---


 
 
 #### [ApplicationProductListingResponse](#ApplicationProductListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | filters | ArrayList<[ProductFilters](#ProductFilters)>? |  yes  |  |
 | page | [Page](#Page) |  no  |  |
 | sortOn | ArrayList<[ProductSortOn](#ProductSortOn)>? |  yes  |  |
 | items | ArrayList<[ProductListingDetail](#ProductListingDetail)>? |  yes  |  |

---


 
 
 #### [ProductDetail](#ProductDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | imageNature | String? |  yes  |  |
 | similars | ArrayList<String>? |  yes  |  |
 | medias | ArrayList<[Media1](#Media1)>? |  yes  |  |
 | hasVariant | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | brand | [ProductBrand](#ProductBrand)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | color | String? |  yes  |  |
 | type | String? |  yes  |  |
 | attributes | HashMap<String,Any>? |  yes  |  |
 | slug | String |  no  |  |
 | itemCode | String? |  yes  |  |
 | rating | Double? |  yes  |  |
 | tryouts | ArrayList<String>? |  yes  |  |
 | description | String? |  yes  |  |
 | highlights | ArrayList<String>? |  yes  |  |
 | teaserTag | HashMap<String,Any>? |  yes  |  |
 | promoMeta | HashMap<String,Any>? |  yes  |  |
 | shortDescription | String? |  yes  |  |
 | groupedAttributes | ArrayList<[ProductDetailGroupedAttribute](#ProductDetailGroupedAttribute)>? |  yes  |  |
 | itemType | String? |  yes  |  |
 | productOnlineDate | String? |  yes  |  |
 | ratingCount | Int? |  yes  |  |

---




 
 
 #### [SellerPhoneNumber](#SellerPhoneNumber)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | number | String |  no  |  |
 | countryCode | Int |  no  |  |

---


 
 
 #### [ContactDetails](#ContactDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | emails | ArrayList<String>? |  yes  |  |
 | phone | ArrayList<[SellerPhoneNumber](#SellerPhoneNumber)>? |  yes  |  |

---


 
 
 #### [GetAddressSerializer](#GetAddressSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | address2 | String? |  yes  |  |
 | address1 | String? |  yes  |  |
 | addressType | String? |  yes  |  |
 | state | String? |  yes  |  |
 | latitude | Double? |  yes  |  |
 | landmark | String? |  yes  |  |
 | city | String? |  yes  |  |
 | country | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | longitude | Double? |  yes  |  |
 | pincode | Int? |  yes  |  |

---


 
 
 #### [Document](#Document)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String |  no  |  |
 | verified | Boolean? |  yes  |  |
 | url | String? |  yes  |  |
 | legalName | String? |  yes  |  |
 | value | String |  no  |  |

---


 
 
 #### [BusinessCountryInfo](#BusinessCountryInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | country | String? |  yes  |  |
 | countryCode | String? |  yes  |  |

---


 
 
 #### [Website](#Website)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | url | String? |  yes  |  |

---


 
 
 #### [BusinessDetails](#BusinessDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | website | [Website](#Website)? |  yes  |  |

---


 
 
 #### [GetCompanyProfileSerializerResponse](#GetCompanyProfileSerializerResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | modifiedBy | [UserSerializer](#UserSerializer)? |  yes  |  |
 | businessType | String |  no  |  |
 | mode | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | verifiedBy | [UserSerializer](#UserSerializer)? |  yes  |  |
 | notificationEmails | ArrayList<String>? |  yes  |  |
 | contactDetails | [ContactDetails](#ContactDetails)? |  yes  |  |
 | businessInfo | String? |  yes  |  |
 | addresses | ArrayList<[GetAddressSerializer](#GetAddressSerializer)>? |  yes  |  |
 | uid | Int |  no  |  |
 | documents | ArrayList<[Document](#Document)>? |  yes  |  |
 | businessCountryInfo | [BusinessCountryInfo](#BusinessCountryInfo)? |  yes  |  |
 | verifiedOn | String? |  yes  |  |
 | stage | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | franchiseEnabled | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | companyType | String |  no  |  |
 | warnings | HashMap<String,Any>? |  yes  |  |
 | businessDetails | [BusinessDetails](#BusinessDetails)? |  yes  |  |
 | createdBy | [UserSerializer](#UserSerializer)? |  yes  |  |

---


 
 
 #### [CreateUpdateAddressSerializer](#CreateUpdateAddressSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | address2 | String? |  yes  |  |
 | address1 | String |  no  |  |
 | latitude | Double |  no  |  |
 | state | String |  no  |  |
 | landmark | String? |  yes  |  |
 | addressType | String |  no  |  |
 | city | String |  no  |  |
 | country | String |  no  |  |
 | countryCode | String? |  yes  |  |
 | longitude | Double |  no  |  |
 | pincode | Int |  no  |  |

---


 
 
 #### [UpdateCompany](#UpdateCompany)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | businessType | String? |  yes  |  |
 | addresses | ArrayList<[CreateUpdateAddressSerializer](#CreateUpdateAddressSerializer)>? |  yes  |  |
 | rejectReason | String? |  yes  |  |
 | companyType | String? |  yes  |  |
 | notificationEmails | ArrayList<String>? |  yes  |  |
 | warnings | HashMap<String,Any>? |  yes  |  |
 | documents | ArrayList<[Document](#Document)>? |  yes  |  |
 | businessDetails | [BusinessDetails](#BusinessDetails)? |  yes  |  |
 | contactDetails | [ContactDetails](#ContactDetails)? |  yes  |  |
 | franchiseEnabled | Boolean? |  yes  |  |
 | businessInfo | String? |  yes  |  |

---


 
 
 #### [DocumentsObj](#DocumentsObj)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | verified | Int? |  yes  |  |
 | pending | Int? |  yes  |  |

---


 
 
 #### [MetricsSerializer](#MetricsSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | store | [DocumentsObj](#DocumentsObj)? |  yes  |  |
 | stage | String? |  yes  |  |
 | companyDocuments | [DocumentsObj](#DocumentsObj)? |  yes  |  |
 | product | [DocumentsObj](#DocumentsObj)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | storeDocuments | [DocumentsObj](#DocumentsObj)? |  yes  |  |
 | brand | [DocumentsObj](#DocumentsObj)? |  yes  |  |

---


 
 
 #### [BrandBannerSerializer](#BrandBannerSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | portrait | String? |  yes  |  |
 | landscape | String? |  yes  |  |

---


 
 
 #### [CreateUpdateBrandRequestSerializer](#CreateUpdateBrandRequestSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | banner | [BrandBannerSerializer](#BrandBannerSerializer)? |  yes  |  |
 | brandTier | String? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | synonyms | ArrayList<String>? |  yes  |  |
 | uid | Int? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | description | String? |  yes  |  |
 | logo | String |  no  |  |
 | localeLanguage | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [UserSerializer1](#UserSerializer1)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | userId | String? |  yes  |  |
 | username | String? |  yes  |  |
 | contact | String? |  yes  |  |

---


 
 
 #### [GetBrandResponseSerializer](#GetBrandResponseSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | modifiedBy | [UserSerializer1](#UserSerializer1)? |  yes  |  |
 | name | String |  no  |  |
 | banner | [BrandBannerSerializer](#BrandBannerSerializer)? |  yes  |  |
 | rejectReason | String? |  yes  |  |
 | slugKey | String? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | synonyms | ArrayList<String>? |  yes  |  |
 | verifiedOn | String? |  yes  |  |
 | stage | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | verifiedBy | [UserSerializer1](#UserSerializer1)? |  yes  |  |
 | warnings | HashMap<String,Any>? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | description | String? |  yes  |  |
 | logo | String? |  yes  |  |
 | localeLanguage | HashMap<String,Any>? |  yes  |  |
 | createdBy | [UserSerializer1](#UserSerializer1)? |  yes  |  |

---


 
 
 #### [CompanyBrandPostRequestSerializer](#CompanyBrandPostRequestSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | company | Int |  no  |  |
 | brands | ArrayList<Int> |  no  |  |

---


 
 
 #### [GetCompanySerializer](#GetCompanySerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | modifiedBy | [UserSerializer](#UserSerializer)? |  yes  |  |
 | name | String? |  yes  |  |
 | businessType | String? |  yes  |  |
 | rejectReason | String? |  yes  |  |
 | addresses | ArrayList<[GetAddressSerializer](#GetAddressSerializer)>? |  yes  |  |
 | verifiedOn | String? |  yes  |  |
 | stage | String? |  yes  |  |
 | companyType | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | verifiedBy | [UserSerializer](#UserSerializer)? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | createdBy | [UserSerializer](#UserSerializer)? |  yes  |  |

---


 
 
 #### [CompanyBrandSerializer](#CompanyBrandSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | modifiedBy | [UserSerializer1](#UserSerializer1)? |  yes  |  |
 | rejectReason | String? |  yes  |  |
 | verifiedOn | String? |  yes  |  |
 | stage | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | verifiedBy | [UserSerializer1](#UserSerializer1)? |  yes  |  |
 | warnings | HashMap<String,Any>? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | brand | [GetBrandResponseSerializer](#GetBrandResponseSerializer)? |  yes  |  |
 | company | [GetCompanySerializer](#GetCompanySerializer)? |  yes  |  |
 | createdBy | [UserSerializer1](#UserSerializer1)? |  yes  |  |

---


 
 
 #### [CompanyBrandListSerializer](#CompanyBrandListSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[CompanyBrandSerializer](#CompanyBrandSerializer)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [GetAddressSerializer1](#GetAddressSerializer1)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | address2 | String? |  yes  |  |
 | address1 | String? |  yes  |  |
 | addressType | String? |  yes  |  |
 | state | String? |  yes  |  |
 | latitude | Double? |  yes  |  |
 | landmark | String? |  yes  |  |
 | city | String? |  yes  |  |
 | country | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | longitude | Double? |  yes  |  |
 | pincode | Int? |  yes  |  |

---


 
 
 #### [ProductReturnConfigSerializer](#ProductReturnConfigSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | onSameStore | Boolean? |  yes  |  |
 | storeUid | Int? |  yes  |  |

---


 
 
 #### [LocationTimingSerializer](#LocationTimingSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | minute | Int? |  yes  |  |
 | hour | Int? |  yes  |  |

---


 
 
 #### [LocationDayWiseSerializer](#LocationDayWiseSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | closing | [LocationTimingSerializer](#LocationTimingSerializer)? |  yes  |  |
 | weekday | String |  no  |  |
 | opening | [LocationTimingSerializer](#LocationTimingSerializer)? |  yes  |  |
 | open | Boolean |  no  |  |

---


 
 
 #### [InvoiceCredSerializer](#InvoiceCredSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | password | String? |  yes  |  |
 | username | String? |  yes  |  |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [InvoiceDetailsSerializer](#InvoiceDetailsSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | eInvoice | [InvoiceCredSerializer](#InvoiceCredSerializer)? |  yes  |  |
 | eWaybill | [InvoiceCredSerializer](#InvoiceCredSerializer)? |  yes  |  |

---


 
 
 #### [LocationManagerSerializer](#LocationManagerSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | mobileNo | [SellerPhoneNumber](#SellerPhoneNumber) |  no  |  |
 | email | String? |  yes  |  |

---


 
 
 #### [LocationSerializer](#LocationSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | storeType | String? |  yes  |  |
 | address | [GetAddressSerializer1](#GetAddressSerializer1) |  no  |  |
 | productReturnConfig | [ProductReturnConfigSerializer](#ProductReturnConfigSerializer)? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | timing | ArrayList<[LocationDayWiseSerializer](#LocationDayWiseSerializer)>? |  yes  |  |
 | stage | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | code | String |  no  |  |
 | notificationEmails | ArrayList<String>? |  yes  |  |
 | warnings | HashMap<String,Any>? |  yes  |  |
 | documents | ArrayList<[Document](#Document)>? |  yes  |  |
 | gstCredentials | [InvoiceDetailsSerializer](#InvoiceDetailsSerializer)? |  yes  |  |
 | manager | [LocationManagerSerializer](#LocationManagerSerializer)? |  yes  |  |
 | contactNumbers | ArrayList<[SellerPhoneNumber](#SellerPhoneNumber)>? |  yes  |  |
 | displayName | String |  no  |  |
 | company | Int |  no  |  |

---


 
 
 #### [LocationIntegrationType](#LocationIntegrationType)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | order | String? |  yes  |  |
 | inventory | String? |  yes  |  |

---


 
 
 #### [GetLocationSerializer](#GetLocationSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | modifiedBy | [UserSerializer1](#UserSerializer1)? |  yes  |  |
 | productReturnConfig | [ProductReturnConfigSerializer](#ProductReturnConfigSerializer)? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | code | String |  no  |  |
 | verifiedBy | [UserSerializer1](#UserSerializer1)? |  yes  |  |
 | notificationEmails | ArrayList<String>? |  yes  |  |
 | integrationType | [LocationIntegrationType](#LocationIntegrationType)? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | phoneNumber | String |  no  |  |
 | uid | Int? |  yes  |  |
 | documents | ArrayList<[Document](#Document)>? |  yes  |  |
 | manager | [LocationManagerSerializer](#LocationManagerSerializer)? |  yes  |  |
 | contactNumbers | ArrayList<[SellerPhoneNumber](#SellerPhoneNumber)>? |  yes  |  |
 | displayName | String |  no  |  |
 | address | [GetAddressSerializer](#GetAddressSerializer) |  no  |  |
 | timing | ArrayList<[LocationDayWiseSerializer](#LocationDayWiseSerializer)>? |  yes  |  |
 | verifiedOn | String? |  yes  |  |
 | stage | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | name | String |  no  |  |
 | storeType | String? |  yes  |  |
 | gstCredentials | [InvoiceDetailsSerializer](#InvoiceDetailsSerializer)? |  yes  |  |
 | warnings | HashMap<String,Any>? |  yes  |  |
 | company | [GetCompanySerializer](#GetCompanySerializer)? |  yes  |  |
 | createdBy | [UserSerializer1](#UserSerializer1)? |  yes  |  |

---


 
 
 #### [LocationListSerializer](#LocationListSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[GetLocationSerializer](#GetLocationSerializer)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [BulkLocationSerializer](#BulkLocationSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | ArrayList<[LocationSerializer](#LocationSerializer)>? |  yes  |  |

---




 
 
 #### [FailedResponse](#FailedResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String |  no  |  |

---


 
 
 #### [CDN](#CDN)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | url | String |  no  |  |

---


 
 
 #### [Upload](#Upload)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | expiry | Int |  no  |  |
 | url | String |  no  |  |

---


 
 
 #### [StartResponse](#StartResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | fileName | String |  no  |  |
 | filePath | String |  no  |  |
 | contentType | String |  no  |  |
 | method | String |  no  |  |
 | namespace | String |  no  |  |
 | operation | String |  no  |  |
 | size | Int |  no  |  |
 | upload | [Upload](#Upload) |  no  |  |
 | cdn | [CDN](#CDN) |  no  |  |
 | tags | ArrayList<String>? |  yes  |  |

---


 
 
 #### [StartRequest](#StartRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | fileName | String |  no  |  |
 | contentType | String |  no  |  |
 | size | Int |  no  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | params | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [CompleteResponse](#CompleteResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |
 | fileName | String |  no  |  |
 | filePath | String |  no  |  |
 | contentType | String |  no  |  |
 | method | String |  no  |  |
 | namespace | String |  no  |  |
 | operation | String |  no  |  |
 | size | Int |  no  |  |
 | upload | [Upload](#Upload) |  no  |  |
 | cdn | [CDN](#CDN) |  no  |  |
 | success | String |  no  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | createdOn | String |  no  |  |
 | modifiedOn | String |  no  |  |

---


 
 
 #### [Opts](#Opts)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | attempts | Int? |  yes  |  |
 | timestamp | Int? |  yes  |  |
 | delay | Int? |  yes  |  |

---


 
 
 #### [CopyFileTask](#CopyFileTask)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |
 | name | String |  no  |  |
 | data | [BulkRequest](#BulkRequest) |  no  |  |
 | opts | [Opts](#Opts) |  no  |  |
 | progress | Int |  no  |  |
 | delay | Int |  no  |  |
 | timestamp | Int |  no  |  |
 | attemptsMade | Int |  no  |  |
 | stacktrace | ArrayList<String>? |  yes  |  |
 | finishedOn | Int |  no  |  |
 | processedOn | Int |  no  |  |

---


 
 
 #### [BulkResponse](#BulkResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | trackingUrl | String |  no  |  |
 | task | [CopyFileTask](#CopyFileTask) |  no  |  |

---


 
 
 #### [ReqConfiguration](#ReqConfiguration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | concurrency | Int? |  yes  |  |

---


 
 
 #### [Destination](#Destination)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | namespace | String |  no  |  |
 | rewrite | String |  no  |  |
 | basepath | String? |  yes  |  |

---


 
 
 #### [BulkRequest](#BulkRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | urls | ArrayList<String> |  no  |  |
 | destination | [Destination](#Destination) |  no  |  |
 | configuration | [ReqConfiguration](#ReqConfiguration)? |  yes  |  |

---


 
 
 #### [Urls](#Urls)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | url | String |  no  |  |
 | signedUrl | String |  no  |  |
 | expiry | Int |  no  |  |

---


 
 
 #### [SignUrlResponse](#SignUrlResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | urls | ArrayList<[Urls](#Urls)> |  no  |  |

---


 
 
 #### [SignUrlRequest](#SignUrlRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | expiry | Int |  no  |  |
 | urls | ArrayList<String> |  no  |  |

---


 
 
 #### [DbRecord](#DbRecord)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean |  no  |  |
 | tags | ArrayList<String> |  no  |  |
 | id | String |  no  |  |
 | fileName | String |  no  |  |
 | operation | String? |  yes  |  |
 | namespace | String |  no  |  |
 | contentType | String |  no  |  |
 | filePath | String |  no  |  |
 | upload | [Upload](#Upload) |  no  |  |
 | cdn | [CDN](#CDN) |  no  |  |
 | createdOn | String |  no  |  |
 | modifiedOn | String |  no  |  |

---


 
 
 #### [BrowseResponse](#BrowseResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[DbRecord](#DbRecord)> |  no  |  |
 | page | [Page](#Page) |  no  |  |

---




 
 
 #### [RedirectDevice](#RedirectDevice)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | link | String? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [WebRedirect](#WebRedirect)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | link | String? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [Redirects](#Redirects)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ios | [RedirectDevice](#RedirectDevice)? |  yes  |  |
 | android | [RedirectDevice](#RedirectDevice)? |  yes  |  |
 | web | [WebRedirect](#WebRedirect)? |  yes  |  |
 | forceWeb | Boolean? |  yes  |  |

---


 
 
 #### [CampaignShortLink](#CampaignShortLink)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | source | String? |  yes  |  |
 | medium | String? |  yes  |  |

---


 
 
 #### [Attribution](#Attribution)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | campaignCookieExpiry | String? |  yes  |  |

---


 
 
 #### [SocialMediaTags](#SocialMediaTags)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | description | String? |  yes  |  |
 | image | String? |  yes  |  |

---


 
 
 #### [ShortLinkReq](#ShortLinkReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String |  no  | Give a name to the link. |
 | url | String |  no  | The web address to shorten. |
 | hash | String? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | expireAt | String? |  yes  |  |
 | enableTracking | Boolean? |  yes  |  |
 | personalized | Boolean? |  yes  | To create personalized short links. |
 | campaign | [CampaignShortLink](#CampaignShortLink)? |  yes  |  |
 | redirects | [Redirects](#Redirects)? |  yes  |  |
 | attribution | [Attribution](#Attribution)? |  yes  |  |
 | socialMediaTags | [SocialMediaTags](#SocialMediaTags)? |  yes  |  |
 | count | Int? |  yes  |  |

---


 
 
 #### [UrlInfo](#UrlInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | original | String? |  yes  |  |
 | short | String? |  yes  |  |
 | hash | String? |  yes  |  |

---


 
 
 #### [ShortLinkRes](#ShortLinkRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | url | [UrlInfo](#UrlInfo)? |  yes  |  |
 | createdBy | String? |  yes  |  |
 | appRedirect | Boolean? |  yes  |  |
 | fallback | String? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | enableTracking | Boolean? |  yes  |  |
 | expireAt | String? |  yes  |  |
 | application | String? |  yes  |  |
 | userId | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | personalized | Boolean? |  yes  | To create personalized short links |
 | campaign | [CampaignShortLink](#CampaignShortLink)? |  yes  |  |
 | redirects | [Redirects](#Redirects)? |  yes  |  |
 | attribution | [Attribution](#Attribution)? |  yes  |  |
 | socialMediaTags | [SocialMediaTags](#SocialMediaTags)? |  yes  |  |
 | count | Int? |  yes  |  |

---


 
 
 #### [ShortLinkList](#ShortLinkList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[ShortLinkRes](#ShortLinkRes)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [ErrorRes](#ErrorRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---




 
 
 #### [DataTresholdDTO](#DataTresholdDTO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | minPrice | Double? |  yes  |  |
 | safeStock | Int? |  yes  |  |
 | periodThreshold | Int? |  yes  |  |
 | periodThresholdType | String? |  yes  |  |
 | periodTypeList | ArrayList<[GenericDTO](#GenericDTO)>? |  yes  |  |

---


 
 
 #### [GenericDTO](#GenericDTO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | text | String? |  yes  |  |
 | value | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [JobConfigDTO](#JobConfigDTO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | integration | String |  no  |  |
 | integrationData | HashMap<String,HashMap<String,Any>>? |  yes  |  |
 | companyName | String? |  yes  |  |
 | companyId | Int |  no  |  |
 | taskDetails | [TaskDTO](#TaskDTO)? |  yes  |  |
 | thresholdDetails | [DataTresholdDTO](#DataTresholdDTO)? |  yes  |  |
 | jobCode | String? |  yes  |  |
 | alias | String? |  yes  |  |

---


 
 
 #### [TaskDTO](#TaskDTO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | Int? |  yes  |  |
 | groupList | ArrayList<[GenericDTO](#GenericDTO)>? |  yes  |  |

---


 
 
 #### [ResponseEnvelopeString](#ResponseEnvelopeString)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | timestamp | String? |  yes  |  |
 | status | Int? |  yes  |  |
 | error | String? |  yes  |  |
 | exception | String? |  yes  |  |
 | message | String? |  yes  |  |
 | totalTimeTakenInMillis | Int? |  yes  |  |
 | httpStatus | String? |  yes  |  |
 | items | String? |  yes  |  |
 | payload | String? |  yes  |  |
 | traceId | String? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [AWSS3config](#AWSS3config)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | bucket | String? |  yes  |  |
 | region | String? |  yes  |  |
 | dir | String? |  yes  |  |
 | accessKey | String? |  yes  |  |
 | secretKey | String? |  yes  |  |
 | localFilePath | String? |  yes  |  |
 | archivePath | String? |  yes  |  |
 | archive | Boolean? |  yes  |  |
 | delete | Boolean? |  yes  |  |
 | unzip | Boolean? |  yes  |  |
 | zipFormat | String? |  yes  |  |
 | fileRegex | String? |  yes  |  |
 | archiveConfig | [ArchiveConfig](#ArchiveConfig)? |  yes  |  |

---


 
 
 #### [ArchiveConfig](#ArchiveConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | delete | Boolean? |  yes  |  |
 | archive | Boolean? |  yes  |  |
 | archiveDir | String? |  yes  |  |

---


 
 
 #### [Audit](#Audit)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | createdBy | String? |  yes  |  |
 | modifiedBy | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |

---


 
 
 #### [CatalogMasterConfig](#CatalogMasterConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sourceSlug | String? |  yes  |  |

---


 
 
 #### [CompanyConfig](#CompanyConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companyId | Int? |  yes  |  |
 | excludeSteps | ArrayList<Int>? |  yes  |  |
 | hiddenClosetKeys | ArrayList<String>? |  yes  |  |
 | openTags | HashMap<String,HashMap<String,Any>>? |  yes  |  |
 | taxIdentifiers | ArrayList<String>? |  yes  |  |
 | deleteQuantityThreshold | Int? |  yes  |  |

---


 
 
 #### [DBConfig](#DBConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | vendor | String? |  yes  |  |
 | host | String? |  yes  |  |
 | port | Int? |  yes  |  |
 | username | String? |  yes  |  |
 | password | String? |  yes  |  |
 | dbname | String? |  yes  |  |
 | query | String? |  yes  |  |
 | procedure | Boolean? |  yes  |  |
 | driverClass | String? |  yes  |  |
 | jdbcUrl | String? |  yes  |  |
 | optionalProperties | HashMap<String,String>? |  yes  |  |

---


 
 
 #### [DBConnectionProfile](#DBConnectionProfile)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | inventory | String? |  yes  |  |

---


 
 
 #### [DBParamConfig](#DBParamConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | params | HashMap<String,HashMap<String,Any>>? |  yes  |  |

---


 
 
 #### [DefaultHeadersDTO](#DefaultHeadersDTO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | store | [PropBeanDTO](#PropBeanDTO)? |  yes  |  |
 | intfArticleId | [PropBeanDTO](#PropBeanDTO)? |  yes  |  |
 | priceEffective | [PropBeanDTO](#PropBeanDTO)? |  yes  |  |
 | quantity | [PropBeanDTO](#PropBeanDTO)? |  yes  |  |

---


 
 
 #### [DocMappingConfig](#DocMappingConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | properties | HashMap<String,HashMap<String,Any>>? |  yes  |  |
 | junkDataThresholdCount | Int? |  yes  |  |
 | propBeanConfigs | ArrayList<[PropBeanConfig](#PropBeanConfig)>? |  yes  |  |
 | unwindField | String? |  yes  |  |
 | defaultHeaders | [DefaultHeadersDTO](#DefaultHeadersDTO)? |  yes  |  |

---


 
 
 #### [EmailConfig](#EmailConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | recepient | String? |  yes  |  |
 | host | String? |  yes  |  |
 | username | String? |  yes  |  |
 | password | String? |  yes  |  |
 | unzip | Boolean? |  yes  |  |
 | readFromContent | Boolean? |  yes  |  |
 | filterBasedOnRecepients | Boolean? |  yes  |  |
 | pcol | String? |  yes  |  |
 | subjectLineRegex | String? |  yes  |  |
 | senderAddress | String? |  yes  |  |
 | localDir | String? |  yes  |  |
 | folderNameHierarchies | ArrayList<String>? |  yes  |  |
 | attachmentRegex | String? |  yes  |  |
 | bodyContentRegex | String? |  yes  |  |
 | passwordProtected | Boolean? |  yes  |  |
 | zipFormat | String? |  yes  |  |
 | attachmentMandate | Boolean? |  yes  |  |
 | filterFilesAfterExtraction | Boolean? |  yes  |  |
 | archiveConfig | [ArchiveConfig](#ArchiveConfig)? |  yes  |  |
 | readAllUnreadMails | Boolean? |  yes  |  |
 | contentType | String? |  yes  |  |
 | downloadableLink | Boolean? |  yes  |  |
 | properties | HashMap<String,String>? |  yes  |  |

---


 
 
 #### [FTPConfig](#FTPConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | host | String? |  yes  |  |
 | port | Int? |  yes  |  |
 | username | String? |  yes  |  |
 | password | String? |  yes  |  |
 | unzip | Boolean? |  yes  |  |
 | retries | Int? |  yes  |  |
 | interval | Int? |  yes  |  |
 | localDir | String? |  yes  |  |
 | remoteDir | String? |  yes  |  |
 | zipFileRegex | String? |  yes  |  |
 | archiveConfig | [ArchiveConfig](#ArchiveConfig)? |  yes  |  |
 | fileRegex | String? |  yes  |  |
 | zipFormat | String? |  yes  |  |
 | readAllFiles | Boolean? |  yes  |  |

---


 
 
 #### [FileConfig](#FileConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | delimiter | String? |  yes  |  |
 | charset | String? |  yes  |  |
 | properties | HashMap<String,HashMap<String,Any>>? |  yes  |  |
 | fileHasHeader | Boolean? |  yes  |  |
 | headerIndex | Int? |  yes  |  |
 | headerArray | ArrayList<String>? |  yes  |  |
 | dataStartIndex | Int? |  yes  |  |
 | propBeanConfigs | ArrayList<[PropBeanConfig](#PropBeanConfig)>? |  yes  |  |
 | junkDataThresholdCount | Int? |  yes  |  |
 | fileType | String? |  yes  |  |
 | lineValidityCheck | Boolean? |  yes  |  |
 | sheetNames | ArrayList<String>? |  yes  |  |
 | readAllSheets | Boolean? |  yes  |  |
 | quoteChar | String? |  yes  |  |
 | escapeChar | String? |  yes  |  |
 | defaultHeaders | [DefaultHeadersDTO](#DefaultHeadersDTO)? |  yes  |  |

---


 
 
 #### [GoogleSpreadSheetConfig](#GoogleSpreadSheetConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | range | String? |  yes  |  |
 | sheetId | String? |  yes  |  |
 | clientSecretLocation | String? |  yes  |  |
 | credStorageDirectory | String? |  yes  |  |
 | localDir | String? |  yes  |  |
 | archiveConfig | [ArchiveConfig](#ArchiveConfig)? |  yes  |  |

---


 
 
 #### [HttpConfig](#HttpConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | hosturl | String? |  yes  |  |
 | username | String? |  yes  |  |
 | password | String? |  yes  |  |
 | requestParams | HashMap<String,String>? |  yes  |  |
 | httpMethod | String? |  yes  |  |
 | requestPayload | String? |  yes  |  |
 | localPath | String? |  yes  |  |
 | archiveConfig | [ArchiveConfig](#ArchiveConfig)? |  yes  |  |

---


 
 
 #### [JobConfig](#JobConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |
 | jobCode | String? |  yes  |  |
 | taskType | String? |  yes  |  |
 | syncDelay | Int? |  yes  |  |
 | cronExpression | String? |  yes  |  |
 | storeFilter | [StoreFilter](#StoreFilter)? |  yes  |  |
 | processConfig | [ProcessConfig](#ProcessConfig)? |  yes  |  |
 | storeConfig | ArrayList<[StoreConfig](#StoreConfig)>? |  yes  |  |
 | properties | HashMap<String,String>? |  yes  |  |
 | immediateFirstRun | Boolean? |  yes  |  |
 | disable | Boolean? |  yes  |  |
 | dependentJobCodes | ArrayList<String>? |  yes  |  |
 | companyConfig | ArrayList<[CompanyConfig](#CompanyConfig)>? |  yes  |  |
 | companyIds | ArrayList<Int>? |  yes  |  |
 | taxIdentifiers | ArrayList<String>? |  yes  |  |
 | priority | String? |  yes  |  |
 | periodThreshold | Int? |  yes  |  |
 | periodThresholdType | String? |  yes  |  |
 | dbConnectionProfile | [DBConnectionProfile](#DBConnectionProfile)? |  yes  |  |
 | params | HashMap<String,HashMap<String,Any>>? |  yes  |  |
 | openTags | HashMap<String,HashMap<String,Any>>? |  yes  |  |
 | deleteQuantityThreshold | Int? |  yes  |  |
 | catalogMasterConfig | [CatalogMasterConfig](#CatalogMasterConfig)? |  yes  |  |
 | aggregatorTypes | ArrayList<String>? |  yes  |  |
 | integrationType | String? |  yes  |  |
 | minPrice | Double? |  yes  |  |
 | audit | [Audit](#Audit)? |  yes  |  |
 | version | Int? |  yes  |  |
 | alias | String? |  yes  |  |

---


 
 
 #### [JobConfigRawDTO](#JobConfigRawDTO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | integration | String |  no  |  |
 | companyName | String |  no  |  |
 | companyId | Int |  no  |  |
 | data | [JobConfig](#JobConfig)? |  yes  |  |

---


 
 
 #### [JsonDocConfig](#JsonDocConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | propBeanConfigs | ArrayList<[PropBeanConfig](#PropBeanConfig)>? |  yes  |  |

---


 
 
 #### [LocalFileConfig](#LocalFileConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | retries | Int? |  yes  |  |
 | interval | Int? |  yes  |  |
 | localDir | String? |  yes  |  |
 | workingDir | String? |  yes  |  |
 | unzip | Boolean? |  yes  |  |
 | zipFileRegex | String? |  yes  |  |
 | fileRegex | String? |  yes  |  |
 | zipFormat | String? |  yes  |  |
 | archiveConfig | [ArchiveConfig](#ArchiveConfig)? |  yes  |  |
 | readAllFiles | Boolean? |  yes  |  |

---


 
 
 #### [MongoDocConfig](#MongoDocConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | collectionName | String? |  yes  |  |
 | findQuery | HashMap<String,HashMap<String,Any>>? |  yes  |  |
 | projectionQuery | HashMap<String,HashMap<String,Any>>? |  yes  |  |
 | propBeanConfigs | ArrayList<[PropBeanConfig](#PropBeanConfig)>? |  yes  |  |
 | aggregatePipeline | ArrayList<HashMap<String,HashMap<String,Any>>>? |  yes  |  |
 | skipSave | Boolean? |  yes  |  |

---


 
 
 #### [OAuthConfig](#OAuthConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | limit | Int? |  yes  |  |
 | pages | Int? |  yes  |  |
 | interval | Int? |  yes  |  |
 | consumerKey | String? |  yes  |  |
 | consumerSecret | String? |  yes  |  |
 | token | String? |  yes  |  |
 | tokenSecret | String? |  yes  |  |
 | restUrl | String? |  yes  |  |
 | restBaseUrl | String? |  yes  |  |
 | functionName | String? |  yes  |  |

---


 
 
 #### [ProcessConfig](#ProcessConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | dbConfig | [DBConfig](#DBConfig)? |  yes  |  |
 | dbParamConfig | [DBParamConfig](#DBParamConfig)? |  yes  |  |
 | sftpConfig | [SFTPConfig](#SFTPConfig)? |  yes  |  |
 | awsS3Config | [AWSS3config](#AWSS3config)? |  yes  |  |
 | mongoDocConfig | [MongoDocConfig](#MongoDocConfig)? |  yes  |  |
 | ftpConfig | [FTPConfig](#FTPConfig)? |  yes  |  |
 | emailConfig | [EmailConfig](#EmailConfig)? |  yes  |  |
 | fileConfig | [FileConfig](#FileConfig)? |  yes  |  |
 | jsonDocConfig | [JsonDocConfig](#JsonDocConfig)? |  yes  |  |
 | docMappingConfig | [DocMappingConfig](#DocMappingConfig)? |  yes  |  |
 | taskStepConfig | [TaskStepConfig](#TaskStepConfig)? |  yes  |  |
 | httpConfig | [HttpConfig](#HttpConfig)? |  yes  |  |
 | localFileConfig | [LocalFileConfig](#LocalFileConfig)? |  yes  |  |
 | oauthConfig | [OAuthConfig](#OAuthConfig)? |  yes  |  |
 | googleSpreadsheetConfig | [GoogleSpreadSheetConfig](#GoogleSpreadSheetConfig)? |  yes  |  |

---


 
 
 #### [PropBeanConfig](#PropBeanConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | required | Boolean? |  yes  |  |
 | mapping | HashMap<String,[PropBeanConfig](#PropBeanConfig)>? |  yes  |  |
 | optional | Boolean? |  yes  |  |
 | send | [Send](#Send)? |  yes  |  |
 | validations | ArrayList<HashMap<String,HashMap<String,Any>>>? |  yes  |  |
 | values | ArrayList<String>? |  yes  |  |
 | include | Boolean? |  yes  |  |
 | sourceField | String? |  yes  |  |
 | sourceFields | ArrayList<String>? |  yes  |  |
 | destinationField | String? |  yes  |  |
 | dataType | String? |  yes  |  |
 | defaultValue | HashMap<String,Any>? |  yes  |  |
 | constValue | HashMap<String,Any>? |  yes  |  |
 | concatStr | String? |  yes  |  |
 | functionName | String? |  yes  |  |
 | transformerName | String? |  yes  |  |
 | allParamFunctionName | String? |  yes  |  |
 | subSeparator | String? |  yes  |  |
 | indexField | String? |  yes  |  |
 | ignoreIfNotExists | Boolean? |  yes  |  |
 | identifierType | String? |  yes  |  |
 | projectionQuery | HashMap<String,HashMap<String,Any>>? |  yes  |  |
 | enrichFromMaster | Boolean? |  yes  |  |

---


 
 
 #### [PropBeanDTO](#PropBeanDTO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | required | Boolean? |  yes  |  |
 | optional | Boolean? |  yes  |  |
 | include | Boolean? |  yes  |  |
 | sourceField | String? |  yes  |  |
 | sourceFields | ArrayList<String>? |  yes  |  |
 | destinationField | String? |  yes  |  |
 | dataType | String? |  yes  |  |
 | defaultValue | HashMap<String,Any>? |  yes  |  |
 | constValue | HashMap<String,Any>? |  yes  |  |
 | concatStr | String? |  yes  |  |
 | functionName | String? |  yes  |  |
 | transformerName | String? |  yes  |  |
 | allParamFunctionName | String? |  yes  |  |
 | subSeparator | String? |  yes  |  |
 | indexField | String? |  yes  |  |
 | ignoreIfNotExists | Boolean? |  yes  |  |
 | identifierType | String? |  yes  |  |
 | projectionQuery | HashMap<String,HashMap<String,Any>>? |  yes  |  |
 | enrichFromMaster | Boolean? |  yes  |  |

---


 
 
 #### [ResponseEnvelopeListJobConfigRawDTO](#ResponseEnvelopeListJobConfigRawDTO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | timestamp | String? |  yes  |  |
 | status | Int? |  yes  |  |
 | error | String? |  yes  |  |
 | exception | String? |  yes  |  |
 | message | String? |  yes  |  |
 | totalTimeTakenInMillis | Int? |  yes  |  |
 | httpStatus | String? |  yes  |  |
 | items | ArrayList<[JobConfigRawDTO](#JobConfigRawDTO)>? |  yes  |  |
 | payload | ArrayList<[JobConfigRawDTO](#JobConfigRawDTO)>? |  yes  |  |
 | traceId | String? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [SFTPConfig](#SFTPConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | host | String? |  yes  |  |
 | port | Int? |  yes  |  |
 | username | String? |  yes  |  |
 | password | String? |  yes  |  |
 | unzip | Boolean? |  yes  |  |
 | retries | Int? |  yes  |  |
 | interval | Int? |  yes  |  |
 | privateKeyPath | String? |  yes  |  |
 | strictHostKeyChecking | Boolean? |  yes  |  |
 | localDir | String? |  yes  |  |
 | remoteDir | String? |  yes  |  |
 | passwordProtected | Boolean? |  yes  |  |
 | zipFileRegex | String? |  yes  |  |
 | fileRegex | String? |  yes  |  |
 | zipFormat | String? |  yes  |  |
 | archiveConfig | [ArchiveConfig](#ArchiveConfig)? |  yes  |  |
 | readAllFiles | Boolean? |  yes  |  |

---


 
 
 #### [Send](#Send)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | raw | Boolean? |  yes  |  |
 | processed | Boolean? |  yes  |  |

---


 
 
 #### [StoreConfig](#StoreConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | jobCode | String? |  yes  |  |
 | storeid | String? |  yes  |  |
 | storeAlias | String? |  yes  |  |
 | storeFileRegex | String? |  yes  |  |
 | storeFileName | String? |  yes  |  |
 | processConfig | [ProcessConfig](#ProcessConfig)? |  yes  |  |
 | properties | HashMap<String,String>? |  yes  |  |

---


 
 
 #### [StoreFilter](#StoreFilter)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | includeTags | ArrayList<String>? |  yes  |  |
 | excludeTags | ArrayList<String>? |  yes  |  |
 | query | HashMap<String,HashMap<String,Any>>? |  yes  |  |

---


 
 
 #### [TaskConfig](#TaskConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | taskConfigId | Int? |  yes  |  |
 | taskParams | ArrayList<[TaskParam](#TaskParam)>? |  yes  |  |

---


 
 
 #### [TaskParam](#TaskParam)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | value | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [TaskStepConfig](#TaskStepConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | taskConfigs | ArrayList<[TaskConfig](#TaskConfig)>? |  yes  |  |
 | taskConfigIds | ArrayList<Int>? |  yes  |  |
 | taskConfigGroupIds | ArrayList<Int>? |  yes  |  |

---


 
 
 #### [ResponseEnvelopeListJobConfigDTO](#ResponseEnvelopeListJobConfigDTO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | timestamp | String? |  yes  |  |
 | status | Int? |  yes  |  |
 | error | String? |  yes  |  |
 | exception | String? |  yes  |  |
 | message | String? |  yes  |  |
 | totalTimeTakenInMillis | Int? |  yes  |  |
 | httpStatus | String? |  yes  |  |
 | items | ArrayList<[JobConfigDTO](#JobConfigDTO)>? |  yes  |  |
 | payload | ArrayList<[JobConfigDTO](#JobConfigDTO)>? |  yes  |  |
 | traceId | String? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [ResponseEnvelopeJobConfigDTO](#ResponseEnvelopeJobConfigDTO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | timestamp | String? |  yes  |  |
 | status | Int? |  yes  |  |
 | error | String? |  yes  |  |
 | exception | String? |  yes  |  |
 | message | String? |  yes  |  |
 | totalTimeTakenInMillis | Int? |  yes  |  |
 | httpStatus | String? |  yes  |  |
 | items | [JobConfigDTO](#JobConfigDTO)? |  yes  |  |
 | payload | [JobConfigDTO](#JobConfigDTO)? |  yes  |  |
 | traceId | String? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [JobHistoryDto](#JobHistoryDto)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | totalAddedCount | Int? |  yes  |  |
 | totalUpdatedCount | Int? |  yes  |  |
 | totalSuppressedCount | Int? |  yes  |  |
 | jobId | Int? |  yes  |  |
 | status | String? |  yes  |  |
 | jobCode | String? |  yes  |  |
 | processedOn | String? |  yes  |  |
 | filename | ArrayList<String>? |  yes  |  |

---


 
 
 #### [JobMetricsDto](#JobMetricsDto)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | jobCode | String? |  yes  |  |
 | isRunMoreThanUsual | String? |  yes  |  |
 | jobHistory | ArrayList<[JobHistoryDto](#JobHistoryDto)>? |  yes  |  |
 | totalSuccessCount | Int? |  yes  |  |
 | totalFailureCount | Int? |  yes  |  |
 | totalWarningCount | Int? |  yes  |  |
 | totalSuppressedCount | Int? |  yes  |  |
 | totalJobRuns | Int? |  yes  |  |

---


 
 
 #### [ResponseEnvelopeJobMetricsDto](#ResponseEnvelopeJobMetricsDto)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | timestamp | String? |  yes  |  |
 | status | Int? |  yes  |  |
 | error | String? |  yes  |  |
 | exception | String? |  yes  |  |
 | message | String? |  yes  |  |
 | totalTimeTakenInMillis | Int? |  yes  |  |
 | httpStatus | String? |  yes  |  |
 | items | [JobMetricsDto](#JobMetricsDto)? |  yes  |  |
 | payload | [JobMetricsDto](#JobMetricsDto)? |  yes  |  |
 | traceId | String? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [JobConfigListDTO](#JobConfigListDTO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | code | String? |  yes  |  |
 | alias | String? |  yes  |  |
 | modifiedBy | String? |  yes  |  |
 | createdBy | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [ResponseEnvelopeListJobConfigListDTO](#ResponseEnvelopeListJobConfigListDTO)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | timestamp | String? |  yes  |  |
 | status | Int? |  yes  |  |
 | error | String? |  yes  |  |
 | exception | String? |  yes  |  |
 | message | String? |  yes  |  |
 | totalTimeTakenInMillis | Int? |  yes  |  |
 | httpStatus | String? |  yes  |  |
 | items | ArrayList<[JobConfigListDTO](#JobConfigListDTO)>? |  yes  |  |
 | payload | ArrayList<[JobConfigListDTO](#JobConfigListDTO)>? |  yes  |  |
 | traceId | String? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---




 
 
 #### [ApplicationInventory](#ApplicationInventory)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | inventory | [AppInventoryConfig](#AppInventoryConfig)? |  yes  |  |
 | authentication | [AuthenticationConfig](#AuthenticationConfig)? |  yes  |  |
 | articleAssignment | [ArticleAssignmentConfig](#ArticleAssignmentConfig)? |  yes  |  |
 | rewardPoints | [RewardPointsConfig](#RewardPointsConfig)? |  yes  |  |
 | cart | [AppCartConfig](#AppCartConfig)? |  yes  |  |
 | payment | [AppPaymentConfig](#AppPaymentConfig)? |  yes  |  |
 | order | [AppOrderConfig](#AppOrderConfig)? |  yes  |  |
 | logistics | [AppLogisticsConfig](#AppLogisticsConfig)? |  yes  |  |
 | business | String? |  yes  |  |
 | commsEnabled | Boolean? |  yes  |  |
 | platforms | ArrayList<String>? |  yes  |  |
 | id | String? |  yes  |  |
 | loyaltyPoints | [LoyaltyPointsConfig](#LoyaltyPointsConfig)? |  yes  |  |
 | app | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | modifiedBy | String? |  yes  |  |

---


 
 
 #### [AppInventoryConfig](#AppInventoryConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brand | [InventoryBrand](#InventoryBrand)? |  yes  |  |
 | store | [InventoryStore](#InventoryStore)? |  yes  |  |
 | category | [InventoryCategory](#InventoryCategory)? |  yes  |  |
 | price | [InventoryPrice](#InventoryPrice)? |  yes  |  |
 | discount | [InventoryDiscount](#InventoryDiscount)? |  yes  |  |
 | outOfStock | Boolean? |  yes  |  |
 | franchiseEnabled | Boolean? |  yes  |  |
 | excludeCategory | ArrayList<Any>? |  yes  |  |
 | image | ArrayList<String>? |  yes  |  |
 | companyStore | ArrayList<Any>? |  yes  |  |

---


 
 
 #### [InventoryBrand](#InventoryBrand)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | criteria | String? |  yes  |  |
 | brands | ArrayList<Any>? |  yes  |  |

---


 
 
 #### [InventoryStore](#InventoryStore)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | criteria | String? |  yes  |  |
 | stores | ArrayList<Any>? |  yes  |  |
 | rules | [AppStoreRules](#AppStoreRules)? |  yes  |  |

---


 
 
 #### [AppStoreRules](#AppStoreRules)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companies | ArrayList<Int>? |  yes  |  |
 | brands | ArrayList<Any>? |  yes  |  |

---


 
 
 #### [InventoryCategory](#InventoryCategory)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | criteria | String? |  yes  |  |
 | categories | ArrayList<Any>? |  yes  |  |

---


 
 
 #### [InventoryPrice](#InventoryPrice)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | min | Double? |  yes  |  |
 | max | Double? |  yes  |  |

---


 
 
 #### [InventoryDiscount](#InventoryDiscount)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | min | Double? |  yes  |  |
 | max | Double? |  yes  |  |

---


 
 
 #### [AuthenticationConfig](#AuthenticationConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | required | Boolean? |  yes  |  |
 | provider | String? |  yes  |  |

---


 
 
 #### [ArticleAssignmentConfig](#ArticleAssignmentConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | rules | [ArticleAssignmentRules](#ArticleAssignmentRules)? |  yes  |  |
 | postOrderReassignment | Boolean? |  yes  |  |

---


 
 
 #### [ArticleAssignmentRules](#ArticleAssignmentRules)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | storePriority | [StorePriority](#StorePriority)? |  yes  |  |

---


 
 
 #### [StorePriority](#StorePriority)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |
 | storetypeOrder | ArrayList<Any>? |  yes  |  |

---


 
 
 #### [AppCartConfig](#AppCartConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | deliveryCharges | [DeliveryCharges](#DeliveryCharges)? |  yes  |  |
 | enabled | Boolean? |  yes  |  |
 | maxCartItems | Int? |  yes  |  |
 | minCartValue | Double? |  yes  |  |
 | bulkCoupons | Boolean? |  yes  |  |

---


 
 
 #### [DeliveryCharges](#DeliveryCharges)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |
 | charges | [Charges](#Charges)? |  yes  |  |

---


 
 
 #### [Charges](#Charges)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | threshold | Double? |  yes  |  |
 | charges | Double? |  yes  |  |

---


 
 
 #### [AppPaymentConfig](#AppPaymentConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | callbackUrl | [CallbackUrl](#CallbackUrl)? |  yes  |  |
 | methods | [Methods](#Methods)? |  yes  |  |
 | paymentSelectionLock | [PaymentSelectionLock](#PaymentSelectionLock)? |  yes  |  |
 | modeOfPayment | String? |  yes  |  |
 | source | String? |  yes  |  |
 | enabled | Boolean? |  yes  |  |
 | codAmountLimit | Double? |  yes  |  |
 | codCharges | Double? |  yes  |  |

---


 
 
 #### [CallbackUrl](#CallbackUrl)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | app | String? |  yes  |  |
 | web | String? |  yes  |  |

---


 
 
 #### [Methods](#Methods)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pl | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | card | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | nb | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | wl | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | ps | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | upi | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | qr | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | cod | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | pp | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | jp | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | pac | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | fc | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | jiopp | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | stripepg | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | juspaypg | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | payubizpg | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | payumoneypg | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | rupifipg | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |
 | simpl | [PaymentModeConfig](#PaymentModeConfig)? |  yes  |  |

---


 
 
 #### [PaymentModeConfig](#PaymentModeConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [PaymentSelectionLock](#PaymentSelectionLock)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |
 | defaultOptions | String? |  yes  |  |
 | paymentIdentifier | String? |  yes  |  |

---


 
 
 #### [AppOrderConfig](#AppOrderConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |
 | forceReassignment | Boolean? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [AppLogisticsConfig](#AppLogisticsConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | logisticsBySeller | Boolean? |  yes  |  |
 | serviceabilityCheck | Boolean? |  yes  |  |
 | sameDayDelivery | Boolean? |  yes  |  |
 | dpAssignment | Boolean? |  yes  |  |

---


 
 
 #### [LoyaltyPointsConfig](#LoyaltyPointsConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |
 | autoApply | Boolean? |  yes  |  |

---


 
 
 #### [AppInventoryPartialUpdate](#AppInventoryPartialUpdate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | rewardPoints | [RewardPointsConfig](#RewardPointsConfig)? |  yes  |  |
 | cart | [AppCartConfig](#AppCartConfig)? |  yes  |  |
 | payment | [AppPaymentConfig](#AppPaymentConfig)? |  yes  |  |
 | loyaltyPoints | [LoyaltyPointsConfig](#LoyaltyPointsConfig)? |  yes  |  |
 | commsEnabled | Boolean? |  yes  |  |

---


 
 
 #### [BrandCompanyInfo](#BrandCompanyInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companyName | String? |  yes  |  |
 | companyId | Int? |  yes  |  |

---


 
 
 #### [CompanyByBrandsRequest](#CompanyByBrandsRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brands | Int |  no  | Brand uids |
 | searchText | String? |  yes  | Search company by name |

---


 
 
 #### [CompanyByBrandsResponse](#CompanyByBrandsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[BrandCompanyInfo](#BrandCompanyInfo)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [StoreByBrandsRequest](#StoreByBrandsRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companyId | Int? |  yes  | Current company id for current company stores only. Don't send in case of cross selling enabled |
 | brands | Int |  no  | Brand uids |
 | searchText | String? |  yes  | Search store by name or store code |

---


 
 
 #### [StoreByBrandsResponse](#StoreByBrandsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[BrandStoreInfo](#BrandStoreInfo)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [BrandStoreInfo](#BrandStoreInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | storeName | String? |  yes  |  |
 | storeId | Int? |  yes  |  |
 | storeType | String? |  yes  |  |
 | storeCode | String? |  yes  |  |
 | storeAddress | [OptedStoreAddress](#OptedStoreAddress)? |  yes  |  |
 | company | [OptedCompany](#OptedCompany)? |  yes  |  |

---


 
 
 #### [CompanyBrandInfo](#CompanyBrandInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | value | Int? |  yes  |  |
 | brandLogoUrl | String? |  yes  |  |
 | brandBannerUrl | String? |  yes  |  |
 | brandBannerPortraitUrl | String? |  yes  |  |

---


 
 
 #### [BrandsByCompanyResponse](#BrandsByCompanyResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brands | [CompanyBrandInfo](#CompanyBrandInfo)? |  yes  |  |

---


 
 
 #### [CreateApplicationRequest](#CreateApplicationRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | app | [App](#App)? |  yes  |  |
 | configuration | [AppInventory](#AppInventory)? |  yes  |  |
 | domain | [AppDomain](#AppDomain)? |  yes  |  |

---


 
 
 #### [CreateAppResponse](#CreateAppResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | app | [Application](#Application)? |  yes  |  |
 | configuration | [ApplicationInventory](#ApplicationInventory)? |  yes  |  |

---


 
 
 #### [ApplicationsResponse](#ApplicationsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Application](#Application)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [MobileAppConfiguration](#MobileAppConfiguration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isActive | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | appName | String? |  yes  |  |
 | landingImage | [LandingImage](#LandingImage)? |  yes  |  |
 | splashImage | [SplashImage](#SplashImage)? |  yes  |  |
 | application | String? |  yes  |  |
 | platformType | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |
 | packageName | String? |  yes  |  |

---


 
 
 #### [LandingImage](#LandingImage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | aspectRatio | String? |  yes  |  |
 | secureUrl | String? |  yes  |  |

---


 
 
 #### [SplashImage](#SplashImage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | aspectRatio | String? |  yes  |  |
 | secureUrl | String? |  yes  |  |

---


 
 
 #### [MobileAppConfigRequest](#MobileAppConfigRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | appName | String? |  yes  |  |
 | landingImage | [LandingImage](#LandingImage)? |  yes  |  |
 | splashImage | [SplashImage](#SplashImage)? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [BuildVersionHistory](#BuildVersionHistory)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | versions | [BuildVersion](#BuildVersion)? |  yes  |  |
 | latestAvailableVersionName | String? |  yes  |  |

---


 
 
 #### [BuildVersion](#BuildVersion)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | application | String? |  yes  |  |
 | platformType | String? |  yes  |  |
 | buildStatus | String? |  yes  |  |
 | versionName | String? |  yes  |  |
 | versionCode | Int? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [AppSupportedCurrency](#AppSupportedCurrency)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | supportedCurrency | ArrayList<String>? |  yes  |  |
 | application | String? |  yes  |  |
 | defaultCurrency | [DefaultCurrency](#DefaultCurrency)? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |

---


 
 
 #### [DefaultCurrency](#DefaultCurrency)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ref | String? |  yes  |  |
 | code | String? |  yes  |  |

---


 
 
 #### [CurrencyConfig](#CurrencyConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | code | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | decimalDigits | Int? |  yes  |  |
 | symbol | String? |  yes  |  |

---


 
 
 #### [DomainAdd](#DomainAdd)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  | Full domain name |

---


 
 
 #### [DomainAddRequest](#DomainAddRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | domain | [DomainAdd](#DomainAdd)? |  yes  |  |

---


 
 
 #### [DomainsResponse](#DomainsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | domains | ArrayList<[Domain](#Domain)>? |  yes  |  |

---


 
 
 #### [UpdateDomain](#UpdateDomain)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |

---


 
 
 #### [UpdateDomainTypeRequest](#UpdateDomainTypeRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | domain | [UpdateDomain](#UpdateDomain)? |  yes  |  |
 | action | String? |  yes  |  |

---


 
 
 #### [DomainStatusRequest](#DomainStatusRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | domainUrl | String? |  yes  | Domain url |

---


 
 
 #### [DomainStatus](#DomainStatus)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | status | Boolean? |  yes  |  |

---


 
 
 #### [DomainStatusResponse](#DomainStatusResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | connected | Boolean? |  yes  |  |
 | status | ArrayList<[DomainStatus](#DomainStatus)>? |  yes  |  |

---


 
 
 #### [DomainSuggestionsRequest](#DomainSuggestionsRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | domainUrl | String? |  yes  | Domain url |
 | custom | Boolean? |  yes  | Get suggestion for custom domains or fynd domains |

---


 
 
 #### [DomainSuggestion](#DomainSuggestion)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | unsupported | Boolean? |  yes  | Whether TLD domain is supported or not |
 | isAvailable | Boolean |  no  |  |
 | price | Double? |  yes  | Price for purchasing a custom domain. Not present for fynd domain |
 | currency | String? |  yes  | Custom domain price currency. Not present for fynd domain |

---


 
 
 #### [DomainSuggestionsResponse](#DomainSuggestionsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | domains | ArrayList<[DomainSuggestion](#DomainSuggestion)>? |  yes  | Domain url |

---


 
 
 #### [GetIntegrationsOptInsResponse](#GetIntegrationsOptInsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | [IntegrationOptIn](#IntegrationOptIn)? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [IntegrationOptIn](#IntegrationOptIn)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | validators | [Validators](#Validators)? |  yes  |  |
 | description | String? |  yes  |  |
 | descriptionHtml | String? |  yes  |  |
 | constants | String? |  yes  |  |
 | companies | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | support | ArrayList<String>? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | meta | [IntegrationMeta](#IntegrationMeta)? |  yes  |  |
 | icon | String? |  yes  |  |
 | owner | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | token | String? |  yes  |  |
 | secret | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [Validators](#Validators)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | company | [CompanyValidator](#CompanyValidator)? |  yes  |  |
 | store | [StoreValidator](#StoreValidator)? |  yes  |  |
 | inventory | [InventoryValidator](#InventoryValidator)? |  yes  |  |
 | order | [OrderValidator](#OrderValidator)? |  yes  |  |

---


 
 
 #### [CompanyValidator](#CompanyValidator)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | jsonSchema | [JsonSchema](#JsonSchema)? |  yes  |  |
 | browserScript | String? |  yes  |  |

---


 
 
 #### [JsonSchema](#JsonSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | key | String? |  yes  |  |
 | type | String? |  yes  |  |
 | tooltip | String? |  yes  |  |

---


 
 
 #### [StoreValidator](#StoreValidator)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | jsonSchema | ArrayList<[JsonSchema](#JsonSchema)>? |  yes  |  |
 | browserScript | String? |  yes  |  |

---


 
 
 #### [InventoryValidator](#InventoryValidator)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | jsonSchema | ArrayList<[JsonSchema](#JsonSchema)>? |  yes  |  |
 | browserScript | String? |  yes  |  |

---


 
 
 #### [OrderValidator](#OrderValidator)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | jsonSchema | ArrayList<[JsonSchema](#JsonSchema)>? |  yes  |  |
 | browserScript | String? |  yes  |  |

---


 
 
 #### [IntegrationMeta](#IntegrationMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isPublic | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [Integration](#Integration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | validators | [Validators](#Validators)? |  yes  |  |
 | description | String? |  yes  |  |
 | descriptionHtml | String? |  yes  |  |
 | constants | HashMap<String,Any>? |  yes  |  |
 | companies | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | support | ArrayList<String>? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | meta | [IntegrationMeta](#IntegrationMeta)? |  yes  |  |
 | icon | String? |  yes  |  |
 | owner | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | token | String? |  yes  |  |
 | secret | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [IntegrationConfigResponse](#IntegrationConfigResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | [IntegrationLevel](#IntegrationLevel)? |  yes  |  |

---


 
 
 #### [IntegrationLevel](#IntegrationLevel)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | opted | Boolean? |  yes  |  |
 | permissions | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | lastPatch | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | id | String? |  yes  |  |
 | integration | String? |  yes  |  |
 | level | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | meta | ArrayList<Any>? |  yes  |  |
 | token | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |
 | data | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [OptedStoreIntegration](#OptedStoreIntegration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | otherOpted | Boolean? |  yes  |  |
 | otherIntegration | [IntegrationOptIn](#IntegrationOptIn)? |  yes  |  |
 | otherEntity | [OtherEntity](#OtherEntity)? |  yes  |  |

---


 
 
 #### [OtherEntity](#OtherEntity)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | opted | Boolean? |  yes  |  |
 | permissions | ArrayList<String>? |  yes  |  |
 | lastPatch | [LastPatch](#LastPatch)? |  yes  |  |
 | id | String? |  yes  |  |
 | integration | String? |  yes  |  |
 | level | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | data | [OtherEntityData](#OtherEntityData)? |  yes  |  |
 | meta | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | token | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [LastPatch](#LastPatch)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | op | String? |  yes  |  |
 | path | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [OtherEntityData](#OtherEntityData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | articleIdentifier | String? |  yes  |  |

---


 
 
 #### [App](#App)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companyId | String? |  yes  | Current company id |
 | channelType | String? |  yes  |  |
 | auth | [ApplicationAuth](#ApplicationAuth)? |  yes  |  |
 | name | String? |  yes  | User friendly name for application |
 | desc | String? |  yes  | Basic description of application |

---


 
 
 #### [AppInventory](#AppInventory)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brand | [InventoryBrandRule](#InventoryBrandRule)? |  yes  |  |
 | store | [InventoryStoreRule](#InventoryStoreRule)? |  yes  |  |
 | image | ArrayList<String>? |  yes  |  |
 | franchiseEnabled | Boolean? |  yes  |  |
 | outOfStock | Boolean? |  yes  |  |
 | payment | [InventoryPaymentConfig](#InventoryPaymentConfig)? |  yes  |  |
 | articleAssignment | [InventoryArticleAssignment](#InventoryArticleAssignment)? |  yes  |  |

---


 
 
 #### [AppDomain](#AppDomain)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |

---


 
 
 #### [CompaniesResponse](#CompaniesResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | [AppInventoryCompanies](#AppInventoryCompanies)? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [AppInventoryCompanies](#AppInventoryCompanies)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | companyType | String? |  yes  |  |

---


 
 
 #### [StoresResponse](#StoresResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | [AppInventoryStores](#AppInventoryStores)? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [AppInventoryStores](#AppInventoryStores)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | displayName | String? |  yes  |  |
 | storeType | String? |  yes  |  |
 | storeCode | String? |  yes  |  |
 | companyId | Int? |  yes  |  |

---


 
 
 #### [FilterOrderingStoreRequest](#FilterOrderingStoreRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | allStores | Boolean? |  yes  |  |
 | deployedStores | ArrayList<Int>? |  yes  |  |
 | q | String? |  yes  |  |

---


 
 
 #### [DeploymentMeta](#DeploymentMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | deployedStores | ArrayList<Int>? |  yes  |  |
 | allStores | Boolean? |  yes  |  |
 | enabled | Boolean? |  yes  |  |
 | type | String? |  yes  |  |
 | id | String? |  yes  |  |
 | app | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [OrderingStoreConfig](#OrderingStoreConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | deploymentMeta | [DeploymentMeta](#DeploymentMeta)? |  yes  |  |

---


 
 
 #### [OtherSellerCompany](#OtherSellerCompany)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [OtherSellerApplication](#OtherSellerApplication)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | id | String? |  yes  |  |
 | domain | String? |  yes  |  |
 | company | [OtherSellerCompany](#OtherSellerCompany)? |  yes  |  |
 | optType | String? |  yes  |  |

---


 
 
 #### [OtherSellerApplications](#OtherSellerApplications)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[OtherSellerApplication](#OtherSellerApplication)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [OptedApplicationResponse](#OptedApplicationResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | id | String? |  yes  |  |
 | domain | String? |  yes  |  |
 | company | [OptedCompany](#OptedCompany)? |  yes  |  |
 | optedInventory | [OptedInventory](#OptedInventory)? |  yes  |  |
 | optOutInventory | [OptOutInventory](#OptOutInventory)? |  yes  |  |

---


 
 
 #### [OptedCompany](#OptedCompany)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [OptedInventory](#OptedInventory)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | optType | [OptType](#OptType)? |  yes  |  |
 | items | Any? |  yes  |  |

---


 
 
 #### [OptType](#OptType)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String? |  yes  |  |
 | display | String? |  yes  |  |

---


 
 
 #### [OptedStore](#OptedStore)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | storeCode | String? |  yes  |  |
 | id | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | address | [OptedStoreAddress](#OptedStoreAddress)? |  yes  |  |
 | displayName | String? |  yes  |  |
 | storeType | String? |  yes  |  |
 | companyId | Int? |  yes  |  |

---


 
 
 #### [OptOutInventory](#OptOutInventory)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | store | ArrayList<Int> |  no  |  |
 | company | ArrayList<Int> |  no  |  |

---


 
 
 #### [TokenResponse](#TokenResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tokens | [Tokens](#Tokens)? |  yes  |  |
 | id | String? |  yes  |  |
 | application | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [Tokens](#Tokens)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | firebase | [Firebase](#Firebase)? |  yes  |  |
 | moengage | [Moengage](#Moengage)? |  yes  |  |
 | segment | [Segment](#Segment)? |  yes  |  |
 | gtm | [Gtm](#Gtm)? |  yes  |  |
 | freshchat | [Freshchat](#Freshchat)? |  yes  |  |
 | safetynet | [Safetynet](#Safetynet)? |  yes  |  |
 | fyndRewards | [FyndRewards](#FyndRewards)? |  yes  |  |
 | googleMap | [GoogleMap](#GoogleMap)? |  yes  |  |

---


 
 
 #### [Firebase](#Firebase)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | credentials | [Credentials](#Credentials)? |  yes  |  |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [Credentials](#Credentials)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ios | [Ios](#Ios)? |  yes  |  |
 | android | [Android](#Android)? |  yes  |  |
 | projectId | String? |  yes  |  |
 | gcmSenderId | String? |  yes  |  |
 | applicationId | String? |  yes  |  |
 | apiKey | String? |  yes  |  |

---


 
 
 #### [Ios](#Ios)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | applicationId | String? |  yes  |  |
 | apiKey | String? |  yes  |  |

---


 
 
 #### [Android](#Android)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | applicationId | String? |  yes  |  |
 | apiKey | String? |  yes  |  |

---


 
 
 #### [Moengage](#Moengage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | credentials | [MoengageCredentials](#MoengageCredentials)? |  yes  |  |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [MoengageCredentials](#MoengageCredentials)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | appId | String? |  yes  |  |

---


 
 
 #### [Segment](#Segment)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | credentials | [SegmentCredentials](#SegmentCredentials)? |  yes  |  |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [SegmentCredentials](#SegmentCredentials)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | writeKey | String? |  yes  |  |

---


 
 
 #### [Gtm](#Gtm)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | credentials | [GtmCredentials](#GtmCredentials)? |  yes  |  |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [GtmCredentials](#GtmCredentials)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | apiKey | String? |  yes  |  |

---


 
 
 #### [Freshchat](#Freshchat)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | credentials | [FreshchatCredentials](#FreshchatCredentials)? |  yes  |  |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [FreshchatCredentials](#FreshchatCredentials)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | appId | String? |  yes  |  |
 | appKey | String? |  yes  |  |
 | webToken | String? |  yes  |  |

---


 
 
 #### [Safetynet](#Safetynet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | credentials | [SafetynetCredentials](#SafetynetCredentials)? |  yes  |  |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [SafetynetCredentials](#SafetynetCredentials)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | apiKey | String? |  yes  |  |

---


 
 
 #### [FyndRewards](#FyndRewards)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | credentials | [FyndRewardsCredentials](#FyndRewardsCredentials)? |  yes  |  |

---


 
 
 #### [FyndRewardsCredentials](#FyndRewardsCredentials)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | publicKey | String? |  yes  |  |

---


 
 
 #### [GoogleMap](#GoogleMap)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | credentials | [GoogleMapCredentials](#GoogleMapCredentials)? |  yes  |  |

---


 
 
 #### [GoogleMapCredentials](#GoogleMapCredentials)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | apiKey | String? |  yes  |  |

---


 
 
 #### [RewardPointsConfig](#RewardPointsConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | credit | [Credit](#Credit)? |  yes  |  |
 | debit | [Debit](#Debit)? |  yes  |  |

---


 
 
 #### [Credit](#Credit)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [Debit](#Debit)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |
 | autoApply | Boolean? |  yes  |  |
 | strategyChannel | String? |  yes  |  |

---


 
 
 #### [ProductDetailFeature](#ProductDetailFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | similar | ArrayList<String>? |  yes  |  |
 | sellerSelection | Boolean? |  yes  |  |
 | updateProductMeta | Boolean? |  yes  |  |
 | requestProduct | Boolean? |  yes  |  |

---


 
 
 #### [LaunchPage](#LaunchPage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pageType | String? |  yes  |  |
 | params | HashMap<String,Any>? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [LandingPageFeature](#LandingPageFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | launchPage | [LaunchPage](#LaunchPage)? |  yes  |  |
 | continueAsGuest | Boolean? |  yes  |  |
 | loginBtnText | String? |  yes  |  |
 | showDomainTextbox | Boolean? |  yes  |  |
 | showRegisterBtn | Boolean? |  yes  |  |

---


 
 
 #### [RegistrationPageFeature](#RegistrationPageFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | askStoreAddress | Boolean? |  yes  |  |

---


 
 
 #### [AppFeature](#AppFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | productDetail | [ProductDetailFeature](#ProductDetailFeature)? |  yes  |  |
 | landingPage | [LandingPageFeature](#LandingPageFeature)? |  yes  |  |
 | registrationPage | [RegistrationPageFeature](#RegistrationPageFeature)? |  yes  |  |
 | homePage | [HomePageFeature](#HomePageFeature)? |  yes  |  |
 | common | [CommonFeature](#CommonFeature)? |  yes  |  |
 | cart | [CartFeature](#CartFeature)? |  yes  |  |
 | qr | [QrFeature](#QrFeature)? |  yes  |  |
 | pcr | [PcrFeature](#PcrFeature)? |  yes  |  |
 | order | [OrderFeature](#OrderFeature)? |  yes  |  |
 | id | String? |  yes  |  |
 | app | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [HomePageFeature](#HomePageFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | orderProcessing | Boolean? |  yes  |  |

---


 
 
 #### [CommonFeature](#CommonFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | communicationOptinDialog | [CommunicationOptinDialogFeature](#CommunicationOptinDialogFeature)? |  yes  |  |
 | deploymentStoreSelection | [DeploymentStoreSelectionFeature](#DeploymentStoreSelectionFeature)? |  yes  |  |
 | listingPrice | [ListingPriceFeature](#ListingPriceFeature)? |  yes  |  |
 | currency | [CurrencyFeature](#CurrencyFeature)? |  yes  |  |
 | revenueEngine | [RevenueEngineFeature](#RevenueEngineFeature)? |  yes  |  |
 | feedback | [FeedbackFeature](#FeedbackFeature)? |  yes  |  |
 | compareProducts | [CompareProductsFeature](#CompareProductsFeature)? |  yes  |  |
 | rewardPoints | [RewardPointsConfig](#RewardPointsConfig)? |  yes  |  |

---


 
 
 #### [CommunicationOptinDialogFeature](#CommunicationOptinDialogFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | visibility | Boolean? |  yes  |  |

---


 
 
 #### [DeploymentStoreSelectionFeature](#DeploymentStoreSelectionFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [ListingPriceFeature](#ListingPriceFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | String? |  yes  |  |

---


 
 
 #### [CurrencyFeature](#CurrencyFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | ArrayList<String>? |  yes  |  |
 | type | String? |  yes  |  |
 | defaultCurrency | String? |  yes  |  |

---


 
 
 #### [RevenueEngineFeature](#RevenueEngineFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [FeedbackFeature](#FeedbackFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [CompareProductsFeature](#CompareProductsFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [CartFeature](#CartFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | gstInput | Boolean? |  yes  |  |
 | staffSelection | Boolean? |  yes  |  |
 | placingForCustomer | Boolean? |  yes  |  |
 | googleMap | Boolean? |  yes  |  |
 | revenueEngineCoupon | Boolean? |  yes  |  |

---


 
 
 #### [QrFeature](#QrFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | application | Boolean? |  yes  |  |
 | products | Boolean? |  yes  |  |
 | collections | Boolean? |  yes  |  |

---


 
 
 #### [PcrFeature](#PcrFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | staffSelection | Boolean? |  yes  |  |

---


 
 
 #### [OrderFeature](#OrderFeature)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | buyAgain | Boolean? |  yes  |  |

---


 
 
 #### [AppFeatureRequest](#AppFeatureRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | feature | [AppFeature](#AppFeature)? |  yes  |  |

---


 
 
 #### [AppFeatureResponse](#AppFeatureResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | feature | [AppFeature](#AppFeature)? |  yes  |  |

---


 
 
 #### [Currency](#Currency)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | code | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | decimalDigits | Int? |  yes  |  |
 | symbol | String? |  yes  |  |

---


 
 
 #### [Domain](#Domain)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | verified | Boolean? |  yes  |  |
 | isPrimary | Boolean? |  yes  |  |
 | isShortlink | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [ApplicationWebsite](#ApplicationWebsite)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |
 | basepath | String? |  yes  |  |

---


 
 
 #### [ApplicationCors](#ApplicationCors)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | domains | ArrayList<String>? |  yes  |  |

---


 
 
 #### [ApplicationAuth](#ApplicationAuth)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |

---


 
 
 #### [ApplicationRedirections](#ApplicationRedirections)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | from | String? |  yes  |  |
 | redirectTo | String? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [ApplicationMeta](#ApplicationMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [SecureUrl](#SecureUrl)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | secureUrl | String? |  yes  |  |

---


 
 
 #### [Application](#Application)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | website | [ApplicationWebsite](#ApplicationWebsite)? |  yes  |  |
 | cors | [ApplicationCors](#ApplicationCors)? |  yes  |  |
 | auth | [ApplicationAuth](#ApplicationAuth)? |  yes  |  |
 | description | String? |  yes  |  |
 | channelType | String? |  yes  |  |
 | cacheTtl | Int? |  yes  |  |
 | isInternal | Boolean? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | owner | String? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | token | String? |  yes  |  |
 | redirections | ArrayList<[ApplicationRedirections](#ApplicationRedirections)>? |  yes  |  |
 | meta | ArrayList<[ApplicationMeta](#ApplicationMeta)>? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |
 | banner | [SecureUrl](#SecureUrl)? |  yes  |  |
 | logo | [SecureUrl](#SecureUrl)? |  yes  |  |
 | favicon | [SecureUrl](#SecureUrl)? |  yes  |  |
 | domains | ArrayList<[Domain](#Domain)>? |  yes  |  |
 | appType | String? |  yes  |  |
 | mobileLogo | [SecureUrl](#SecureUrl)? |  yes  |  |
 | domain | [Domain](#Domain)? |  yes  |  |

---


 
 
 #### [NotFound](#NotFound)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [UnhandledError](#UnhandledError)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [InvalidPayloadRequest](#InvalidPayloadRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [SuccessMessageResponse](#SuccessMessageResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [InventoryBrandRule](#InventoryBrandRule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | criteria | String? |  yes  | Whether enable all or explicitly few brands as inventory |
 | brands | ArrayList<Int>? |  yes  | Brand uids in case of explicit criteria |

---


 
 
 #### [StoreCriteriaRule](#StoreCriteriaRule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companies | ArrayList<Int>? |  yes  | list of company uids |
 | brands | ArrayList<Int>? |  yes  | list of brand uids |

---


 
 
 #### [InventoryStoreRule](#InventoryStoreRule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | criteria | String? |  yes  | Whether enable all or explicitly few stores or use filter of brands and company as inventory stores |
 | rules | ArrayList<[StoreCriteriaRule](#StoreCriteriaRule)>? |  yes  | List of rules with company and brands uids. Used when critera is `filter` |
 | stores | ArrayList<Int>? |  yes  | List of store uids. Used when critera is `explicit` |

---


 
 
 #### [InventoryPaymentConfig](#InventoryPaymentConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | modeOfPayment | String? |  yes  |  |
 | source | String? |  yes  |  |

---


 
 
 #### [StorePriorityRule](#StorePriorityRule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | enabled | Boolean? |  yes  |  |
 | storetypeOrder | ArrayList<String>? |  yes  |  |

---


 
 
 #### [ArticleAssignmentRule](#ArticleAssignmentRule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | storePriority | [StorePriorityRule](#StorePriorityRule)? |  yes  |  |

---


 
 
 #### [InventoryArticleAssignment](#InventoryArticleAssignment)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | postOrderReassignment | Boolean? |  yes  |  |
 | rules | [ArticleAssignmentRule](#ArticleAssignmentRule)? |  yes  |  |

---


 
 
 #### [CompanyAboutAddress](#CompanyAboutAddress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pincode | Int? |  yes  |  |
 | address1 | String? |  yes  |  |
 | address2 | String? |  yes  |  |
 | city | String? |  yes  |  |
 | state | String? |  yes  |  |
 | country | String? |  yes  |  |
 | addressType | String? |  yes  |  |

---


 
 
 #### [UserEmail](#UserEmail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  |  |
 | primary | Boolean? |  yes  |  |
 | verified | Boolean? |  yes  |  |
 | email | String? |  yes  |  |

---


 
 
 #### [UserPhoneNumber](#UserPhoneNumber)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  |  |
 | primary | Boolean? |  yes  |  |
 | verified | Boolean? |  yes  |  |
 | countryCode | Int? |  yes  |  |
 | phone | String? |  yes  |  |

---


 
 
 #### [ApplicationInformation](#ApplicationInformation)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | address | [InformationAddress](#InformationAddress)? |  yes  |  |
 | support | [InformationSupport](#InformationSupport)? |  yes  |  |
 | socialLinks | [SocialLinks](#SocialLinks)? |  yes  |  |
 | links | [Links](#Links)? |  yes  |  |
 | copyrightText | String? |  yes  |  |
 | id | String? |  yes  |  |
 | businessHighlights | [BusinessHighlights](#BusinessHighlights)? |  yes  |  |
 | application | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | v | Int? |  yes  |  |

---


 
 
 #### [InformationAddress](#InformationAddress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | loc | String? |  yes  |  |
 | addressLine | ArrayList<String>? |  yes  |  |
 | phone | [InformationPhone](#InformationPhone)? |  yes  |  |
 | city | String? |  yes  |  |
 | country | String? |  yes  |  |
 | pincode | Int? |  yes  |  |

---


 
 
 #### [InformationPhone](#InformationPhone)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | code | String? |  yes  |  |
 | number | String? |  yes  |  |

---


 
 
 #### [InformationSupport](#InformationSupport)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | phone | ArrayList<String>? |  yes  |  |
 | email | ArrayList<String>? |  yes  |  |
 | timing | String? |  yes  |  |

---


 
 
 #### [SocialLinks](#SocialLinks)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | facebook | [FacebookLink](#FacebookLink)? |  yes  |  |
 | instagram | [InstagramLink](#InstagramLink)? |  yes  |  |
 | twitter | [TwitterLink](#TwitterLink)? |  yes  |  |
 | pinterest | [PinterestLink](#PinterestLink)? |  yes  |  |
 | googlePlus | [GooglePlusLink](#GooglePlusLink)? |  yes  |  |
 | youtube | [YoutubeLink](#YoutubeLink)? |  yes  |  |
 | linkedIn | [LinkedInLink](#LinkedInLink)? |  yes  |  |
 | vimeo | [VimeoLink](#VimeoLink)? |  yes  |  |
 | blogLink | [BlogLink](#BlogLink)? |  yes  |  |

---


 
 
 #### [FacebookLink](#FacebookLink)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | icon | String? |  yes  |  |
 | link | String? |  yes  |  |

---


 
 
 #### [InstagramLink](#InstagramLink)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | icon | String? |  yes  |  |
 | link | String? |  yes  |  |

---


 
 
 #### [TwitterLink](#TwitterLink)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | icon | String? |  yes  |  |
 | link | String? |  yes  |  |

---


 
 
 #### [PinterestLink](#PinterestLink)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | icon | String? |  yes  |  |
 | link | String? |  yes  |  |

---


 
 
 #### [GooglePlusLink](#GooglePlusLink)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | icon | String? |  yes  |  |
 | link | String? |  yes  |  |

---


 
 
 #### [YoutubeLink](#YoutubeLink)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | icon | String? |  yes  |  |
 | link | String? |  yes  |  |

---


 
 
 #### [LinkedInLink](#LinkedInLink)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | icon | String? |  yes  |  |
 | link | String? |  yes  |  |

---


 
 
 #### [VimeoLink](#VimeoLink)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | icon | String? |  yes  |  |
 | link | String? |  yes  |  |

---


 
 
 #### [BlogLink](#BlogLink)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | icon | String? |  yes  |  |
 | link | String? |  yes  |  |

---


 
 
 #### [Links](#Links)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | link | String? |  yes  |  |

---


 
 
 #### [BusinessHighlights](#BusinessHighlights)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | title | String? |  yes  |  |
 | icon | String? |  yes  |  |
 | subTitle | String? |  yes  |  |

---


 
 
 #### [ApplicationDetail](#ApplicationDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | description | String |  no  |  |
 | logo | [SecureUrl](#SecureUrl) |  no  |  |
 | mobileLogo | [SecureUrl](#SecureUrl) |  no  |  |
 | favicon | [SecureUrl](#SecureUrl) |  no  |  |
 | banner | [SecureUrl](#SecureUrl) |  no  |  |
 | domain | [Domain](#Domain)? |  yes  |  |
 | domains | ArrayList<[Domain](#Domain)>? |  yes  |  |
 | id | String? |  yes  |  |

---


 
 
 #### [CurrenciesResponse](#CurrenciesResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Currency](#Currency)>? |  yes  |  |

---


 
 
 #### [AppCurrencyResponse](#AppCurrencyResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | application | String? |  yes  |  |
 | defaultCurrency | [DefaultCurrency](#DefaultCurrency)? |  yes  |  |
 | supportedCurrency | ArrayList<[Currency](#Currency)>? |  yes  |  |

---


 
 
 #### [StoreLatLong](#StoreLatLong)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | coordinates | ArrayList<Double>? |  yes  |  |

---


 
 
 #### [OptedStoreAddress](#OptedStoreAddress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | state | String? |  yes  |  |
 | address1 | String? |  yes  |  |
 | latLong | [StoreLatLong](#StoreLatLong)? |  yes  |  |
 | address2 | String? |  yes  |  |
 | pincode | Int? |  yes  |  |
 | country | String? |  yes  |  |
 | city | String? |  yes  |  |

---


 
 
 #### [OrderingStore](#OrderingStore)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | address | [OptedStoreAddress](#OptedStoreAddress)? |  yes  |  |
 | id | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | displayName | String? |  yes  |  |
 | storeType | String? |  yes  |  |
 | storeCode | String? |  yes  |  |
 | pincode | Int? |  yes  |  |
 | code | String? |  yes  |  |

---


 
 
 #### [OrderingStores](#OrderingStores)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[OrderingStore](#OrderingStore)>? |  yes  |  |
 | deployedStores | ArrayList<Int>? |  yes  |  |
 | allStores | Boolean? |  yes  |  |
 | enabled | Boolean? |  yes  |  |
 | type | String? |  yes  |  |
 | id | String? |  yes  |  |
 | app | String? |  yes  |  |
 | v | Int? |  yes  |  |

---




 
 
 #### [CouponDateMeta](#CouponDateMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | modifiedOn | String? |  yes  |  |
 | createdOn | String? |  yes  |  |

---


 
 
 #### [Validation](#Validation)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | userRegisteredAfter | String? |  yes  |  |
 | appId | ArrayList<String>? |  yes  |  |
 | anonymous | Boolean? |  yes  |  |

---


 
 
 #### [DisplayMetaDict](#DisplayMetaDict)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | subtitle | String? |  yes  |  |

---


 
 
 #### [DisplayMeta](#DisplayMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | subtitle | String? |  yes  |  |
 | auto | [DisplayMetaDict](#DisplayMetaDict)? |  yes  |  |
 | remove | [DisplayMetaDict](#DisplayMetaDict)? |  yes  |  |
 | title | String? |  yes  |  |
 | apply | [DisplayMetaDict](#DisplayMetaDict)? |  yes  |  |
 | description | String? |  yes  |  |

---


 
 
 #### [PaymentAllowValue](#PaymentAllowValue)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | max | Int? |  yes  |  |

---


 
 
 #### [PaymentModes](#PaymentModes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | types | ArrayList<String>? |  yes  |  |
 | codes | ArrayList<String>? |  yes  |  |
 | uses | [PaymentAllowValue](#PaymentAllowValue)? |  yes  |  |
 | networks | ArrayList<String>? |  yes  |  |

---


 
 
 #### [PaymentCodes](#PaymentCodes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ps | [PaymentModes](#PaymentModes)? |  yes  |  |
 | qr | [PaymentModes](#PaymentModes)? |  yes  |  |
 | nb | [PaymentModes](#PaymentModes)? |  yes  |  |
 | stripepg | [PaymentModes](#PaymentModes)? |  yes  |  |
 | wl | [PaymentModes](#PaymentModes)? |  yes  |  |
 | card | [PaymentModes](#PaymentModes)? |  yes  |  |
 | simpl | [PaymentModes](#PaymentModes)? |  yes  |  |
 | pl | [PaymentModes](#PaymentModes)? |  yes  |  |
 | rupifipg | [PaymentModes](#PaymentModes)? |  yes  |  |
 | upi | [PaymentModes](#PaymentModes)? |  yes  |  |

---


 
 
 #### [PriceRange](#PriceRange)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | max | Int? |  yes  |  |
 | min | Int? |  yes  |  |

---


 
 
 #### [PostOrder](#PostOrder)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cancellationAllowed | Boolean? |  yes  |  |
 | returnAllowed | Boolean? |  yes  |  |

---


 
 
 #### [BulkBundleRestriction](#BulkBundleRestriction)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | multiStoreAllowed | Boolean |  no  |  |

---


 
 
 #### [UsesRemaining](#UsesRemaining)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | total | Int? |  yes  |  |
 | user | Int? |  yes  |  |
 | app | Int? |  yes  |  |

---


 
 
 #### [UsesRestriction](#UsesRestriction)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | remaining | [UsesRemaining](#UsesRemaining)? |  yes  |  |
 | maximum | [UsesRemaining](#UsesRemaining)? |  yes  |  |

---


 
 
 #### [Restrictions](#Restrictions)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | payments | [PaymentCodes](#PaymentCodes)? |  yes  |  |
 | priceRange | [PriceRange](#PriceRange)? |  yes  |  |
 | postOrder | [PostOrder](#PostOrder)? |  yes  |  |
 | bulkBundle | [BulkBundleRestriction](#BulkBundleRestriction)? |  yes  |  |
 | couponAllowed | Boolean? |  yes  |  |
 | uses | [UsesRestriction](#UsesRestriction)? |  yes  |  |
 | platforms | ArrayList<String>? |  yes  |  |
 | orderingStores | ArrayList<Int>? |  yes  |  |

---


 
 
 #### [RuleDefinition](#RuleDefinition)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | valueType | String |  no  |  |
 | type | String |  no  |  |
 | applicableOn | String |  no  |  |
 | currencyCode | String? |  yes  |  |
 | isExact | Boolean? |  yes  |  |
 | autoApply | Boolean? |  yes  |  |
 | scope | ArrayList<String>? |  yes  |  |
 | calculateOn | String |  no  |  |

---


 
 
 #### [Identifier](#Identifier)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | storeId | ArrayList<Int>? |  yes  |  |
 | categoryId | ArrayList<Int>? |  yes  |  |
 | itemId | ArrayList<Int>? |  yes  |  |
 | articleId | ArrayList<String>? |  yes  |  |
 | brandId | ArrayList<Int>? |  yes  |  |
 | collectionId | ArrayList<String>? |  yes  |  |
 | companyId | ArrayList<Int>? |  yes  |  |
 | userId | ArrayList<String>? |  yes  |  |

---


 
 
 #### [Validity](#Validity)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | priority | Int? |  yes  |  |

---


 
 
 #### [Ownership](#Ownership)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | payableCategory | String |  no  |  |
 | payableBy | String |  no  |  |

---


 
 
 #### [CouponAuthor](#CouponAuthor)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | createdBy | String? |  yes  |  |
 | modifiedBy | String? |  yes  |  |

---


 
 
 #### [State](#State)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isDisplay | Boolean? |  yes  |  |
 | isArchived | Boolean? |  yes  |  |
 | isPublic | Boolean? |  yes  |  |

---


 
 
 #### [CouponAction](#CouponAction)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | actionDate | String? |  yes  |  |
 | txnMode | String? |  yes  |  |

---


 
 
 #### [CouponSchedule](#CouponSchedule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cron | String? |  yes  |  |
 | end | String? |  yes  |  |
 | nextSchedule | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | duration | Int? |  yes  |  |
 | start | String? |  yes  |  |

---


 
 
 #### [Rule](#Rule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | max | Double? |  yes  |  |
 | key | Double? |  yes  |  |
 | value | Double? |  yes  |  |
 | discountQty | Double? |  yes  |  |
 | min | Double? |  yes  |  |

---


 
 
 #### [CouponAdd](#CouponAdd)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tags | ArrayList<String>? |  yes  |  |
 | dateMeta | [CouponDateMeta](#CouponDateMeta)? |  yes  |  |
 | validation | [Validation](#Validation)? |  yes  |  |
 | displayMeta | [DisplayMeta](#DisplayMeta) |  no  |  |
 | typeSlug | String |  no  |  |
 | restrictions | [Restrictions](#Restrictions)? |  yes  |  |
 | ruleDefinition | [RuleDefinition](#RuleDefinition) |  no  |  |
 | identifiers | [Identifier](#Identifier) |  no  |  |
 | validity | [Validity](#Validity) |  no  |  |
 | ownership | [Ownership](#Ownership) |  no  |  |
 | author | [CouponAuthor](#CouponAuthor)? |  yes  |  |
 | state | [State](#State)? |  yes  |  |
 | action | [CouponAction](#CouponAction)? |  yes  |  |
 | schedule | [CouponSchedule](#CouponSchedule)? |  yes  |  |
 | code | String |  no  |  |
 | rule | ArrayList<[Rule](#Rule)> |  no  |  |

---


 
 
 #### [CouponsResponse](#CouponsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | [CouponAdd](#CouponAdd)? |  yes  |  |

---


 
 
 #### [SuccessMessage](#SuccessMessage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |
 | success | Boolean? |  yes  |  |

---


 
 
 #### [OperationErrorResponse](#OperationErrorResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |
 | success | Boolean? |  yes  |  |

---


 
 
 #### [CouponUpdate](#CouponUpdate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tags | ArrayList<String>? |  yes  |  |
 | dateMeta | [CouponDateMeta](#CouponDateMeta)? |  yes  |  |
 | validation | [Validation](#Validation)? |  yes  |  |
 | displayMeta | [DisplayMeta](#DisplayMeta) |  no  |  |
 | typeSlug | String |  no  |  |
 | restrictions | [Restrictions](#Restrictions)? |  yes  |  |
 | ruleDefinition | [RuleDefinition](#RuleDefinition) |  no  |  |
 | identifiers | [Identifier](#Identifier) |  no  |  |
 | validity | [Validity](#Validity) |  no  |  |
 | ownership | [Ownership](#Ownership) |  no  |  |
 | author | [CouponAuthor](#CouponAuthor)? |  yes  |  |
 | state | [State](#State)? |  yes  |  |
 | action | [CouponAction](#CouponAction)? |  yes  |  |
 | schedule | [CouponSchedule](#CouponSchedule)? |  yes  |  |
 | code | String |  no  |  |
 | rule | ArrayList<[Rule](#Rule)> |  no  |  |

---


 
 
 #### [CouponPartialUpdate](#CouponPartialUpdate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | archive | Boolean? |  yes  | Send true to unpublish coupon |
 | schedule | [CouponSchedule](#CouponSchedule)? |  yes  |  |

---


 
 
 #### [CartItem](#CartItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | productId | String |  no  |  |
 | size | String |  no  |  |
 | quantity | Int? |  yes  |  |

---


 
 
 #### [OpenapiCartDetailsRequest](#OpenapiCartDetailsRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cartItems | [CartItem](#CartItem)? |  yes  |  |

---


 
 
 #### [CouponBreakup](#CouponBreakup)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isApplied | Boolean? |  yes  |  |
 | type | String? |  yes  |  |
 | uid | String? |  yes  |  |
 | message | String? |  yes  |  |
 | value | Double? |  yes  |  |
 | code | String? |  yes  |  |

---


 
 
 #### [DisplayBreakup](#DisplayBreakup)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |
 | message | ArrayList<String>? |  yes  |  |
 | key | String? |  yes  |  |
 | value | Double? |  yes  |  |
 | currencySymbol | String? |  yes  |  |

---


 
 
 #### [RawBreakup](#RawBreakup)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | total | Double? |  yes  |  |
 | youSaved | Double? |  yes  |  |
 | mrpTotal | String? |  yes  |  |
 | vog | Double? |  yes  |  |
 | subtotal | Double? |  yes  |  |
 | convenienceFee | Double? |  yes  |  |
 | deliveryCharge | Double? |  yes  |  |
 | discount | Double? |  yes  |  |
 | coupon | Double? |  yes  |  |
 | fyndCash | Double? |  yes  |  |
 | gstCharges | Double? |  yes  |  |
 | codCharge | Double? |  yes  |  |

---


 
 
 #### [LoyaltyPoints](#LoyaltyPoints)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | total | Double? |  yes  |  |
 | isApplied | Boolean? |  yes  |  |
 | applicable | Double? |  yes  |  |
 | description | String? |  yes  |  |

---


 
 
 #### [CartBreakup](#CartBreakup)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | coupon | [CouponBreakup](#CouponBreakup)? |  yes  |  |
 | display | ArrayList<[DisplayBreakup](#DisplayBreakup)>? |  yes  |  |
 | raw | [RawBreakup](#RawBreakup)? |  yes  |  |
 | loyaltyPoints | [LoyaltyPoints](#LoyaltyPoints)? |  yes  |  |

---


 
 
 #### [BaseInfo](#BaseInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | uid | Int? |  yes  |  |

---


 
 
 #### [ProductImage](#ProductImage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | secureUrl | String? |  yes  |  |
 | aspectRatio | String? |  yes  |  |
 | url | String? |  yes  |  |

---


 
 
 #### [CategoryInfo](#CategoryInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | uid | Int? |  yes  | Product Category Id |

---


 
 
 #### [ActionQuery](#ActionQuery)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | productSlug | ArrayList<String>? |  yes  | Contains list of product slug |

---


 
 
 #### [ProductAction](#ProductAction)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | query | [ActionQuery](#ActionQuery)? |  yes  |  |
 | url | String? |  yes  |  |

---


 
 
 #### [CartProduct](#CartProduct)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brand | [BaseInfo](#BaseInfo)? |  yes  |  |
 | images | ArrayList<[ProductImage](#ProductImage)>? |  yes  |  |
 | type | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | categories | ArrayList<[CategoryInfo](#CategoryInfo)>? |  yes  |  |
 | action | [ProductAction](#ProductAction)? |  yes  |  |
 | name | String? |  yes  |  |
 | slug | String? |  yes  | Unique product url name generated via product name and other meta data |

---


 
 
 #### [BasePrice](#BasePrice)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | currencyCode | String? |  yes  |  |
 | effective | Double? |  yes  |  |
 | marked | Double? |  yes  |  |
 | currencySymbol | String? |  yes  |  |

---


 
 
 #### [ArticlePriceInfo](#ArticlePriceInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | base | [BasePrice](#BasePrice)? |  yes  |  |
 | converted | [BasePrice](#BasePrice)? |  yes  |  |

---


 
 
 #### [ProductArticle](#ProductArticle)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | size | String? |  yes  |  |
 | type | String? |  yes  |  |
 | uid | String? |  yes  |  |
 | quantity | Int? |  yes  |  |
 | extraMeta | HashMap<String,Any>? |  yes  |  |
 | price | [ArticlePriceInfo](#ArticlePriceInfo)? |  yes  |  |
 | seller | [BaseInfo](#BaseInfo)? |  yes  |  |
 | store | [BaseInfo](#BaseInfo)? |  yes  |  |

---


 
 
 #### [ProductPrice](#ProductPrice)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | marked | Double? |  yes  |  |
 | selling | Double? |  yes  |  |
 | currencyCode | String? |  yes  |  |
 | effective | Double? |  yes  |  |
 | addOn | Double? |  yes  |  |
 | currencySymbol | String? |  yes  |  |

---


 
 
 #### [ProductPriceInfo](#ProductPriceInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | base | [ProductPrice](#ProductPrice)? |  yes  |  |
 | converted | [ProductPrice](#ProductPrice)? |  yes  |  |

---


 
 
 #### [CartProductIdentifer](#CartProductIdentifer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | identifier | String? |  yes  | Article idenfier generated by cart |

---


 
 
 #### [ProductAvailability](#ProductAvailability)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | deliverable | Boolean? |  yes  |  |
 | outOfStock | Boolean? |  yes  |  |
 | isValid | Boolean? |  yes  |  |
 | otherStoreQuantity | Int? |  yes  |  |
 | sizes | ArrayList<String>? |  yes  |  |

---


 
 
 #### [PromoMeta](#PromoMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [CartProductInfo](#CartProductInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | product | [CartProduct](#CartProduct)? |  yes  |  |
 | article | [ProductArticle](#ProductArticle)? |  yes  |  |
 | pricePerUnit | [ProductPriceInfo](#ProductPriceInfo)? |  yes  |  |
 | identifiers | [CartProductIdentifer](#CartProductIdentifer) |  no  |  |
 | availability | [ProductAvailability](#ProductAvailability)? |  yes  |  |
 | quantity | Int? |  yes  |  |
 | bulkOffer | HashMap<String,Any>? |  yes  |  |
 | message | String? |  yes  |  |
 | key | String? |  yes  |  |
 | discount | String? |  yes  |  |
 | promoMeta | [PromoMeta](#PromoMeta)? |  yes  |  |
 | price | [ProductPriceInfo](#ProductPriceInfo)? |  yes  |  |
 | isSet | Boolean? |  yes  |  |
 | couponMessage | String? |  yes  |  |

---


 
 
 #### [OpenapiCartDetailsResponse](#OpenapiCartDetailsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |
 | breakupValues | [CartBreakup](#CartBreakup)? |  yes  |  |
 | isValid | Boolean? |  yes  |  |
 | items | ArrayList<[CartProductInfo](#CartProductInfo)>? |  yes  |  |

---


 
 
 #### [OpenApiErrorResponse](#OpenApiErrorResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | errors | HashMap<String,Any>? |  yes  | Contains field name which has error as key and error message as value |
 | message | String? |  yes  |  |
 | success | Boolean? |  yes  |  |

---


 
 
 #### [ShippingAddress](#ShippingAddress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | areaCodeSlug | String? |  yes  |  |
 | pincode | Int? |  yes  |  |
 | phone | Int? |  yes  |  |
 | city | String |  no  |  |
 | area | String? |  yes  |  |
 | state | String |  no  |  |
 | landmark | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | areaCode | String |  no  |  |
 | name | String? |  yes  |  |
 | addressType | String? |  yes  |  |
 | country | String |  no  |  |
 | address | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | email | String? |  yes  |  |

---


 
 
 #### [OpenApiCartServiceabilityRequest](#OpenApiCartServiceabilityRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cartItems | [CartItem](#CartItem)? |  yes  |  |
 | shippingAddress | [ShippingAddress](#ShippingAddress) |  no  |  |

---


 
 
 #### [PromiseFormatted](#PromiseFormatted)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | max | String? |  yes  |  |
 | min | String? |  yes  |  |

---


 
 
 #### [PromiseTimestamp](#PromiseTimestamp)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | max | Double? |  yes  |  |
 | min | Double? |  yes  |  |

---


 
 
 #### [ShipmentPromise](#ShipmentPromise)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | formatted | [PromiseFormatted](#PromiseFormatted)? |  yes  |  |
 | timestamp | [PromiseTimestamp](#PromiseTimestamp)? |  yes  |  |

---


 
 
 #### [OpenApiCartServiceabilityResponse](#OpenApiCartServiceabilityResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isValid | Boolean? |  yes  |  |
 | items | ArrayList<[CartProductInfo](#CartProductInfo)>? |  yes  |  |
 | message | String? |  yes  |  |
 | breakupValues | [CartBreakup](#CartBreakup)? |  yes  |  |
 | deliveryPromise | [ShipmentPromise](#ShipmentPromise)? |  yes  |  |

---


 
 
 #### [OpenApiFiles](#OpenApiFiles)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String |  no  |  |
 | values | ArrayList<String> |  no  |  |

---


 
 
 #### [CartItemMeta](#CartItemMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | groupId | String? |  yes  |  |
 | primaryItem | Boolean? |  yes  |  |

---


 
 
 #### [MultiTenderPaymentMeta](#MultiTenderPaymentMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | currentStatus | String? |  yes  |  |
 | orderId | String? |  yes  |  |
 | paymentGateway | String? |  yes  |  |
 | extraMeta | HashMap<String,Any>? |  yes  |  |
 | paymentId | String? |  yes  |  |

---


 
 
 #### [MultiTenderPaymentMethod](#MultiTenderPaymentMethod)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | meta | [MultiTenderPaymentMeta](#MultiTenderPaymentMeta)? |  yes  |  |
 | mode | String |  no  |  |
 | name | String? |  yes  | Payment mode name |
 | amount | Double |  no  | Payment amount |

---


 
 
 #### [OpenApiOrderItem](#OpenApiOrderItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | couponEffectiveDiscount | Double |  no  |  |
 | codCharges | Double |  no  |  |
 | priceMarked | Double |  no  |  |
 | files | ArrayList<[OpenApiFiles](#OpenApiFiles)>? |  yes  |  |
 | productId | Int |  no  |  |
 | quantity | Int? |  yes  |  |
 | cashbackApplied | Double |  no  |  |
 | meta | [CartItemMeta](#CartItemMeta)? |  yes  |  |
 | priceEffective | Double |  no  |  |
 | discount | Double |  no  |  |
 | deliveryCharges | Double |  no  |  |
 | loyaltyDiscount | Double? |  yes  |  |
 | amountPaid | Double |  no  |  |
 | extraMeta | HashMap<String,Any>? |  yes  |  |
 | paymentMethods | ArrayList<[MultiTenderPaymentMethod](#MultiTenderPaymentMethod)> |  no  |  |
 | size | String |  no  |  |
 | employeeDiscount | Double? |  yes  |  |

---


 
 
 #### [OpenApiPlatformCheckoutReq](#OpenApiPlatformCheckoutReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | codCharges | Double |  no  |  |
 | files | ArrayList<[OpenApiFiles](#OpenApiFiles)>? |  yes  |  |
 | cashbackApplied | Double |  no  |  |
 | shippingAddress | [ShippingAddress](#ShippingAddress)? |  yes  |  |
 | couponCode | String |  no  |  |
 | employeeDiscount | HashMap<String,Any>? |  yes  |  |
 | couponValue | Double |  no  |  |
 | cartItems | ArrayList<[OpenApiOrderItem](#OpenApiOrderItem)> |  no  |  |
 | loyaltyDiscount | Double? |  yes  |  |
 | deliveryCharges | Double |  no  |  |
 | paymentMethods | ArrayList<[MultiTenderPaymentMethod](#MultiTenderPaymentMethod)> |  no  |  |
 | coupon | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |
 | paymentMode | String? |  yes  |  |
 | affiliateOrderId | String? |  yes  |  |
 | billingAddress | [ShippingAddress](#ShippingAddress) |  no  |  |
 | orderId | String? |  yes  |  |
 | cartValue | Double |  no  |  |

---


 
 
 #### [OpenApiCheckoutResponse](#OpenApiCheckoutResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |
 | success | Boolean? |  yes  |  |
 | orderId | String |  no  | Fynd order id |
 | orderRefId | String? |  yes  | Order id sent in request |

---




 
 
 #### [AppUser](#AppUser)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | applicationId | String? |  yes  |  |
 | blockReason | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | updatedBy | String? |  yes  |  |
 | userId | String? |  yes  |  |

---


 
 
 #### [E](#E)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | code | HashMap<String,Any>? |  yes  |  |
 | exception | String? |  yes  |  |
 | info | String? |  yes  |  |
 | message | String? |  yes  |  |
 | requestId | String? |  yes  |  |
 | stackTrace | String? |  yes  |  |
 | status | Int? |  yes  |  |

---


 
 
 #### [Giveaway](#Giveaway)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | schedule | [Schedule](#Schedule)? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | applicationId | String? |  yes  |  |
 | audience | [RewardsAudience](#RewardsAudience)? |  yes  |  |
 | bannerImage | [Asset](#Asset)? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | description | String? |  yes  |  |
 | name | String? |  yes  |  |
 | rule | [RewardsRule](#RewardsRule)? |  yes  |  |
 | title | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |

---


 
 
 #### [GiveawayResponse](#GiveawayResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Giveaway](#Giveaway)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [HistoryPretty](#HistoryPretty)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | applicationId | String? |  yes  |  |
 | claimed | Boolean? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | expiresOn | String? |  yes  |  |
 | points | Double? |  yes  |  |
 | remainingPoints | Double? |  yes  |  |
 | text1 | String? |  yes  |  |
 | text2 | String? |  yes  |  |
 | text3 | String? |  yes  |  |
 | txnName | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | userId | String? |  yes  |  |

---


 
 
 #### [HistoryRes](#HistoryRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[HistoryPretty](#HistoryPretty)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |
 | points | Double? |  yes  |  |

---


 
 
 #### [Offer](#Offer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | schedule | [Schedule](#Schedule)? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | applicationId | String? |  yes  |  |
 | bannerImage | [Asset](#Asset)? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | name | String? |  yes  |  |
 | rule | HashMap<String,Any>? |  yes  |  |
 | share | [ShareMessages](#ShareMessages)? |  yes  |  |
 | subText | String? |  yes  |  |
 | text | String? |  yes  |  |
 | type | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | updatedBy | String? |  yes  |  |
 | url | String? |  yes  |  |

---


 
 
 #### [Points](#Points)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | available | Double? |  yes  |  |

---


 
 
 #### [Referral](#Referral)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | code | String? |  yes  |  |

---


 
 
 #### [RewardUser](#RewardUser)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | referral | [Referral](#Referral)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | userBlockReason | String? |  yes  |  |
 | userId | String? |  yes  |  |

---


 
 
 #### [RewardsAudience](#RewardsAudience)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | headerUserId | String? |  yes  |  |
 | id | String? |  yes  |  |

---


 
 
 #### [RewardsRule](#RewardsRule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | amount | Double? |  yes  |  |

---


 
 
 #### [ShareMessages](#ShareMessages)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | String? |  yes  |  |
 | facebook | String? |  yes  |  |
 | fallback | String? |  yes  |  |
 | message | String? |  yes  |  |
 | messenger | String? |  yes  |  |
 | sms | String? |  yes  |  |
 | text | String? |  yes  |  |
 | twitter | String? |  yes  |  |
 | whatsapp | String? |  yes  |  |

---


 
 
 #### [UserRes](#UserRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | points | [Points](#Points)? |  yes  |  |
 | user | [RewardUser](#RewardUser)? |  yes  |  |

---




 
 
 #### [StatGroup](#StatGroup)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String? |  yes  |  |
 | url | String? |  yes  |  |
 | title | String? |  yes  |  |

---


 
 
 #### [StatsGroups](#StatsGroups)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | groups | ArrayList<[StatGroup](#StatGroup)>? |  yes  |  |

---


 
 
 #### [StatsGroupComponent](#StatsGroupComponent)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String? |  yes  |  |
 | url | String? |  yes  |  |
 | title | String? |  yes  |  |
 | type | String? |  yes  |  |
 | filters | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [StatsGroupComponents](#StatsGroupComponents)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | components | ArrayList<[StatsGroupComponent](#StatsGroupComponent)>? |  yes  |  |

---


 
 
 #### [StatsRes](#StatsRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String? |  yes  |  |
 | title | String? |  yes  |  |
 | type | String? |  yes  |  |
 | data | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [ReceivedAt](#ReceivedAt)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | String? |  yes  |  |

---


 
 
 #### [AbandonCartsDetail](#AbandonCartsDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | propertiesCartId | String? |  yes  |  |
 | contextTraitsFirstName | String? |  yes  |  |
 | contextTraitsLastName | String? |  yes  |  |
 | contextTraitsPhoneNumber | String? |  yes  |  |
 | contextTraitsEmail | String? |  yes  |  |
 | contextAppApplicationId | String? |  yes  |  |
 | propertiesBreakupValuesRawTotal | String? |  yes  |  |
 | receivedAt | [ReceivedAt](#ReceivedAt)? |  yes  |  |

---


 
 
 #### [AbandonCartsList](#AbandonCartsList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[AbandonCartsDetail](#AbandonCartsDetail)>? |  yes  |  |
 | cartTotal | String? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [AbandonCartDetail](#AbandonCartDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | userId | String? |  yes  |  |
 | cartValue | String? |  yes  |  |
 | articles | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | breakup | HashMap<String,Any>? |  yes  |  |
 | address | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [ExportJobReq](#ExportJobReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | marketplaceName | String? |  yes  |  |
 | startTime | String? |  yes  |  |
 | endTime | String? |  yes  |  |
 | eventType | String? |  yes  |  |
 | traceId | String? |  yes  |  |

---


 
 
 #### [ExportJobRes](#ExportJobRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | String? |  yes  |  |
 | jobId | String? |  yes  |  |

---


 
 
 #### [ExportJobStatusRes](#ExportJobStatusRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | String? |  yes  |  |
 | jobId | String? |  yes  |  |
 | downloadUrl | String? |  yes  |  |

---


 
 
 #### [GetLogsListReq](#GetLogsListReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | marketplaceName | String? |  yes  |  |
 | startDate | String? |  yes  |  |
 | companyId | String? |  yes  |  |
 | endDate | String? |  yes  |  |

---


 
 
 #### [MkpLogsResp](#MkpLogsResp)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | startTimeIso | String? |  yes  |  |
 | endTimeIso | String? |  yes  |  |
 | eventType | String? |  yes  |  |
 | traceId | String? |  yes  |  |
 | count | String? |  yes  |  |
 | status | String? |  yes  |  |

---


 
 
 #### [GetLogsListRes](#GetLogsListRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[MkpLogsResp](#MkpLogsResp)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [SearchLogReq](#SearchLogReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | marketplaceName | String? |  yes  |  |
 | startDate | String? |  yes  |  |
 | companyId | String? |  yes  |  |
 | endDate | String? |  yes  |  |
 | identifier | String? |  yes  |  |
 | identifierValue | String? |  yes  |  |

---


 
 
 #### [LogInfo](#LogInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | status | String? |  yes  |  |
 | eventType | String? |  yes  |  |
 | marketplaceName | String? |  yes  |  |
 | event | String? |  yes  |  |
 | traceId | String? |  yes  |  |
 | companyId | Double? |  yes  |  |
 | brandId | Double? |  yes  |  |
 | storeCode | String? |  yes  |  |
 | storeId | Double? |  yes  |  |
 | itemId | Double? |  yes  |  |
 | articleId | String? |  yes  |  |
 | sellerIdentifier | String? |  yes  |  |

---


 
 
 #### [SearchLogRes](#SearchLogRes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[LogInfo](#LogInfo)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---




 
 
 #### [ValidityObject](#ValidityObject)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | start | String |  no  |  |
 | end | String |  no  |  |

---


 
 
 #### [CreateUpdateDiscount](#CreateUpdateDiscount)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | companyId | Int |  no  |  |
 | isActive | Boolean |  no  |  |
 | appIds | ArrayList<String> |  no  |  |
 | jobType | String |  no  |  |
 | discountType | String |  no  |  |
 | discountLevel | String |  no  |  |
 | value | Int? |  yes  |  |
 | filePath | String? |  yes  |  |
 | brandIds | ArrayList<Int>? |  yes  |  |
 | storeIds | ArrayList<Int>? |  yes  |  |
 | validity | [ValidityObject](#ValidityObject) |  no  |  |

---


 
 
 #### [DiscountJob](#DiscountJob)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |
 | name | String |  no  |  |
 | companyId | Int |  no  |  |
 | isActive | Boolean |  no  |  |
 | appIds | ArrayList<String>? |  yes  |  |
 | jobType | String? |  yes  |  |
 | discountType | String? |  yes  |  |
 | discountLevel | String? |  yes  |  |
 | value | Int? |  yes  |  |
 | filePath | String? |  yes  |  |
 | brandIds | ArrayList<Int>? |  yes  |  |
 | storeIds | ArrayList<Int>? |  yes  |  |
 | validity | [ValidityObject](#ValidityObject) |  no  |  |
 | createdOn | String |  no  |  |
 | modifiedOn | String |  no  |  |
 | createdBy | [UserDetails](#UserDetails) |  no  |  |
 | modifiedBy | [UserDetails](#UserDetails) |  no  |  |
 | meta | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [ListOrCalender](#ListOrCalender)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[DiscountJob](#DiscountJob)> |  no  |  |
 | page | [Page](#Page) |  no  |  |

---


 
 
 #### [FileJobResponse](#FileJobResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | stage | String |  no  |  |
 | total | Int |  no  |  |
 | failed | Int |  no  |  |
 | companyId | Int |  no  |  |
 | body | HashMap<String,Any>? |  yes  |  |
 | type | String |  no  |  |
 | fileType | String |  no  |  |

---


 
 
 #### [DownloadFileJob](#DownloadFileJob)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brandIds | ArrayList<Int>? |  yes  |  |
 | storeIds | ArrayList<Int>? |  yes  |  |

---


 
 
 #### [CancelJobResponse](#CancelJobResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean |  no  |  |

---


 
 
 #### [UserDetails](#UserDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | username | String |  no  |  |
 | userId | String |  no  |  |

---


 
 
 #### [BadRequestObject](#BadRequestObject)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String |  no  |  |

---




 
 
 #### [AddProxyReq](#AddProxyReq)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | attachedPath | String? |  yes  | Proxy path slug |
 | proxyUrl | String? |  yes  | Proxied url |

---


 
 
 #### [AddProxyResponse](#AddProxyResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | attachedPath | String? |  yes  |  |
 | proxyUrl | String? |  yes  |  |
 | companyId | String? |  yes  |  |
 | applicationId | String? |  yes  |  |
 | extensionId | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | modifiedAt | String? |  yes  |  |

---


 
 
 #### [ApiError](#ApiError)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | code | String? |  yes  |  |
 | message | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [RemoveProxyResponse](#RemoveProxyResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |
 | data | HashMap<String,Any>? |  yes  |  |

---




 
 
 #### [EventConfig](#EventConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |
 | eventName | String? |  yes  |  |
 | eventType | String? |  yes  |  |
 | eventCategory | String? |  yes  |  |
 | version | String? |  yes  |  |
 | displayName | String? |  yes  |  |
 | description | String? |  yes  |  |
 | createdOn | String? |  yes  |  |

---


 
 
 #### [EventConfigList](#EventConfigList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[EventConfig](#EventConfig)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [SubscriberConfigList](#SubscriberConfigList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[SubscriberResponse](#SubscriberResponse)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [EventProcessedStatus](#EventProcessedStatus)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |
 | subscriberId | String? |  yes  |  |
 | attempt | Int? |  yes  |  |
 | responseCode | String? |  yes  |  |
 | responseMessage | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | processedOn | String? |  yes  |  |
 | status | Boolean? |  yes  |  |

---


 
 
 #### [EventPayload](#EventPayload)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |
 | eventTraceId | String? |  yes  |  |
 | messageId | String? |  yes  |  |
 | eventName | String? |  yes  |  |
 | eventType | String? |  yes  |  |
 | version | String? |  yes  |  |
 | status | Boolean? |  yes  |  |

---


 
 
 #### [SubscriberConfig](#SubscriberConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | webhookUrl | String? |  yes  |  |
 | association | [Association](#Association)? |  yes  |  |
 | status | [SubscriberStatus](#SubscriberStatus)? |  yes  |  |
 | emailId | String? |  yes  |  |
 | authMeta | [AuthMeta](#AuthMeta)? |  yes  |  |
 | eventId | ArrayList<Int>? |  yes  |  |

---


 
 
 #### [SubscriberResponse](#SubscriberResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | webhookUrl | String? |  yes  |  |
 | association | [Association](#Association)? |  yes  |  |
 | status | [SubscriberStatus](#SubscriberStatus)? |  yes  |  |
 | authMeta | [AuthMeta](#AuthMeta)? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | updatedOn | String? |  yes  |  |
 | eventConfigs | ArrayList<[EventConfig](#EventConfig)>? |  yes  |  |

---


 
 
 #### [SubscriberEvent](#SubscriberEvent)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | Int? |  yes  |  |
 | subscriberId | Int? |  yes  |  |
 | eventId | Int? |  yes  |  |
 | createdDate | String? |  yes  |  |

---


 
 
 #### [AuthMeta](#AuthMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | secret | String? |  yes  |  |

---


 
 
 #### [Association](#Association)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companyId | Int? |  yes  |  |
 | applicationId | ArrayList<String>? |  yes  |  |
 | extensionId | String? |  yes  |  |

---




### Enums




