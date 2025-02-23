---
title: "Integrate Dynamics 365 for Customer Engagement appswith Microsoft Teams| MicrosoftDocs"
ms.custom: 
description: "Integrate Dynamics 365 for Customer Engagement appswith Microsoft Teams."
ms.date: 6/20/2019
ms.reviewer: 
ms.service: crm-online
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
applies_to: 
  - Dynamics 365 for Customer Engagement apps
  - Dynamics 365 for Customer Engagement Version 9.x
ms.assetid: 8097c9ec-023b-407d-ac0e-074b5e1964a5
caps.latest.revision: 17
author: mduelae
ms.author: mkaur
manager: kvivek
search.audienceType: 
  - enduser
search.app: 
  - D365CE
  - Powerplatform
---
# Microsoft Teams integration with Dynamics 365 for Customer Engagement apps

[!INCLUDE[cc-applies-to-update-9-0-0](../includes/cc_applies_to_update_9_0_0.md)]

## Overview 
If you're familiar with [Microsoft Teams](https://products.office.com/microsoft-teams/group-chat-software), you know it's the place to manage all your conversations, files, and tools in one team workspace. Create and edit documents right in the app and enjoy instant access to SharePoint, OneNote, Power BI, and now, [!INCLUDE [pn-crm-online](../includes/pn-crm-online.md)]. 

Dynamics 365 for Microsoft Teams integration enables users to easily work with Dynamics 365 customer information and share files directly from Microsoft Teams. This helps them to be more productive and get work done more effectively. 

- **Collaboration hub**: Access a shared workspace for Office apps that most of us already use to work sales opportunities.  
- **Cross-functional collaboration**: Work together with customers and any colleague across functions, even if they aren’t a Dynamics 365 for Customer Engagement apps user.
- **File integration**: Co-author documents using Office 365 and automatically sync to Dynamics 365. 
- **Teams mobile app**: Search from Microsoft Teams mobile app using the Dynamics 365 bot while on the go. 

> [!div class="mx-imgBorder"] 
> ![Features of Teams app](media/teams-intro.png "Features of Teams app")

With the Dynamics 365 for Teams integration, add the Dynamics 365 for Customer Engagement app features that you rely on, to the Teams app you collaborate with. This lets you easily work with Dynamics 365 customer information and share files directly from Microsoft Teams.

- Access Dynamics 365 records by adding a Dynamics 365 tab into the Teams channel. Collaborate at a large scale not only on a single Dynamics 365 record (like a sales opportunity), but also on multiple records with a Dynamics 365 view.
- Use Microsoft Teams integration to seamlessly collaborate on documents between Dynamics 365 and Microsoft Teams. 
- Collaborate on a set of records, such as *active opportunity* using Teams conversation and easily access records on the go using the Dynamics 365 bot for Microsoft Teams mobile app. 

> [!VIDEO https://www.youtube.com/embed/U11x5BlQlDU]

## Feedback

 If you have additonal feedback or questions regarding this feature, contact [D365forTeams@microsoft.com](mailto:D365forTeams@microsoft.com).

## Privacy notice

While using the Dynamics 365 for Customer Engagement appsfor Sales bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent. The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS). Read more about LUIS [here](https://www.luis.ai/). The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso). This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with Dynamics data and retrieves the desired information for the user query.

By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input – which results in an enhanced conversational user experience. The LUIS service and Azure bot framework  may have varying levels of compliance compared to Dynamics 365 for Customer Engagement appsfor Sales. While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics data or account, a user of the Dynamics 365 for Sales bot could voluntarily enter a query containing Customer Data, Personal Data or other data and such query content could get sent to the LUIS service and the Azure bot framework. 

The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, encrypted at rest and is not used for training or service improvement. Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

To manage admin settings for apps in Teams, go to the Microsoft 365 admin center and open **Settings** > **Services & add-ins**, then choose Microsoft Teams. If you're signed in as an Office 365 admin, you can access these controls [here](https://admin.microsoft.com/adminportal/home#/Settings/ServicesAndAddIns), including the ability to uninstall.


### See also
 [Download and install Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)<br/>
 [Microsoft Teams help center](https://support.office.com/teams)

