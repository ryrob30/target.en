---
keywords: multi-value;attributes;recommendations;multi value;multivalue;multi-value
description: Information about working with a multi-value field in Adobe Target Recommendations using special multi-value operators.
title: Working with multi-value attributes in Adobe Target Recommendations
feature: criteria
---

# Work with multi-value attributes

Sometimes you might want to work with a multi-value field. Consider the following examples:

* You offer movies to users. A given movie has multiple actors.
* You sell tickets to concerts. A given user has multiple favorite bands.
* You sell clothing. A shirt is available in multiple sizes.

To handle recommendations in these scenarios, you can pass multi-value data to [!DNL Target Recommendations] and use special multi-value operators.

To allow [!DNL Recommendations] to identify multi-value data, it should be sent as a JSON array, as in the below code samples.

## Pass a multi-value parameter in JavaScript

```
function targetPageParams() { 
  return { 
    'entity.id':                   '123', 
    'entity.categoryId':            '["A", "A:B", "A:B:C", "A:B:C:D"]',        
    'entity.MultiValueAttribute':   '["X", "Y", "Z"]', 
    'entity.event.detailsOnly':     'true', 
    'excludedIds":                  '[123, 3232, 2323, 4344]', 
    'orderId":                      '123456', 
    'orderTotal":                   '195.32', 
    'productPurchaseId":            '[001,002,003]' 
  }; 
}
```

For more information, see [Implementing multi-value attributes](/help/c-recommendations/c-products/custom-entity-attributes.md#section_80FEFE49E8AF415D99B739AA3CBA2A14) in *Custom entity attributes*.

## Pass a multi-value entity attribute in a CSV file

```
## RECSRecommendations Upload File,,,,,,,,,,,,,,,,,,,
## RECS''## RECS'' indicates a Recommendations pre-process header. Please do not remove these lines.,,,,,,,,,,,,,,,,,,,
## RECS,,,,,,,,,,,,,,,,,,,
## RECSUse this file to upload product display information to Recommendations. Each product has its own row. Each line must contain 19 values and if not all are filled a space should be left.,,,,,,,,,,,,,,,,,,,
## RECSThe last 100 columns (entity.custom1 - entity.custom100) are custom. The name 'customN' can be replaced with a custom name such as 'onSale' or 'brand'.,,,,,,,,,,,,,,,,,,,
## RECSIf the products already exist in Recommendations then changes uploaded here will override the data in Recommendations. Any new attributes entered here will be added to the product''s entry in Recommendations.,,,,,,,,,,,,,,,,,,,
## RECSentity.id ,entity.name,entity. categoryId ,entity. message ,entity.thumbnailUrl ,entity.value ,entity.pageUrl ,entity.inventory ,entity.margin ,entity.custom1 ,entity.custom2 ,entity.custom3 ,entity.custom4,entity.custom5,entity.custom6,entity.custom7,entity.custom8,entity.custom9,entity.custom10,
1,Sample Product 1,category1,Save 10%,http://sample.store/products/images/product1_th.jpg,325,http://sample.store/products/product_detail.jsp?productId=1,1000,48,a,"[ ""v1"", ""v2"" ]",, , , , , , , ,
2,Sample Product 2,category1,Save 10%,http://sample.store/products/images/product2_th.jpg,369,http://sample.store/products/product_detail.jsp?productId=2,1000,52,a,"[ ""v1"", ""v2"" ]",, , , , , , , ,
3,Sample Product 3,category1,Save 10%,http://sample.store/products/images/product3_th.jpg,479,http://sample.store/products/product_detail.jsp?productId=3,1000,78,a,"[ ""v1"", ""v2"" ]",,,,,,,,,
4,Sample Product 4,category1,Save 10%,http://sample.store/products/images/product4_th.jpg,409,http://sample.store/products/product_detail.jsp?productId=4,1000,66,a,"[ ""v1"", ""v2"" ]",,,,,,,,,
5,Sample Product 5,category1,Save 10%,http://sample.store/products/images/product5_th.jpg,325,http://sample.store/products/product_detail.jsp?productId=5,1000,45,a,"[ ""v1"", ""v2"" ]",,,,,,,,, 
```

When an entity attribute, profile attribute, or mbox parameter is provided as multi-value according to the above format, [!DNL Recommendations] automatically infers that the field is multi-value.

The following operators are available for use with multi-value entity, profile, and mbox attributes:

* [!UICONTROL is contained in list]
* [!UICONTROL is not contained in list]

## Working with multi-value attributes in inclusion rules

>[!NOTE]
>
>Support for dynamic matching to multi-value attributes is currently available only in criteria when using a profile attribute matching or parameter (mbox) attribute matching rule when comparing a single value left side to a multi-value right side. Multi-value attributes are not currently supported in promotions, entity attribute matching, or for lists on the left side of inclusion rules.

### Example: Exclude recently watched items

Suppose that you want to prevent any movies that are in the user’s last ten watched movies from being recommended. First, write a profile script called `user.lastWatchedMovies` to track the last ten viewed movies as a JSON array. Then, you can exclude the items by using the following inclusion rule:

```
`Profile Attribute Matching`
`id - is not contained in list - user.lastWatchedMovies`
```

JSON API representation of the inclusion rule:

```
{
    "attribute": "id",
    "operation": "isNotContainedInList",
    "source": {
        "name": "user.lastWatchedMovies",
        "type": "PROFILE"
    }
} 
```

### Example: Recommend items from the user's favorites

Suppose that you want to recommend tickets only to concerts if the band playing is one of the user's favorite bands. First, ensure that you have a profile variable called `profile.favoriteBands` that contains the user's favorite bands. Then, ensure that your catalog includes an attribute `entity.artistPerforming` that includes the artist performing in the concert. Then, you can use the following inclusion rule:

```
`Profile Attribute Matching`
`artistPerforming - is contained in list - profile.favoriteBands`
```

JSON API representation of the inclusion rule:

```
{
    "attribute": "artistPerforming",
    "operation": "isContainedInList",
    "source": {
        "name": "profile.favoriteBands",
        "type": "PROFILE"
    }
}
```

### Example: API creation of criteria recommending items from a user's favorites

Criteria using multi-value filtering rules, like all criteria, can be created via Adobe I/O APIs. An example API call to create a criteria where the entity attribute `id` is contained in the mbox parameter list `favorites` is provided here:

```
curl -X POST \
  https://<serverhost>/api/recs/<client>/criteria/item \
  -H 'Accept: application/vnd.adobe.target.v1+json' \
  -H 'Accept-Encoding: gzip, deflate' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Content-Type: application/json' \
  -H 'User-Agent: <from API client>' \
  -H 'X-Target-user-email: <email address>' \
  -H 'cache-control: no-cache' \
  -d '{
    "name": "viewed criteria",
    "criteriaTitle": "test title",
    "type": "VIEWED_CF",
    "key": "CURRENT",
    "daysCount": "TWO_WEEKS",
    "aggregation": "NONE",
    "backupDisabled": false,
    "partialDesignAllowed": true,
    "configuration": {
        "inclusionRules": [
            {
                "attribute": "id",
                "operation": "isContainedInList",
                "source": {
                    "name": "mbox.favorites",
                    "type": "MBOX"
                }
            }
        ]
    }
}'
```

This would be paired with JavaScript on the page to pass in the favorites contents:

```
<!-- pass in the value of mbox parameter “favorites” as JSON array -->
<script type="text/javascript">
   mboxCreate('myMbox','entity.id=<key>','favorites=["a","b","c"]');
</script>
```
