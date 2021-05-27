---
description: Met de desktop kunt u eenvoudig bepalen waar elke werkruimte is opgeslagen, of deze zich op de Data Workbench-server, op uw lokale computer of op beide bevindt.
title: Bestandsversie
uuid: 5e7430f3-1425-41d2-828b-bc8f5786bf3b
exl-id: 82a70d51-a95c-4ddd-8d3c-cd0364940693
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Bestandsversie{#file-versioning}

Met de desktop kunt u eenvoudig bepalen waar elke werkruimte is opgeslagen, of deze zich op de Data Workbench-server, op uw lokale computer of op beide bevindt.

## Bestandsversies {#section-d555c96b016344f19b356c12213dd2a9} identificeren

**Server**

Een serverwerkruimte wordt opgeslagen op de verbonden server van de Data Workbench en is beschikbaar aan alle gebruikers die toegang tot dit profiel en lusje hebben. Een serverwerkruimte wordt weergegeven als één miniatuur.

![](assets/wsp_thumb_server.png)

De werkruimten van de server worden door gebrek opgeslagen in de aangewezen subomslag binnen de omslag van Werkruimten op de aangesloten server van de Data Workbench.

**Lokaal**

Een lokale werkruimte is de lokale versie van een serverwerkruimte. Een lokale werkruimte wordt weergegeven als twee overlappende miniaturen. De miniatuur bovenaan wordt aanvankelijk omgeven door een gloed, wat aangeeft dat er onlangs wijzigingen zijn aangebracht in de werkruimte van de server. Deze gloed verdwijnt na verloop van tijd.

![](assets/wsp_thumb_local.png)

Lokale werkruimten worden standaard opgeslagen in de naammap [!DNL User\working profile name\Workspaces\tab] in de installatiemap van de Data Workbench (of Insight).

>[!NOTE]
>
>Wanneer u een lokale versie van een serverwerkruimte hebt, moet u terugkeren naar de serverversie voordat u een bijgewerkte versie van de serverwerkruimte kunt downloaden. Als u de serverversie wilt herstellen zonder lokale wijzigingen, klikt u met de rechtermuisknop op de miniatuur van de lokale werkruimte en klikt u op **[!UICONTROL Revert to server version]**.

**Gebruiker**

Een gebruikerswerkruimte is een werkruimte die is gemaakt op en alleen bestaat op de lokale computer. Een gebruikerswerkruimte wordt weergegeven als één miniatuur met een gestippelde omtrek van een lege werkruimte erachter, wat aangeeft dat er geen bronwerkruimte is op de server van de verbonden Data Workbench.

![](assets/wsp_thumb_user.png)

Gebruikerswerkruimten worden standaard opgeslagen in de map User\*working profile name*\Workspaces\*tab name* in de installatiemap Insight.
