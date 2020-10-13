---
keywords: target documentation change log;documentation updates;new topics;edits;updates;update
description: This page lists important changes made to the Adobe Target documentation, ordered by releases.
title: Documentation changes in the Adobe Target product documentation.
feature: release notes
topic: Standard 
uuid: 6fba75e2-0a93-488d-9010-fffa423600c0
---

# Documentation changes{#documentation-changes}

This page lists important changes made to the [!DNL Adobe Target] product documentation.

## Adobe Target Standard/Premium 20.9.1 (September 30, 2020)

|Date|Topic|Changes|
| --- | --- | --- |
|October 13|[Target announcements and events](/help/r-release-notes/target-announcements.md)|Added information about the following live webinar scheduled for November 10, 2020:<ul><li>Personalize and test at zero latency with on-device decisions from Adobe Target</li></ul>|
||[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Added information about the following live webinar scheduled for November 10, 2020:<ul><li>Personalize and test at zero latency with on-device decisions from Adobe Target</li></ul>|
|October 12|[Troubleshoot content delivery](/help/c-activities/c-troubleshooting-activities/content-trouble.md)|Updated [Retrieve the authorization token to use with debugging tools](/help/c-activities/c-troubleshooting-activities/content-trouble.md#section_BED130298E794D1FA229DB7C3358BA54) to indicate the permission level you must have to generate an authentication token.|
||[Profile API settings](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/profile-api-settings.md)|Updated topic to indicate the permission level you must have to generate an authentication token.|
||[Auto-Target](/help/c-activities/auto-target-to-optimize.md)|Added real-world success story using Auto-Target.|
||[Include the same experience on similar pages](/help/c-experiences/c-visual-experience-composer/temtest.md)|Added section to explain how to render the same activity across the entire domain.|
||[Known issues and resolved issues](/help/r-release-notes/known-issues-resolved-issues.md)|Added the following known issue:<ul><li>Analytics for Target (A4T) metrics for Auto-Allocate and Auto-Target activities</li></ul>|
|October 8|[Known issues and resolved issues](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics)|Added the following resolved issue:<ul><li>[Auto-Target reporting](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics)</li></ul>Moved the following issue from the Known Issues section to the Resolved Issues section:<ul><li>[Reporting](/help/r-release-notes/known-issues-resolved-issues.md#conversions-audiences)</li></ul>|
||[Hybrid implementation](/help/c-implementing-target/hybrid-implementation.md)|New topic.|
|October 7|[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Added information about the Target Standard/Premium 20.10.1 release.|
|October 1|[Estimate the traffic required for success](/help/c-activities/t-automated-personalization/ap-traffic-estimator.md)|Added FAQ section.|
|September 30|[Target announcements and events](/help/r-release-notes/target-announcements.md)|Added information about the following live webinar:<ul><li>Adaptive, Fine-tuned Personalization at Scale with Adobe Target and Analytics</li></ul>|
||[Release Notes](/help/r-release-notes/release-notes.md): 20.9.1|This release includes enhancements and fixes. You can read about them and link to the documentation from the Release Notes. This release also includes many documentation updates throughout the help.|

## Adobe Target Standard/Premium 20.8.1 (September 2, 2020)

|Date|Topic|Changes|
| --- | --- | --- |
|September 29|[Troubleshoot the Analytics and Target integration (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md#section_75002584FA63456D8D9086172925DD8D)|Added information about how to inspect the supplemental ID in at.js 1.x and at.js 2.x.|
|September 24|[Activity QA bookmarklet](/help/c-activities/c-activity-qa/activity-qa-bookmark.md)|Updated the code for the activity QA bookmarklet for at.js 2.*x*.|
||[Catalog search](/help/c-recommendations/c-products/catalog-search.md#faq)|Added a note about searching on a custom attribute with a numeric value.|
||[Recommendations FAQ](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md)|Added the following FAQ: "Why does Catalog Search not show the correct results when I search on a custom attribute with a numeric value?"|
||[How Target works](/help/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934)|Updated the Target Cluster and Target Central Cluster locations listed in "The edge network."|
|September 23|[Use an Analytics tracking server](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md)|Updated entire topic with information from the [!DNL Adobe Experience Platform Debugger] and the browser Developer Tools.|
||[Profile and variable glossary](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md)|Updated the "user.header('x-forwarded-for')" row to indicate that "user.header('x-cluster-client-ip')" has been deprecated.|
||[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Added information about the Target Standard/Premium 20.9.1 (September 30, 2020) release.|
|September 15|[Target release notes (current)](/help/r-release-notes/release-notes.md)|Added information about the Target Standard/Premium 20.8.3 release, which includes Analytics for Target (A4T) support for Auto-Target activities. Support for Auto-Allocate activities was added in a previous release.|
||[Analytics for Target (A4T) support for Auto-Allocate and Auto-Target activities](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa).|Added information about A4T support in Auto-Target activities.|
||[Activity QA bookmarklet](/help/c-activities/c-activity-qa/activity-qa-bookmark.md)|Updated text to indicate that the method to manually force yourself out of QA mode by loading a page on your site with the `at_preview_token` parameter with an empty value applies to at.js 1.*x* only.|
||[Catalog search](/help/c-recommendations/c-products/catalog-search.md)|Updated entire topic.|
|September 10|[Target release notes (current)](/help/r-release-notes/release-notes.md)|Added information about the Target Standard/Premium 20.9.2 release that includes the following new feature: Control recommendations slots within criteria sequences.|
||[Create criteria sequences](/help/c-recommendations/c-algorithms/create-criteria-sequence.md)|Added information about "Limit the number of items returned" feature.|
|September 9|[Activity QA bookmarklet](/help/c-activities/c-activity-qa/activity-qa-bookmark.md)|Added JavaScript code for use with at.js 2.*x*.|
|September 3|[Visual Experience Composer helper extension](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)|Updated the "Obtain and install the VEC Helper browser extension" section with information about the cookie name and domain.|
||[Troubleshooting Issues Related to the Visual Experience Composer and Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md)|Updated the "How do the recently announced Google Chrome SameSite cookie enforcement policies impact the VEC and EEC?" section with information about the cookie name and domain.|
|September 2|[Release Notes](/help/r-release-notes/release-notes.md): 20.8.1|This release includes enhancements and fixes. You can read about them and link to the documentation from the Release Notes. This release also includes many documentation updates throughout the help.|

## Adobe Target Standard/Premium 20.7.1 (July 27, 2020)

|Date|Topic|Changes|
| --- | --- | --- |
|August 31|[Use Adobe Analytics with Recommendations](/help/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md)|Added FAQ section.|
|August 28|[Known issues and resolved issues](/help/r-release-notes/known-issues-resolved-issues.md)|Updated the following:<ul><li>Added to the Known issues section: "Reporting - Conversions currently increment differently based on which audience is used."</li><li>Added to the Resolved issues section: "Pages not loading in the Visual Experience Composer (VEC) or Enhanced Experience Composer (EEC) when using Google Chrome version 80+."</li></ul> |
||[Target release notes (current)](/help/r-release-notes/release-notes.md)|The deprecation date for mbox.js has been changed from August 30, 2020 to January 18, 2021.|
|August 26|[Use Adobe Analytics with Target Recommendations](/help/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md)|New topic.|
|August 24|[Success metrics](/help/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B)|Updated "Advanced settings" section.|
|August 21|[Adobe Target welcome kit overview](/help/c-intro/target-welcome-kit.md)|New article and subtopics.|
|August 20|[Troubleshooting Issues Related to the Visual Experience Composer and Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md)|Added the following section: "How do the recently announced Google Chrome SameSite cookie enforcement policies impact the VEC and EEC?"|
||[Click tracking](/help/c-activities/r-success-metrics/click-tracking.md)|Updated the following text: "If you select more than one element, if an entrant clicks on any one of the chosen elements, the click is counted. To count each item separately, set up individual success metrics for each element. To count one item by clicking on several elements on a page, edit the CSS Element Selector to match multiple elements."|
||[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Added information about the Target Standard/Premium 20.9.1 (September 2, 2020) release.|
|August 14|[Known issues and resolved issues](/help/r-release-notes/known-issues-resolved-issues.md)|Added known issue about QA in Recommendations activities.|
||[targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)|Added text indicating that if you are using `serverState` and using `<script>` tags in the content returned, ensure that your HTML content uses `<\/script>` instead of `</script>`.|
|August 12|[Understand the Target UI](/help/c-intro/understand-the-target-ui.md)|New topic.|
||[Adobe Target API overview](/help/api/api-overview.md)|New topic.|
|August 10|[CNAME and Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md)|Added text indicating that the size of the cookie header will increase when using CNAME.|
||[Integrate Target with Adobe Audience Manager](/help/c-integrating-target-with-mac/audience-manager-target-integration.md)|New topic.|
||[Target announcements and events](/help/r-release-notes/target-announcements.md)|Added link to view the following archived webinar: "How HSBC leverages Adobe Target and AI to rapidly optimize and deliver personalization at scale."|
|August 6|[Auto-Target](/help/c-activities/auto-target-to-optimize.md#how-long)|Updated text for the following FAQ: "How long should I wait for models to build?"|
||[Classifications - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-classifications.md)|Updated the text for targettype.|
|August 5|[Delete the Target cookie](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cookie-deleting.md)|Updated entire topic.|
|August 4|[Target announcements and events](/help/r-release-notes/target-announcements.md)|Added registration information about the "Personalization Strategies Using Artificial Intelligence and Adobe Target" webinar scheduled for August 13.|
||[Enabling mixed content in your browser](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/mixed-content.md)|Updated topic.|
|August 3|[Success metrics](/help/c-activities/r-success-metrics/success-metrics.md)|Added note clarifying what the [!UICONTROL Increment Count] options mean in regard to visitors vs. visits.|
|July 31|[Known issues and resolved issues](/help/r-release-notes/known-issues-resolved-issues.md)|Added new known issue: "Image Offers showing “Processing” label."|
||[adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md)|Added code sample to use `getoffers()` to perform a pageLoad. |
||[Target announcements and events](/help/r-release-notes/target-announcements.md)|Added registration information about the upcoming Adobe Target Community Coffee Break on August 5.|
|July 28|[Personalization Insights reports](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md),<br>[Automated Segments report](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md),<br>and [Important Attributes report](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md)|Updated text in the note at the top of the topics.|
||[Auto-Allocate](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)|Added the following FAQs:<ul><li>Can I use the Reset Report Data option while running an Auto-Allocate activity?</li><li>How does Auto-Allocate build models with regard to environments?</li></ul>|
||[Auto-Target](/help/c-activities/auto-target-to-optimize.md)|Added the following FAQ:<ul><li>Can I use the Reset Report Data option while running an Auto-Target activity?</li></ul>Updated text in the "Considerations" section.|
||[Automated Personalization FAQs](/help/c-activities/t-automated-personalization/automated-personalization-faq.md)|Added the following FAQs:<ul><li>Can I use the Reset Report Data option while running an Automated Personalization activity?</li><li>How does Automated Personalization build models with regard to environments?</li></ul>|
||[Supported browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md)|Added information about Internet Explorer and unknown elements.|
||[Customer attributes](/help/c-target/c-visitor-profile/working-with-customer-attributes.md)|Updated following paragraph:<br>[!DNL Adobe] does not guarantee that 100% of customer attribute (visitor profile) data from CRM databases will be onboarded to the [!DNL Experience Cloud] and, thus, be available for use for targeting in [!DNL Target]. In our current design, there is a possibility that a small percentage of data (up to 0.1% of large production batches) might not be onboarded.|
|July 27|[Administer Target](/help/administrating-target/administrating-target.md)|Updated text in all linked topics on this page to reflect the new UI changes for the [!UICONTROL Administration] pages.|
||[Target announcements and events](/help/r-release-notes/target-announcements.md)|Made the following changes: <ul><li>Added registration information for the following webinar: "How HSBC leverages Adobe Target and AI to rapidly optimize and deliver personalization at scale."</li><li>Added information about Adobe again being named a Leader in Gartner Magic Quadrant for Personalization Engines.</li></ul>|
||[Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md)|Clarified information under Step 4: Select a location.|
|July 24|<br>[at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)|Added information about at.js 2.3.2.|
||[Release Notes](/help/r-release-notes/release-notes.md): 20.7.1|This release includes enhancements and fixes. You can read about them and link to the documentation from the Release Notes. This release also includes many documentation updates throughout the help.|

## Adobe Target Standard/Premium 20.5.1 (June 17, 2020)

|Date|Topic|Changes|
| --- | --- | --- |
|July 17|[Target announcements and events](/help/r-release-notes/target-announcements.md)|Added information about the July 22 Adobe Target Coffee Break.|
|July 15|[Auto-Allocate can give you faster test results and higher revenue than a manual test](/help/c-activities/automated-traffic-allocation/faster-results-higher-revenue.md)|New topic.|
|July 14|[Auto-Allocate](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md),<br>[Auto-Target](/help/c-activities/auto-target-to-optimize.md),<br>and<br>[Automated Personalization FAQ](/help/c-activities/t-automated-personalization/automated-personalization-faq.md)|Added FAQs recommending that you should not change the goal metric midway through an activity.|
|July 7|[Target announcements and events](/help/r-release-notes/target-announcements.md)|Added information about the July 8 Adobe Target Coffee Break.|
|June 25|[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Added information about the Target Standard/Premium 20.6.1 release (July 2020).|
||[Target documentation overview](/help/r-release-notes/target-documentation.md)|New topic detailing the different sources of [!DNL Target] documentation.|
|June 23|[Target announcements and events](/help/r-release-notes/target-announcements.md)|Added information about the June 24 Adobe Target Coffee Break.|
||[Profile attributes](/help/c-target/c-visitor-profile/profile-parameters.md)|Added note that creating dependent profile scripts that use the result of one profile script in another profile script is not recommended.|
||[How at.js works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)|Added the following video: Office hours: at.js tips and overview|
|June 17|[CNAME and Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md)|Updated topic.|
||[Response tokens](/help/administrating-target/response-tokens.md)|Added information about response tokens for Traffic Allocation Method for [!UICONTROL Auto-Target] and [!UICONTROL Automated Personalization] activities.|
||[Activity creation](/help/c-integrating-target-with-mac/a4t/campaign-creation.md)|Added information about Analytics for Target (A4T) support for Auto-Allocate activities.|
||[Users](/help/administrating-target/c-user-management/c-user-management/user-management.md)|Added information about the new [!UICONTROL Publisher] role under *Specify roles and permissions*.|
||[Configure enterprise permissions](/help/administrating-target/c-user-management/property-channel/properties-overview.md)|Added information about the new [!UICONTROL Publisher] role under *Step 6: Specify roles and permissions*.|
||[Enterprise user permissions](/help/administrating-target/c-user-management/property-channel/property-channel.md)|Added link to the *Office hours: Target Premium Workspaces session*.|
||[Release Notes](/help/r-release-notes/release-notes.md): 20.5.1|This release includes enhancements and fixes. You can read about them and link to the documentation from the Release Notes. This release also includes many documentation updates throughout the help.|

## Adobe Target Standard/Premium 20.4.1 (May 6, 2020)

|Date|Topic|Changes|
| --- | --- | --- |
|June 15|[Target release notes (current)](/help/r-release-notes/release-notes.md)|Added information about the at.js 1.8.2 and at.js 2.3.1 releases.|
||[at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)|Added information about the at.js 1.8.2 and at.js 2.3.1 releases.|
||[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Updated the notes for the [!DNL Target Standard/Premium] 20.5.1 release (June 17, 2020) to include information about A4T support in [!DNL Analysis Workspace].|
|June 12|[targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)|Added information about the `deviceIdLifetime` setting.|
||[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Added information about the at.js 1.8.2 and at.js 2.3.1 releases.|
|June 8|[Target for mobile apps FAQ](/help/c-target-mobile-app/target-for-mobile-apps-faq.md)|Updated text for the following FAQ: "Is Target Mobile a functionality of Adobe Target Premium Product SKU only?"|
||[View reports - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md)|Updated entire topic.|
|June 5|[Target announcements and events](/help/r-release-notes/target-announcements.md)|Added information about the June 10 Adobe Target Coffee Break.|
||[Lift and confidence - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-lift-and-confidence.md)|Updated text for the following FAQ: "Why can't I see lift and confidence on calculated metrics?"|
|June 4|[A4T reporting](/help/c-integrating-target-with-mac/a4t/reporting.md)|Updated the "Reports in Analytics" section.|
|June 1|[Target announcements](/help/r-release-notes/target-announcements.md)|Added new page to announce upcoming Target events.|
||[Mobile Viewports for Responsive Experiences](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md)|Updated viewport dimensions and resolutions for Apple iPhone 11, Apple iPhone SE, and Google Pixel 2 XL models.|
|May 28|[Reporting FAQ](/help/c-reports/reporting-frequently-asked-questions.md)|Added the following new FAQ: <ul><li>How are the New Visitors and Returning Visitors metrics counted?</li></ul>|
|May 27|[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Added information about Analytics for Target (A4T) support for Auto-Allocate activities.|
|May 26|[Profile attributes](/help/c-target/c-visitor-profile/profile-parameters.md)|Added following information: "The parameter remains in the profile after disabling the script. Users whose profiles already contain a parameter that is used in an activity's audience will qualify in that activity."|
|May 21|[Allowlist Target edge nodes](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md)|Added `mboxedge30.tt.omtrdc.net` to the list.|
|May 20|[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Added information about the upcoming Target Standard/Premium 20.6.1 (June 10, 2020) release.|
||[Hosts](/help/administrating-target/hosts.md)|Added note to the "Security best practices" section.|
|May 14|[Target release notes (current)](/help/r-release-notes/release-notes.md)|Added information about Profile Batch Status API v2 changes.|
|May 13|[CNAME and Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md)|Added "Known limitations" section.|
|May 11|[Hosts](/help/administrating-target/hosts.md)|Added information about using the ubox functionality with redirects and allowlists.|
||[Work with redirectors](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md)|Added information about using hosts to avoid Open Redirect Vulnerabilities.|
||[Integrate Recommendations with email](/help/c-recommendations/c-recommendations-faq/integrating-recs-email.md)|Added information about using hosts to avoid Open Redirect Vulnerabilities.|
||[Email: implement Target](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md)|Added information about using hosts to avoid Open Redirect Vulnerabilities.|
||[Activity QA](/help/c-activities/c-activity-qa/activity-qa.md)|Updated the "Considerations" section.|
||[targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)|Updated "overrideMboxEdgeServer" row under "Settings."|
|May 6|[Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md)|Added information about ITP 2.3.|
||[Release Notes](/help/r-release-notes/release-notes.md): 20.4.1|This release includes enhancements and fixes. You can read about them and link to the documentation from the Release Notes. This release also includes many documentation updates throughout the help.|

## Adobe Target Standard/Premium 20.2.1 (February 19, 2020)

|Date|Topic|Changes|
| --- | --- | --- |
|May 4|[Reporting FAQ](/help/c-reports/reporting-frequently-asked-questions.md#uneven)|Added new FAQ: "Why is the traffic split between my experiences uneven in my A/B or MVT activity?"|
|April 29|[Known issues and resolved issues](/help/r-release-notes/known-issues-resolved-issues.md)|Added known issue for reporting with extreme orders.|
|April 28|[Profile and variable glossary](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md)|Removed information about using `user.header('x-forwarded-for')` with newer AWS edges to retrieve users' IP addresses. This command now works with newer AWS edges.|
||[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Changed date of the Target Standard/Premium release (20.4.1) to May 6.|
|April 23|[CNAME and Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md)|Updated topic.|
|April 22|[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Added new section: *Profile Batch Status API v2 changes (May 4, 2020).*|
|April 14|[Allowlist Target edge hosts](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md)|New topic.|
|April 10|[Single Page Application implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md#bp)|Added new section: "Implementation best practices."|
|April 7|[Lift and confidence - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-lift-and-confidence.md#lift-condidence)|Updated text for "Why can't I see lift and confidence on calculated metrics?"|
|April 2|[Profile and variable glossary](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md)|Added information about using `user.header('x-forwarded-for')` with newer AWS edges to retrieve users' IP addresses.|
||[Upgrading from at.js 1.*x* to at.js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md)|Added following note:<ul><li>After installing the ECID library v4.3.0+ and at.js 2.*x*, you will be able to create activities that span unique domains as well as track users. It is important to note that this functionality works only after the session expires.</li></ul>|
|March 30|[Known issues and resolved issues](/help/r-release-notes/known-issues-resolved-issues.md#atjs)|Added a known issues that affects at.js versions prior to at.js 2.2.0. This issue caused click tracking to not report conversions in Analytics for Target (A4T) when Adobe Analytics code was not present on page elements.|
||[at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)|Added the following information to at.js version 2.2.0 details:<ul><li>Fixed an issue that caused click tracking to not report conversions in Analytics for Target (A4T) when Adobe Analytics code was not present on page elements.</li></ul>|
|March 25|[at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)|Added information about the following new versions of at.js:<ul><li>at.js version 2.3.0</li><li>at.js version 1.8.1</li></ul>|
||[targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)|Added the following new rows in the "Settings" section:<ul><li>cspScriptNonce</li><li>cspStyleNonce</li></ul>Added the following new section:<ul><li>Content Security Policy</li></ul>|
|March 24|[Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md#impact)|Added information about impacts for the following:<ul><li>Profile scripts based on 3rdPartyID</li><li>QA/Preview URLs in iOS devices</li></ul>|
|March 20|[Release notes (current)](/help/r-release-notes/release-notes.md)|Indicated that the Target Standard/Premium 20.2.1 release will be March 23, 2020.|
|March 13|[Limits](/help/r-troubleshooting-target/target-limits.md)|Udated the number of "Audiences, reusable per account."|
|March  12|[Release Notes (current)](/help/r-release-notes/release-notes.md#summit)|Added registration information for free access to the online, digital Summit conference.|
|March 9|[Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md)|Added more information in the "Replacement of last octet of IP addresses" section.|
||[Work with multi-value attributes](/help/c-recommendations/c-algorithms/work-with-multi-value-attributes.md)|Updated code sample in *Pass a multi-value parameter in JavaScript*.|
||[Custom entity attributes](/help/c-recommendations/c-products/custom-entity-attributes.md)|Added code sample in *Using APIs* under *Implementing multi-value attributes*.|
|March 4|[Profile attributes](/help/c-target/c-visitor-profile/profile-parameters.md)|Updated entire topic, with extensive revisions to the "Best practices" section.|
|February 21|[Release notes (current)](/help/r-release-notes/release-notes.md)|Added information about the new Adobe Experience Cloud navigation.|
|February 20|[targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)|Updated the description for the `enabled` setting. Added information for the following settings: `pageLoadEnabled` and `viewsEnabled`.|
||[Geo](/help/c-target/c-audiences/c-target-rules/geo.md)|Added note that `mboxOverride.browserIp` is supported in at.js 1.*x* only.|
||[at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)|Clarified text explaining which versions of at.js the Target team supports.|
||[Release Notes](/help/r-release-notes/release-notes.md): 20.2.1|This release includes enhancements and fixes. You can read about them and link to the documentation from the Release Notes. This release also includes many documentation updates throughout the help.|

## Adobe Target Standard/Premium 20.1.1 (February 4, 2020)

|Date|Topic|Changes|
| --- | --- | --- |
|February 4|[Release Notes](/help/r-release-notes/release-notes.md): 20.1.1|This release includes enhancements and fixes. You can read about them and link to the documentation from the Release Notes. This release also includes many documentation updates throughout the help.|
