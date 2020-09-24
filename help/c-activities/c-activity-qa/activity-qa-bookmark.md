---
keywords: qa;preview;bookmarklet;preview links
description: Information to help you use the Adobe Target QA bookmarklet to force Target to release you from QA mode.
title: Activity QA bookmarklet for Adobe Target
feature: qa
topic: Advanced,Standard,Classic
uuid: 2890e215-16c9-4b22-a8eb-732cd6efede3
---

# Activity QA bookmarklet{#activity-qa-bookmarklet}

Information to help you use the [!DNL Target] QA bookmarklet to force [!DNL Target] to release you from QA mode.

>[!NOTE]
>
>The process to create a bookmarklet varies by browser type and version. Consult your browser's help or search on the Internet for specific directions.

## Activity QA bookmarklet for at.js 1.*x*

Because [QA mode](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) is sticky, after you browse a website in QA mode, your [!DNL Target] session must expire or you need to have [!DNL Target] release you from QA mode before you can view your site like a typical visitor. Use the QA [!DNL Target] bookmarklet to force yourself out of QA mode.

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser's Bookmarks Toolbar:

```
javascript:(
    function () {
        if (window.location.href.indexOf('?') != -1) {
            var parts = window.location.href.split('at_preview_token',2);
            if (parts.length > 1) {
                window.location.href = parts[0].concat('at_preview_token=');
            } else {
                window.location.href = window.location.href.concat("&at_preview_token=")
            }
        } else {
            window.location.href = window.location.href.concat("?at_preview_token=")
        }
    }
)();
```

You can also manually force yourself out of QA mode by loading a page on your site with the `at_preview_token` parameter with an empty value. 

For example:

`https://www.mysite.com/?at_preview_token=` 

## Activity QA bookmarklet for at.js 2.*x*

In contrast to at.js 1.*x*, at.js 2.*x* does not support third-party cookies, and QA mode is only sticky for the first-party domain (by means of a first-party cookie set by at.js). Thus, in at.js 2.*x*, QA mode session is managed only on the client-side and no QA mode cookies are sent to Target. 

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser's Bookmarks Toolbar:

```
javascript:(
    function () {
        var AT_QA_MODE = 'at_qa_mode=';
        var isSet = document.cookie.split(';').some(function (cookie) {
            return cookie.trim().startsWith(AT_QA_MODE);
        });
        if (isSet) {
            document.cookie = AT_QA_MODE + '; Path=/; Max-Age=-0;';
            var url = window.location.href.split('at_preview_token',2)[0];
            window.open(url.substring(0, url.length - 1), '_self', 'noreferrer');
        }
    })();
```

## Use the Activity QA bookmarklet

Click the bookmarklet on your browser's toolbar.

