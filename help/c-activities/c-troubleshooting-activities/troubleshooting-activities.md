---
keywords: troubleshoot target;troubleshooting target;default content;test not live;activity not live;targeting not working;previous experience displays;cannot create activities;can't create activities;create activities;page structure changed;page structure modified;error message;error delete profile script;ajax not working
description: If your activity does not appear on your site, these troubleshooting suggestions should help you find your solution.
title: Troubleshoot activities
feature: activities
topic: Advanced,Standard,Classic
uuid: 5b22c369-0efc-48c0-a0dc-0179b18536fe
---

# Troubleshoot activities{#troubleshoot-activities}

If your activity does not appear on your site, these troubleshooting suggestions should help you find your solution.

>[!NOTE]
>
>In addition to the following troubleshooting information, see [Troubleshooting Target](../../r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) for links to additional troubleshooting topics, FAQs, and other useful information about troubleshooting activities and other features in [!DNL Adobe Target].

The following sections contain problems you might encounter with suggested solutions.

## I created an activity using the Target UI and I cannot update it via API.

Activities created using the Target UI should be updated via the Target UI. Activities created via API should be updated via API. If you originally create an activity using the API, for example, but then later edit the activity via the Target UI, not all of the changes are updated. All of the changes are stored on the backend and can be updated by making another API call.

As best practice, try updating the activity using the same method (UI or API) that was used to originally create the activity.

## You are seeing default content.

Make sure your activity is complete and has been activated.

## Activity is not live.

**Validate:** Go to overview tab and see if test is marked inactive or draft.

**Options:**

* Activate test.  
* Use Preview Links to display inactive test.

## You don't qualify for the audience targeting conditions.

**Validate:** Review targeting conditions on overview page.

**Options:**

* Qualify and try again.
* Use Preview Links to bypass targeting conditions.

## The page doesn't qualify for the page targeting conditions.

**Validate:** On the overview page, determine if the page falls outside of the targeting conditions.

**Options:**

* Go to the Visual Experience Composer, click URL\> Advanced\>current page.

## A previous experience displays rather than the new experience.

**Validate:** Try one of the options below and attempt to view the experience again.

**Options:**

* Clear cache and cookies, then try again.

* Try a different browser.
* Use Private/Incognito mode.

## You were recently added to Target but cannot create activities.

**Validate:** Click Create Activity. If the option is not available, you most likely have not been given sufficient rights to create an activity.

**Options:**

Once you are added as a user in Target you need to have the Approver role in order to create Activities.

* Ask the Admin of your account to make you an Approver.
* If you are the Admin, give yourself the Approver role from **[!UICONTROL Administration]** > **[!UICONTROL Users]** in Target. 

  See [Assign Yourself the Approver Role](../../administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## The structure of the page changed since setting up activity.

**Validate:** Go to the Visual Experience Composer for the existing activity. Look for warning message indicating that the selectors (or structure) has changed.

**Options:**

* Rebuild the activity.

For more information about how page modifications affect Target's ability to display, see [Page Modification Scenarios](../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## The structure of the page is modified during page load (at run time).

**Validate:** Ask developer.

**Note:** In order for Target to recognize where activity changes should be applied, avoid dynamically inserting an elements with the same class or dynamically modifying the class of any siblings.

**Options:**

* Update page code to uniquely identify each element that will be tested (using an id).
* Stop dynamically modifying the class or siblings as described above.

For more information about how page modifications affect Target's ability to display, see [Page Modification Scenarios](../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Mbox.js is popping all subsequent code out of the head and into the body.

**Validate:** View source to determine if an declarations follow the mbox.js file before the closing `</body>` tag.

**Options:**

* Place mbox.js as the last item inside the `<head>` section of your page.
* Use unique div ids on the highest-level elements inside the body.

## Other activities are running on the same page.

**Validate:** Use the Collisions tab to see of other activities are running.

**Note:** The Collisions tab does not work with the Template Testing module.

**Options:**

* Increase the priority of this activity.
* Decrease the priority of other activities.
* Deactivate other activities.

## An error message appears when you delete a profile script.

**Validate:** Deleting a profile script from Target Standard/Premium displays the error message, "Failed to delete profile script."

**Options:**

Do one of the following:

* Delete again. The success message appears.
* Wait about 10 minutes for the Target Standard/Premium importer to run. The importer updates the profile script list.

## Some ajax [!DNL Target] calls are not working.

**Note:** Multiple ajax [!DNL Target] calls with the same name but different parameters will not work on the same page. Only the first call will be made.

## You activated an activity using the Target API, but the activity shows a status of [!UICONTROL Inactive] in the Target UI.

When you perform certain actions, such as activating an activity outside of the UI using the Target API, the update can take up to ten minutes to propagate to the UI.