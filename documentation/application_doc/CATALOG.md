



##### [Back to Application docs](./README.md)

## Catalog Methods
Catalog API's allows you to access list of products, prices, seller details, similar features, variants and many more useful features. 
* [getProductDetailBySlug](#getproductdetailbyslug)
* [getProductSizesBySlug](#getproductsizesbyslug)
* [getProductPriceBySlug](#getproductpricebyslug)
* [getProductSellersBySlug](#getproductsellersbyslug)
* [getProductComparisonBySlugs](#getproductcomparisonbyslugs)
* [getSimilarComparisonProductBySlug](#getsimilarcomparisonproductbyslug)
* [getComparedFrequentlyProductBySlug](#getcomparedfrequentlyproductbyslug)
* [getProductSimilarByIdentifier](#getproductsimilarbyidentifier)
* [getProductVariantsBySlug](#getproductvariantsbyslug)
* [getProductStockByIds](#getproductstockbyids)
* [getProductStockForTimeByIds](#getproductstockfortimebyids)
* [getProducts](#getproducts)
* [getBrands](#getbrands)
* [getBrandDetailBySlug](#getbranddetailbyslug)
* [getCategories](#getcategories)
* [getCategoryDetailBySlug](#getcategorydetailbyslug)
* [getHomeProducts](#gethomeproducts)
* [getDepartments](#getdepartments)
* [getSearchResults](#getsearchresults)
* [getCollections](#getcollections)
* [getCollectionItemsBySlug](#getcollectionitemsbyslug)
* [getCollectionDetailBySlug](#getcollectiondetailbyslug)
* [getFollowedListing](#getfollowedlisting)
* [unfollowById](#unfollowbyid)
* [followById](#followbyid)
* [getFollowerCountById](#getfollowercountbyid)
* [getFollowIds](#getfollowids)
* [getStores](#getstores)
* [getInStockLocations](#getinstocklocations)
* [getLocationDetailsById](#getlocationdetailsbyid)



## Methods with example and description


### getProductDetailBySlug
Get a product




```kotlin
catalog.getProductDetailBySlug(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of a product. You can get slug value from the endpoint /service/application/catalog/v1.0/products/ |  



Use this API to retrieve a product by its slug value.

*Returned Response:*




[ProductDetail](#ProductDetail)

Success. Returns a Product object. Check the example shown below or refer `ProductDetail` for more details.




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
  "custom_order": {},
  "color": "808080",
  "similars": [
    "brand"
  ],
  "_custom_json": {}
}
```
</details>









---


### getProductSizesBySlug
Get the sizes of a product




```kotlin
catalog.getProductSizesBySlug(slug: slug, storeId: storeId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of a product. You can get slug value from the endpoint /service/application/catalog/v1.0/products/ |   
| storeId | Int? | no | The ID of the store that is selling the product, e.g. 1,2,3. |  



A product can have multiple sizes. Use this API to fetch all the available sizes of a product.

*Returned Response:*




[ProductSizes](#ProductSizes)

Success. Returns a ProductSize object. Check the example shown below or refer `ProductSizes` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "sellable": true,
  "sizes": [
    {
      "display": "13",
      "value": "13",
      "quantity": 10,
      "is_available": true
    }
  ],
  "discount": "",
  "stores": {
    "count": 1
  },
  "size_chart": {},
  "price": {
    "marked": {
      "min": 66.5,
      "max": 66.5,
      "currency_code": "INR",
      "currency_symbol": "₹"
    },
    "effective": {
      "min": 66.5,
      "max": 66.5,
      "currency_code": "INR",
      "currency_symbol": "₹"
    }
  },
  "tags": [
    "Digital"
  ]
}
```
</details>









---


### getProductPriceBySlug
Get the price of a product size at a PIN Code




```kotlin
catalog.getProductPriceBySlug(slug: slug, size: size, pincode: pincode, storeId: storeId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of a product. You can get slug value from the endpoint /service/application/catalog/v1.0/products/ |   
| size | String | yes | A string indicating the size of the product, e.g. S, M, XL. You can get slug value from the endpoint /service/application/catalog/v1.0/products/sizes |   
| pincode | String | yes | The PIN Code of the area near which the selling locations should be searched, e.g. 400059 |   
| storeId | Int? | no | The ID of the store that is selling the product, e.g. 1,2,3. |  



Prices may vary for different sizes of a product. Use this API to retrieve the price of a product size at all the selling locations near to a PIN Code.

*Returned Response:*




[ProductSizePriceResponse](#ProductSizePriceResponse)

Success. Returns a ProductSizePrice object. Check the example shown below or refer `ProductSizePriceResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "price_per_piece": {
    "effective": 66.5,
    "marked": 66.5,
    "currency_code": "INR",
    "currency_symbol": "₹"
  },
  "price": {
    "effective": 399,
    "marked": 399,
    "currency_code": "INR",
    "currency_symbol": "₹"
  },
  "quantity": 5,
  "pincode": 400603,
  "article_id": "1",
  "long_lat": [
    72.9159784,
    19.0990231
  ],
  "item_type": "set",
  "discount": "",
  "article_assignment": {
    "level": "multi-companies",
    "strategy": "optimal"
  },
  "seller": {
    "uid": 1,
    "name": "Natalie Norman"
  },
  "store": {
    "uid": 1,
    "name": "Wayne Lamb",
    "count": 2
  },
  "strategy_wise_listing": [
    {
      "distance": 11,
      "quantity": 5,
      "tat": 2592000,
      "pincode": 400603
    },
    {
      "distance": 11,
      "quantity": 5,
      "tat": 2592000,
      "pincode": 400603
    }
  ],
  "set": {
    "size_distribution": {
      "sizes": [
        {
          "size": "5",
          "pieces": 1
        },
        {
          "size": "7",
          "pieces": 1
        },
        {
          "size": "8",
          "pieces": 2
        },
        {
          "size": "9",
          "pieces": 1
        },
        {
          "size": "10",
          "pieces": 1
        }
      ]
    },
    "quantity": 6
  }
}
```
</details>









---


### getProductSellersBySlug
Get the sellers of a product size at a PIN Code




```kotlin
catalog.getProductSellersBySlug(slug: slug, size: size, pincode: pincode, strategy: strategy, pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of a product. You can get slug value from the endpoint /service/application/catalog/v1.0/products/ |   
| size | String | yes | A string indicating the size of the product, e.g. S, M, XL. You can get slug value from the endpoint /service/application/catalog/v1.0/products/sizes |   
| pincode | String | yes | The 6-digit PIN Code of the area near which the selling locations should be searched, e.g. 400059 |   
| strategy | String? | no | Sort stores on the basis of strategy. eg, fast-delivery, low-price, optimal. |   
| pageNo | Int? | no | The page number to navigate through the given set of results. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |  



A product of a particular size may be sold by multiple sellers. Use this API to fetch the sellers having the stock of a particular size at a given PIN Code.

*Returned Response:*




[ProductSizeSellersResponse](#ProductSizeSellersResponse)

Success. Returns a ProductSizeSeller object. Check the example shown below or refer `ProductSizeSellersResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "price_per_piece": {
        "effective": 66.5,
        "marked": 66.5,
        "currency_code": "INR",
        "currency_symbol": "₹"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency_code": "INR",
        "currency_symbol": "₹"
      },
      "quantity": 5,
      "pincode": 400603,
      "article_id": "1",
      "discount": "",
      "article_assignment": {
        "level": "single-company",
        "strategy": "optimal"
      },
      "seller": {
        "uid": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "uid": 1,
        "name": "Wayne Lamb"
      }
    },
    {
      "price_per_piece": {
        "effective": 66.5,
        "marked": 66.5,
        "currency_code": "INR",
        "currency_symbol": "₹"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency_code": "INR",
        "currency_symbol": "₹"
      },
      "quantity": 5,
      "pincode": 400603,
      "article_id": "2",
      "discount": "",
      "article_assignment": {
        "level": "single-company",
        "strategy": "optimal"
      },
      "seller": {
        "uid": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "uid": 1,
        "name": "Wayne Lamb"
      }
    }
  ],
  "page": {
    "current": 1,
    "total": 1,
    "has_previous": false,
    "has_next": false,
    "item_total": 2,
    "type": "number"
  },
  "sort_on": [
    {
      "default": true,
      "is_selected": true,
      "name": "Best price & fast delivery",
      "value": "optimal"
    },
    {
      "default": false,
      "is_selected": false,
      "name": "Best Price",
      "value": "low-price"
    },
    {
      "default": false,
      "is_selected": false,
      "name": "Fastest Delivery",
      "value": "fast-delivery"
    }
  ]
}
```
</details>









---


### getProductComparisonBySlugs
Compare products




```kotlin
catalog.getProductComparisonBySlugs(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | ArrayList<String> | yes | A short, human-readable, URL-friendly identifier of a product. You can get slug value from the endpoint /service/application/catalog/v1.0/products/. |  



Use this API to compare the features of products belonging to the same category. Note that at least one slug is mandatory in the request query.

*Returned Response:*




[ProductsComparisonResponse](#ProductsComparisonResponse)

Success. Returns an array of objects containing the attributes for comparision. Check the example shown below or refer `ProductsComparisonResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "attributes_metadata": [
    {
      "title": "Alexander Sawyer",
      "details": [
        {
          "key": "color",
          "display": "Kimberly Davidson",
          "description": ""
        },
        {
          "key": "gender",
          "display": "Kimberly Mcdaniel",
          "description": ""
        },
        {
          "key": "material",
          "display": "Monica Hampton",
          "description": ""
        },
        {
          "key": "weight",
          "display": "John Mendoza",
          "description": ""
        }
      ]
    }
  ],
  "items": [
    {
      "type": "product",
      "name": "benchmark collaborative paradigms",
      "item_type": "set",
      "slug": "benchmark-collaborative-paradigms",
      "id": 1,
      "brand": {
        "type": "brand",
        "name": "Barry, Jennings and Larson",
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
        "primary_color_hex": "808080"
      },
      "medias": [
        {
          "type": "image",
          "url": "http://cdn4.gofynd.com/media/pictures/tagged_items/original/1309_LGLAPTOPSLEEVE5/1_1564735832806.jpg"
        }
      ],
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
      "discount": "14% OFF",
      "price": {
        "marked": {
          "min": 1399,
          "max": 1399,
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
      "rating": 2.7,
      "rating_count": 2
    },
    {
      "type": "product",
      "name": "deploy viral systems",
      "item_type": "set",
      "slug": "deploy-viral-systems",
      "id": 2,
      "brand": {
        "type": "brand",
        "name": "Barry, Jennings and Larson",
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
            "slug": "deploy-viral-systems"
          }
        },
        "type": "page"
      },
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
        "primary_color_hex": "808080"
      },
      "medias": [
        {
          "type": "image",
          "url": "http://cdn4.gofynd.com/media/pictures/tagged_items/original/1309_LGLAPTOPSLEEVE5/1_1564735832806.jpg"
        }
      ],
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
      "discount": "14% OFF",
      "price": {
        "marked": {
          "min": 1399,
          "max": 1399,
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
      "rating": 2.7,
      "rating_count": 2
    }
  ]
}
```
</details>









---


### getSimilarComparisonProductBySlug
Get comparison between similar products




```kotlin
catalog.getSimilarComparisonProductBySlug(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of a product. You can get slug value from the endpoint /service/application/catalog/v1.0/products/ |  



Use this API to compare a given product automatically with similar products. Only one slug is needed.

*Returned Response:*




[ProductCompareResponse](#ProductCompareResponse)

Success. Returns an array of objects containing the attributes for comparision. Check the example shown below or refer `ProductCompareResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getComparedFrequentlyProductBySlug
Get comparison between frequently compared products with the given product




```kotlin
catalog.getComparedFrequentlyProductBySlug(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of a product. You can get slug value from the endpoint /service/application/catalog/v1.0/products/ |  



Use this API to compare a given product automatically with products that are frequently compared with it. Only one slug is needed.

*Returned Response:*




[ProductFrequentlyComparedSimilarResponse](#ProductFrequentlyComparedSimilarResponse)

Success. Returns an array of objects containing the attributes for comparision. Check the example shown below or refer `ProductFrequentlyComparedSimilarResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "similars": {
    "title": "Most Compared",
    "subtitle": "We bet you would love these!",
    "attributes_metadata": [
      {
        "title": "Alexander Sawyer",
        "details": [
          {
            "key": "color",
            "display": "Kimberly Davidson",
            "description": ""
          },
          {
            "key": "gender",
            "display": "Kimberly Mcdaniel",
            "description": ""
          },
          {
            "key": "material",
            "display": "Monica Hampton",
            "description": ""
          },
          {
            "key": "weight",
            "display": "John Mendoza",
            "description": ""
          }
        ]
      }
    ],
    "items": [
      {
        "type": "product",
        "name": "benchmark collaborative paradigms",
        "item_type": "set",
        "slug": "benchmark-collaborative-paradigms",
        "id": 1,
        "brand": {
          "type": "brand",
          "name": "Barry, Jennings and Larson",
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
          "primary_color_hex": "808080"
        },
        "medias": [
          {
            "type": "image",
            "url": "http://cdn4.gofynd.com/media/pictures/tagged_items/original/1309_LGLAPTOPSLEEVE5/1_1564735832806.jpg"
          }
        ],
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
        "discount": "14% OFF",
        "price": {
          "marked": {
            "min": 1399,
            "max": 1399,
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
        "rating": 2.7,
        "rating_count": 2
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
        "name": "deploy viral systems",
        "slug": "deploy-viral-systems",
        "uid": 2,
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
              "slug": "deploy-viral-systems"
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
        "rating": 2.7
      }
    ]
  }
}
```
</details>









---


### getProductSimilarByIdentifier
Get similar products




```kotlin
catalog.getProductSimilarByIdentifier(slug: slug, similarType: similarType).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of a product. You can get slug value from the endpoint /service/application/catalog/v1.0/products/ |   
| similarType | String | yes | Similarity criteria such as basic, visual, price, seller, category and spec. Visual - Products having similar patterns, Price - Products in similar price range, Seller - Products sold by the same seller, Category - Products belonging to the same category, e.g. sports shoes, Spec - Products having similar specifications, e.g. phones with same memory. |  



Use this API to retrieve products similar to the one specified by its slug. You can search not only similar looking products, but also those that are sold by same seller, or those that belong to the same category, price, specifications, etc.

*Returned Response:*




[SimilarProductByTypeResponse](#SimilarProductByTypeResponse)

Success. Returns a group of similar products based on type. Check the example shown below or refer `SimilarProductByTypeResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "similars": {
    "title": "Brand",
    "subtitle": "",
    "type": "brand",
    "items": [
      {
        "type": "product",
        "attributes": {
          "primary_color_hex": null,
          "features": "<li>Dura-pump Technology</li> <li>i-Pure Technology</li> <li>Powerful Air Throw</li> <li>Cool Flow Dispenser</li> <li>Engg. Plastic: Blower</li> <li>Blower/Fan Diameter (mm): 180</li> <li>Ice Chamber</li> <li>Cool Flow Dispenser</li> <li>Cooling Media: Honeycomb</li> <li>Air Throw Distance (mt): 9/30</li>",
          "model": "DiET 35T",
          "air-cooler-type": "Portable",
          "primary_color": ""
        },
        "categories": [
          {
            "id": 2717,
            "uid": 2717,
            "name": "Air Coolers",
            "logo": {
              "type": "image",
              "url": "https://hdn-1.fynd.com/media/banner_portrait/brand/original/540_ecba3a1af141467da8abc20500f983db.jpg"
            },
            "action": {
              "page": {
                "type": "products",
                "query": {
                  "category": [
                    "air-coolers"
                  ]
                }
              },
              "type": "page"
            },
            "_custom_json": {}
          }
        ],
        "sellable": true,
        "name": "Symphony Diet 35t Portable Air Cooler",
        "slug": "symphony-diet-35t-portable-air-cooler",
        "uid": 7502019,
        "item_type": "standard",
        "item_code": "491297014",
        "brand": {
          "type": "brand",
          "name": "Symphony",
          "logo": {
            "type": "image",
            "url": "https://hdn-1.jiox0.de/jiox0/brands/pictures/square-logo/original/69sKmY_CX-Logo.jpeg"
          },
          "action": {
            "page": {
              "type": "products",
              "query": {
                "brand": [
                  "symphony"
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
            "params": {
              "slug": [
                "symphony-diet-35t-portable-air-cooler"
              ]
            }
          },
          "type": "page"
        },
        "medias": [
          {
            "type": "image",
            "url": "https://hdn-1.jiox0.de/jiox0/products/pictures/item/free/original/63/491297014/0/5aKOS19APd-symphony-diet-35t-air-coolers-491297014-i-1-1200wx1200h.jpeg"
          },
          {
            "type": "image",
            "url": "https://hdn-1.jiox0.de/jiox0/products/pictures/item/free/original/63/491297014/1/NY6IJ7xfug-symphony-diet-35t-air-coolers-491297014-i-2-1200wx1200h.jpeg"
          }
        ],
        "discount": "",
        "price": {
          "marked": {
            "min": 9299,
            "max": 9299,
            "currency_code": "INR",
            "currency_symbol": "₹"
          },
          "effective": {
            "min": 9299,
            "max": 9299,
            "currency_code": "INR",
            "currency_symbol": "₹"
          }
        },
        "is_tryout": false,
        "_custom_json": {},
        "highlights": [
          "Powerful Air Throw ",
          "Large 35 Litre Tank Capacity ",
          "Automatic Louvers ",
          "Multi Directional Wheels ",
          "High Efficiency Honey Comb Pad"
        ],
        "description": "Exclusively suited for your cozy bedroom, Symphony DiET 35T Portable Air Cooler, assures you your comfort while it makes summers fun. Powered by a 35 litre tank, a high efficiency honeycomb pad and ice chamber, it is indeed your coolest buddy in summers. Automatic louvers, multi-directional wheels and three speed remote controlled setting options make it an ideal buy.",
        "country_of_origin": "India"
      }
    ]
  }
}
```
</details>









---


### getProductVariantsBySlug
Get variant of a particular product




```kotlin
catalog.getProductVariantsBySlug(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of a product. You can get slug value from the endpoint /service/application/catalog/v1.0/products/ |  



A product can have a different type of variants such as colour, shade, memory. Use this API to fetch all the available variants of a product using its slug.

*Returned Response:*




[ProductVariantsResponse](#ProductVariantsResponse)

Success. Returns all variants of a product. Check the example shown below or refer `ProductVariantsResponse` for more details. For `display_type:image`, `color` key will be present otherwise `value` key will be shown.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "variants": [
    {
      "header": "Addtn. Color",
      "key": "color",
      "display_type": "image",
      "logo": "https://d2zv4gzhlr4ud6.cloudfront.net/media/pictures/tagged_items/360x0/56_MKT02AI060CORAL/1_1567590349681.jpg",
      "items": [
        {
          "action": {
            "page": {
              "type": "product",
              "query": {
                "slug": "benchmark-collaborative-paradigms"
              }
            },
            "type": "page"
          },
          "uid": 1,
          "slug": "benchmark-collaborative-paradigms",
          "medias": [
            {
              "type": "image",
              "url": "http://cdn4.gofynd.com/media/pictures/tagged_items/original/1309_LGLAPTOPSLEEVE5/1_1564735832806.jpg"
            }
          ],
          "name": "benchmark collaborative paradigms",
          "is_available": true,
          "color_name": "DarkGrey",
          "color": "808080"
        }
      ]
    }
  ]
}
```
</details>









---


### getProductStockByIds
Get the stock of a product




```kotlin
catalog.getProductStockByIds(itemId: itemId, alu: alu, skuCode: skuCode, ean: ean, upc: upc).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| itemId | String? | no | The Item ID of the product (Max. 50 allowed) |   
| alu | String? | no | ALU of the product (limited upto 50 ALU identifier in a single request) |   
| skuCode | String? | no | Stock-keeping Unit of the product (limited upto 50 SKU Code in a single request) |   
| ean | String? | no | European Article Number of the product (limited upto 50 EAN identifier in a single request) |   
| upc | String? | no | Universal Product Code of the product (limited upto 50 UPC identifier in a single request) |  



Retrieve the available stock of the products. Use this API to retrieve stock of multiple products (up to 50) at a time.

*Returned Response:*




[ProductStockStatusResponse](#ProductStockStatusResponse)

Success. Returns the status of the product stock.Check the example shown below or refer `ProductStockStatusResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "uid": "1",
      "item_id": 1,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "2",
      "item_id": 1,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "3",
      "item_id": 2,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "4",
      "item_id": 2,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "5",
      "item_id": 3,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "6",
      "item_id": 3,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "7",
      "item_id": 4,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "8",
      "item_id": 4,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "9",
      "item_id": 5,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "10",
      "item_id": 5,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "11",
      "item_id": 6,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "12",
      "item_id": 6,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "13",
      "item_id": 7,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "14",
      "item_id": 7,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "15",
      "item_id": 8,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "16",
      "item_id": 8,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "17",
      "item_id": 9,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "18",
      "item_id": 9,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "19",
      "item_id": 10,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "20",
      "item_id": 10,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "21",
      "item_id": 11,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "22",
      "item_id": 11,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "23",
      "item_id": 12,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "24",
      "item_id": 12,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "25",
      "item_id": 13,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "26",
      "item_id": 13,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "27",
      "item_id": 14,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "28",
      "item_id": 14,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "29",
      "item_id": 15,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    },
    {
      "uid": "30",
      "item_id": 15,
      "identifier": {
        "sku_code": "P10101101154425S"
      },
      "price": {
        "effective": 399,
        "marked": 399,
        "currency": "INR"
      },
      "size": "13",
      "company": {
        "id": 1,
        "name": "Natalie Norman"
      },
      "store": {
        "id": 1,
        "name": "Wayne Lamb",
        "code": "Wayne-Lamb"
      },
      "quantity": 5
    }
  ]
}
```
</details>









---


### getProductStockForTimeByIds
Get the stock of a product




```kotlin
catalog.getProductStockForTimeByIds(timestamp: timestamp, pageSize: pageSize, pageId: pageId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| timestamp | String | yes | Timestamp in UTC format (2020-07-23T10:27:50Z) |   
| pageSize | Int? | no | The number of items to retrieve in each page. |   
| pageId | String? | no | Page ID to retrieve next set of results. |  



Retrieve the available stock of the products. Use this API to get the stock status of products whose inventory is updated at the specified time

*Returned Response:*




[ProductStockPolling](#ProductStockPolling)

Success. Returns the status of the product stock.Check the example shown below or refer `ProductStockPolling` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getProducts
Get all the products




```kotlin
catalog.getProducts(q: q, f: f, filters: filters, sortOn: sortOn, pageId: pageId, pageSize: pageSize, pageNo: pageNo, pageType: pageType).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| q | String? | no | The search query for entering partial or full name of product, brand, category, or collection. |   
| f | String? | no | The search filter parameters. Filter parameters will be passed in f parameter as shown in the example below. Double Pipe (||) denotes the OR condition, whereas Triple-colon (:::) indicates a new filter paramater applied as an AND condition. |   
| filters | Boolean? | no | This is a boolean value, True for fetching all filter parameters and False for disabling the filter parameters. |   
| sortOn | String? | no | The order in which the list of products should be sorted, e.g. popularity, price, latest and discount, in either ascending or descending order. See the supported values below. |   
| pageId | String? | no | Page ID to retrieve next set of results. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |   
| pageNo | Int? | no | The page number to navigate through the given set of results. |   
| pageType | String? | no | Available pagination types are cursor or number. |  



Use this API to list all the products. You may choose a sort order or make arbitrary search queries by entering the product name, brand, category or collection.

*Returned Response:*




[ProductListingResponse](#ProductListingResponse)

Success. Returns a paginated list of products..Check the example shown below or refer `ProductListingResponse` for more details.




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
        "kind": "singlevalued"
      },
      "values": [
        {
          "display": "Available",
          "count": 3,
          "is_selected": false,
          "value": "true"
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


### getBrands
Get all the brands




```kotlin
catalog.getBrands(department: department, pageNo: pageNo, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| department | String? | no | The name of the department. Use this parameter to filter products by a particular department. See the list of available departments below. Also, you can get available departments from the endpoint /service/application/catalog/v1.0/departments/ |   
| pageNo | Int? | no | The page number to navigate through the given set of results. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |  



A brand is the name under which a product is sold. Use this API to list all the brands. You can also filter the brands by department.

*Returned Response:*




[BrandListingResponse](#BrandListingResponse)

Success. Returns a paginated list of brands. Check the example shown below or refer `BrandListingResponse` for more details.




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


### getBrandDetailBySlug
Get metadata of a brand




```kotlin
catalog.getBrandDetailBySlug(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of a brand. You can get slug value from the endpoint /service/application/catalog/v1.0/brands/. |  



Fetch metadata of a brand such as name, information, logo, banner, etc.

*Returned Response:*




[BrandDetailResponse](#BrandDetailResponse)

Success. Returns a metadata object. Check the example shown below or refer `BrandDetailResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "logo": {
    "type": "image",
    "url": "https://hdn-1.fynd.com/media/logo/brand/original/12391_0d956c6c71a4427895c15e44cba82f88.jpg"
  },
  "banners": {
    "portrait": {
      "type": "image",
      "url": "https://hdn-1.fynd.com/media/banner_portrait/brand/original/12537_9cdfc6835e814b0986ee1643d38cf6cd.png"
    },
    "landscape": {
      "type": "image",
      "url": "https://hdn-1.fynd.com/media/banner/brand/original/12536_e1a5cdcefc7540e68cedd8c2b0673179.png"
    }
  },
  "uid": 1,
  "name": "Hess Inc"
}
```
</details>









---


### getCategories
List all the categories




```kotlin
catalog.getCategories(department: department).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| department | String? | no | The name of the department. Use this parameter to filter products by a particular department. See the list of available departments below. Also, you can get available departments from the endpoint /service/application/catalog/v1.0/departments/ |  



Use this API to list all the categories. You can also filter the categories by department.

*Returned Response:*




[CategoryListingResponse](#CategoryListingResponse)

Success. Returns a list of categories. Check the example shown below or refer `CategoryListingResponse` for more details.




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


### getCategoryDetailBySlug
Get metadata of a category




```kotlin
catalog.getCategoryDetailBySlug(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of a brand. You can get slug value from the endpoint /service/application/catalog/v1.0/brands/. |  



Fetch metadata of a category such as name, information, logo, banner, etc.

*Returned Response:*




[CategoryMetaResponse](#CategoryMetaResponse)

Success. Returns metadata of a category. Check the example shown below or refer `CategoryMetaResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "logo": {
    "type": "image",
    "url": "http://cdn4.gofynd.com/media/banner/category/original/12063_a5bb91bd5cb44c3c9db98c2a0e6b3d99.jpg"
  },
  "uid": 1,
  "name": "Kyle Cabrera",
  "banners": {
    "portrait": {
      "type": "image",
      "url": "http://cdn4.gofynd.com/media/banner_portrait/category/original/12064_e69e1d8b5e934d3488f0dc8663d8a158.jpg"
    },
    "landscape": {
      "type": "image",
      "url": "http://cdn4.gofynd.com/media/banner/category/original/12063_a5bb91bd5cb44c3c9db98c2a0e6b3d99.jpg"
    }
  },
  "_custom_json": {}
}
```
</details>









---


### getHomeProducts
List the products




```kotlin
catalog.getHomeProducts(sortOn: sortOn, pageId: pageId, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| sortOn | String? | no | The order in which the list of products should be sorted, e.g. popularity, price, latest and discount, in either ascending or descending order. |   
| pageId | String? | no | Page ID to retrieve next set of results. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |  



List all the products associated with a brand, collection or category in a random order.

*Returned Response:*




[HomeListingResponse](#HomeListingResponse)

Success. Returns a paginated list of products. Check the example shown below or refer `HomeListingResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
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
      "name": "whiteboard holistic functionalities",
      "slug": "whiteboard-holistic-functionalities",
      "uid": 7,
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
            "slug": "whiteboard-holistic-functionalities"
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
      "name": "envisioneer user-centric technologies",
      "slug": "envisioneer-user-centric-technologies",
      "uid": 6,
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
            "slug": "envisioneer-user-centric-technologies"
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
      "name": "deploy viral systems",
      "slug": "deploy-viral-systems",
      "uid": 2,
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
            "slug": "deploy-viral-systems"
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
      "name": "syndicate compelling e-commerce",
      "slug": "syndicate-compelling-e-commerce",
      "uid": 8,
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
            "slug": "syndicate-compelling-e-commerce"
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
      "name": "leverage granular e-commerce",
      "slug": "leverage-granular-e-commerce",
      "uid": 3,
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
            "slug": "leverage-granular-e-commerce"
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
      "name": "deliver bleeding-edge systems",
      "slug": "deliver-bleeding-edge-systems",
      "uid": 13,
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
            "slug": "deliver-bleeding-edge-systems"
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
      "name": "drive scalable applications",
      "slug": "drive-scalable-applications",
      "uid": 5,
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
            "slug": "drive-scalable-applications"
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
      "name": "cultivate web-enabled e-tailers",
      "slug": "cultivate-web-enabled-e-tailers",
      "uid": 4,
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
            "slug": "cultivate-web-enabled-e-tailers"
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
      "rating": 2.7
    }
  ],
  "page": {
    "next_id": "AoJftsmkNiEx",
    "has_previous": false,
    "has_next": true,
    "item_total": 15,
    "type": "number"
  },
  "sort_on": "random_36547cfbb4c54a1a992c17aa5 asc"
}
```
</details>









---


### getDepartments
List all the departments




```kotlin
catalog.getDepartments().safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```




Departments are a way to categorise similar products. A product can lie in multiple departments. For example, a skirt can below to the 'Women's Fashion' Department while a handbag can lie in 'Women's Accessories' Department. Use this API to list all the departments. If successful, returns the list of departments specified in `DepartmentResponse`

*Returned Response:*




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


### getSearchResults
Get relevant suggestions for a search query




```kotlin
catalog.getSearchResults(q: q).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| q | String | yes | The search query for entering partial or full name of a product, brand or category. For example, if the given search query `q` is _ski_, the relevant search suggestions could be _skirt_, _ski shoes_, __skin cream_ etc. |  



Retrieves a list of suggestions for a given search query. Each suggestion is a valid search term that's generated on the basis of query. This is particularly useful to enhance the user experience while using the search tool.

*Returned Response:*




[AutoCompleteResponse](#AutoCompleteResponse)

Success. Returns a list autocomplete suggestions for the search query `q`. Check the example shown below or refer `AutoCompleteResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json

```
</details>









---


### getCollections
List all the collections




```kotlin
catalog.getCollections(pageNo: pageNo, pageSize: pageSize, tag: tag).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| pageNo | Int? | no | The page number to navigate through the given set of results. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |   
| tag | ArrayList<String>? | no | List of tags  to filter collections |  



Collections are a great way to organize your products and can improve the ability for customers to find items quickly and efficiently.

*Returned Response:*




[GetCollectionListingResponse](#GetCollectionListingResponse)

Success. Returns a list of collections. Check the example shown below or refer `GetCollectionListingResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {
    "type": "number",
    "current": 1,
    "total": 1,
    "has_previous": false,
    "has_next": false,
    "item_total": 2
  },
  "items": [
    {
      "uid": "601a4f39448327cfa83e7db2",
      "type": "query",
      "query": {
        "category": [
          "Anna-Navarro"
        ]
      },
      "name": "collection with Anna-Navarro",
      "banners": {
        "portrait": {
          "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1571729908/production/applications/app_000000000000000000000001/media/collection/portrait/pewrpnjrhcrca1dmtvx5.png",
          "aspect_ratio": "13:20"
        },
        "landscape": {
          "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1571729858/production/applications/app_000000000000000000000001/media/collection/landscape/tkclmj847hdvfbudeqbr.png",
          "aspect_ratio": "27:20"
        }
      },
      "logo": {
        "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1571729838/production/applications/app_000000000000000000000001/media/collection/logo/xierjsrcwhd2fphzyjod.png",
        "aspect_ratio": "1:1"
      },
      "published": true,
      "description": "Crimsoune Club | Upto 70% Off",
      "is_active": true,
      "tags": [
        "men",
        "women"
      ],
      "slug": "crimsoune-club-upto-70-off-754fa043",
      "action": {
        "type": "collection",
        "url": "https://api.addsale.com/platform/content/v1/collections/crimsoune-club-upto-70-off-754fa043/items/"
      },
      "allow_facets": true,
      "allow_sort": true,
      "visible_facets_keys": [],
      "meta": {},
      "badge": {},
      "sort_on": "popular",
      "_custom_json": {},
      "_locale_language": {},
      "_schedule": {}
    },
    {
      "uid": "601a4f39448327cfa83e7db0",
      "type": "items",
      "query": {},
      "name": "collection with items",
      "banners": {
        "portrait": {
          "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1571729908/production/applications/app_000000000000000000000001/media/collection/portrait/pewrpnjrhcrca1dmtvx5.png",
          "aspect_ratio": "13:20"
        },
        "landscape": {
          "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1571729858/production/applications/app_000000000000000000000001/media/collection/landscape/tkclmj847hdvfbudeqbr.png",
          "aspect_ratio": "27:20"
        }
      },
      "logo": {
        "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1571729838/production/applications/app_000000000000000000000001/media/collection/logo/xierjsrcwhd2fphzyjod.png",
        "aspect_ratio": "1:1"
      },
      "published": true,
      "description": "Crimsoune Club | Upto 70% Off",
      "is_active": true,
      "tags": [
        "men",
        "women"
      ],
      "slug": "crimsoune-club-upto-70-off-754fa043",
      "action": {
        "type": "collection",
        "url": "https://api.addsale.com/platform/content/v1/collections/crimsoune-club-upto-70-off-754fa043/items/"
      },
      "allow_facets": true,
      "allow_sort": true,
      "visible_facets_keys": [],
      "meta": {},
      "badge": {},
      "sort_on": "popular",
      "_custom_json": {},
      "_locale_language": {},
      "_schedule": {}
    }
  ],
  "filters": {
    "tags": [
      {
        "name": "men",
        "is_selected": false,
        "display": "men"
      },
      {
        "name": "women",
        "is_selected": false,
        "display": "women"
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


### getCollectionItemsBySlug
Get the items in a collection




```kotlin
catalog.getCollectionItemsBySlug(slug: slug, f: f, filters: filters, sortOn: sortOn, pageId: pageId, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of a collection. You can get slug value from the endpoint /service/application/catalog/v1.0/collections/. |   
| f | String? | no | The search filter parameters. Filter parameters will be passed in f parameter as shown in the example below. Double Pipe (||) denotes the OR condition, whereas Triple-colon (:::) indicates a new filter paramater applied as an AND condition. |   
| filters | Boolean? | no | This is a boolean value, True for fetching all filter parameters and False for disabling the filter parameters. |   
| sortOn | String? | no | The order in which the list of products should be sorted, e.g. popularity, price, latest and discount, in either ascending or descending order. See the supported values below. |   
| pageId | String? | no | Page ID to retrieve next set of results. |   
| pageSize | Int? | no | The number of items to retrieve in each page. |  



Get items in a collection specified by its `slug`.

*Returned Response:*




[ProductListingResponse](#ProductListingResponse)

Success. Returns a list items in a given collection. Check the example shown below or refer `ProductListingResponse` for more details.




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
          "count": 1,
          "is_selected": false,
          "value": "Debra-Villarreal",
          "logo": {
            "type": "image",
            "url": "http://cdn4.gofynd.com/media/category_tab_icons/department/Men.png"
          }
        },
        {
          "display": "Tracey Miller",
          "count": 1,
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
          "count": 1,
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
          "count": 1,
          "is_selected": false,
          "value": "men"
        },
        {
          "display": "Women",
          "count": 1,
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
          "count": 1,
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
          "count": 1,
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
          "count": 1,
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
          "count": 1,
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
          "count": 1,
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
          "count": 1,
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
          "count": 1,
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
          "count": 1,
          "is_selected": false,
          "value": "808080"
        }
      ]
    },
    {
      "key": {
        "display": "Available",
        "name": "is_available",
        "kind": "singlevalued"
      },
      "values": [
        {
          "display": "Available",
          "count": 3,
          "is_selected": false,
          "value": "true"
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
      "rating": 2.7
    }
  ],
  "sort_on": [
    {
      "display": "Latest Products.",
      "name": "Latest Products.",
      "logo": "https://d2zv4gzhlr4ud6.cloudfront.net/media/pictures/tagged_items/360x0/56_MKT02AI060CORAL/1_1567590349681.jpg",
      "value": "latest",
      "is_selected": false
    }
  ],
  "page": {
    "type": "number",
    "current": 1,
    "total": 1,
    "has_previous": false,
    "has_next": false,
    "item_total": 1
  }
}
```
</details>









---


### getCollectionDetailBySlug
Get a particular collection




```kotlin
catalog.getCollectionDetailBySlug(slug: slug).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| slug | String | yes | A short, human-readable, URL-friendly identifier of a collection. You can get slug value from the endpoint /service/application/catalog/v1.0/collections/. |  



Get the details of a collection by its `slug`.

*Returned Response:*




[CollectionDetailResponse](#CollectionDetailResponse)

Success. Returns a Collection object. Check the example shown below or refer `CollectionDetailResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "uid": "601a4f39448327cfa83e7db0",
  "type": "items",
  "query": {},
  "name": "collection with items",
  "banners": {
    "portrait": {
      "type": "image",
      "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1571729908/production/applications/app_000000000000000000000001/media/collection/portrait/pewrpnjrhcrca1dmtvx5.png"
    },
    "landscape": {
      "type": "image",
      "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1571729858/production/applications/app_000000000000000000000001/media/collection/landscape/tkclmj847hdvfbudeqbr.png"
    }
  },
  "logo": {
    "type": "image",
    "url": "https://res.cloudinary.com/dwzm9bysq/image/upload/v1571729838/production/applications/app_000000000000000000000001/media/collection/logo/xierjsrcwhd2fphzyjod.png"
  },
  "published": true,
  "description": "Crimsoune Club | Upto 70% Off",
  "is_active": true,
  "tags": [
    "men",
    "women"
  ],
  "slug": "crimsoune-club-upto-70-off-754fa043",
  "action": {
    "page": {
      "type": "collection",
      "query": {
        "collection": [
          "crimsoune-club-upto-70-off-754fa043"
        ]
      }
    },
    "type": "page"
  },
  "allow_facets": true,
  "allow_sort": true,
  "visible_facets_keys": [],
  "meta": {},
  "badge": {},
  "sort_on": "popular",
  "_custom_json": {},
  "_locale_language": {},
  "_schedule": {}
}
```
</details>









---


### getFollowedListing
Get a list of followed Products, Brands, Collections




```kotlin
catalog.getFollowedListing(collectionType: collectionType, pageId: pageId, pageSize: pageSize).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| collectionType | String | yes | Type of collection followed, i.e. products, brands, or collections. |   
| pageId | String? | no | Page ID to retrieve next set of results. |   
| pageSize | Int? | no | Page ID to retrieve next set of results. |  



Users can follow a product they like. This API retrieves the products the user have followed.

*Returned Response:*




[GetFollowListingResponse](#GetFollowListingResponse)

Success. Returns a Followed resource object. Check the example shown below or refer `GetFollowListingResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "items": [
    {
      "type": "product",
      "name": "revolutionize end-to-end technologies",
      "item_type": "set",
      "slug": "revolutionize-end-to-end-technologies",
      "uid": 1,
      "brand": {
        "type": "brand",
        "name": "Chen PLC",
        "logo": {
          "type": "image",
          "url": "https://hdn-1.fynd.com/media/logo/brand/original/12391_0d956c6c71a4427895c15e44cba82f88.jpg"
        },
        "action": {
          "page": {
            "type": "products",
            "query": {
              "brand": [
                "Chen-PLC"
              ]
            }
          },
          "type": "page"
        },
        "_custom_json": {}
      },
      "sellable": false,
      "action": {
        "page": {
          "type": "product",
          "query": {
            "slug": "revolutionize-end-to-end-technologies"
          }
        },
        "type": "page"
      },
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
        "primary_color_hex": "808080"
      },
      "medias": [
        {
          "type": "image",
          "url": "http://cdn4.gofynd.com/media/pictures/tagged_items/original/1309_LGLAPTOPSLEEVE5/1_1564735832806.jpg"
        }
      ],
      "categories": [
        {
          "id": 3,
          "uid": 3,
          "name": "Paul Palmer",
          "logo": {
            "type": "image",
            "url": "https://hdn-1.fynd.com/media/banner_portrait/brand/original/540_ecba3a1af141467da8abc20500f983db.jpg"
          },
          "action": {
            "page": {
              "type": "category",
              "query": {
                "category": [
                  "Paul-Palmer"
                ]
              }
            },
            "type": "page"
          },
          "_custom_json": {}
        }
      ],
      "discount": "14% OFF",
      "price": {
        "marked": {
          "min": 1399,
          "max": 1399,
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
      "rating": 2.7,
      "rating_count": 2
    },
    {
      "type": "product",
      "name": "grow B2B experiences",
      "item_type": "set",
      "slug": "grow-B2B-experiences",
      "uid": 15,
      "brand": {
        "type": "brand",
        "name": "Chen PLC",
        "logo": {
          "type": "image",
          "url": "https://hdn-1.fynd.com/media/logo/brand/original/12391_0d956c6c71a4427895c15e44cba82f88.jpg"
        },
        "action": {
          "page": {
            "type": "products",
            "query": {
              "brand": [
                "Chen-PLC"
              ]
            }
          },
          "type": "page"
        },
        "_custom_json": {}
      },
      "sellable": false,
      "action": {
        "page": {
          "type": "product",
          "query": {
            "slug": "grow-B2B-experiences"
          }
        },
        "type": "page"
      },
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
        "primary_color_hex": "808080"
      },
      "medias": [
        {
          "type": "image",
          "url": "http://cdn4.gofynd.com/media/pictures/tagged_items/original/1309_LGLAPTOPSLEEVE5/1_1564735832806.jpg"
        }
      ],
      "categories": [
        {
          "id": 3,
          "uid": 3,
          "name": "Paul Palmer",
          "logo": {
            "type": "image",
            "url": "https://hdn-1.fynd.com/media/banner_portrait/brand/original/540_ecba3a1af141467da8abc20500f983db.jpg"
          },
          "action": {
            "page": {
              "type": "category",
              "query": {
                "category": [
                  "Paul-Palmer"
                ]
              }
            },
            "type": "page"
          },
          "_custom_json": {}
        }
      ],
      "discount": "14% OFF",
      "price": {
        "marked": {
          "min": 1399,
          "max": 1399,
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
      "rating": 2.7,
      "rating_count": 2
    },
    {
      "type": "product",
      "name": "target robust systems",
      "item_type": "set",
      "slug": "target-robust-systems",
      "uid": 14,
      "brand": {
        "type": "brand",
        "name": "Chen PLC",
        "logo": {
          "type": "image",
          "url": "https://hdn-1.fynd.com/media/logo/brand/original/12391_0d956c6c71a4427895c15e44cba82f88.jpg"
        },
        "action": {
          "page": {
            "type": "products",
            "query": {
              "brand": [
                "Chen-PLC"
              ]
            }
          },
          "type": "page"
        },
        "_custom_json": {}
      },
      "sellable": false,
      "action": {
        "page": {
          "type": "product",
          "query": {
            "slug": "target-robust-systems"
          }
        },
        "type": "page"
      },
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
        "primary_color_hex": "808080"
      },
      "medias": [
        {
          "type": "image",
          "url": "http://cdn4.gofynd.com/media/pictures/tagged_items/original/1309_LGLAPTOPSLEEVE5/1_1564735832806.jpg"
        }
      ],
      "categories": [
        {
          "id": 3,
          "uid": 3,
          "name": "Paul Palmer",
          "logo": {
            "type": "image",
            "url": "https://hdn-1.fynd.com/media/banner_portrait/brand/original/540_ecba3a1af141467da8abc20500f983db.jpg"
          },
          "action": {
            "page": {
              "type": "category",
              "query": {
                "category": [
                  "Paul-Palmer"
                ]
              }
            },
            "type": "page"
          },
          "_custom_json": {}
        }
      ],
      "discount": "14% OFF",
      "price": {
        "marked": {
          "min": 1399,
          "max": 1399,
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
      "rating": 2.7,
      "rating_count": 2
    }
  ],
  "page": {
    "next_id": "6066fc7b3b17fd7038c46317",
    "has_previous": false,
    "has_next": true,
    "item_total": 15,
    "type": "number"
  }
}
```
</details>









---


### unfollowById
Unfollow an entity (product/brand/collection)




```kotlin
catalog.unfollowById(collectionType: collectionType, collectionId: collectionId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| collectionType | String | yes | Type of collection followed, i.e. products, brands, or collections. |   
| collectionId | String | yes | The ID of the collection type. |  



You can undo a followed product, brand or collection by its ID. This action is referred as _unfollow_.

*Returned Response:*




[FollowPostResponse](#FollowPostResponse)

Success. Returns a response object. Check the example shown below or refer `FollowPostResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "message": "Products Removed From Wishlist",
  "id": "1"
}
```
</details>









---


### followById
Follow an entity (product/brand/collection)




```kotlin
catalog.followById(collectionType: collectionType, collectionId: collectionId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| collectionType | String | yes | Type of collection followed, i.e. products, brands, or collections. |   
| collectionId | String | yes | The ID of the collection type. |  



Follow a particular entity such as product, brand, collection specified by its ID.

*Returned Response:*




[FollowPostResponse](#FollowPostResponse)

Success. Returns a response object. Check the example shown below or refer `FollowPostResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "message": "Brands Added To Wishlist",
  "id": "1"
}
```
</details>









---


### getFollowerCountById
Get Follow Count




```kotlin
catalog.getFollowerCountById(collectionType: collectionType, collectionId: collectionId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| collectionType | String | yes | Type of collection, i.e. products, brands, or collections. |   
| collectionId | String | yes | The ID of the collection type. |  



Get the total count of followers for a given collection type and collection ID.

*Returned Response:*




[FollowerCountResponse](#FollowerCountResponse)

Success. Returns the number of followers for a given collection type. Check the example shown below or refer `FollowerCountResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "count": 0
}
```
</details>









---


### getFollowIds
Get the IDs of followed products, brands and collections.




```kotlin
catalog.getFollowIds(collectionType: collectionType).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| collectionType | String? | no | Type of collection, i.e. products, brands, collections. |  



You can get the IDs of all the followed Products, Brands and Collections. Pass collection_type as query parameter to fetch specific Ids

*Returned Response:*




[FollowIdsResponse](#FollowIdsResponse)

Success. Returns the IDs of all the Products, Brands and Collections which were followed. Check the example shown below or refer `FollowIdsResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "data": {
    "products": [
      1,
      15,
      14,
      13,
      12,
      11,
      10,
      9,
      8,
      7,
      6,
      5,
      4,
      3,
      2
    ],
    "brands": [
      1
    ],
    "collections": []
  }
}
```
</details>









---


### getStores
Get store meta information.




```kotlin
catalog.getStores(pageNo: pageNo, pageSize: pageSize, q: q, city: city, range: range, latitude: latitude, longitude: longitude).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| pageNo | Int? | no | The page number to navigate through the given set of results. |   
| pageSize | Int? | no | Number of items to retrieve in each page. |   
| q | String? | no | Search a store by its name or store_code. |   
| city | String? | no | Search stores by the city in which they are situated. |   
| range | Int? | no | Use this to retrieve stores within a particular range in meters, e.g. 10000, to indicate a 10km range |   
| latitude | Double? | no | Latitude of the location from where one wants to retreive the nearest stores, e.g. 72.8691788 |   
| longitude | Double? | no | Longitude of the location from where one wants to retreive the nearest stores, e.g. 19.1174114 |  



Use this API to get a list of stores in a specific application.

*Returned Response:*




[StoreListingResponse](#StoreListingResponse)

Success. Returns a list of selling locations. Check the example shown below or refer `StoreListingResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {
    "type": "number",
    "current": 1,
    "total": 1,
    "has_previous": false,
    "has_next": false,
    "item_total": 1
  },
  "data": [
    {
      "pincode": 400059,
      "city": "MUMBAI",
      "state": "MAHARASHTRA",
      "country": "INDIA",
      "address": "SHOPSENSE RETAIL TECHNOLOGIES PRIVATE LIMITED 1ST FLOOR WEWORK VIJAY DIAMOND, CROSS RD B, AJIT NAGAR,",
      "store_email": "ASHISHCHANDORKAR@FYND.COM",
      "lat_long": {
        "type": "Point",
        "coordinates": [
          72.8691788,
          19.1174114
        ]
      },
      "name": "RRL01",
      "store_code": "WH_8513",
      "uid": 1
    }
  ]
}
```
</details>









---


### getInStockLocations
Get store meta information.




```kotlin
catalog.getInStockLocations(pageNo: pageNo, pageSize: pageSize, q: q, city: city, range: range, latitude: latitude, longitude: longitude).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| pageNo | Int? | no | The page number to navigate through the given set of results. |   
| pageSize | Int? | no | Number of items to retrieve in each page. |   
| q | String? | no | Search a store by its name or store_code. |   
| city | String? | no | Search stores by the city in which they are situated. |   
| range | Int? | no | Use this to retrieve stores within a particular range in meters, e.g. 10000, to indicate a 10km range |   
| latitude | Double? | no | Latitude of the location from where one wants to retreive the nearest stores, e.g. 72.8691788 |   
| longitude | Double? | no | Longitude of the location from where one wants to retreive the nearest stores, e.g. 19.1174114 |  



Use this API to get a list of stores in a specific application.

*Returned Response:*




[ApplicationStoreListing](#ApplicationStoreListing)

Success. Returns a list of selling locations. Check the example shown below or refer `StoreListingResponse` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "page": {
    "current": 1,
    "type": "number",
    "total": 1,
    "has_previous": false,
    "has_next": false,
    "item_total": 5
  },
  "items": [
    {
      "uid": 1,
      "_custom_json": {},
      "additional_contacts": [
        {
          "country_code": 91,
          "number": "9594495254"
        }
      ],
      "address": {
        "lat_long": {
          "type": "Point",
          "coordinates": [
            72.809786,
            19.138787
          ]
        },
        "city": "MUMBAI",
        "pincode": 400061,
        "state": "MAHARASHTRA",
        "country": "INDIA",
        "landmark": "",
        "address2": "",
        "address1": "YARI ROAD, ANDHERI WEST"
      },
      "company_id": 1,
      "display_name": "Reliance Digital P. Ltd",
      "manager": {
        "mobile_no": {
          "country_code": 91,
          "number": "9594495254"
        },
        "name": "Fahim Sakri",
        "email": "fahimsakri@gmail.com"
      },
      "name": "Reliance Digital P. Ltd",
      "store_code": "HS-52b69",
      "store_type": "high_street",
      "company": {
        "company_type": "mbo",
        "business_type": "ltd/pvt ltd",
        "name": "Reliance Digital P. Ltd1234789123",
        "uid": 1
      },
      "departments": [
        {
          "priority_order": 7,
          "name": "Baby Care & Kids Essentials",
          "uid": 7,
          "logo": {
            "type": "image",
            "url": "https://hdn-1.fynd.com/media/category_tab_icons/department/Babycareandkidsessential.png"
          },
          "is_active": true,
          "slug": "baby-care-kids-essentials"
        },
        {
          "priority_order": 9,
          "name": "Industrial Supplies",
          "uid": 11,
          "logo": {
            "type": "image",
            "url": "https://hdn-1.fynd.com/media/logo/department/original/15483_a8803bf3fc244c748180588166df82da.jpg"
          },
          "is_active": true,
          "slug": "industrial-supplies"
        },
        {
          "priority_order": 10,
          "name": "Electricals",
          "uid": 14,
          "logo": {
            "type": "image",
            "url": "https://hdn-1.fynd.com/department/pictures/square-logo/original/M93qfyuh1-https:hdn-1.fynd.commedialogodepartmentoriginal17588_44516b7413fd4a4a858556857aa0c4c8.jpg.jpeg"
          },
          "is_active": true,
          "slug": "electricals"
        },
        {
          "priority_order": 1,
          "name": "Fashion",
          "uid": 21,
          "logo": {
            "type": "image",
            "url": "https://hdn-1.fynd.com/department/pictures/square-logo/original/jSt0jjI7D-https/hdn-1.fynd.com/department/pictures/square-logo/original/6ouiCBSSn-https/hdn-1.fynd.com/department/pictures/square-logo/original/o2Rti5if7-.jpeg.jpeg.jpeg"
          },
          "is_active": true,
          "slug": "fashion"
        },
        {
          "slug": "automobile",
          "is_active": true,
          "logo": {
            "type": "image",
            "url": "https://hdn-1.addsale.com/x0/department/pictures/square-logo/original/kRhYFHWZ5-.jpeg"
          },
          "name": "AUTOMOBILE",
          "uid": 24,
          "priority_order": 1
        }
      ]
    }
  ]
}
```
</details>









---


### getLocationDetailsById
Get store meta information.




```kotlin
catalog.getLocationDetailsById(locationId: locationId).safeAwait{ response,error->
    
    response?.let{
      // Use response
    } ->
     
    error?.let{
      
    } 
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| locationId | Int | yes | Unique Location ID. |  



Use this API to get meta details for a store.

*Returned Response:*




[StoreDetails](#StoreDetails)

Success. Returns a metadata object. Check the example shown below or refer `StoreDetails` for more details.




<details>
<summary><i>&nbsp; Example:</i></summary>

```json
{
  "uid": 1,
  "_custom_json": {},
  "additional_contacts": [
    {
      "country_code": 91,
      "number": "9594495254"
    }
  ],
  "address": {
    "lat_long": {
      "type": "Point",
      "coordinates": [
        72.809786,
        19.138787
      ]
    },
    "city": "MUMBAI",
    "pincode": 400061,
    "state": "MAHARASHTRA",
    "country": "INDIA",
    "landmark": "",
    "address2": "",
    "address1": "YARI ROAD, ANDHERI WEST"
  },
  "company_id": 1,
  "display_name": "Reliance Digital P. Ltd",
  "manager": {
    "mobile_no": {
      "country_code": 91,
      "number": "9594495254"
    },
    "name": "Fahim Sakri",
    "email": "fahimsakri@gmail.com"
  },
  "name": "Reliance Digital P. Ltd",
  "store_code": "HS-52b69",
  "store_type": "high_street",
  "timing": [
    {
      "weekday": "monday",
      "open": true,
      "closing": {
        "minute": 30,
        "hour": 21
      },
      "opening": {
        "minute": 0,
        "hour": 11
      }
    },
    {
      "weekday": "tuesday",
      "open": true,
      "closing": {
        "minute": 30,
        "hour": 21
      },
      "opening": {
        "minute": 0,
        "hour": 11
      }
    },
    {
      "weekday": "wednesday",
      "open": true,
      "closing": {
        "minute": 30,
        "hour": 21
      },
      "opening": {
        "minute": 0,
        "hour": 11
      }
    },
    {
      "weekday": "thursday",
      "open": true,
      "closing": {
        "minute": 30,
        "hour": 21
      },
      "opening": {
        "minute": 0,
        "hour": 11
      }
    },
    {
      "weekday": "friday",
      "open": true,
      "closing": {
        "minute": 30,
        "hour": 21
      },
      "opening": {
        "minute": 0,
        "hour": 11
      }
    },
    {
      "weekday": "saturday",
      "open": true,
      "closing": {
        "minute": 30,
        "hour": 21
      },
      "opening": {
        "minute": 0,
        "hour": 11
      }
    },
    {
      "weekday": "sunday",
      "open": true,
      "closing": {
        "minute": 30,
        "hour": 21
      },
      "opening": {
        "minute": 0,
        "hour": 11
      }
    }
  ],
  "company": {
    "company_type": "mbo",
    "business_type": "ltd/pvt ltd",
    "name": "Reliance Digital P. Ltd1234789123",
    "uid": 1
  }
}
```
</details>









---



### Schemas

 
 
 #### [Meta](#Meta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | source | String? |  yes  |  |

---


 
 
 #### [Media](#Media)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | meta | [Meta](#Meta)? |  yes  |  |
 | type | String? |  yes  |  |
 | url | String? |  yes  |  |

---


 
 
 #### [ProductListingActionPage](#ProductListingActionPage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | query | HashMap<String,Any>? |  yes  |  |
 | params | HashMap<String,Any>? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [ProductListingAction](#ProductListingAction)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [ProductListingActionPage](#ProductListingActionPage)? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [ProductBrand](#ProductBrand)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | logo | [Media](#Media)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |

---


 
 
 #### [Price](#Price)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | min | Double? |  yes  |  |
 | max | Double? |  yes  |  |
 | currencySymbol | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |

---


 
 
 #### [ProductListingPrice](#ProductListingPrice)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | marked | [Price](#Price)? |  yes  |  |
 | effective | [Price](#Price)? |  yes  |  |

---


 
 
 #### [ProductDetailAttribute](#ProductDetailAttribute)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | String? |  yes  |  |
 | type | String? |  yes  |  |
 | key | String? |  yes  |  |

---


 
 
 #### [ProductDetailGroupedAttribute](#ProductDetailGroupedAttribute)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | details | ArrayList<[ProductDetailAttribute](#ProductDetailAttribute)>? |  yes  |  |

---


 
 
 #### [ProductDetail](#ProductDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | similars | ArrayList<String>? |  yes  |  |
 | shortDescription | String? |  yes  |  |
 | tryouts | ArrayList<String>? |  yes  |  |
 | highlights | ArrayList<String>? |  yes  |  |
 | teaserTag | String? |  yes  |  |
 | attributes | HashMap<String,Any>? |  yes  |  |
 | categories | ArrayList<[ProductBrand](#ProductBrand)>? |  yes  |  |
 | discount | String? |  yes  |  |
 | name | String? |  yes  |  |
 | medias | ArrayList<[Media](#Media)>? |  yes  |  |
 | hasVariant | Boolean? |  yes  |  |
 | uid | Int? |  yes  |  |
 | productOnlineDate | String? |  yes  |  |
 | description | String? |  yes  |  |
 | rating | Double? |  yes  |  |
 | brand | [ProductBrand](#ProductBrand)? |  yes  |  |
 | slug | String |  no  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | price | [ProductListingPrice](#ProductListingPrice)? |  yes  |  |
 | ratingCount | Int? |  yes  |  |
 | color | String? |  yes  |  |
 | groupedAttributes | ArrayList<[ProductDetailGroupedAttribute](#ProductDetailGroupedAttribute)>? |  yes  |  |
 | itemType | String? |  yes  |  |
 | imageNature | String? |  yes  |  |
 | itemCode | String? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [ErrorResponse](#ErrorResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | error | String? |  yes  |  |

---


 
 
 #### [SizeChartValues](#SizeChartValues)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | col4 | String? |  yes  |  |
 | col5 | String? |  yes  |  |
 | col2 | String? |  yes  |  |
 | col1 | String? |  yes  |  |
 | col3 | String? |  yes  |  |
 | col6 | String? |  yes  |  |

---


 
 
 #### [ColumnHeader](#ColumnHeader)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | String? |  yes  |  |
 | convertable | Boolean? |  yes  |  |

---


 
 
 #### [ColumnHeaders](#ColumnHeaders)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | col4 | [ColumnHeader](#ColumnHeader)? |  yes  |  |
 | col5 | [ColumnHeader](#ColumnHeader)? |  yes  |  |
 | col2 | [ColumnHeader](#ColumnHeader)? |  yes  |  |
 | col1 | [ColumnHeader](#ColumnHeader)? |  yes  |  |
 | col3 | [ColumnHeader](#ColumnHeader)? |  yes  |  |
 | col6 | [ColumnHeader](#ColumnHeader)? |  yes  |  |

---


 
 
 #### [SizeChart](#SizeChart)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | unit | String? |  yes  |  |
 | description | String? |  yes  |  |
 | title | String? |  yes  |  |
 | image | String? |  yes  |  |
 | sizes | ArrayList<[SizeChartValues](#SizeChartValues)>? |  yes  |  |
 | sizeTip | String? |  yes  |  |
 | headers | [ColumnHeaders](#ColumnHeaders)? |  yes  |  |

---


 
 
 #### [ProductSize](#ProductSize)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | String? |  yes  |  |
 | display | String? |  yes  |  |
 | quantity | Int? |  yes  |  |
 | isAvailable | Boolean? |  yes  |  |

---


 
 
 #### [ProductSizeStores](#ProductSizeStores)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | count | Int? |  yes  |  |

---


 
 
 #### [ProductSizes](#ProductSizes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sizeChart | [SizeChart](#SizeChart)? |  yes  |  |
 | sizes | ArrayList<[ProductSize](#ProductSize)>? |  yes  |  |
 | price | [ProductListingPrice](#ProductListingPrice)? |  yes  |  |
 | sellable | Boolean? |  yes  |  |
 | discount | String? |  yes  |  |
 | stores | [ProductSizeStores](#ProductSizeStores)? |  yes  |  |

---


 
 
 #### [Seller](#Seller)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | count | Int? |  yes  |  |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [StrategyWiseListing](#StrategyWiseListing)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | pincode | Int? |  yes  |  |
 | tat | Int? |  yes  |  |
 | quantity | Int? |  yes  |  |
 | distance | Int? |  yes  |  |

---


 
 
 #### [Store](#Store)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | count | Int? |  yes  |  |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [ProductStockPrice](#ProductStockPrice)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | currency | String? |  yes  |  |
 | marked | Double? |  yes  |  |
 | effective | Double? |  yes  |  |

---


 
 
 #### [ReturnConfig](#ReturnConfig)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | unit | String? |  yes  |  |
 | returnable | Boolean? |  yes  |  |
 | time | Int? |  yes  |  |

---


 
 
 #### [ArticleAssignment](#ArticleAssignment)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | strategy | String? |  yes  |  |
 | level | String? |  yes  |  |

---


 
 
 #### [ProductSetDistributionSize](#ProductSetDistributionSize)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | size | String? |  yes  |  |
 | pieces | Int? |  yes  |  |

---


 
 
 #### [ProductSetDistribution](#ProductSetDistribution)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sizes | ArrayList<[ProductSetDistributionSize](#ProductSetDistributionSize)>? |  yes  |  |

---


 
 
 #### [ProductSet](#ProductSet)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sizeDistribution | [ProductSetDistribution](#ProductSetDistribution)? |  yes  |  |
 | quantity | Int? |  yes  |  |

---


 
 
 #### [Details](#Details)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | String? |  yes  |  |
 | type | String? |  yes  |  |
 | key | String? |  yes  |  |

---


 
 
 #### [MarketPlaceSttributes](#MarketPlaceSttributes)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | details | ArrayList<[Details](#Details)>? |  yes  |  |

---


 
 
 #### [ProductSizePriceResponse](#ProductSizePriceResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | seller | [Seller](#Seller)? |  yes  |  |
 | specialBadge | String? |  yes  |  |
 | strategyWiseListing | ArrayList<[StrategyWiseListing](#StrategyWiseListing)>? |  yes  |  |
 | sellerCount | Int? |  yes  |  |
 | itemType | String? |  yes  |  |
 | store | [Store](#Store)? |  yes  |  |
 | pricePerPiece | [ProductStockPrice](#ProductStockPrice)? |  yes  |  |
 | articleId | String? |  yes  |  |
 | discount | String? |  yes  |  |
 | returnConfig | [ReturnConfig](#ReturnConfig)? |  yes  |  |
 | articleAssignment | [ArticleAssignment](#ArticleAssignment)? |  yes  |  |
 | price | [ProductStockPrice](#ProductStockPrice)? |  yes  |  |
 | pincode | Int? |  yes  |  |
 | longLat | ArrayList<Double>? |  yes  |  |
 | quantity | Int? |  yes  |  |
 | set | [ProductSet](#ProductSet)? |  yes  |  |
 | marketplaceAttributes | ArrayList<[MarketPlaceSttributes](#MarketPlaceSttributes)>? |  yes  |  |

---


 
 
 #### [Page](#Page)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | hasPrevious | Boolean? |  yes  |  |
 | hasNext | Boolean? |  yes  |  |
 | nextId | String? |  yes  |  |
 | current | Int? |  yes  |  |
 | type | String |  no  |  |
 | size | Int? |  yes  |  |
 | itemTotal | Int? |  yes  |  |

---


 
 
 #### [ProductSizeSellerFilter](#ProductSizeSellerFilter)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | String? |  yes  |  |
 | name | String? |  yes  |  |
 | isSelected | Boolean? |  yes  |  |

---


 
 
 #### [ProductSizeSellersResponse](#ProductSizeSellersResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page) |  no  |  |
 | sortOn | ArrayList<[ProductSizeSellerFilter](#ProductSizeSellerFilter)>? |  yes  |  |
 | items | ArrayList<[ProductSizePriceResponse](#ProductSizePriceResponse)>? |  yes  |  |

---


 
 
 #### [AttributeDetail](#AttributeDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | logo | String? |  yes  |  |
 | description | String? |  yes  |  |
 | display | String? |  yes  |  |
 | key | String? |  yes  |  |

---


 
 
 #### [AttributeMetadata](#AttributeMetadata)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | details | ArrayList<[AttributeDetail](#AttributeDetail)>? |  yes  |  |

---


 
 
 #### [ProductsComparisonResponse](#ProductsComparisonResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[ProductDetail](#ProductDetail)>? |  yes  |  |
 | attributesMetadata | ArrayList<[AttributeMetadata](#AttributeMetadata)>? |  yes  |  |

---


 
 
 #### [ProductCompareResponse](#ProductCompareResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | subtitle | String? |  yes  |  |
 | items | ArrayList<[ProductDetail](#ProductDetail)>? |  yes  |  |
 | attributesMetadata | ArrayList<[AttributeMetadata](#AttributeMetadata)>? |  yes  |  |

---


 
 
 #### [ProductFrequentlyComparedSimilarResponse](#ProductFrequentlyComparedSimilarResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | similars | [ProductCompareResponse](#ProductCompareResponse)? |  yes  |  |

---


 
 
 #### [ProductSimilarItem](#ProductSimilarItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String? |  yes  |  |
 | subtitle | String? |  yes  |  |
 | items | ArrayList<[ProductDetail](#ProductDetail)>? |  yes  |  |

---


 
 
 #### [SimilarProductByTypeResponse](#SimilarProductByTypeResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | similars | [ProductSimilarItem](#ProductSimilarItem)? |  yes  |  |

---


 
 
 #### [ProductVariantItemResponse](#ProductVariantItemResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | medias | ArrayList<[Media](#Media)>? |  yes  |  |
 | uid | Int? |  yes  |  |
 | color | String? |  yes  |  |
 | isAvailable | Boolean? |  yes  |  |
 | slug | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | value | String? |  yes  |  |
 | colorName | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [ProductVariantResponse](#ProductVariantResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | displayType | String? |  yes  |  |
 | items | ArrayList<[ProductVariantItemResponse](#ProductVariantItemResponse)>? |  yes  |  |
 | key | String? |  yes  |  |
 | header | String? |  yes  |  |

---


 
 
 #### [ProductVariantsResponse](#ProductVariantsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | variants | ArrayList<[ProductVariantResponse](#ProductVariantResponse)>? |  yes  |  |

---


 
 
 #### [StoreDetail](#StoreDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | code | String? |  yes  |  |
 | name | String? |  yes  |  |
 | city | String? |  yes  |  |
 | id | Int? |  yes  |  |

---


 
 
 #### [CompanyDetail](#CompanyDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | id | Int? |  yes  |  |

---


 
 
 #### [ProductStockStatusItem](#ProductStockStatusItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | itemId | Int? |  yes  |  |
 | seller | [Seller](#Seller)? |  yes  |  |
 | uid | String? |  yes  |  |
 | store | [StoreDetail](#StoreDetail)? |  yes  |  |
 | company | [CompanyDetail](#CompanyDetail)? |  yes  |  |
 | identifier | HashMap<String,Any>? |  yes  |  |
 | price | [ProductStockPrice](#ProductStockPrice)? |  yes  |  |
 | size | String? |  yes  |  |
 | quantity | Int? |  yes  |  |

---


 
 
 #### [ProductStockStatusResponse](#ProductStockStatusResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[ProductStockStatusItem](#ProductStockStatusItem)>? |  yes  |  |

---


 
 
 #### [ProductStockPolling](#ProductStockPolling)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page) |  no  |  |
 | items | ArrayList<[ProductStockStatusItem](#ProductStockStatusItem)>? |  yes  |  |

---


 
 
 #### [ProductListingDetail](#ProductListingDetail)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | similars | ArrayList<String>? |  yes  |  |
 | shortDescription | String? |  yes  |  |
 | tryouts | ArrayList<String>? |  yes  |  |
 | highlights | ArrayList<String>? |  yes  |  |
 | teaserTag | String? |  yes  |  |
 | attributes | HashMap<String,Any>? |  yes  |  |
 | categories | ArrayList<[ProductBrand](#ProductBrand)>? |  yes  |  |
 | discount | String? |  yes  |  |
 | name | String? |  yes  |  |
 | medias | ArrayList<[Media](#Media)>? |  yes  |  |
 | hasVariant | Boolean? |  yes  |  |
 | uid | Int? |  yes  |  |
 | productOnlineDate | String? |  yes  |  |
 | description | String? |  yes  |  |
 | rating | Double? |  yes  |  |
 | brand | [ProductBrand](#ProductBrand)? |  yes  |  |
 | slug | String |  no  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | price | [ProductListingPrice](#ProductListingPrice)? |  yes  |  |
 | ratingCount | Int? |  yes  |  |
 | color | String? |  yes  |  |
 | groupedAttributes | ArrayList<[ProductDetailGroupedAttribute](#ProductDetailGroupedAttribute)>? |  yes  |  |
 | itemType | String? |  yes  |  |
 | imageNature | String? |  yes  |  |
 | itemCode | String? |  yes  |  |
 | type | String? |  yes  |  |
 | sellable | Boolean? |  yes  |  |

---


 
 
 #### [ProductSortOn](#ProductSortOn)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | value | String? |  yes  |  |
 | name | String? |  yes  |  |
 | isSelected | Boolean? |  yes  |  |

---


 
 
 #### [ProductFiltersValue](#ProductFiltersValue)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | queryFormat | String? |  yes  |  |
 | selectedMin | Int? |  yes  |  |
 | selectedMax | Int? |  yes  |  |
 | isSelected | Boolean |  no  |  |
 | displayFormat | String? |  yes  |  |
 | display | String |  no  |  |
 | min | Int? |  yes  |  |
 | currencySymbol | String? |  yes  |  |
 | currencyCode | String? |  yes  |  |
 | count | Int? |  yes  |  |
 | value | String? |  yes  |  |
 | max | Int? |  yes  |  |

---


 
 
 #### [ProductFiltersKey](#ProductFiltersKey)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | logo | String? |  yes  |  |
 | display | String |  no  |  |
 | kind | String? |  yes  |  |
 | name | String |  no  |  |

---


 
 
 #### [ProductFilters](#ProductFilters)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | values | ArrayList<[ProductFiltersValue](#ProductFiltersValue)> |  no  |  |
 | key | [ProductFiltersKey](#ProductFiltersKey) |  no  |  |

---


 
 
 #### [ProductListingResponse](#ProductListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page) |  no  |  |
 | items | ArrayList<[ProductListingDetail](#ProductListingDetail)>? |  yes  |  |
 | sortOn | ArrayList<[ProductSortOn](#ProductSortOn)>? |  yes  |  |
 | filters | ArrayList<[ProductFilters](#ProductFilters)>? |  yes  |  |

---


 
 
 #### [ImageUrls](#ImageUrls)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | landscape | [Media](#Media)? |  yes  |  |
 | portrait | [Media](#Media)? |  yes  |  |

---


 
 
 #### [BrandItem](#BrandItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | departments | ArrayList<String>? |  yes  |  |
 | uid | Int? |  yes  |  |
 | logo | [Media](#Media)? |  yes  |  |
 | slug | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | discount | String? |  yes  |  |
 | name | String? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |

---


 
 
 #### [BrandListingResponse](#BrandListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page) |  no  |  |
 | items | ArrayList<[BrandItem](#BrandItem)>? |  yes  |  |

---


 
 
 #### [BrandDetailResponse](#BrandDetailResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | logo | [Media](#Media)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |

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
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | childs | ArrayList<HashMap<String,Any>>? |  yes  |  |
 | slug | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |

---


 
 
 #### [SecondLevelChild](#SecondLevelChild)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | childs | ArrayList<[ThirdLevelChild](#ThirdLevelChild)>? |  yes  |  |
 | slug | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |

---


 
 
 #### [Child](#Child)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | childs | ArrayList<[SecondLevelChild](#SecondLevelChild)>? |  yes  |  |
 | slug | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |

---


 
 
 #### [CategoryItems](#CategoryItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | childs | ArrayList<[Child](#Child)>? |  yes  |  |
 | slug | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | name | String? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |

---


 
 
 #### [DepartmentCategoryTree](#DepartmentCategoryTree)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[CategoryItems](#CategoryItems)>? |  yes  |  |
 | department | String? |  yes  |  |

---


 
 
 #### [CategoryListingResponse](#CategoryListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | departments | ArrayList<[DepartmentIdentifier](#DepartmentIdentifier)>? |  yes  |  |
 | data | ArrayList<[DepartmentCategoryTree](#DepartmentCategoryTree)>? |  yes  |  |

---


 
 
 #### [CategoryMetaResponse](#CategoryMetaResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | logo | [Media](#Media)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |

---


 
 
 #### [HomeListingResponse](#HomeListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |
 | page | [Page](#Page) |  no  |  |
 | items | ArrayList<[ProductListingDetail](#ProductListingDetail)>? |  yes  |  |

---


 
 
 #### [Department](#Department)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | logo | [Media](#Media)? |  yes  |  |
 | priorityOrder | Int? |  yes  |  |
 | slug | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [DepartmentResponse](#DepartmentResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[Department](#Department)>? |  yes  |  |

---


 
 
 #### [AutocompleteItem](#AutocompleteItem)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | logo | [Media](#Media)? |  yes  |  |
 | type | String? |  yes  |  |
 | display | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |

---


 
 
 #### [AutoCompleteResponse](#AutoCompleteResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | items | ArrayList<[AutocompleteItem](#AutocompleteItem)>? |  yes  |  |

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


 
 
 #### [GetCollectionDetailNest](#GetCollectionDetailNest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tag | ArrayList<String>? |  yes  |  |
 | logo | [Media](#Media)? |  yes  |  |
 | schedule | HashMap<String,Any>? |  yes  |  |
 | allowFacets | Boolean? |  yes  |  |
 | cron | HashMap<String,Any>? |  yes  |  |
 | allowSort | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | uid | String? |  yes  |  |
 | description | String? |  yes  |  |
 | slug | String? |  yes  |  |
 | action | [ProductListingAction](#ProductListingAction)? |  yes  |  |
 | appId | String? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |
 | visibleFacetsKeys | ArrayList<String>? |  yes  |  |
 | badge | HashMap<String,Any>? |  yes  |  |
 | type | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |

---


 
 
 #### [GetCollectionListingResponse](#GetCollectionListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | filters | [CollectionListingFilter](#CollectionListingFilter)? |  yes  |  |
 | page | [Page](#Page) |  no  |  |
 | items | ArrayList<[GetCollectionDetailNest](#GetCollectionDetailNest)>? |  yes  |  |

---


 
 
 #### [CollectionDetailResponse](#CollectionDetailResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tag | ArrayList<String>? |  yes  |  |
 | appId | String? |  yes  |  |
 | badge | HashMap<String,Any>? |  yes  |  |
 | logo | [Media](#Media)? |  yes  |  |
 | description | String? |  yes  |  |
 | schedule | HashMap<String,Any>? |  yes  |  |
 | allowFacets | Boolean? |  yes  |  |
 | meta | HashMap<String,Any>? |  yes  |  |
 | type | String? |  yes  |  |
 | allowSort | Boolean? |  yes  |  |
 | slug | String? |  yes  |  |
 | query | HashMap<String,Any>? |  yes  |  |
 | cron | HashMap<String,Any>? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | name | String? |  yes  |  |
 | banners | [ImageUrls](#ImageUrls)? |  yes  |  |
 | visibleFacetsKeys | ArrayList<String>? |  yes  |  |

---


 
 
 #### [GetFollowListingResponse](#GetFollowListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page) |  no  |  |
 | items | ArrayList<[ProductListingDetail](#ProductListingDetail)> |  no  |  |

---


 
 
 #### [FollowPostResponse](#FollowPostResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String |  no  |  |
 | id | String |  no  |  |

---


 
 
 #### [FollowerCountResponse](#FollowerCountResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | count | Int? |  yes  |  |

---


 
 
 #### [FollowIdsData](#FollowIdsData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | collections | ArrayList<Int>? |  yes  |  |
 | products | ArrayList<Int>? |  yes  |  |
 | brands | ArrayList<Int>? |  yes  |  |

---


 
 
 #### [FollowIdsResponse](#FollowIdsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [FollowIdsData](#FollowIdsData)? |  yes  |  |

---


 
 
 #### [LatLong](#LatLong)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | coordinates | ArrayList<Double>? |  yes  |  |
 | type | String? |  yes  |  |

---


 
 
 #### [Store1](#Store1)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | state | String? |  yes  |  |
 | address | String? |  yes  |  |
 | latLong | [LatLong](#LatLong)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | country | String? |  yes  |  |
 | storeEmail | String? |  yes  |  |
 | pincode | Int? |  yes  |  |
 | storeCode | String? |  yes  |  |
 | city | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [StoreListingResponse](#StoreListingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page) |  no  |  |
 | items | ArrayList<[Store1](#Store1)> |  no  |  |

---


 
 
 #### [PhoneNumber](#PhoneNumber)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | countryCode | Int? |  yes  |  |
 | number | String? |  yes  |  |

---


 
 
 #### [StoreManagerSerializer](#StoreManagerSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | mobileNo | [PhoneNumber](#PhoneNumber)? |  yes  |  |
 | email | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [StoreDepartments](#StoreDepartments)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | Int? |  yes  |  |
 | logo | String? |  yes  |  |
 | priorityOrder | Int? |  yes  |  |
 | slug | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [StoreAddressSerializer](#StoreAddressSerializer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | state | String? |  yes  |  |
 | longitude | Double? |  yes  |  |
 | landmark | String? |  yes  |  |
 | country | String? |  yes  |  |
 | address1 | String? |  yes  |  |
 | address2 | String? |  yes  |  |
 | latitude | Double? |  yes  |  |
 | pincode | Int? |  yes  |  |
 | city | String? |  yes  |  |

---


 
 
 #### [CompanyStore](#CompanyStore)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | businessType | String? |  yes  |  |
 | companyType | String? |  yes  |  |
 | uid | Int? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [AppStore](#AppStore)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | manager | [StoreManagerSerializer](#StoreManagerSerializer)? |  yes  |  |
 | departments | ArrayList<[StoreDepartments](#StoreDepartments)>? |  yes  |  |
 | address | [StoreAddressSerializer](#StoreAddressSerializer)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | company | [CompanyStore](#CompanyStore)? |  yes  |  |
 | name | String? |  yes  |  |
 | contactNumbers | ArrayList<[PhoneNumber](#PhoneNumber)>? |  yes  |  |

---


 
 
 #### [ApplicationStoreListing](#ApplicationStoreListing)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | page | [Page](#Page)? |  yes  |  |
 | items | ArrayList<[AppStore](#AppStore)>? |  yes  |  |
 | filters | ArrayList<[StoreDepartments](#StoreDepartments)>? |  yes  |  |

---


 
 
 #### [Time](#Time)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | hour | Int? |  yes  |  |
 | minute | Int? |  yes  |  |

---


 
 
 #### [StoreTiming](#StoreTiming)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | opening | [Time](#Time)? |  yes  |  |
 | weekday | String? |  yes  |  |
 | open | Boolean? |  yes  |  |
 | closing | [Time](#Time)? |  yes  |  |

---


 
 
 #### [StoreDetails](#StoreDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | manager | [StoreManagerSerializer](#StoreManagerSerializer)? |  yes  |  |
 | departments | ArrayList<[StoreDepartments](#StoreDepartments)>? |  yes  |  |
 | address | [StoreAddressSerializer](#StoreAddressSerializer)? |  yes  |  |
 | uid | Int? |  yes  |  |
 | timing | ArrayList<[StoreTiming](#StoreTiming)>? |  yes  |  |
 | company | [CompanyStore](#CompanyStore)? |  yes  |  |
 | customJson | HashMap<String,Any>? |  yes  |  |
 | name | String? |  yes  |  |
 | contactNumbers | ArrayList<[PhoneNumber](#PhoneNumber)>? |  yes  |  |

---



