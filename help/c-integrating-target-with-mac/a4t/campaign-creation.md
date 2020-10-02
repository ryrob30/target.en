---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: You can configure an activity in Target Standard/Premium to use Adobe Analytics as the reporting source (A4T).
title: Activity creation
feature: a4t general
topic: Advanced,Standard,Classic
uuid: b04ad535-62fb-4dd3-ab3f-23da60fbffbd
---

# Activity creation{#activity-creation}

You can configure an activity in [!DNL Target] to use [!DNL Adobe Analytics] as the reporting source (A4T).

Before you set up an activity that uses [!DNL Analytics] as the reporting source, establish the goal for the activity, such as improving revenue per visitor (RPV) or increasing clicks on your shopping cart. Choose a final success metric for the activity. Although you can select additional metrics at any time in [!DNL Analytics], you must still specify a particular metric you expect this test to affect.

## Create an activity that uses Analytics as the reporting source

Creating a [!DNL Target] activity that uses [!DNL Analytics] as the reporting source is similar to setting up a regular [!DNL Target] activity, with a few important differences. For example, you cannot select a segment for reporting while creating the activity because all segments available in [!DNL Analytics] can be applied when viewing a report. 

1. Click **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >An activity name cannot include the "%" character if [!DNL Analytics] is used as the reporting source.

1. Select the activity type and begin setting up the activity.
1. When you get to the **[!UICONTROL Settings]** portion of the activity creation flow, choose **[!UICONTROL Adobe Analytics]** and specify your company.
1. Select a report suite.

   You can choose any report suite that is available to you in [!DNL Analytics]. The report suite defines where the collected data will be available. Virtual report suites are not included in the report suite list.

   You might encounter two possible errors while selecting the report suite:

   * You get an error that no report suites are available, but your account is properly set up.

     You might need to check your [!DNL Analytics] company. If your [!DNL Adobe Experience Cloud] account is tied to more than one [!DNL Analytics] company, log out of [!DNL Target], and log in to [!DNL Analytics] under the right company. Then return to [!DNL Target], and the report suites will load. 

   * You don't see the report suite that you expect.

     Only report suites that are provisioned to connect to [!DNL Target] will be available for selection. If you don't see the report suite(s) you expect, first try logging out and logging back in to the [!DNL Adobe Experience Cloud] to try again.

   If the report suite(s) is still missing from the list, please [contact Customer Care](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Specify your tracking server.

   See [Using an Analytics Tracking Server](../../c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Define the experience.
1. Specify the activity goal.

   You are required to select a success metric to use as a goal for each activity. Your activity goal is the conversion activity that signals a successful activity. It is best practice never to run a test without having a goal to improve in some specific way. You can choose any [!DNL Analytics] metric available in the [!DNL Analytics] metric selector.

   >[!NOTE]
   >
   >You can send a custom Target-based metric to [!DNL Analytics] rather than relying only on [!DNL Analytics] data. For example, you can monitor clicking on a page, which is usually not tracked by [!DNL Analytics]. This custom metric is sent to [!DNL Analytics] automatically from the [!DNL Target] server, and appears as the "[!DNL Target] Conversion" metric in the metrics selector in [!DNL Analytics]. The [!DNL Target] Conversion metric is empty if you choose to use [!DNL Analytics] metrics.

   Setting a goal doesn't mean you can't use another metric when evaluating test results. The goal is, however, a reminder of the one thing you want to improve with the activity.

   The visitor remains in the activity after they reach the goal. The visitor continues to see activity content but is not counted as a new activity entry.

   >[!NOTE]
   >
   >When setting up an activity after setting up [!DNL Analytics] as your reporting source, there is no option to set up audiences for reporting. [!DNL Analytics] segments are available in the [!DNL Target] Activities report.

1. Click **[!UICONTROL Save]**.

## Analytics for Target (A4T) support for Auto-Allocate and Auto-Target activities {#a4t-aa}

We’ve upgraded the Adobe Target-to-Adobe Analytics integration, known as [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md). Auto-Allocate and Auto-Target activities now support Analytics for Target.

This integration allows you to:

* Use [Auto-Allocate](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)’s multi-armed bandit capability to drive traffic to winning experiences
* Use [Auto-Target](/help/c-activities/auto-target-to-optimize.md)’s ensemble machine learning algorithm to choose a best experience for each visitor based on their profile, behavior, and context

all while using an [!DNL Adobe Analytics] goal metric and [!DNL Adobe Analytics]’ rich reporting and analysis capabilities.

If you’ve already [implemented A4T for use with A/B Test and Experience Targeting activities](/help/c-integrating-target-with-mac/a4t/a4timplementation.md), there’s no additional setup required, you’re ready to go!

To get started:

1. While creating an A/B Test activity, on the **[!UICONTROL Targeting]** page, select one of the following options as the **[!UICONTROL Traffic Allocation Method]**:

   * Auto-allocate to best experience
   * Auto-target for personalized experiences

1. Select **[!UICONTROL Adobe Analytics]** for your **[!UICONTROL Reporting Source]** on the **[!UICONTROL Goals & Settings]** page and select the report suite corresponding to your desired optimization goal.

1. Choose a Primary Goal metric.

   * Choose **[!UICONTROL Conversion]** to use [!DNL Adobe Target] to specify the optimization goal.
   * Choose **[!UICONTROL Use an Analytics metric]** and then select a metric from [!DNL Analytics] for use as the optimization goal. You can use an out-of-box [!DNL Analytics] conversion metric or an [!DNL Analytics] custom event.

1. Save and activate your activity.

   [!UICONTROL Auto-Allocate] will use your selected metric to optimize the activity, driving visitors to the experience that maximizes your goal metric.

   Or

   [!UICONTROL Auto-Target] will use your selected metric to optimize the activity, driving visitors to a personalized best experience.

1. Use the **[!UICONTROL Reports]** tab to view your activity’s reporting by your choice of [!DNL Adobe Analytics] metrics. Click **[!UICONTROL View in Analytics]** to dive deep and further segment your reporting data.

### Supported goal metrics

[!UICONTROL A4T] for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] allow you to choose any of the following metric types as your primary goal metric for optimization:

* [!DNL Adobe Target] conversion metrics
* [!DNL Adobe Analytics] conversion metrics
* [!DNL Adobe Analytics] custom events

[!UICONTROL A4T] for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] requires you to choose a metric that is based on a binomial event, that is, an event that either does or does not happen, for example a click, a conversion, an order, etc. (These types of events are also sometimes referred to as Bernoulli, binary, or discrete events.)

[!UICONTROL A4T] for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] does not support optimization for continuous metrics such as revenue, number of products ordered, session duration, number of page views in session, etc. (These unsupported types of metrics are also sometimes referred to as non-binomial or non-Bernoulli metrics.)

The following metric types are unsupported as primary goal metrics:

* [!DNL Adobe Target] engagement and revenue metrics
* [!DNL Adobe Analytics] engagement and revenue metrics

  It might be possible to select an [!DNL Analytics] engagement or revenue metric as your primary goal metric because [!DNL Target] cannot identify and exclude all engagement and revenue metrics from [!DNL Analytics]. Take caution to select only binomial conversion metrics or custom events from [!DNL Analytics].

* [!DNL Adobe Analytics] calculated metrics

### Limitations and notes

**Auto-Allocate and Auto-Target**

* The reporting source cannot be changed from [!DNL Analytics] to [!DNL Target] or vice versa after an activity has been activated.
* Although calculated metrics are not supported as primary goal metrics, it is often possible to achieve the intended result by instead selecting a custom event as the primary goal metric. For example, if you want to optimize for a metric such as "form completions per visitor," select a custom event corresponding to "form completions" as your primary goal metric. [!DNL Target] automatically normalizes conversion metrics on a per-visit basis to account for uneven traffic distribution, so it is not necessary to use a calculated metric to perform normalization.
* [!DNL Target] uses the "Same Touch" attribution model in the [!UICONTROL Auto-Allocate] A4T implementation.

**Auto-Allocate**

* [!UICONTROL Auto-Allocate] models continue to train every two hours, as usual.

**Auto-Target**

* [!UICONTROL Auto-Target] models continue to train every 24 hours, as usual. However, conversion event data coming from [!DNL Analytics] is delayed by an additional six to 24 hours. This delay means the distribution of traffic by [!DNL Target] will trail the latest events recorded in [!DNL Analytics]. This will have the largest effect in the first 48 hours after an activity is first activated; the activity’s performance will more closely mirror [!DNL Analytics] conversion behavior after five days have elapsed. You should consider using [!UICONTROL Auto-Allocate] instead of [!UICONTROL Auto-Target] for short-duration activities where most traffic occurs within the first five days of the activity’s life.
* When using [!DNL Analytics] as the data source for an [!UICONTROL Auto-Target] activity, sessions are considered to be ended after six hours have elapsed. Conversions occurring after six hours will not be counted.

For more information, see [Attribution models and lookback windows](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/models.html) in the *Analytics Tools Guide*.
