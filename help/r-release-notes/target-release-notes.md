---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming DNL Adobe Target releases.
title: Adobe Target prerelease notes
feature: 
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

This article contains prerelease information. Release dates, features, and other information are subject to change without notice. 

**Last Updated: October 15, 2020**

To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

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

## Target Standard/Premium 20.10.1 (October 27, 2020)

This release contains the following new features:

|Feature|Details|
| --- | --- |
|On-device Decisions|On-device Decisions lets both marketers and product developers deliver experimentation and Machine Learning-driven personalization from within a user's device, across channels, at near-zero latency.<br>Speed and performance matters--in customer insights and user satisfaction. On-device Decisions lets marketers, and now product developers, test and optimize experiences right from within a users device, decreasing decision and load times to nearly zero for real-time, contextual experiences.<br>On-device Decisions allows you to compile all personalization and experimentation instructions onto "optimization artifacts," which are loaded onto customer devices. These zero-latency artifacts give marketers one-to-one personalization, behavioral retargeting, and real-time product and content recommendations, while giving developers and product owners direct code access to test user experiences and target and phase product launches, refining in real-time. And because On-device Decisions connects natively with [!DNL Adobe Experience Cloud] products, [!DNL Target] users get rapid analysis and faster experience iterations.<br>**Register now for a live webinar.** Join Adobe Target product experts as they discuss how moving critical experience optimization decisions on-device to execute locally with zero latency can open doors to exciting new use cases while improving site performance for your customers.<ul><li>November 10, 2020</li><li>10 a.m. PT / 12 p.m. CT / 1 p.m. ET</li><li>[Register Here](https://www.adobeeventsonline.com/Target/2020/OnDeviceDecisions/invite.html)</li></ul>|

This release contains the following enhancements, fixes, and changes:

* Fixed an issue that prevented [!UICONTROL Average Lift Confidence Interval] and [!UICONTROL Confidence] from displaying in [!DNL Auto-Target] reporting for the [!UICONTROL Total] row. Measurements displayed correctly for all individual experiences. (TGT-37301)
* Fixed an issue that impacted [!DNL Adobe Target Premium] users’ [!UICONTROL Auto-Target] reporting from September 15, 2:30 p.m. (PDT) to October 6, 9:25 a.m. (PDT). When viewing reports for the impacted conversion metrics (configured using either the "[!UICONTROL Viewed a page]” or “[!UICONTROL Clicked on mbox]” option), the conversions rates are incorrectly reported. There is no known delivery issue at this time. For information about how to resynchronize and correct your reporting, see [Auto-Target reporting](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics) under *Resolved issues* in *Known issues and resolved issues*.
* Added a selectable [!UICONTROL Last Updated At] column in the [!UICONTROL Catalog Search] table and a [!UICONTROL Last Updated At] filter. This enhancement saves time and effort because you don't have to open each individual item to see when it was last updated and you can filter by date the items were last updated.

  ![Last Updated at column and filter illustration](/help/r-release-notes/assets/column-and-filter.png)

* Updates were made to help make the Target UI compliant with [Web Content Accessibility Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/) 2.0 Level A and AA Success Criteria (WCAG 2.0 AA). (TGT-34384 & TGT-24679)
* Made Content Security Policy (CSP) improvements. (TGT-37035)
* Introduced a way to specify the client code as a parameter for customers using CNAME. (TNT-38571)


## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
