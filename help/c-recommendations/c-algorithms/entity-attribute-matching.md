---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;entity attribute matching
description: Filter dynamically in Adobe Target Recommendations by comparing a pool of potential recommendations items to a specific item that the user has interacted with.
title: Filter by Entity Attribute Matching in dynamic inclusion rules in Adobe Target Recommendations
feature: criteria
---

# ![PREMIUM](/help/assets/premium.png) Entity Attribute Matching

Filter dynamically in [!DNL Adobe Target] [!DNL Recommendations] by comparing a pool of potential recommendations items to a specific item that the user has interacted with.

>[!NOTE]
>
>The [process for creating and using inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) for criteria and promotions is similar, as are the use cases and examples.

For example, recommend only items that match the current item’s brand as in the following example:

If the mbox on a Brand Landing Page returns `entity.brand=Nike`, then only Nike products are returned and displayed on that page. Similarly, on the Brand Landing Page for Adidas, only Adidas products are returned. With this type of dynamic inclusion rule, the user has to only specify one recommendation rule that returns relevant brand results across all brand pages rather than specifying a collection or a static filter to match each brand name.

Note that you must deliver the `entity.brand` in the mbox on those landing pages for this to work.

## Entity Attribute Matching examples 

[!UICONTROL Entity Attribute Matching] allows you to recommend only the items that match, for example:

* An attribute from the item the user is currently viewing
* The item the user most recently viewed
* The item the user most recently purchased
* The item the user most frequently viewed
* An item stored in a custom attribute in the visitor's profile

### Recommending items based on brand

After your entity attribute rules are built, they will filter out all recommendations with attributes that do not match the entity value passed on the page.

The following example shows recommendations matching product brand shown on the page:

When you visit a page that features a Nike product, the page sets the value of the `entity.brand` parameter to “Nike”.

![Example Target call](/help/c-recommendations/c-algorithms/assets/example-target-call.png)

In the recommendations on the page, you will see Nike products only.

![Nike recommendations](/help/c-recommendations/c-algorithms/assets/nike.png)

If you then view an Adidas product page, the `entity.brand` value will be reset to “Adidas” and you will see Adidas products recommended on Adidas product pages.

![Adidas recommendations](/help/c-recommendations/c-algorithms/assets/adidas.png)

### Upselling to a more expensive product

Suppose that you're an apparel retailer and want to encourage users to consider higher-priced and, therefore, more profitable items. You can use the "equals" and "is between" operators to promote more expensive items that are from the same category and the same brand. For example, a shoe retailer can promote more expensive running shoes in an effort to up-sell a visitor looking at running shoes, as in the following code sample:

```
Entity Attribute Matching
category - equals - current item's - category 
And 
Entity Attribute Matching
brand - equals - current item's - brand 
And 
Entity Attribute Matching
value - is between - 100% and 1000% of - current item's - value
```

### Promoting private-label products

You can mix dynamic and static filters to promote private-label products. For example, an office supply company can promote toner cartridges of the company's house brand to drive a more profitable sale for a visitor looking at toner -- and promote pens of the company's house brand to drive a more profitable sale for a visitor looking at pens, as in the following code sample:

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```