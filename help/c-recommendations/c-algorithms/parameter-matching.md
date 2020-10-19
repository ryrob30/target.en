---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;parameter matching
description: Filter dynamically in Adobe Target Recommendations by comparing items (entities) against a value in the request (API or mbox).
title: Filter by Parameter Matching in dynamic inclusion rules in Adobe Target Recommendations
feature: criteria
---

# ![PREMIUM](/help/assets/premium.png) Parameter Matching

Filter dynamically by comparing items (entities) against a value in the request (API or mbox).

For example, only recommend content that matches the "industry" page parameter or other parameters, such as device dimensions or geo-location, as in the following examples.

* Mbox parameters for screen width and height can be used to target mobile visitors and recommend only mobile devices and accessories.
* Create a recommendations rule that returns only the top-selling mobile phones that match or exceed the screen height of the mobile device the visitor is using the view the page.
* Regional geo-location parameters can be used to return recommendations for tools during the winter. Snow blowers and other snow abatement tools can be recommended for visitors in areas where it snows but not recommended for visitors in areas where it does not snow.

>[!NOTE]
>
>If the activity was created before October 31, 2016, its delivery will fail if it uses the "Parameter Matching" filter. To work around this problem:
>
>* Create a new activity and add your criteria in it.
>* Use a criteria that does not contain the "Parameter Matching" filter.
>* Remove the "Parameter Matching" filter from your criteria.

## Parameter Matching examples

[!UICONTROL Parameter Matching] allows you to recommend content that matches the page parameters or the visitor's parameters, such as device dimensions or geo-location, as in the the following example:

[!DNL Recommendations] can match parameter values sent in the [!DNL Target] call. In this instance, [!DNL Target] detects that a visitor is using a mobile device, based on the screen height and width parameters sent in the [!DNL Target] call, and will recommend only items that are mobile devices.

Consider the following example Target call:

![Target call](/help/c-recommendations/c-algorithms/assets/example-target-call-2.png)

On the page a visitor is viewing, he or she will see mobile device products.

![Mobile device products](/help/c-recommendations/c-algorithms/assets/phones.png)
