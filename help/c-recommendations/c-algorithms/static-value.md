---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;static;static filter
description: Manually enter one or more static values to filter using inclusion rules in Adobe Target Recommendations.
title: Filter by static values in inclusion rules in Adobe Target Recommendations
feature: criteria
---

# ![PREMIUM](/help/assets/premium.png) Static Filter

Manually enter one or more static values to filter using inclusion rules in Adobe Target Recommendations.

For example, only recommend content with an MPAA rating of "G" or "PG."

Available operators:

* equals
* does not equal
* contains
* does not contain
* starts with
* ends with
* value is present
* value is not present
* is greater than or equal to
* is less than or equal to

>[!NOTE]
>
>If you are familiar with how inclusion rules were configured prior to the Target 17.6.1 release (June 2017), you'll notice that some of the options and operators have changed. Only those operators applicable to the selected option display and some operators were renamed ("matches" is now "equals") to be more consistent and intuitive. All existing exclusion rules created prior to this release were automatically migrated into the new structure. No restructuring is necessary on your part.

You can create as many inclusion rules as necessary. The inclusion rules are joined with an AND operator. All rules must be met to include an item in a recommendation.