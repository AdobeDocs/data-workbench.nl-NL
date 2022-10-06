---
description: Stappen om het dashboard in IIS op te stellen.
title: Het dashboard implementeren
uuid: e9a5d62e-9d59-448a-9728-8087aec0fdec
exl-id: d59efcc3-7405-407d-840a-b5202f418d51
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Het dashboard implementeren{#deploying-the-dashboard}

{{eol}}

Stappen om het dashboard in IIS op te stellen.

1. Maak een installatiemap om het dashboard te installeren, zoals [!DNL c:\inetpub\wwwroot\dashboard].
1. Maak de toepassingspool van het dashboard in IIS.
1. Open de IIS Manager-console.
1. Ga naar **[!UICONTROL Application Pools]**.
1. Selecteren **[!UICONTROL Add Application Pool…]**in de **[!UICONTROL Actions]** rechts.
1. In de **[!UICONTROL Add Application Pool]** vorm, gebruik het dashboard voor de naam en selecteer .NET Kader v.4.0.xxxx als uw .NET Versie van het Kader.
1. Andere velden standaard laten en klikken **[!UICONTROL OK]** om de toepassingspool te maken.
1. Implementeer de dashboardtoepassing.
1. Open de IIS Manager-console.
1. Breid uit **[!UICONTROL Default Web Site]**, wordt de map weergegeven die u hebt gemaakt in c:\inetpub\wwwroot\dashboard by default.
1. Klik met de rechtermuisknop op de map en selecteer **[!UICONTROL Convert to Application]**.
1. Selecteer de **[!UICONTROL Application Pool]**Gemaakt in Stap 2 (bijvoorbeeld &quot;Dashboard&quot;).
1. Onder **[!UICONTROL Sites]**, klikt u met de rechtermuisknop op de website waarop u wilt implementeren (bijvoorbeeld &quot;Standaardwebsite&quot;).
1. Selecteren **[!UICONTROL Deploy]** > **[!UICONTROL Import Application]**.
1. Blader naar en selecteer het dashboardimplementatiebestand van Adobe.
1. Klikken **[!UICONTROL Next]** twee keer om naar het Enter scherm van de Informatie van de Toepassing te werk te gaan.
1. Vanuit dit scherm kunt u de implementatie van het dashboard aanpassen.
1. Voor **[!UICONTROL Application Path]**, voert u de eerder geselecteerde mapnaam in.
1. Onder **[!UICONTROL Disable Automatic Database Upgrade]**, enter `False`, aangezien dit een nieuwe installatie is.
1. Pas indien nodig de verbindingstekenreeks aan. Bijvoorbeeld:

   ```
   Data Source=.;Initial Catalog=thinclientdb;Integrated Security=SSPI;Connect Timeout=30; 
   Application Name=Insight Dashboard;MultipleActiveResultSets=true;
   ```

1. Klikken **[!UICONTROL Next]** en IIS beginnen de toepassing te installeren.
1. Nadat de installatie is voltooid, ziet u geen fouten in het installatielogboekbestand.
