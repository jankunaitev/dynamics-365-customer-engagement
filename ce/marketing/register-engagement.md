---
title: "Register link clicks and website visits (Dynamics 365 for Marketing) | Microsoft Docs"
description: "Set up your website to record visits from known and unknown contacts, and create redirect links that register clicks from anywhere in Dynamics 365 for Marketing"
keywords: website;redirect URL;behavioral analysis;behavior;tracking
ms.date: 04/01/2018
ms.service: dynamics-365-marketing
ms.custom: 
  - dyn365-marketing
ms.topic: article
applies_to: 
  - Dynamics 365 for Customer Engagement (online)
  - Dynamics 365 for Customer Engagement Version 9.x
ms.assetid: bde3efc9-6ef1-4705-a925-34670c823f40
author: kamaybac
ms.author: kamaybac
manager: shellyha
ms.reviewer:
topic-status: Drafting
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365Mktg
---

# Register contacts' engagement with your internet marketing initiatives

[!INCLUDE[cc_applies_to_update_9_0_0](../includes/cc_applies_to_update_9_0_0.md)]

You can measure customer engagement with your marketing initiatives in several ways, including by:

- Adding a script to the pages of your website that enables [!INCLUDE[pn-marketing-business-app-module-name](../includes/pn-marketing-business-app-module-name.md)] to record how people use your website and to connect browsing records to anonymous and known contacts.
- Setting up redirect URLs, which log clicks on links that you post to social-media sites, ad banners, and other places online. You'll be able to see how often a link was clicked, when it was clicked, and the physical location where it was clicked. You'll also be able to see which redirect URLs any given lead or contact clicked on (provided they are working on a machine where the right cookie is set).

[!INCLUDE[cc-marketing-cookies](../includes/cc-marketing-cookies.md)]

<a name="monitor-visitors"></a>

## Monitor how visitors use your website

When people come to your website, they are expressing an interest in your organization and its products. And where they go on your site tells you even more about what they are interested in. Frequent or extended browsing sessions with your site, especially in the products or purchasing areas, can be a strong indicator of a contact who is ready to buy.

<!-- [!INCLUDE[pn-marketing-business-app-module-name](../includes/pn-marketing-business-app-module-name.md)] can track each visitor who comes to your website by using cookies to identify individual browsers each time they open a page or return to your site. Visitors will be anonymous at first, but after a visitor submits a landing page with contact information, [!INCLUDE[pn-microsoftcrm](../includes/pn-dynamics-365.md)] can link the browser cookie to a contact record, and you'll be able to see the full history of how that contact uses your site, including information from when he or she was still anonymous. -->

To enable website tracking, you must add [!INCLUDE[pn-javascript](../includes/pn-javascript.md)] code generated by [!INCLUDE[pn-microsoftcrm](../includes/pn-dynamics-365.md)] to each page that you want to track. Each script that the system generates has a unique ID value, which identifies the individual script and is stored with each visit it records (other than this, each script is identical). [!INCLUDE[pn-microsoftcrm](../includes/pn-dynamics-365.md)] treats all visits to pages that have the same script as occurring on the same website. You might use just one script on all pages, or you might set up several different scripts to divide your site into logical areas of interest. If your organization runs several websites (such as one for each brand), you would typically track each one separately by using different [!INCLUDE[pn-javascript](../includes/pn-javascript.md)] code on each of them, though you could also track them all as a single site. The easiest way to add [!INCLUDE[pn-microsoftcrm](../includes/pn-dynamics-365.md)] [!INCLUDE[pn-javascript](../includes/pn-javascript.md)] code to all the pages of your site that need it is probably by adding the code to the page templates in your CMS system.

> [!IMPORTANT]
> The website tracking script that is supplied by this feature will attempt to set a cookie for all visitors to your site. If your site includes a feature that allows visitors to opt-out of cookies, the supplied [!INCLUDE[pn-microsoftcrm](../includes/pn-microsoftcrm.md)] script will still attempt to set its cookie even for visitors who have opted-out. If you want to fully respect the opt-out preference of your site visitors, then you must modify the [!INCLUDE[pn-microsoftcrm](../includes/pn-microsoftcrm.md)] website tracking script as required so that it also works with your site's opt-out mechanism.

### Find or create tracking and form-capture codes for your website

For each collection of webpages that you want to treat as a discrete unit in [!INCLUDE[pn-microsoftcrm](../includes/pn-dynamics-365.md)], you must set up a website record, which generates both tracking and form-capture codes for use on those pages.

1. Go to **Marketing** &gt; **Internet Marketing** &gt; **Websites** to see the current list of websites you are tracking.

1. Find the website you want to work with, or select **New** to create a new one.

1. Your new or existing website record opens. Here you can enter and read information and settings for your website. You'll also find results and analytics gathered for the current site so far (if any). The following settings and information are most important when setting up a website for tracking:

   - **Name**: Shows a name for the website record, which you'll see in the list view and anywhere else you need to identify the record.
   - **URL**: Shows the address of the site (or sub-site) where you'll use the codes generated by this record. This isn't required, nor is it used in the generated codes, but this can be important information to help you and other users know where the code is being used.
   - **Timeout**: The system counts all page loads requested by a single visitor within a short space of time as belonging to the same session. A session is closed when the amount of time specified here passes with no new page requests from that visitor.

1. If you're working with a new website record, then select **Save** on the command bar to generate the website-tracking and form-capture codes. After you've saved the record at least once, you'll see the following:
   - **JavaScript code**: This is the code that you must place on each webpage that you want to track as part of the current website. It is read-only. Copy the code from here and paste it onto each webpage (or CMS template) as needed.
   - **Form capture code**: This is the code that you must place on each external webpage that includes an externally designed form that you'd like to use to submit data back to [!INCLUDE[pn-marketing-business-app-module-name](../includes/pn-marketing-business-app-module-name.md)]. Copy the code from here and paste it onto each webpage (or CMS template) as needed.  [!INCLUDE[proc-more-information](../includes/proc-more-information.md)] [Use form capture to integrate a form created externally](embed-forms.md#form-capture).

### View site-visit data and analytics

The same website record where you find the [!INCLUDE[pn-javascript](../includes/pn-javascript.md)] tracking code also shows the data collected by using that code. To see the results, go to **Marketing** &gt; **Internet Marketing** &gt; **Websites** and open the website record you want to examine. Browse the following three tabs to see what has been happening on your site:

- **General Info**: This is where you find the basic metadata and [!INCLUDE[pn-javascript](../includes/pn-javascript.md)] code for the current site. After your script has started to collect data, you'll find the results here, including your top 10 pages and other information.
- **Timeline**: Shows a detailed timeline of each click recorded for the current website over time.

> [!NOTE]
> Website results and insights are also reported for each individual contact record. [!INCLUDE[proc-more-information](../includes/proc-more-information.md)] [Contact insights](insights.md#contact-insights)

## Track visitors to your [!INCLUDE[pn-microsoftcrm](../includes/pn-dynamics-365.md)] marketing pages

Each time you publish a marketing page, [!INCLUDE[pn-microsoftcrm](../includes/pn-dynamics-365.md)] sets up a new website (including unique [!INCLUDE[pn-javascript](../includes/pn-javascript.md)] tracking code) to track interactions with that page only. You'll find these in the **Marketing** &gt; **Internet Marketing** &gt; **Websites** list next to your other websites. For more information about how to work with website tracking and view the results, see the previous section.

## Set up redirect URLs

*Redirect URLs* are links that redirect through your [!INCLUDE[pn-microsoftcrm](../includes/pn-dynamics-365.md)] server on their way to some other piece of content that the person who clicked the link is actually looking for.

[!INCLUDE[pn-microsoftcrm](../includes/pn-dynamics-365.md)] logs each click on a redirect URL as it passes the user on to the actual target. By using different redirect URLs in your banner ads, tweets, [!INCLUDE[tn-facebook](../includes/tn-facebook.md)] posts, and elsewhere, you'll be able to see how many people clicked on each of those links, where they were (physically) when they did so, and more. This can help you evaluate which of your communication channels are having the greatest impact, and which you should improve or abandon.

### Find or create a redirect URL

To find or create a redirect URL.

1. Go to **Marketing** &gt; **Internet Marketing** &gt; **Redirect URLs** to see the current list of redirect URLs you have set up.

2. Find and open the redirect URL you want to work with, or select **New** on the command bar to create a new one.

3. Your new or existing redirect-URL record opens. Here you can enter and read description information and settings for your redirect URL. You'll also find results and analytics gathered for the current redirect URL so far (if any). The following settings and information are most important when setting up a redirect URL:

   - **Name**: Enter a name for the redirect-URL record, which you'll see in the list view and anywhere else where you need to identify the record. You should use a name that reflects how and where you will use the link, such as "LinkedIn spring campaign."
   - **Original URL**: Enter the URL for the page or download that should open when somebody clicks on the redirect URL (after being logged and forwarded from the [!INCLUDE[pn-microsoftcrm](../includes/pn-dynamics-365.md)] server).
   - **Redirecting URL**: This is the redirecting URL, generated by [!INCLUDE[pn-microsoftcrm](../includes/pn-dynamics-365.md)], that you can copy and use wherever you want to post the link. It is generated the first time you save the record.

4. Select **Save** to save your work and generate the redirecting URL.

### View redirect URL click data and analytics

The same redirect-URL record where you can find the redirecting URL also shows the data collected by using that URL. To see these results, go to **Marketing** &gt; **Internet Marketing** &gt; **Redirect URLs** and open the redirect-URL record you want to examine. Browse the following two tabs to see information gathered by the URL:

- **General Info**: This is where you find the basic metadata and the redirecting URL itself. After your redirecting URL has started to collect data, you'll find the results here, including a map with geodata and other information.
- **Timeline**: Shows a detailed timeline of each click recorded over time.

> [!NOTE]
> Redirect URL results and insights are also reported for each individual contact and lead record. [!INCLUDE[proc-more-information](../includes/proc-more-information.md)] [Contact insights](insights.md#contact-insights)

### See also

[Design lead-scoring models](score-manage-leads.md)  
[Set up lead scoring](set-up-lead-scoring.md)  
[How Dynamics 365 for Marketing uses cookies](cookies.md)
