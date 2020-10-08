---
keywords: document.write;target;implement;implement target;dtm;dynamic tag management;at.js;mbox.js;target.js;mbox
description: Implement Target by referencing the Target libraries (at.js or mbox.js) on your web pages.
title: Understand the Target JavaScript libraries
feature: implementation general
topic: Target
uuid: c8a254c9-afc9-4a55-be01-788c11bef7cc
---

# Understand the [!DNL Target] JavaScript libraries{#understand-the-target-javascript-libraries}

Implement [!DNL Target] by referencing the [!DNL Target] libraries (at.js or mbox.js) on your web pages.

>[!NOTE]
>
>The mbox.js library is no longer being developed. All customers should migrate from mbox.js to at.js. For more information, see [Migrate to at.js from mbox.js](../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

## Differences Between the Two Libraries {#section_40117C78C2F84FECAC4F1BA40CC4F171}

The following table explains the differences between the two libraries:

| Library Reference | Description |
|--- |--- |
|at.js|at.js replaces mbox.js for [!DNL Target] implementations.<br>Among other benefits, at.js improves page-load times for web implementations, improves security, prevents  document.write warnings in Google Chrome, and provides better implementation options for single-page applications.<br>For more information, see [at.js Implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md).|
|mbox.js|Prior to [!DNL Target] 16.3.1 (March 2016), [!DNL Target] required a call to mbox.js to create the global mbox required for [!DNL Target] to deliver activities, track clicks, and track most success metrics. This file contains the libraries needed for all of your activities. You do not need to maintain different activity-specific versions of the file.<br>If you already have wrapping mboxes on your pages from an older style of [!DNL Target] implementation, these mboxes can still be used in the new interface. The updated mbox.js file is still required, but these mboxes can be selected for activities and edited using the  Visual Experience Composer.<br>[!DNL Target] Standard and Premium update and supplement mbox.js with a reference to a  target.js file. The  target.js file is hosted by Adobe. The  Target.js file makes it possible to edit content on any page using the  Visual Experience Composer, even if the page does not contain predefined mboxes. You must reference this file on every page on your site.<br>For more information, see [mbox.js Implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md).<br>**Important**: The mbox.js library is still supported, but there will be no feature updates. All customers should migrate to at.js. For more information, see [Migrate to at.js from mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md)<br>|

## Impact of at.js and mbox.js on Page-Load Time {#section_16630CD0FF0A498EB596A51381366A5A}

Many customers and consultants want to know the impact of [!DNL at.js] and [!DNL mbox.js] on page-load time, especially in the context of new vs returning users. Unfortunately, it's hard to measure and give concrete numbers regarding how [!DNL at.js] or [!DNL mbox.js] influence page-load time due to each customer's implementation.

However, if the Visitor API is present on the page, we can better understand how [!DNL at.js] and [!DNL mbox.js] influence page-load time.

>[!NOTE]
>
>The Visitor API and [!DNL at.js] or [!DNL mbox.js] have an impact on page-load time only when you are using the global mbox (because of the body-hiding technique). Regional mboxes are not impacted by Visitor API integration.

The following sections describe the sequence of actions for new and returning visitors:

### New visitors

1. The Visitor API is loaded, parsed, and executed.
1. at.js / mbox.js is loaded, parsed, and executed.
1. If global mbox auto-create is enabled, the Target JavaScript library:

   * Instantiates the Visitor object.
   * The Target library tries to retrieve Experience Cloud Visitor ID data.
   * Because this is a new visitor, the Visitor API fires a cross-domain request to demdex.net.
   * After Experience Cloud Visitor ID data is retrieved, a request to Target is fired.

### Returning Visitors

1. The Visitor API is loaded, parsed, and executed.
1. at.js / mbox.js is loaded, parsed, and executed.
1. If global mbox auto-create is enabled, the Target JavaScript library:

   * Instantiates the Visitor object.
   * The Target library tries to retrieve Experience Cloud Visitor ID data.
   * The Visitor API retrieves data from cookies.
   * After Experience Cloud Visitor ID data is retrieved, a request to Target is fired.

>[!NOTE]
>
>For new visitors, when the Visitor API is present, Target has to go over the wire multiple times to make sure that Target requests contain Experience Cloud Visitor ID data. For returning visitors, Target goes over the wire only to Target to retrieve the personalized content. 
