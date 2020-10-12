---
keywords: Recommendations;offer;preview;launch;status;criteria;algorithm
description: After you’ve created your Recommendations, A/B Test, or Experience Targeting (XT) activity containing Adobe Target Recommendations offers, you’ll want to preview it to ensure results are available before launching the activity. Target Recommendations offers multiple ways to preview your recommendations. 
title: After you’ve created your Recommendations, A/B Test, or Experience Targeting (XT) activity containing Adobe Target Recommendations offers, you’ll want to preview it to ensure results are available before launching the activity. Target Recommendations offers multiple ways to preview your recommendations. 
feature: recs creation
subtopic: Recommendations
---

# Preview and launch your Recommendations activity

After you’ve created your [!UICONTROL Recommendations], [!UICONTROL A/B Test], or [!UICONTROL Experience Targeting] (XT) activity containing [Recommendations offers](/help/c-recommendations/recommendations-as-an-offer.md), you’ll want to preview your recommendations to ensure that results are available before launching the activity. [!DNL Target Recommendations] offers multiple ways to preview your recommendations.

## Checking Recommendations algorithm status

After creating an activity, [!DNL Recommendations] runs an algorithm to generate recommendations. This algorithm might take a few hours to run.

You can check whether the algorithm has finished running in the [!UICONTROL Activity] overview diagram, where the criteria status is listed. The following illustration shows the status in the activity diagram on a [!DNL Recommendations] activity's [!UICONTROL Overview] page:

![Recommendations activity Overview page](/help/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

The following illustration depicts the status on an [!UICONTROL A/B Test] or XT activity’s [!UICONTROL Overview] page:

![A/B Test Overview page](/help/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

Status results include the following, as illustrated below:

* [!UICONTROL Results Ready]: Indicates the algorithm has returned results
* [!UICONTROL Results Not Ready]: Indicates the algorithm has not finished running.
* [!UICONTROL Feed Failure]: Indicates the custom criteria feed file could not be retrieved.

![Results dialog box](/help/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## How long will the algorithm take to run?

After saving an activity containing a criteria, [!DNL Target] computes recommendations based on the selected collection, criteria, design, and promotions. This computation takes some time to perform and the time-frame differs based on the selected recommendation logic, data range, number of items in your catalog, amount of behavioral data your customers have generated, and the selected behavioral data source.

The behavioral data source has the largest impact on processing time, as follows:

### mboxes

If mboxes is selected as the behavioral data source, once created, the criteria immediately runs. Depending on the amount of behavioral data used and the size of the catalog, the algorithm can take up to 12 hours to run. Making changes to the criteria configuration generally results in the algorithm re-running. Depending on the change made, the previously computed recommendations might not be available until a re-run is complete, or for larger changes, only backup or default content is available until a re-run is complete. If an algorithm is not modified, it is automatically re-run by [!DNL Target] every 12-48 hours, depending on the selected data range.

### Adobe Analytics

If the criteria uses [!DNL Adobe Analytics] as the behavioral data source, once created, the time for criteria availability depends on whether the selected report suite and lookback window has been used for any other criteria.

* **One-time report suite setup**: The first time a report suite is used with a given data range lookback window, [!DNL Target Recommendations] can take from two to seven days to fully download the behavioral data for the selected report suite from [!DNL Analytics]. This timeframe is dependent on the [!DNL Analytics] system load.
* **New or edited criteria using an already available report suite**: When creating a new criteria or editing an existing criteria, if the selected report suite has already been used with [!DNL Target Recommendations], with a data range equal to or lesser than the selected data range, the data is immediately available and no one-time setup is required. In this case, or if an algorithm's settings are edited while not modifying the selected report suite or data range, the algorithm runs or re-runs within 12 hours.
* **Ongoing algorithm runs**: Data flows from [!DNL Analytics] to [!DNL Target Recommendations] on a daily basis. For example, for the [!UICONTROL Viewed Affinity] recommendation, when a user views a product, a product-view tracking call is passed into [!DNL Analytics] close to real-time. The [!DNL Analytics] data is pushed to [!DNL Target] early the next day and [!DNL Target] runs the algorithm in fewer than 12 hours.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] requires no offline algorithm run and results are instantly available. [!UICONTROL Top Viewed] and [!UICONTROL Top Sellers] algorithms based on mbox data generally produce results very quickly due to the simpler computation required. These can be good options when you want to preview a design change or confirm that behavioral data are being collected correctly.

## Using QA links to preview Recommendations

After the algorithm has results ready, you can preview those results using the [QA link](/help/c-activities/c-activity-qa/activity-qa.md) functionality of [!DNL Adobe Target]. QA links are available in the [!UICONTROL Activity QA] section of the Activity overview page:

![Activity QA link](/help/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>By default, [!DNL Target] automatically adds you to the required audience for the QA link. If this setting is turned off and your activity has targeting rules, your user profile needs to meet those targeting rules to see the experience containing recommendations.

Using a QA link allows you to preview the recommendations on your page:

![Featured products](/help/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* Target QA mode is “sticky” and saved in a cookie. If you do not exit QA mode, you’ll keep seeing the QA results throughout the site. To exit QA mode, use the [bookmarklet](/help/c-activities/c-activity-qa/activity-qa-bookmark.md).
>
>* While in QA mode, browsing the site will not affect your profile’s [!UICONTROL Recently Viewed Items] or [!UICONTROL Recently Purchased Items]." This behavior occurs by design to avoid unintentional pollution of production behavioral data. To preview results from a [!UICONTROL Recently Viewed Items] or [!UICONTROL User-Based Recommendations] criteria, first browse the site outside of QA mode, then use the same session to open a QA mode link.

## Using the CSV download to preview recommendations

In some cases, you might want to audit the specific items that are recommended. This is particularly helpful when using algorithms like [!UICONTROL People Who Viewed This, Viewed That], where a different set of items are recommended depending on the item the user is currently viewing, and you might have thousands or millions of different items in your catalog.

Results are not available for download until a [!UICONTROL Results Ready] status is shown for at least one algorithm in the activity.

To download results for preview, click the menu icon in the upper-right hand corner of the Activity overview page, then click **[!UICONTROL Download data]**.

![Download data option](/help/c-recommendations/t-create-recs-activity/assets/download-data.png)

A CSV file is download. Open it to see the recommended items:

![Recommended items CSV file](/help/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

From left to right is a list of recommended items, in this case the most frequently viewed. The recommendations are separated by environment, in this case only the Production environment has recommendations. For this algorithm, we have not applied any restrictions based on key value, so the row labeled with an asterisk (*) contains the complete set of recommendations. For other algorithm types based on a key value, such as [!UICONTROL People Who Viewed This, Viewed That], the key values (i.e. the “This” items) are listed in the left-most column and the recommended items (i.e. the “That” items) are listed left-to-right in the Recommendation_X columns.

>[!NOTE]
>
>Results downloads are not available for activities containing a [!UICONTROL User-Based Recommendations] algorithm. Results downloads are not available for criteria using the [!UICONTROL Recently-Viewed Items] recommendation logic.

## Activating your Recommendations activity

From the [!UICONTROL Activity Overview] tab, click the drop-down arrow next to the status, then select **[!UICONTROL Activate]**.

![Activate option](/help/c-recommendations/t-create-recs-activity/assets/activate.png)

Note that the status becomes [!UICONTROL Activating]:

![Activating](/help/c-recommendations/t-create-recs-activity/assets/activating.png)

After a few seconds to a couple of minutes, the status switches to [!UICONTROL Live]:

![Live](/help/c-recommendations/t-create-recs-activity/assets/live.png)

Note that you can also deactivate or archive the activity using the same drop-down list.

## Avoiding disruptions when changing Recommendations settings

Changing [!DNL Recommendations] collections, criteria, promotions, or design settings in a live activity might result in the algorithm results becoming invalid and the status of an algorithm changing to [!UICONTROL Results Not Ready].

To avoid disrupting a live activity, we recommend taking the following approach when modifying a live activity:

1. Duplicate the activity and criteria you want to modify.
1. Make changes to the duplicated activity and criteria and wait for the algorithm to generate results.
1. Preview the new, modified activity and confirm that results are as desired.
1. Activate the new activity.
1. Deactivate the old activity.

If you need to retain historical reporting results in the same activity, an alternative approach is possible, which might result in a temporary disruption to recommendations availability:

1. Duplicate the activity and criteria you want to modify.
1. Make changes to the duplicated activity and criteria and wait for the algorithm to generate results.
1. Preview the new, modified activity and confirm that results are as desired.
1. Pause the existing activity and swap the settings/criteria to the new criteria.
1. Preview the existing activity and confirm that results are as desired.
1. Re-activate the activity.
