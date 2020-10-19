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
* Regional geo-location parameters can be used to return recommendations for tools during the winter. Snow blowers and other snow abatement tools can be recommended for visitors in areas where it snows but not recommended for visitors in areas where it does not snow.

>[!NOTE]
>
>If the activity was created before October 31, 2016, its delivery will fail if it uses the "Parameter Matching" filter. To work around this problem:
>
>* Create a new activity and add your criteria in it.
>* Use a criteria that does not contain the "Parameter Matching" filter.
>* Remove the "Parameter Matching" filter from your criteria.

Available operators:

* equals
* does not equal
* contains
* does not contain
* starts with
* ends with
* is greater than or equal to
* is less than or equal to
* is between