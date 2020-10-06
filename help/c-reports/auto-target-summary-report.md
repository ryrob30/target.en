---
keywords: reports;auto-target;auto target;AT;report
description: Information about how to interpret the Auto-Target Summary report in Adobe Target.
title: Auto-Target Summary report
feature: reports
subtopic: Multivariate Test
topic: Standard
uuid: a30fa886-e8df-408f-bbc9-11a917a592d8
---

# ![PREMIUM](/help/assets/premium.png) Auto-Target Summary report{#auto-target-summary-report}

Information about how to interpret the [!UICONTROL Auto-Target Summary] reports in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Auto-Target] is available as part of the [!DNL Target Premium] solution. It is not included with [!DNL Target Standard] without a [Target Premium license](/help/c-intro/intro.md#premium).

To display the [!UICONTROL Auto-Target Summary] reports:

1. From the [!UICONTROL Activities] page, click the desired [!UICONTROL Auto-Target] activity.

   If you have many activities, you can filter the list by selecting options from the [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Property], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], and [!UICONTROL Activity Source] drop-down lists.

1. Click the [!UICONTROL Reports] tab, then click the desired icon:

   * Table View
   * Graph View
   * Automated Segments
   * Important Attributes

## Table View

The following illustration shows what a typical summary report looks like in [!UICONTROL Table View] when viewing an [!UICONTROL Auto-Target] activity's report:

![Auto-Target table view report](/help/c-reports/assets/at-table-view.png)

Some tips and considerations as you interpret your [!UICONTROL Auto-Target] reports:

* The various rows in the table help you understand activity performance.

    * The top two rows in the table on the reporting page show the results of an A/B test between the visitors who were assigned to the control (i.e. randomly served experiences) and the visitors who were assigned to the personalization algorithm. This information can be used to measure how the personalization algorithm performed compared to the randomly-served control. 
    * The remaining rows show experience-level results. For each experience, there is a comparison between the average response of visitors who were shown that experience as a randomly served control, and the average response of visitors who were shown the experience using the personalization algorithm.

* The green check icon next to each experience in the report indicates that a personalized machine-learning model has been generated for that experience. The clock icon indicates that not enough traffic has been served to build the model.

    * Because the model is built per experience, it is possible to see a model for some experiences with a green check and others with a clock icon. 
    * In this case, to increase the speed of the activity having models built for all experiences, additional traffic is sent to experiences with unbuilt models. 
    * There must be at least two experiences with built models (green checkmark) in order for personalization to begin.

* Comparing the conversion rate of experience A with that of experience B is not the right comparison in [!UICONTROL Auto-Target]. The question is whether experience A performs better when served in an intelligent way versus a random way (in other words, versus the control). Marketers should also use caution about interpreting the lifts of individual experiences because the personalization algorithm is attempting to optimize for the success metric over the entire activity, not over each individual experience. 
* Experiences with the highest lift can be understood as having the highest differentiation within the population. That is the algorithm has found a segment that likes that particular experience the most.
* The various columns in the table show the number of visits, conversion rate, average lift and confidence level, and confidence. For more information, see [Average Lift, Lift Bounds, and Confidence Interval](/help/c-reports/c-report-settings/average-lift-bounds-and-confidence-interval.md).

## Graph View

The following illustration shows what a typical summary report looks like in [!UICONTROL Graph View] when viewing an [!UICONTROL Auto-Target] activity's report:

![Auto-Target graph view report](/help/c-reports/assets/at-graph-view.png)

As shown below, you can use the two drop-down lists to choose the desired metrics, counting methodology, and more. See [Report settings overview](/help/c-reports/c-report-settings/report-settings.md) for more information:

![Auto-Target graph view report](/help/c-reports/assets/at-graph-view-2.png)

## Automated Segments

Click the [!UICONTROL Automated Segments] icon. This report shows how different visitors respond differently to the offers/experiences in your AP/AT activity. This report shows how different automated segments defined by Target's personalization models responded to the offers/experiences in the activity.

![Automated segments icon](/help/c-reports/assets/icon-automated-sements.png)

For more information, see [Automated Segments report](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Important Attributes

Click the [!UICONTROL Important Attributes] icon. This report shows how, in different activities, different attributes are more (or less) important to how the model decides to personalize. This report shows the top attributes that influenced the model and their relative importance.

![Important attributes icon](/help/c-reports/assets/icon-important-attributes.png)

For more information, see [Important Attributes report](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md).
