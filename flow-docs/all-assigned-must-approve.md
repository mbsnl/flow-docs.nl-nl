---
title: Een goedkeuringsstroom maken waarin iedereen goedkeuring moet verlenen | Microsoft Docs
description: "Maak een goedkeuringsstroom waarin iedereen een aanvraag moet goedkeuren of één persoon deze moet afwijzen."
services: 
suite: flow
documentationcenter: na
author: msftman
manager: anneta
editor: 
tags: 
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/22/2017
ms.author: deonhe
ms.openlocfilehash: 0e0309793cfcb45ca7ee72910803a4abc27d2f26
ms.sourcegitcommit: 4f2cb27d392f46aa1d8680d6278876780ed3871b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/15/2017
---
# <a name="create-an-approval-flow-that-requires-everyone-to-approve"></a>Een goedkeuringsstroom maken waarin iedereen goedkeuring moet verlenen
In deze procedure ziet u hoe u een goedkeuringswerkstroom maakt waarbij iedereen (alle toegewezen goedkeurder) goedkeuring moet verlenen aan een vakantieaanvraag, maar er maar één goedkeurder nodig is om de hele aanvraag af te wijzen.

Dit type goedkeuringswerkstroom is nuttig in een organisatie waarin de manager en de manager van de manager beiden akkoord moeten gaan met de vakantieaanvraag van een werknemer. De aanvraag kan echter worden afgewezen door een van de twee managers.

## <a name="prerequisites"></a>Vereisten
* Toegang tot [Microsoft Flow](https://flow.microsoft.com), Office 365 Outlook en Office 365-gebruikers.
* Een SharePoint Online-[lijst](https://support.office.com/en-us/article/SharePoint-lists-I-An-introduction-f11cd5fe-bc87-4f9e-9bfe-bbd87a22a194).
  
    In deze procedure wordt ervan uitgegaan dat u al een SharePoint Online-lijst hebt gemaakt die wordt gebruikt voor het aanvragen van vakantie. Zie de procedure voor [parallelle goedkeuringen](parallel-modern-approvals.md) voor een uitgebreid voorbeeld waarin wordt uitgelegd hoe uw SharePoint-lijst eruit kan zien.
* Bekendheid met de basisprincipes van het maken van stromen.
  
    U kunt nalezen hoe u [acties, triggers](multi-step-logic-flow.md#add-another-action) en [voorwaarden](add-a-condition.md) maakt. In de volgende stappen wordt ervan uitgegaan dat u weet hoe u deze acties uitvoert.

> [!NOTE]
> In deze procedure worden SharePoint Online en Office 365 Outlook gebruikt, maar u kunt ook andere services gebruiken, zoals Zendesk, Salesforce of Gmail of een van de andere meer dan [150 services](https://flow.microsoft.com/connectors/) waarvoor Microsoft Flow ondersteuning biedt.
> 
> 

## <a name="create-the-flow"></a>De stroom maken
> [!NOTE]
> Als u nog geen verbinding met SharePoint of Office 365 hebt gemaakt, volgt u de instructies wanneer u wordt gevraagd u aan te melden.
> 
> 

In deze procedure worden tokens gebruikt. Als u de lijst met tokens wilt weergeven, tikt of klikt u op een invoerbesturingselement en zoekt u het gewenste token in de lijst **Dynamische inhoud** die wordt geopend.

Meld u aan bij [Microsoft Flow](https://flow.microsoft.com) en voer de volgende stappen uit om de stroom te maken.

1. Selecteer **Mijn stromen** > **Leeg item maken**.
2. Voeg de trigger **SharePoint - Wanneer een item is gemaakt of gewijzigd** toe.
3. Voer het **Siteadres** in voor de SharePoint-site die als host fungeert voor uw lijst met vakantieaanvragen en selecteer de lijst in het vak **Lijstnaam**.
4. Voeg de actie **Office 365-gebruikers - Manager ophalen** toe en voeg het token **Via e-mail gemaakt** toe aan het vak **Gebruiker (UPN)**.
   
    Het token **Via e-mail gemaakt** bevindt zich onder de categorie **Wanneer een item is gemaakt of gewijzigd** van de lijst **Dynamische inhoud**.
5. Voeg nog een actie **Office 365-gebruikers - Manager ophalen** toe en voeg het token **E-mail** toe aan het vak **Gebruiker (UPN)**.
   
    Het token **E-mail** bevindt zich onder de categorie **Manager ophalen** van de lijst **Dynamische inhoud**.
   
    U kunt de naam van de kaart **Manager ophalen 2** ook wijzigen in een herkenbare naam, zoals 'Hogere manager'.
6. Voeg de actie **Een goedkeuring starten** toe en selecteer **Iedereen van de lijst met toegewezen leden** in de lijst **Goedkeuringstype**.
   
   > [!IMPORTANT]
   > Als een goedkeurder een aanvraag afwijst, wordt de goedkeuringsaanvraag beschouwd als afgewezen voor alle goedkeurders.
   > 
   > 
7. Gebruik de volgende tabel als richtlijn om de kaart **Een goedkeuring starten** in te vullen.
   
   | Veld | Beschrijving |
   | --- | --- |
   |  Goedkeuringstype |Gebruik **Iemand van de lijst met toegewezen leden** om aan te geven dat een van de goedkeurders de aanvraag kan goedkeuren of afwijzen. </p>Gebruik **Iedereen van de lijst met toegewezen leden** om aan te geven dat een aanvraag alleen wordt goedgekeurd als iedereen akkoord gaat en de aanvraag wordt afgewezen als één persoon deze weigert. |
   |  Titel |De titel van de goedkeuringsaanvraag. |
   |  Toegewezen aan |De e-mailadressen van de goedkeurders. |
   |  Details |Aanvullende informatie die u wilt verzenden naar de goedkeurders in het veld **Toegewezen aan**. |
   |  Itemkoppeling |Een URL naar het goedkeuringsitem. In dit voorbeeld is dit een koppeling naar het item in SharePoint. |
   |  Beschrijving van itemkoppeling |Een tekstbeschrijving voor **Itemkoppeling**. |
   
   > [!TIP]
   > De actie **Een goedkeuring starten** heeft meerdere tokens, waaronder **Antwoord** en **Antwoordoverzicht**. Gebruik deze tokens in uw stroom om een uitgebreid rapport met resultaten te maken nadat u een goedkeuringsaanvraagstroom hebt uitgevoerd.
   > 
   > 
   
    De kaart **Een goedkeuring starten** is een sjabloon voor de goedkeuringsaanvraag die naar goedkeurders wordt verzonden. Configureer deze op een manier die goed werkt voor uw organisatie. Hier volgt een voorbeeld.
   
    ![een goedkeuring starten](media/all-assigned-must-approve/start-an-approval-card.png)
8. Voeg de actie **Office 365 Outlook - Een e-mail verzenden** toe en configureer deze zo dat er een e-mail wordt verzonden met de resultaten van de aanvraag.
   
    Hier ziet u een voorbeeld van hoe de kaart **Een e-mail verzenden** eruitziet.
   
    ![een e-mail verzenden](media/all-assigned-must-approve/send-an-email-card.png)

> [!NOTE]
> Een actie die volgt na de actie **Een goedkeuring starten**, wordt uitgevoerd op basis van uw selectie in de lijst **Goedkeuringstype** op de kaart **Een goedkeuring starten**. In de volgende tabel ziet u een lijst met de werking op basis van uw selectie.
> 
> 

| Goedkeuringstype | Werking |
| --- | --- |
| Iemand in de lijst met toegewezen leden |Acties die volgen na de actie **Een goedkeuring starten**, worden uitgevoerd nadat een van de goedkeurders een beslissing heeft genomen. |
| Iedereen van de lijst met toegewezen leden |Acties die volgen na de actie **Een goedkekuring starten** worden uitgevoerd nadat een goedkeurder de aanvraag afwijst of iedereen de aanvraag goedkeurt. |

Typ bovenaan het scherm een naam voor de stroom in het vak **Stroomnaam** en selecteer **Stroom maken** om deze op te slaan.

Uw flow is nu voltooid. Als u de stappen hebt gevolgd, lijkt uw stroom op de volgende afbeelding:

![afbeelding van algemene stroom](media/all-assigned-must-approve/overall-flow.png)

Wanneer er nu een item in uw SharePoint-lijst wordt gewijzigd, wordt de stroom geactiveerd en worden er goedkeuringsaanvragen verzonden naar alle goedkeurders die staan vermeld in het vak **Toegewezen aan** van de kaart **Een goedkeuring starten**. Met uw stroom worden goedkeuringsaanvragen verzonden via de mobiele app van Microsoft Flow en via e-mail. De persoon die het item maakt in SharePoint, ontvangt een e-mail met een samenvatting van de resultaten, waarin duidelijk wordt aangegeven of de aanvraag is goedgekeurd of afgewezen.

Hier volgt een voorbeeld van de goedkeuringsaanvraag die aan elke goedkeurder wordt verzonden.

![goedkeuringsaanvraag](media/all-assigned-must-approve/approval-request.png)

Hier volgt een voorbeeld van hoe een antwoord en antwoordoverzicht eruit kunnen zien nadat de stroom is uitgevoerd.

![antwoordtokens](media/all-assigned-must-approve/response-output.png)

## <a name="learn-more-about-approvals"></a>Meer informatie over goedkeuringen
* [Moderne goedkeuringen met één goedkeurder](modern-approvals.md)
* [Sequentiële moderne goedkeuringen](sequential-modern-approvals.md)
* [Parallelle moderne goedkeuringen](sequential-modern-approvals.md)
