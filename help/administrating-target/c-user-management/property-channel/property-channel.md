---
keywords: workspaces;manage property;permissions;product configuration;product profile;roles;project
description: Information about creating properties and using the Properties and Permissions functionality that lets Target administrators create separate workspaces (product profiles) in Target and then assign users different roles and permissions for individual pages, properties, or web sites based on these workspaces.
title: Enterprise user permissions
feature: user management
subtopic: Getting Started
uuid: 1961730d-2357-406f-acac-a36b7a63bd35
---

# ![PREMIUM](/help/assets/premium.png) Enterprise user permissions{#enterprise-user-permissions}

Enterprise user permissions is a means of formal administering enterprise-wide user access to [!DNL Target]. Add users to [!DNL Target], assign permissions based on their roles, and create workspaces for teams based on different departments, global locations, channels, and other logical groupings. You can assign users the roles of [!UICONTROL Observer], [!UICONTROL Editor], or [!UICONTROL Approver].

## Determine whether you have access to enterprise user permissions

>[!NOTE]
>
>Properties and Permissions functionality is available as part of the [!DNL Target] Premium solution. They are not available in [!DNL Target] Standard without a [!DNL Target] Premium license.
>
>Your [!DNL Target] implementation can be using any version of at.js or mbox.js.

You can tell whether your organization has a Standard or Premium license by clicking the [!UICONTROL Administration] link at the top of the [!DNL Target] UI.

* **[!DNL Target Standard] Customers**: If you see the [!UICONTROL Users] tab ([!UICONTROL Adminitration > Users]) (and not the [!UICONTROL Properties] tab), your organization has a [!DNL Target Standard] license. [!DNL Target Standard]customers should follow the instructions in [Users](/help/administrating-target/c-user-management/c-user-management/user-management.md) to add users and assign permissions in the [!DNL Adobe Admin Console].

* **[!DNL Target Premium] Customers**: If you see the [!UICONTROL Properties] tab ([!UICONTROL Administration > Properties]) and the [!UICONTROL Users] tab, your organization has a [!DNL Target Premium] license. [!DNL Target Premium] customers should follow the instructions in this article and in [Configure enterprise permissions](/help/administrating-target/c-user-management/property-channel/properties-overview.md).

## Before you get started with enterprise permissions

>[!IMPORTANT]
>
>Ensure that you read the [Caveats](../../../administrating-target/c-user-management/property-channel/property-channel.md#section_9714311B1CD9497A86F4910F8AE635E2) section below before proceeding with enterprise permissions.

## Terms and definitions used in this section {#section_F8D229544FEA41C3BC2EFD1F95AA0116}

The following terms are used throughout this section and might be new to users wanting to use the Properties and Permissions functionality in [!DNL Target] Premium.

### Property

Properties are similar in nature to those within [!DNL Adobe Platform Launch] in that they use a unique snippet of code to differentiate them.

A web property is a library of rules and one embed code. A web property can be any grouping of one or more domains and subdomains.

Properties are enabled by adding a specific name/value pair as a parameter with any call (Target call, api call, etc.) to [!DNL Target].

Properties belong to specific channels (Web, Mobile, Email, or API/Other).

### Workspace (Product Profile)

A workspace lets an organization assign a specific set of users to a specific set of properties. In many ways, a workspace is similar to a report suite in [!DNL Adobe Analytics].

Note: Workspaces are known as [!UICONTROL Product Profiles] in the [!DNL Adobe Admin Console for Enterprise].

If you are part of a multi-national organization, you might have a workspace for your European web pages, properties, or sites and another workspace for your American web pages, properties, or sites. If you are part of a multi-brand organization, you might have a separate workspace for each of your brands.

Users can be part of multiple workspaces and can even have different roles within each workspace.

Users can have different views of [!DNL Adobe Target] by moving between workspaces, similar to how [!DNL Analytics] users have different views of [!DNL Analytics] by moving between Report Suites.

Workspaces can include complete different audiences, code offers, and activities.

All audiences and activities created before the new Enterprise Permissions model migration will be grouped together in the "Default Workspace," discussed below.

All activities created via [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services], and [!DNL Adobe Target Classic] will be part of the "Default Workspace."

### Default workspace

All existing workspaces (product profiles) within [!DNL Admin Console] are merged into a single workspace called "Default Workspace" during your organization's migration to the new Enterprise Permissions model.

>[!IMPORTANT]
>
>Do not delete the Default Workspace.

All user roles and access to all [!DNL Target] functionality remains exactly the same as they were prior to the migration to the new Enterprise Permissions model.

### User groups

You can create user groups, such as Developers, Analysts, Marketers, Executives, etc., and then assign privileges across multiple Adobe products and workspaces. Assigning a new team member all the appropriate privileges across different Adobe products can be as easy as adding them to a specific user group.

### Roles and permissions

Roles and permissions determine the access levels that users have to create and manage activities in your [!DNL Target] implementation. In [!DNL Target], roles include the following:

| Role | Description |
|--- |--- |
|Approver|Can create, edit, and activate or stop activities.|
|Editor|Can create and edit activities before they are live, but cannot approve the launch of an activity.|
|Observer|Can view activities, but cannot create or edit them.|
|Publisher|Similar to the Observer role (can view activities, but cannot create or edit them). However, the Publisher role has the additional permission to activate activities.|

### Channel

Channel refers to the content type of where your [!DNL Target] activities are delivered: webpages, mobile apps, email messages,and so forth.

When you create a new activity, it is created in the currently selected workspace. You'll see channel selection options in the first dialog box that lets you choose the desired channel for the activity: Web, Mobile App, Email, or Other/API.

## Permissions overview {#section_DC2172520DA84605B218A5E9FB6D187A}

The following information explains the way permissions were enforced previously in [!DNL Target] and how they are enforced using the [!UICONTROL Properties] and [!UICONTROL Permissions] functionality.

The new [!UICONTROL Permissions] functionality lets you create different projects (called "Product Profiles" in the [!DNL Adobe Admin Console for Enterprise]) to allow you to assign different permissions for a single user that dictate that user's access rights for each project. These distinct projects can be compared to the way that report suites work in [!DNL Adobe Analytics]. Each project can have specific users with specific roles that apply to a set of properties. The result is that customers will be able to restrict the view, edit, and approval access to their users based on region, environment (dev/stage/prod), channel, or other custom criteria, as shown below:

![](assets/permissions.png)

For example, a specific user might have "approval" access on the Americas websites but only "view" access on the European mobile app. That same user might not have any access to even view the activities offered on web and mobile properties in the APAC region.

The current [!DNL Target] [!UICONTROL Permissions] model has three permission roles (Observer, Editor, and Approver), as shown in the following illustration:

![](assets/permissions_1.png)

Each role has different levels of permissions:

| Role | Description |
|--- |--- |
|Approver|Can create, edit, and activate or stop activities.|
|Editor|Can create and edit activities before they are live, but cannot approve the launch of an activity.|
|Observer|Can view activities, but cannot create or edit them.|
|Publisher|Similar to the Observer role (can view activities, but cannot create or edit them). However, the Publisher role has the additional permission to activate activities.|

It is important to note that each user's role applies to every page, property, or site in your account that includes [!DNL Target] tags, as shown below:

![](assets/permissions_2.png)

The new [!DNL Target] [!UICONTROL Permissions] model has the same three permission roles (Observer, Editor, and Approver); however, you can assign a user's permissions roles separately for individual pages, properties, or sites, as shown below:

![](assets/permissions_3.png)

In this example, Jan has Approver permissions to the US Homepage and the US Site and Observer permissions to the France Site.

Furthermore, Jan won't be able to see pages, properties, or sites in [!DNL Target] that she doesn't have permissions to see, as shown below:

![](assets/permissions_4.png)

In this example, Jan cannot see the Product Pages, Russia Site, and the Careers Site.

## Use-case scenarios {#section_F3CE8576959E4F4CB13BEEED38311DD8}

The following use cases might be helpful to understand how properties, projects, roles, and permissions can help you achieve your marketing goals with [!DNL Target]:

### Multi-national organization

If you are part of a multi-national organization, you might have a workspace for your European web pages, properties, or sites and another workspace for your American web pages, properties, or sites.
After a reorganization, using the personas in the illustrations above, you might set up workspaces and permissions similar to the following:

* **Jan**: Jan is the Head of Optimization in the Center of Excellence for her organization's United States web pages, properties, and sites. She most likely has System Admin rights in the Adobe Experience Cloud.

  In her role, she has Approver permissions for the US Homepage and the US Site. With Approver permissions, she can create, edit, and activate or stop activities.

  Jan also consults with the optimization team in France and, therefore, has Observer permissions for the France Site that give her read-only access to activities. Jan can view activities, but cannot create or edit them.

  Because Jan has no role that necessitates her seeing the Product Pages, Russia Site, or Careers Site, she cannot see activities for those sites.

* **Ernie**: Ernie is a Marketing Manager for the organization in charge of marketing in the United States.

  Because Ernie is fairly new to the organization and somewhat inexperienced with Target, he has Editor permissions for the US Homepage, US Site, and Product Pages. With Editor permissions, Ernie can create and edit activities before they are live, but he cannot approve the launch of an activity—someone with Approval permissions, such as Jan, must approve the activity before it can be put into production.

  Because Ernie has no role that necessitates him seeing the Russia Site, France Site, or Careers Site, he cannot see activities for those sites.

* **Diana**: Diana is now an Analyst for the organization and has been granted Observer permissions for the US Homepage US Site, Product Pages, Russia Site, and the France Site that give her read-only access to activities. Diana can view activities, but cannot create or edit them.

  Because Diana has no role that necessitates her seeing the Careers Site, she cannot see activities for those sites.

### Multi-brand organization

If you are part of a multi-brand organization, you might have a separate workspace for each brand's web pages, properties, or sites.

After a reorganization, using the personas in the illustrations above, you might set up projects and permissions similar to the following:

* **Jan**: Jan is the Head of Optimization in the Center of Excellence for a heath-care organization that operates in the hospital-product and consumer-product spaces. She most likely has System Admin rights in the Adobe Experience Cloud.

  In her role, she has Approver permissions for the Hospital Site. With Approver permissions, she can create, edit, and activate or stop activities.

  Jan also consults with the optimization team in the consumer-products space and, therefore, has Observer permissions for that site that give her read-only access to activities. Jan can view activities, but cannot create or edit them.

* **Ernie**: Ernie is a Marketing Manager for the organization in charge of marketing in the consumer-product space.

  Because Ernie is fairly new to the organization and somewhat inexperienced with Target, he has Editor permissions for the Consumer Site. With Editor permissions, Ernie can create and edit activities before they are live, but he cannot approve the launch of an activity—someone with Approval permissions for the Consumer Site, but not Jan in this scenario, must approve the activity before it can be put into production.

  Because Ernie has no role that necessitates him seeing the Hospital Site, he cannot see activities for that site.

* **Diana**: Diana is now an Analyst for the organization and has been granted Observer permissions for the Hospital Site and the Consumer Site that give her read-only access to activities. Diana can view activities, but cannot create or edit them.

## Target UI Property and Permissions touchpoints {#section_3414371393BB42999A268628B5456EC9}

The new Permissions functionality can be seen in various places in the [!DNL Target] UI.

* **Workspace (Product Profile) drop-down list:** The Workspace drop-down list displays at the top of the [!UICONTROL Activities], [!UICONTROL Audiences], and [!UICONTROL Offers] pages. Select the desired workspace to filter the list to display only items in the selected workspace.

  ![](assets/workspace_drop-down.png)

* **Activity Creation:** When you create a new activity, it is created in the currently selected workspace. You'll see channel selection options in the first dialog box that lets you choose the desired channel for the activity: Web, Mobile App, Email, or Other/API.

  ![](assets/channel_options.png)

* **Audience Creation:** When you create a new audience, it is created in the currently selected workspace. 
* **Offer Creation:** When you create a new offer, it is created in the currently selected workspace. 
* **Properties page (Administration > Properties):** You can use the [!UICONTROL Search] box to search the [!UICONTROL Property] list.

  ![](assets/properties_list.png)

## Caveats {#section_9714311B1CD9497A86F4910F8AE635E2}

Consider the following when using or configuring properties and permissions in [!DNL Target] Premium:

* **Important**: Do not delete workspaces with activities. If this happens, work with client care to recover those activities.
* When using the All My Workspaces view:

    * You can see activities, audiences, and offers for all workspaces that you have the proper roles and permissions to access. 
    * When you select the All My Workspaces view, a new column is added to the Activities, Audiences, and Offers page that lists the item's workspace and your user permission associated with that item (Observer, Editor, or Approver), 
    * When creating an activity, audience, or offer in the All My Workspaces view, you must select the workspace where the item is to be created. Only those workspaces can be selected for which you have the Editor or Approver permission. 
    * When copying an activity, audience, or offer in the All My Workspaces view, you must select the workspace where the item is to be copied. Only those workspaces can be selected for which you have the Editor or Approver permission.

* Any setting on the following the Administration pages can be controlled by any Approver in any workspace:

    * Visual Experience Composer 
    * Reporting
    * Scene7 Configuration
    * Implementation
    * Properties
    * Hosts 
    * Environments 
    * Response Tokens
    * Users

* Users cannot move resources from one workspace (product profile) to another. Copy, however, is supported. 
* When viewing audiences from the [!DNL Audiences] page, the page loads slower than expected. If you interact with the search bar in any way, audiences display faster. This is a known issue and will be fixed in an upcoming update. This issue does not affect selecting audiences during the activity-creation workflow. 
* The following resources are part of the new Enterprise Permissions model:

  * Activities, audiences, and code offers created within Target Standard/Premium after the customer is enabled for permissions. (Note: customers must be entitled to Target Premium.)
  * Properties can be added to existing activities in the Default Workspace; however, this is subject to change.
  * Only new resources (such as activities, code offers, and audiences) created within Target Premium (after Enterprise Permissions are enabled) will be available to restrict by permissions.
  * External resources are available only to users in the Default Workspace. A user's role in the Default Workspace applies globally (to all Target requests and all Target resources).

* The following resources are *not* part of the new Enterprise Permissions model:

  * Image offers
  * All Recommendations resources, including Criteria Library, Design Library, Catalog, Recommendations Setup.
  * Existing resources (such as activities, code offers, and audiences) created within Target Premium prior to enabling Enterprise Permissions can be copied but cannot be moved to other workspaces.
  * Activities, audiences, code offers, image offers, or any other resource created using the following solutions or methods cannot be controlled by the Enterprise Permissions model, but will be part of the Default Workspace: Target Classic, Adobe Experience Manager (AEM), Adobe Mobile Services, and resources created via API. Resources created via API include activities, audiences, code offers, and image offers).
  * Image offers (assets stored under `https://[tenantName].marketing.adobe.com/content/mac/[tenantName]/target/offers.html#image-library` cannot be controlled by the Enterprise Permissions model at this time.
  * clickTracking and redirects will only work when the destination link or destination page are part of a property that is included in the activity. Additionally, clickTracking may not work when using the `targetPageParams()` function. The `targetPageParamsAll()` is the recommended function.

  [!DNL Target] currently requires an `at_property` token to be present on any page where tracking occurs. In the event that the token is (1) not present, (2) not detected at the time of activity setup (within the VEC), or (3) not passed to the clickTracking Target call via the `targetPageParamsAll()` function, the metric will not be incremented and will appear as "0."

  The same applies for activities using redirects. The destination page must have an `at_property` token and be recognized at the time of setup within the VEC.

  In a future release, Target will work on pages where no `at_property` token is present or pages where a different `at_property` token is present.

* The Enterprise User Permissions functionality is not supported in [Adobe I/O API calls](https://developers.adobetarget.com).

## Frequently Asked Questions {#faqs}

FAQs about enterprise permissions include the following:

### Can I move an activity from one workspace to another?

Unfortunately, you cannot move activities from one workspace to another. However, you can copy an activity to any workspace knowing that reporting data will not carry over. For more information, see "Copying/Editing an Activity When Using Workspaces" in [Copying/Editing an Activity When Using Workspaces](../../../c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6).

Activities created before the migration continue to run the same way in the Default Workspace unless they are edited and assigned properties. Activities under a specific workspace will honor properties assigned to that workspace and, therefore, behavior might not remain same as before the migration.

### Why do I get an error message indicating that no property is associated with this activity, even though there is a property assigned?

If you implemented [!DNL Target] with [!DNL Adobe Launch] and get an error message indicating that there is no property associated with the activity, pass the `at_property` parameter with the `targetPageParams` function.

### Are click-track conversions recorded if a redirect page and the activity URL belong to different properties?

Click tracking is not recorded on pages where the page and activity URL belong to different properties.

Consider the following scenario (applies to both at.js and mbox.js):

* Page1 belongs to Property1.
* Page2 belongs to Property2.
* In the activity, Page1 redirects to Page2, which contains clicktracks.

When a visitor opens Page1 in a browser, he or she is redirected to Page2. Because Page2 does not qualify to deliver the activity, its Target call does not contain clicktracks in its response. 

If the redirect page and the activity URL belong to the same property, clicktracks work as expected. For more information, see [Click tracking](/help/c-activities/r-success-metrics/click-tracking.md).

## Training videos

The following videos contain more information about the concepts discussed in this article.

### Training Video: Enterprise Permissions Training Video ![Overview badge](/help/assets/overview.png)

Learning objectives:

* The three role levels that Adobe Target users can hold 
* The concepts of Properties and Workspaces, and how these boundaries and groupings work to allow for control over users' access levels 
* Different Property examples for your organization to consider

>[!VIDEO](https://video.tv.adobe.com/v/19042/)

### Office hours: Target Premium Workspaces

This video is a recording of "Office Hours," an initiative led by the Adobe Customer Care team.

* Creating a workspace (product profile)
* Creating properties
* Adding users
* Updating implementation

>[!NOTE]
>
>The [!DNL Target] [!UICONTROL Administration] menu UI (formerly [!UICONTROL Setup]) has been redesigned to provide improved performance, reduce the maintenance time required when releasing new features, and to improve the user experience across the product. The information in the following video is generally correct; however, options might be in slightly different locations. Updated videos will be posted soon.

>[!VIDEO](https://video.tv.adobe.com/v/23643/)
