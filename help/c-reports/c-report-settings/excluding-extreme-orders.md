---
keywords: Target;reports;report settings;extreme orders;extreme values
description: You can exclude extreme values from affecting reports in Adobe Target so a few unusual orders don't affect your activity results. An example of an unusual order might be a coach buying uniforms for an entire team instead of individual shoppers buying individual uniforms.
title: Exclude extreme values in Adobe Target reports
feature: report settings
uuid: bb151b54-09ef-40b5-bc04-95c61b761f5a
---

# Exclude extreme values

You can exclude extreme values from affecting reports in [!DNL Adobe Target] so a few unusual orders don't affect your activity results. An example of an unusual order might be a coach buying uniforms for an entire team instead of individual shoppers buying individual uniforms.

>[!NOTE]
>
>The [!UICONTROL Exclude Extreme Values] flag applies to activities with [!UICONTROL Revenue] and [!UICONTROL Engagement] metric types only.

Extreme values are automatically flagged based on the rules described below. You can toggle between seeing and excluding the extreme values from your reports. An activity will have its extreme values excluded after the activity has run for an hour or after 15 orders, whichever comes first.

A value is considered extreme if it is more than +/- 3 standard deviations from the average order value using the last month of data (up to the point in time in which the calculation was made).

For example, the extreme value filter is often useful when using RPV. RPV combines conversion rate and average order value, and often exposes the volatility of those metrics. If you use RPV and determine that orders don't appear to be distributed normally, you might see more normal results if you apply the extreme order filter.

When a value is marked extreme, its order value is replaced with the average order value of the experience for the last month, excluding the extremes. The order is also marked as extreme in the [!UICONTROL Order Details] report and in the CSV download for daily results.

**To exclude extreme values from your reports:** 

1. Open an activity that includes Revenue or Engagement metric types, then click the **[!UICONTROL Reports]** tab.
1. Click the gear icon to display the **[!UICONTROL Settings]** dialog box.

   ![Step Result](assets/exclude_extreme_values.png)

1. Slide the **[!UICONTROL Exclude Extreme Values]** toggle to the "on" or "off" position, as desired.
1. Click **[!UICONTROL Save]**.
