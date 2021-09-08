



### Class and Methods

* ## [Theme](#Theme)
  * Methods
    * [getAllPages](#getallpages)
    * [createPage](#createpage)
    * [updateMultiplePages](#updatemultiplepages)
    * [getPage](#getpage)
    * [updatePage](#updatepage)
    * [deletePage](#deletepage)
    * [getThemeLibrary](#getthemelibrary)
    * [addToThemeLibrary](#addtothemelibrary)
    * [applyTheme](#applytheme)
    * [isUpgradable](#isupgradable)
    * [upgradeTheme](#upgradetheme)
    * [getPublicThemes](#getpublicthemes)
    * [createTheme](#createtheme)
    * [getAppliedTheme](#getappliedtheme)
    * [getFonts](#getfonts)
    * [getThemeById](#getthemebyid)
    * [updateTheme](#updatetheme)
    * [deleteTheme](#deletetheme)
    * [getThemeForPreview](#getthemeforpreview)
    * [publishTheme](#publishtheme)
    * [unpublishTheme](#unpublishtheme)
    * [archiveTheme](#archivetheme)
    * [unarchiveTheme](#unarchivetheme)
    
---

## Theme


#### getAllPages
Get all pages of a theme




```kotlin
client.application("<APPLICATION_ID>").theme.getAllPages(themeId: themeId).safeAwait{ response,error->
    
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
| themeId | String | yes | ID of the theme to be retrieved |  



Use this API to retrieve all the available pages of a theme by its ID.

*Returned Response*




[AllAvailablePageSchema](#AllAvailablePageSchema)

Success. Returns an array all the pages of the theme. Refer `AllAvailablePageSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; All pages</i></summary>

```json
{
  "$ref": "#/components/examples/AllAvailablePagesExample"
}
```
</details>

</details>









---


#### createPage
Create a page 




```kotlin
client.application("<APPLICATION_ID>").theme.createPage(themeId: themeId, body: body).safeAwait{ response,error->
    
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
| themeId | String | yes | ID of the theme |  
| body | [AvailablePageSchema](#AvailablePageSchema) | yes | Request body |


Use this API to create a page for a theme by its ID.

*Returned Response*




[AvailablePageSchema](#AvailablePageSchema)

Success. Returns the page of the theme. Refer `AvailablePageSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; page</i></summary>

```json
{
  "$ref": "#/components/examples/AvailablePageExample"
}
```
</details>

</details>









---


#### updateMultiplePages
Update multiple pages of a theme




```kotlin
client.application("<APPLICATION_ID>").theme.updateMultiplePages(themeId: themeId, body: body).safeAwait{ response,error->
    
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
| themeId | String | yes | ID of the theme to be retrieved |  
| body | [AllAvailablePageSchema](#AllAvailablePageSchema) | yes | Request body |


Use this API to update multiple pages of a theme by its ID.

*Returned Response*




[AllAvailablePageSchema](#AllAvailablePageSchema)

Success. Returns an array all the pages of the theme. Refer `AllAvailablePageSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; All pages</i></summary>

```json
{
  "$ref": "#/components/examples/AllAvailablePagesExample"
}
```
</details>

</details>









---


#### getPage
Get page of a theme




```kotlin
client.application("<APPLICATION_ID>").theme.getPage(themeId: themeId, pageValue: pageValue).safeAwait{ response,error->
    
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
| themeId | String | yes | ID of the theme to be retrieved |   
| pageValue | String | yes | Value of the page to be retrieved |  



Use this API to retrieve a page of a theme.

*Returned Response*




[AvailablePageSchema](#AvailablePageSchema)

Success. Returns an object of the page.  Refer `AvailablePageSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Home page</i></summary>

```json
{
  "$ref": "#/components/examples/AvailablePageExample"
}
```
</details>

</details>









---


#### updatePage
Updates a page 




```kotlin
client.application("<APPLICATION_ID>").theme.updatePage(themeId: themeId, pageValue: pageValue, body: body).safeAwait{ response,error->
    
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
| themeId | String | yes | ID of the theme |   
| pageValue | String | yes | Value of the page to be updated |  
| body | [AvailablePageSchema](#AvailablePageSchema) | yes | Request body |


Use this API to update a page for a theme by its ID.

*Returned Response*




[AvailablePageSchema](#AvailablePageSchema)

Success. Returns a the page of the theme. Refer `AvailablePageSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; page</i></summary>

```json
{
  "$ref": "#/components/examples/AvailablePageExample"
}
```
</details>

</details>









---


#### deletePage
Deletes a page 




```kotlin
client.application("<APPLICATION_ID>").theme.deletePage(themeId: themeId, pageValue: pageValue).safeAwait{ response,error->
    
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
| themeId | String | yes | ID of the theme |   
| pageValue | String | yes | Value of the page to be updated |  



Use this API to delete a page for a theme by its ID and page_value.

*Returned Response*




[AvailablePageSchema](#AvailablePageSchema)

Success. Returns a the page of the theme. Refer `AvailablePageSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; page</i></summary>

```json
{
  "$ref": "#/components/examples/AvailablePageExample"
}
```
</details>

</details>









---


#### getThemeLibrary
Get a list of themes from the theme library




```kotlin
client.application("<APPLICATION_ID>").theme.getThemeLibrary(pageSize: pageSize, pageNo: pageNo).safeAwait{ response,error->
    
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
| pageSize | Int? | no | The number of items to retrieve in each page. Default value is 10.  |   
| pageNo | Int? | no | The page number to navigate through the given set of results. Default value is 1. |  



Theme library is a personalized collection of themes that are chosen and added from the available themes. Use this API to fetch a list of themes from the library along with their configuration details. 

*Returned Response*




[ThemesListingResponseSchema](#ThemesListingResponseSchema)

Success. Refer `ThemesListingResponseSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/ThemesListingResponse"
}
```
</details>

</details>









---


#### addToThemeLibrary
Add a theme to the theme library




```kotlin
client.application("<APPLICATION_ID>").theme.addToThemeLibrary(body: body).safeAwait{ response,error->
    
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
| body | [AddThemeRequestSchema](#AddThemeRequestSchema) | yes | Request body |


Theme library is a personalized collection of themes that are chosen and added from the available themes. Use this API to choose a theme and add it to the theme library.

*Returned Response*




[ThemesSchema](#ThemesSchema)

Success. Refer `ThemesSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
}
```
</details>

</details>









---


#### applyTheme
Apply a theme




```kotlin
client.application("<APPLICATION_ID>").theme.applyTheme(body: body).safeAwait{ response,error->
    
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
| body | [AddThemeRequestSchema](#AddThemeRequestSchema) | yes | Request body |


Use this API to apply a theme to the website.

*Returned Response*




[ThemesSchema](#ThemesSchema)

Success. Refer `ThemesSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
}
```
</details>

</details>









---


#### isUpgradable
Checks if theme is upgradable




```kotlin
client.application("<APPLICATION_ID>").theme.isUpgradable(themeId: themeId).safeAwait{ response,error->
    
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
| themeId | String | yes | Theme ID |  



There's always a possibility that new features get added to a theme. Use this API to check if the applied theme has an upgrade available.

*Returned Response*




[UpgradableThemeSchema](#UpgradableThemeSchema)

Success. If the boolean value of `upgrade` returns **true**, the theme can be upgraded. Refer `UpgradableThemeSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/UpgradableTheme"
}
```
</details>

</details>









---


#### upgradeTheme
Upgrade a theme




```kotlin
client.application("<APPLICATION_ID>").theme.upgradeTheme(themeId: themeId).safeAwait{ response,error->
    
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
| themeId | String | yes | ID allotted to the theme. |  



Use this API to upgrade the current theme to its latest version.

*Returned Response*




[ThemesSchema](#ThemesSchema)

Success. Upgrades the theme and shares the details of the new version in the response. Refer `ThemesSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
}
```
</details>

</details>









---


#### getPublicThemes
Get all public themes




```kotlin
client.application("<APPLICATION_ID>").theme.getPublicThemes(pageSize: pageSize, pageNo: pageNo).safeAwait{ response,error->
    
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
| pageSize | Int? | no | The number of items to retrieve in each page. Default value is 10.  |   
| pageNo | Int? | no | The page number to navigate through the given set of results. Default value is 1.  |  



Use this API to get a list of free themes that you can apply to your website.

*Returned Response*




[ThemesListingResponseSchema](#ThemesListingResponseSchema)

Success. Refer `ThemesListingResponseSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/ThemesListingResponse"
}
```
</details>

</details>









---


#### createTheme
Create a new theme




```kotlin
client.application("<APPLICATION_ID>").theme.createTheme(body: body).safeAwait{ response,error->
    
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
| body | [ThemesSchema](#ThemesSchema) | yes | Request body |


Themes improve the look and appearance of a website. Use this API to create a theme.

*Returned Response*




[ThemesSchema](#ThemesSchema)

Theme




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
}
```
</details>

</details>









---


#### getAppliedTheme
Get the applied theme




```kotlin
client.application("<APPLICATION_ID>").theme.getAppliedTheme().safeAwait{ response,error->
    
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



Use this API to retrieve the theme that is currently applied to the website along with its details.

*Returned Response*




[ThemesSchema](#ThemesSchema)

Success. Refer `ThemesSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
}
```
</details>

</details>









---


#### getFonts
Get all the supported fonts in a theme




```kotlin
client.application("<APPLICATION_ID>").theme.getFonts().safeAwait{ response,error->
    
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



Font is a collection of characters with a similar design. Use this API to retrieve a list of website fonts.

*Returned Response*




[FontsSchema](#FontsSchema)

Success. Refer `FontsSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/FontsResponse"
}
```
</details>

</details>









---


#### getThemeById
Gets theme by id




```kotlin
client.application("<APPLICATION_ID>").theme.getThemeById(themeId: themeId).safeAwait{ response,error->
    
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
| themeId | String | yes | ID allotted to the theme. |  



Use this API to retrieve the details of a specific theme by using its ID.

*Returned Response*




[ThemesSchema](#ThemesSchema)

Success. Refer `ThemesSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
}
```
</details>

</details>









---


#### updateTheme
Update a theme




```kotlin
client.application("<APPLICATION_ID>").theme.updateTheme(themeId: themeId, body: body).safeAwait{ response,error->
    
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
| themeId | String | yes | ID allotted to the theme. |  
| body | [ThemesSchema](#ThemesSchema) | yes | Request body |


Use this API to edit an existing theme. You can customize the website font, sections, images, styles, and many more.

*Returned Response*




[ThemesSchema](#ThemesSchema)

Success. Refer `ThemesSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
}
```
</details>

</details>









---


#### deleteTheme
Delete a theme




```kotlin
client.application("<APPLICATION_ID>").theme.deleteTheme(themeId: themeId).safeAwait{ response,error->
    
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
| themeId | String | yes | ID allotted to the theme. |  



Use this API to delete a theme from the theme library.

*Returned Response*




[ThemesSchema](#ThemesSchema)

Success. Refer `ThemesSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
}
```
</details>

</details>









---


#### getThemeForPreview
Get a theme preview




```kotlin
client.application("<APPLICATION_ID>").theme.getThemeForPreview(themeId: themeId).safeAwait{ response,error->
    
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
| themeId | String | yes | ID allotted to the theme. |  



A theme can be previewed before applying it. Use this API to retrieve the theme preview by using its ID.

*Returned Response*




[ThemesSchema](#ThemesSchema)

Success. Refer `ThemesSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
}
```
</details>

</details>









---


#### publishTheme
Publish a theme




```kotlin
client.application("<APPLICATION_ID>").theme.publishTheme(themeId: themeId).safeAwait{ response,error->
    
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
| themeId | String | yes | ID allotted to the theme. |  



Use this API to publish a theme that is either newly created or edited.

*Returned Response*




[ThemesSchema](#ThemesSchema)

Success. Refer `ThemesSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
}
```
</details>

</details>









---


#### unpublishTheme
Unpublish a theme




```kotlin
client.application("<APPLICATION_ID>").theme.unpublishTheme(themeId: themeId).safeAwait{ response,error->
    
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
| themeId | String | yes | ID allotted to the theme. |  



Use this API to remove an existing theme from the list of available themes.

*Returned Response*




[ThemesSchema](#ThemesSchema)

Success. Refer `ThemesSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
}
```
</details>

</details>









---


#### archiveTheme
Archive a theme




```kotlin
client.application("<APPLICATION_ID>").theme.archiveTheme(themeId: themeId).safeAwait{ response,error->
    
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
| themeId | String | yes | ID allotted to the theme. |  



Use this API to store an existing theme but not delete it so that it can be used in future if required. 

*Returned Response*




[ThemesSchema](#ThemesSchema)

Success. Refer `ThemesSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
}
```
</details>

</details>









---


#### unarchiveTheme
Unarchive a theme




```kotlin
client.application("<APPLICATION_ID>").theme.unarchiveTheme(themeId: themeId).safeAwait{ response,error->
    
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
| themeId | String | yes | ID allotted to the theme. |  



Use this API to restore an archived theme and bring it back for editing or publishing. 

*Returned Response*




[ThemesSchema](#ThemesSchema)

Success. Refer `ThemesSchema` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; Success</i></summary>

```json
{
  "$ref": "#/components/examples/Themes"
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




