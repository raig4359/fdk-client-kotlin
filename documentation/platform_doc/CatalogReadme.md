



### Catalog Methods

* ## [Catalog]
  * Methods
    * [deleteSearchKeywords](#deletesearchkeywords)
    * [getSearchKeywords](#getsearchkeywords)
    * [updateSearchKeywords](#updatesearchkeywords)
    * [getAllSearchKeyword](#getallsearchkeyword)
    * [createCustomKeyword](#createcustomkeyword)
    * [deleteAutocompleteKeyword](#deleteautocompletekeyword)
    * [getAutocompleteKeywordDetail](#getautocompletekeyworddetail)
    * [updateAutocompleteKeyword](#updateautocompletekeyword)
    * [getAutocompleteConfig](#getautocompleteconfig)
    * [createCustomAutocompleteRule](#createcustomautocompleterule)
    * [getProductBundle](#getproductbundle)
    * [createProductBundle](#createproductbundle)
    * [getProductBundleDetail](#getproductbundledetail)
    * [updateProductBundle](#updateproductbundle)
    * [getSizeGuides](#getsizeguides)
    * [createSizeGuide](#createsizeguide)
    * [getSizeGuide](#getsizeguide)
    * [updateSizeGuide](#updatesizeguide)
    * [getCatalogConfiguration](#getcatalogconfiguration)
    * [getConfigurations](#getconfigurations)
    * [createConfigurationProductListing](#createconfigurationproductlisting)
    * [getConfigurationByType](#getconfigurationbytype)
    * [createConfigurationByType](#createconfigurationbytype)
    * [getQueryFilters](#getqueryfilters)
    * [getAllCollections](#getallcollections)
    * [createCollection](#createcollection)
    * [getCollectionDetail](#getcollectiondetail)
    * [deleteCollection](#deletecollection)
    * [updateCollection](#updatecollection)
    * [getCollectionItems](#getcollectionitems)
    * [addCollectionItems](#addcollectionitems)
    * [getCatalogInsights](#getcataloginsights)
    * [getSellerInsights](#getsellerinsights)
    * [createMarketplaceOptin](#createmarketplaceoptin)
    * [getMarketplaceOptinDetail](#getmarketplaceoptindetail)
    * [getCompanyDetail](#getcompanydetail)
    * [getCompanyBrandDetail](#getcompanybranddetail)
    * [getCompanyMetrics](#getcompanymetrics)
    * [getStoreDetail](#getstoredetail)
    * [getGenderAttribute](#getgenderattribute)
    * [listProductTemplateCategories](#listproducttemplatecategories)
    * [listDepartmentsData](#listdepartmentsdata)
    * [getDepartmentData](#getdepartmentdata)
    * [listProductTemplate](#listproducttemplate)
    * [validateProductTemplate](#validateproducttemplate)
    * [downloadProductTemplateViews](#downloadproducttemplateviews)
    * [downloadProductTemplateView](#downloadproducttemplateview)
    * [validateProductTemplateSchema](#validateproducttemplateschema)
    * [listHSNCodes](#listhsncodes)
    * [listProductTemplateExportDetails](#listproducttemplateexportdetails)
    * [listTemplateBrandTypeValues](#listtemplatebrandtypevalues)
    * [listCategories](#listcategories)
    * [createCategories](#createcategories)
    * [getCategoryData](#getcategorydata)
    * [updateCategory](#updatecategory)
    * [getProducts](#getproducts)
    * [createProduct](#createproduct)
    * [deleteProduct](#deleteproduct)
    * [getProduct](#getproduct)
    * [editProduct](#editproduct)
    * [getProductValidation](#getproductvalidation)
    * [getProductSize](#getproductsize)
    * [getProductBulkUploadHistory](#getproductbulkuploadhistory)
    * [updateProductAssetsInBulk](#updateproductassetsinbulk)
    * [createProductsInBulk](#createproductsinbulk)
    * [deleteProductBulkJob](#deleteproductbulkjob)
    * [getCompanyTags](#getcompanytags)
    * [getProductAssetsInBulk](#getproductassetsinbulk)
    * [createProductAssetsInBulk](#createproductassetsinbulk)
    * [deleteSize](#deletesize)
    * [getInventoryBySize](#getinventorybysize)
    * [addInventory](#addinventory)
    * [getInventoryBySizeIdentifier](#getinventorybysizeidentifier)
    * [deleteInventory](#deleteinventory)
    * [getInventoryBulkUploadHistory](#getinventorybulkuploadhistory)
    * [createBulkInventoryJob](#createbulkinventoryjob)
    * [createBulkInventory](#createbulkinventory)
    * [deleteBulkInventoryJob](#deletebulkinventoryjob)
    * [getInventoryExport](#getinventoryexport)
    * [createInventoryExportJob](#createinventoryexportjob)
    * [exportInventoryConfig](#exportinventoryconfig)
    * [getAllHsnCodes](#getallhsncodes)
    * [createHsnCode](#createhsncode)
    * [getHsnCode](#gethsncode)
    * [updateHsnCode](#updatehsncode)
    * [bulkHsnCode](#bulkhsncode)
    * [getApplicationBrands](#getapplicationbrands)
    * [getDepartments](#getdepartments)
    * [getCategories](#getcategories)
    * [getAppicationProducts](#getappicationproducts)
    * [getProductDetailBySlug](#getproductdetailbyslug)
    * [getAppProducts](#getappproducts)
    
---

## Catalog


#### deleteSearchKeywords
Delete a Search Keywords




```kotlin
client.application("<APPLICATION_ID>").catalog.deleteSearchKeywords(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| id | String | yes | A `id` is a unique identifier for a particular detail. Pass the `id` of the keywords which you want to delete. |  



Delete a keywords by it's id. Returns an object that tells whether the keywords was deleted successfully

*Returned Response*




[DeleteResponse](#DeleteResponse)

Status object. Tells whether the operation was successful. See example below or refer `DeleteResponse`




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "message": "Words Deleted"
}
```
</details>









---


#### getSearchKeywords
Get a Search Keywords Details




```kotlin
client.application("<APPLICATION_ID>").catalog.getSearchKeywords(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| id | String | yes | A `id` is a unique identifier for a particular detail. Pass the `id` of the keywords which you want to retrieve. |  



Get the details of a words by its `id`. If successful, returns a Collection resource in the response body specified in `GetSearchWordsDetailResponseSchema`

*Returned Response*




[GetSearchWordsDetailResponse](#GetSearchWordsDetailResponse)

The Collection object. See example below or refer `GetSearchWordsDetailResponseSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "uid": "602fa1e9a596ce349563f6b9",
  "words": [
    "sds"
  ],
  "app_id": "000000000000000000000001",
  "is_active": true,
  "result": {
    "query": {
      "department": [
        "men"
      ]
    },
    "sort_on": "popular"
  },
  "_custom_json": {}
}
```
</details>









---


#### updateSearchKeywords
Update Search Keyword




```kotlin
client.application("<APPLICATION_ID>").catalog.updateSearchKeywords(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| id | String | yes | A `id` is a unique identifier for a particular detail. Pass the `id` of the keywords which you want to delete. |  
| body | [CreateSearchKeyword](#CreateSearchKeyword) | yes | Request body |


Update Search Keyword by its id. On successful request, returns the updated collection

*Returned Response*




[GetSearchWordsData](#GetSearchWordsData)

The Collection object. See example below or refer `GetSearchWordsDataSchema` for details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getAllSearchKeyword
List all Search Custom Keyword Listing




```kotlin
client.application("<APPLICATION_ID>").catalog.getAllSearchKeyword().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |  



Custom Search Keyword allows you to map conditions with keywords to give you the ultimate results

*Returned Response*




[GetSearchWordsResponse](#GetSearchWordsResponse)

List of custom search keywords. See example below or refer `GetSearchWordsResponseSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {
    "current": 1,
    "size": 1,
    "has_previous": false,
    "has_next": false,
    "item_count": 1
  },
  "items": [
    {
      "uid": "602fa1e9a596ce349563f6b9",
      "words": [
        "sds"
      ],
      "app_id": "000000000000000000000001",
      "is_active": true,
      "result": {
        "query": {
          "department": [
            "men"
          ]
        },
        "sort_on": "popular"
      },
      "_custom_json": {}
    }
  ]
}
```
</details>









---


#### createCustomKeyword
Add a Custom Search Keywords




```kotlin
client.application("<APPLICATION_ID>").catalog.createCustomKeyword(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |  
| body | [CreateSearchKeyword](#CreateSearchKeyword) | yes | Request body |


Create a Custom Search Keywords. See `CreateSearchKeywordSchema` for the list of attributes needed to create a mapping and /collections/query-options for the available options to create a rule. On successful request, returns a paginated list of collections specified in `CreateSearchKeywordSchema`

*Returned Response*




[GetSearchWordsData](#GetSearchWordsData)

Get keyword object with id that is added. See example below or refer `GetSearchWordsDataSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "uid": "602fa1e9a596ce349563f6b9",
  "words": [
    "sds"
  ],
  "app_id": "000000000000000000000001",
  "is_active": true,
  "result": {
    "query": {
      "department": [
        "men"
      ]
    },
    "sort_on": "popular"
  },
  "_custom_json": {}
}
```
</details>









---


#### deleteAutocompleteKeyword
Delete a Autocomplete Keywords




```kotlin
client.application("<APPLICATION_ID>").catalog.deleteAutocompleteKeyword(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| id | String | yes | A `id` is a unique identifier for a particular detail. Pass the `id` of the keywords which you want to delete. |  



Delete a keywords by it's id. Returns an object that tells whether the keywords was deleted successfully

*Returned Response*




[DeleteResponse](#DeleteResponse)

Status object. Tells whether the operation was successful. See example below or refer `DeleteResponse`




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "message": "Words Deleted"
}
```
</details>









---


#### getAutocompleteKeywordDetail
Get a Autocomplete Keywords Details




```kotlin
client.application("<APPLICATION_ID>").catalog.getAutocompleteKeywordDetail(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| id | String | yes | A `id` is a unique identifier for a particular detail. Pass the `id` of the keywords which you want to retrieve. |  



Get the details of a words by its `id`. If successful, returns a keywords resource in the response body specified in `GetAutocompleteWordsResponseSchema`

*Returned Response*




[GetAutocompleteWordsResponse](#GetAutocompleteWordsResponse)

The mapping object. See example below or refer `GetAutocompleteWordsResponseSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "uid": "602fa1eaa596ce349563f6c6",
  "app_id": "000000000000000000000001",
  "words": [
    "dasd"
  ],
  "is_active": true,
  "results": [
    {
      "_custom_json": {},
      "display": "Helllow",
      "logo": {
        "url": "https://hdn-1.addsale.com/addsale/company/61/applications/600a5b3fe0991a4718cdb448/company/1/application/000000000000000000000001/search/pictures/square-logo/original/n_8bvEaBw-Helllow.png"
      },
      "action": {
        "type": "page",
        "page": {
          "query": {
            "brand": [
              "nike"
            ]
          },
          "type": "products",
          "url": "/products/?brand=nike"
        }
      }
    }
  ]
}
```
</details>









---


#### updateAutocompleteKeyword
Create & Update Autocomplete Keyword




```kotlin
client.application("<APPLICATION_ID>").catalog.updateAutocompleteKeyword(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| id | String | yes | A `id` is a unique identifier for a particular detail. Pass the `id` of the keywords which you want to delete. |  
| body | [CreateAutocompleteKeyword](#CreateAutocompleteKeyword) | yes | Request body |


Update a mapping by it's id. On successful request, returns the updated Keyword mapping

*Returned Response*




[GetAutocompleteWordsResponse](#GetAutocompleteWordsResponse)

The Mapping object. See example below or refer `GetAutocompleteWordsResponseSchema` for details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getAutocompleteConfig
List all Autocomplete Keyword Listing




```kotlin
client.application("<APPLICATION_ID>").catalog.getAutocompleteConfig().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |  



Custom Autocomplete Keyword allows you to map conditions with keywords to give you the ultimate results

*Returned Response*




[GetAutocompleteWordsResponse](#GetAutocompleteWordsResponse)

List of custom autocomplete keywords. See example below or refer `GetAutocompleteWordsResponseSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {
    "current": 1,
    "size": 1,
    "has_previous": false,
    "has_next": false,
    "item_count": 1
  },
  "items": [
    {
      "uid": "602fa1eaa596ce349563f6c6",
      "app_id": "000000000000000000000001",
      "words": [
        "dasd"
      ],
      "is_active": true,
      "results": [
        {
          "_custom_json": {},
          "display": "Helllow",
          "logo": {
            "url": "https://hdn-1.addsale.com/addsale/company/61/applications/600a5b3fe0991a4718cdb448/company/1/application/000000000000000000000001/search/pictures/square-logo/original/n_8bvEaBw-Helllow.png"
          },
          "action": {
            "type": "page",
            "page": {
              "query": {
                "brand": [
                  "nike"
                ]
              },
              "type": "products",
              "url": "/products/?brand=nike"
            }
          }
        }
      ]
    }
  ]
}
```
</details>









---


#### createCustomAutocompleteRule
Add a Custom Autocomplete Keywords




```kotlin
client.application("<APPLICATION_ID>").catalog.createCustomAutocompleteRule(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |  
| body | [CreateAutocompleteKeyword](#CreateAutocompleteKeyword) | yes | Request body |


Create a Custom Autocomplete Keywords. See `CreateAutocompleteKeywordSchema` for the list of attributes needed to create a mapping and /collections/query-options for the available options to create a rule. On successful request, returns a paginated list of collections specified in `CreateAutocompleteKeywordSchema`

*Returned Response*




[CreateAutocompleteWordsResponse](#CreateAutocompleteWordsResponse)

List of all the collections including the one you added. See example below or refer `CreateAutocompleteWordsResponseSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getProductBundle
List all Product Bundles




```kotlin
client.catalog.getProductBundle(q: q).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| q | String? | no | A search string that is searched with product bundle name. |  



Get all product bundles for a particular company

*Returned Response*




[GetProductBundleListingResponse](#GetProductBundleListingResponse)

List of bundle configured for a company. See example below or refer `GetProductBundleListingResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {
    "current": 1,
    "total": 1,
    "has_previous": false,
    "has_next": false,
    "total_item_count": 4
  },
  "items": [
    {
      "slug": "bag",
      "logo": "http://g.com/poo.png/",
      "name": "Bag",
      "choice": "multi",
      "products": [
        {
          "product_uid": 7500001,
          "max_quantity": 1,
          "min_quantity": 1,
          "auto_add_to_cart": false,
          "auto_select": false,
          "allow_remove": true
        }
      ],
      "meta": {},
      "same_store_assignment": true,
      "is_active": true,
      "page_visibility": [
        "pdp"
      ],
      "created_by": {
        "username": "917827311650_22960",
        "uid": "123"
      },
      "company_id": 1,
      "created_on": "2021-02-19 16:40:26.310007",
      "modified_by": {
        "username": "917827311650_22960",
        "uid": "123"
      },
      "modified_on": "2021-02-19 16:40:26.310027",
      "id": "602f9ca2a596ce312f5956f9"
    },
    {
      "choice": "multi",
      "same_store_assignment": true,
      "products": [
        {
          "auto_select": false,
          "allow_remove": true,
          "auto_add_to_cart": false,
          "max_quantity": 1,
          "product_uid": 7500001,
          "min_quantity": 1
        }
      ],
      "is_active": true,
      "slug": "bag",
      "meta": {},
      "logo": "http://g.com/poo.png/",
      "page_visibility": [
        "pdp"
      ],
      "name": "Bag",
      "created_by": {
        "username": "917827311650_22960",
        "uid": "123"
      },
      "company_id": 1,
      "created_on": "2021-02-19 16:21:35.091512",
      "modified_by": {
        "username": "917827311650_22960",
        "uid": "123"
      },
      "modified_on": "2021-02-19 16:21:35.091540",
      "id": "602f9837a596ce2edf9868e2"
    },
    {
      "slug": "bag",
      "is_active": true,
      "same_store_assignment": true,
      "meta": {},
      "choice": "multi",
      "logo": "http://g.com/poo.png/",
      "page_visibility": [
        "pdp"
      ],
      "name": "Bag",
      "products": [
        {
          "auto_select": false,
          "min_quantity": 1,
          "allow_remove": true,
          "auto_add_to_cart": false,
          "max_quantity": 1,
          "product_uid": 7500001
        }
      ],
      "created_by": {
        "username": "917827311650_22960",
        "uid": "123"
      },
      "company_id": 1,
      "created_on": "2021-02-19 16:20:24.605207",
      "modified_by": {
        "username": "917827311650_22960",
        "uid": "123"
      },
      "modified_on": "2021-02-19 16:20:24.605230",
      "id": "602f97f0a596ce2ead47cd0b"
    },
    {
      "products": [
        {
          "auto_select": false,
          "auto_add_to_cart": false,
          "min_quantity": 1,
          "allow_remove": true,
          "max_quantity": 1,
          "product_uid": 7500001
        }
      ],
      "is_active": true,
      "logo": "http://g.com/poo.png/",
      "name": "Bag",
      "choice": "multi",
      "slug": "bag",
      "same_store_assignment": true,
      "page_visibility": [
        "pdp"
      ],
      "meta": {},
      "created_by": {
        "username": "917827311650_22960",
        "uid": "123"
      },
      "company_id": 1,
      "created_on": "2021-02-19 16:16:46.196449",
      "modified_by": {
        "username": "917827311650_22960",
        "uid": "123"
      },
      "modified_on": "2021-02-19 16:16:46.196467",
      "id": "602f9716a596ce2e415196df"
    }
  ]
}
```
</details>









---


#### createProductBundle
Create Product Bundle




```kotlin
client.catalog.createProductBundle(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |  
| body | [ProductBundleRequest](#ProductBundleRequest) | yes | Request body |


Create Product Bundle. See `ProductBundleRequest` for the request body parameter need to create a product bundle. On successful request, returns in `ProductBundleRequest` with id

*Returned Response*




[GetProductBundleCreateResponse](#GetProductBundleCreateResponse)

Get bundle with id that is added. See example below or refer `GetProductBundleCreateResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "slug": "bag",
  "logo": "http://g.com/poo.png/",
  "name": "Bag",
  "choice": "multi",
  "products": [
    {
      "product_uid": 7500001,
      "max_quantity": 1,
      "min_quantity": 1,
      "auto_add_to_cart": false,
      "auto_select": false,
      "allow_remove": true
    }
  ],
  "meta": {},
  "same_store_assignment": true,
  "is_active": true,
  "page_visibility": [
    "pdp"
  ],
  "created_by": {
    "username": "917827311650_22960",
    "uid": "123"
  },
  "company_id": 1,
  "created_on": "2021-02-19 16:40:26.310007",
  "modified_by": {
    "username": "917827311650_22960",
    "uid": "123"
  },
  "modified_on": "2021-02-19 16:40:26.310027",
  "id": "602f9ca2a596ce312f5956f9"
}
```
</details>









---


#### getProductBundleDetail
Get a particular Product Bundle details




```kotlin
client.catalog.getProductBundleDetail(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| id | String | yes | A `id` is a unique identifier for a particular detail. Pass the `id` of the keywords which you want to retrieve. |  



Get a particular Bundle details by its `id`. If successful, returns a Product bundle resource in the response body specified in `GetProductBundleResponse`

*Returned Response*




[GetProductBundleResponse](#GetProductBundleResponse)

The Collection object. See example below or refer `GetProductBundleResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "slug": "bag",
  "company_id": 1,
  "logo": "http://g.com/poo.png/",
  "name": "Bag",
  "choice": "multi",
  "products": [
    {
      "product_uid": 7500001,
      "product_details": {
        "country_of_origin": "India",
        "slug": "slug-1",
        "item_code": "760B3BFF-4905-44B8-A50E-082829E7107F",
        "attributes": {
          "brand_name": "brand 2"
        },
        "name": "Some Phone",
        "images": [
          "https://hdn-1.addsale.com/x0/media/pictures/tagged_items/original/random_code_4/FE6DUR_000000.png"
        ],
        "uid": 7500001
      },
      "max_quantity": 1,
      "min_quantity": 1,
      "auto_add_to_cart": false,
      "auto_select": false,
      "allow_remove": true
    }
  ],
  "meta": {},
  "same_store_assignment": true,
  "page_visibility": [
    "pdp"
  ]
}
```
</details>









---


#### updateProductBundle
Update a Product Bundle




```kotlin
client.catalog.updateProductBundle(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| id | String | yes | A `id` is a unique identifier for a particular detail. Pass the `id` of the keywords which you want to delete. |  
| body | [ProductBundleUpdateRequest](#ProductBundleUpdateRequest) | yes | Request body |


Update a Product Bundle by its id. On successful request, returns the updated product bundle

*Returned Response*




[GetProductBundleCreateResponse](#GetProductBundleCreateResponse)

The Collection object. See example below or refer `GetProductBundleCreateResponse` for details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "slug": "bag",
  "logo": "http://g.com/poo.png/",
  "name": "Bag",
  "choice": "multi",
  "products": [
    {
      "product_uid": 7500001,
      "max_quantity": 1,
      "min_quantity": 1,
      "auto_add_to_cart": false,
      "auto_select": false,
      "allow_remove": true
    }
  ],
  "meta": {},
  "same_store_assignment": true,
  "is_active": true,
  "page_visibility": [
    "pdp"
  ],
  "created_by": {
    "username": "917827311650_22960",
    "uid": "123"
  },
  "company_id": 1,
  "created_on": "2021-02-19 16:40:26.310007",
  "modified_by": {
    "username": "917827311650_22960",
    "uid": "123"
  },
  "modified_on": "2021-02-19 16:40:26.310027",
  "id": "602f9ca2a596ce312f5956f9"
}
```
</details>









---


#### getSizeGuides
Get list of size guides




```kotlin
client.catalog.getSizeGuides(active: active, q: q, tag: tag, pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Id of the company for which the size guides are to be fetched. |   
| active | Boolean? | no | filter size guide on basis of active, in-active |   
| q | String? | no | Query that is to be searched. |   
| tag | String? | no | to filter size guide on basis of tag. |   
| pageNo | Int? | no | The page number to navigate through the given set of results |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 10. |  



This API allows to view all the size guides associated to the seller.

*Returned Response*




[ListSizeGuide](#ListSizeGuide)

Size guide object. See example below or refer `ListSizeGuide` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "modified_by": {
        "username": "silverbolt",
        "user_id": "-1"
      },
      "active": true,
      "id": "60364384f08385bee776f83d",
      "title": "Demo SG",
      "modified_on": "2021-02-24T17:46:04.146000Z",
      "brand_id": 2,
      "created_by": {
        "username": "silverbolt",
        "user_id": "-1"
      },
      "subtitle": "I am demo",
      "company_id": 12,
      "created_on": "2021-02-24T17:46:04.146000Z",
      "guide": {
        "meta": {
          "values": [
            {
              "col_1": "10",
              "col_2": "20"
            },
            {
              "col_1": "12",
              "col_2": "22"
            },
            {
              "col_1": "14",
              "col_2": "24"
            }
          ],
          "unit": "cm",
          "headers": {
            "col_1": {
              "value": "Head",
              "convertable": false
            },
            "col_2": {
              "value": "Shoulder",
              "convertable": true
            }
          }
        }
      },
      "tag": "demo",
      "name": "Demo"
    }
  ],
  "page": {
    "current": 1,
    "size": 1,
    "has_previous": false,
    "has_next": false,
    "item_count": 1
  }
}
```
</details>









---


#### createSizeGuide
Create a size guide.




```kotlin
client.catalog.createSizeGuide(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Id of the company inside which the size guide is to be created. |  
| body | [ValidateSizeGuide](#ValidateSizeGuide) | yes | Request body |


This API allows to create a size guide associated to a brand.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### getSizeGuide
Get a single size guide.




```kotlin
client.catalog.getSizeGuide(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Id of the company associated to size guide. |   
| id | String | yes | Id of the size guide to be viewed. |  



This API helps to get data associated to a size guide.

*Returned Response*




[SizeGuideResponse](#SizeGuideResponse)

Brand object. See example below or refer `SizeGuideResponseSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "active": true,
  "brand_id": 1,
  "created_on": "2021-02-24T17:46:04.146000Z",
  "modified_on": "2021-02-25T15:19:30.822000Z",
  "created_by": {
    "username": "silverbolt",
    "user_id": "-1"
  },
  "modified_by": {
    "username": "917827311650_22960",
    "user_id": "123"
  },
  "name": "edited size guide",
  "company_id": 1,
  "guide": {
    "meta": {
      "headers": {
        "col_1": {
          "value": "Head",
          "convertable": false
        },
        "col_2": {
          "value": "Shoulder",
          "convertable": true
        }
      },
      "values": [
        {
          "col_1": "10",
          "col_2": "20"
        },
        {
          "col_1": "12",
          "col_2": "22"
        },
        {
          "col_1": "14",
          "col_2": "24"
        }
      ],
      "unit": "cm"
    }
  },
  "tag": "demo",
  "title": "Demo SG",
  "subtitle": "I am demo",
  "id": "60364384f08385bee776f83d"
}
```
</details>









---


#### updateSizeGuide
Edit a size guide.




```kotlin
client.catalog.updateSizeGuide(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Id of the company. |   
| id | String | yes | Mongo id of the size guide to be edited |  
| body | [ValidateSizeGuide](#ValidateSizeGuide) | yes | Request body |


This API allows to edit a size guide.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### getCatalogConfiguration
Get configuration meta  details for catalog for admin panel




```kotlin
client.application("<APPLICATION_ID>").catalog.getCatalogConfiguration().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |  



configuration meta  details for catalog.

*Returned Response*




[GetCatalogConfigurationMetaData](#GetCatalogConfigurationMetaData)

configuration details for catalog. See example below or refer `GetCatalogConfigurationMetaDataSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getConfigurations
Get configured details for catalog




```kotlin
client.application("<APPLICATION_ID>").catalog.getConfigurations().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |  



configured details for catalog.

*Returned Response*




[GetAppCatalogConfiguration](#GetAppCatalogConfiguration)

Get application level configured catalog details. See example below or refer `GetAppCatalogConfigurationSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "data": {
    "app_id": "000000000000000000000001",
    "listing": {
      "filter": {
        "attribute_config": [
          {
            "key": "gender",
            "priority": 1,
            "type": "multivalued",
            "name": "Gender",
            "value_config": {
              "condition": "OR",
              "sort": "count",
              "value": "",
              "bucket_points": [],
              "map": {}
            },
            "is_active": true
          },
          {
            "key": "min_price_effective",
            "priority": 2,
            "type": "range",
            "name": "Price",
            "value_config": {
              "condition": "OR",
              "sort": "count",
              "value": "",
              "bucket_points": [],
              "map": {
                "< 500": "Below Rs. 500",
                ">= 6000": "Above Rs. 6000"
              }
            },
            "is_active": true
          },
          {
            "key": "departments",
            "priority": 3,
            "type": "multivalued",
            "name": "Department",
            "value_config": {
              "condition": "OR",
              "sort": "count",
              "value": "metadata",
              "bucket_points": [],
              "map": {}
            },
            "is_active": true
          },
          {
            "key": "brand_id",
            "priority": 4,
            "type": "multivalued",
            "name": "Brand",
            "value_config": {
              "condition": "OR",
              "sort": "ascending",
              "value": "metadata",
              "bucket_points": [],
              "map": {
                "5th Avenue": "A {{value}}"
              }
            },
            "is_active": true
          },
          {
            "key": "season",
            "priority": 5,
            "type": "multivalued",
            "name": "Season",
            "value_config": {
              "condition": "OR",
              "sort": "count",
              "value": "",
              "bucket_points": [],
              "map": {
                "": ""
              }
            },
            "is_active": false
          },
          {
            "key": "is_set",
            "priority": 6,
            "type": "multivalued",
            "name": "Set",
            "value_config": {
              "condition": "OR",
              "sort": "descending",
              "value": "",
              "bucket_points": [],
              "map": {
                "true": "Yes",
                "false": "No"
              }
            },
            "is_active": true
          },
          {
            "key": "rating",
            "priority": 7,
            "type": "multivalued",
            "name": "Rating",
            "value_config": {
              "condition": "OR",
              "sort": "count",
              "value": "",
              "bucket_points": [],
              "map": {
                "": ""
              }
            },
            "is_active": true
          },
          {
            "key": "size_depth",
            "priority": 8,
            "type": "range",
            "name": "Size Depth",
            "value_config": {
              "condition": "OR",
              "sort": "count",
              "value": "",
              "bucket_points": [],
              "map": {
                "{} - {}": "{} - {}"
              }
            },
            "is_active": true
          }
        ],
        "allow_single": false
      },
      "sort": {
        "default": "",
        "config": [
          {
            "key": "price_dsc",
            "logo": "https://hdn-1.fynd.com/global/menu-icons/Price%20High%20to%20Low.png",
            "priority": 1,
            "name": "Price High to Low",
            "is_active": false
          },
          {
            "key": "rating_dsc",
            "logo": "https://hdn-1.fynd.com/global/menu-icons/Rating.png",
            "priority": 2,
            "name": "Rating",
            "is_active": true
          },
          {
            "key": "depth_desc",
            "priority": 3,
            "name": "Size Depth (High to Low)",
            "is_active": true
          },
          {
            "key": "discount_dsc",
            "logo": "https://hdn-1.fynd.com/global/menu-icons/Discount%20Low%20to%20High.png",
            "priority": 4,
            "name": "Discount High to Low",
            "is_active": true
          },
          {
            "key": "popular",
            "logo": "https://hdn-1.fynd.com/global/menu-icons/Popularity.png",
            "priority": 5,
            "name": "Popularity",
            "is_active": true
          },
          {
            "key": "relevance",
            "priority": 6,
            "name": "Relevance",
            "is_active": true
          },
          {
            "key": "price_asc",
            "logo": "https://hdn-1.fynd.com/global/menu-icons/Price%20Low%20to%20High.png",
            "priority": 7,
            "name": "Price Low to High",
            "is_active": true
          }
        ]
      }
    },
    "product": {
      "similar": {
        "config": [
          {
            "key": "seller",
            "size": {
              "max": 10,
              "min": 2
            },
            "priority": 1,
            "title": "Seller",
            "is_active": true,
            "subtitle": ""
          },
          {
            "key": "visual",
            "size": {
              "max": 10,
              "min": 2
            },
            "priority": 2,
            "title": "Visual",
            "is_active": true,
            "subtitle": ""
          },
          {
            "key": "brand",
            "size": {
              "max": 10,
              "min": 2
            },
            "priority": 3,
            "title": "Brand",
            "is_active": true,
            "subtitle": ""
          },
          {
            "key": "specs",
            "size": {
              "max": 10,
              "min": 2
            },
            "priority": 4,
            "title": "Specs",
            "is_active": true,
            "subtitle": ""
          }
        ]
      },
      "variant": {
        "config": [
          {
            "key": "color",
            "display_type": "image",
            "size": {
              "max": 10,
              "min": 2
            },
            "priority": 1,
            "name": "Additional Colors12",
            "is_active": true
          },
          {
            "key": "storage",
            "display_type": "text",
            "size": {
              "max": 10,
              "min": 2
            },
            "priority": 2,
            "name": "Memory",
            "is_active": true
          },
          {
            "key": "visual",
            "display_type": "image",
            "size": {
              "max": 10,
              "min": 2
            },
            "priority": 3,
            "name": "Additional Colors",
            "is_active": true
          },
          {
            "key": "ram_storage",
            "display_type": "text",
            "size": {
              "max": 10,
              "min": 2
            },
            "priority": 4,
            "name": "Ram_Storage",
            "is_active": true
          },
          {
            "key": "shade",
            "display_type": "color",
            "size": {
              "max": 10,
              "min": 2
            },
            "priority": 5,
            "name": "Additional Shades",
            "is_active": true
          },
          {
            "key": "water_resistant",
            "display_type": "text",
            "size": {
              "max": 10,
              "min": 2
            },
            "priority": 6,
            "name": "Water_Resistant",
            "is_active": true
          }
        ]
      }
    },
    "config_id": "000000000000000000000001",
    "config_type": "app"
  },
  "is_default": false
}
```
</details>









---


#### createConfigurationProductListing
Add configuration for products & listings




```kotlin
client.application("<APPLICATION_ID>").catalog.createConfigurationProductListing(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |  
| body | [AppConfiguration](#AppConfiguration) | yes | Request body |


Add configuration for products & listing.

*Returned Response*




[GetAppCatalogConfiguration](#GetAppCatalogConfiguration)

success flag will tell whether the operation was successful.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getConfigurationByType
Get configured details for catalog




```kotlin
client.application("<APPLICATION_ID>").catalog.getConfigurationByType(type: type).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| type | String | yes | type can be brands, categories etc. |  



configured details for catalog.

*Returned Response*




[GetAppCatalogEntityConfiguration](#GetAppCatalogEntityConfiguration)

Get application level configured catalog details. See example below or refer `GetAppCatalogEntityConfigurationSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### createConfigurationByType
Add configuration for categories and brands




```kotlin
client.application("<APPLICATION_ID>").catalog.createConfigurationByType(type: type, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| type | String | yes | type can be brands, categories etc. |  
| body | [AppConfiguration](#AppConfiguration) | yes | Request body |


Add configuration for categories & brands.

*Returned Response*




[GetAppCatalogConfiguration](#GetAppCatalogConfiguration)

success flag will tell whether the operation was successful.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getQueryFilters
Get query filters to configure a collection




```kotlin
client.application("<APPLICATION_ID>").catalog.getQueryFilters().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |  



Get query filters to configure a collection

*Returned Response*




[GetCollectionQueryOptionResponse](#GetCollectionQueryOptionResponse)

The attached items of an collection. See example below or refer `GetCollectionQueryOptionResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "filters": [
    {
      "key": {
        "display": "Department",
        "name": "department",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Department.png"
      },
      "values": [
        {
          "display": "Men's Fashion",
          "count": 2113,
          "is_selected": false,
          "value": "men",
          "logo": {
            "type": "image",
            "url": "https://hdn-1.fynd.com/media/category_tab_icons/department/Men.png"
          }
        }
      ]
    },
    {
      "key": {
        "display": "Category",
        "name": "category",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Category.png"
      },
      "values": [
        {
          "display": "T-Shirts",
          "count": 968,
          "is_selected": false,
          "value": "192",
          "logo": "https://hdn-1.fynd.com/media/logo/category/original/15442_57fdc97abfd248aaaf8841f097a4ed67.jpg"
        }
      ]
    },
    {
      "key": {
        "display": "Size",
        "name": "sizes",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Sizes.png"
      },
      "values": [
        {
          "display": "S",
          "count": 1438,
          "is_selected": false,
          "value": "S"
        }
      ]
    },
    {
      "key": {
        "display": "Brand",
        "name": "brand",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Brand%20ID.png"
      },
      "values": [
        {
          "display": "Superdry",
          "count": 4263,
          "is_selected": false,
          "value": "235",
          "logo": "https://hdn-1.fynd.com/media/logo/brand/original/1008_238113b8e11448f792e9bf860aac30f2.jpg"
        }
      ]
    },
    {
      "key": {
        "display": "Rating",
        "name": "rating",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Rating.png"
      },
      "values": [
        {
          "count": 3,
          "display": "5 ★",
          "value": "[4 TO *}",
          "is_selected": false
        }
      ]
    },
    {
      "key": {
        "display": "Company",
        "name": "company_id_list",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Store%20ID%20List.png"
      },
      "values": [
        {
          "display": "RELIANCE BRANDS LIMITED",
          "count": 4262,
          "is_selected": false,
          "value": "46"
        }
      ]
    },
    {
      "key": {
        "display": "Store Ids",
        "name": "store_id_list",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Store%20ID%20List.png"
      },
      "values": [
        {
          "display": "PHOENIX, ,PALLADIUM,  LOWER PAREL - 5410",
          "count": 1385,
          "is_selected": false,
          "value": "2201"
        }
      ]
    },
    {
      "key": {
        "display": "Image",
        "name": "image_nature",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/image%20Nature.png"
      },
      "values": [
        {
          "display": "Good Quality",
          "count": 3111,
          "is_selected": false,
          "value": "standard"
        },
        {
          "display": "No Image",
          "count": 1152,
          "is_selected": false,
          "value": "default"
        }
      ]
    },
    {
      "key": {
        "display": "Set",
        "name": "is_set",
        "kind": "multivalued",
        "logo": ""
      },
      "values": [
        {
          "display": "No",
          "count": 4263,
          "is_selected": false,
          "value": false
        }
      ]
    },
    {
      "key": {
        "display": "Product Fit",
        "name": "product_fit",
        "kind": "multivalued",
        "logo": ""
      },
      "values": [
        {
          "display": "Regular",
          "count": 14,
          "is_selected": false,
          "value": "Regular"
        }
      ]
    },
    {
      "key": {
        "display": "Primary Material",
        "name": "primary_material",
        "kind": "multivalued",
        "logo": ""
      },
      "values": [
        {
          "display": "Cotton",
          "count": 1246,
          "is_selected": false,
          "value": "Cotton"
        }
      ]
    },
    {
      "key": {
        "display": "Gender",
        "name": "gender",
        "kind": "multivalued",
        "logo": ""
      },
      "values": [
        {
          "display": "Men",
          "count": 2125,
          "is_selected": false,
          "value": "Men"
        },
        {
          "display": "Women",
          "count": 1492,
          "is_selected": false,
          "value": "Women"
        }
      ]
    },
    {
      "key": {
        "display": "Primary Colour",
        "name": "primary_color",
        "kind": "multivalued",
        "logo": ""
      },
      "values": [
        {
          "display": "Multi",
          "count": 1403,
          "is_selected": false,
          "value": "Multi"
        }
      ]
    },
    {
      "key": {
        "display": "Size Depth",
        "name": "size_depth",
        "kind": "range",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Size%20Depth.png"
      },
      "values": [
        {
          "count": 4263,
          "min": 0,
          "max": 9,
          "is_selected": false,
          "selected_min": 0,
          "selected_max": 9,
          "query_format": "[{} TO {}]",
          "display_format": "{} - {}",
          "display": "0 - 9"
        }
      ]
    },
    {
      "key": {
        "display": "Price",
        "name": "min_price_effective",
        "kind": "range",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Min%20price%20effective.png"
      },
      "values": [
        {
          "count": 4263,
          "min": 398,
          "max": 24999,
          "is_selected": false,
          "selected_min": 398.8,
          "selected_max": 24998.77,
          "currency_code": "INR",
          "currency_symbol": "₹",
          "query_format": "[{},INR TO {},INR]"
        }
      ]
    },
    {
      "key": {
        "display": "Discount",
        "name": "platform_discount",
        "kind": "range",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Platform%20Discount.png"
      },
      "values": [
        {
          "count": 4263,
          "min": 0,
          "max": 50,
          "is_selected": false,
          "selected_min": 0,
          "selected_max": 50,
          "query_format": "[{} TO {}]",
          "display_format": "{} - {}",
          "display": "0 - 50"
        }
      ]
    }
  ],
  "sort_on": [
    {
      "display": "Latest Products",
      "name": "Latest Products",
      "logo": "https://hdn-1.fynd.com/global/menu-icons/Latest%20Products.png",
      "value": "latest",
      "is_selected": true
    },
    {
      "display": "Popularity",
      "name": "Popularity",
      "logo": "https://hdn-1.fynd.com/global/menu-icons/Popularity.png",
      "value": "popular",
      "is_selected": false
    },
    {
      "display": "Price Low to High",
      "name": "Price Low to High",
      "logo": "https://hdn-1.fynd.com/global/menu-icons/Price%20High%20to%20Low.png",
      "value": "price_asc",
      "is_selected": false
    },
    {
      "display": "Price High to Low",
      "name": "Price High to Low",
      "logo": "https://hdn-1.fynd.com/global/menu-icons/Price%20High%20to%20Low.png",
      "value": "price_dsc",
      "is_selected": false
    },
    {
      "display": "Discount Low to High",
      "name": "Discount Low to High",
      "logo": "https://hdn-1.fynd.com/global/menu-icons/Discount%20Low%20to%20High.png",
      "value": "discount_asc",
      "is_selected": false
    },
    {
      "display": "Discount High to Low",
      "name": "Discount High to Low",
      "logo": "https://hdn-1.fynd.com/global/menu-icons/Discount%20Low%20to%20High.png",
      "value": "discount_dsc",
      "is_selected": false
    },
    {
      "display": "Rating",
      "name": "Rating",
      "logo": "https://hdn-1.fynd.com/global/menu-icons/Rating.png",
      "value": "rating_dsc",
      "is_selected": false
    },
    {
      "display": "Size Depth (High to Low)",
      "name": "Size Depth (High to Low)",
      "logo": "https://hdn-1.fynd.com/global/menu-icons/Size%20Depth.png",
      "value": "depth_desc",
      "is_selected": false
    }
  ]
}
```
</details>









---


#### getAllCollections
List all the collections




```kotlin
client.application("<APPLICATION_ID>").catalog.getAllCollections().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |  



A Collection allows you to organize your products into hierarchical groups. For example, a dress might be in the category _Clothing_, the individual product might also be in the collection _Summer_. On successful request, returns all the collections as specified in `CollectionListingSchema`

*Returned Response*




[GetCollectionListingResponse](#GetCollectionListingResponse)

List of collections. See example below or refer `GetCollectionListingResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {
    "current": 1,
    "size": 19,
    "has_previous": false,
    "has_next": true,
    "item_total": 190
  },
  "items": [
    {
      "uid": "6040fed076d8a500011ef829",
      "type": "query",
      "query": {
        "brand": [
          "6",
          "3",
          "4",
          "2"
        ],
        "min_price_effective": "[6319,INR TO 11805,INR]",
        "platform_discount": "[15 TO 39]",
        "sort_on": "price_asc"
      },
      "name": "test1",
      "banners": {
        "portrait": {
          "type": "image",
          "url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000001/collections/pictures/portrait-banner/original/mP6OnINGR-1601466767814.jpeg"
        },
        "landscape": {
          "type": "image",
          "url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000001/collections/pictures/landscape-banner/original/3jSEzw9CN-1601465376892.jpeg"
        }
      },
      "logo": {
        "type": "image",
        "url": "https://hdn-1.addsale.com/x0/company/1/applications/000000000000000000000001/collections/pictures/square-logo/original/y_-XUYXwx-1602326103322.jpeg"
      },
      "published": true,
      "description": "this is description",
      "is_active": true,
      "tags": [],
      "slug": "test1",
      "action": {
        "page": {
          "type": "collection",
          "query": {
            "collection": [
              "test1"
            ]
          }
        },
        "type": "page"
      },
      "allow_facets": true,
      "allow_sort": true,
      "visible_facets_keys": [],
      "meta": {},
      "badge": {
        "text": "",
        "color": "#ffffff"
      },
      "sort_on": "price_asc",
      "_custom_json": {},
      "_locale_language": {},
      "_schedule": {
        "start": "2021-03-04T15:35:13.640000Z",
        "next_schedule": [
          {
            "start": "2021-03-04T15:35:13.640000Z",
            "end": null
          }
        ],
        "end": null
      }
    },
    {
      "uid": "6040a9b250f97e0001886294",
      "type": "items",
      "query": {},
      "name": "newapiplaform",
      "banners": {
        "portrait": {
          "type": "image",
          "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588858137/production/applications/app_000000000000000000000001/media/collection/portrait/xzuftshmmw4yuwzb12pm.png"
        },
        "landscape": {
          "type": "image",
          "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588857999/production/applications/app_000000000000000000000001/media/collection/landscape/avm7xibo2jgk8glc4bwl.png"
        }
      },
      "logo": {
        "type": "image",
        "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588857854/production/applications/app_000000000000000000000001/media/collection/logo/w9ns7nfgv7fk45xqrpoh.png"
      },
      "published": true,
      "description": "sadasd",
      "is_active": true,
      "tags": [
        "sdsadas",
        "asd"
      ],
      "slug": "newapiplaform",
      "action": {
        "page": {
          "type": "collection",
          "query": {
            "collection": [
              "newapiplaform"
            ]
          }
        },
        "type": "page"
      },
      "allow_facets": true,
      "allow_sort": true,
      "visible_facets_keys": [],
      "meta": {},
      "badge": {
        "text": "",
        "color": "#aa2727"
      },
      "sort_on": "popular",
      "_custom_json": {},
      "_locale_language": {},
      "_schedule": {
        "start": "2021-03-04T09:33:53.686000Z",
        "next_schedule": [
          {
            "start": "2021-03-04T09:33:53.686000Z",
            "end": null
          }
        ],
        "end": null
      }
    },
    {
      "uid": "603f68fd953a69000145dc92",
      "type": "query",
      "query": {},
      "name": "new",
      "banners": {
        "portrait": {
          "type": "image",
          "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588858137/production/applications/app_000000000000000000000001/media/collection/portrait/xzuftshmmw4yuwzb12pm.png"
        },
        "landscape": {
          "type": "image",
          "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588857999/production/applications/app_000000000000000000000001/media/collection/landscape/avm7xibo2jgk8glc4bwl.png"
        }
      },
      "logo": {
        "type": "image",
        "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588857854/production/applications/app_000000000000000000000001/media/collection/logo/w9ns7nfgv7fk45xqrpoh.png"
      },
      "published": true,
      "description": "",
      "is_active": true,
      "tags": [],
      "slug": "old",
      "action": {
        "page": {
          "type": "collection",
          "query": {
            "collection": [
              "old"
            ]
          }
        },
        "type": "page"
      },
      "allow_facets": true,
      "allow_sort": true,
      "visible_facets_keys": [],
      "meta": {},
      "badge": {
        "color": "#ffffff",
        "text": ""
      },
      "sort_on": "popular",
      "_custom_json": {},
      "_locale_language": {},
      "_schedule": {
        "start": "2021-03-03T10:45:40.544000Z",
        "next_schedule": [
          {
            "start": "2021-03-03T10:45:40.544000Z",
            "end": null
          }
        ],
        "end": null
      }
    }
  ],
  "filters": {
    "tags": [
      {
        "name": "1+",
        "is_selected": false,
        "display": "1+"
      },
      {
        "name": "aa",
        "is_selected": false,
        "display": "aa"
      },
      {
        "name": "asd",
        "is_selected": false,
        "display": "asd"
      },
      {
        "name": "dda",
        "is_selected": false,
        "display": "dda"
      },
      {
        "name": "fahim",
        "is_selected": false,
        "display": "fahim"
      },
      {
        "name": "gfg",
        "is_selected": false,
        "display": "gfg"
      },
      {
        "name": "sakri",
        "is_selected": false,
        "display": "sakri"
      },
      {
        "name": "sdsadas",
        "is_selected": false,
        "display": "sdsadas"
      },
      {
        "name": "uuy",
        "is_selected": false,
        "display": "uuy"
      }
    ],
    "type": [
      {
        "name": "items",
        "is_selected": false,
        "display": "items"
      },
      {
        "name": "query",
        "is_selected": false,
        "display": "query"
      }
    ]
  }
}
```
</details>









---


#### createCollection
Add a Collection




```kotlin
client.application("<APPLICATION_ID>").catalog.createCollection(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |  
| body | [CreateCollection](#CreateCollection) | yes | Request body |


Create a collection. See `CreateCollectionRequestSchema` for the list of attributes needed to create a collection and collections/query-options for the available options to create a collection. On successful request, returns a paginated list of collections specified in `CollectionCreateResponse`

*Returned Response*




[CollectionCreateResponse](#CollectionCreateResponse)

List of all the collections including the one you added. See example below or refer `CollectionCreateResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "uid": "604f585a7051e30001173ac1",
  "type": "query",
  "query": {},
  "name": "New",
  "banners": {
    "portrait": {
      "type": "image",
      "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588858137/production/applications/app_000000000000000000000001/media/collection/portrait/xzuftshmmw4yuwzb12pm.png"
    },
    "landscape": {
      "type": "image",
      "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588857999/production/applications/app_000000000000000000000001/media/collection/landscape/avm7xibo2jgk8glc4bwl.png"
    }
  },
  "logo": {
    "type": "image",
    "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588857854/production/applications/app_000000000000000000000001/media/collection/logo/w9ns7nfgv7fk45xqrpoh.png"
  },
  "published": true,
  "description": "",
  "is_active": true,
  "tags": [],
  "slug": "new",
  "action": {
    "page": {
      "type": "collection",
      "query": {
        "collection": [
          "new"
        ]
      }
    },
    "type": "page"
  },
  "allow_facets": true,
  "allow_sort": true,
  "visible_facets_keys": [],
  "meta": {},
  "badge": {
    "color": "#ffffff",
    "text": ""
  },
  "sort_on": "depth_desc",
  "_custom_json": {},
  "_locale_language": {},
  "_schedule": {
    "start": "2021-03-15T12:51:21.333000+00:00Z",
    "next_schedule": [
      {
        "start": "2021-03-15T12:51:21.333000+00:00Z",
        "end": null
      }
    ],
    "end": null
  },
  "seo": {
    "title": "Test",
    "description": "Test description"
  }
}
```
</details>









---


#### getCollectionDetail
Get a particular collection




```kotlin
client.application("<APPLICATION_ID>").catalog.getCollectionDetail(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| slug | String | yes | A `slug` is a human readable, URL friendly unique identifier of an object. Pass the `slug` of the collection which you want to retrieve. |  



Get the details of a collection by its `slug`. If successful, returns a Collection resource in the response body specified in `CollectionDetailResponse`

*Returned Response*




[CollectionDetailResponse](#CollectionDetailResponse)

The Collection object. See example below or refer `CollectionDetailResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "uid": "5ec5fc757cb1e4740a17da23",
  "type": "query",
  "query": {
    "l3_categories": [
      "12"
    ],
    "sort_on": "discount_asc"
  },
  "name": "new",
  "banners": {
    "portrait": {
      "type": "image",
      "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588858137/production/applications/app_000000000000000000000001/media/collection/portrait/xzuftshmmw4yuwzb12pm.png"
    },
    "landscape": {
      "type": "image",
      "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588857999/production/applications/app_000000000000000000000001/media/collection/landscape/avm7xibo2jgk8glc4bwl.png"
    }
  },
  "logo": {
    "type": "image",
    "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588857854/production/applications/app_000000000000000000000001/media/collection/logo/w9ns7nfgv7fk45xqrpoh.png"
  },
  "published": true,
  "description": "",
  "is_active": true,
  "tags": [],
  "slug": "new",
  "action": {
    "page": {
      "type": "collection",
      "query": {
        "collection": [
          "new"
        ]
      }
    },
    "type": "page"
  },
  "allow_facets": true,
  "allow_sort": true,
  "visible_facets_keys": [],
  "meta": {},
  "badge": {
    "color": "#ffffff",
    "text": ""
  },
  "sort_on": "popular",
  "_custom_json": {},
  "_locale_language": {},
  "_schedule": {
    "start": "2020-05-21T03:58:41.237000Z",
    "next_schedule": [
      {
        "start": "2020-05-21T03:58:41.237000Z",
        "end": null
      }
    ],
    "end": null
  }
}
```
</details>









---


#### deleteCollection
Delete a Collection




```kotlin
client.application("<APPLICATION_ID>").catalog.deleteCollection(id: id).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| id | String | yes | A `id` is a unique identifier of a collection. |  



Delete a collection by it's id. Returns an object that tells whether the collection was deleted successfully

*Returned Response*




[DeleteResponse](#DeleteResponse)

Status object. Tells whether the operation was successful. See example below or refer `DeleteResponse`




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "message": "Collection Deleted"
}
```
</details>









---


#### updateCollection
Update a collection




```kotlin
client.application("<APPLICATION_ID>").catalog.updateCollection(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| id | String | yes | A `id` is a unique identifier of a collection. |  
| body | [UpdateCollection](#UpdateCollection) | yes | Request body |


Update a collection by it's id. On successful request, returns the updated collection

*Returned Response*




[UpdateCollection](#UpdateCollection)

The Collection object. See example below or refer `UpdateCollectionSchema` for details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "uid": "604f585a7051e30001173ac1",
  "type": "query",
  "query": {},
  "name": "New",
  "banners": {
    "portrait": {
      "type": "image",
      "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588858137/production/applications/app_000000000000000000000001/media/collection/portrait/xzuftshmmw4yuwzb12pm.png"
    },
    "landscape": {
      "type": "image",
      "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588857999/production/applications/app_000000000000000000000001/media/collection/landscape/avm7xibo2jgk8glc4bwl.png"
    }
  },
  "logo": {
    "type": "image",
    "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1588857854/production/applications/app_000000000000000000000001/media/collection/logo/w9ns7nfgv7fk45xqrpoh.png"
  },
  "published": true,
  "description": "",
  "is_active": true,
  "tags": [],
  "slug": "new",
  "action": {
    "page": {
      "type": "collection",
      "query": {
        "collection": [
          "new"
        ]
      }
    },
    "type": "page"
  },
  "allow_facets": true,
  "allow_sort": true,
  "visible_facets_keys": [],
  "meta": {},
  "badge": {
    "color": "#ffffff",
    "text": ""
  },
  "sort_on": "depth_desc",
  "_custom_json": {},
  "_locale_language": {},
  "_schedule": {
    "start": "2021-03-15T12:51:21.333000+00:00Z",
    "next_schedule": [
      {
        "start": "2021-03-15T12:51:21.333000+00:00Z",
        "end": null
      }
    ],
    "end": null
  },
  "seo": {
    "title": "Test",
    "description": "Test description"
  }
}
```
</details>









---


#### getCollectionItems
Get the items for a collection




```kotlin
client.application("<APPLICATION_ID>").catalog.getCollectionItems(id: id, sortOn: sortOn, pageId: pageId, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| id | String | yes | A `id` is a unique identifier of a collection. |   
| sortOn | String? | no | Each response will contain sort_on param, which should be sent back to make pagination work. |   
| pageId | String? | no | Each response will contain next_id param, which should be sent back to make pagination work. |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 12. |  



Get items from a collection specified by its `id`.

*Returned Response*




[GetCollectionItemsResponse](#GetCollectionItemsResponse)

The attached items of an collection. See example below or refer `GetCollectionItemsResponseSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### addCollectionItems
Add items to a collection




```kotlin
client.application("<APPLICATION_ID>").catalog.addCollectionItems(id: id, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| id | String | yes | A `id` is a unique identifier of a collection. |  
| body | [CollectionItemRequest](#CollectionItemRequest) | yes | Request body |


Adds items to a collection specified by its `id`. See `CollectionItemRequest` for the list of attributes needed to add items to an collection.

*Returned Response*




[UpdatedResponse](#UpdatedResponse)

Status object. Tells whether the operation was successful.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "message": "items updated"
}
```
</details>









---


#### getCatalogInsights
Analytics data of catalog and inventory.




```kotlin
client.application("<APPLICATION_ID>").catalog.getCatalogInsights(brand: brand).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| brand | String? | no | Brand slug |  



Catalog Insights api returns the count of catalog related data like products, brands, departments and categories that have been made live as per configuration of the app.

*Returned Response*




[CatalogInsightResponse](#CatalogInsightResponse)

Response Data




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "item": {
    "count": 637707,
    "out_of_stock_count": 452806,
    "sellable_count": 184901
  }
}
```
</details>









---


#### getSellerInsights
Analytics data of catalog and inventory that are being cross-selled.




```kotlin
client.catalog.getSellerInsights(sellerAppId: sellerAppId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| sellerAppId | String | yes | Id of the seller application which is serving the invetory/catalog of the company |  



Analytics data of catalog and inventory that are being cross-selled.

*Returned Response*




[CrossSellingResponse](#CrossSellingResponse)

Response Data




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "products": 18,
  "articles": 18
}
```
</details>









---


#### createMarketplaceOptin
Create/Update opt-in infomation.




```kotlin
client.catalog.createMarketplaceOptin(marketplace: marketplace, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | The company id for which the detail needs to be retrieved. |   
| marketplace | String | yes | The marketplace for which the detail needs to be retrieved. |  
| body | [OptInPostRequest](#OptInPostRequest) | yes | Request body |


Use this API to create/update opt-in information for given platform. If successful, returns data in the response body as specified in `OptInPostResponseSchema`

*Returned Response*




[UpdatedResponse](#UpdatedResponse)

See example below or refer `UpdatedResponse` for details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getMarketplaceOptinDetail
Get opt-in infomation.




```kotlin
client.catalog.getMarketplaceOptinDetail().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes |  |  



Use this API to fetch opt-in information for all the platforms. If successful, returns a logs in the response body as specified in `GetOptInPlatformSchema`

*Returned Response*




[GetOptInPlatform](#GetOptInPlatform)

See example below or refer `GetOptInPlatformSchema` for details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getCompanyDetail
Get the Company details.




```kotlin
client.catalog.getCompanyDetail().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | The company id for which the detail needs to be retrieved. |  



Get the details of the company associated with the given company_id passed.

*Returned Response*




[OptinCompanyDetail](#OptinCompanyDetail)

See example below or refer `OptinCompanyDetailSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getCompanyBrandDetail
Get the Company Brand details of Optin.




```kotlin
client.catalog.getCompanyBrandDetail(isActive: isActive, q: q, pageNo: pageNo, pageSize: pageSize, marketplace: marketplace).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | The company id for which the detail needs to be retrieved. |   
| isActive | Boolean? | no | The is_active status for the optin id. |   
| q | Boolean? | no | The search value to filter the list. |   
| pageNo | Int? | no | The number of page for the company id. |   
| pageSize | Int? | no | Number of records that can be seen on the page for the company id. |   
| marketplace | String? | no | The marketplace platform associated with the company id. |  



Get the details of the Brands associated with the given company_id passed.

*Returned Response*




[OptinCompanyBrandDetailsView](#OptinCompanyBrandDetailsView)

See example below or refer `OptinCompanyBrandDetailsView` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getCompanyMetrics
Get the Company metrics




```kotlin
client.catalog.getCompanyMetrics().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | The company id for which the detail needs to be retrieved. |  



Get the Company metrics associated with the company ID passed.

*Returned Response*




[OptinCompanyMetrics](#OptinCompanyMetrics)

See example below or refer `OptinCompanyMetrics` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getStoreDetail
Get the Store details.




```kotlin
client.catalog.getStoreDetail(q: q, pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | The company id for which the detail needs to be retrieved. |   
| q | String? | no | The search related the store for the company id. |   
| pageNo | Int? | no | The number of page for the company id. |   
| pageSize | Int? | no | Number of records that can be seen on the page for the company id. |  



Get the details of the store associated with the company ID passed.

*Returned Response*




[OptinStoreDetails](#OptinStoreDetails)

See example below or refer `OptinStoreDetailsSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getGenderAttribute
Get gender attribute details




```kotlin
client.catalog.getGenderAttribute(attributeSlug: attributeSlug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | company for which you want to view the genders |   
| attributeSlug | String | yes | slug of the attribute for which you want to view the genders |  



This API allows to view the gender attribute details.

*Returned Response*




[GenderDetail](#GenderDetail)

Size guide object. See example below or refer `GenderDetailSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "description": "Clothing department needs gener attribute",
  "schema": {
    "format": "",
    "mandatory": false,
    "multi": true,
    "enum": [
      "Men",
      "Women",
      "Boy",
      "Girl",
      "more",
      "men"
    ],
    "type": "str"
  },
  "meta": {
    "enriched": false,
    "mandatory_details": {
      "l3_keys": []
    }
  },
  "slug": "gender",
  "name": "Gender",
  "enabled_for_end_consumer": true,
  "details": {
    "display_type": "text"
  },
  "is_nested": true,
  "filters": {
    "indexing": true,
    "priority": 2
  },
  "departments": [
    "men-s-fashion",
    "kids",
    "women-s-fashion",
    "beauty-personal-care"
  ],
  "logo": "https://hdn-1.addsale.com/x0/products/pictures/attribute/logo/original/Rhv89tqRo-brand-website-logo.png",
  "id": "5ed11eb0be8d5e00016f0335"
}
```
</details>









---


#### listProductTemplateCategories
List Department specifiec product categories




```kotlin
client.catalog.listProductTemplateCategories(departments: departments, itemType: itemType).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| departments | String | yes | A `department` is name of a departments whose category needs to be listed. Can specify multiple departments. |   
| itemType | String | yes | An `item_type` is the type of item, it can be `set`, `standard`, `digital`, etc. |  



Allows you to list all product categories values for the departments specified

*Returned Response*




[ProdcutTemplateCategoriesResponse](#ProdcutTemplateCategoriesResponse)

List of all categories attached to departments specified. See example below or refer `ProdcutTemplateCategoriesResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {},
  "items": []
}
```
</details>









---


#### listDepartmentsData
List all Departments




```kotlin
client.catalog.listDepartmentsData(pageNo: pageNo, pageSize: pageSize, name: name, search: search, isActive: isActive).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| pageNo | Int? | no | The page number to navigate through the given set of results |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 10. |   
| name | String? | no | Can search departments by passing name. |   
| search | String? | no | Can search departments by passing name of the department in search parameter. |   
| isActive | Boolean? | no | Can query for departments based on whether they are active or inactive. |  



Allows you to list all departments, also can search using name and filter active and incative departments, and item type

*Returned Response*




[DepartmentsResponse](#DepartmentsResponse)

List of departments data. See example below or refer `DepartmentsResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {
    "current": 1,
    "size": 1,
    "has_previous": false,
    "has_next": false,
    "item_total": 12
  },
  "items": [
    {
      "uid": 5,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "created_on": "2020-07-01T05:33:39.325000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/BSQ9Gk_123522-best-starry-sky-wallpaper-1920x1200-ipad-pro.jpgc7d0c15c-c1ff-47eb-8423-6e2df51f2ddf/BSQ9Gk_123522-best-starry-sky-wallpaper-1920x1200-ipad-pro.jpg",
      "modified_by": {
        "username": "917753852478_51632",
        "user_id": "5677"
      },
      "modified_on": "2021-03-03T15:55:25.118000Z",
      "name": "Sample Dept",
      "platforms": {},
      "priority_order": 111,
      "slug": "sample-dept",
      "synonyms": [
        "test",
        "sampe"
      ],
      "tags": [],
      "id": "5efc2033623d390001782238"
    },
    {
      "uid": 2,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "app@fynd.com",
        "user_id": "0"
      },
      "created_on": "2020-05-19T06:53:37.629000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/addsale/media/logo/department/original/15974_381e2236c2a348cc851c29a5d05c66a9.png",
      "modified_by": {
        "user_id": "10",
        "username": "fahimsakri_gofynd_com_44938"
      },
      "modified_on": "2021-03-04T14:01:02.556000Z",
      "name": "Men's Fashion",
      "platforms": {
        "fynd": true,
        "fynd_store": true,
        "marketplace": true,
        "openapi": true,
        "uniket_store": true,
        "uniket_wholesale": true
      },
      "priority_order": 111,
      "slug": "men-s-fashion",
      "synonyms": [],
      "tags": [],
      "id": "5ec3827156a7200001c9aeea"
    },
    {
      "uid": 4,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "fahimsakri_gofynd_com_44938",
        "user_id": "10"
      },
      "created_on": "2020-06-29T10:59:33.620000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/ywPVrU_preview_a637ca6e4da6e38f03eb0d650ac5d6ba.jpgc73cc22f-b5ee-4fd4-a585-8ada35762d68/ywPVrU_preview_a637ca6e4da6e38f03eb0d650ac5d6ba.jpg",
      "modified_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "modified_on": "2020-08-06T18:08:02.675000Z",
      "name": "Groceries",
      "platforms": {},
      "priority_order": 10,
      "slug": "groceries",
      "synonyms": [],
      "tags": [],
      "id": "5ef9c9959b04f00001e40dba"
    },
    {
      "uid": 1,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "app@fynd.com",
        "user_id": "0"
      },
      "created_on": "2020-05-18T16:14:41.689000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/platform/pictures/free-logo/original/_G1Z2Fg1L-http:d3p8ifzkmzds37.cloudfront.netmedialogodepartmentoriginal15870_c287d3c2431a432bb0e49363ef6b82bc.png.png",
      "modified_by": {
        "user_id": "5677",
        "username": "917753852478_51632"
      },
      "modified_on": "2021-03-04T15:39:38.528000Z",
      "name": "Electronics",
      "platforms": {
        "fynd": true,
        "fynd_store": true,
        "marketplace": true,
        "openapi": true,
        "uniket_store": true,
        "uniket_wholesale": true
      },
      "priority_order": 100,
      "slug": "electronics",
      "synonyms": [],
      "tags": [],
      "id": "5ec2b471661a4100019fca0d"
    },
    {
      "uid": 3,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "created_on": "2020-05-27T12:04:19.111000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/landscape-banner/original/g2plam_logo_Jio.pngeeb392ca-3958-46a0-9f13-23c205b596f7/g2plam_logo_Jio.png",
      "modified_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "modified_on": "2020-08-06T18:07:46.060000Z",
      "name": "Industrial Supplies",
      "platforms": {},
      "priority_order": 111,
      "slug": "industrial-supplies",
      "synonyms": [],
      "tags": [],
      "id": "5ece5743cd1bae0001440427"
    },
    {
      "uid": 6,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "abhinavsrivastava_gofynd_com_05674",
        "user_id": "13"
      },
      "created_on": "2020-07-06T07:56:01.508000Z",
      "is_active": false,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/wTcfEi_crysis_-_1.jpg14580947-a659-486d-b2d3-d2ca025b1cac/wTcfEi_crysis_-_1.jpg",
      "modified_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "modified_on": "2020-08-06T18:08:12.576000Z",
      "name": "Clothing",
      "platforms": {},
      "priority_order": 1,
      "slug": "clothing",
      "synonyms": [],
      "tags": [],
      "id": "5f02d9116b0ae500018923dd"
    },
    {
      "uid": 8,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "created_on": "2020-08-05T09:04:33.604000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/RxTsd8_0DEFAULT-LOGO.jpg000ccfc1-2f79-4426-9ac3-de2468c2fcb9/RxTsd8_0DEFAULT-LOGO.jpg",
      "modified_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "modified_on": "2020-08-05T09:44:01.234000Z",
      "name": "Kids",
      "platforms": {},
      "priority_order": 3,
      "slug": "kids",
      "synonyms": [],
      "tags": [],
      "id": "5f2a762131c66700018cdc47"
    },
    {
      "uid": 9,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "created_on": "2020-08-05T09:44:46.632000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/tKkDB8_0DEFAULT-LOGO.jpg1c324d4d-f667-4af8-8d98-37205d34e3b5/tKkDB8_0DEFAULT-LOGO.jpg",
      "modified_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "modified_on": "2020-08-06T18:07:35.231000Z",
      "name": "Women's Fashion",
      "platforms": {},
      "priority_order": 2,
      "slug": "women-s-fashion",
      "synonyms": [],
      "tags": [],
      "id": "5f2a7f8e31c66700018cdc49"
    },
    {
      "uid": 10,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "created_on": "2020-08-05T09:45:12.075000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/oLoxiL_0DEFAULT-LOGO.jpgbd050200-700a-4a3e-9da6-e6b78fbee943/oLoxiL_0DEFAULT-LOGO.jpg",
      "modified_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "modified_on": "2020-08-05T09:48:01.660000Z",
      "name": "Beauty & Personal Care",
      "platforms": {},
      "priority_order": 4,
      "slug": "beauty-personal-care",
      "synonyms": [],
      "tags": [],
      "id": "5f2a7fa831c66700018cdc4a"
    },
    {
      "uid": 11,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "created_on": "2020-08-05T09:45:39.797000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/vQv4ot_0DEFAULT-LOGO.jpg701cb5af-2024-4abf-ae5d-b68bc1a3cd43/vQv4ot_0DEFAULT-LOGO.jpg",
      "modified_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "modified_on": "2020-08-06T11:38:57.599000Z",
      "name": "Home & Living",
      "platforms": {},
      "priority_order": 5,
      "slug": "home-living",
      "synonyms": [],
      "tags": [],
      "id": "5f2a7fc331c66700018cdc4b"
    },
    {
      "uid": 14,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "created_on": "2020-08-05T09:48:42.347000Z",
      "is_active": false,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/hTobjV_0DEFAULT-LOGO.jpga020159c-7fe7-4c1c-a11a-4be61a60da9f/hTobjV_0DEFAULT-LOGO.jpg",
      "modified_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "modified_on": "2020-08-05T09:48:42.347000Z",
      "name": "Baby Care & Kids Essentials",
      "platforms": {},
      "priority_order": 7,
      "slug": "baby-care-kids-essentials",
      "synonyms": [],
      "tags": [],
      "id": "5f2a807a31c66700018cdc4e"
    },
    {
      "_cls": "Department",
      "created_on": "2021-01-13T10:12:33.002000Z",
      "modified_on": "2021-01-13T13:50:55.415000Z",
      "created_by": {
        "username": "919821012599_75351",
        "user_id": "5721"
      },
      "modified_by": {
        "username": "919821012599_75351",
        "user_id": "5721"
      },
      "uid": 21,
      "name": "Skin care products",
      "slug": "skin-care-produts",
      "logo": "https://hdn-1.addsale.com/x0/department/pictures/square-logo/original/rNz8grLys-.png",
      "tags": [],
      "is_active": true,
      "priority_order": 10235,
      "platforms": {},
      "synonyms": [
        "skin",
        "care"
      ],
      "_custom_json": {},
      "id": "5ffec79192813f0001eb6560"
    }
  ]
}
```
</details>









---


#### getDepartmentData
Get specific departments details by passing in unique id of the department




```kotlin
client.catalog.getDepartmentData(uid: uid).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| uid | String | yes | A `uid` is a unique identifier of a department. |  



Allows you to get department data, by uid

*Returned Response*




[DepartmentsResponse](#DepartmentsResponse)

Departments Data. See example below or refer `DepartmentsResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {},
  "items": [
    {
      "uid": 5,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "created_on": "2020-07-01T05:33:39.325000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/BSQ9Gk_123522-best-starry-sky-wallpaper-1920x1200-ipad-pro.jpgc7d0c15c-c1ff-47eb-8423-6e2df51f2ddf/BSQ9Gk_123522-best-starry-sky-wallpaper-1920x1200-ipad-pro.jpg",
      "modified_by": {
        "username": "917753852478_51632",
        "user_id": "5677"
      },
      "modified_on": "2021-03-03T15:55:25.118000Z",
      "name": "Sample Dept",
      "platforms": {},
      "priority_order": 111,
      "slug": "sample-dept",
      "synonyms": [
        "test",
        "sampe"
      ],
      "tags": [],
      "id": "5efc2033623d390001782238"
    },
    {
      "uid": 2,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "app@fynd.com",
        "user_id": "0"
      },
      "created_on": "2020-05-19T06:53:37.629000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/addsale/media/logo/department/original/15974_381e2236c2a348cc851c29a5d05c66a9.png",
      "modified_by": {
        "user_id": "10",
        "username": "fahimsakri_gofynd_com_44938"
      },
      "modified_on": "2021-03-04T14:01:02.556000Z",
      "name": "Men's Fashion",
      "platforms": {
        "fynd": true,
        "fynd_store": true,
        "marketplace": true,
        "openapi": true,
        "uniket_store": true,
        "uniket_wholesale": true
      },
      "priority_order": 111,
      "slug": "men-s-fashion",
      "synonyms": [],
      "tags": [],
      "id": "5ec3827156a7200001c9aeea"
    },
    {
      "uid": 4,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "fahimsakri_gofynd_com_44938",
        "user_id": "10"
      },
      "created_on": "2020-06-29T10:59:33.620000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/ywPVrU_preview_a637ca6e4da6e38f03eb0d650ac5d6ba.jpgc73cc22f-b5ee-4fd4-a585-8ada35762d68/ywPVrU_preview_a637ca6e4da6e38f03eb0d650ac5d6ba.jpg",
      "modified_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "modified_on": "2020-08-06T18:08:02.675000Z",
      "name": "Groceries",
      "platforms": {},
      "priority_order": 10,
      "slug": "groceries",
      "synonyms": [],
      "tags": [],
      "id": "5ef9c9959b04f00001e40dba"
    },
    {
      "uid": 1,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "app@fynd.com",
        "user_id": "0"
      },
      "created_on": "2020-05-18T16:14:41.689000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/platform/pictures/free-logo/original/_G1Z2Fg1L-http:d3p8ifzkmzds37.cloudfront.netmedialogodepartmentoriginal15870_c287d3c2431a432bb0e49363ef6b82bc.png.png",
      "modified_by": {
        "user_id": "5677",
        "username": "917753852478_51632"
      },
      "modified_on": "2021-03-04T15:39:38.528000Z",
      "name": "Electronics",
      "platforms": {
        "fynd": true,
        "fynd_store": true,
        "marketplace": true,
        "openapi": true,
        "uniket_store": true,
        "uniket_wholesale": true
      },
      "priority_order": 100,
      "slug": "electronics",
      "synonyms": [],
      "tags": [],
      "id": "5ec2b471661a4100019fca0d"
    },
    {
      "uid": 3,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "created_on": "2020-05-27T12:04:19.111000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/landscape-banner/original/g2plam_logo_Jio.pngeeb392ca-3958-46a0-9f13-23c205b596f7/g2plam_logo_Jio.png",
      "modified_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "modified_on": "2020-08-06T18:07:46.060000Z",
      "name": "Industrial Supplies",
      "platforms": {},
      "priority_order": 111,
      "slug": "industrial-supplies",
      "synonyms": [],
      "tags": [],
      "id": "5ece5743cd1bae0001440427"
    },
    {
      "uid": 6,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "abhinavsrivastava_gofynd_com_05674",
        "user_id": "13"
      },
      "created_on": "2020-07-06T07:56:01.508000Z",
      "is_active": false,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/wTcfEi_crysis_-_1.jpg14580947-a659-486d-b2d3-d2ca025b1cac/wTcfEi_crysis_-_1.jpg",
      "modified_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "modified_on": "2020-08-06T18:08:12.576000Z",
      "name": "Clothing",
      "platforms": {},
      "priority_order": 1,
      "slug": "clothing",
      "synonyms": [],
      "tags": [],
      "id": "5f02d9116b0ae500018923dd"
    },
    {
      "uid": 8,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "created_on": "2020-08-05T09:04:33.604000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/RxTsd8_0DEFAULT-LOGO.jpg000ccfc1-2f79-4426-9ac3-de2468c2fcb9/RxTsd8_0DEFAULT-LOGO.jpg",
      "modified_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "modified_on": "2020-08-05T09:44:01.234000Z",
      "name": "Kids",
      "platforms": {},
      "priority_order": 3,
      "slug": "kids",
      "synonyms": [],
      "tags": [],
      "id": "5f2a762131c66700018cdc47"
    },
    {
      "uid": 9,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "created_on": "2020-08-05T09:44:46.632000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/tKkDB8_0DEFAULT-LOGO.jpg1c324d4d-f667-4af8-8d98-37205d34e3b5/tKkDB8_0DEFAULT-LOGO.jpg",
      "modified_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "modified_on": "2020-08-06T18:07:35.231000Z",
      "name": "Women's Fashion",
      "platforms": {},
      "priority_order": 2,
      "slug": "women-s-fashion",
      "synonyms": [],
      "tags": [],
      "id": "5f2a7f8e31c66700018cdc49"
    },
    {
      "uid": 10,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "created_on": "2020-08-05T09:45:12.075000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/oLoxiL_0DEFAULT-LOGO.jpgbd050200-700a-4a3e-9da6-e6b78fbee943/oLoxiL_0DEFAULT-LOGO.jpg",
      "modified_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "modified_on": "2020-08-05T09:48:01.660000Z",
      "name": "Beauty & Personal Care",
      "platforms": {},
      "priority_order": 4,
      "slug": "beauty-personal-care",
      "synonyms": [],
      "tags": [],
      "id": "5f2a7fa831c66700018cdc4a"
    },
    {
      "uid": 11,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "created_on": "2020-08-05T09:45:39.797000Z",
      "is_active": true,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/vQv4ot_0DEFAULT-LOGO.jpg701cb5af-2024-4abf-ae5d-b68bc1a3cd43/vQv4ot_0DEFAULT-LOGO.jpg",
      "modified_by": {
        "username": "918793638893_86554",
        "user_id": "3"
      },
      "modified_on": "2020-08-06T11:38:57.599000Z",
      "name": "Home & Living",
      "platforms": {},
      "priority_order": 5,
      "slug": "home-living",
      "synonyms": [],
      "tags": [],
      "id": "5f2a7fc331c66700018cdc4b"
    },
    {
      "uid": 14,
      "_cls": "Department",
      "_custom_json": {},
      "created_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "created_on": "2020-08-05T09:48:42.347000Z",
      "is_active": false,
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/hTobjV_0DEFAULT-LOGO.jpga020159c-7fe7-4c1c-a11a-4be61a60da9f/hTobjV_0DEFAULT-LOGO.jpg",
      "modified_by": {
        "username": "asavarijadhav_gofynd_com_99880",
        "user_id": "5634"
      },
      "modified_on": "2020-08-05T09:48:42.347000Z",
      "name": "Baby Care & Kids Essentials",
      "platforms": {},
      "priority_order": 7,
      "slug": "baby-care-kids-essentials",
      "synonyms": [],
      "tags": [],
      "id": "5f2a807a31c66700018cdc4e"
    },
    {
      "_cls": "Department",
      "created_on": "2021-01-13T10:12:33.002000Z",
      "modified_on": "2021-01-13T13:50:55.415000Z",
      "created_by": {
        "username": "919821012599_75351",
        "user_id": "5721"
      },
      "modified_by": {
        "username": "919821012599_75351",
        "user_id": "5721"
      },
      "uid": 21,
      "name": "Skin care products",
      "slug": "skin-care-produts",
      "logo": "https://hdn-1.addsale.com/x0/department/pictures/square-logo/original/rNz8grLys-.png",
      "tags": [],
      "is_active": true,
      "priority_order": 10235,
      "platforms": {},
      "synonyms": [
        "skin",
        "care"
      ],
      "_custom_json": {},
      "id": "5ffec79192813f0001eb6560"
    }
  ]
}
```
</details>









---


#### listProductTemplate
List all Templates




```kotlin
client.catalog.listProductTemplate(departments: departments).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| departments | String | yes | A `departments` is the name of a particular department. |  



Allows you to list all product templates, also can filter by department

*Returned Response*




[TemplatesResponse](#TemplatesResponse)

List of product templates. See example below or refer `TemplatesResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {
    "current": 1,
    "size": 3,
    "has_previous": false,
    "has_next": true,
    "item_total": 36
  },
  "items": [
    {
      "name": "Accessories",
      "categories": [
        "accessories-adornments",
        "messenger-bags",
        "wallets",
        "satchels",
        "backpacks",
        "laptop-bags",
        "briefcases",
        "suitcases",
        "duffles",
        "analog-watches",
        "chronograph-watches",
        "digital-watches",
        "aviators",
        "wayfarers",
        "round-sunglasses",
        "cateye-sunglasses",
        "rectangle-sunglasses",
        "oversized-sunglasses",
        "browline-sunglasses",
        "square-sunglasses",
        "sports-sunglasses",
        "belts",
        "ties",
        "cufflinks",
        "pocket-squares",
        "tie-pins",
        "brooches",
        "baseball-caps",
        "hats",
        "shawls",
        "mufflers",
        "stoles",
        "socks",
        "dupattas",
        "handbags",
        "clutches",
        "totes",
        "sling-bags",
        "hobos",
        "scarves",
        "stockings",
        "hairbands",
        "hair-clips",
        "pouches",
        "oval-sunglasses",
        "gloves",
        "frames",
        "maang-tikka",
        "bags",
        "sunglasses",
        "mittens",
        "money-clips",
        "card-cases",
        "brushes",
        "horns",
        "spray",
        "cleaner",
        "cream",
        "polishes",
        "decoration-charms",
        "care-kits",
        "trees",
        "shoe-bag",
        "laces",
        "insoles",
        "handkerchief",
        "toy-box",
        "play-gym",
        "camera-bag",
        "fanny-pack",
        "usb-cable",
        "rca-cable",
        "usb-c-to-multiport-adapter",
        "batteries",
        "power-banks",
        "lightning-cable",
        "tos-cable",
        "aux-cable",
        "hdmi-cable",
        "charging-cable",
        "mini-display-port-hdmi-cable",
        "thunderbolt-cable",
        "bluetooth-headphones",
        "headphone",
        "bluetooth-earphones",
        "earphones",
        "hard-disk-drive",
        "photo-frame",
        "notebook",
        "pen",
        "luggage-tag",
        "stationery-combo",
        "jewellery-case",
        "folder",
        "key-chain",
        "suspender",
        "cummerbund",
        "cravet",
        "toiletry-bag",
        "cosmetic-bag",
        "gift-bag",
        "packaging-material",
        "spectacle-case",
        "cuff-bands",
        "playing-cards",
        "kalangi",
        "kataar",
        "safa",
        "watch-case",
        "paper-weight",
        "caps",
        "visor-caps",
        "bucket-hats",
        "beanie-caps",
        "cowboy-hats",
        "gatsby-caps",
        "fedora-hats",
        "rain-cover",
        "round-glasses",
        "rectangle-glasses",
        "cateye-glasses",
        "aviator-glasses",
        "square-glasses",
        "oval-glasses",
        "almond-glasses",
        "wayfarer-glasses",
        "toric-contact-lenses",
        "daily-disposable",
        "monthly-reusable",
        "multifocal-varifocal",
        "solutions-accessories",
        "coloured-lenses"
      ],
      "description": "This is the file validation template for the fashion department and accessories category.",
      "departments": [
        "electronics",
        "men",
        "women",
        "kids",
        "toys"
      ],
      "attributes": [
        "gender",
        "age-group",
        "occasion",
        "collection",
        "season",
        "color",
        "material",
        "product_type",
        "pattern",
        "closure_type",
        "product_length",
        "feature",
        "care_instructions",
        "package_contents",
        "essential",
        "gst-inclusive",
        "gst-if-exclusive",
        "fragile",
        "manufacturer-packer-importer-name",
        "manufacturer-packer-importer-address"
      ],
      "slug": "accessories",
      "banner": "https://hdn-1.fynd.com/seller/pictures/landscape-banner/original/F4W6Pd_DEFAULT-BANNER_LANDSCAPE.jpgd54cb24d-dd2c-441c-bca0-8f65ea3b101c/F4W6Pd_DEFAULT-BANNER_LANDSCAPE.jpg",
      "logo": "https://hdn-1.fynd.com/seller/pictures/logo/original/hkE1dC_0DEFAULT-LOGO.jpgfb5b1b31-9449-43db-9049-435fec88ee77/hkE1dC_0DEFAULT-LOGO.jpg",
      "is_physical": true,
      "id": "5f04a23544a2e5404274bc07"
    },
    {
      "slug": "all-attributes-template",
      "categories": [
        "hd-television"
      ],
      "banner": "https://hdn-1.addsale.com/x0/seller/pictures/landscape-banner/original/tBqIbw_dj.jpg0b8e229f-45bd-4a96-97a5-3e5b193828d2/tBqIbw_dj.jpg",
      "name": "All attributes Template",
      "attributes": [
        "test-attribute-3",
        "test-attribute",
        "test-attribute-1",
        "test-attribute-4",
        "gender",
        "neck-type",
        "qwertyu",
        "testtt-attribute-5",
        "storage_humidity",
        "operating_humidity",
        "certifications",
        "aspect_ratio",
        "storage_temperature",
        "memory_details",
        "cache_memory",
        "operating_temperature",
        "expansion_slots",
        "included_software",
        "web_camera",
        "video_memory",
        "optical_drive",
        "hard_drive_speed",
        "hard_drive_type",
        "hard_drive",
        "speaker_type",
        "core_type",
        "processor_core",
        "processor_model_number",
        "processor_speed",
        "processor_brand",
        "processor_sub_brand",
        "battery_cell",
        "laptop_type",
        "graphics_card_model",
        "accessories",
        "services",
        "promotion_freebie",
        "action",
        "home_delivery",
        "colour_reproduction",
        "brightness",
        "data_transfer_on_cloud",
        "card_reader",
        "battery_filter",
        "volumetric_weight_in_kg",
        "price_filter",
        "brands_filter",
        "number_of_usb_ports_filter",
        "number_of_hdmi_ports_filter",
        "smart_tv_filter",
        "resolution_filter",
        "display_technology",
        "panel_type",
        "record_as_you_watch",
        "schedule_recording",
        "no_of_channels",
        "additional_side_panel_ports",
        "response_time",
        "contrast_ratio",
        "hdmi_arc",
        "tv_operating_system",
        "refresh_rate",
        "connect_to_router_via",
        "connect_to_home_theatre_via",
        "no_of_hdmi_ports",
        "no_of_usb_ports",
        "standby_power_consumption",
        "connect_to_set_top_box_via",
        "stream_content_from_devices",
        "surround_sound_technology",
        "tv_speaker_type",
        "graphics_card_sub_brand",
        "hdr",
        "power_supply",
        "power_consumption",
        "connect_to_dvd_players_via",
        "graphics_card_brand",
        "rated_speaker_output_power_rms",
        "3d_technology",
        "optimized_heat_dissipation",
        "backlit_keyboard_support",
        "ethernet_lan_support",
        "hdmi_support",
        "anti_glare_screen",
        "phone_network_and_connectivity",
        "storage_filter",
        "ram_filter",
        "pallet",
        "waterproof",
        "selfie_camera_filter",
        "primary_camera_filter",
        "screen_size_filter",
        "battery_power_features",
        "in_the_box_warranty",
        "features",
        "screen_display_camera",
        "phone_battery_charge_time",
        "network_inter_device_connectivity",
        "phone_os",
        "phone_build_convenience",
        "phone_hardware_storage",
        "testcomparsion",
        "country_of_origin",
        "manufacturer_packer_importer_address",
        "manufacturer_packer_importer_name",
        "warranty_type",
        "dlna_compliant",
        "user_guides_attachment",
        "resq_support_guide_attachment",
        "water_resistant",
        "speaker_support",
        "fm_radio",
        "nfc_support",
        "package_content",
        "talk_time",
        "standby_time",
        "quick_charge",
        "preloaded_apps",
        "metal_frame",
        "touch_screen",
        "glass_type",
        "meta_description",
        "short_description",
        "is_flammable",
        "transfer_price_tp",
        "screen_size",
        "bluetooth",
        "wi_fi",
        "3g",
        "internal_storage",
        "in_the_box",
        "memory_ram",
        "4g",
        "usb",
        "otg_support",
        "edge",
        "nfc",
        "microphone",
        "dummy_int",
        "product_details",
        "subtitle",
        "general_information",
        "expandable",
        "style_note",
        "is_waterproof",
        "brand_name",
        "color",
        "model",
        "product_type",
        "series",
        "product_identifiers",
        "style",
        "sub_brand",
        "socks_length",
        "heel_height",
        "occasion",
        "storage",
        "season",
        "processor",
        "collection",
        "storage_type",
        "topwear_length",
        "bottomwear_length",
        "denim_type",
        "boot_length",
        "dial_shape",
        "thickness",
        "lens_colour",
        "sensors",
        "dial_colour",
        "material",
        "usb_support",
        "fingerprint_recognition",
        "strap_type",
        "operating_system",
        "frame_style",
        "brand_rating",
        "operating_system_type",
        "4g_bands",
        "strap_colour",
        "4g_support",
        "2g_bands",
        "frame_colour",
        "video_formats",
        "3g_bands",
        "feature",
        "3g_support",
        "movement_type",
        "bluetooth_version",
        "pattern",
        "wi_fi_support",
        "bluetooth_support",
        "inner_material",
        "selfie_camera",
        "closure_type",
        "screen_resolution",
        "product_fit",
        "screen_size_diagonal",
        "dimensions",
        "display_type",
        "plating",
        "primary_camera",
        "toe_type",
        "dual_camera_rear",
        "clasp_type",
        "ram",
        "padding",
        "microphone_support",
        "sim_type",
        "capacity",
        "arch_type",
        "stone_type",
        "warranty_description",
        "additional_connectivity",
        "compartments",
        "audio_formats",
        "sleeve_type",
        "audio_jack",
        "diameter",
        "battery_capacity",
        "sleeve_length",
        "battery_operated",
        "product_length",
        "battery_run_time",
        "neck_type",
        "battery_type",
        "collar_type",
        "battery_voltage",
        "cellular_technology",
        "waist_rise",
        "edge_support",
        "coverage",
        "expandable_memory",
        "package_contents",
        "gprs_support",
        "care_instructions",
        "hybrid_sim_slot",
        "model_info",
        "variant",
        "warranty",
        "complexion",
        "skin_type",
        "spf",
        "speciality",
        "finish",
        "lasting_power",
        "benefits",
        "hair_type",
        "fragrance_family",
        "fragrance_type",
        "product_format",
        "active_ingredients",
        "ingredients",
        "how_to_use",
        "shelf_life",
        "safety_warning",
        "testtt-attribute-6"
      ],
      "departments": [
        "electronics"
      ],
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/7V0z2B_dj.jpg21ac07ea-9f83-403e-ad37-69076c6c5c46/7V0z2B_dj.jpg",
      "description": "Blah Blah",
      "is_physical": true,
      "id": "5ed5f84d2abe0f0001174d73"
    },
    {
      "name": "Baby Care & Toys",
      "categories": [
        "kids-puzzles",
        "kids-shirts"
      ],
      "description": "This is the file validation template for the Baby Care & Toys department.",
      "departments": [
        "baby-care-kids-essentials",
        "toys",
        "kids"
      ],
      "attributes": [
        "gender",
        "age-group",
        "occasion",
        "collection",
        "season",
        "color",
        "material",
        "product_type",
        "no-of-pieces",
        "battery_operated",
        "is-portable",
        "is_flammable",
        "capacity",
        "carrying-capacity",
        "inner-dimension",
        "seat-dimension",
        "package_contents",
        "additional-features",
        "certification",
        "essential",
        "gst-inclusive",
        "gst-if-exclusive",
        "fragile",
        "manufacturer-packer-importer-name",
        "manufacturer-packer-importer-address"
      ],
      "slug": "baby-care-toys",
      "banner": "https://hdn-1.fynd.com/seller/pictures/landscape-banner/original/Ikt1sK_DEFAULT-BANNER_LANDSCAPE.jpg7f923d3d-abc9-4a2e-9a49-204a36e1073c/Ikt1sK_DEFAULT-BANNER_LANDSCAPE.jpg",
      "logo": "https://hdn-1.fynd.com/seller/pictures/logo/original/saEu9Z_0DEFAULT-LOGO.jpg4cd36f29-a15b-4ec1-ab33-1162ede2c61f/saEu9Z_0DEFAULT-LOGO.jpg",
      "is_physical": true,
      "id": "5f04a24944a2e5404274bc09"
    },
    {
      "name": "Bags",
      "categories": [
        "seal-bags",
        "reusable-bag",
        "poly-bag",
        "shoe-bag",
        "sling-bags",
        "bags"
      ],
      "description": "This is the file validation template for the fashion department and bags category.",
      "departments": [
        "kids",
        "women",
        "men"
      ],
      "attributes": [
        "gender",
        "age-group",
        "color",
        "outer-material",
        "inner_material",
        "product_type",
        "collection",
        "occasion",
        "season",
        "pattern",
        "closure_type",
        "care_instructions",
        "compartments",
        "expandable",
        "water-resistence",
        "water-resistence-details",
        "water-proof",
        "water-proof-details",
        "warranty_type",
        "warranty_description",
        "package_contents",
        "essential",
        "gst-inclusive",
        "gst-if-exclusive",
        "fragile",
        "manufacturer-packer-importer-name",
        "manufacturer-packer-importer-address"
      ],
      "slug": "bags",
      "banner": "https://hdn-1.fynd.com/seller/pictures/landscape-banner/original/ejcGMm_DEFAULT-BANNER_LANDSCAPE.jpg658c38fd-d6de-4fcf-9f0e-3a886b2e2225/ejcGMm_DEFAULT-BANNER_LANDSCAPE.jpg",
      "logo": "https://hdn-1.fynd.com/seller/pictures/logo/original/GIysAV_0DEFAULT-LOGO.jpgf1942433-2bcb-4939-9128-675f66cd6d70/GIysAV_0DEFAULT-LOGO.jpg",
      "is_physical": true,
      "id": "5f04a24a44a2e5404274bc0b"
    },
    {
      "modified_on": "2020-08-19T04:04:30.421000Z",
      "logo": "https://hdn-1.addsale.com/x0/products/pictures/template/logo/original/fW2zqHspe-q1.png",
      "created_on": "2020-08-19T04:04:30.421000Z",
      "banner": "https://hdn-1.addsale.com/x0/products/pictures/template/banner/original/_YRvLuMDn-q1.jpeg",
      "attributes": [
        "base-material"
      ],
      "modified_by": {
        "username": "fahimsakri_gofynd_com_44938",
        "user_id": "10"
      },
      "departments": [
        "men-s-fashion",
        "kids",
        "women-s-fashion",
        "beauty-personal-care"
      ],
      "slug": "base-template",
      "description": "ad",
      "name": "Base Template",
      "categories": [
        "adcdas"
      ],
      "created_by": {
        "username": "fahimsakri_gofynd_com_44938",
        "user_id": "10"
      },
      "is_physical": true,
      "id": "5f3ca4ce3f7e74000111925f"
    },
    {
      "description": "This is the file validation template for the Beauty & Personal Care department. ",
      "name": "Beauty & Personal Care",
      "slug": "beauty-personal-care",
      "departments": [
        "beauty-personal-care"
      ],
      "attributes": [
        "gender",
        "age-group",
        "occasion",
        "collection",
        "season",
        "color",
        "product_type",
        "complexion",
        "skin_type",
        "spf",
        "speciality",
        "finish",
        "lasting_power",
        "coverage",
        "hair_type",
        "fragrance_family",
        "fragrance_type",
        "closure_type",
        "capacity",
        "product_format",
        "active_ingredients",
        "benefits",
        "how-to-use",
        "shelf_life",
        "safety_warning",
        "mask_type",
        "material",
        "adjustable",
        "reusable",
        "foldable",
        "filtration",
        "compatible_filter",
        "package_contents",
        "warranty_type",
        "warranty_description",
        "essential",
        "gst-inclusive",
        "gst-if-exclusive",
        "fragile",
        "manufacturer-packer-importer-name",
        "manufacturer-packer-importer-address"
      ],
      "categories": [
        "foundation",
        "concealer",
        "mascara",
        "kajal",
        "eyeshadow",
        "false-eyelashes",
        "eyebrow-enhancer",
        "eyeliner",
        "personal-care-gift-sets",
        "primer",
        "compact",
        "hair-removal-cream",
        "lip-liner",
        "nail-polish-remover",
        "liquid-lipstick",
        "lipstick",
        "nail-polish",
        "moisturizing-socks",
        "hand-cream",
        "sindoor",
        "crayon-lipstick",
        "eye-brushes",
        "manicure-kits",
        "lip-gloss",
        "makeup-remover",
        "nail-art-kit",
        "foot-cream",
        "bb-cream",
        "brush-sets",
        "pedicure-kits",
        "face-brushes",
        "highlighters",
        "lip-balm",
        "lip-brushes",
        "sunscreen",
        "trimmer",
        "facial-kits",
        "colour-contact-lens",
        "body-wash",
        "toners",
        "cleanser",
        "epilator",
        "eye-gels",
        "face-wash",
        "eye-masks",
        "eye-creams",
        "facial-wipes",
        "masks",
        "perfume",
        "moisturizer",
        "serum",
        "night-cream",
        "shoe-deodorant",
        "razor",
        "soaps",
        "body-scrubs",
        "day-cream",
        "deodorants",
        "eye-roll-on",
        "eye-serums",
        "attar",
        "bath-sets",
        "bathing-accessories",
        "scrubs",
        "sets",
        "underarm-roll-on",
        "wax-strips",
        "body-creams",
        "body-lotions",
        "talcum-powders",
        "body-butters",
        "body-mousse",
        "hair-brushes",
        "combs",
        "hair-spa",
        "hair-colour",
        "hair-spa-kits",
        "hair-cream",
        "hair-extensions",
        "anti-stretch-mark-cream",
        "body-oils",
        "body-souffles",
        "conditioner",
        "hair-accessories",
        "hair-oil",
        "hair-serum",
        "hair-spray",
        "shampoo",
        "body-mists",
        "body-sprays",
        "liquid-soap",
        "beard-oil",
        "beard-colour",
        "beard-wash",
        "beard-balm",
        "nail-cutter",
        "home-fragrance",
        "gift-set",
        "hand-soap",
        "hand-sanitizer",
        "face-oil",
        "body-massage-balm",
        "face-gel",
        "face-mist",
        "bath-oil",
        "insect-repellent",
        "anti-ageing-cream",
        "bath-salt",
        "anti-acne-cream",
        "face-massage-cream",
        "whitening-cream",
        "anti-wrinkle-cream",
        "foot-spray",
        "anti-blemish-cream",
        "blush",
        "makeup-fixer",
        "makeup-kit",
        "sponge",
        "foot-scrub",
        "eyeshadow-palette",
        "cc-cream",
        "eye-wipes",
        "head-wrap",
        "patches",
        "nipple-butter",
        "pillow-spray",
        "pillow-roll-on",
        "fragrance-plug",
        "pain-relief-balm",
        "headache-roll-on",
        "mirror",
        "toilet-seat-spray",
        "intimate-wash",
        "massager",
        "makeup-accessories",
        "pillow",
        "nail-accessories",
        "sanitary-napkins",
        "protective-mask",
        "kohl-kajal",
        "natural-lipstick",
        "pearl-lipstick",
        "creme-lipstick",
        "matte-lipstick",
        "glossy-lipstick",
        "compact-spray",
        "compact-stick",
        "compact-powder",
        "highlighter-cake",
        "blush-highlighter",
        "kajal-stick",
        "compact-cake",
        "roll-on-kajal-pencil",
        "liquid-compact",
        "stick-highlighter",
        "kajal-pencil",
        "gel-kajal",
        "liquid-glossy-lipstick",
        "liquid-matte-lipstick",
        "crayon-matte-lipstick",
        "liquid-creme-lipstick",
        "crayon-glossy-lipstick",
        "natural-lip-gloss",
        "liquid-natural-lipstick",
        "crayon-creme-lipstick",
        "pearl-lip-gloss",
        "liquid-pearl-lipstick",
        "crayon-natural-lipstick",
        "liquid-highlighter",
        "crayon-pearl-lipstick",
        "glossy-lip-gloss",
        "matte-lip-gloss",
        "creme-lip-gloss",
        "eye-concealer",
        "object-disinfectant",
        "face-disinfectant",
        "vegetable-fruit-wash",
        "infrared-thermometer",
        "safety-goggle",
        "personal-protective-equipment-kit",
        "examination-gloves",
        "face-shield"
      ],
      "banner": "https://hdn-1.fynd.com/seller/pictures/landscape-banner/original/ZxNlYp_DEFAULT-BANNER_LANDSCAPE.jpg66a71bf3-c1a7-4aa0-98e6-f2a837caa59a/ZxNlYp_DEFAULT-BANNER_LANDSCAPE.jpg",
      "logo": "https://hdn-1.fynd.com/seller/pictures/logo/original/OInLCX_0DEFAULT-LOGO.jpg03aeaeb8-2d04-4694-b641-f60fbdea5c4d/OInLCX_0DEFAULT-LOGO.jpg",
      "is_physical": true,
      "id": "5f05b34844a2e571575f3047"
    },
    {
      "name": "Clothing",
      "categories": [
        "casual-shirts",
        "formal-shirts",
        "sweaters",
        "sweatshirts",
        "hoodies",
        "cardigans",
        "suits",
        "front-open-jackets",
        "blazers",
        "waistcoats",
        "jeans",
        "chinos",
        "cargos",
        "corduroys",
        "formal-trousers",
        "3-4ths",
        "trunks",
        "boardshorts",
        "rashguard",
        "briefs",
        "trackpants",
        "tracksuits",
        "joggers",
        "t-shirts",
        "shorts",
        "gowns",
        "blouson-top",
        "tunics",
        "corsets",
        "kaftan-top",
        "shift-dress",
        "jumpsuits",
        "jeggings",
        "skirts",
        "palazzos",
        "culottes",
        "leggings",
        "shrugs",
        "sports-bra",
        "bikinis",
        "swimsuit",
        "sarong",
        "kaftan",
        "shapewear",
        "camisole",
        "activewear-tops",
        "tights",
        "yoga-pants",
        "capris",
        "harem",
        "bomber-jackets",
        "gilet",
        "leather-jackets",
        "polos",
        "bodycon-dress",
        "off-shoulder-dress",
        "skater-dress",
        "maxi-dress",
        "sheath-dress",
        "sweater-dress",
        "tube-dress",
        "slip-dress",
        "asymmetric-dress",
        "bodysuit",
        "peplum-top",
        "crop-top",
        "tiered-dress",
        "maxi-top",
        "tank-top",
        "tube-top",
        "strappy-top",
        "activewear-jackets",
        "denim-jackets",
        "windcheater",
        "peplum-dress",
        "off-shoulder-top",
        "shirt-dress",
        "kids-shirts",
        "twin-sets",
        "dungarees",
        "trousers",
        "western-jackets",
        "frocks",
        "dresses",
        "tops",
        "casual-pants",
        "beachwear-bottoms",
        "coat",
        "fusion-set",
        "indowestern-kurta",
        "tapered-jeans",
        "joggers-jeans",
        "straight-chinos",
        "tapered-chinos",
        "double-breasted-suits",
        "activewear-crop-tops",
        "flat-front-formal-trousers",
        "pleated-formal-trousers",
        "straight-formal-trousers",
        "straight-jeans",
        "flared-jeans",
        "tapered-formal-trousers",
        "straight-skirt",
        "flared-skirt",
        "asymmetric-skirt",
        "pleated-corduroys",
        "tapered-corduroys",
        "straight-corduroys",
        "cropped-chinos",
        "cropped-corduroys",
        "bootcut-jeans",
        "drop-crotch-jeans",
        "cropped-jeans",
        "bootcut-formal-trousers",
        "cropped-formal-trousers",
        "five-buttoned-suits",
        "tuxedo-suits",
        "one-buttoned-suits",
        "two-buttoned-suits",
        "four-buttoned-suits",
        "three-buttoned-suits",
        "pleated-chinos",
        "pleated-jeans",
        "beachwear-bikini-tops",
        "pleated-skirt",
        "flared-formal-trousers",
        "activewear-tank-tops",
        "beachwear-bikini-bottoms",
        "pencil-skirt",
        "activewear-blouse",
        "casual-joggers"
      ],
      "description": "This is the file validation template for the fashion department and clothing category.",
      "departments": [
        "men",
        "women",
        "kids",
        "clothing"
      ],
      "attributes": [
        "gender",
        "age-group",
        "color",
        "material",
        "occasion",
        "collection",
        "season",
        "product_fit",
        "product_type",
        "product_length",
        "pattern",
        "sleeve_type",
        "sleeve_length",
        "closure_type",
        "neck_type",
        "waist_rise",
        "denim-fade",
        "care_instructions",
        "package_contents",
        "number-of-pockets",
        "model_info",
        "essential",
        "gst-inclusive",
        "gst-if-exclusive",
        "fragile",
        "manufacturer-packer-importer-name",
        "manufacturer-packer-importer-address"
      ],
      "slug": "clothing",
      "banner": "https://hdn-1.fynd.com/seller/pictures/landscape-banner/original/720R34_DEFAULT-BANNER_LANDSCAPE.jpga765babe-cfaa-4cc5-9da7-f4e1402fa97e/720R34_DEFAULT-BANNER_LANDSCAPE.jpg",
      "logo": "https://hdn-1.fynd.com/seller/pictures/logo/original/jKZEs7_0DEFAULT-LOGO.jpg78413c0a-11a8-43f8-88ad-1442e9fdb898/jKZEs7_0DEFAULT-LOGO.jpg",
      "is_physical": true,
      "id": "5f04a25044a2e5404274bc0e"
    },
    {
      "description": "asdd",
      "attributes": [
        "color",
        "warranty_type",
        "care_instructions"
      ],
      "modified_on": "2020-08-20T16:15:33.598000Z",
      "modified_by": {
        "username": "fahimsakri_gofynd_com_44938",
        "user_id": "10"
      },
      "name": "FA-Template",
      "categories": [
        "vision-qa-f9447f89-d2da-41fc-ac33-b9f286308c14"
      ],
      "logo": "https://hdn-1.addsale.com/x0/products/pictures/template/logo/original/fW2zqHspe-q1.png",
      "departments": [
        "electronics"
      ],
      "banner": "https://hdn-1.addsale.com/x0/products/pictures/template/banner/original/L_u77Mz4T-FA-Template.png",
      "slug": "fa-template",
      "created_on": "2020-08-19T09:51:08.215000Z",
      "created_by": {
        "username": "fahimsakri_gofynd_com_44938",
        "user_id": "10"
      },
      "is_physical": true,
      "id": "5f3cf60c9788cc00018ab276"
    },
    {
      "name": "Footwear",
      "categories": [
        "sneakers",
        "running-shoes",
        "hiking-shoes",
        "football-shoes",
        "indoor-sports-shoes",
        "trainers",
        "outdoor-sports-shoes",
        "moccasins",
        "loafers",
        "boat-shoes",
        "brogues",
        "derby-shoes",
        "oxfords",
        "monk-strap-shoes",
        "lace-ups",
        "formal-slip-ons",
        "boots",
        "sandals",
        "flip-flops",
        "floaters",
        "d-orsay",
        "espadrilles",
        "pointed-toe",
        "flat-slip-ons",
        "gladiators",
        "flat-sandals",
        "stilettos",
        "wedges",
        "block-heels",
        "kitten-heels",
        "louis-heels",
        "cone-heels",
        "heel-sandals",
        "ballerinas",
        "casual-slip-ons",
        "casual-lace-ups",
        "ethnic-sandals",
        "clogs",
        "slippers",
        "school-shoes",
        "high-heels",
        "flats",
        "mules",
        "crocs",
        "heels-pumps",
        "mojaris",
        "jutties",
        "labour-shoes"
      ],
      "description": "This is the file validation template for the fashion department and footwear category.",
      "departments": [
        "men",
        "women",
        "kids"
      ],
      "attributes": [
        "gender",
        "age-group",
        "color",
        "outer-material",
        "inner_material",
        "sole-material",
        "occasion",
        "collection",
        "season",
        "product_type",
        "pattern",
        "closure_type",
        "toe_type",
        "arch_type",
        "heel_height",
        "heel-height-unit-of-measure",
        "care_instructions",
        "package_contents",
        "water-resistence",
        "water-resistence-details",
        "water-proof",
        "water-proof-details",
        "warranty_type",
        "warranty_description",
        "essential",
        "gst-inclusive",
        "gst-if-exclusive",
        "fragile",
        "manufacturer-packer-importer-name",
        "manufacturer-packer-importer-address"
      ],
      "slug": "footwear",
      "banner": "https://hdn-1.fynd.com/seller/pictures/landscape-banner/original/phMzNh_DEFAULT-BANNER_LANDSCAPE.jpgf06e7d2f-15a0-405a-b37b-1333c618abdb/phMzNh_DEFAULT-BANNER_LANDSCAPE.jpg",
      "logo": "https://hdn-1.fynd.com/seller/pictures/logo/original/PkIwbo_0DEFAULT-LOGO.jpgbb9acb1b-5e2c-44d4-918a-9429367ccb7d/PkIwbo_0DEFAULT-LOGO.jpg",
      "is_physical": true,
      "id": "5f04a25344a2e5404274bc10"
    },
    {
      "slug": "groceries",
      "name": "Groceries",
      "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/EtkWQm_fruit___vegetable_logo.jpgc541c78c-dabc-4823-bb72-c4bd3e5db449/EtkWQm_fruit___vegetable_logo.jpg",
      "departments": [
        "groceries"
      ],
      "description": "Groceries",
      "banner": "https://hdn-1.addsale.com/x0/seller/pictures/landscape-banner/original/BPjEl6_fruit___vegetable_logo.jpg577eb6bb-de4e-444c-a86a-bc23e0d97178/BPjEl6_fruit___vegetable_logo.jpg",
      "attributes": [
        "ingredient-type",
        "manufacturer_packer_importer_address"
      ],
      "categories": [
        "buns",
        "non-veg-pickle",
        "condensed-milk",
        "shoe-shiners",
        "bath-stool-tub-basin-sets",
        "soda-cocktail-mix",
        "tofu",
        "buckets-mugs",
        "fresh-mutton",
        "games-calculators",
        "kolam",
        "namkeen-savoury-snacks",
        "gift-bags",
        "honey",
        "cutlery-spoons-fork",
        "pita",
        "potato-onion-tomato",
        "apples-pomegranate",
        "dishwash-powder",
        "country-eggs",
        "fish-tuna",
        "coconut-milk",
        "sugarfree-sweeteners",
        "cups-mugs-tumblers",
        "turkey",
        "breakfast-snack-mixes",
        "diabetic-drinks",
        "other-dal",
        "herbs-seasoning",
        "incense-sticks",
        "scissor",
        "slice-cakes",
        "dips-dressings",
        "files",
        "lavash",
        "flakes",
        "tawa-sauce-pan",
        "breads",
        "jaggery",
        "soya-chunks",
        "exotic-vegetables",
        "wine-rise-vinegar",
        "recipe-packs",
        "pen",
        "cookware-sets",
        "jam-conserve-marmalade",
        "holi-pichkari",
        "knives-peelers",
        "chicken-sausages",
        "poha",
        "jowar-flour",
        "cook-serve",
        "unsweetened-cold-press",
        "decorations",
        "dust-cloth-wipes",
        "jelly",
        "gift-boxes",
        "organic-cold-press-oil",
        "glucose-powder-tablets",
        "frozen-non-veg-snacks",
        "leafy-vegetables",
        "salted-biscuits",
        "cooking-chocolates-cocoa",
        "marinated-meat",
        "berries",
        "basmati-rice",
        "ground-coffee",
        "cut-vegetables",
        "moong-dal",
        "glue",
        "fabric-pre-post-wash",
        "canola-rapeseed-oil",
        "water-fridge-bottle",
        "frozen-fish-seafood",
        "choppers-graters",
        "soya",
        "kiwi-melon-citrus-fruits",
        "buttermilk",
        "focaccia",
        "healthy-baked-snacks",
        "bowls",
        "car-freshener",
        "nachos",
        "powdered-spices",
        "rawa",
        "pressure-cookers",
        "chips",
        "cream-rolls",
        "tape",
        "bajra",
        "jowar",
        "ice-cream",
        "wicks",
        "cooking-pastes",
        "erasers-sharpeners",
        "imported-fruits",
        "notebooks",
        "masoor-dal",
        "canned-seafood",
        "regular-white-vinegar",
        "croissants-bread",
        "pasta",
        "root-vegetables",
        "whole-spices",
        "chana-dal",
        "glassware",
        "cucumber-gourds-capsicum",
        "papads-ready-to-fry",
        "lamp",
        "hakka-noodles",
        "balsamic-cider-vinegar",
        "garbage-bags",
        "pumpkin-drumstick",
        "other-plastic-ware",
        "frozen-indian-breads",
        "glucose-milk-biscuits",
        "non-alcoholic-drinks",
        "paneer",
        "toor-dal",
        "fresh-salads-sprouts",
        "fresh-chicken",
        "wheat-flour",
        "fruits-pulps",
        "cheese-spread",
        "camphor",
        "cabbage-broccoli-cauliflower",
        "sugar",
        "candles",
        "plates",
        "mangoes",
        "aerated-drinks",
        "toffee-candy-lollypop",
        "pizza-base",
        "thai-asian-sauce",
        "shoe-brushes",
        "gas-stove",
        "sports-energy-drinks",
        "shrikhand",
        "hangers-clips-ropes",
        "croutons",
        "floor-other-cleaners",
        "toilet-cleaners",
        "macaroni",
        "folders",
        "choco-nut-spread",
        "salts",
        "butter",
        "pavs",
        "hangers",
        "khari",
        "frozen-veg-snacks",
        "tea-cakes",
        "seasonal-fruits",
        "olive",
        "seasonal-accessories",
        "cream",
        "heat-eat-ready-meals",
        "dishwash-liquid-paste",
        "rubs",
        "beans-pulses",
        "seasonal-vegetables",
        "besan",
        "shoe-polish",
        "packaged-water",
        "kids-cereal",
        "instant-coffee",
        "powdered-milk",
        "dishwash-bar",
        "home-baking",
        "laundry-storage-baskets",
        "detergent-liquid",
        "instant-noodles",
        "canned-food",
        "disposable-cups-plates",
        "brinjals",
        "imported-cleaners",
        "tinned-packed-sweets",
        "container-set",
        "lamp-oil",
        "mayonnaise",
        "wall-hooks",
        "spreads",
        "juices",
        "quinoa-grains",
        "pooja-thali",
        "milk",
        "syrups-concentrates",
        "cut-fruit-tender-coconut",
        "kitchen-rolls",
        "cold-drinks",
        "vessels",
        "premium-cookies",
        "pooja-bells",
        "other-pooja-needs",
        "rise-flour",
        "breadcrumbs",
        "cup-cakes",
        "berry",
        "regional-rice",
        "regional-grains",
        "chilli-soya-sauce",
        "gourmet-popcorn",
        "beans-okra",
        "wafers",
        "sparkling-drinks",
        "muffins",
        "daliya",
        "match-box",
        "bagels-bread",
        "rice-products",
        "dry-fruits",
        "dal-mix",
        "flavoured-water",
        "roasted-seeds-nuts",
        "marshmallow",
        "toilet-paper",
        "wet-wipes",
        "fruit-baskets",
        "leaf-dust-tea",
        "rakhi",
        "insect-repellent",
        "bajra-flour",
        "ghee",
        "lunch-boxes",
        "cup-noodles",
        "chocolates",
        "candle-holder",
        "frozen-mutton",
        "marie-health-digestive",
        "pencils",
        "turkey-duck",
        "vermicelli",
        "exotic-flavoured-tea",
        "powdered-mixes",
        "urad-dal",
        "toilet-other-brushes",
        "jalapeno",
        "maida",
        "chutney",
        "fresh-sweets",
        "dessert-mixes",
        "instant-pasta",
        "kitchen-tools-other-accessories",
        "mushrooms",
        "chilli-lemon-garlic-ginger",
        "gherkin",
        "cooking-oil",
        "curry-paste",
        "tumblers",
        "lamb",
        "cheese",
        "other-seafood",
        "other-meat",
        "frozen-chicken",
        "banana-sapota-papaya",
        "granola-cereal-bars",
        "sabudana",
        "cream-biscuits",
        "bread-sticks",
        "chia-seeds",
        "utensil-scrub-pad-glove",
        "soya-granules",
        "soups",
        "spring-water",
        "rusks",
        "olive-oil",
        "organic-eggs",
        "aluminium-foil-cling-wrap",
        "colours-crayons",
        "corn-snacks",
        "pulses",
        "protein-eggs",
        "tomatoes-vegetables",
        "cookies",
        "still-drinks",
        "mustard-cheese-sauce",
        "regional-flour",
        "detergent-powder",
        "flavoured-other-oils",
        "chikki-gajak",
        "curd",
        "strainers-ladle-spatula",
        "holi-colours",
        "trail-cocktail-mixes",
        "baking-cake-decoration",
        "biscuits",
        "pencil-box",
        "muesli",
        "air-freshener",
        "quinoa",
        "metal-furniture-cleaners",
        "green-tea",
        "paper-napkin",
        "flavoured-milk",
        "mints-chewing-gum",
        "lighters",
        "lassi",
        "edamame-beans",
        "dry-fish",
        "blended-masalas",
        "tomato-ketchup",
        "kadai-fry-pans",
        "dustbins",
        "syrups",
        "wheat",
        "kitchen-glass-drains",
        "pork-ham",
        "panini",
        "flours-pre-mixes",
        "cfl-led-bulbs",
        "baguette-bread",
        "brooms-dust-pans",
        "prawns-shrimps",
        "soap-cases-dispensers",
        "oats-porridge",
        "mops-wipers",
        "exam-pads",
        "tea-bags",
        "pastries",
        "mosquito-repellent",
        "cut-peeled-veggies",
        "pickle",
        "brownies",
        "margarine",
        "soya-milk",
        "fresh-fish",
        "cloth-dryer-iron-table",
        "gift-wrap",
        "farm-eggs",
        "detergent-bar",
        "battery-electricals"
      ],
      "is_physical": true,
      "id": "5efc43b13b4ca00001328666"
    },
    {
      "description": "This is the file validation template for the Home & Living Department",
      "name": "Home & Living",
      "slug": "home-living",
      "departments": [
        "home-living"
      ],
      "categories": [
        "slippers",
        "chairs",
        "table",
        "beds",
        "vases",
        "bed-sheets",
        "dining-table",
        "blankets",
        "bath-robe",
        "bathing-accessories",
        "napkins",
        "hanger",
        "lunch-box",
        "photo-frame",
        "toiletry-bag",
        "pillow",
        "cup-saucer",
        "pet-collar-charm",
        "alarm-clocks",
        "dessert-plates",
        "vintage-clocks",
        "tissue-holder",
        "flush-mount-lights",
        "jewellery-box-stands",
        "desk-accessories",
        "serving-sets",
        "cake-stands",
        "bath-towel",
        "cutlery",
        "knives",
        "knives-holder",
        "pillow-covers",
        "placemats",
        "saucer",
        "coasters",
        "tea-sets",
        "forks",
        "shower-curtains",
        "serving-bowls",
        "soap-dispensers",
        "spoons",
        "bath-mats",
        "table-runner",
        "bed-covers",
        "tea-coffee-accessories",
        "coverlets",
        "soap-dishes",
        "duvet",
        "bed-sheets-sets",
        "duvet-cover",
        "bolster-pillows",
        "quilts-rajais",
        "mattress",
        "bed-linen-set",
        "candles",
        "clothes-storage",
        "shoe-racks",
        "cushion-fillers",
        "scented-candles",
        "art-pieces",
        "key-holder",
        "planters",
        "showpieces",
        "decals-stickers",
        "mirrors",
        "clocks",
        "coffee-tables",
        "dining-benches",
        "ottoman",
        "artificial-flowers",
        "dining-chair",
        "dining-table-set",
        "drapery",
        "console-table",
        "baking-mould",
        "cup",
        "dohars",
        "cushion-covers",
        "fountains",
        "comforters",
        "mugs",
        "flowerpot",
        "cushions",
        "decorative-objects",
        "napkin-holder",
        "trays",
        "table-cloth",
        "tea-cosy",
        "shower-caps",
        "shower-mats",
        "bed-skirts",
        "wardrobe-organisers",
        "mattress-protectors",
        "pillow-protectors",
        "tea-light-candles",
        "sculptures",
        "faux-plants",
        "vintage-finds",
        "wall-art",
        "dressing-tables",
        "benches",
        "sofas",
        "storage-trunks",
        "curtains",
        "side-table",
        "pillow-shams",
        "wind-chimes",
        "candle-holders",
        "cheese-boards",
        "serving-platters",
        "pitchers",
        "drinking-glasses",
        "pet-collar",
        "bathroom-faucets",
        "lamp-bases",
        "wreath",
        "pendant-lamps",
        "hearth-fireplace",
        "sconces",
        "succulents-plants",
        "fireplace-screens",
        "garlands",
        "electric-fireplaces",
        "storage-boxes",
        "elecrtonics-tech-accessories",
        "diffusers",
        "potpourri",
        "throws",
        "ceiling-lights",
        "pet-feeding-bowl",
        "chandeliers",
        "carpets",
        "salad-plates",
        "room-partitions",
        "bar-accessories",
        "decorative-lights",
        "hand-towel",
        "lamp-shades",
        "face-towel",
        "study-table-lamps",
        "floor-runner",
        "wall-lamps",
        "frying-pan",
        "door-mats",
        "carafe",
        "dinner-plates",
        "snifter",
        "dinner-set",
        "peg-measure",
        "platters",
        "shot-bottles",
        "bathroom-caddy",
        "vinegar-dispenser",
        "toilet-brush-holder",
        "cutlery-holder",
        "toothbrush-holder",
        "kitchen-trolly",
        "stemware",
        "measuring-cup",
        "baking-tray",
        "strainer",
        "stew-pan",
        "whisk",
        "cocktail-shaker",
        "flask",
        "food-container",
        "string-lights",
        "bottle-holder",
        "poufs",
        "chopping-board",
        "fireplace-tools",
        "dish-rack",
        "log-racks-holders",
        "ladle",
        "aroma-oils",
        "peeler",
        "incense-sticks-holders",
        "tongs",
        "incense-sticks",
        "kettle",
        "kulladhs",
        "table-linen-set",
        "handbag-organiser",
        "upholstery",
        "laundry-bag",
        "floor-lamps",
        "magazine-organiser",
        "lighting-accessories",
        "makeup-organiser",
        "table-lamps",
        "shelf-liner",
        "rugs-dhurries",
        "shoes-organiser",
        "sweater-bag",
        "bowls",
        "decanters",
        "garbage-bag",
        "beach-towel",
        "bookcase",
        "towel-set",
        "pool-table",
        "bath-rug",
        "poker-table",
        "shower-holder",
        "table-tennis",
        "towel-holder",
        "bar-counter-stools",
        "bath-mirror",
        "bar-carts",
        "towel-rod",
        "bar-furniture",
        "floor-mats",
        "bedside-table",
        "kadhai",
        "foundations",
        "sauce-pan",
        "pillow-inserts",
        "tawa",
        "bathroom-vanities",
        "cocktail-set",
        "lounging-relaxing-furniture",
        "canister",
        "oil-dispenser",
        "salt-pepper-shakers",
        "spatula",
        "casserole",
        "handi",
        "glasses",
        "kitchen-linen-set",
        "wardrobe-organiser",
        "jewellery-organiser",
        "separators",
        "closet-storage",
        "garbage-bag-holder",
        "hooks",
        "foosball-table",
        "board-game",
        "wall-shelves",
        "media-furniture",
        "file-cabinets",
        "leather-furniture",
        "buffets-sidebars",
        "mattress-pads",
        "wastebaskets",
        "hampers-baskets",
        "outdoor-dining-furniture",
        "entry-furniture",
        "water-jugs",
        "table-covers",
        "lanterns",
        "desk-organiser",
        "drawer-organiser",
        "suit-organiser",
        "swab-storage",
        "tote-basket",
        "hanger-holder",
        "cabinet",
        "hockey-table",
        "shuffleboard",
        "game-accessories",
        "desk",
        "office-chairs",
        "dining-storage",
        "kitchen-island",
        "nightstands",
        "duvet-inserts",
        "mattress-toppers",
        "medicine-cabinets",
        "bathroom-hardware-accessories",
        "salt-pepper-grinders",
        "water-bottle"
      ],
      "attributes": [
        "occasion",
        "collection",
        "color",
        "material",
        "product_type",
        "bed_size",
        "utility",
        "quality",
        "pattern",
        "filling",
        "shape",
        "sheet-type",
        "sheet_size",
        "thread_count",
        "product-dimensions",
        "pocket_depth",
        "group-id",
        "variation-type",
        "variation-based-on",
        "capacity",
        "dishwasher_safe",
        "microwave_safe",
        "oven_safe",
        "additional-features",
        "care_instructions",
        "package_contents",
        "sales_package",
        "warranty_type",
        "warranty_description",
        "gst-inclusive",
        "gst-if-exclusive",
        "fragile",
        "manufacturer-packer-importer-name",
        "manufacturer-packer-importer-address"
      ],
      "banner": "https://hdn-1.fynd.com/seller/pictures/landscape-banner/original/EHRCqs_DEFAULT-BANNER_LANDSCAPE.jpgc596e149-f6e1-4695-9446-9a8b88797d4c/EHRCqs_DEFAULT-BANNER_LANDSCAPE.jpg",
      "logo": "https://hdn-1.fynd.com/seller/pictures/logo/original/UAiJlq_0DEFAULT-LOGO.jpg25c9816d-2376-4eaf-b4ab-accb37e9a564/UAiJlq_0DEFAULT-LOGO.jpg",
      "is_physical": true,
      "id": "5f05acfa44a2e55081728be2"
    },
    {
      "categories": [
        "3-ply-box",
        "5-ply-box",
        "7-ply-box",
        "9-ply-box",
        "bubble-roll",
        "card-board-roll",
        "courier-bag",
        "courier-pouch",
        "die-cut-box",
        "double-side-tape",
        "drawer-box",
        "duct-tape",
        "filament-tape",
        "laminated-box",
        "packaging-tape",
        "poly-bag",
        "printed-tape",
        "reusable-bag",
        "seal-bags",
        "stretch-wrap",
        "suit-box",
        "zip-lock-bags",
        "box"
      ],
      "name": "Industrial Supplies",
      "banner": "https://hdn-1.fynd.com/seller/pictures/landscape-banner/original/9DpMn3_Beauty_&_Personal_Care_L.jpg80d89967-9c2c-498b-a79c-d176b3e71ea5/9DpMn3_Beauty_and_Personal_Care_L.jpg",
      "slug": "industrial-supplies",
      "attributes": [
        "color",
        "primary_color",
        "style",
        "features",
        "safety_warning",
        "is_flammable",
        "water_resistant",
        "product_details",
        "package_contents",
        "essential",
        "pallet"
      ],
      "logo": "https://hdn-1.fynd.com/seller/pictures/logo/original/I2NV2c_indi.jpg2eaf85b5-8076-4b0b-8f01-f119d6d8b559/I2NV2c_indi.jpg",
      "departments": [
        "industrial-supplies"
      ],
      "description": "Products used for business and industrial manufacturing process comes under this category. Example: Packaging Material",
      "modified_by": {
        "username": "meghagolecha_fynd_com_89167",
        "user_id": "23244269"
      },
      "modified_on": "2020-08-20T19:12:26.040000Z",
      "is_active": true,
      "is_physical": true,
      "id": "5f11eced5ca7f90001685a70"
    }
  ]
}
```
</details>









---


#### validateProductTemplate
Validate Product Template Schema




```kotlin
client.catalog.validateProductTemplate(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| slug | String | yes | A `slug` is a unique identifier for a particular template. |  



Allows you to list all product templates validation values for all the fields present in the database

*Returned Response*




[TemplatesValidationResponse](#TemplatesValidationResponse)

List of fields and validation values fro each. See example below or refer `TemplatesValidationResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
null
```
</details>









---


#### downloadProductTemplateViews
Download Product Template View




```kotlin
client.catalog.downloadProductTemplateViews(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| slug | String | yes | A `slug` is a unique identifier for a particular template. |  



Allows you to download product template data

*Returned Response*




[String](#String)

CSV File of product template data. See example below or refer `TemplatesResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### downloadProductTemplateView
Download Product Template View




```kotlin
client.catalog.downloadProductTemplateView(itemType: itemType).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| itemType | String | yes | An `item_type` defines the type of item. |  



Allows you to download product template data

*Returned Response*




[String](#String)

CSV File of product template data.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### validateProductTemplateSchema
Validate Product Template Schema




```kotlin
client.catalog.validateProductTemplateSchema(itemType: itemType).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| itemType | String | yes | An `item_type` defines the type of item. The default value is standard. |  



Allows you to list all product templates validation values for all the fields present in the database

*Returned Response*




[InventoryValidationResponse](#InventoryValidationResponse)

List of fields and validation values fro each. See example below or refer `InventoryValidationResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "data": {
    "title": "InventoryValidationResponse",
    "type": "object",
    "properties": {
      "item": {
        "$ref": ""
      },
      "sizes": {
        "title": "Sizes",
        "type": "array",
        "items": {
          "$ref": ""
        }
      }
    },
    "required": [
      "item",
      "sizes"
    ],
    "definitions": {
      "ItemQuery": {
        "title": "ItemQuery",
        "type": "object",
        "properties": {
          "uid": {
            "title": "Uid",
            "type": "integer"
          },
          "brand_uid": {
            "title": "Brand Uid",
            "type": "integer"
          },
          "item_code": {
            "title": "Item Code",
            "type": "integer"
          }
        }
      },
      "InventoryBaseSchema": {
        "title": "InventoryBaseSchema",
        "type": "object",
        "properties": {
          "price": {
            "title": "Actual Price",
            "exclusiveMinimum": 1,
            "type": "number"
          },
          "price_effective": {
            "title": "Selling Price",
            "exclusiveMinimum": 1,
            "type": "number"
          },
          "seller_identifier": {
            "title": "Gtin Value",
            "pattern": "^[A-Za-z0-9]*$",
            "type": "string"
          },
          "quantity": {
            "title": "Quantity",
            "minimum": 0,
            "type": "integer"
          },
          "store_code": {
            "title": "Store Code",
            "type": "string",
            "enum": [
              "RUOSH43",
              "S106",
              "S108",
              "TIO9",
              "talha"
            ]
          },
          "currency": {
            "title": "Currency",
            "enum": [
              "INR",
              "QAR"
            ],
            "type": "string"
          },
          "size": {
            "title": "Size",
            "type": "string"
          }
        },
        "required": [
          "price",
          "price_effective",
          "seller_identifier",
          "quantity",
          "store_code",
          "currency",
          "size"
        ]
      }
    }
  },
  "message": "Success"
}
```
</details>









---


#### listHSNCodes
List HSN Codes




```kotlin
client.catalog.listHSNCodes().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |  



Allows you to list all hsn Codes

*Returned Response*




[HSNCodesResponse](#HSNCodesResponse)

List of all HSN Codes. See example below or refer `HSNCodesResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "data": {
    "country_of_origin": [
      "India"
    ],
    "hsn_code": [
      "11111111"
    ]
  },
  "message": "Success"
}
```
</details>









---


#### listProductTemplateExportDetails
Allows you to list all product templates export list details




```kotlin
client.catalog.listProductTemplateExportDetails().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |  



Can view details including trigger data, task id , etc.

*Returned Response*




[ProductDownloadsResponse](#ProductDownloadsResponse)

List of Product Downloads Data. See example below or refer `ProductDownloadsResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {},
  "items": [
    {
      "created_by": {
        "username": "917972410891_48194",
        "user_id": "5646"
      },
      "data": {
        "type": "csv",
        "brand": [
          "ruosh"
        ],
        "templates": [
          "mobile-phones-and-tablet"
        ]
      },
      "status": "success",
      "task_id": "c4b54ace-44ef-11eb-9806-1ef9bc4a2da1",
      "template_tags": {
        "mobile-phones-and-tablet": {
          "display": "Mobile Phones & Tablet",
          "logo": "https://hdn-1.jiox0.de/jiox0/seller/pictures/logo/original/Oda39B_99946594-portable-devices-with-tablet-and-mobile-phone-vector-icon-for-apps-and-websites.jpgcc2dff44-7fae-4002-9ebe-d2b59c8bee91/Oda39B_99946594-portable-devices-with-tablet-and-mobile-phone-vector-icon-for-apps-and-websites.jpg"
        }
      },
      "trigger_on": "2020-12-23T07:23:35.302000Z",
      "seller_id": 3,
      "completed_on": "2020-12-23T07:23:41.031000Z",
      "url": "https://regrowth.s3.amazonaws.com/slingshot-catalogues/seller-catalog/3/c4b54ace-44ef-11eb-9806-1ef9bc4a2da1/c4b54ace-44ef-11eb-9806-1ef9bc4a2da1.zip",
      "id": "5fe2f077516d980001880943"
    }
  ]
}
```
</details>









---


#### listTemplateBrandTypeValues
Allows you to list all values for Templates, Brands or Type




```kotlin
client.catalog.listTemplateBrandTypeValues(filter: filter).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| filter | String | yes | A `filter` is the unique identifier of the type of value required. |  



The filter type query parameter defines what type of data to return. The type of query returns the valid values for the same

*Returned Response*




[ProductConfigurationDownloads](#ProductConfigurationDownloads)

See example below or refer `ProductConfigurationDownloadsSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "data": [
    {
      "display": "csv",
      "value": "csv"
    },
    {
      "display": "excel",
      "value": "excel"
    }
  ],
  "multivalue": false
}
```
</details>









---


#### listCategories
Get product categories list




```kotlin
client.catalog.listCategories(level: level, departments: departments, q: q, pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| level | String? | no | Get category for multiple levels |   
| departments | String? | no | Get category for multiple departments filtered |   
| q | String? | no | Get multiple categories filtered by search string |   
| pageNo | Int? | no | The page number to navigate through the given set of results |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 10. |  



This API gets meta associated to product categories.

*Returned Response*




[CategoryResponse](#CategoryResponse)

Category Meta. See example below or refer `CategoryResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {
    "current": 1,
    "size": 58,
    "has_previous": false,
    "has_next": true,
    "item_total": 574
  },
  "items": [
    {
      "name": "Air Conditioners",
      "media": {
        "logo": "https://hdn-1.addsale.com/x0/category/pictures/square-logo/original/zTgh1zslj-.png",
        "portrait": "https://hdn-1.addsale.com/x0/category/pictures/portrait-banner/original/VKqwRngFh-.png",
        "landscape": "https://hdn-1.addsale.com/x0/category/pictures/landscape-banner/original/_7GDi3tyi-.png"
      },
      "marketplaces": {},
      "tryouts": [],
      "is_active": true,
      "created_by": {
        "username": "917972410891_48194",
        "user_id": "5646"
      },
      "uid": 22330,
      "slug": "air-conditioners",
      "priority": 1,
      "synonyms": [],
      "modified_by": {
        "username": "917972410891_48194",
        "user_id": "5646"
      },
      "level": 3,
      "hierarchy": [
        {
          "l1": 1,
          "department": 1,
          "l2": 22329
        }
      ],
      "created_on": "2021-04-02T15:43:59.410000Z",
      "departments": [
        1
      ],
      "modified_on": "2021-04-02T15:43:59.410000Z",
      "id": "60673bbf7896da00017885ad"
    },
    {
      "name": "Home Appliances",
      "media": {
        "logo": "https://hdn-1.addsale.com/x0/category/pictures/square-logo/original/zTgh1zslj-.png",
        "portrait": "https://hdn-1.addsale.com/x0/category/pictures/portrait-banner/original/VKqwRngFh-.png",
        "landscape": "https://hdn-1.addsale.com/x0/category/pictures/landscape-banner/original/_7GDi3tyi-.png"
      },
      "is_active": true,
      "created_by": {
        "username": "917972410891_48194",
        "user_id": "5646"
      },
      "uid": 22329,
      "slug": "home-appliances",
      "priority": 1,
      "synonyms": [],
      "modified_by": {
        "username": "917972410891_48194",
        "user_id": "5646"
      },
      "level": 2,
      "hierarchy": [],
      "created_on": "2021-04-02T15:42:55.405000Z",
      "departments": [
        1
      ],
      "modified_on": "2021-04-02T15:42:55.405000Z",
      "id": "60673b7f7896da00017885ac"
    },
    {
      "created_by": {
        "username": "919821012599_75351",
        "user_id": "5721"
      },
      "slug": "dummy-category-level-2",
      "level": 2,
      "uid": 22323,
      "is_active": true,
      "media": {
        "portrait": "https://hdn-1.addsale.com/x0/category/pictures/portrait-banner/original/VKqwRngFh-.png",
        "landscape": "https://hdn-1.addsale.com/x0/category/pictures/landscape-banner/original/0wCdjxWpI-.png",
        "logo": "https://hdn-1.addsale.com/x0/category/pictures/square-logo/original/zTgh1zslj-.png"
      },
      "name": "Dummy category level 2 by fahim",
      "modified_on": "2021-03-04T15:43:50.495000Z",
      "modified_by": {
        "username": "917753852478_51632",
        "user_id": "5677"
      },
      "synonyms": [
        "skin",
        "care",
        "asdasd"
      ],
      "created_on": "2021-01-14T05:28:02.148000Z",
      "priority": 123456,
      "hierarchy": [],
      "departments": [
        21
      ],
      "id": "5fffd662e64eb40001fc8a42"
    },
    {
      "synonyms": [],
      "marketplaces": {},
      "created_on": "2021-02-25T00:00:47.589000Z",
      "modified_by": {
        "username": "917753852478_51632",
        "user_id": "5677"
      },
      "media": {
        "landscape": "https://hdn-1.addsale.com/x0/category/pictures/landscape-banner/original/0wCdjxWpI-.png",
        "logo": "https://hdn-1.addsale.com/x0/category/pictures/square-logo/original/EfCt9iXx8-http/d3p8ifzkmzds37.cloudfront.net/media/logo/department/original/15870_c287d3c2431a432bb0e49363ef6b82bc.png.jpeg",
        "portrait": "https://hdn-1.addsale.com/x0/category/pictures/portrait-banner/original/S1axCMOJ4-.png"
      },
      "modified_on": "2021-03-04T15:39:52.108000Z",
      "hierarchy": [
        {
          "l2": 22323,
          "l1": 22322,
          "department": 21
        }
      ],
      "name": "Dummy level 4",
      "is_active": true,
      "slug": "dummy-level-4",
      "departments": [
        21
      ],
      "level": 3,
      "tryouts": [],
      "uid": 22325,
      "priority": 986532,
      "created_by": {
        "username": "silverbolt",
        "user_id": "-1"
      },
      "id": "60369b57d23031d14be92c18"
    },
    {
      "created_by": {
        "username": "919821012599_75351",
        "user_id": "5721"
      },
      "slug": "dummy-level-3",
      "level": 3,
      "uid": 22324,
      "is_active": true,
      "media": {
        "landscape": "https://hdn-1.addsale.com/x0/category/pictures/landscape-banner/original/0wCdjxWpI-.png",
        "logo": "https://hdn-1.addsale.com/x0/category/pictures/square-logo/original/EfCt9iXx8-http/d3p8ifzkmzds37.cloudfront.net/media/logo/department/original/15870_c287d3c2431a432bb0e49363ef6b82bc.png.jpeg",
        "portrait": "https://hdn-1.addsale.com/x0/category/pictures/portrait-banner/original/S1axCMOJ4-.png"
      },
      "name": "Dummy level 3 by fahim",
      "tryouts": [
        "Lipstick",
        "Eyeliner"
      ],
      "modified_on": "2021-03-04T15:39:46.246000Z",
      "modified_by": {
        "username": "917753852478_51632",
        "user_id": "5677"
      },
      "synonyms": [],
      "marketplaces": {},
      "created_on": "2021-01-14T05:28:59.852000Z",
      "priority": 986532,
      "hierarchy": [
        {
          "l2": 22323,
          "l1": 22322,
          "department": 21
        },
        {
          "l2": 3732,
          "l1": 3672,
          "department": 4
        },
        {
          "l2": 730,
          "l1": 595,
          "department": 2
        }
      ],
      "departments": [
        2,
        4,
        21
      ],
      "id": "5fffd69be64eb40001fc8a65"
    },
    {
      "uid": 3151,
      "departments": [
        4
      ],
      "is_active": true,
      "level": 1,
      "media": {
        "logo": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/YHIeoQ_fruit___vegetable_logo.jpg16aab608-a78a-458f-b60b-524525f27dec/YHIeoQ_fruit___vegetable_logo.jpg",
        "portrait": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/ywPVrU_preview_a637ca6e4da6e38f03eb0d650ac5d6ba.jpgc73cc22f-b5ee-4fd4-a585-8ada35762d68/ywPVrU_preview_a637ca6e4da6e38f03eb0d650ac5d6ba.jpg",
        "landscape": "https://hdn-1.addsale.com/x0/seller/pictures/logo/original/ywPVrU_preview_a637ca6e4da6e38f03eb0d650ac5d6ba.jpgc73cc22f-b5ee-4fd4-a585-8ada35762d68/ywPVrU_preview_a637ca6e4da6e38f03eb0d650ac5d6ba.jpg"
      },
      "name": "Gourmet & World Food",
      "priority": 123,
      "slug": "gourmet-world-food",
      "synonyms": [
        "gourmet & world food",
        "food",
        "gourmet"
      ],
      "created_on": "2016-04-09T06:44:35Z",
      "hierarchy": [],
      "modified_by": {
        "username": "917753852478_51632",
        "uid": "5677"
      },
      "modified_on": "2021-03-03T09:35:50.415000Z",
      "id": "5fabab8ea18a1284b97ff6c4"
    },
    {
      "modified_by": {
        "username": "917753852478_51632",
        "uid": "5677"
      },
      "marketplaces": {},
      "hierarchy": [
        {
          "l1": 595,
          "l2": 714,
          "department": 2
        },
        {
          "l1": 2,
          "l2": 4,
          "department": 1
        }
      ],
      "created_on": "2021-03-03T06:30:08.342000Z",
      "created_by": {
        "username": "917753852478_51632",
        "uid": "5677"
      },
      "level": 3,
      "name": "Test Category kaf",
      "media": {
        "landscape": "https://hdn-1.addsale.com/x0/category/pictures/landscape-banner/original/0wCdjxWpI-.png",
        "logo": "https://hdn-1.addsale.com/x0/category/pictures/square-logo/original/EfCt9iXx8-http/d3p8ifzkmzds37.cloudfront.net/media/logo/department/original/15870_c287d3c2431a432bb0e49363ef6b82bc.png.jpeg",
        "portrait": "https://hdn-1.addsale.com/x0/category/pictures/portrait-banner/original/VKqwRngFh-.png"
      },
      "tryouts": [
        "Lipstick",
        "Blush"
      ],
      "is_active": true,
      "slug": "test-category-kaf",
      "uid": 22328,
      "synonyms": [
        "test",
        "category"
      ],
      "priority": 23,
      "departments": [
        1,
        2
      ],
      "modified_on": "2021-03-03T08:34:47.999000Z",
      "id": "603f2cf0aac0360001c00731"
    },
    {
      "level": 3,
      "departments": [
        1
      ],
      "is_active": false,
      "created_by": {
        "username": "silverbolt",
        "user_id": "-1"
      },
      "created_on": "2021-02-25T09:26:53.123000Z",
      "tryouts": [],
      "slug": "smart-cell",
      "marketplaces": {},
      "priority": 5,
      "media": {
        "portrait": "http://cdn4.gofynd.com/media/logo/department/original/13239_660c6f5b2b8d458789de4552d241ea1b.jpg",
        "landscape": "https://hdn-1.fynd.com/media/banner/category/original/16128_380bed8bff064a0b981041df65e0d8b3.jpg",
        "logo": "http://d3p8ifzkmzds37.cloudfront.net/media/logo/department/original/15870_c287d3c2431a432bb0e49363ef6b82bc.png"
      },
      "modified_on": "2021-02-25T09:26:53.123000Z",
      "synonyms": [],
      "uid": 22327,
      "hierarchy": [
        {
          "l1": 2,
          "l2": 3,
          "department": 1
        }
      ],
      "name": "Smart Cell",
      "modified_by": {
        "username": "silverbolt",
        "user_id": "-1"
      },
      "id": "60372005d230311fe9e51f0b"
    },
    {
      "is_active": true,
      "hierarchy": [
        {
          "department": 21,
          "l1": 22322,
          "l2": 22323
        }
      ],
      "slug": "dummy-level-98",
      "priority": 986532,
      "uid": 22326,
      "departments": [
        21
      ],
      "created_by": {
        "username": "silverbolt",
        "user_id": "-1"
      },
      "modified_on": "2021-02-25T00:09:35.026000Z",
      "marketplaces": {},
      "tryouts": [],
      "synonyms": [],
      "media": {
        "landscape": "https://hdn-1.addsale.com/x0/category/pictures/landscape-banner/original/0wCdjxWpI-.png",
        "portrait": "https://hdn-1.addsale.com/x0/category/pictures/portrait-banner/original/S1axCMOJ4-.png",
        "logo": "https://hdn-1.addsale.com/x0/category/pictures/square-logo/original/EfCt9iXx8-http/d3p8ifzkmzds37.cloudfront.net/media/logo/department/original/15870_c287d3c2431a432bb0e49363ef6b82bc.png.jpeg"
      },
      "level": 3,
      "name": "Dummy level 98",
      "created_on": "2021-02-25T00:09:35.026000Z",
      "modified_by": {
        "username": "silverbolt",
        "user_id": "-1"
      },
      "id": "60369d67d2303111b8924dcf"
    },
    {
      "uid": 315,
      "created_on": "2016-04-09T06:44:35Z",
      "departments": [
        2,
        3
      ],
      "hierarchy": [
        {
          "l1": 65,
          "l2": 66,
          "department": 2
        },
        {
          "l1": 442,
          "l2": 26,
          "department": 2
        },
        {
          "l1": 442,
          "l2": 26,
          "department": 3
        }
      ],
      "is_active": true,
      "level": 3,
      "marketplaces": {},
      "media": {
        "landscape": "https://hdn-1.fynd.com/media/banner/category/original/19961_f042f1f4a90f4e828b6d77d6dbea264d.jpg",
        "logo": "https://hdn-1.fynd.com/media/logo/category/original/81ef023d375044e9b9daa66b81ec411f.jpg",
        "portrait": "https://hdn-1.fynd.com/media/banner_portrait/category/original/19960_c679d51cb1bd4ca99f00f9050aa647a4.jpg"
      },
      "modified_by": {
        "username": "917753852478_51632",
        "user_id": "5677"
      },
      "modified_on": "2021-02-15T15:48:05.329000Z",
      "name": "Sports Bra",
      "priority": 281,
      "slug": "sports-bra",
      "synonyms": [
        "Sports Bra",
        "activewear bra",
        "gym bra"
      ],
      "tryouts": [],
      "id": "5fdba984642de8d93efb0d71"
    }
  ]
}
```
</details>









---


#### createCategories
Create product categories




```kotlin
client.catalog.createCategories(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |  
| body | [CategoryRequestBody](#CategoryRequestBody) | yes | Request body |


This API lets user create product categories

*Returned Response*




[CategoryCreateResponse](#CategoryCreateResponse)

Category Meta. See example below or refer `CategoryCreateResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "message": "Success",
  "uid": 0
}
```
</details>









---


#### getCategoryData
Get product category by uid




```kotlin
client.catalog.getCategoryData(uid: uid).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| uid | String | yes | Category unique id |  



This API gets meta associated to product categories.

*Returned Response*




[SingleCategoryResponse](#SingleCategoryResponse)

Get Data for one category. See example below or refer `CategoryResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "data": {
    "name": "Air Conditioners",
    "media": {
      "portrait": "https://hdn-1.addsale.com/x0/category/pictures/portrait-banner/original/_4p7Kz9Yp-banner.png",
      "landscape": "https://hdn-1.addsale.com/x0/category/pictures/landscape-banner/original/nsi0nJ6gX-landscape.png",
      "logo": "https://hdn-1.addsale.com/x0/category/pictures/square-logo/original/zTgh1zslj-.png"
    },
    "marketplaces": {},
    "tryouts": [],
    "is_active": true,
    "created_by": {
      "username": "917972410891_48194",
      "user_id": "5646"
    },
    "uid": 22330,
    "slug": "air-conditioners",
    "priority": 1,
    "synonyms": [],
    "modified_by": {
      "username": "nikhilmhatre_gofynd_com_97636",
      "user_id": "16"
    },
    "level": 3,
    "hierarchy": [
      {
        "l1": 1,
        "department": 1,
        "l2": 22329
      }
    ],
    "created_on": "2021-04-02T15:43:59.410000Z",
    "departments": [
      1
    ],
    "modified_on": "2021-04-13T13:57:56.443000Z",
    "id": "60673bbf7896da00017885ad"
  }
}
```
</details>









---


#### updateCategory
Update product categories




```kotlin
client.catalog.updateCategory(uid: uid, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| uid | String | yes | Category unique id |  
| body | [CategoryRequestBody](#CategoryRequestBody) | yes | Request body |


Update a product category using this apu

*Returned Response*




[CategoryUpdateResponse](#CategoryUpdateResponse)

Category Meta. See example below or refer `CategoryUpdateResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### getProducts
Get product list




```kotlin
client.catalog.getProducts(brandIds: brandIds, categoryIds: categoryIds, itemIds: itemIds, departmentIds: departmentIds, itemCode: itemCode, q: q, pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Get list of products filtered by company Id |   
| brandIds | ArrayList<Int>? | no | Get multiple products filtered by Brand Ids |   
| categoryIds | ArrayList<Int>? | no | Get multiple products filtered by Category Ids |   
| itemIds | ArrayList<Int>? | no | Get multiple products filtered by Item Ids |   
| departmentIds | ArrayList<Int>? | no | Get multiple products filtered by Department Ids |   
| itemCode | ArrayList<Double>? | no | Get multiple products filtered by Item Code |   
| q | String? | no | Get multiple products filtered by q string |   
| pageNo | Int? | no | The page number to navigate through the given set of results |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 10. |  



This API gets meta associated to products.

*Returned Response*




[ProductListingResponse](#ProductListingResponse)

Product Meta. See example below for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "name": "TV Set",
      "description": "Tv",
      "country_of_origin": "India",
      "currency": "INR",
      "short_description": "",
      "is_set": true,
      "item_code": "TVSET111",
      "brand_uid": 1,
      "template_tag": "television",
      "highlights": [
        "42 Inch"
      ],
      "slug": "tv-set",
      "_custom_json": {},
      "l3_mapping": [
        "electronics>qled_television"
      ],
      "image_nature": "standard",
      "departments": [
        1
      ],
      "created_on": 1599024995,
      "created_by": {
        "username": "919049753052_37528",
        "user_id": "5"
      },
      "modified_on": 1627642010,
      "modified_by": {
        "username": "xxxxxxxxxx",
        "user_id": "xxxxxxxxxxx"
      },
      "stage": "verified",
      "uid": 7501547,
      "verified_by": {
        "username": "Silverbolt",
        "user_id": "0"
      },
      "verified_on": 1626965521,
      "all_sizes": [
        {
          "item_code": "TVSET111",
          "brand_uid": 1,
          "seller_identifier": "HGS272727272",
          "identifiers": [
            {
              "gtin_type": "ean",
              "gtin_value": "HGS272727272",
              "primary": true
            }
          ],
          "company_id": 1,
          "size": "XXLX23, MX11, LX67, XLX45 (146 PCS)",
          "marked_price": 35000
        }
      ],
      "category_slug": "qled-television",
      "is_image_less_product": false,
      "media": [
        {
          "url": "https://hdn-1.addsale.com/x0/products/pictures/item/free/135x0/dcizgsG_Y-Tv-Set.png",
          "type": "image"
        }
      ],
      "variants": {},
      "product_publish": {
        "is_set": false,
        "product_online_date": 1627642009
      },
      "is_dependent": false,
      "is_physical": true,
      "item_type": "set",
      "category_uid": 1,
      "custom_order": {
        "manufacturing_time": 2,
        "is_custom_order": true,
        "manufacturing_time_unit": "days"
      },
      "moq": {
        "minimum": 1,
        "is_set": false
      },
      "multi_size": true,
      "no_of_boxes": 1,
      "product_group_tag": [],
      "size_guide": "slim-fit-shirts-for-men",
      "tags": [],
      "teaser_tag": {},
      "synonyms": [],
      "hsn_code": "11111111",
      "return_config": {
        "unit": "days",
        "returnable": false,
        "time": 0
      },
      "all_company_ids": [
        1
      ],
      "all_identifiers": [
        "19WE100"
      ],
      "trader": {
        "address": "sdfdsfsdf",
        "name": "asdasd"
      },
      "trader_type": "Packer",
      "verification_status": "pending",
      "sizes": [
        {
          "size": "FGX33, GHX33 (66 PCS)",
          "store_count": 1
        },
        {
          "size": "XSE WE23X100 (100 PCS)",
          "store_count": 2
        },
        {
          "size": "XSEX100 (100 PCS)",
          "store_count": 3
        },
        {
          "size": "XXLX23, MX11, LX67, XLX45 (146 PCS)",
          "store_count": 3
        }
      ],
      "id": "5f4f2f6371a5970001f13655",
      "brand": {
        "name": "Apple",
        "logo": {
          "aspect_ratio": "1:1",
          "aspect_ratio_f": 1,
          "url": "https://hdn-1.jiox0.de/jioecomm/seller/pictures/logo/50x0/apple-7f951c/logo_apple.png",
          "secure_url": "https://hdn-1.jiox0.de/jioecomm/seller/pictures/logo/50x0/apple-7f951c/logo_apple.png"
        },
        "uid": 13
      },
      "images": [
        {
          "aspect_ratio": "16:25",
          "aspect_ratio_f": 0.64,
          "url": "https://hdn-1.addsale.com/x0/products/pictures/item/free/135x0/dcizgsG_Y-Tv-Set.png",
          "secure_url": "https://hdn-1.addsale.com/x0/products/pictures/item/free/135x0/dcizgsG_Y-Tv-Set.png"
        }
      ],
      "price": {
        "marked": {
          "min": 35000,
          "max": 35000
        },
        "effective": {
          "min": 25000,
          "max": 25000
        }
      }
    }
  ],
  "page": {
    "type": "number",
    "current": 1,
    "size": 1,
    "item_total": 1,
    "has_previous": false,
    "has_next": false
  }
}
```
</details>









---


#### createProduct
Create a product.




```kotlin
client.catalog.createProduct(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Id of the company associated to product that is to be viewed. |  
| body | [ProductCreateUpdate](#ProductCreateUpdate) | yes | Request body |


This API allows to create product.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### deleteProduct
Delete a product.




```kotlin
client.catalog.deleteProduct(itemId: itemId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id of the company associated to product that is to be deleted. |   
| itemId | Int | yes | Id of the product to be updated. |  



This API allows to delete product.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### getProduct
Get a single product.




```kotlin
client.catalog.getProduct(itemCode: itemCode, itemId: itemId, brandUid: brandUid, uid: uid).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| itemCode | String? | no | Item code of the product. |   
| companyId | Int | yes | Company Id of the product. |   
| itemId | Int | yes | Item Id of the product. |   
| brandUid | Int? | no | Brand Id of the product. |   
| uid | Int? | no | Id of the product. |  



This API helps to get data associated to a particular product.

*Returned Response*




[Product](#Product)

Product object. See example below or refer `product.utils.format_product_response` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "data": {
    "template_tag": "industrial-supplies",
    "brand_uid": 1486,
    "currency": "INR",
    "item_code": "TP_FS_01",
    "slug": "printed-fyndstore-packaging-tape-4inch-x-6-meter-length-pack-of-2-49d7343fc677",
    "name": "Printed Fyndstore Packaging Tape (4inch X 6 Meter length) - Pack of 2",
    "hsn_code": "48190000",
    "country_of_origin": "India",
    "description": "FyndStore 4 inch Printed BOPP Tapes ",
    "is_set": true,
    "is_active": true,
    "departments": [
      11
    ],
    "uid": 1282497,
    "category_slug": "printed-tape",
    "company_id": 884,
    "media": [
      {
        "url": "https://hdn-1.fynd.com/media/pictures/tagged_items/original/TPFS01/IMG20200624130956.jpg",
        "type": "image"
      }
    ],
    "variants": {},
    "is_dependent": false,
    "item_type": "set",
    "multi_size": true,
    "product_publish": {
      "is_set": false,
      "product_online_date": "2020-09-10T15:16:12.322000Z"
    },
    "id": "5f5a433c74f3f400017cdaa0",
    "brand": {
      "name": "RollUp",
      "logo": {
        "aspect_ratio": "1:1",
        "aspect_ratio_f": 1,
        "url": "https://hdn-1.fynd.com/brands/pictures/square-logo/50x0/mPBaWqGRnjR-RMOnlpdMPKm-yjn5mua63gfmzdpombb1.png",
        "secure_url": "https://hdn-1.fynd.com/brands/pictures/square-logo/50x0/mPBaWqGRnjR-RMOnlpdMPKm-yjn5mua63gfmzdpombb1.png"
      },
      "uid": 1486
    },
    "return_config": {
      "returnable": true,
      "time": 30,
      "unit": "days"
    },
    "sizes": [
      {
        "item_dimensions_unit_of_measure": "cm",
        "item_weight": 0.15,
        "set": {
          "quantity": 1,
          "size_distribution": {
            "sizes": [
              {
                "pieces": 1,
                "size": "OS"
              }
            ]
          }
        },
        "item_height": 10.16,
        "item_width": 10.16,
        "price_effective": 999,
        "size": "OS",
        "seller_identifier": "TP_FS_01",
        "brand_uid": 1486,
        "price": 1000,
        "item_weight_unit_of_measure": "gram",
        "currency": "INR",
        "item_length": 10.16,
        "item_code": "TP_FS_01",
        "company_id": 884,
        "is_set": true,
        "track_inventory": true,
        "identifiers": [
          {
            "gtin_value": "TP_FS_01",
            "primary": true,
            "gtin_type": "sku_code"
          }
        ],
        "price_transfer": 0,
        "id": "5f5a433c74f3f400017cdaa1",
        "store_count": 1
      }
    ],
    "attributes": {
      "style": "TPFS01",
      "color": "White",
      "pallet": 1,
      "l3_mapping": [
        "industrial_supplies>printed_tape"
      ],
      "image_nature": "standard",
      "created_on": "2020-09-10T15:16:12.322000Z",
      "created_by": {
        "username": "sumitdafda_gofynd_com_68387",
        "user_id": "23108029",
        "company_id": 884
      },
      "modified_on": "2020-09-24T04:51:00.229000Z",
      "modified_by": {
        "username": "sumitdafda_gofynd_com_68387",
        "user_id": "23108029",
        "company_id": 884
      },
      "stage": "verified",
      "verified_by": {
        "username": "sumitdafda_gofynd_com_68387",
        "user_id": "23108029",
        "company_id": 884
      },
      "verified_on": 1600923060,
      "is_image_less_product": false,
      "other_available_sizes": []
    }
  }
}
```
</details>









---


#### editProduct
Edit a product.




```kotlin
client.catalog.editProduct(itemId: itemId, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Id of the company associated to product that is to be viewed. |   
| itemId | Int | yes | Id of the product to be updated. |  
| body | [ProductCreateUpdate](#ProductCreateUpdate) | yes | Request body |


This API allows to edit product.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "uid": 1,
  "success": true
}
```
</details>









---


#### getProductValidation
Validate product/size data




```kotlin
client.catalog.getProductValidation().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Validates data against given company |  



This API validates product data.

*Returned Response*




[ValidateProduct](#ValidateProduct)

Validate Meta. See example below for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "valid": true
}
```
</details>









---


#### getProductSize
Get a single product size.




```kotlin
client.catalog.getProductSize(itemCode: itemCode, itemId: itemId, brandUid: brandUid, uid: uid).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| itemCode | String? | no | Item code of the product size. |   
| companyId | Int | yes | Company Id of the product size. |   
| itemId | Int | yes | Item Id of the product size. |   
| brandUid | Int? | no | Brand Id of the product size. |   
| uid | Int? | no | Id of the product size. |  



This API helps to get data associated to a particular product size.

*Returned Response*




[ProductListingResponse](#ProductListingResponse)

Product object. See example below for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "name": "SQUADMTGIVESPACE",
  "country_of_origin": "India",
  "highlights": null,
  "hsn_code": "61099090",
  "item_code": "ACTESTCREATELISTING1",
  "is_set": false,
  "description": "",
  "currency": "INR",
  "slug": "play-clan-squadmtgivespace-857587-e928b0",
  "template_tag": "topwear",
  "is_active": false,
  "departments": [
    1
  ],
  "uid": 857587,
  "all_sizes": [
    "3XL"
  ],
  "category_slug": "t-shirts",
  "company_id": 61,
  "media": [],
  "size_guide": "play-clan-men-casual-tees",
  "is_dependent": false,
  "item_type": "standard",
  "multi_size": true,
  "product_publish": {
    "is_set": false,
    "product_online_date": 1595478043
  },
  "id": "5f19101b99ee0500011dc896",
  "brand": {
    "name": "play clan",
    "logo": {
      "aspect_ratio": "1:1",
      "aspect_ratio_f": 1,
      "url": "https://hdn-1.fynd.com/brands/pictures/square-logo/50x0/zjt4-wU8Lk-VQYu0pcokb-r6yteuannoorjkq9f4tk.jpg",
      "secure_url": "https://hdn-1.fynd.com/brands/pictures/square-logo/50x0/zjt4-wU8Lk-VQYu0pcokb-r6yteuannoorjkq9f4tk.jpg"
    },
    "uid": 85
  },
  "images": [],
  "sizes": [
    {
      "price_transfer": 0,
      "price_effective": 10000,
      "price": 10000,
      "currency": "INR",
      "is_set": false,
      "size": "3XL",
      "identifiers": [
        {
          "gtin_type": "sku_code",
          "gtin_value": "ACTESTCREATELISTING1_3XL",
          "primary": true
        }
      ]
    }
  ],
  "attributes": {
    "essential": "Yes",
    "color": "Red",
    "gender": [
      "Men"
    ],
    "material": "cotton",
    "pattern": "Printed",
    "product_fit": "Regular",
    "sleeve_length": "Short",
    "neck_type": "Round Neck",
    "primary_color": "Red",
    "primary_material": "Others",
    "l3_mapping": [
      "men>casual_tees",
      "women>casual_tees",
      "girls>casual_tees",
      "more>casual_tees"
    ],
    "image_nature": "standard",
    "meta_nature": "standard",
    "created_on": "2020-07-23T04:20:43.810000Z",
    "created_by": {
      "username": "silverbolt",
      "user_id": "-1",
      "company_id": 1181
    },
    "modified_on": "2020-07-23T04:20:44.185000Z",
    "modified_by": {
      "username": "silverbolt",
      "user_id": "-1",
      "company_id": 61
    },
    "stage": "verified",
    "verified_by": {
      "username": "Silverbolt",
      "user_id": "0"
    },
    "verified_on": 1595478044,
    "is_image_less_product": false
  }
}
```
</details>









---


#### getProductBulkUploadHistory
Get a list of all bulk product upload jobs.




```kotlin
client.catalog.getProductBulkUploadHistory(pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Company Id of of which Product Bulk Upload History to be obtained. |   
| pageNo | Int? | no | The page number to navigate through the given set of results |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 12. |  



This API helps to get bulk product upload jobs data.

*Returned Response*




[ProductBulkRequestList](#ProductBulkRequestList)

List of bulk product upload jobs. See `BulkRequestGetSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "stage": "completed",
      "company_id": 61,
      "is_active": true,
      "cancelled_records": [],
      "failed": 0,
      "template_tag": "footwear",
      "modified_on": "2021-03-12T08:11:08.646000Z",
      "created_on": "2021-03-12T08:11:06.848000Z",
      "failed_records": [],
      "created_by": {
        "username": "yadavanuja039_gmail_com_82948",
        "user_id": "23218433",
        "full_name": "Anuja Yadav"
      },
      "total": 1,
      "file_path": "https://hdn-1.fynd.com/company/61/self/documents/product-import/free/original/mkX5ApRmw-sample_bulk_products_footwear.xlsx",
      "succeed": 1,
      "modified_by": {
        "username": "Silverbolt",
        "user_id": "0"
      },
      "cancelled": 0,
      "template": {
        "name": "Footwear",
        "banner": "https://hdn-1.fynd.com/seller/pictures/landscape-banner/original/nFPtXR_Beauty_&_Personal_Care_L.jpgf30455a5-d265-4382-b513-65afb9240320/nFPtXR_Beauty_and_Personal_Care_L.jpg",
        "slug": "footwear",
        "logo": "https://hdn-1.fynd.com/seller/pictures/logo/original/9Y2UEp_ssssss.jpg7359e4c6-4c53-4dbe-a920-ef8ac658afb1/9Y2UEp_ssssss.jpg",
        "departments": [
          "men",
          "women",
          "kids",
          "fashion"
        ],
        "description": "Footwear is a garment worn on the feet to protect against environmental adversities like heat or ground textures. Example: Sports Shoes"
      },
      "id": "604b221a73bfa20001cb00e8"
    }
  ],
  "page": {
    "current": 1,
    "size": 26,
    "has_previous": false,
    "has_next": true,
    "item_total": 251
  }
}
```
</details>









---


#### updateProductAssetsInBulk
Create a Bulk asset upload Job.




```kotlin
client.catalog.updateProductAssetsInBulk(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Company Id in which assets to be uploaded. |  
| body | [BulkJob](#BulkJob) | yes | Request body |


This API helps to create a bulk asset upload job.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### createProductsInBulk
Create products in bulk associated with given batch Id.




```kotlin
client.catalog.createProductsInBulk(batchId: batchId, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Company Id in which assets to be uploaded. |   
| batchId | String | yes | Batch Id in which assets to be uploaded. |  
| body | [BulkProductRequest](#BulkProductRequest) | yes | Request body |


This API helps to create products in bulk push to kafka for approval/creation.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### deleteProductBulkJob
Delete Bulk product job.




```kotlin
client.catalog.deleteProductBulkJob(batchId: batchId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id of the company associated to size that is to be deleted. |   
| batchId | Int | yes | Batch Id of the bulk product job to be deleted. |  



This API allows to delete bulk product job associated with company.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### getCompanyTags
Get a list of all tags associated with company.




```kotlin
client.catalog.getCompanyTags().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Company Id of the product size. |  



This API helps to get tags data associated to a particular copmpany.

*Returned Response*




[ProductTagsViewResponse](#ProductTagsViewResponse)

Tag List. See example below for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": {
    "tags": [
      "demo",
      "custom"
    ]
  }
}
```
</details>









---


#### getProductAssetsInBulk
Get a list of all bulk asset jobs.




```kotlin
client.catalog.getProductAssetsInBulk(pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Company Id of the product size. |   
| pageNo | Int? | no | The page number to navigate through the given set of results |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 12. |  



This API helps to get bulk asset jobs data associated to a particular company.

*Returned Response*




[BulkAssetResponse](#BulkAssetResponse)

List of bulk asset jobs List. See `BulkUtil.modify_batch_response` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "created_on": "2021-02-25T16:45:22.425000Z",
      "file_path": "https://hdn-1.fynd.com/company/61/self/documents/product-import/free/original/ZUSmmXHmZ-U8mTYx3KR-Nike-hoddie.zip",
      "succeed": 1,
      "cancelled_records": [],
      "failed": 0,
      "failed_records": [],
      "stage": "completed",
      "is_active": true,
      "modified_by": {
        "user_id": "23175373",
        "username": "nikhilmhatre_gofynd_com_28085_23175373"
      },
      "modified_on": "2021-02-25T16:47:24.551000Z",
      "retry": 1,
      "total": 1,
      "company_id": 61,
      "created_by": {
        "user_id": "23175373",
        "username": "nikhilmhatre_gofynd_com_28085_23175373",
        "full_name": "nikhil mhatre"
      },
      "cancelled": 0,
      "tracking_url": "https://api.fynd.com/common/assets/v1/asset/status/extract-zips/3296",
      "id": "6037d422aa879600015c6d1d"
    }
  ],
  "page": {
    "current": 1,
    "size": 3,
    "has_previous": false,
    "has_next": false,
    "item_total": 1
  }
}
```
</details>









---


#### createProductAssetsInBulk
Create a Bulk asset upload Job.




```kotlin
client.catalog.createProductAssetsInBulk(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Company Id in which assets to be uploaded. |  
| body | [ProductBulkAssets](#ProductBulkAssets) | yes | Request body |


This API helps to create a bulk asset upload job.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### deleteSize
Delete a Size associated with product.




```kotlin
client.catalog.deleteSize(itemId: itemId, size: size).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id of the company associated to size that is to be deleted. |   
| itemId | Int | yes | Item Id of the product associated with size to be deleted. |   
| size | Int | yes | size to be deleted. |  



This API allows to delete size associated with product.

*Returned Response*




[ProductSizeDeleteResponse](#ProductSizeDeleteResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### getInventoryBySize
Get Inventory for company




```kotlin
client.catalog.getInventoryBySize(itemId: itemId, size: size, pageNo: pageNo, pageSize: pageSize, q: q).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Id of the company associated to product that is to be viewed. |   
| itemId | String | yes | Item code of the product of which size is to be get. |   
| size | String | yes | Size of which inventory is to get. |   
| pageNo | Int? | no | The page number to navigate through the given set of results |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 12. |   
| q | String? | no | Search with help of store code. |  



This API allows get Inventory data for particular company grouped by size and store.

*Returned Response*




[InventoryResponse](#InventoryResponse)

returns a list of all inventory grouped by size and store




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "store": {
        "name": "yosss sdd dsdyo",
        "store_code": "sanic6sdfsf7",
        "uid": 59,
        "address": {
          "state": "MAHARASHTRA",
          "address1": "A/204, SAI VANDAN, NARAYAN NAGAR, TULINJ ROAD",
          "lat_long": {
            "type": "Point",
            "coordinates": [
              72.8231511,
              19.4232024
            ]
          },
          "address2": "",
          "pincode": 401209,
          "country": "INDIA",
          "city": "MUMBAI",
          "landmark": ""
        },
        "manager": {
          "name": "abc",
          "email": "a@b.com",
          "mobile_no": {
            "number": "2382634324",
            "country_code": 91
          }
        },
        "integration_type": {
          "order": "browntape",
          "inventory": "browntape"
        },
        "_custom_json": {}
      },
      "uid": "59_RTYUIDSDFV",
      "size": "AAX1 (1 PCS)",
      "inventory_updated_on": "2021-04-06T03:30:01.487000",
      "seller_identifier": "RTYUIDSDFV",
      "item_id": 7500651,
      "quantity": 10,
      "price": 1234,
      "price_effective": 1234,
      "price_transfer": 0,
      "currency": "INR",
      "sellable_quantity": 10,
      "identifiers": [
        {
          "gtin_type": "sku_code",
          "gtin_value": "RTYUIDSDFV",
          "primary": true
        }
      ]
    },
    {
      "store": {
        "name": "Saran Ledonne",
        "store_code": "af6198fe-2c23-4441-bbf4-e694c96e255c",
        "uid": 10,
        "address": {
          "state": "MAHA",
          "address1": "NO",
          "lat_long": {
            "type": "Point",
            "coordinates": [
              1,
              1
            ]
          },
          "address2": "",
          "pincode": 400072,
          "country": "INDIA",
          "city": "MUMBAI"
        },
        "manager": {
          "name": "abc",
          "email": "rehman@cashkart.com",
          "mobile_no": {
            "number": "9167943983",
            "country_code": 91
          }
        },
        "integration_type": {
          "order": "browntape",
          "inventory": "browntape"
        },
        "_custom_json": {}
      },
      "uid": "10_RTYUIDSDFV",
      "size": "AAX1 (1 PCS)",
      "inventory_updated_on": "2021-04-06T03:29:35.291000",
      "seller_identifier": "RTYUIDSDFV",
      "item_id": 7500651,
      "quantity": 10,
      "price": 1234,
      "price_effective": 1234,
      "price_transfer": 0,
      "currency": "INR",
      "sellable_quantity": 10,
      "identifiers": [
        {
          "gtin_type": "sku_code",
          "gtin_value": "RTYUIDSDFV",
          "primary": true
        }
      ]
    },
    {
      "store": {
        "name": "ABC-1-17",
        "store_code": "ABC-1-17",
        "uid": 11061,
        "address": {
          "state": "MAHARASHTRA",
          "address1": "14/1, VINOBHA BHAVE NAGAR",
          "lat_long": {
            "type": "Point",
            "coordinates": [
              1,
              1
            ]
          },
          "address2": "VINOBHA BHAVE NAGAR, KURLA WEST, KURLA, ",
          "pincode": 400070,
          "country": "INDIA",
          "city": "MUMBAI"
        },
        "manager": {
          "name": "Fahim",
          "email": "fahimsakri@gofynd.com",
          "mobile_no": {
            "number": "9594495254",
            "country_code": 91
          }
        },
        "integration_type": {
          "order": "browntape",
          "inventory": "browntape"
        },
        "_custom_json": {}
      },
      "uid": "11061_RTYUIDSDFV",
      "size": "AAX1 (1 PCS)",
      "inventory_updated_on": "2021-03-17T12:35:29.992000",
      "seller_identifier": "RTYUIDSDFV",
      "item_id": 7500651,
      "quantity": 10000000,
      "price": 1234,
      "price_effective": 1234,
      "price_transfer": 0,
      "currency": "INR",
      "sellable_quantity": 10000000,
      "order_committed_quantity": 0,
      "identifiers": [
        {
          "gtin_type": "sku_code",
          "gtin_value": "RTYUIDSDFV",
          "primary": true
        }
      ]
    },
    {
      "store": {
        "name": "RRL01",
        "store_code": "WH_8513",
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
        "manager": {
          "name": "ASHISH CHANDORKAR",
          "email": "ASHISHCHANDORKAR@FYND.COM",
          "mobile_no": {
            "number": "8369782851",
            "country_code": 91
          }
        },
        "integration_type": {
          "order": "browntape",
          "inventory": "browntape"
        },
        "_custom_json": {}
      },
      "uid": "1_RTYUIDSDFV",
      "size": "AAX1 (1 PCS)",
      "inventory_updated_on": "2021-03-31T19:00:10.943000",
      "seller_identifier": "RTYUIDSDFV",
      "item_id": 7500651,
      "quantity": 39,
      "price": 1234,
      "price_effective": 1234,
      "price_transfer": 0,
      "currency": "INR",
      "sellable_quantity": 18,
      "order_committed_quantity": 7,
      "not_available_quantity": 0,
      "damaged_quantity": 0,
      "identifiers": [
        {
          "gtin_type": "sku_code",
          "gtin_value": "RTYUIDSDFV",
          "primary": true
        }
      ]
    },
    {
      "store": {
        "name": "RRL01",
        "store_code": "WH_8513",
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
        "manager": {
          "name": "ASHISH CHANDORKAR",
          "email": "ASHISHCHANDORKAR@FYND.COM",
          "mobile_no": {
            "number": "8369782851",
            "country_code": 91
          }
        },
        "integration_type": {
          "order": "browntape",
          "inventory": "browntape"
        },
        "_custom_json": {}
      },
      "uid": "1_rtyuidsdfv",
      "size": "AAX1 (1 PCS)",
      "inventory_updated_on": "2020-07-07T10:37:06.146000",
      "seller_identifier": "RTYUIDSDFV",
      "item_id": 7500651,
      "quantity": 39,
      "price": 1234,
      "price_effective": 1234,
      "price_transfer": 0,
      "currency": "INR",
      "sellable_quantity": 0,
      "order_committed_quantity": 39,
      "identifiers": [
        {
          "gtin_type": "sku_code",
          "gtin_value": "RTYUIDSDFV",
          "primary": true
        }
      ]
    }
  ],
  "page": {
    "type": "number",
    "current": 1,
    "size": 1,
    "item_total": 5,
    "has_previous": false,
    "has_next": false
  }
}
```
</details>









---


#### addInventory
Add Inventory for particular size and store.




```kotlin
client.catalog.addInventory(itemId: itemId, size: size, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Id of the company associated to product that is to be viewed. |   
| itemId | Double | yes | Item code of the product of which size is to be get. |   
| size | String | yes | Size in which inventory is to be added. |  
| body | [InventoryRequest](#InventoryRequest) | yes | Request body |


This API allows add Inventory for particular size and store.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### getInventoryBySizeIdentifier
Get Inventory for company




```kotlin
client.catalog.getInventoryBySizeIdentifier(itemId: itemId, sizeIdentifier: sizeIdentifier, pageNo: pageNo, pageSize: pageSize, q: q, locationIds: locationIds).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Id of the company associated to product that is to be viewed. |   
| itemId | String | yes | Item code of the product of which size is to be get. |   
| sizeIdentifier | String | yes | Size Identifier (Seller Identifier or Primary Identifier) of which inventory is to get. |   
| pageNo | Int? | no | The page number to navigate through the given set of results |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 12. |   
| q | String? | no | Search with help of store code. |   
| locationIds | ArrayList<Int>? | no | Search by store ids. |  



This API allows get Inventory data for particular company grouped by size and store.

*Returned Response*




[InventoryResponse](#InventoryResponse)

returns a list of all inventory grouped by size and store




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "store": {
        "name": "yosss sdd dsdyo",
        "store_code": "sanic6sdfsf7",
        "uid": 59,
        "address": {
          "state": "MAHARASHTRA",
          "address1": "A/204, SAI VANDAN, NARAYAN NAGAR, TULINJ ROAD",
          "lat_long": {
            "type": "Point",
            "coordinates": [
              72.8231511,
              19.4232024
            ]
          },
          "address2": "",
          "pincode": 401209,
          "country": "INDIA",
          "city": "MUMBAI",
          "landmark": ""
        },
        "manager": {
          "name": "abc",
          "email": "a@b.com",
          "mobile_no": {
            "number": "2382634324",
            "country_code": 91
          }
        },
        "integration_type": {
          "order": "browntape",
          "inventory": "browntape"
        },
        "_custom_json": {}
      },
      "uid": "59_RTYUIDSDFV",
      "size": "AAX1 (1 PCS)",
      "inventory_updated_on": "2021-04-06T03:30:01.487000",
      "seller_identifier": "RTYUIDSDFV",
      "item_id": 7500651,
      "quantity": 10,
      "price": 1234,
      "price_effective": 1234,
      "price_transfer": 0,
      "currency": "INR",
      "sellable_quantity": 10,
      "identifiers": [
        {
          "gtin_type": "sku_code",
          "gtin_value": "RTYUIDSDFV",
          "primary": true
        }
      ]
    },
    {
      "store": {
        "name": "Saran Ledonne",
        "store_code": "af6198fe-2c23-4441-bbf4-e694c96e255c",
        "uid": 10,
        "address": {
          "state": "MAHA",
          "address1": "NO",
          "lat_long": {
            "type": "Point",
            "coordinates": [
              1,
              1
            ]
          },
          "address2": "",
          "pincode": 400072,
          "country": "INDIA",
          "city": "MUMBAI"
        },
        "manager": {
          "name": "abc",
          "email": "rehman@cashkart.com",
          "mobile_no": {
            "number": "9167943983",
            "country_code": 91
          }
        },
        "integration_type": {
          "order": "browntape",
          "inventory": "browntape"
        },
        "_custom_json": {}
      },
      "uid": "10_RTYUIDSDFV",
      "size": "AAX1 (1 PCS)",
      "inventory_updated_on": "2021-04-06T03:29:35.291000",
      "seller_identifier": "RTYUIDSDFV",
      "item_id": 7500651,
      "quantity": 10,
      "price": 1234,
      "price_effective": 1234,
      "price_transfer": 0,
      "currency": "INR",
      "sellable_quantity": 10,
      "identifiers": [
        {
          "gtin_type": "sku_code",
          "gtin_value": "RTYUIDSDFV",
          "primary": true
        }
      ]
    },
    {
      "store": {
        "name": "ABC-1-17",
        "store_code": "ABC-1-17",
        "uid": 11061,
        "address": {
          "state": "MAHARASHTRA",
          "address1": "14/1, VINOBHA BHAVE NAGAR",
          "lat_long": {
            "type": "Point",
            "coordinates": [
              1,
              1
            ]
          },
          "address2": "VINOBHA BHAVE NAGAR, KURLA WEST, KURLA, ",
          "pincode": 400070,
          "country": "INDIA",
          "city": "MUMBAI"
        },
        "manager": {
          "name": "Fahim",
          "email": "fahimsakri@gofynd.com",
          "mobile_no": {
            "number": "9594495254",
            "country_code": 91
          }
        },
        "integration_type": {
          "order": "browntape",
          "inventory": "browntape"
        },
        "_custom_json": {}
      },
      "uid": "11061_RTYUIDSDFV",
      "size": "AAX1 (1 PCS)",
      "inventory_updated_on": "2021-03-17T12:35:29.992000",
      "seller_identifier": "RTYUIDSDFV",
      "item_id": 7500651,
      "quantity": 10000000,
      "price": 1234,
      "price_effective": 1234,
      "price_transfer": 0,
      "currency": "INR",
      "sellable_quantity": 10000000,
      "order_committed_quantity": 0,
      "identifiers": [
        {
          "gtin_type": "sku_code",
          "gtin_value": "RTYUIDSDFV",
          "primary": true
        }
      ]
    },
    {
      "store": {
        "name": "RRL01",
        "store_code": "WH_8513",
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
        "manager": {
          "name": "ASHISH CHANDORKAR",
          "email": "ASHISHCHANDORKAR@FYND.COM",
          "mobile_no": {
            "number": "8369782851",
            "country_code": 91
          }
        },
        "integration_type": {
          "order": "browntape",
          "inventory": "browntape"
        },
        "_custom_json": {}
      },
      "uid": "1_RTYUIDSDFV",
      "size": "AAX1 (1 PCS)",
      "inventory_updated_on": "2021-03-31T19:00:10.943000",
      "seller_identifier": "RTYUIDSDFV",
      "item_id": 7500651,
      "quantity": 39,
      "price": 1234,
      "price_effective": 1234,
      "price_transfer": 0,
      "currency": "INR",
      "sellable_quantity": 18,
      "order_committed_quantity": 7,
      "not_available_quantity": 0,
      "damaged_quantity": 0,
      "identifiers": [
        {
          "gtin_type": "sku_code",
          "gtin_value": "RTYUIDSDFV",
          "primary": true
        }
      ]
    },
    {
      "store": {
        "name": "RRL01",
        "store_code": "WH_8513",
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
        "manager": {
          "name": "ASHISH CHANDORKAR",
          "email": "ASHISHCHANDORKAR@FYND.COM",
          "mobile_no": {
            "number": "8369782851",
            "country_code": 91
          }
        },
        "integration_type": {
          "order": "browntape",
          "inventory": "browntape"
        },
        "_custom_json": {}
      },
      "uid": "1_rtyuidsdfv",
      "size": "AAX1 (1 PCS)",
      "inventory_updated_on": "2020-07-07T10:37:06.146000",
      "seller_identifier": "RTYUIDSDFV",
      "item_id": 7500651,
      "quantity": 39,
      "price": 1234,
      "price_effective": 1234,
      "price_transfer": 0,
      "currency": "INR",
      "sellable_quantity": 0,
      "order_committed_quantity": 39,
      "identifiers": [
        {
          "gtin_type": "sku_code",
          "gtin_value": "RTYUIDSDFV",
          "primary": true
        }
      ]
    }
  ],
  "page": {
    "type": "number",
    "current": 1,
    "size": 1,
    "item_total": 5,
    "has_previous": false,
    "has_next": false
  }
}
```
</details>









---


#### deleteInventory
Delete a Inventory.




```kotlin
client.catalog.deleteInventory(size: size, itemId: itemId, locationId: locationId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id of the company associated with Inventory that is to be deleted. |   
| size | String | yes | size that is to be deleted. |   
| itemId | Int | yes | Id of the product associated with Inventory to be deleted. |   
| locationId | Double | yes | Location ID of store of which inventory is to be deleted. |  



This API allows to delete inventory of a particular product for particular company.

*Returned Response*




[InventoryDelete](#InventoryDelete)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### getInventoryBulkUploadHistory
Get a list of all bulk Inventory upload jobs.




```kotlin
client.catalog.getInventoryBulkUploadHistory(pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Company Id of of which Inventory Bulk Upload History to be obtained. |   
| pageNo | Int? | no | The page number to navigate through the given set of results |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 12. |  



This API helps to get bulk Inventory upload jobs data.

*Returned Response*




[BulkInventoryGet](#BulkInventoryGet)

List of bulk Inventory upload jobs. See `BulkInventoryGetSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "succeed": 1,
      "stage": "completed",
      "file_path": "https://hdn-1.addsale.com/x0/company/1/self/documents/inventory-import/free/original/50DbgKLND-NtnL_EAVb-REicn1sDv-V8ZrKdnLt-product_inventory.csv",
      "created_on": "2021-03-11T10:54:44.998000Z",
      "cancelled_records": [],
      "created_by": {
        "username": "nikhilmhatre_gofynd_com_97636",
        "user_id": "16",
        "full_name": "Nikhil Mhatre"
      },
      "modified_on": "2021-03-11T10:54:45.296000Z",
      "cancelled": 0,
      "failed": 0,
      "modified_by": {
        "user_id": "0",
        "username": "Silverbolt"
      },
      "company_id": 1,
      "total": 1,
      "is_active": true,
      "failed_records": [],
      "id": "6049f6f5723043000125a9ea"
    },
    {
      "created_by": {
        "username": "silverbolt",
        "user_id": "-1"
      },
      "cancelled": 0,
      "modified_by": {
        "username": "Silverbolt",
        "user_id": "0"
      },
      "created_on": "2021-03-04T09:46:51.714000Z",
      "company_id": 1,
      "failed": 0,
      "failed_records": [],
      "succeed": 1,
      "file_path": "https://hdn-1.addsale.com/x0/company/1/self/documents/inventory-import/free/original/NtnL_EAVb-REicn1sDv-V8ZrKdnLt-product_inventory.csv",
      "cancelled_records": [],
      "total": 1,
      "is_active": true,
      "modified_on": "2021-03-04T09:46:55.349000Z",
      "stage": "completed",
      "id": "6040ac8b1803830001fcc1ed"
    },
    {
      "company_id": 1,
      "failed": 0,
      "modified_by": {
        "user_id": "-1",
        "username": "silverbolt"
      },
      "cancelled": 0,
      "is_active": true,
      "cancelled_records": [],
      "file_path": "https://hdn-1.addsale.com/x0/company/1/self/documents/inventory-import/free/original/bmBZY9iAX-REicn1sDv-V8ZrKdnLt-product_inventory.csv",
      "created_by": {
        "user_id": "-1",
        "username": "silverbolt"
      },
      "modified_on": "2021-03-04T09:22:32.222000Z",
      "succeed": 0,
      "failed_records": [],
      "stage": "terminated",
      "created_on": "2021-03-04T09:22:32.222000Z",
      "total": 1,
      "id": "6040a6d8104f110001a85061"
    },
    {
      "company_id": 1,
      "failed": 0,
      "modified_by": {
        "user_id": "-1",
        "username": "silverbolt"
      },
      "cancelled": 0,
      "is_active": true,
      "cancelled_records": [],
      "file_path": "https://hdn-1.addsale.com/x0/company/1/self/documents/inventory-import/free/original/m73yWRT3v-REicn1sDv-V8ZrKdnLt-product_inventory.csv",
      "created_by": {
        "user_id": "-1",
        "username": "silverbolt"
      },
      "modified_on": "2021-03-04T09:20:29.719000Z",
      "succeed": 0,
      "failed_records": [],
      "stage": "terminated",
      "created_on": "2021-03-04T09:20:29.719000Z",
      "total": 1,
      "id": "6040a65d104f110001a85060"
    },
    {
      "created_on": "2021-03-04T08:50:49.367000Z",
      "cancelled_records": [],
      "failed_records": [],
      "succeed": 0,
      "cancelled": 0,
      "file_path": "https://hdn-1.addsale.com/x0/company/1/self/documents/inventory-import/free/original/W9lxe19Uu-REicn1sDv-V8ZrKdnLt-product_inventory.csv",
      "total": 1,
      "created_by": {
        "username": "silverbolt",
        "user_id": "-1"
      },
      "is_active": true,
      "modified_by": {
        "username": "silverbolt",
        "user_id": "-1"
      },
      "company_id": 1,
      "failed": 0,
      "modified_on": "2021-03-04T08:50:49.367000Z",
      "stage": "terminated",
      "id": "60409f699b21e30001c1e6b5"
    },
    {
      "total": 1,
      "succeed": 1,
      "created_on": "2021-02-10T10:57:57.236000Z",
      "failed": 0,
      "modified_by": {
        "user_id": "0",
        "username": "Silverbolt"
      },
      "created_by": {
        "username": "917972410891_48194",
        "user_id": "5646",
        "full_name": "Sourabh Nilakhe"
      },
      "is_active": true,
      "cancelled_records": [],
      "failed_records": [],
      "company_id": 1,
      "file_path": "https://hdn-1.addsale.com/x0/company/1/self/documents/inventory-import/free/original/REicn1sDv-V8ZrKdnLt-product_inventory.csv",
      "modified_on": "2021-02-10T10:57:57.571000Z",
      "stage": "completed",
      "cancelled": 0,
      "id": "6023bc35c85ca1000171e08a"
    },
    {
      "total": 1,
      "succeed": 1,
      "created_on": "2021-02-10T10:57:22.535000Z",
      "failed": 0,
      "modified_by": {
        "user_id": "0",
        "username": "Silverbolt"
      },
      "created_by": {
        "username": "917972410891_48194",
        "user_id": "5646",
        "full_name": "Sourabh Nilakhe"
      },
      "is_active": true,
      "cancelled_records": [],
      "failed_records": [],
      "company_id": 1,
      "file_path": "https://hdn-1.addsale.com/x0/company/1/self/documents/inventory-import/free/original/Oth_LaVyI-V8ZrKdnLt-product_inventory.csv",
      "modified_on": "2021-02-10T10:57:23.311000Z",
      "stage": "completed",
      "cancelled": 0,
      "id": "6023bc12c85ca1000171e089"
    },
    {
      "created_by": {
        "user_id": "16",
        "username": "nikhilmhatre_gofynd_com_97636",
        "full_name": "Nikhil Mhatre"
      },
      "succeed": 1,
      "failed": 0,
      "file_path": "https://hdn-1.addsale.com/x0/company/1/self/documents/inventory-import/free/original/V8ZrKdnLt-product_inventory.csv",
      "company_id": 1,
      "created_on": "2021-01-13T13:58:06.155000Z",
      "stage": "completed",
      "modified_by": {
        "username": "Silverbolt",
        "user_id": "0"
      },
      "is_active": true,
      "total": 1,
      "failed_records": [],
      "modified_on": "2021-01-13T13:58:06.369000Z",
      "cancelled_records": [],
      "cancelled": 0,
      "id": "5ffefc6ee2db8f000183fab8"
    },
    {
      "succeed": 0,
      "is_active": true,
      "cancelled": 0,
      "failed_records": [
        {
          "identifiers": "1.91887E+11",
          "message": "Invalid identifier: 1.91887E+11. Product not found."
        }
      ],
      "total": 1,
      "stage": "failed",
      "modified_by": {
        "username": "Silverbolt",
        "user_id": "0"
      },
      "file_path": "https://hdn-1.addsale.com/x0/company/1/self/documents/inventory-import/free/original/t3T6X2Riy-product_inventory.csv",
      "cancelled_records": [],
      "created_by": {
        "username": "nikhilmhatre_gofynd_com_97636",
        "user_id": "16",
        "full_name": "Nikhil Mhatre"
      },
      "created_on": "2021-01-13T13:57:38.598000Z",
      "company_id": 1,
      "failed": 1,
      "modified_on": "2021-01-13T13:57:38.832000Z",
      "id": "5ffefc5252f31100012ea981"
    },
    {
      "total": 1,
      "company_id": 1,
      "created_by": {
        "user_id": "16",
        "username": "nikhilmhatre_gofynd_com_97636",
        "full_name": "Nikhil Mhatre"
      },
      "failed": 1,
      "modified_on": "2021-01-13T13:57:13.847000Z",
      "succeed": 0,
      "stage": "failed",
      "cancelled_records": [],
      "failed_records": [
        {
          "identifiers": "1.91887E+11",
          "message": "Invalid identifier: 1.91887E+11. Product not found."
        }
      ],
      "file_path": "https://hdn-1.addsale.com/x0/company/1/self/documents/inventory-import/free/original/NSTuhgsgq-product_inventory.csv",
      "is_active": true,
      "created_on": "2021-01-13T13:57:13.639000Z",
      "cancelled": 0,
      "modified_by": {
        "username": "Silverbolt",
        "user_id": "0"
      },
      "id": "5ffefc39a0d1e20001ae118c"
    },
    {
      "succeed": 1,
      "failed": 0,
      "failed_records": [],
      "cancelled": 0,
      "file_path": "https://hdn-1.addsale.com/x0/company/1/self/documents/inventory-import/free/original/cwQV-Z6gT-product_inventory.xlsx",
      "created_on": "2021-01-12T06:37:06.167000Z",
      "is_active": true,
      "cancelled_records": [],
      "created_by": {
        "user_id": "16",
        "username": "nikhilmhatre_gofynd_com_97636",
        "full_name": "Nikhil Mhatre"
      },
      "company_id": 1,
      "stage": "completed",
      "modified_by": {
        "username": "Silverbolt",
        "user_id": "0"
      },
      "modified_on": "2021-01-12T06:37:06.307000Z",
      "total": 1,
      "id": "5ffd4392b4c34d000170697b"
    },
    {
      "succeed": 1,
      "failed": 0,
      "failed_records": [],
      "cancelled": 0,
      "file_path": "https://hdn-1.addsale.com/x0/company/1/self/documents/inventory-import/free/original/gccehef2f-product_inventory.xlsx",
      "created_on": "2021-01-12T06:36:24.292000Z",
      "is_active": true,
      "cancelled_records": [],
      "created_by": {
        "user_id": "16",
        "username": "nikhilmhatre_gofynd_com_97636",
        "full_name": "Nikhil Mhatre"
      },
      "company_id": 1,
      "stage": "completed",
      "modified_by": {
        "username": "Silverbolt",
        "user_id": "0"
      },
      "modified_on": "2021-01-12T06:36:24.535000Z",
      "total": 1,
      "id": "5ffd4368b4c34d0001706960"
    }
  ],
  "page": {
    "type": "number",
    "current": 1,
    "size": 4,
    "item_total": 39,
    "has_previous": false,
    "has_next": true
  }
}
```
</details>









---


#### createBulkInventoryJob
Create a Bulk Inventory upload Job.




```kotlin
client.catalog.createBulkInventoryJob(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Company Id in which Inventory to be uploaded. |  
| body | [BulkJob](#BulkJob) | yes | Request body |


This API helps to create a bulk Inventory upload job.

*Returned Response*




[CommonResponse](#CommonResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### createBulkInventory
Create products in bulk associated with given batch Id.




```kotlin
client.catalog.createBulkInventory(batchId: batchId, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Company Id in which Inventory is to be uploaded. |   
| batchId | String | yes | Batch Id of the bulk create job. |  
| body | [InventoryBulkRequest](#InventoryBulkRequest) | yes | Request body |


This API helps to create products in bulk push to kafka for approval/creation.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### deleteBulkInventoryJob
Delete Bulk Inventory job.




```kotlin
client.catalog.deleteBulkInventoryJob(batchId: batchId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Company Id of the company of which bulk Inventory job is to be deleted. |   
| batchId | String | yes | Batch Id of the bulk delete job. |  



This API allows to delete bulk Inventory job associated with company.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### getInventoryExport
Get Inventory export history.




```kotlin
client.catalog.getInventoryExport().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Company Id in which assets to be uploaded. |  



This API helps to get Inventory export history.

*Returned Response*




[InventoryExportJob](#InventoryExportJob)

Returns a list of inventory export jobs




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


#### createInventoryExportJob
Create a Inventory export Job.




```kotlin
client.catalog.createInventoryExportJob(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | Int | yes | Company Id in which assets to be uploaded. |  
| body | [InventoryExportRequest](#InventoryExportRequest) | yes | Request body |


This API helps to create a Inventory export job.

*Returned Response*




[SuccessResponse](#SuccessResponse)

Returns a success response




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### exportInventoryConfig
Get List of different filters for inventory export




```kotlin
client.catalog.exportInventoryConfig(filterType: filterType).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | Id of the company associated to product that is to be viewed. |   
| filterType | String? | no | filter type from any one of ['brand', 'store', 'type'] |  



This API allows get List of different filters like brand, store, and type for inventory export.

*Returned Response*




[InventoryConfig](#InventoryConfig)

returns filters configuration for inventory export




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
[
  {
    "display": "csv",
    "value": "csv"
  },
  {
    "display": "excel",
    "value": "excel"
  }
]
```
</details>









---


#### getAllHsnCodes
Hsn Code List.




```kotlin
client.catalog.getAllHsnCodes(pageNo: pageNo, pageSize: pageSize, q: q).safeAwait{ response,error->
    
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
| pageNo | Int? | no | page no |   
| pageSize | Int? | no | page size |   
| q | String? | no | search using hsn code. |  



Hsn Code List.

*Returned Response*




[HsnCodesListingResponse](#HsnCodesListingResponse)

List of all HSN Codes. See example below or refer `HsnCodesListingResponseSchema` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "company_id": 1,
      "hs2_code": "xx",
      "hsn_code": "xxxxxxxx",
      "tax1": 0,
      "tax2": 0,
      "threshold1": 999999,
      "threshold2": 0,
      "tax_on_esp": true,
      "tax_on_mrp": false,
      "id": "xxxxxxxxxxxx"
    }
  ],
  "page": {
    "current": 1,
    "size": 2,
    "has_previous": false,
    "has_next": true,
    "item_total": 20
  }
}
```
</details>









---


#### createHsnCode
Create Hsn Code.




```kotlin
client.catalog.createHsnCode(body: body).safeAwait{ response,error->
    
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
| body | [HsnUpsert](#HsnUpsert) | yes | Request body |


Create Hsn Code.

*Returned Response*




[HsnCode](#HsnCode)

See example below for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "data": {
    "company_id": 1,
    "hs2_code": "xx",
    "modified_by": {
      "username": "narutouzumaki",
      "user_id": "0"
    },
    "id": "xxxxxxxxxxxx",
    "tax_on": "esp",
    "slabs": [
      {
        "tax": 0,
        "threshold": 999999
      },
      {
        "tax": 0,
        "threshold": 0
      }
    ],
    "hsn_code": "xxxxxxxx"
  }
}
```
</details>









---


#### getHsnCode
Fetch Hsn Code.




```kotlin
client.catalog.getHsnCode(id: id).safeAwait{ response,error->
    
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
| id | String | yes | Unique id |  



Fetch Hsn Code.

*Returned Response*




[HsnCode](#HsnCode)

See example below details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "data": {
    "company_id": 1,
    "hs2_code": "xx",
    "modified_by": {
      "username": "narutouzumaki",
      "user_id": "0"
    },
    "id": "xxxxxxxxxxxx",
    "tax_on": "esp",
    "slabs": [
      {
        "tax": 0,
        "threshold": 999999
      },
      {
        "tax": 0,
        "threshold": 0
      }
    ],
    "hsn_code": "xxxxxxxx"
  }
}
```
</details>









---


#### updateHsnCode
Update Hsn Code.




```kotlin
client.catalog.updateHsnCode(id: id, body: body).safeAwait{ response,error->
    
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
| id | String | yes | Unique id |  
| body | [HsnUpsert](#HsnUpsert) | yes | Request body |


Update Hsn Code.

*Returned Response*




[HsnCode](#HsnCode)

See example below for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "data": {
    "company_id": 1,
    "hs2_code": "xx",
    "modified_by": {
      "username": "narutouzumaki",
      "user_id": "0"
    },
    "id": "xxxxxxxxxxxx",
    "tax_on": "esp",
    "slabs": [
      {
        "tax": 0,
        "threshold": 999999
      },
      {
        "tax": 0,
        "threshold": 0
      }
    ],
    "hsn_code": "xxxxxxxx"
  }
}
```
</details>









---


#### bulkHsnCode
Bulk Create or Update Hsn Code.




```kotlin
client.catalog.bulkHsnCode(body: body).safeAwait{ response,error->
    
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
| body | [BulkHsnUpsert](#BulkHsnUpsert) | yes | Request body |


Bulk Create or Update Hsn Code.

*Returned Response*




[BulkHsnResponse](#BulkHsnResponse)

See example below for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "success": true
}
```
</details>









---


#### getApplicationBrands
List all the brands




```kotlin
client.application("<APPLICATION_ID>").catalog.getApplicationBrands(department: department, pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| department | String? | no | The name of the department. Use this parameter to filter products by a particular department. See below the list of available departments. You can retrieve available departments from the **v1.0/departments/** API |   
| pageNo | Int? | no | The page number to navigate through the given set of results |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 12. |  



A brand is the name under which a product is being sold. Use this API to list all the brands. You can pass optionally filter the brands by the department. If successful, returns a paginated list of brands specified in `BrandListingResponse`

*Returned Response*




[BrandListingResponse](#BrandListingResponse)

List of Brands. See example below or refer `BrandListingResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "uid": 1,
      "name": "Barry, Jennings and Larson",
      "slug": "Hess-Inc",
      "action": {
        "page": {
          "type": "products",
          "query": {
            "brand": [
              "Hess-Inc"
            ]
          }
        },
        "type": "page"
      },
      "logo": {
        "type": "image",
        "url": "https://hdn-1.fynd.com/media/logo/brand/original/12391_0d956c6c71a4427895c15e44cba82f88.jpg"
      },
      "banners": {
        "portrait": {
          "type": "image",
          "url": "https://hdn-1.fynd.com/media/banner_portrait/brand/original/12537_9cdfc6835e814b0986ee1643d38cf6cd.png"
        }
      },
      "en_name": "Barry, Jennings and Larson"
    }
  ],
  "page": {
    "current": 1,
    "total": 1,
    "has_previous": false,
    "has_next": false,
    "item_total": 1,
    "type": "number"
  }
}
```
</details>









---


#### getDepartments
List all the departments




```kotlin
client.application("<APPLICATION_ID>").catalog.getDepartments().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |  



Departments are a way to categorise similar products. A product can lie in multiple departments. For example, a skirt can below to the 'Women's Fashion' Department while a handbag can lie in 'Women's Accessories' Department. Use this API to list all the departments. If successful, returns the list of departments specified in `DepartmentResponse`

*Returned Response*




[DepartmentResponse](#DepartmentResponse)

List of Departments. See example below or refer `DepartmentResponse` for details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "uid": 1,
      "name": "Zachary Harris",
      "slug": "Zachary-Harris",
      "priority_order": 7,
      "logo": {
        "type": "image",
        "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
      }
    },
    {
      "uid": 2,
      "name": "Aaron Reilly",
      "slug": "Aaron-Reilly",
      "priority_order": 7,
      "logo": {
        "type": "image",
        "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
      }
    },
    {
      "uid": 3,
      "name": "Bobby Sandoval",
      "slug": "Bobby-Sandoval",
      "priority_order": 7,
      "logo": {
        "type": "image",
        "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
      }
    },
    {
      "uid": 4,
      "name": "Seth Hughes",
      "slug": "Seth-Hughes",
      "priority_order": 7,
      "logo": {
        "type": "image",
        "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
      }
    },
    {
      "uid": 5,
      "name": "Michelle Moore",
      "slug": "Michelle-Moore",
      "priority_order": 7,
      "logo": {
        "type": "image",
        "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
      }
    },
    {
      "uid": 6,
      "name": "Annette Baldwin",
      "slug": "Annette-Baldwin",
      "priority_order": 7,
      "logo": {
        "type": "image",
        "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
      }
    },
    {
      "uid": 7,
      "name": "Chris Mata",
      "slug": "Chris-Mata",
      "priority_order": 7,
      "logo": {
        "type": "image",
        "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
      }
    },
    {
      "uid": 8,
      "name": "Nicole Jacobs",
      "slug": "Nicole-Jacobs",
      "priority_order": 7,
      "logo": {
        "type": "image",
        "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
      }
    },
    {
      "uid": 9,
      "name": "Pamela Smith",
      "slug": "Pamela-Smith",
      "priority_order": 7,
      "logo": {
        "type": "image",
        "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
      }
    },
    {
      "uid": 10,
      "name": "Nicole Simon",
      "slug": "Nicole-Simon",
      "priority_order": 7,
      "logo": {
        "type": "image",
        "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
      }
    }
  ]
}
```
</details>









---


#### getCategories
List all the categories




```kotlin
client.application("<APPLICATION_ID>").catalog.getCategories(department: department).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| department | String? | no | The name of the department. Use this parameter to filter products by a particular department. See below the list of available departments. You can retrieve available departments from the **v1.0/departments/** API |  



List all the categories. You can optionally pass filter the brands by the department. If successful, returns a paginated list of brands specified in `CategoryListingResponse`

*Returned Response*




[CategoryListingResponse](#CategoryListingResponse)

List of Categories. See example below or refer `CategoryListingResponse` for details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "departments": [
    {
      "slug": "Cody-Doyle",
      "uid": 1
    }
  ],
  "data": [
    {
      "department": "Cody-Doyle",
      "items": [
        {
          "name": "Janet Parker",
          "image": {
            "aspect_ratio": "13:20",
            "aspect_ratio_f": 0.65,
            "url": "https://d2zv4gzhlr4ud6.cloudfront.net/media/banner_portrait/category/resize-w:130,h:200/12064_e69e1d8b5e934d3488f0dc8663d8a158.jpg"
          },
          "uid": 1,
          "slug": "Janet-Parker",
          "_custom_json": {},
          "action": {
            "type": "category",
            "url": "https://api.addsale.com/platform/content/v1/products/?l1_category=Janet-Parker&department=Jaime-Chambers",
            "query": {
              "l1_category": [
                "Janet-Parker"
              ],
              "department": [
                "Jaime-Chambers"
              ]
            }
          },
          "childs": [
            {
              "name": "Hannah Lawson",
              "image": {
                "aspect_ratio": "13:20",
                "aspect_ratio_f": 0.65,
                "url": "https://d2zv4gzhlr4ud6.cloudfront.net/media/banner_portrait/category/resize-w:130,h:200/12064_e69e1d8b5e934d3488f0dc8663d8a158.jpg"
              },
              "uid": 2,
              "slug": "Hannah-Lawson",
              "_custom_json": {},
              "action": {
                "type": "category",
                "url": "https://api.addsale.com/platform/content/v1/products/?l2_category=Hannah-Lawson&department=Jaime-Chambers",
                "query": {
                  "l2_category": [
                    "Hannah-Lawson"
                  ],
                  "department": [
                    "Jaime-Chambers"
                  ]
                }
              },
              "childs": [
                {
                  "name": "Logan Black",
                  "image": {
                    "aspect_ratio": "13:20",
                    "aspect_ratio_f": 0.65,
                    "url": "https://d2zv4gzhlr4ud6.cloudfront.net/media/banner_portrait/category/resize-w:130,h:200/12064_e69e1d8b5e934d3488f0dc8663d8a158.jpg"
                  },
                  "uid": 3,
                  "slug": "Logan-Black",
                  "_custom_json": {},
                  "action": {
                    "type": "category",
                    "url": "https://api.addsale.com/platform/content/v1/products/?category=Logan-Black&department=Jaime-Chambers",
                    "query": {
                      "category": [
                        "Logan-Black"
                      ],
                      "department": [
                        "Jaime-Chambers"
                      ]
                    }
                  },
                  "childs": []
                }
              ]
            }
          ]
        }
      ]
    }
  ]
}
```
</details>









---


#### getAppicationProducts
List the products




```kotlin
client.application("<APPLICATION_ID>").catalog.getAppicationProducts(q: q, f: f, filters: filters, sortOn: sortOn, pageId: pageId, pageSize: pageSize, pageNo: pageNo, pageType: pageType).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| q | String? | no | The search query. This can be a partial or complete name of a either a product, brand or category |   
| f | String? | no | The search filter parameters. All the parameter filtered from filter parameters will be passed in **f** parameter in this format. **?f=brand:voi-jeans||and:::category:t-shirts||shirts** |   
| filters | Boolean? | no | Pass `filters` parameter to fetch the filter details. This flag is used to fetch all filters |   
| sortOn | String? | no | The order to sort the list of products on. The supported sort parameters are popularity, price, redemption and discount in either ascending or descending order. See the supported values below. |   
| pageId | String? | no | Each response will contain **page_id** param, which should be sent back to make pagination work. |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 12. |   
| pageNo | Int? | no | If page_type is number then pass it to fetch page items. Default is 1. |   
| pageType | String? | no | For pagination type should be cursor or number. Default is cursor. |  



List all the products associated with a brand, collection or category in a requested sort order. The API additionally supports arbitrary search queries that may refer the name of any product, brand, category or collection. If successful, returns a paginated list of products specified in `ApplicationProductListingResponse`

*Returned Response*




[ApplicationProductListingResponse](#ApplicationProductListingResponse)

List of Products. See example below or refer `ApplicationProductListingResponse` for details




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "filters": [
    {
      "key": {
        "display": "Department",
        "name": "department",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Department.svg"
      },
      "values": [
        {
          "display": "Debra Villarreal",
          "count": 15,
          "is_selected": false,
          "value": "Debra-Villarreal",
          "logo": {
            "type": "image",
            "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
          }
        },
        {
          "display": "Tracey Miller",
          "count": 15,
          "is_selected": false,
          "value": "Tracey-Miller",
          "logo": {
            "type": "image",
            "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
          }
        }
      ]
    },
    {
      "key": {
        "display": "Category",
        "name": "category",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Category.svg"
      },
      "values": [
        {
          "display": "Amy Kim DDS",
          "count": 15,
          "is_selected": false,
          "value": "3",
          "logo": "http://cdn4.gofynd.com/media/banner/category/original/12063_a5bb91bd5cb44c3c9db98c2a0e6b3d99.jpg"
        }
      ]
    },
    {
      "key": {
        "display": "Gender",
        "name": "gender",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Gender.svg"
      },
      "values": [
        {
          "display": "Men",
          "count": 15,
          "is_selected": false,
          "value": "men"
        },
        {
          "display": "Women",
          "count": 15,
          "is_selected": false,
          "value": "women"
        }
      ]
    },
    {
      "key": {
        "display": "Size",
        "name": "sizes",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Sizes.svg"
      },
      "values": [
        {
          "display": "13",
          "count": 15,
          "is_selected": false,
          "value": "13"
        }
      ]
    },
    {
      "key": {
        "display": "Brand",
        "name": "brand",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Brand%20ID.svg"
      },
      "values": [
        {
          "display": "Barry, Jennings and Larson",
          "count": 15,
          "is_selected": false,
          "value": "1",
          "logo": "https://hdn-1.fynd.com/media/logo/brand/original/12391_0d956c6c71a4427895c15e44cba82f88.jpg"
        }
      ]
    },
    {
      "key": {
        "display": "Rating",
        "name": "rating",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/Rating.svg"
      },
      "values": [
        {
          "count": 15,
          "display": "2 - 3",
          "value": "[2 TO 3}",
          "is_selected": false
        }
      ]
    },
    {
      "key": {
        "display": "Image",
        "name": "image_nature",
        "kind": "multivalued",
        "logo": "https://hdn-1.fynd.com/global/menu-icons/image%20Nature.svg"
      },
      "values": [
        {
          "display": "GoodQuality",
          "count": 15,
          "is_selected": false,
          "value": "standard"
        }
      ]
    },
    {
      "key": {
        "display": "Monica Hampton",
        "name": "material",
        "kind": "multivalued",
        "logo": ""
      },
      "values": [
        {
          "display": "Neoprene",
          "count": 15,
          "is_selected": false,
          "value": "Neoprene"
        }
      ]
    },
    {
      "key": {
        "display": "John Mendoza",
        "name": "weight",
        "kind": "multivalued",
        "logo": ""
      },
      "values": [
        {
          "display": "100",
          "count": 15,
          "is_selected": false,
          "value": "100"
        }
      ]
    },
    {
      "key": {
        "display": "Kimberly Mcdaniel",
        "name": "gender",
        "kind": "multivalued",
        "logo": ""
      },
      "values": [
        {
          "display": "['Men', 'Women']",
          "count": 15,
          "is_selected": false,
          "value": "['Men', 'Women']"
        }
      ]
    },
    {
      "key": {
        "display": "Kimberly Davidson",
        "name": "color",
        "kind": "multivalued",
        "logo": ""
      },
      "values": [
        {
          "display": "Grey",
          "count": 15,
          "is_selected": false,
          "value": "808080"
        }
      ]
    },
    {
      "key": {
        "display": "Available",
        "name": "is_available",
        "kind": "singlevalued",
        "logo": ""
      },
      "values": [
        {
          "display": "Available",
          "count": 3,
          "is_selected": false,
          "value": true
        }
      ]
    }
  ],
  "items": [
    {
      "type": "product",
      "attributes": {
        "primary_color_hex": "808080",
        "weight": "100",
        "gender": "women",
        "material": "Neoprene",
        "primary_color": "DarkGrey"
      },
      "categories": [
        {
          "id": 3,
          "uid": 3,
          "name": "Amy Kim DDS",
          "logo": {
            "type": "image",
            "url": "https://hdn-1.fynd.com/media/banner_portrait/brand/original/540_ecba3a1af141467da8abc20500f983db.jpg"
          },
          "action": {
            "page": {
              "type": "category",
              "query": {
                "category": [
                  "Amy-Kim-DDS"
                ]
              }
            },
            "type": "page"
          },
          "_custom_json": {}
        }
      ],
      "sellable": true,
      "name": "benchmark collaborative paradigms",
      "slug": "benchmark-collaborative-paradigms",
      "uid": 1,
      "item_type": "set",
      "brand": {
        "type": "brand",
        "name": "Hess Inc",
        "logo": {
          "type": "image",
          "url": "https://hdn-1.fynd.com/media/logo/brand/original/12391_0d956c6c71a4427895c15e44cba82f88.jpg"
        },
        "action": {
          "page": {
            "type": "products",
            "query": {
              "brand": [
                "Hess-Inc"
              ]
            }
          },
          "type": "page"
        },
        "_custom_json": {}
      },
      "action": {
        "page": {
          "type": "product",
          "query": {
            "slug": "benchmark-collaborative-paradigms"
          }
        },
        "type": "page"
      },
      "medias": [
        {
          "type": "image",
          "url": "https://hdn-1.fynd.com/media/fynd_store_items/l2_category/original/2830_c5bb5fc02f414307a828c4c56483c30a.jpg"
        }
      ],
      "discount": "14% OFF",
      "price": {
        "marked": {
          "min": 1399,
          "max": 1499,
          "currency_code": "INR",
          "currency_symbol": "₹"
        },
        "effective": {
          "min": 1199,
          "max": 1399,
          "currency_code": "INR",
          "currency_symbol": "₹"
        }
      },
      "is_tryout": false,
      "promo_meta": {
        "title": "",
        "subtitle": ""
      },
      "item_code": "ITEM_CODE_1",
      "rating": 2.7
    },
    {
      "type": "product",
      "attributes": {
        "primary_color_hex": "808080",
        "weight": "100",
        "gender": "women",
        "material": "Neoprene",
        "primary_color": "DarkGrey"
      },
      "categories": [
        {
          "id": 3,
          "uid": 3,
          "name": "Amy Kim DDS",
          "logo": {
            "type": "image",
            "url": "https://hdn-1.fynd.com/media/banner_portrait/brand/original/540_ecba3a1af141467da8abc20500f983db.jpg"
          },
          "action": {
            "page": {
              "type": "category",
              "query": {
                "category": [
                  "Amy-Kim-DDS"
                ]
              }
            },
            "type": "page"
          },
          "_custom_json": {}
        }
      ],
      "sellable": true,
      "name": "architect granular e-business",
      "slug": "architect-granular-e-business",
      "uid": 10,
      "item_type": "set",
      "brand": {
        "type": "brand",
        "name": "Hess Inc",
        "logo": {
          "type": "image",
          "url": "https://hdn-1.fynd.com/media/logo/brand/original/12391_0d956c6c71a4427895c15e44cba82f88.jpg"
        },
        "action": {
          "page": {
            "type": "products",
            "query": {
              "brand": [
                "Hess-Inc"
              ]
            }
          },
          "type": "page"
        },
        "_custom_json": {}
      },
      "action": {
        "page": {
          "type": "product",
          "query": {
            "slug": "architect-granular-e-business"
          }
        },
        "type": "page"
      },
      "medias": [
        {
          "type": "image",
          "url": "https://hdn-1.fynd.com/media/fynd_store_items/l2_category/original/2830_c5bb5fc02f414307a828c4c56483c30a.jpg"
        }
      ],
      "discount": "14% OFF",
      "price": {
        "marked": {
          "min": 1399,
          "max": 1499,
          "currency_code": "INR",
          "currency_symbol": "₹"
        },
        "effective": {
          "min": 1199,
          "max": 1399,
          "currency_code": "INR",
          "currency_symbol": "₹"
        }
      },
      "is_tryout": false,
      "promo_meta": {
        "title": "",
        "subtitle": ""
      },
      "item_code": "ITEM_CODE_2",
      "rating": 2.7
    },
    {
      "type": "product",
      "attributes": {
        "primary_color_hex": "808080",
        "weight": "100",
        "gender": "women",
        "material": "Neoprene",
        "primary_color": "DarkGrey"
      },
      "categories": [
        {
          "id": 3,
          "uid": 3,
          "name": "Amy Kim DDS",
          "logo": {
            "type": "image",
            "url": "https://hdn-1.fynd.com/media/banner_portrait/brand/original/540_ecba3a1af141467da8abc20500f983db.jpg"
          },
          "action": {
            "page": {
              "type": "category",
              "query": {
                "category": [
                  "Amy-Kim-DDS"
                ]
              }
            },
            "type": "page"
          },
          "_custom_json": {}
        }
      ],
      "sellable": true,
      "name": "facilitate enterprise supply-chains",
      "slug": "facilitate-enterprise-supply-chains",
      "uid": 11,
      "item_type": "set",
      "brand": {
        "type": "brand",
        "name": "Hess Inc",
        "logo": {
          "type": "image",
          "url": "https://hdn-1.fynd.com/media/logo/brand/original/12391_0d956c6c71a4427895c15e44cba82f88.jpg"
        },
        "action": {
          "page": {
            "type": "products",
            "query": {
              "brand": [
                "Hess-Inc"
              ]
            }
          },
          "type": "page"
        },
        "_custom_json": {}
      },
      "action": {
        "page": {
          "type": "product",
          "query": {
            "slug": "facilitate-enterprise-supply-chains"
          }
        },
        "type": "page"
      },
      "medias": [
        {
          "type": "image",
          "url": "https://hdn-1.fynd.com/media/fynd_store_items/l2_category/original/2830_c5bb5fc02f414307a828c4c56483c30a.jpg"
        }
      ],
      "discount": "14% OFF",
      "price": {
        "marked": {
          "min": 1399,
          "max": 1499,
          "currency_code": "INR",
          "currency_symbol": "₹"
        },
        "effective": {
          "min": 1199,
          "max": 1399,
          "currency_code": "INR",
          "currency_symbol": "₹"
        }
      },
      "is_tryout": false,
      "promo_meta": {
        "title": "",
        "subtitle": ""
      },
      "item_code": "ITEM_CODE_3",
      "rating": 2.7
    },
    {
      "type": "product",
      "attributes": {
        "primary_color_hex": "808080",
        "weight": "100",
        "gender": "women",
        "material": "Neoprene",
        "primary_color": "DarkGrey"
      },
      "categories": [
        {
          "id": 3,
          "uid": 3,
          "name": "Amy Kim DDS",
          "logo": {
            "type": "image",
            "url": "https://hdn-1.fynd.com/media/banner_portrait/brand/original/540_ecba3a1af141467da8abc20500f983db.jpg"
          },
          "action": {
            "page": {
              "type": "category",
              "query": {
                "category": [
                  "Amy-Kim-DDS"
                ]
              }
            },
            "type": "page"
          },
          "_custom_json": {}
        }
      ],
      "sellable": true,
      "name": "optimize web-enabled e-tailers",
      "slug": "optimize-web-enabled-e-tailers",
      "uid": 12,
      "item_type": "set",
      "brand": {
        "type": "brand",
        "name": "Hess Inc",
        "logo": {
          "type": "image",
          "url": "https://hdn-1.fynd.com/media/logo/brand/original/12391_0d956c6c71a4427895c15e44cba82f88.jpg"
        },
        "action": {
          "page": {
            "type": "products",
            "query": {
              "brand": [
                "Hess-Inc"
              ]
            }
          },
          "type": "page"
        },
        "_custom_json": {}
      },
      "action": {
        "page": {
          "type": "product",
          "query": {
            "slug": "optimize-web-enabled-e-tailers"
          }
        },
        "type": "page"
      },
      "medias": [
        {
          "type": "image",
          "url": "https://hdn-1.fynd.com/media/fynd_store_items/l2_category/original/2830_c5bb5fc02f414307a828c4c56483c30a.jpg"
        }
      ],
      "discount": "14% OFF",
      "price": {
        "marked": {
          "min": 1399,
          "max": 1499,
          "currency_code": "INR",
          "currency_symbol": "₹"
        },
        "effective": {
          "min": 1199,
          "max": 1399,
          "currency_code": "INR",
          "currency_symbol": "₹"
        }
      },
      "is_tryout": false,
      "promo_meta": {
        "title": "",
        "subtitle": ""
      },
      "item_code": "ITEM_CODE_4",
      "rating": 2.7
    }
  ],
  "sort_on": [
    {
      "display": "Latest Products.",
      "name": "Latest Products.",
      "logo": "https://d2zv4gzhlr4ud6.cloudfront.net/media/pictures/tagged_items/360x0/56_MKT02AI060CORAL/1_1567590349681.jpg",
      "value": "latest",
      "is_selected": true
    }
  ],
  "page": {
    "current": 1,
    "total": 2,
    "has_previous": false,
    "has_next": true,
    "item_total": 15,
    "type": "number"
  }
}
```
</details>









---


#### getProductDetailBySlug
Get a product




```kotlin
client.application("<APPLICATION_ID>").catalog.getProductDetailBySlug(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| slug | String | yes | The unique identifier of a product. i.e; `slug` of a product. You can retrieve these from the APIs that list products like **v1.0/products/** |  



Products are the core resource of an application. Products can be associated by categories, collections, brands and more. This API retrieves the product specified by the given **slug**. If successful, returns a Product resource in the response body specified in `ProductDetail`

*Returned Response*




[ProductDetail](#ProductDetail)

The Product object. See example below or refer `ProductDetail` for details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "type": "product",
  "grouped_attributes": [
    {
      "title": "Alexander Sawyer",
      "details": [
        {
          "key": "Kimberly Davidson",
          "type": "text",
          "value": "DarkGrey"
        },
        {
          "key": "Kimberly Mcdaniel",
          "type": "text",
          "value": "Men,Women"
        },
        {
          "key": "Monica Hampton",
          "type": "text",
          "value": "Neoprene"
        },
        {
          "key": "John Mendoza",
          "type": "text",
          "value": "100 g"
        }
      ]
    }
  ],
  "medias": [
    {
      "type": "image",
      "url": "http://cdn4.gofynd.com/media/pictures/tagged_items/original/1309_LGLAPTOPSLEEVE5/1_1564735832806.jpg"
    }
  ],
  "brand": {
    "name": "Barry, Jennings and Larson",
    "uid": 1,
    "logo": {
      "type": "image",
      "url": "https://hdn-1.fynd.com/media/logo/brand/original/12391_0d956c6c71a4427895c15e44cba82f88.jpg"
    },
    "action": {
      "page": {
        "type": "products",
        "query": {
          "brand": [
            "Hess-Inc"
          ]
        }
      },
      "type": "page"
    },
    "_custom_json": {}
  },
  "uid": 1,
  "slug": "benchmark-collaborative-paradigms",
  "attributes": {
    "color_hex": "808080",
    "weight": 100,
    "product_type": "LaptopBags",
    "gender": [
      "Men",
      "Women"
    ],
    "material": "Neoprene",
    "style_note": "Shape up your overall appeal with this stunning laptop bag. The amazing storage and great design will let you carry your laptop in style!",
    "item_code": "LGLAPTOPSLEEVE5",
    "occasion": "Casual",
    "primary_color": "Grey",
    "primary_material": "Others",
    "variant": "LGLAPTOPSLEEVE5",
    "color": "DarkGrey",
    "product_details": "This is a Unisex Product.",
    "primary_color_hex": "808080",
    "brand": "Barry, Jennings and Larson"
  },
  "name": "benchmark collaborative paradigms",
  "has_variant": true,
  "categories": [
    {
      "id": 3,
      "uid": 3,
      "name": "Amy Kim DDS",
      "logo": {
        "type": "image",
        "url": "https://hdn-1.fynd.com/media/banner_portrait/brand/original/540_ecba3a1af141467da8abc20500f983db.jpg"
      },
      "action": {
        "page": {
          "type": "category",
          "query": {
            "category": [
              "Amy-Kim-DDS"
            ]
          }
        },
        "type": "page"
      },
      "_custom_json": {}
    }
  ],
  "tryouts": [],
  "rating": 2.7,
  "rating_count": 2,
  "image_nature": "standard",
  "tags": [
    "Digital"
  ],
  "teaser_tag": {},
  "no_of_boxes": 1,
  "product_online_date": "2021-02-03T07:22:29Z",
  "custom_order": {},
  "color": "808080",
  "similars": [
    "brand"
  ]
}
```
</details>









---


#### getAppProducts
Get applicationwise products




```kotlin
client.application("<APPLICATION_ID>").catalog.getAppProducts(brandIds: brandIds, categoryIds: categoryIds, departmentIds: departmentIds, pageNo: pageNo, pageSize: pageSize, q: q).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| companyId | String | yes | A `company_id` is a unique identifier for a particular seller account. |   
| applicationId | String | yes | A `application_id` is a unique identifier for a particular sale channel. |   
| brandIds | ArrayList<Int>? | no | Get multiple products filtered by Brand Ids |   
| categoryIds | ArrayList<Int>? | no | Get multiple products filtered by Category Ids |   
| departmentIds | ArrayList<Int>? | no | Get multiple products filtered by Department Ids |   
| pageNo | Int? | no | The page number to navigate through the given set of results |   
| pageSize | Int? | no | Number of items to retrieve in each page. Default is 10. |   
| q | String? | no | Search with Item Code, Name, Slug or Identifier. |  



Products are the core resource of an application. Products can be associated by categories, collections, brands and more. If successful, returns a Product resource in the response body specified in `ApplicationProductListingResponseDatabasePowered`

*Returned Response*




[ProductListingResponse](#ProductListingResponse)

The Product object. See example below or refer `ApplicationProductListingResponseDatabasePowered` for details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "name": "TV Set",
      "description": "Tv",
      "country_of_origin": "India",
      "currency": "INR",
      "short_description": "",
      "is_set": true,
      "item_code": "TVSET111",
      "brand_uid": 1,
      "template_tag": "television",
      "highlights": [
        "42 Inch"
      ],
      "slug": "tv-set",
      "_custom_json": {},
      "l3_mapping": [
        "electronics>qled_television"
      ],
      "image_nature": "standard",
      "departments": [
        1
      ],
      "created_on": 1599024995,
      "created_by": {
        "username": "919049753052_37528",
        "user_id": "5"
      },
      "modified_on": 1627642010,
      "modified_by": {
        "username": "xxxxxxxxxx",
        "user_id": "xxxxxxxxxxx"
      },
      "stage": "verified",
      "uid": 7501547,
      "verified_by": {
        "username": "Silverbolt",
        "user_id": "0"
      },
      "verified_on": 1626965521,
      "all_sizes": [
        {
          "item_code": "TVSET111",
          "brand_uid": 1,
          "seller_identifier": "HGS272727272",
          "identifiers": [
            {
              "gtin_type": "ean",
              "gtin_value": "HGS272727272",
              "primary": true
            }
          ],
          "company_id": 1,
          "size": "XXLX23, MX11, LX67, XLX45 (146 PCS)",
          "marked_price": 35000
        }
      ],
      "category_slug": "qled-television",
      "is_image_less_product": false,
      "media": [
        {
          "url": "https://hdn-1.addsale.com/x0/products/pictures/item/free/135x0/dcizgsG_Y-Tv-Set.png",
          "type": "image"
        }
      ],
      "variants": {},
      "product_publish": {
        "is_set": false,
        "product_online_date": 1627642009
      },
      "is_dependent": false,
      "is_physical": true,
      "item_type": "set",
      "category_uid": 1,
      "custom_order": {
        "manufacturing_time": 2,
        "is_custom_order": true,
        "manufacturing_time_unit": "days"
      },
      "moq": {
        "minimum": 1,
        "is_set": false
      },
      "multi_size": true,
      "no_of_boxes": 1,
      "product_group_tag": [],
      "size_guide": "slim-fit-shirts-for-men",
      "tags": [],
      "teaser_tag": {},
      "synonyms": [],
      "hsn_code": "11111111",
      "return_config": {
        "unit": "days",
        "returnable": false,
        "time": 0
      },
      "all_company_ids": [
        1
      ],
      "all_identifiers": [
        "19WE100"
      ],
      "trader": {
        "address": "sdfdsfsdf",
        "name": "asdasd"
      },
      "trader_type": "Packer",
      "verification_status": "pending",
      "sizes": [
        {
          "size": "FGX33, GHX33 (66 PCS)",
          "store_count": 1
        },
        {
          "size": "XSE WE23X100 (100 PCS)",
          "store_count": 2
        },
        {
          "size": "XSEX100 (100 PCS)",
          "store_count": 3
        },
        {
          "size": "XXLX23, MX11, LX67, XLX45 (146 PCS)",
          "store_count": 3
        }
      ],
      "id": "5f4f2f6371a5970001f13655",
      "brand": {
        "name": "Apple",
        "logo": {
          "aspect_ratio": "1:1",
          "aspect_ratio_f": 1,
          "url": "https://hdn-1.jiox0.de/jioecomm/seller/pictures/logo/50x0/apple-7f951c/logo_apple.png",
          "secure_url": "https://hdn-1.jiox0.de/jioecomm/seller/pictures/logo/50x0/apple-7f951c/logo_apple.png"
        },
        "uid": 13
      },
      "images": [
        {
          "aspect_ratio": "16:25",
          "aspect_ratio_f": 0.64,
          "url": "https://hdn-1.addsale.com/x0/products/pictures/item/free/135x0/dcizgsG_Y-Tv-Set.png",
          "secure_url": "https://hdn-1.addsale.com/x0/products/pictures/item/free/135x0/dcizgsG_Y-Tv-Set.png"
        }
      ],
      "price": {
        "marked": {
          "min": 35000,
          "max": 35000
        },
        "effective": {
          "min": 25000,
          "max": 25000
        }
      }
    }
  ],
  "page": {
    "type": "number",
    "current": 1,
    "size": 1,
    "item_total": 1,
    "has_previous": false,
    "has_next": false
  }
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




 
 
 #### [DeleteResponse](#DeleteResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [ErrorResponse](#ErrorResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | Int? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | message | String? |  yes  |  |
 | code | String? |  yes  |  |

---


 
 
 #### [GetSearchWordsData](#GetSearchWordsData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | words | ArrayList<String>? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | result | HashMap<String,Any>? |  yes  |  |
 | uid | String? |  yes  |  |
 | appId | String? |  yes  |  |

---


 
 
 #### [GetSearchWordsDetailResponse](#GetSearchWordsDetailResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | [GetSearchWordsData](#GetSearchWordsData)? |  yes  |  |

---


 
 
 #### [SearchKeywordResult](#SearchKeywordResult)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sortOn | String |  no  |  |
 | query | HashMap<String,Any> |  no  |  |

---


 
 
 #### [CreateSearchKeyword](#CreateSearchKeyword)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | words | ArrayList<String>? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | result | [SearchKeywordResult](#SearchKeywordResult) |  no  |  |
 | isActive | Boolean? |  yes  |  |
 | appId | String? |  yes  |  |

---


 
 
 #### [GetSearchWordsResponse](#GetSearchWordsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[GetSearchWordsData](#GetSearchWordsData)>? |  yes  |  |

---


 
 
 #### [GetAutocompleteWordsData](#GetAutocompleteWordsData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | words | ArrayList<String>? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | results | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | uid | String? |  yes  |  |
 | appId | String? |  yes  |  |

---


 
 
 #### [GetAutocompleteWordsResponse](#GetAutocompleteWordsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[GetAutocompleteWordsData](#GetAutocompleteWordsData)>? |  yes  |  |

---


 
 
 #### [AutocompletePageAction](#AutocompletePageAction)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | params | HashMap<String,Any>? |  yes  |  |
 | query | HashMap<String,Any> |  no  |  |
 | url | String? |  yes  |  |
 | type | String |  no  |  |

---


 
 
 #### [AutocompleteAction](#AutocompleteAction)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [AutocompletePageAction](#AutocompletePageAction)? |  yes  |  |
 | type | String? |  yes  |  |

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
 | customJson | HashMap<String,Any>? |  yes  |  |
 | logo | [Media](#Media)? |  yes  |  |

---


 
 
 #### [CreateAutocompleteKeyword](#CreateAutocompleteKeyword)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | words | ArrayList<String>? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | results | ArrayList<[AutocompleteResult](#AutocompleteResult)>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | appId | String? |  yes  |  |

---


 
 
 #### [CreateAutocompleteWordsResponse](#CreateAutocompleteWordsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | words | ArrayList<String>? |  yes  |  |
 | appId | String? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | results | ArrayList<HashMap<String,Any>>? |  yes  |  |

---


 
 
 #### [ProductBundleItem](#ProductBundleItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | allowRemove | Boolean? |  yes  |  |
 | productUid | Int |  no  |  |
 | autoSelect | Boolean? |  yes  |  |
 | autoAddToCart | Boolean? |  yes  |  |
 | maxQuantity | Int |  no  |  |
 | minQuantity | Int |  no  |  |

---


 
 
 #### [GetProductBundleCreateResponse](#GetProductBundleCreateResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pageVisibility | ArrayList<String>? |  yes  |  |
 | name | String |  no  |  |
 | choice | String |  no  |  |
 | createdOn | String? |  yes  |  |
 | id | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | slug | String |  no  |  |
 | logo | String? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | sameStoreAssignment | Boolean? |  yes  |  |
 | products | ArrayList<[ProductBundleItem](#ProductBundleItem)> |  no  |  |
 | isActive | Boolean |  no  |  |
 | companyId | Int? |  yes  |  |

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
 | pageVisibility | ArrayList<String>? |  yes  |  |
 | name | String |  no  |  |
 | choice | String |  no  |  |
 | createdOn | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | slug | String |  no  |  |
 | logo | String? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | sameStoreAssignment | Boolean? |  yes  |  |
 | products | ArrayList<[ProductBundleItem](#ProductBundleItem)> |  no  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [Size](#Size)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | quantity | Int? |  yes  |  |
 | display | String? |  yes  |  |
 | isAvailable | Boolean? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [Price](#Price)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | minMarked | Double? |  yes  |  |
 | maxMarked | Double? |  yes  |  |
 | minEffective | Double? |  yes  |  |
 | currency | String? |  yes  |  |
 | maxEffective | Double? |  yes  |  |

---


 
 
 #### [LimitedProductData](#LimitedProductData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | images | ArrayList<String>? |  yes  |  |
 | quantity | Int? |  yes  |  |
 | sizes | ArrayList<String>? |  yes  |  |
 | countryOfOrigin | String? |  yes  |  |
 | price | HashMap<String,Any>? |  yes  |  |
 | name | String? |  yes  |  |
 | itemCode | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | attributes | HashMap<String,Any>? |  yes  |  |
 | uid | Int? |  yes  |  |
 | identifier | HashMap<String,Any>? |  yes  |  |
 | shortDescription | String? |  yes  |  |

---


 
 
 #### [GetProducts](#GetProducts)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sizes | ArrayList<[Size](#Size)>? |  yes  |  |
 | allowRemove | Boolean? |  yes  |  |
 | price | [Price](#Price)? |  yes  |  |
 | productUid | Int? |  yes  |  |
 | autoAddToCart | Boolean? |  yes  |  |
 | autoSelect | Boolean? |  yes  |  |
 | maxQuantity | Int? |  yes  |  |
 | minQuantity | Int? |  yes  |  |
 | productDetails | [LimitedProductData](#LimitedProductData)? |  yes  |  |

---


 
 
 #### [GetProductBundleResponse](#GetProductBundleResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pageVisibility | ArrayList<String>? |  yes  |  |
 | name | String? |  yes  |  |
 | choice | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | logo | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | products | ArrayList<[GetProducts](#GetProducts)>? |  yes  |  |
 | sameStoreAssignment | Boolean? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | companyId | Int? |  yes  |  |

---


 
 
 #### [ProductBundleUpdateRequest](#ProductBundleUpdateRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pageVisibility | ArrayList<String>? |  yes  |  |
 | name | String |  no  |  |
 | choice | String |  no  |  |
 | modifiedOn | String? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | slug | String |  no  |  |
 | logo | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | sameStoreAssignment | Boolean? |  yes  |  |
 | products | ArrayList<[ProductBundleItem](#ProductBundleItem)> |  no  |  |
 | isActive | Boolean |  no  |  |

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
 | brandId | Int? |  yes  |  |
 | name | String |  no  |  |
 | createdOn | String? |  yes  |  |
 | id | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | description | String? |  yes  |  |
 | tag | String? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | subtitle | String? |  yes  |  |
 | guide | [Guide](#Guide)? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | image | String? |  yes  |  |
 | title | String |  no  |  |
 | companyId | Int? |  yes  |  |

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
 | brandId | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | id | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | tag | String? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | subtitle | String? |  yes  |  |
 | guide | HashMap<String,Any>? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | title | String? |  yes  |  |
 | companyId | Int? |  yes  |  |

---


 
 
 #### [MetaDataListingFilterMetaResponse](#MetaDataListingFilterMetaResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | units | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | display | String? |  yes  |  |
 | key | String? |  yes  |  |
 | filterTypes | ArrayList<String>? |  yes  |  |

---


 
 
 #### [MetaDataListingFilterResponse](#MetaDataListingFilterResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | ArrayList<[MetaDataListingFilterMetaResponse](#MetaDataListingFilterMetaResponse)>? |  yes  |  |

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


 
 
 #### [MetaDataListingResponse](#MetaDataListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | filter | [MetaDataListingFilterResponse](#MetaDataListingFilterResponse) |  no  |  |
 | sort | [MetaDataListingSortResponse](#MetaDataListingSortResponse) |  no  |  |

---


 
 
 #### [GetCatalogConfigurationDetailsProduct](#GetCatalogConfigurationDetailsProduct)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | similar | HashMap<String,Any>? |  yes  |  |
 | detail | HashMap<String,Any>? |  yes  |  |
 | variant | HashMap<String,Any>? |  yes  |  |
 | compare | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [GetCatalogConfigurationMetaData](#GetCatalogConfigurationMetaData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | listing | [MetaDataListingResponse](#MetaDataListingResponse)? |  yes  |  |
 | product | [GetCatalogConfigurationDetailsProduct](#GetCatalogConfigurationDetailsProduct)? |  yes  |  |

---


 
 
 #### [ConfigurationBucketPoints](#ConfigurationBucketPoints)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | start | Double? |  yes  |  |
 | end | Double? |  yes  |  |

---


 
 
 #### [ConfigurationListingFilterValue](#ConfigurationListingFilterValue)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | bucketPoints | ArrayList<[ConfigurationBucketPoints](#ConfigurationBucketPoints)>? |  yes  |  |
 | value | String? |  yes  |  |
 | condition | String? |  yes  |  |
 | map | HashMap<String,Any>? |  yes  |  |
 | sort | String? |  yes  |  |

---


 
 
 #### [ConfigurationListingFilterConfig](#ConfigurationListingFilterConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String |  no  |  |
 | type | String |  no  |  |
 | name | String? |  yes  |  |
 | priority | Int |  no  |  |
 | logo | String? |  yes  |  |
 | valueConfig | [ConfigurationListingFilterValue](#ConfigurationListingFilterValue)? |  yes  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [ConfigurationListingFilter](#ConfigurationListingFilter)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | allowSingle | Boolean |  no  |  |
 | attributeConfig | ArrayList<[ConfigurationListingFilterConfig](#ConfigurationListingFilterConfig)>? |  yes  |  |

---


 
 
 #### [ConfigurationListingSortConfig](#ConfigurationListingSortConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String |  no  |  |
 | name | String? |  yes  |  |
 | priority | Int |  no  |  |
 | logo | String? |  yes  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [ConfigurationListingSort](#ConfigurationListingSort)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | config | ArrayList<[ConfigurationListingSortConfig](#ConfigurationListingSortConfig)>? |  yes  |  |
 | defaultKey | String |  no  |  |

---


 
 
 #### [ConfigurationListing](#ConfigurationListing)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | filter | [ConfigurationListingFilter](#ConfigurationListingFilter) |  no  |  |
 | sort | [ConfigurationListingSort](#ConfigurationListingSort) |  no  |  |

---


 
 
 #### [ProductSize](#ProductSize)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | max | Int |  no  |  |
 | min | Int |  no  |  |

---


 
 
 #### [ConfigurationProductConfig](#ConfigurationProductConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String |  no  |  |
 | size | [ProductSize](#ProductSize)? |  yes  |  |
 | priority | Int |  no  |  |
 | logo | String? |  yes  |  |
 | subtitle | String? |  yes  |  |
 | isActive | Boolean |  no  |  |
 | title | String? |  yes  |  |

---


 
 
 #### [ConfigurationProductSimilar](#ConfigurationProductSimilar)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | config | ArrayList<[ConfigurationProductConfig](#ConfigurationProductConfig)>? |  yes  |  |

---


 
 
 #### [ConfigurationProductVariantConfig](#ConfigurationProductVariantConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String |  no  |  |
 | displayType | String |  no  |  |
 | size | [ProductSize](#ProductSize) |  no  |  |
 | name | String |  no  |  |
 | priority | Int |  no  |  |
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
 | configId | String? |  yes  |  |
 | id | String? |  yes  |  |
 | listing | [ConfigurationListing](#ConfigurationListing)? |  yes  |  |
 | product | [ConfigurationProduct](#ConfigurationProduct)? |  yes  |  |
 | appId | String |  no  |  |
 | configType | String |  no  |  |

---


 
 
 #### [GetAppCatalogConfiguration](#GetAppCatalogConfiguration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isDefault | Boolean? |  yes  |  |
 | data | [AppCatalogConfiguration](#AppCatalogConfiguration)? |  yes  |  |

---


 
 
 #### [AppConfiguration](#AppConfiguration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | configId | String? |  yes  |  |
 | listing | [ConfigurationListing](#ConfigurationListing)? |  yes  |  |
 | product | [ConfigurationProduct](#ConfigurationProduct)? |  yes  |  |
 | appId | String |  no  |  |
 | configType | String |  no  |  |

---


 
 
 #### [GetCatalogConfigurationDetailsSchemaListing](#GetCatalogConfigurationDetailsSchemaListing)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | filter | HashMap<String,Any>? |  yes  |  |
 | sort | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [EntityConfiguration](#EntityConfiguration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | configId | String? |  yes  |  |
 | id | String? |  yes  |  |
 | listing | [GetCatalogConfigurationDetailsSchemaListing](#GetCatalogConfigurationDetailsSchemaListing)? |  yes  |  |
 | product | [GetCatalogConfigurationDetailsProduct](#GetCatalogConfigurationDetailsProduct)? |  yes  |  |
 | appId | String |  no  |  |
 | configType | String |  no  |  |

---


 
 
 #### [GetAppCatalogEntityConfiguration](#GetAppCatalogEntityConfiguration)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isDefault | Boolean? |  yes  |  |
 | data | [EntityConfiguration](#EntityConfiguration)? |  yes  |  |

---


 
 
 #### [ProductSortOn](#ProductSortOn)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isSelected | Boolean? |  yes  |  |
 | value | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [ProductFiltersValue](#ProductFiltersValue)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | count | Int? |  yes  |  |
 | selectedMin | Int? |  yes  |  |
 | displayFormat | String? |  yes  |  |
 | value | String |  no  |  |
 | queryFormat | String? |  yes  |  |
 | max | Int? |  yes  |  |
 | display | String |  no  |  |
 | min | Int? |  yes  |  |
 | currencySymbol | String? |  yes  |  |
 | selectedMax | Int? |  yes  |  |
 | currencyCode | String? |  yes  |  |
 | isSelected | Boolean |  no  |  |

---


 
 
 #### [ProductFiltersKey](#ProductFiltersKey)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | kind | String? |  yes  |  |
 | display | String |  no  |  |
 | name | String |  no  |  |
 | logo | String? |  yes  |  |

---


 
 
 #### [ProductFilters](#ProductFilters)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | values | ArrayList<[ProductFiltersValue](#ProductFiltersValue)> |  no  |  |
 | key | [ProductFiltersKey](#ProductFiltersKey) |  no  |  |

---


 
 
 #### [GetCollectionQueryOptionResponse](#GetCollectionQueryOptionResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sortOn | ArrayList<[ProductSortOn](#ProductSortOn)>? |  yes  |  |
 | filters | ArrayList<[ProductFilters](#ProductFilters)>? |  yes  |  |

---


 
 
 #### [CollectionListingFilterType](#CollectionListingFilterType)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | isSelected | Boolean? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [CollectionListingFilterTag](#CollectionListingFilterTag)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | isSelected | Boolean? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [CollectionListingFilter](#CollectionListingFilter)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | ArrayList<[CollectionListingFilterType](#CollectionListingFilterType)>? |  yes  |  |
 | tags | ArrayList<[CollectionListingFilterTag](#CollectionListingFilterTag)>? |  yes  |  |

---


 
 
 #### [Media1](#Media1)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | meta | HashMap<String,Any>? |  yes  |  |
 | url | String |  no  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [BannerImage](#BannerImage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | aspectRatio | String? |  yes  |  |
 | url | String? |  yes  |  |

---


 
 
 #### [ImageUrls](#ImageUrls)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | landscape | [BannerImage](#BannerImage)? |  yes  |  |
 | portrait | [BannerImage](#BannerImage)? |  yes  |  |

---


 
 
 #### [ProductListingActionPage](#ProductListingActionPage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | query | HashMap<String,Any>? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [ProductListingAction](#ProductListingAction)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [ProductListingActionPage](#ProductListingActionPage)? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [GetCollectionDetailNest](#GetCollectionDetailNest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | uid | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | allowSort | Boolean? |  yes  |  |
 | tag | ArrayList<String>? |  yes  |  |
 | logo | [Media1](#Media1)? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |
 | cron | HashMap<String,Any>? |  yes  |  |
 | schedule | HashMap<String,Any>? |  yes  |  |
 | type | String? |  yes  |  |
 | name | String? |  yes  |  |
 | visibleFacetsKeys | ArrayList<String>? |  yes  |  |
 | badge | HashMap<String,Any>? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | allowFacets | Boolean? |  yes  |  |
 | appId | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [GetCollectionListingResponse](#GetCollectionListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | filters | [CollectionListingFilter](#CollectionListingFilter)? |  yes  |  |
 | items | ArrayList<[GetCollectionDetailNest](#GetCollectionDetailNest)>? |  yes  |  |

---


 
 
 #### [UserInfo](#UserInfo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | String? |  yes  |  |
 | userId | String? |  yes  |  |
 | email | String? |  yes  |  |
 | username | String? |  yes  |  |

---


 
 
 #### [CollectionImage](#CollectionImage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | aspectRatio | String |  no  |  |
 | url | String |  no  |  |

---


 
 
 #### [SeoDetail](#SeoDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | title | String? |  yes  |  |

---


 
 
 #### [CollectionBanner](#CollectionBanner)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | landscape | [CollectionImage](#CollectionImage) |  no  |  |
 | portrait | [CollectionImage](#CollectionImage) |  no  |  |

---


 
 
 #### [Schedule](#Schedule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | start | String? |  yes  |  |
 | cron | String? |  yes  |  |
 | duration | Int? |  yes  |  |
 | end | String? |  yes  |  |

---


 
 
 #### [CollectionBadge](#CollectionBadge)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | color | String? |  yes  |  |
 | text | String? |  yes  |  |

---


 
 
 #### [CreateCollection](#CreateCollection)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | slug | String |  no  |  |
 | description | String? |  yes  |  |
 | createdBy | [UserInfo](#UserInfo)? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | modifiedBy | [UserInfo](#UserInfo)? |  yes  |  |
 | allowSort | Boolean? |  yes  |  |
 | logo | [CollectionImage](#CollectionImage) |  no  |  |
 | seo | [SeoDetail](#SeoDetail)? |  yes  |  |
 | banners | [CollectionBanner](#CollectionBanner) |  no  |  |
 | query | HashMap<String,Any>? |  yes  |  |
 | schedule | [Schedule](#Schedule)? |  yes  |  |
 | type | String |  no  |  |
 | name | String |  no  |  |
 | localeLanguage | HashMap<String,Any>? |  yes  |  |
 | sortOn | String? |  yes  |  |
 | visibleFacetsKeys | ArrayList<String>? |  yes  |  |
 | badge | [CollectionBadge](#CollectionBadge)? |  yes  |  |
 | allowFacets | Boolean? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | appId | String |  no  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [CollectionCreateResponse](#CollectionCreateResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cron | HashMap<String,Any>? |  yes  |  |
 | schedule | HashMap<String,Any>? |  yes  |  |
 | type | String? |  yes  |  |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | tag | ArrayList<String>? |  yes  |  |
 | logo | [BannerImage](#BannerImage)? |  yes  |  |
 | visibleFacetsKeys | ArrayList<String>? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | badge | HashMap<String,Any>? |  yes  |  |
 | allowFacets | Boolean? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |
 | appId | String? |  yes  |  |
 | allowSort | Boolean? |  yes  |  |

---


 
 
 #### [CollectionDetailResponse](#CollectionDetailResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cron | HashMap<String,Any>? |  yes  |  |
 | schedule | HashMap<String,Any>? |  yes  |  |
 | type | String? |  yes  |  |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | tag | ArrayList<String>? |  yes  |  |
 | logo | [Media1](#Media1)? |  yes  |  |
 | visibleFacetsKeys | ArrayList<String>? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | badge | HashMap<String,Any>? |  yes  |  |
 | allowFacets | Boolean? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |
 | appId | String? |  yes  |  |
 | allowSort | Boolean? |  yes  |  |

---


 
 
 #### [UpdateCollection](#UpdateCollection)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | slug | String? |  yes  |  |
 | description | String? |  yes  |  |
 | published | Boolean? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | modifiedBy | [UserInfo](#UserInfo)? |  yes  |  |
 | allowSort | Boolean? |  yes  |  |
 | logo | [CollectionImage](#CollectionImage)? |  yes  |  |
 | seo | [SeoDetail](#SeoDetail)? |  yes  |  |
 | banners | [CollectionBanner](#CollectionBanner)? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |
 | schedule | [Schedule](#Schedule)? |  yes  |  |
 | name | String? |  yes  |  |
 | localeLanguage | HashMap<String,Any>? |  yes  |  |
 | sortOn | String? |  yes  |  |
 | badge | [CollectionBadge](#CollectionBadge)? |  yes  |  |
 | visibleFacetsKeys | ArrayList<String>? |  yes  |  |
 | allowFacets | Boolean? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

---


 
 
 #### [ProductBrand](#ProductBrand)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | name | String? |  yes  |  |
 | logo | [Media1](#Media1)? |  yes  |  |

---


 
 
 #### [ProductDetailAttribute](#ProductDetailAttribute)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | String? |  yes  |  |
 | type | String? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [ProductDetailGroupedAttribute](#ProductDetailGroupedAttribute)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | details | ArrayList<[ProductDetailAttribute](#ProductDetailAttribute)>? |  yes  |  |

---


 
 
 #### [Price1](#Price1)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | max | Double? |  yes  |  |
 | currencySymbol | String? |  yes  |  |
 | min | Double? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [ProductListingPrice](#ProductListingPrice)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | marked | [Price1](#Price1)? |  yes  |  |
 | effective | [Price1](#Price1)? |  yes  |  |

---


 
 
 #### [ProductListingDetail](#ProductListingDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brand | [ProductBrand](#ProductBrand)? |  yes  |  |
 | groupedAttributes | ArrayList<[ProductDetailGroupedAttribute](#ProductDetailGroupedAttribute)>? |  yes  |  |
 | highlights | ArrayList<String>? |  yes  |  |
 | itemCode | String? |  yes  |  |
 | slug | String |  no  |  |
 | description | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | sellable | Boolean? |  yes  |  |
 | discount | String? |  yes  |  |
 | imageNature | String? |  yes  |  |
 | similars | ArrayList<String>? |  yes  |  |
 | color | String? |  yes  |  |
 | tryouts | ArrayList<String>? |  yes  |  |
 | type | String? |  yes  |  |
 | name | String? |  yes  |  |
 | shortDescription | String? |  yes  |  |
 | productOnlineDate | String? |  yes  |  |
 | promoMeta | HashMap<String,Any>? |  yes  |  |
 | itemType | String? |  yes  |  |
 | price | [ProductListingPrice](#ProductListingPrice)? |  yes  |  |
 | teaserTag | HashMap<String,Any>? |  yes  |  |
 | attributes | HashMap<String,Any>? |  yes  |  |
 | medias | ArrayList<[Media1](#Media1)>? |  yes  |  |
 | hasVariant | Boolean? |  yes  |  |
 | ratingCount | Int? |  yes  |  |
 | rating | Double? |  yes  |  |

---


 
 
 #### [GetCollectionItemsResponse](#GetCollectionItemsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sortOn | ArrayList<[ProductSortOn](#ProductSortOn)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |
 | filters | ArrayList<[ProductFilters](#ProductFilters)>? |  yes  |  |
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


 
 
 #### [CatalogInsightItem](#CatalogInsightItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sellableCount | Int? |  yes  |  |
 | count | Int? |  yes  |  |
 | outOfStockCount | Int? |  yes  |  |

---


 
 
 #### [CatalogInsightBrand](#CatalogInsightBrand)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | articleFreshness | Int? |  yes  |  |
 | availableSizes | Int? |  yes  |  |
 | availableArticles | Int? |  yes  |  |
 | totalSizes | Int? |  yes  |  |
 | totalArticles | Int? |  yes  |  |

---


 
 
 #### [CatalogInsightResponse](#CatalogInsightResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | item | [CatalogInsightItem](#CatalogInsightItem)? |  yes  |  |
 | brandDistribution | [CatalogInsightBrand](#CatalogInsightBrand)? |  yes  |  |

---


 
 
 #### [CrossSellingData](#CrossSellingData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | articles | Int? |  yes  |  |
 | products | Int? |  yes  |  |

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
 | storeIds | ArrayList<Int>? |  yes  |  |
 | optLevel | String |  no  |  |
 | enabled | Boolean? |  yes  |  |
 | brandIds | ArrayList<Int>? |  yes  |  |

---


 
 
 #### [CompanyOptIn](#CompanyOptIn)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brandIds | ArrayList<Int> |  no  |  |
 | createdOn | Int |  no  |  |
 | storeIds | ArrayList<Int> |  no  |  |
 | modifiedOn | Int |  no  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | optLevel | String |  no  |  |
 | platform | String |  no  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | enabled | Boolean |  no  |  |
 | companyId | Int |  no  |  |

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
 | uid | Int? |  yes  |  |
 | businessType | String? |  yes  |  |
 | companyType | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [CompanyBrandDetail](#CompanyBrandDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | totalArticle | Int? |  yes  |  |
 | brandId | Int? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | brandName | String? |  yes  |  |

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
 | store | Int? |  yes  |  |
 | company | String? |  yes  |  |
 | brand | Int? |  yes  |  |

---


 
 
 #### [StoreDetail](#StoreDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | documents | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | storeType | String? |  yes  |  |
 | timing | HashMap<String,Any>? |  yes  |  |
 | uid | Int? |  yes  |  |
 | storeCode | String? |  yes  |  |
 | additionalContacts | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | displayName | String? |  yes  |  |
 | companyId | Int? |  yes  |  |

---


 
 
 #### [OptinStoreDetails](#OptinStoreDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[StoreDetail](#StoreDetail)>? |  yes  |  |

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


 
 
 #### [AttributeMasterFilter](#AttributeMasterFilter)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | dependsOn | ArrayList<String>? |  yes  |  |
 | priority | Int? |  yes  |  |
 | indexing | Boolean |  no  |  |

---


 
 
 #### [AttributeSchemaRange](#AttributeSchemaRange)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | max | Int? |  yes  |  |
 | min | Int? |  yes  |  |

---


 
 
 #### [AttributeMaster](#AttributeMaster)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | format | String? |  yes  |  |
 | type | String |  no  |  |
 | range | [AttributeSchemaRange](#AttributeSchemaRange)? |  yes  |  |
 | mandatory | Boolean? |  yes  |  |
 | allowedValues | ArrayList<String>? |  yes  |  |
 | multi | Boolean? |  yes  |  |

---


 
 
 #### [AttributeMasterDetails](#AttributeMasterDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | displayType | String |  no  |  |

---


 
 
 #### [GenderDetail](#GenderDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | isNested | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | id | String? |  yes  |  |
 | description | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | logo | String? |  yes  |  |
 | meta | [AttributeMasterMeta](#AttributeMasterMeta)? |  yes  |  |
 | filters | [AttributeMasterFilter](#AttributeMasterFilter)? |  yes  |  |
 | schema | [AttributeMaster](#AttributeMaster)? |  yes  |  |
 | enabledForEndConsumer | Boolean? |  yes  |  |
 | departments | ArrayList<String>? |  yes  |  |
 | details | [AttributeMasterDetails](#AttributeMasterDetails)? |  yes  |  |

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
 | message | String? |  yes  |  |
 | code | String? |  yes  |  |
 | errors | HashMap<String,Any>? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | status | Int? |  yes  |  |

---


 
 
 #### [UserSerializer](#UserSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | contact | String? |  yes  |  |
 | userId | String? |  yes  |  |
 | username | String? |  yes  |  |

---


 
 
 #### [GetDepartment](#GetDepartment)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | itemType | String? |  yes  |  |
 | name | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | pageNo | Int? |  yes  |  |
 | slug | String? |  yes  |  |
 | modifiedBy | [UserSerializer](#UserSerializer)? |  yes  |  |
 | logo | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | priorityOrder | Int? |  yes  |  |
 | createdBy | [UserSerializer](#UserSerializer)? |  yes  |  |
 | pageSize | Int? |  yes  |  |
 | synonyms | ArrayList<String>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | search | String? |  yes  |  |

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
 | message | String? |  yes  |  |
 | code | String? |  yes  |  |
 | errors | HashMap<String,Any>? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | status | Int? |  yes  |  |

---


 
 
 #### [ProductTemplate](#ProductTemplate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | slug | String |  no  |  |
 | description | String? |  yes  |  |
 | tag | String? |  yes  |  |
 | attributes | ArrayList<String>? |  yes  |  |
 | logo | String? |  yes  |  |
 | isPhysical | Boolean |  no  |  |
 | isArchived | Boolean? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | categories | ArrayList<String>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | departments | ArrayList<String>? |  yes  |  |

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
 | sizes | HashMap<String,Any>? |  yes  |  |
 | highlights | HashMap<String,Any>? |  yes  |  |
 | itemCode | HashMap<String,Any>? |  yes  |  |
 | brandUid | HashMap<String,Any>? |  yes  |  |
 | slug | HashMap<String,Any>? |  yes  |  |
 | description | HashMap<String,Any>? |  yes  |  |
 | hsnCode | HashMap<String,Any>? |  yes  |  |
 | trader | HashMap<String,Any>? |  yes  |  |
 | sizeGuide | HashMap<String,Any>? |  yes  |  |
 | productGroupTag | HashMap<String,Any>? |  yes  |  |
 | returnConfig | HashMap<String,Any>? |  yes  |  |
 | isDependent | HashMap<String,Any>? |  yes  |  |
 | customOrder | HashMap<String,Any>? |  yes  |  |
 | countryOfOrigin | HashMap<String,Any>? |  yes  |  |
 | name | HashMap<String,Any>? |  yes  |  |
 | multiSize | HashMap<String,Any>? |  yes  |  |
 | variants | HashMap<String,Any>? |  yes  |  |
 | tags | HashMap<String,Any>? |  yes  |  |
 | shortDescription | HashMap<String,Any>? |  yes  |  |
 | moq | HashMap<String,Any>? |  yes  |  |
 | itemType | HashMap<String,Any>? |  yes  |  |
 | command | HashMap<String,Any>? |  yes  |  |
 | media | HashMap<String,Any>? |  yes  |  |
 | traderType | HashMap<String,Any>? |  yes  |  |
 | teaserTag | HashMap<String,Any>? |  yes  |  |
 | categorySlug | HashMap<String,Any>? |  yes  |  |
 | noOfBoxes | HashMap<String,Any>? |  yes  |  |
 | currency | HashMap<String,Any>? |  yes  |  |
 | productPublish | HashMap<String,Any>? |  yes  |  |
 | isActive | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [GlobalValidation](#GlobalValidation)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | required | ArrayList<String>? |  yes  |  |
 | definitions | HashMap<String,Any>? |  yes  |  |
 | description | String? |  yes  |  |
 | properties | [Properties](#Properties)? |  yes  |  |
 | title | String? |  yes  |  |

---


 
 
 #### [TemplateValidationData](#TemplateValidationData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | globalValidation | [GlobalValidation](#GlobalValidation)? |  yes  |  |
 | templateValidation | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [TemplateDetails](#TemplateDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | id | String? |  yes  |  |
 | slug | String |  no  |  |
 | description | String? |  yes  |  |
 | tag | String? |  yes  |  |
 | attributes | ArrayList<String>? |  yes  |  |
 | logo | String? |  yes  |  |
 | isPhysical | Boolean |  no  |  |
 | isArchived | Boolean? |  yes  |  |
 | categories | ArrayList<String>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | departments | ArrayList<String>? |  yes  |  |

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
 | message | String? |  yes  |  |
 | data | HashMap<String,Any>? |  yes  |  |

---


 
 
 #### [HSNData](#HSNData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | countryOfOrigin | ArrayList<String>? |  yes  |  |
 | hsnCode | ArrayList<String>? |  yes  |  |

---


 
 
 #### [HSNCodesResponse](#HSNCodesResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |
 | data | [HSNData](#HSNData)? |  yes  |  |

---


 
 
 #### [VerifiedBy](#VerifiedBy)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | userId | String? |  yes  |  |
 | username | String? |  yes  |  |

---


 
 
 #### [ProductDownloadItemsData](#ProductDownloadItemsData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | templates | ArrayList<String>? |  yes  |  |
 | brand | ArrayList<String>? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [ProductDownloadsItems](#ProductDownloadsItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | url | String? |  yes  |  |
 | sellerId | Double? |  yes  |  |
 | triggerOn | String? |  yes  |  |
 | id | String? |  yes  |  |
 | createdBy | [VerifiedBy](#VerifiedBy)? |  yes  |  |
 | completedOn | String? |  yes  |  |
 | templateTags | HashMap<String,Any>? |  yes  |  |
 | data | [ProductDownloadItemsData](#ProductDownloadItemsData)? |  yes  |  |
 | taskId | String? |  yes  |  |
 | status | String? |  yes  |  |

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
 | multivalue | Boolean? |  yes  |  |
 | data | ArrayList<HashMap<String,Any>>? |  yes  |  |

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
 | landscape | String |  no  |  |
 | portrait | String |  no  |  |
 | logo | String |  no  |  |

---


 
 
 #### [Hierarchy](#Hierarchy)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | department | Int |  no  |  |
 | l1 | Int |  no  |  |
 | l2 | Int |  no  |  |

---


 
 
 #### [Category](#Category)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | marketplaces | [CategoryMapping](#CategoryMapping)? |  yes  |  |
 | media | [Media2](#Media2)? |  yes  |  |
 | name | String |  no  |  |
 | createdOn | String? |  yes  |  |
 | id | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | slug | String? |  yes  |  |
 | synonyms | ArrayList<String>? |  yes  |  |
 | uid | Int? |  yes  |  |
 | priority | Int? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | level | Int |  no  |  |
 | hierarchy | ArrayList<[Hierarchy](#Hierarchy)>? |  yes  |  |
 | tryouts | ArrayList<String>? |  yes  |  |
 | isActive | Boolean |  no  |  |
 | departments | ArrayList<Int> |  no  |  |

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
 | media | [Media2](#Media2)? |  yes  |  |
 | name | String |  no  |  |
 | slug | String? |  yes  |  |
 | synonyms | ArrayList<String>? |  yes  |  |
 | priority | Int? |  yes  |  |
 | level | Int |  no  |  |
 | hierarchy | ArrayList<[Hierarchy](#Hierarchy)>? |  yes  |  |
 | tryouts | ArrayList<String>? |  yes  |  |
 | isActive | Boolean |  no  |  |
 | departments | ArrayList<Int> |  no  |  |

---


 
 
 #### [CategoryCreateResponse](#CategoryCreateResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [SingleCategoryResponse](#SingleCategoryResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [Category](#Category)? |  yes  |  |

---


 
 
 #### [CategoryUpdateResponse](#CategoryUpdateResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [Logo](#Logo)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | aspectRatioF | Int? |  yes  |  |
 | aspectRatio | String? |  yes  |  |
 | url | String? |  yes  |  |
 | secureUrl | String? |  yes  |  |

---


 
 
 #### [Brand](#Brand)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | logo | [Logo](#Logo)? |  yes  |  |

---


 
 
 #### [Image](#Image)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | aspectRatioF | Double? |  yes  |  |
 | aspectRatio | String? |  yes  |  |
 | url | String? |  yes  |  |
 | secureUrl | String? |  yes  |  |

---


 
 
 #### [ProductPublished](#ProductPublished)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | productOnlineDate | Int? |  yes  |  |
 | isSet | Boolean? |  yes  |  |

---


 
 
 #### [Product](#Product)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sizes | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | brand | [Brand](#Brand)? |  yes  |  |
 | highlights | ArrayList<String>? |  yes  |  |
 | itemCode | String? |  yes  |  |
 | brandUid | Int? |  yes  |  |
 | description | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | hsnCode | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | categoryUid | Int? |  yes  |  |
 | isPhysical | Boolean? |  yes  |  |
 | sizeGuide | String? |  yes  |  |
 | departments | ArrayList<Int>? |  yes  |  |
 | imageNature | String? |  yes  |  |
 | color | String? |  yes  |  |
 | isDependent | Boolean? |  yes  |  |
 | customOrder | HashMap<String,Any>? |  yes  |  |
 | countryOfOrigin | String? |  yes  |  |
 | images | ArrayList<[Image](#Image)>? |  yes  |  |
 | name | String? |  yes  |  |
 | multiSize | Boolean? |  yes  |  |
 | templateTag | String? |  yes  |  |
 | variants | HashMap<String,Any>? |  yes  |  |
 | shortDescription | String? |  yes  |  |
 | moq | HashMap<String,Any>? |  yes  |  |
 | isSet | Boolean? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | itemType | String? |  yes  |  |
 | media | ArrayList<[Media1](#Media1)>? |  yes  |  |
 | id | String? |  yes  |  |
 | categorySlug | String? |  yes  |  |
 | primaryColor | String? |  yes  |  |
 | currency | String? |  yes  |  |
 | allSizes | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | productPublish | [ProductPublished](#ProductPublished)? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | l3Mapping | ArrayList<String>? |  yes  |  |

---


 
 
 #### [ProductListingResponse](#ProductListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[Product](#Product)>? |  yes  |  |

---


 
 
 #### [Trader](#Trader)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | address | String |  no  |  |
 | name | String |  no  |  |

---


 
 
 #### [ReturnConfig](#ReturnConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | unit | String? |  yes  |  |
 | returnable | Boolean? |  yes  |  |
 | time | Int? |  yes  |  |

---


 
 
 #### [CustomOrder](#CustomOrder)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | manufacturingTime | Int? |  yes  |  |
 | isCustomOrder | Boolean? |  yes  |  |
 | manufacturingTimeUnit | String? |  yes  |  |

---


 
 
 #### [OrderQuantity](#OrderQuantity)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | minimum | Int? |  yes  |  |
 | isSet | Boolean? |  yes  |  |
 | maximum | Int? |  yes  |  |

---


 
 
 #### [TeaserTag](#TeaserTag)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | url | String? |  yes  |  |
 | tag | String? |  yes  |  |

---


 
 
 #### [ProductPublish](#ProductPublish)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | productOnlineDate | String? |  yes  |  |
 | isSet | Boolean? |  yes  |  |

---


 
 
 #### [ProductCreateUpdate](#ProductCreateUpdate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | highlights | ArrayList<String>? |  yes  |  |
 | itemCode | String |  no  |  |
 | brandUid | Int |  no  |  |
 | slug | String |  no  |  |
 | description | String? |  yes  |  |
 | hsnCode | String |  no  |  |
 | trader | [Trader](#Trader)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | isImageLessProduct | Boolean? |  yes  |  |
 | sizeGuide | String? |  yes  |  |
 | productGroupTag | ArrayList<String>? |  yes  |  |
 | departments | ArrayList<Int> |  no  |  |
 | returnConfig | [ReturnConfig](#ReturnConfig)? |  yes  |  |
 | isDependent | Boolean? |  yes  |  |
 | requester | String? |  yes  |  |
 | changeRequestId | String? |  yes  |  |
 | customOrder | [CustomOrder](#CustomOrder)? |  yes  |  |
 | countryOfOrigin | String |  no  |  |
 | name | String |  no  |  |
 | multiSize | Boolean? |  yes  |  |
 | templateTag | String |  no  |  |
 | variants | HashMap<String,Any>? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | shortDescription | String? |  yes  |  |
 | moq | [OrderQuantity](#OrderQuantity)? |  yes  |  |
 | isSet | Boolean? |  yes  |  |
 | companyId | Int |  no  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | itemType | String |  no  |  |
 | media | ArrayList<[Media1](#Media1)>? |  yes  |  |
 | traderType | String? |  yes  |  |
 | teaserTag | [TeaserTag](#TeaserTag)? |  yes  |  |
 | categorySlug | String |  no  |  |
 | noOfBoxes | Int? |  yes  |  |
 | currency | String |  no  |  |
 | productPublish | [ProductPublish](#ProductPublish)? |  yes  |  |
 | isActive | Boolean? |  yes  |  |

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
 | fullName | String? |  yes  |  |
 | username | String? |  yes  |  |

---


 
 
 #### [ProductBulkRequest](#ProductBulkRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | failed | Int? |  yes  |  |
 | failedRecords | ArrayList<String>? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | cancelledRecords | ArrayList<String>? |  yes  |  |
 | cancelled | Int? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | modifiedBy | [UserDetail](#UserDetail)? |  yes  |  |
 | createdBy | [UserDetail](#UserDetail)? |  yes  |  |
 | stage | String? |  yes  |  |
 | templateTag | String? |  yes  |  |
 | total | Int? |  yes  |  |
 | filePath | String? |  yes  |  |
 | template | [ProductTemplate](#ProductTemplate)? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | succeed | Int? |  yes  |  |
 | companyId | Int? |  yes  |  |

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
 | uid | String? |  yes  |  |
 | userId | String? |  yes  |  |
 | email | String? |  yes  |  |
 | username | String? |  yes  |  |

---


 
 
 #### [BulkJob](#BulkJob)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | failed | Int? |  yes  |  |
 | failedRecords | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | createdOn | String |  no  |  |
 | cancelledRecords | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | cancelled | Int? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | modifiedBy | [UserInfo1](#UserInfo1)? |  yes  |  |
 | createdBy | [UserInfo1](#UserInfo1)? |  yes  |  |
 | stage | String? |  yes  |  |
 | total | Int |  no  |  |
 | templateTag | String? |  yes  |  |
 | trackingUrl | String? |  yes  |  |
 | filePath | String? |  yes  |  |
 | customTemplateTag | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | succeed | Int? |  yes  |  |
 | companyId | Int |  no  |  |

---


 
 
 #### [BulkProductRequest](#BulkProductRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | templateTag | String |  no  |  |
 | batchId | String |  no  |  |
 | data | ArrayList<HashMap<String,Any>> |  no  |  |
 | companyId | Int |  no  |  |

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
 | failed | Int? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | failedRecords | ArrayList<String>? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | cancelledRecords | ArrayList<String>? |  yes  |  |
 | retry | Int? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | cancelled | Int? |  yes  |  |
 | id | String? |  yes  |  |
 | createdBy | [UserCommon](#UserCommon)? |  yes  |  |
 | stage | String? |  yes  |  |
 | total | Int? |  yes  |  |
 | trackingUrl | String? |  yes  |  |
 | filePath | String? |  yes  |  |
 | modifiedBy | [UserCommon](#UserCommon)? |  yes  |  |
 | succeed | Int? |  yes  |  |
 | companyId | Int? |  yes  |  |

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
 | user | HashMap<String,Any> |  no  |  |
 | url | String |  no  |  |
 | companyId | Int? |  yes  |  |

---


 
 
 #### [ProductSizeDeleteDataResponse](#ProductSizeDeleteDataResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | companyId | Int? |  yes  |  |
 | size | String? |  yes  |  |
 | itemId | Int? |  yes  |  |

---


 
 
 #### [ProductSizeDeleteResponse](#ProductSizeDeleteResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |
 | data | [ProductSizeDeleteDataResponse](#ProductSizeDeleteDataResponse)? |  yes  |  |

---


 
 
 #### [InventoryResponse](#InventoryResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | identifiers | HashMap<String,Any>? |  yes  |  |
 | quantity | Int? |  yes  |  |
 | size | String? |  yes  |  |
 | price | Int? |  yes  |  |
 | sellerIdentifier | Int? |  yes  |  |
 | sellableQuantity | Int? |  yes  |  |
 | priceTransfer | Int? |  yes  |  |
 | uid | String? |  yes  |  |
 | currency | String? |  yes  |  |
 | priceEffective | Int? |  yes  |  |
 | inventoryUpdatedOn | String? |  yes  |  |
 | store | HashMap<String,Any>? |  yes  |  |
 | itemId | Int? |  yes  |  |

---


 
 
 #### [GTIN](#GTIN)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | gtinType | String |  no  |  |
 | gtinValue | String |  no  |  |
 | primary | Boolean? |  yes  |  |

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
 | itemDimensionsUnitOfMeasure | String? |  yes  |  |
 | identifiers | ArrayList<[GTIN](#GTIN)> |  no  |  |
 | quantity | Int |  no  |  |
 | size | String |  no  |  |
 | price | Double |  no  |  |
 | itemWidth | Double? |  yes  |  |
 | itemHeight | Double? |  yes  |  |
 | set | [InventorySet](#InventorySet)? |  yes  |  |
 | itemWeight | Double? |  yes  |  |
 | priceTransfer | Double? |  yes  |  |
 | itemLength | Double? |  yes  |  |
 | itemWeightUnitOfMeasure | String? |  yes  |  |
 | storeCode | String |  no  |  |
 | priceEffective | Double |  no  |  |
 | currency | String |  no  |  |
 | isSet | Boolean? |  yes  |  |

---


 
 
 #### [ItemQuery](#ItemQuery)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | itemCode | String? |  yes  |  |
 | brandUid | Int? |  yes  |  |

---


 
 
 #### [InventoryRequest](#InventoryRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sizes | ArrayList<[InvSize](#InvSize)> |  no  |  |
 | item | [ItemQuery](#ItemQuery) |  no  |  |
 | companyId | Int |  no  |  |

---


 
 
 #### [InventoryDeleteData](#InventoryDeleteData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | size | String? |  yes  |  |
 | itemId | Int? |  yes  |  |
 | locationId | Int? |  yes  |  |

---


 
 
 #### [InventoryDelete](#InventoryDelete)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |
 | data | [InventoryDeleteData](#InventoryDeleteData)? |  yes  |  |

---


 
 
 #### [BulkInventoryGetItems](#BulkInventoryGetItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | failed | Int? |  yes  |  |
 | failedRecords | ArrayList<String>? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | cancelledRecords | ArrayList<String>? |  yes  |  |
 | id | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | modifiedBy | HashMap<String,Any>? |  yes  |  |
 | createdBy | HashMap<String,Any>? |  yes  |  |
 | stage | String? |  yes  |  |
 | total | Int? |  yes  |  |
 | succeed | Int? |  yes  |  |
 | filePath | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | cancelled | Int? |  yes  |  |
 | companyId | Int? |  yes  |  |

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
 | itemDimensionsUnitOfMeasure | String? |  yes  |  |
 | identifiers | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | quantity | Int |  no  |  |
 | size | String? |  yes  |  |
 | price | Double |  no  |  |
 | itemWidth | Double? |  yes  |  |
 | itemHeight | Double? |  yes  |  |
 | set | [InventorySet](#InventorySet)? |  yes  |  |
 | itemWeight | Double? |  yes  |  |
 | sellerIdentifier | String |  no  |  |
 | priceTransfer | Double? |  yes  |  |
 | itemLength | Double? |  yes  |  |
 | itemWeightUnitOfMeasure | String? |  yes  |  |
 | storeCode | String |  no  |  |
 | priceEffective | Double |  no  |  |
 | currency | String |  no  |  |
 | isSet | Boolean? |  yes  |  |

---


 
 
 #### [InventoryBulkRequest](#InventoryBulkRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sizes | ArrayList<[Size1](#Size1)> |  no  |  |
 | batchId | String |  no  |  |
 | user | HashMap<String,Any>? |  yes  |  |
 | companyId | Int |  no  |  |

---


 
 
 #### [InventoryExportJob](#InventoryExportJob)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | url | String? |  yes  |  |
 | sellerId | Int |  no  |  |
 | triggerOn | String? |  yes  |  |
 | requestParams | HashMap<String,Any>? |  yes  |  |
 | completedOn | String? |  yes  |  |
 | taskId | String |  no  |  |
 | status | String? |  yes  |  |

---


 
 
 #### [InventoryExportRequest](#InventoryExportRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | store | ArrayList<Int>? |  yes  |  |
 | brand | ArrayList<Int>? |  yes  |  |
 | type | String? |  yes  |  |

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
 | multivalues | Boolean? |  yes  |  |
 | data | ArrayList<[FilerList](#FilerList)>? |  yes  |  |

---


 
 
 #### [PageResponse](#PageResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | hasPrevious | Boolean? |  yes  |  |
 | size | Int? |  yes  |  |
 | hasNext | Boolean? |  yes  |  |
 | current | String? |  yes  |  |
 | itemTotal | Int? |  yes  |  |

---


 
 
 #### [HsnCodesObject](#HsnCodesObject)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tax1 | Double? |  yes  |  |
 | taxOnEsp | Boolean? |  yes  |  |
 | threshold2 | Double? |  yes  |  |
 | companyId | Int? |  yes  |  |
 | id | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | hsnCode | String? |  yes  |  |
 | taxOnMrp | Boolean? |  yes  |  |
 | threshold1 | Double? |  yes  |  |
 | tax2 | Double? |  yes  |  |
 | hs2Code | String? |  yes  |  |

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
 | taxOnEsp | Boolean? |  yes  |  |
 | threshold2 | Double? |  yes  |  |
 | companyId | Int |  no  |  |
 | hsnCode | String |  no  |  |
 | uid | Int? |  yes  |  |
 | taxOnMrp | Boolean |  no  |  |
 | threshold1 | Double |  no  |  |
 | tax2 | Double? |  yes  |  |
 | hs2Code | String |  no  |  |

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
 | name | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | departments | ArrayList<String>? |  yes  |  |
 | logo | [Media](#Media)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
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
 | name | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | logo | [Media](#Media)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | priorityOrder | Int? |  yes  |  |

---


 
 
 #### [DepartmentResponse](#DepartmentResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Department](#Department)>? |  yes  |  |

---


 
 
 #### [DepartmentIdentifier](#DepartmentIdentifier)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | slug | String? |  yes  |  |

---


 
 
 #### [ThirdLevelChild](#ThirdLevelChild)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | name | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | childs | ArrayList<HashMap<String,Any>>? |  yes  |  |

---


 
 
 #### [SecondLevelChild](#SecondLevelChild)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | name | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | childs | ArrayList<[ThirdLevelChild](#ThirdLevelChild)>? |  yes  |  |

---


 
 
 #### [Child](#Child)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | name | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | childs | ArrayList<[SecondLevelChild](#SecondLevelChild)>? |  yes  |  |

---


 
 
 #### [CategoryItems](#CategoryItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | childs | ArrayList<[Child](#Child)>? |  yes  |  |

---


 
 
 #### [DepartmentCategoryTree](#DepartmentCategoryTree)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | department | String? |  yes  |  |
 | items | ArrayList<[CategoryItems](#CategoryItems)>? |  yes  |  |

---


 
 
 #### [CategoryListingResponse](#CategoryListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | departments | ArrayList<[DepartmentIdentifier](#DepartmentIdentifier)>? |  yes  |  |
 | data | ArrayList<[DepartmentCategoryTree](#DepartmentCategoryTree)>? |  yes  |  |

---


 
 
 #### [ApplicationProductListingResponse](#ApplicationProductListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sortOn | ArrayList<[ProductSortOn](#ProductSortOn)>? |  yes  |  |
 | page | [Page](#Page) |  no  |  |
 | filters | ArrayList<[ProductFilters](#ProductFilters)>? |  yes  |  |
 | items | ArrayList<[ProductListingDetail](#ProductListingDetail)>? |  yes  |  |

---


 
 
 #### [ProductDetail](#ProductDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | brand | [ProductBrand](#ProductBrand)? |  yes  |  |
 | groupedAttributes | ArrayList<[ProductDetailGroupedAttribute](#ProductDetailGroupedAttribute)>? |  yes  |  |
 | highlights | ArrayList<String>? |  yes  |  |
 | itemCode | String? |  yes  |  |
 | slug | String |  no  |  |
 | description | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | imageNature | String? |  yes  |  |
 | similars | ArrayList<String>? |  yes  |  |
 | color | String? |  yes  |  |
 | tryouts | ArrayList<String>? |  yes  |  |
 | type | String? |  yes  |  |
 | name | String? |  yes  |  |
 | shortDescription | String? |  yes  |  |
 | productOnlineDate | String? |  yes  |  |
 | promoMeta | HashMap<String,Any>? |  yes  |  |
 | itemType | String? |  yes  |  |
 | teaserTag | HashMap<String,Any>? |  yes  |  |
 | attributes | HashMap<String,Any>? |  yes  |  |
 | medias | ArrayList<[Media1](#Media1)>? |  yes  |  |
 | hasVariant | Boolean? |  yes  |  |
 | ratingCount | Int? |  yes  |  |
 | rating | Double? |  yes  |  |

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




