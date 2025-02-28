



##### [Back to Application docs](./README.md)

## Feedback Methods
User Reviews and Rating System
* [createAbuseReport](#createabusereport)
* [updateAbuseReport](#updateabusereport)
* [getAbuseReports](#getabusereports)
* [getAttributes](#getattributes)
* [createAttribute](#createattribute)
* [getAttribute](#getattribute)
* [updateAttribute](#updateattribute)
* [createComment](#createcomment)
* [updateComment](#updatecomment)
* [getComments](#getcomments)
* [checkEligibility](#checkeligibility)
* [deleteMedia](#deletemedia)
* [createMedia](#createmedia)
* [updateMedia](#updatemedia)
* [getMedias](#getmedias)
* [getReviewSummaries](#getreviewsummaries)
* [createReview](#createreview)
* [updateReview](#updatereview)
* [getReviews](#getreviews)
* [getTemplates](#gettemplates)
* [createQuestion](#createquestion)
* [updateQuestion](#updatequestion)
* [getQuestionAndAnswers](#getquestionandanswers)
* [getVotes](#getvotes)
* [createVote](#createvote)
* [updateVote](#updatevote)



## Methods with example and description


### createAbuseReport
Post a new abuse request




```kotlin
feedback.createAbuseReport(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [ReportAbuseRequest](#ReportAbuseRequest) | yes | Request body |


Use this API to report a specific entity (question/review/comment) for abuse.

*Returned Response:*




[InsertResponse](#InsertResponse)

Success. Returns an abuse ID.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### updateAbuseReport
Update abuse details




```kotlin
feedback.updateAbuseReport(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [UpdateAbuseStatusRequest](#UpdateAbuseStatusRequest) | yes | Request body |


Use this API to update the abuse details, i.e. status and description.

*Returned Response:*




[UpdateResponse](#UpdateResponse)

Success.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getAbuseReports
Get a list of abuse data




```kotlin
feedback.getAbuseReports(entityId: entityId, entityType: entityType, id: id, pageId: pageId, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| entityId | String | yes | ID of the eligible entity as specified in the entity type (question ID/review ID/comment ID). |   
| entityType | String | yes | Type of entity, e.g. question, review or comment. |   
| id | String? | no | abuse id |   
| pageId | String? | no | Pagination page ID to retrieve next set of results. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |  



Use this API to retrieve a list of abuse data from entity type and entity ID.

*Returned Response:*




[ReportAbuseGetResponse](#ReportAbuseGetResponse)

Success. Check the example shown below or refer `ReportAbuseGetResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getAttributes
Get a list of attribute data




```kotlin
feedback.getAttributes(pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| pageNo | Int? | no | The page number to navigate through the given set of results. Default value is 1.  |   
| pageSize | Int? | no | The number of items to retrieve in each page. |  



Use this API to retrieve a list of all attribute data, e.g. quality, material, product fitting, packaging, etc.

*Returned Response:*




[AttributeResponse](#AttributeResponse)

Success. Check the example shown below or refer `AttributeResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### createAttribute
Add a new attribute request




```kotlin
feedback.createAttribute(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [SaveAttributeRequest](#SaveAttributeRequest) | yes | Request body |


Use this API to add a new attribute (e.g. product quality/material/value for money) with its name, slug and description.

*Returned Response:*




[InsertResponse](#InsertResponse)

Success. Returns an attribute ID.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getAttribute
Get data of a single attribute




```kotlin
feedback.getAttribute(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of an attribute. You can get slug value from the endpoint 'service/application/feedback/v1.0/attributes'. |  



Use this API to retrieve a single attribute data from a given slug.

*Returned Response:*




[Attribute](#Attribute)

Success. Check the example shown below or refer `Attribute` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### updateAttribute
Update details of an attribute 




```kotlin
feedback.updateAttribute(slug: slug, body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of an attribute. You can get slug value from the endpoint 'service/application/feedback/v1.0/attributes'. |  
| body | [UpdateAttributeRequest](#UpdateAttributeRequest) | yes | Request body |


Use this API update the attribute's name and description.

*Returned Response:*




[UpdateResponse](#UpdateResponse)

Success.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### createComment
Post a new comment




```kotlin
feedback.createComment(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [CommentRequest](#CommentRequest) | yes | Request body |


Use this API to add a new comment for a specific entity.

*Returned Response:*




[InsertResponse](#InsertResponse)

Success. Returns a comment ID.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### updateComment
Update the status of a comment




```kotlin
feedback.updateComment(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [UpdateCommentRequest](#UpdateCommentRequest) | yes | Request body |


Use this API to update the comment status (active or approve) along with new comment if any.

*Returned Response:*




[UpdateResponse](#UpdateResponse)

Success.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getComments
Get a list of comments




```kotlin
feedback.getComments(entityType: entityType, id: id, entityId: entityId, userId: userId, pageId: pageId, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| entityType | String | yes | Type of entity, e.g. question, review or comment. |   
| id | String? | no | Comment ID |   
| entityId | String? | no | ID of the eligible entity as specified in the entity type (question ID/review ID/comment ID). |   
| userId | String? | no | User ID - a flag/filter to get comments for a user. |   
| pageId | String? | no | Pagination page ID to retrieve next set of results. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |  



Use this API to retrieve a list of comments for a specific entity type, e.g. products.

*Returned Response:*




[CommentGetResponse](#CommentGetResponse)

Success. Check the example shown below or refer `CommentGetResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### checkEligibility
Checks eligibility to rate and review, and shows the cloud media configuration




```kotlin
feedback.checkEligibility(entityType: entityType, entityId: entityId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| entityType | String | yes | Type of entity, e.g. question, rate, review, answer, or comment. |   
| entityId | String | yes | ID of the eligible entity as specified in the entity type. |  



Use this API to check whether an entity is eligible to be rated and reviewed. Moreover, it shows the cloud media configuration too.

*Returned Response:*




[CheckEligibilityResponse](#CheckEligibilityResponse)

Success. Returns a Product object. Check the example shown below or refer `CheckEligibilityResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### deleteMedia
Delete Media




```kotlin
feedback.deleteMedia(ids: ids).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| ids | ArrayList<String> | yes | List of media ID |  



Use this API to delete media for an entity ID.

*Returned Response:*




[UpdateResponse](#UpdateResponse)

Success.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### createMedia
Add Media




```kotlin
feedback.createMedia(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [AddMediaListRequest](#AddMediaListRequest) | yes | Request body |


Use this API to add media to an entity, e.g. review.

*Returned Response:*




[InsertResponse](#InsertResponse)

Success. Returns media IDs.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### updateMedia
Update Media




```kotlin
feedback.updateMedia(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [UpdateMediaListRequest](#UpdateMediaListRequest) | yes | Request body |


Use this API to update media (archive/approve) for an entity.

*Returned Response:*




[UpdateResponse](#UpdateResponse)

Success.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getMedias
Get Media




```kotlin
feedback.getMedias(entityType: entityType, entityId: entityId, id: id, type: type, pageId: pageId, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| entityType | String | yes | Type of entity, e.g. question or product. |   
| entityId | String | yes | ID of the eligible entity as specified in the entity type(question ID/product ID). |   
| id | String? | no | ID of the media. |   
| type | String? | no | Media type. |   
| pageId | String? | no | Pagination page ID to retrieve next set of results. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |  



Use this API to retrieve all media from an entity.

*Returned Response:*




[MediaGetResponse](#MediaGetResponse)

Success. Check the example shown below or refer `MediaGetResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getReviewSummaries
Get a review summary




```kotlin
feedback.getReviewSummaries(entityType: entityType, entityId: entityId, id: id, pageId: pageId, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| entityType | String | yes | Type of entity, e.g. product, delivery, seller, order placed, order delivered, application, or template. |   
| entityId | String | yes | ID of the eligible entity as specified in the entity type. |   
| id | String? | no | Review summary identifier. |   
| pageId | String? | no | Pagination page ID to retrieve next set of results. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |  



Review summary gives ratings and attribute metrics of a review per entity. Use this API to retrieve the following response data: review count, rating average. 'review metrics'/'attribute rating metrics' which contains name, type, average and count.

*Returned Response:*




[ReviewMetricGetResponse](#ReviewMetricGetResponse)

Success. Check the example shown below or refer `ReviewMetricGetResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### createReview
Add customer reviews




```kotlin
feedback.createReview(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [UpdateReviewRequest](#UpdateReviewRequest) | yes | Request body |


Use this API to add customer reviews for a specific entity along with the following data: attributes rating, entity rating, title, description, media resources and template ID.

*Returned Response:*




[UpdateResponse](#UpdateResponse)

Success. Returns a review ID.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### updateReview
Update customer reviews




```kotlin
feedback.updateReview(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [UpdateReviewRequest](#UpdateReviewRequest) | yes | Request body |


Use this API to update customer reviews for a specific entity along with following data: attributes rating, entity rating, title, description, media resources and template ID.

*Returned Response:*




[UpdateResponse](#UpdateResponse)

Success.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getReviews
Get list of customer reviews




```kotlin
feedback.getReviews(entityType: entityType, entityId: entityId, id: id, userId: userId, media: media, rating: rating, attributeRating: attributeRating, facets: facets, sort: sort, active: active, approve: approve, pageId: pageId, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| entityType | String | yes | Type of entity, e.g. product, delivery, seller, l3, order placed, order delivered, application, or template. |   
| entityId | String | yes | ID of the eligible entity as specified in the entity type. |   
| id | String? | no | ID of the review. |   
| userId | String? | no | ID of the user. |   
| media | String? | no | media type, e.g. image | video | video_file | video_link |   
| rating | ArrayList<Double>? | no | rating filter, e.g. 1-5 |   
| attributeRating | ArrayList<String>? | no | Filter for attribute rating. |   
| facets | Boolean? | no | This is a boolean value for enabling metadata (facets). Selecting *true* will enable facets. |   
| sort | String? | no | Sort by: default | top | recent |   
| active | Boolean? | no | Get the active reviews. |   
| approve | Boolean? | no | Get the approved reviews. |   
| pageId | String? | no | Pagination page ID to retrieve next set of results. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |  



Use this API to retrieve a list of customer reviews based on entity and filters provided.

*Returned Response:*




[ReviewGetResponse](#ReviewGetResponse)

Success. Check the example shown below or refer `ReviewGetResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getTemplates
Get the feedback templates for a product or l3




```kotlin
feedback.getTemplates(templateId: templateId, entityId: entityId, entityType: entityType).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| templateId | String? | no | ID of the feedback template. |   
| entityId | String? | no | ID of the eligible entity as specified in the entity type. |   
| entityType | String? | no | Type of entity, e.g. product, delivery, seller, l3, order placed, order delivered, or application. |  



Use this API to retrieve the details of the following feedback template. order, delivered, application, seller, order, placed, product

*Returned Response:*




[TemplateGetResponse](#TemplateGetResponse)

Success. Check the example shown below or refer `TemplateGetResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### createQuestion
Create a new question




```kotlin
feedback.createQuestion(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [CreateQNARequest](#CreateQNARequest) | yes | Request body |


Use this API to create a new question with following data- tags, text, type, choices for MCQ type questions, maximum length of answer.

*Returned Response:*




[InsertResponse](#InsertResponse)

Success. Returns a qna ID.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### updateQuestion
Update a question




```kotlin
feedback.updateQuestion(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [UpdateQNARequest](#UpdateQNARequest) | yes | Request body |


Use this API to update the status of a question, its tags and its choices.

*Returned Response:*




[UpdateResponse](#UpdateResponse)

Success.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getQuestionAndAnswers
Get a list of QnA




```kotlin
feedback.getQuestionAndAnswers(entityType: entityType, entityId: entityId, id: id, userId: userId, showAnswer: showAnswer, pageId: pageId, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| entityType | String | yes | Type of entity, e.g. product, l3, etc. |   
| entityId | String | yes | ID of the eligible entity as specified in the entity type. |   
| id | String? | no | QNA ID |   
| userId | String? | no | User ID |   
| showAnswer | Boolean? | no | This is a boolean value. Select *true* to display answers given. |   
| pageId | String? | no | Pagination page ID to retrieve next set of results. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |  



Use this API to retrieve a list of questions and answers for a given entity.

*Returned Response:*




[QNAGetResponse](#QNAGetResponse)

Success. Check the example shown below or refer `QNAGetResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getVotes
Get a list of votes




```kotlin
feedback.getVotes(id: id, refType: refType, pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| id | String? | no | vote ID |   
| refType | String? | no | Entity type, e.g. review | comment. |   
| pageNo | Int? | no | The page number to navigate through the given set of results. Default value is 1. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |  



Use this API to retrieve a list of votes of a current logged in user. Votes can be filtered using `ref_type`, i.e. review | comment.

*Returned Response:*




[VoteResponse](#VoteResponse)

Success. Check the example shown below or refer `VoteResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### createVote
Create a new vote




```kotlin
feedback.createVote(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [VoteRequest](#VoteRequest) | yes | Request body |


Use this API to create a new vote, where the action could be an upvote or a downvote. This is useful when you want to give a vote (say upvote) to a review (ref_type) of a product (entity_type).

*Returned Response:*




[InsertResponse](#InsertResponse)

Success. Returns a vote ID.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### updateVote
Update a vote




```kotlin
feedback.updateVote(body: body).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- |
| body | [UpdateVoteRequest](#UpdateVoteRequest) | yes | Request body |


Use this API to update a vote with a new action, i.e. either an upvote or a downvote.

*Returned Response:*




[UpdateResponse](#UpdateResponse)

Success.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---



### Schemas

 
 
 #### [AbuseReport](#AbuseReport)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | abused | Boolean? |  yes  |  |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | description | String? |  yes  |  |
 | entity | [Entity](#Entity)? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | state | [FeedbackState](#FeedbackState)? |  yes  |  |
 | tags | ArrayList<[TagMeta](#TagMeta)>? |  yes  |  |

---


 
 
 #### [Access](#Access)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | answer | Boolean? |  yes  |  |
 | askQuestion | Boolean? |  yes  |  |
 | comment | Boolean? |  yes  |  |
 | rnr | Boolean? |  yes  |  |

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


 
 
 #### [ApplicationSchema](#ApplicationSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |

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


 
 
 #### [AttributeResponse](#AttributeResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Attribute](#Attribute)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [AutoDetectors](#AutoDetectors)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | textDetector | ArrayList<[TextDetector](#TextDetector)>? |  yes  |  |

---


 
 
 #### [CheckEligibilityResponse](#CheckEligibilityResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | access | [Access](#Access)? |  yes  |  |

---


 
 
 #### [Cloud](#Cloud)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | provider | String? |  yes  |  |

---


 
 
 #### [Comment](#Comment)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | comment | ArrayList<String>? |  yes  |  |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | entity | [Entity](#Entity)? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | state | [FeedbackState](#FeedbackState)? |  yes  |  |
 | tags | ArrayList<[TagMeta](#TagMeta)>? |  yes  |  |
 | voteCount | [VoteCount](#VoteCount)? |  yes  |  |

---


 
 
 #### [CommentGetResponse](#CommentGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Comment](#Comment)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [CommentRequest](#CommentRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | comment | ArrayList<String> |  no  |  |
 | entityId | String |  no  |  |
 | entityType | String |  no  |  |

---


 
 
 #### [CreateQNARequest](#CreateQNARequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | choices | ArrayList<String>? |  yes  |  |
 | entityId | String |  no  |  |
 | entityType | String |  no  |  |
 | maxLen | Int? |  yes  |  |
 | sortPriority | Int? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |
 | text | String |  no  |  |
 | type | String? |  yes  |  |

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


 
 
 #### [CustomerReview](#CustomerReview)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | autoDetectors | [AutoDetectors](#AutoDetectors)? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | deviceMeta | [DeviceMeta](#DeviceMeta)? |  yes  |  |
 | entity | [ProductEntity](#ProductEntity)? |  yes  |  |
 | id | String? |  yes  |  |
 | locationMeta | [LocationMeta](#LocationMeta)? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | name | String? |  yes  |  |
 | rating | [ReviewRating](#ReviewRating)? |  yes  |  |
 | review | [Review](#Review)? |  yes  |  |
 | slug | String? |  yes  |  |
 | state | [State](#State)? |  yes  |  |
 | tags | ArrayList<[TagMeta](#TagMeta)>? |  yes  |  |
 | template | [Template](#Template)? |  yes  |  |
 | voteCount | [VoteCount](#VoteCount)? |  yes  |  |

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
 | type | String? |  yes  | entity type could be review/comment/ |

---


 
 
 #### [EntityMeta](#EntityMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | orderId | String? |  yes  |  |
 | type | String? |  yes  | product, delivery,seller |

---


 
 
 #### [FeedbackError](#FeedbackError)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | code | String? |  yes  |  |
 | exception | String? |  yes  |  |
 | info | String? |  yes  |  |
 | message | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | requestId | String? |  yes  |  |
 | stackTrace | String? |  yes  |  |
 | status | Int? |  yes  |  |

---


 
 
 #### [FeedbackMedia](#FeedbackMedia)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | application | [ApplicationSchema](#ApplicationSchema)? |  yes  |  |
 | cloud | [Cloud](#Cloud)? |  yes  |  |
 | createdBy | [CreatedBy](#CreatedBy)? |  yes  |  |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | description | String? |  yes  |  |
 | entity | [Entity](#Entity)? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | reference | [Entity](#Entity)? |  yes  |  |
 | state | [MediaState](#MediaState)? |  yes  |  |
 | tags | ArrayList<[TagMeta](#TagMeta)>? |  yes  |  |
 | type | String? |  yes  |  |
 | url | [Url](#Url)? |  yes  |  |

---


 
 
 #### [FeedbackState](#FeedbackState)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  |  |
 | archive | Boolean? |  yes  |  |
 | media | String? |  yes  |  |
 | qna | Boolean? |  yes  |  |
 | rating | Boolean? |  yes  |  |
 | review | Boolean? |  yes  |  |

---


 
 
 #### [GeoLoc](#GeoLoc)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | latitude | String? |  yes  |  |
 | longitude | String? |  yes  |  |

---


 
 
 #### [InsertResponse](#InsertResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ids | String? |  yes  |  |

---


 
 
 #### [Location](#Location)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | countryCode | String? |  yes  |  |
 | flagUrl | String? |  yes  |  |
 | geoLoc | [GeoLoc](#GeoLoc)? |  yes  |  |
 | name | String? |  yes  |  |
 | pincode | String? |  yes  |  |

---


 
 
 #### [LocationMeta](#LocationMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | demand | [Location](#Location)? |  yes  |  |
 | supply | [Location](#Location)? |  yes  |  |

---


 
 
 #### [MediaGetResponse](#MediaGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[FeedbackMedia](#FeedbackMedia)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [MediaMeta](#MediaMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | cloud | [Cloud](#Cloud)? |  yes  |  |
 | comment | ArrayList<String>? |  yes  |  |
 | description | String? |  yes  |  |
 | id | String? |  yes  |  |
 | type | String? |  yes  |  |
 | url | [Url](#Url)? |  yes  |  |

---


 
 
 #### [MediaState](#MediaState)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | approve | Boolean? |  yes  |  |
 | archive | Boolean? |  yes  |  |

---


 
 
 #### [NumberGetResponse](#NumberGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | page | [PageNumber](#PageNumber)? |  yes  |  |

---


 
 
 #### [Page](#Page)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | current | Int? |  yes  |  |
 | hasNext | Boolean? |  yes  |  |
 | hasPrevious | Boolean? |  yes  |  |
 | itemTotal | Int? |  yes  |  |
 | nextId | String? |  yes  |  |
 | size | Int? |  yes  |  |
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


 
 
 #### [ProductEntity](#ProductEntity)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  | For products, ID will be product ID, delivery, ID will be order id, seller ID will be company ID |
 | meta | [EntityMeta](#EntityMeta)? |  yes  |  |
 | type | String? |  yes  | product, delivery, seller, app, order |

---


 
 
 #### [QNA](#QNA)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | comments | ArrayList<[Comment](#Comment)>? |  yes  |  |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | entity | [Entity](#Entity)? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | question | [Question](#Question)? |  yes  |  |
 | state | [QNAState](#QNAState)? |  yes  |  |
 | tag | ArrayList<String>? |  yes  |  |
 | tags | ArrayList<[TagMeta](#TagMeta)>? |  yes  |  |

---


 
 
 #### [QNAGetResponse](#QNAGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[QNA](#QNA)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [QNAState](#QNAState)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  |  |
 | approve | Boolean? |  yes  |  |
 | modify | Boolean? |  yes  |  |
 | priority | Int? |  yes  |  |
 | reply | Boolean? |  yes  |  |
 | vote | Boolean? |  yes  |  |

---


 
 
 #### [Question](#Question)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | choices | ArrayList<String>? |  yes  |  |
 | maxLen | Int? |  yes  |  |
 | text | String? |  yes  |  |
 | type | String? |  yes  | type could be single_choice/text/multi_choice |

---


 
 
 #### [Rating](#Rating)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | attributes | ArrayList<[Attribute](#Attribute)>? |  yes  |  |
 | attributesSlugs | ArrayList<String>? |  yes  |  |
 | ui | [UI](#UI)? |  yes  |  |

---


 
 
 #### [RatingGetResponse](#RatingGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Rating](#Rating)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [RatingMetric](#RatingMetric)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | avg | Double? |  yes  |  |
 | count | Int? |  yes  | Valuetype could be average, count |
 | name | String? |  yes  | Attribute name like Camera, Battery and rating name like a number 5,4,3 |
 | slug | String? |  yes  |  |
 | type | String? |  yes  | type could be attribute_rating and rating |

---


 
 
 #### [ReportAbuseGetResponse](#ReportAbuseGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[AbuseReport](#AbuseReport)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

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
 | answerIds | ArrayList<String>? |  yes  |  |
 | comments | ArrayList<String>? |  yes  |  |
 | description | String? |  yes  |  |
 | mediaMeta | ArrayList<[MediaMeta](#MediaMeta)>? |  yes  |  |
 | title | String? |  yes  |  |

---


 
 
 #### [ReviewFacet](#ReviewFacet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | name | String? |  yes  |  |
 | selected | Boolean? |  yes  |  |
 | slug | String? |  yes  |  |
 | type | String? |  yes  | rating, attribute rating |

---


 
 
 #### [ReviewGetResponse](#ReviewGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | facets | ArrayList<[ReviewFacet](#ReviewFacet)>? |  yes  |  |
 | items | ArrayList<[CustomerReview](#CustomerReview)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |
 | sort | ArrayList<[SortMethod](#SortMethod)>? |  yes  |  |

---


 
 
 #### [ReviewMediaMeta](#ReviewMediaMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | maxCount | Double? |  yes  |  |
 | size | Double? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [ReviewMetric](#ReviewMetric)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | attributeMetric | ArrayList<[RatingMetric](#RatingMetric)>? |  yes  |  |
 | createdOn | String? |  yes  |  |
 | entity | [Entity](#Entity)? |  yes  | entity could be product, seller, delivery |
 | id | String? |  yes  |  |
 | modifiedOn | String? |  yes  |  |
 | ratingAvg | Double? |  yes  |  |
 | ratingCount | Int? |  yes  | total rating count |
 | ratingMetric | ArrayList<[RatingMetric](#RatingMetric)>? |  yes  |  |
 | reviewCount | Int? |  yes  | total review count |

---


 
 
 #### [ReviewMetricGetResponse](#ReviewMetricGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[ReviewMetric](#ReviewMetric)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [ReviewRating](#ReviewRating)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | attributes | ArrayList<[AttributeObject](#AttributeObject)>? |  yes  |  |
 | value | Double? |  yes  |  |

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


 
 
 #### [State](#State)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  |  |
 | approve | Boolean? |  yes  |  |
 | autoDecided | Boolean? |  yes  |  |
 | status | Int? |  yes  |  |

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
 | review | [TemplateReview](#TemplateReview)? |  yes  |  |
 | state | [FeedbackState](#FeedbackState)? |  yes  |  |

---


 
 
 #### [TemplateGetResponse](#TemplateGetResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Template](#Template)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---


 
 
 #### [TemplateReview](#TemplateReview)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | header | String? |  yes  |  |
 | imageMeta | [ReviewMediaMeta](#ReviewMediaMeta)? |  yes  |  |
 | title | String? |  yes  |  |
 | videoMeta | [ReviewMediaMeta](#ReviewMediaMeta)? |  yes  |  |
 | voteAllowed | Boolean? |  yes  |  |

---


 
 
 #### [TextDetector](#TextDetector)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | confidence | Double? |  yes  |  |
 | text | String? |  yes  |  |
 | textClass | String? |  yes  |  |
 | textType | String? |  yes  |  |

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


 
 
 #### [UpdateAbuseStatusRequest](#UpdateAbuseStatusRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | abusive | Boolean? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | approve | Boolean? |  yes  |  |
 | description | String? |  yes  |  |
 | entityId | String? |  yes  |  |
 | entityType | String? |  yes  |  |
 | id | String? |  yes  |  |

---


 
 
 #### [UpdateAttributeRequest](#UpdateAttributeRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | description | String? |  yes  |  |
 | name | String |  no  |  |
 | slug | String? |  yes  |  |

---


 
 
 #### [UpdateCommentRequest](#UpdateCommentRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  |  |
 | approve | Boolean? |  yes  |  |
 | comment | ArrayList<String> |  no  |  |
 | id | String |  no  |  |

---


 
 
 #### [UpdateMediaListRequest](#UpdateMediaListRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | approve | Boolean? |  yes  |  |
 | archive | Boolean? |  yes  |  |
 | entityType | String? |  yes  |  |
 | ids | ArrayList<String>? |  yes  |  |

---


 
 
 #### [UpdateQNARequest](#UpdateQNARequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | active | Boolean? |  yes  |  |
 | approve | Boolean? |  yes  |  |
 | choices | ArrayList<String>? |  yes  |  |
 | id | String? |  yes  |  |
 | tags | ArrayList<String>? |  yes  |  |

---


 
 
 #### [UpdateResponse](#UpdateResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |

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


 
 
 #### [UpdateVoteRequest](#UpdateVoteRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | action | String? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | id | String? |  yes  |  |
 | refId | String? |  yes  |  |
 | refType | String? |  yes  |  |

---


 
 
 #### [Url](#Url)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | main | String? |  yes  |  |
 | thumbnail | String? |  yes  |  |

---


 
 
 #### [Vote](#Vote)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | action | String? |  yes  | upvote and downvote |
 | dateMeta | [DateMeta](#DateMeta)? |  yes  |  |
 | entity | [Entity](#Entity)? |  yes  |  |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | reference | [Entity](#Entity)? |  yes  | review | comment |
 | state | [FeedbackState](#FeedbackState)? |  yes  |  |
 | tags | ArrayList<[TagMeta](#TagMeta)>? |  yes  |  |

---


 
 
 #### [VoteCount](#VoteCount)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | downvote | Int? |  yes  |  |
 | upvote | Int? |  yes  |  |

---


 
 
 #### [VoteRequest](#VoteRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | action | String? |  yes  |  |
 | entityId | String? |  yes  |  |
 | entityType | String? |  yes  |  |
 | refId | String? |  yes  |  |
 | refType | String? |  yes  | review | comment |

---


 
 
 #### [VoteResponse](#VoteResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Vote](#Vote)>? |  yes  |  |
 | page | [Page](#Page)? |  yes  |  |

---



