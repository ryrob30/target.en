---
keywords: traffic estimator;automated personalization;ap
description: The Traffic Estimator provides feedback that lets you know whether you have sufficient traffic for your Adobe Target activity to succeed.
title: Estimate the traffic required for success
feature: ap
topic: Standard
uuid: 9961ebaa-8761-431d-9605-852025ca580f
---

# ![PREMIUM](/help/assets/premium.png) Estimate the traffic required for success{#estimate-the-traffic-required-for-success}

The [!UICONTROL Traffic Estimator] provides feedback that lets you know whether you have sufficient traffic for your [!DNL Adobe Target] activity to succeed.

Because an [!UICONTROL Automated Personalization] activity uses multiple offer combinations, it is important to know how much traffic is required to provide meaningful results. The [!UICONTROL Traffic Estimator] uses statistics about your page and the number of experiences being tested to estimate the amount of traffic and the test duration needed to make the activity successful.

The [!UICONTROL Traffic Estimator] determines if there is enough traffic to generate personalized models, by comparing the estimated page impressions and typical conversion rate for the pages. Ideally, for a successful activity, the correct sample size ensures that personalized content is ready within 50% of the activity duration or 14 days, whichever is less. This allows sufficient time for obtaining personalized content and learning which content to deliver.

Remember that [!DNL Target] randomly serves experiences until the personalization algorithms are built. The checkmark icon beside each offer shows when the model for that offer is ready and [!DNL Target] is able to begin delivering personalized content. Because lift is expected only after the models are ready, the visual indication allows you to set the right expectation. Use the [!UICONTROL Traffic Estimator] in the [!UICONTROL Visual Experience Composer] (VEC) to get a guideline of when the models will be ready.

## Use the Traffic Estimator

1. From the [!UICONTROL Visual Experience Composer], click **[!UICONTROL Traffic]**.

   ![Traffic icon](/help/c-activities/t-automated-personalization/assets/icon-traffic.png)

   The [!UICONTROL Traffic Estimator] opens. You can click **[!UICONTROL Traffic]** again to hide the [!UICONTROL Traffic Estimator].

   ![](assets/ap_est.png)

1. Provide the typical conversion rate (or the conversion rate you expect from this activity), estimated activity impressions per day, and test duration.

   * **Number of Offers**: Calculated automatically based on the number of experiences being created as a part of your activity after any exclusions. 
   * **Typical Conversion Rate**: The conversion rate is expressed as a percentage, based on your estimation or past data from your analytics system. 
   * **Estimated Visits Per Day**: This is the number of visits per day from visitors who are able to view the activity, based on the targeting criteria. This could be based on your analytics data. Note this number should be visits, not unique visitors. 
   * **Test Duration**: The number of days you want the activity to run.

   The [!UICONTROL Traffic Estimato]r uses these statistics to determine what adjustments are needed to run a successful test.

   Near the top of the [!UICONTROL Traffic Estimator], the values you entered are calculated and the results are shown.

   ![](assets/ap_est_no.png)

   As you change the numbers, the estimate changes. For example, if you are testing a large number of combinations and your conversion rate and impressions are too low, the [!UICONTROL Traffic Estimator] shows how long the test will need to run to be successful. Or, if your traffic is low, the [!UICONTROL Traffic Estimator] might suggest a lower number of offer combinations so you can run the test the desired number of days.

   If you do not have sufficient traffic, you can do one or all of the following:

   * Consider using an [Auto-Target](/help/c-activities/auto-target-to-optimize.md) activity instead of [!UICONTROL Automated Personalization] to create experiences with several offer changes in one experience variation. 
   * Reduce the number of offer combinations within your [!UICONTROL Automated Personalization] activity. 
   * Increase the duration of the activity.

   Adjust the numbers until the [!UICONTROL Traffic Estimator] says you have sufficient traffic, then design your test accordingly.

   ![](assets/ap_est_yes.png)

   If the traffic is sufficient, the [!UICONTROL Traffic] icon shows a green check. If it is insufficient, the icon shows a red warning label.

## Frequently Asked Questions about the Traffic Estimator

Consider the following FAQs as you work with the [!UICONTROL Traffic Estimator]:

### Why is [!DNL Target] not building personalized models when my AP activity has enough traffic?

In certain circumstances, your traffic might be large enough for a personalized model to be built, but that traffic might inform [!DNL Target] that there is no meaningful difference between the personalized model and random. Although the model is built in [!DNL Target] and tested, it will not be deployed because the model is not significantly better than random.

A possible reason for the model not being better than random might be that the offers are not significantly different from each other. If this is the case, you can try increasing the differences in the offers by making them more visually different or by changing the content itself.
