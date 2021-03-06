---
title: Veelgestelde vragen | Microsoft Docs
description: Antwoorden op enkele veelgestelde vragen over Microsoft Flow
services: ''
suite: flow
documentationcenter: na
author: stepsic-microsoft-com
manager: anneta
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/15/2017
ms.author: stepsic
ms.openlocfilehash: 99a66520b5a922b4945c9d3c94c7a5c053df98ee
ms.sourcegitcommit: a0435b92fa7f5dedff3b0ff806836c7a07309fd2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/15/2018
---
# <a name="frequently-asked-questions"></a>Veelgestelde vragen
## <a name="audience-and-strategy"></a>Publiek en de strategie
### <a name="what-is-microsoft-flow"></a>Wat is Microsoft Flow?
Microsoft Flow is een cloudservice waarmee line-of-business-gebruikers praktisch en eenvoudig werkstromen kunnen opzetten waarmee tijdrovende zakelijke taken en bedrijfsprocessen over toepassingen en services kunnen worden geautomatiseerd.

### <a name="who-is-the-intended-audience-for-microsoft-flow"></a>Wie is de doelgroep voor Microsoft Flow?
Microsoft Flow heeft twee verschillende doelgroepen:

* Line-of-business 'Citizen Integrators' in enterprise-organisaties die samenwerken met IT om de verantwoordelijkheid voor zakelijke oplossingen dichter naar het bedrijf zelf te verplaatsen.
* IT-besluitvormers die het voor line-of-business-partners mogelijk willen maken hun eigen oplossingen te maken, zodat IT-professionals en integratiespecialisten zich met al hun ervaring kunnen concentreren op meer geavanceerde integratiehulpprogramma's, zoals Azure Logic Apps.

### <a name="how-do-microsoft-flow-and-logic-apps-relate-to-each-other"></a>Hoe zijn Microsoft Flow en Logic Apps met elkaar verbonden?
Microsoft Flow bevat functies waarmee line-of-business-gebruikers geautomatiseerde werkstromen kunnen maken. Logic Apps is een Azure-service die dezelfde handige functies als Microsoft Flow biedt, plus functies zoals integratie met Azure Resource Manager en Azure Portal, PowerShell en xPlat CLI, Visual Studio en aanvullende connectors. [Meer informatie over Logic Apps](https://azure.microsoft.com/services/app-service/logic/).

### <a name="how-does-microsoft-flow-fit-in-microsofts-overall-business-application-platform-strategy"></a>Hoe past Microsoft Flow binnen de algehele strategie van Microsoft’s zakelijke toepassingenplatform?
Microsoft Flow is onderdeel van een krachtig en flexibel platform voor zakelijke toepassingen dat onder andere PowerApps, Common Data Service, Dynamics 365 en Office 365 omvat. Met dit platform kunnen onze klanten, partners en ISV-partners doelgericht oplossingen maken voor hun bedrijf of sector, voor functionele rollen en zelfs voor hun specifieke geografie. Line-of-business-gebruikers, die het beste de behoeften van hun bedrijf begrijpen, kunnen nu eenvoudig gegevens en processen analyseren, opstellen en stroomlijnen. Professionele ontwikkelaars kunnen de line-of-business-benadering eenvoudig uitbreiden naar automatisering, analyse en apps om gebruik te maken van Azure-services zoals Functions, App Service en Logic Apps. Dankzij API-connectors, gateways en de Microsoft Common Data Service kan beter gebruik worden gemaakt van services of gegevens die al in gebruik zijn, zowel in de cloud als on-premises.

## <a name="functionality"></a>Functionaliteit
### <a name="what-do-i-need-to-use-microsoft-flow"></a>Wat heb ik nodig om met Microsoft Flow te kunnen werken?
Als u Microsoft Flow wilt gebruiken, hebt u alleen een webbrowser en een e-mailadres nodig.

### <a name="what-browsers-does-microsoft-flow-support"></a>Welke browsers worden ondersteund door Microsoft Flow?
Microsoft Flow ondersteunt Microsoft Edge en de huidige versie van Chrome en Safari.

### <a name="which-email-addresses-are-supported"></a>Welke e-mailadressen worden ondersteund?
Microsoft Flow biedt ondersteuning voor alle e-mailadressen, behalve adressen die op .gov en .mil eindigen.  

### <a name="is-microsoft-flow-available-on-premises"></a>Is Microsoft Flow on-premises beschikbaar?
Microsoft Flow is puur een openbare-cloudservice. U kunt echter veilig verbinding maken met uw eigen lokale services via de on-premises gegevensgateway.

### <a name="what-services-can-microsoft-flow-connect-to"></a>Met welke services kan Microsoft Flow verbinding maken?
U kunt met Microsoft Flow standaard verbinding maken met meer dan honderd gegevensbronnen. Hieraan worden voortdurend nieuwe bronnen toegevoegd. Enkele voorbeelden van gegevensbronnen en -services zijn:

* SharePoint
* Dynamics 365
* OneDrive
* OneDrive voor Bedrijven
* Google Drive
* Google Sheets
* Trello
* Twitter
* Box
* Facebook
* SalesForce.com
* Mailchimp
* API’s van klanten

Een volledige lijst met beschikbare connectors vindt u [hier](https://go.microsoft.com/fwlink/?LinkId=832211).

Via de [on-premises gegevensgateway](gateway-manage.md) krijgt u toegang tot gegevensbronnen in uw eigen IT-infrastructuur.

### <a name="what-are-templates"></a>Wat zijn sjablonen?
Sjablonen zijn ingebouwde stromen voor populaire en veelvoorkomende scenario's. Als u een sjabloon gebruikt, hebt u alleen toegang tot de services in de sjabloon nodig en hoeft u alleen de vereiste instellingen in te vullen.

### <a name="what-data-sources-will-i-be-able-to-connect-to"></a>Met welke gegevensbronnen kan ik verbinding maken?
U kunt verbinding maken met meer dan honderd standaardservices van Microsoft en derden, waaronder Office 365, Twitter, SharePoint, OneDrive, Dropbox en SQL Server. U kunt ook verbinding maken met premiumservices zoals Salesforce en de Microsoft Common Data-service voor PowerApps.

### <a name="how-do-i-connect-to-a-rest-api-in-my-flow"></a>Hoe kan ik verbinding maken met een REST API in mijn stroom?
Door een [aangepaste connector](register-custom-api.md) te maken, kunt u verbinding maken met een REST API die gebruikmaakt van JSON en ondersteuning biedt voor ten minste één van de meer dan tien ondersteunde verificatiemethoden.

### <a name="how-do-i-connect-to-sql-server-and-other-on-premises-data-sources"></a>Hoe kan ik verbinding maken met SQL Server en andere on-premises gegevensbronnen?
Met de [lokale gegevensgateway](gateway-manage.md) kunt u verbinding maken met services in uw lokale netwerk.

### <a name="can-i-share-the-flows-i-create"></a>Kan ik de stromen delen die ik maak?
U kunt stromen op een van de volgende manieren delen:

* U kunt collega's of groepen als eigenaren van stromen in uw organisatie toevoegen, zodat de gebruikers de stroom ook kunnen bewerken en beheren.
* Voor stromen die handmatig kunnen worden uitgevoerd, kunt u andere personen of groepen in uw organisatie ook toestemming geven om de stroom alleen uit te voeren.

### <a name="how-many-flows-can-i-have"></a>Hoeveel stromen kan ik hebben?
Microsoft Flow wordt geleverd met maar liefst vijftig stromen. Als u er meer nodig hebt, kunt u deze aanvragen.

### <a name="where-do-i-get-started-with-microsoft-flow"></a>Hoe ga ik aan de slag met Microsoft Flow?
Ga aan de slag met de volgende informatiebronnen:

* [Weblog](https://flow.microsoft.com)
* [YouTube-kanaal](https://youtube.com/playlist?list=PL8nfc9haGeb55I9wL9QnWyHp3ctU2_ThF)
* [Onderwerp](getting-started.md)
* [Community](https://powerusers.microsoft.com)

### <a name="what-operating-systems-does-the-mobile-app-for-microsoft-flow-support"></a>Welke besturingssystemen worden ondersteund door de mobiele Microsoft Flow-app?
De mobiele app voor Microsoft Flow is beschikbaar op [Android](https://aka.ms/flowmobiledocsandroid), [iOS](https://aka.ms/flowmobiledocsios) en [Windows Phone](https://aka.ms/flowmobilewindows).

### <a name="can-flows-be-turned-off-or-disabled"></a>Kunnen stromen worden uitgezet of uitgeschakeld?

Ja, elke stroom heeft een aan/uit-schakelaar, waarmee u het verwerken van aanvragen door de stroom kan stopzetten.

In de volgende tabel kunt u zien hoe uw stroom reageert wanneer deze opnieuw wordt ingeschakeld.

Type trigger|Beschrijving
-------|--------
Polling, zoals de trigger voor **herhaling**|Wanneer de stroom weer wordt ingeschakeld, worden alle gebeurtenissen verwerkt die onverwerkt of in behandeling zijn.
Webhook|Wanneer de stroom weer wordt ingeschakeld, worden hierdoor alleen nieuwe gebeurtenissen verwerkt die worden gegenereerd nadat de stroom is ingeschakeld.

### <a name="what-regions-and-languages-does-microsoft-flow-support"></a>Welke regio's en talen ondersteunt Microsoft Flow?
Microsoft Flow is beschikbaar in 42 talen, in [zes regio's](regions-overview.md).

### <a name="how-does-microsoft-flow-compare-to-sharepoint-designer-2013"></a>In hoeverre is Microsoft Flow te vergelijken met SharePoint Designer 2013?
Microsoft Flow is de opvolger van SharePoint Designer voor veel gangbare bedrijfsscenario, zoals goedkeuringen, documentrevisie en onboarding/offboarding. Het wordt in de toekomst het standaardhulpprogramma voor zakelijke automatisering in SharePoint.

### <a name="how-does-microsoft-flow-ensure-that-corporate-data-isnt-accidentally-released-to-social-media-services"></a>Hoe zorgt Microsoft Flow ervoor dat bedrijfsgegevens niet per ongeluk terechtkomen bij sociale mediaservices?
Beheerders kunnen een [beleid ter preventie van gegevensverlies](prevent-data-loss.md) maken om ervoor te zorgen dat in Microsoft Flow alleen goedgekeurde services worden gebruikt.

## <a name="licensing"></a>Licentieverlening
### <a name="will-microsoft-flow-still-have-a-free-or-trial-option"></a>Blijft de gratis versie of proefversie behouden voor Microsoft Flow?
Ja. U kunt gebruikmaken van een gratis versie met beperkte gebruikersrechten of u kunt zich registreren voor een gratis proefversie van Microsoft Flow van 90 dagen. U kunt op elk moment tijdens de proefperiode uw abonnement activeren.

### <a name="what-pricing-plans-do-you-offer"></a>Wat is de prijsstelling voor abonnementen?
Microsoft Flow heeft zowel gratis als betaalde serviceniveaus. [Meer informatie over prijzen](billing-questions.md).

