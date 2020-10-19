---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;profile attribute matching
description: Filter dynamically in Adobe Target Recommendations by comparing items (entities) against a value in the user's profile.
title: Filter by Profile Attribute Matching in dynamic inclusion rules in Adobe Target Recommendations
feature: criteria
---

# ![PREMIUM](/help/assets/premium.png) Profile Attribute Matching

Filter dynamically in [!DNL Adobe Target] [!DNL Recommendations] by comparing items (entities) against a value in the user's profile.

Use [!UICONTROL Profile Attribute Matching] when you want to show recommendations that match a value stored in the visitor’s profile, such as size or favorite brand. 

The following scenarios show how you can use [!UICONTROL Profile Attribute Matching]:

* A company that sells eyeglasses stores a visitor's favorite frame color as “walnut.” For that specific visitor, recommendation are set up to return only eyeglass frames that match “walnut” in color.
* A profile parameter can be defined for the clothing size (e.g., Small, Medium, or Large) of a visitor as they navigate your company’s web site. A recommendation can be set up to match that profile parameter and return products specific only to the user’s preferred clothing size.

## Profile Attribute Matching Examples {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Profile Attribute Matching] allows you to recommend only the items that match an attribute from the visitor's profile, as in the examples below.

### Recommending items from the user's favorite brand

For example, you can use the [!UICONTROL Profile Attribute Matching] option to create a rule that recommends items only where the brand equals the value or text stored in `profile.favoritebrand`. With such a rule, if a visitor is looking at running shorts from a particular brand, only recommendations will display that match that user's favorite brand (the value stored in `profile.favoritebrand` in the visitor's profile).

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Matching jobs to job seekers

Suppose that you're trying to match jobs to job seekers. You want to recommend only jobs that are in the same city as the job seeker.

You can use inclusion rules to match a job seeker's location from his or her visitor's profile to a job listing, as in the following example:

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Recommending clothes that match a visitor's size

Let's look at an example to recommend clothes that match the clothing size set in the visitor's profile.

The product page sends `entity.size` in the mbox call (red arrow in the illustration below).

You can create a [profile script](/help/c-target/c-visitor-profile/profile-parameters.md) to capture the visitor's profile attributes and values from the last page that the visitor visited.

For example,

```
if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'small')) { return 'small';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'medium')) { return 'medium';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'large')) { return 'large';
}
```

The profile script captures the `entity.size` value from the mbox named `target-global-mbox` and returns it as a profile attribute named `user.size` (blue arrow in the illustration below).

![size mbox call](/help/c-recommendations/c-algorithms/assets/size.png)

When creating the recommendation criteria, click [!UICONTROL Add Filtering Rule], then select [!UICONTROL Profile Attribute Matching].

![Profile attribute matching illustration](/help/c-recommendations/c-algorithms/assets/profile-attribute-matching.png)

If your `user.size` profile has been loaded into [!DNL Target], it displays in the drop-down for matching when you set up the rule to match the value passed in the mbox call (`size`) to the profile script name (`user.size`).

You can then select "size" "equals" the value/text stored in "user.size" for your profile attribute matching.

After your profile attribute rules are built, they will filter out all recommendations that have attributes that do not match the visitor's stored profile attribute.

### Recommending items based on size

For a visual example of how profile attribute matching affects recommendations, consider a website that sells fans.

When a visitor clicks various images of fans on this website, each page sets the value of the `entity.size` parameter based on whether the size of the fan in the image is small or large.

Assume you created a profile script to track and count the number of times the value of `entity.size` is set to small vs. large.

If the visitor then returns to the Home Page, he or she will see filtered recommendations based on whether more small fans or large fans were clicked.

Recommendations based on viewing more small fans on the website:

![small fans recommendations](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations based on viewing more large fans on the website:

![large fans recommendations](/help/c-recommendations/c-algorithms/assets/large-fans.png)