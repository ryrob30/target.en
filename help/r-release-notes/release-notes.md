---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: These release notes provide information about features, enhancements, fixes, and known issues for each Adobe Target Standard and Target Premium release.
title: Adobe Target release notes (current) 
feature: release notes
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
---

# Target release notes (current){#target-release-notes-current}

These release notes provide information about features, enhancements, and fixes for each Target Standard and Target Premium release. In addition, release notes for Target APIs, SDKs, the JavaScript library (at.js), and other platform changes are also included, when applicable.

>[!IMPORTANT]
>
>* **Adobe Again Named a Leader in Gartner Magic Quadrant for Personalization Engines**: Adobe was once again named a Leader in the third-annual Gartner Magic Quadrant for Personalization Engines, 2020 report. The Gartner Magic Quadrant for Personalization Engines evaluated vendors across 15 criteria that fall into two categories: completeness of vision and ability to execute. [Read about it on The Adobe Blog](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
>
>* **mbox.js end-of-life**: On January 18, 2021, Adobe Target will no longer support the mbox.js library. Post January 18, 2021, all calls made from mbox.js will gracefully fail and impact your pages that have Target activities running by serving default content. We recommend that all customers migrate to the most recent version of the at.js library before this date to avoid any potential issues with your sites. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [Adobe Target Skill Builder: Developer chat, migrate Adobe Target's mbox.js to at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>   Although, mbox.js is currently supported, we have not provided feature updates to this library since July 2017. The newer at.js provides many advantages over mbox.js. Among other benefits, at.js improves page load times for web implementations, improves security, and provides better implementation options for single page applications.
>
>   By moving all customers to at.js, our engineers and support staff will be able to provide you with new functionality and offer the support you have come to expect from Adobe.
>
>* **Target Announcements**: See the Target announcements page for information about upcoming events, including Target Skill Builder sessions, developer chats, webinars, and Target Coffee Break sessions. For more information, see [Target announcements](/help/r-release-notes/target-announcements.md).

The issue numbers in parentheses are for internal [!DNL Adobe] use.

## Target Standard/Premium 20.9.1 (September 30, 2020)

This maintenance release contains the following enhancements, fixes, and changes:

* Improved navigation and functionality for keyboard-only users. (TGT-34487, TGT-34516, TGT-34517, TGT-34514)
* Added labels in the UI to aid users using assistive technologies. (TGT-34500, TGT-34501, TGT-34502, TGT-24504)
* Improved text and color contrast for images and text in UI. (TGT-34513)

## Target Standard/Premium 20.8.3 (September 15, 2020)

|Feature|Details|
| --- | --- |
|![Premium badge](/help/assets/premium.png) Analytics for Target (A4T) support for Auto-Target activities|[!UICONTROL Auto-Target] activities now support [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>This integration allows you to use the [!UICONTROL Auto-Target] ensemble machine learning algorithm to choose a best experience for each visitor based on their profile, behavior, and context.<br>If you’ve already [implemented A4T](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) for use with A/B Test and Experience Targeting activities, you’re all set!<br>For more information, see [Analytics for Target (A4T) support for Auto-Allocate and Auto-Target activities](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) in *Activity creation*.|

## Target Standard/Premium 20.8.2 (September 10, 2020)

|Feature|Details|
| --- | --- |
|![Premium badge](/help/assets/premium.png) Control recommendations slots within criteria sequences|Criteria Sequences now allow you to control the number of slots taken up by each recommendations criteria, enabling you to mix and match different types of items or different algorithm logic.<br>See [Create criteria sequences](/help/c-recommendations/c-algorithms/create-criteria-sequence.md#sequence) to learn more.|

## Target Standard/Premium 20.8.1 (September 2, 2020)

This release contains the following enhancements, fixes, and changes:

* Fixed an issue that caused errors to display when loading the new [!UICONTROL Administration] pages after switching organizations. (TGT-37730)
* Fixed a display issue that caused the incorrect client code to display on the [!UICONTROL Administration > Implementation] page. (TGT-37849)
* Fixed an issue that sometimes prevented users from using the editing features in the [!UICONTROL Visual Experience Composer] (VEC) after successfully loading the VEC. (TGT-37162)
* Fixed an issue that prevented pages from loading in the VEC and Enhanced Experience Composer (EEC) even though the VEC Helper extension was installed. This was due to changes in Google Chrome 80+. Download the [updated VEC Helper extension](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md). (TGT-37893) 
* Fixed an issue that sometimes prevented users from downloading at.js from the [!UICONTROL Administration > Implementation] page after switching organizations. (TGT-37668)
* The at.js download button is now disabled while loading to prevent [!DNL Target] from sending multiple requests if users click the download button multiple times. (TGT-37633)
* Fixed an issue in [!UICONTROL Experience Targeting] (XT) activities that caused experiences to display "fetching results" for an extended period of time. (TGT-37684)
* Improved navigation and functionality for keyboard-only users. (TGT-34479 & TGT-34473)
* Added labels in the UI to aid users using assistive technologies. (TGT-34480)
* Improved the error message when deleting a mobile viewport that is currently used in an activity. The error message now reads: "This viewport is currently associated to one or multiple activities. You need to remove the viewport from those activities before being able to delete it." (TGT-37030)
* Added support in the VEC to allow click tracking on a css selector that matches more than one element in the page. (TGT-37323)
* Fixed an issue that prevented certain users from displaying the [!UICONTROL Activity] list. The following error message was displayed: "Unable to fetch URLsuggestions." The error occurred for users using carriage returns in their FirstName (FirstName/r/n) in the Adobe Backend system. (TGT-37330)
* Fixed an issue that prevented users from displaying the [!UICONTROL Activity] page if the workspace name (specified in the [!UICONTROL Adobe Admin Console for Enterprise]) contains an apostrophe. (TGT-37709)
* Fixed an issue in [!UICONTROL Auto-Allocate] activities while selecting optimization and conversion metrics where an error message incorrectly informed users to select a report suite, even though a report suite was already specified. (TGT-37689)
* Fixed an issue that sometimes caused metrics on the [!UICONTROL Goals and Settings] page to be blank after navigating to the [!UICONTROL Targeting] page and then back. (TGT-37691)
* Fixed an issue that caused an incorrect last-modified value for [!DNL Recommendations] criteria. (TGT-37666)
* Fixed an issue that caused mbox IDs to display in the Mboxes drop-down list instead of mbox names. (TGT-37739)

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes - Target server-side APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md)|Release notes related to Adobe Target's server-side APIs.|
|[Release notes - Target Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md)|Release notes related to Adobe Target's Node.js SDK.|
|[Release Notes - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md)|Release notes related to Adobe Target's Java SDK.|
|[at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)|Details about changes in each version of the Adobe Target at.js JavaScript library.|
|[mbox.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md)|This page shows changes to each version of mbox.js.<br>Note that the mbox.js library is no longer being developed. All customers should migrate from mbox.js to at.js.|

## Documentation Changes, Past Release Notes, and Experience Cloud Release Notes {#section_1BC5F5208DA548E9B4344A0836E4B943}

In addition to the notes for each release, the following resources provide additional information:

|Resource|Details|
|--- |--- |
|Documentation changes|View detailed information about updates to this guide that might not be included in these release notes.<br>For more information, see [Documentation Changes](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C).|
|Release notes for previous releases|View information about new features and enhancements in previous releases of Target Standard and Target Premium.<br>For more information, see [Release notes for previous releases](../r-release-notes/release-notes-for-previous-releases.md).|
|Adobe Experience Cloud release notes|View the latest release notes for the Adobe Experience Cloud solutions.<br>For more information, see [Experience Cloud Release Notes](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html).|

## Prerelease Information {#section_5D588F0415A2435B851A4D0113ACA3A0}

The following resources let you see what's coming in the next Target release.

|Resource|Details|
|--- |--- |
|Adobe Priority Product Update list|To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)|
|Upcoming release notes|For information about the current month's Target releases, including prerelease information, see the [Target Release Notes - Prerelease](/help/r-release-notes/target-release-notes.md) page.|
