---
keywords: inclusion rules;inclusion criteria;recommendations;create new criteria;promotion;promotions;dynamic filtering;dynamic;empty values;ignore filtering rule;static filter;filter by value;entity attribute matching;profile attribute matching;parameter matching;filter by value;static filter
description: Information about creating inclusion rules in Adobe Target Recommendations for criteria and promotions, and adding additional dynamic or static filtering rules to achieve better results.
title: Use dynamic and static inclusion rules in Adobe Target Recommendations
feature: criteria
mini-toc-levels: 3
uuid: f0ee2086-1126-44a4-9379-aa897dc0e06b
---

# ![PREMIUM](/help/assets/premium.png) Use dynamic and static inclusion rules{#use-dynamic-and-static-inclusion-rules}

Information about creating inclusion rules for criteria and promotions in [!DNL Adobe Target] and adding additional dynamic or static filtering rules to achieve better results for your recommendations.

>[!NOTE]
>
>The process for creating and using inclusion rules for criteria and promotions is similar, as are the use cases and examples. Both criteria and promotions and the use of inclusion rules are covered in this section.

## Adding Filtering Rules to Criteria {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

While you are [creating criteria](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE), click **[!UICONTROL Add Filtering Rule]** under **[!UICONTROL Inclusion Rules]**.

![](assets/inclusion_options_new.png)

The available options vary depending on the selected industry vertical and recommendation key.

## Adding Filtering Rules to Promotions {#section_D59AFB62E2EE423086281CF5D18B1076}

While [creating a promotion](../../c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14), select **[!UICONTROL Promote by Attribute]**, then click **[!UICONTROL Add Filtering Rule]**.

![](assets/inclusion_options.png)

## Filter Types {#section_0125F1ED10A84C0EB45325122460EBCD}

The following sections list the types of filtering options for [!UICONTROL Dynamic Filtering] and [!UICONTROL Filter by Value] for both criteria and promotions:

### Dynamic Filtering

Dynamic inclusion rules are more powerful than static inclusion rules and they yield better results and engagement. Consider the following:

* Dynamic inclusion rules deliver recommendations by matching an attribute in a user’s profile parameter or in an mbox call.

  For example, you can create a "Most Popular Criteria" recommendation, and then of the set of returned recommendations, then filter out any recommendations (in real-time) against an attribute passed when the user accesses a page where the recommendations are displayed.

* Use static rules to limit which items are included in the recommendation (instead of using collections).

* You can create as many dynamic inclusion rules as necessary. The inclusion rules are joined with an AND operator. All rules must be met to include an item in a recommendation.

The following options are available for dynamic filtering:

|Dynamic filtering option|Details|
| --- | --- |
|[Entity Attribute Matching](/help/c-recommendations/c-algorithms/entity-attribute-matching.md)|Filter dynamically by comparing a pool of potential recommendations items to a specific item that the users has interacted with.<br>Use [!UICONTROL Entity Attribute Matching] when you want to show recommendations most likely to appeal to the visitor, such as the visitor's favorite brand.|
|[Profile Attribute Matching](/help/c-recommendations/c-algorithms/profile-attribute-matching.md)|Filter dynamically by comparing items (entities) against a value in the user's profile.<br>Use [!UICONTROL Profile Attribute Matching] when you want to show recommendations that match a value stored in the visitor’s profile, such as size or favorite brand.|
|[Parameter Matching](/help/c-recommendations/c-algorithms/parameter-matching.md)|Filter dynamically by comparing items (entities) against a value in the request (API or mbox).<br>Use [!UICONTROL Parameter Matching] to recommend content that matches the page parameters or the visitor's parameters, such as device dimensions or geo-location.|

### Filter by Value

The following option is available for filtering by value:

|Filtering by value option|Details|
| --- | --- |
|[Static Filter](/help/c-recommendations/c-algorithms/static-value.md)|Manually enter one or more static values to filter.|

## Dynamic criteria and promotion examples

Dynamic criteria and promotions are much more powerful than static criteria and promotions and yield better results and engagement.

The following examples provide general ideas about how you can use dynamic promotions in your marketing efforts:

|Operator|Examples|
| --- | --- |
|Equals|Using the "equals" operator in dynamic promotions, when a visitor is viewing an item on your website (such as a product, article, or movie), you can promote other items from:<ul><li>the same brand</li><li>the same category</li><li>the same category AND from the house brand</li><li>the same store</li></ul>|
|Does Not Equal|Using the "does not equal" operator in dynamic promotions, when a visitor is viewing an item on your website (such as a product, article, or movie), you can promote other items from:<ul><li>a different TV series</li><li>a different genre</li><li>a different product series</li><li>a different style ID</li></ul>|
|Is Between|Using the "is between" operator in dynamic promotions, when a visitor is viewing an item on your website (such as a product, article, or movie), you can promote other items that are:<ul><li>more expensive</li><li>less expensive</li><li>cost plus or minus 30%</li><li>later episodes in the same season</li><li>prior books in a series</li></ul>|

## Handling empty values when filtering by Entity Attribute Matching, Profile Attribute Matching, and Parameter Matching {#section_7D30E04116DB47BEA6FF840A3424A4C8}

You can choose several options to handle empty values when filtering by [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], and [!UICONTROL Parameter Matching] for exit criteria and promotions.

Previously, no results were returned if a value was empty. The "If *x* is Empty" drop-down list lets you choose the appropriate action to perform if the criteria has empty values, as shown in the following illustration:

![](assets/empty_value.png)

To select the desired action, hover over the gear icon (![](assets/icon_gear.png)), then choose the desired action:

| Action | Available For | Details |
|--- |--- |--- |
|[!UICONTROL Ignore this filtering rule]|[!UICONTROL Profile Attribute Matching] and[!UICONTROL Parameter Matching]|This is the default action for [!UICONTROL Profile Attribute Matching] and [!UICONTROL Parameter Matching].<br>This option specifies that the rule is ignored. For example, if there are three filtering rules and the third rule doesn't pass any values, instead of not returning any results, you can simply ignore the third rule with the empty values.|
|[!UICONTROL Do not show any results for this criteria]<br>(Criteria only)|[!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], and [!UICONTROL Parameter Matching]|This is the default action for [!UICONTROL Entity Attribute Matching].<br>This action is how [!DNL Target] handled empty values before the addition of this option: no results will be shown for this criteria.|
|[!UICONTROL Do not promote any items<br>(Promotions only)]|[!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], and [!UICONTROL Parameter Matching]|This is the default action for [!UICONTROL Entity Attribute Matching].<br>This action is how [!DNL Target] handled empty values before the addition of this option: no results will be shown for this criteria.|
|[!UICONTROL Use a static value]|[!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], and [!UICONTROL Parameter Matching]|If a value is empty, you can choose to use a static value.|

## Caveats {#section_A889FAF794B7458CA074DEE06DD0E345}

>[!IMPORTANT]
>
>Different data type attributes might not be compatible in dynamic criteria or promotions during runtime with the "equals" and "does not equal" operators. You should use [!UICONTROL Value], [!UICONTROL Margin], [!UICONTROL Inventory], and [!UICONTROL Environment] values wisely on the right hand side if the left hand side has predefined attributes or custom attributes.

![](assets/left_right.png)

The following table shows effective rules and rules that might not be compatible during runtime:

| Compatible Rules | Potentially Incompatible Rules |
|--- |--- |
|value - is between - 90% and 110% of current item's - salesValue|salesValue - is between - 90% and 110% of current item's - value|
|value - is between - 90% and 110% of current item's - value|clearancePrice - is between - 90% and 110% of current item's - margin|
|margin - is between - 90% and 110% of current item's - margin|storeInventory - equals - current item's - inventory|
|inventory - equals - current item's - inventory||
