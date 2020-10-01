---
keywords: reports;block ip address;block visitor from ip address;download reports;csv;reporting
description: Reports provide information about the performance of your Adobe Target activities
title: Reports
feature: reports
topic: Standard
uuid: 8d20f4e7-72fd-4872-a21f-54ce16a2d2ab
---

# Reports{#reports}

Reports provide information about the progress and results of your [!DNL Adobe Target] activities that help you make decisions based on your data. Report data can help you decide when to end an activity, show you which experience of offer is the winner, and provide insights or learnings you need to determine next actions.

## Display a report {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Click **[!UICONTROL Activities]**, then click the desired activity from the list.

   If you have many activities, you can filter the list by selecting options from the [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], and [!UICONTROL Activity Source] drop-down lists.

   For example, you could select [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting] from the [!UICONTROL Type] drop-down list and [!UICONTROL Live] from the [!UICONTROL Status] drop-down list to display only A/B tests and Experience Targeting activities that are in an active state.

   The following illustration shows the [!UICONTROL Type] drop-down list with two types selected: [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting]. Note that the three types of A/B Tests (Manual, [Auto-Allocate](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), and [Auto-Target](/help/c-activities/auto-target-to-optimize.md)) are selected by default. You can deselect one or more types as needed.

   ![Filter reports by type](/help/c-reports/assets/report_filters-new.png)

1. Click the **[!UICONTROL Reports]** tab.

   Each report includes a legend to help you understand the report.

   ![Report legend](/help/c-reports/assets/report_menu_bar-new.png)

   The legend displays the following information:

    * The activity status, including the date range when the activity ran.
    * The [projected winning experience](/help/c-activities/automated-traffic-allocation/determine-winner.md) (if available). 

   >[!NOTE]
   >
   >Experience results appear after at least one entrant has seen the experience.

1. (Optional) [Configure the report](../c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA), as desired. 
1. (Optional) [Download the report in CSV format](../c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) for analysis in Excel and other tools.

   The following options are available:

    * [!UICONTROL Export Report to CSV]
    * [!UICONTROL Export Order Details to CSV]

1. (Optional) Click the **[!UICONTROL Table View]** and **[!UICONTROL Graph View]** icons to switch between reporting formats.

   ![Table and Graph view icons](/help/c-reports/assets/table-and-graph-icons.png)

   Depending on the type of report you selected, other views and reports might be available:

   |Report Type|View|
   | --- | --- |
   |[Auto-Target](/help/c-activities/auto-target-to-optimize.md)|Click the **[!UICONTROL Automated Segments]** or **[!UICONTROL Important Attributes]** icons.<ul><li>The [Automated Segments report](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) shows how different visitors respond differently to the offers/experiences in your AP/AT activity. This report shows how different automated segments defined by Target's personalization models responded to the offers/experiences in the activity.</li><li>The [Important Attributes report](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) shows how, in different activities, different attributes are more (or less) important to how the model decides to personalize. This report shows the top attributes that influenced the model and their relative importance.</li></ul>|
   |[Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP)|In addition to the [Automated Personalization Summary reports](/help/c-reports/reports-ap.md), you can click the **[!UICONTROL Automated Segments]** or **[!UICONTROL Important Attributes]** icons.<ul><li>The [Automated Segments report](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) shows how different visitors respond differently to the offers/experiences in your AP/AT activity. This report shows how different automated segments defined by Target's personalization models responded to the offers/experiences in the activity.</li><li>The [Important Attributes report](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) hows how, in different activities, different attributes are more (or less) important to how the model decides to personalize. This report shows the top attributes that influenced the model and their relative importance.</li></ul>|
   |[Multivariate Test](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT)|In addition to the [Experience Performance report](/help/c-reports/experience-performance-report.md), you can click the [Location Contribution](/help/c-reports/location-contribution-report.md) icon to switch the report to show contribution by location.|

## Additional reporting information for specific activity types {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

In addition to the general reporting information in this topic and its subtopics, additional information specific to individual activity types is available elsewhere in this guide:

| Activity Type | Details |
|--- |--- |
|[A/B Test](/help/c-activities/t-test-ab/test-ab.md)|To understand lift and confidence and the statistical approaches used in [!DNL Target], see [Plan an A/B Test](/help/c-activities/t-test-ab/sample-size-determination.md).|
|[Interpret Auto-Allocate reports](/help/c-activities/automated-traffic-allocation/determine-winner.md)|Interpret the results of an [!UICONTROL Auto-Allocate] A/B activity by examining important indicators, including lift and confidence, in the [!DNL Target] UI.|
|[Auto-Target](/help/c-activities/auto-target-to-optimize.md) (AT)|Information about the [!UICONTROL Summary] report for AT activities. For more information, see [Auto-Target Summary Report](/help/c-reports/auto-target-summary-report.md).<br>Information about the two [!UICONTROL Personalization Insights] reports for AT and AP activities: [!UICONTROL Automated Segments] report and [!UICONTROL Important Attributes] report. For more information, see [Personalization Insights Reports](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md).|
|[Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP)|Information about the two [!UICONTROL Automated Personalization Summary] reports for AP activities: [!UICONTROL Activity Level] report and [!UICONTROL Offer Level] report. For more information, see [Automated Personalization Summary Reports](/help/c-reports/reports-ap.md).<br>Information about the two [!UICONTROL Personalization Insights] reports for AT and AP activities: [!UICONTROL Automated Segments] report and [!UICONTROL Important Attributes] report. For more information, see [Personalization Insights Reports](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md).|
|[Multivariate Test](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT)|Information about the two reports for MVT activities: [!UICONTROL Experience Performance] report and [!UICONTROL Location Contribution] report. For more information, see [Experience Performance Report](/help/c-reports/experience-performance-report.md) (MVT) and  [Location Contribution Report](/help/c-reports/location-contribution-report.md) (MVT).|
|[Adobe Analytics as the Reporting Source for Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T)|Information about using [!DNL Adobe Analytics] as the reporting source for [!DNL Target]. A4T gives you access to [!DNL Analytics] reports for your [!DNL Target] activities. For more information, see [Analytics for Target (A4T) Reporting](/help/c-reports/analytics-for-target-a4t-reporting.md).|

## Block reporting data from specified IP addresses

You can block visitors from specified IP addresses from being counted in reports. This is helpful, for example, to block reporting data from your internal visitors.

[Contact Client Care](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) to set up IP filters. This filtering does not apply when using [Analytics for Target](../c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) as your reporting source.
