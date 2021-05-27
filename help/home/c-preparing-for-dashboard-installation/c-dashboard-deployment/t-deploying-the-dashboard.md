---
description: Stappen om het dashboard in IIS op te stellen.
title: Het dashboard implementeren
uuid: e9a5d62e-9d59-448a-9728-8087aec0fdec
exl-id: d59efcc3-7405-407d-840a-b5202f418d51
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Het dashboard{#deploying-the-dashboard} implementeren

Stappen om het dashboard in IIS op te stellen.

1. Maak een installatiemap om het dashboard te installeren, zoals [!DNL c:\inetpub\wwwroot\dashboard].
1. Maak de toepassingspool van het dashboard in IIS.
1. Open de IIS Manager-console.
1. Ga naar **[!UICONTROL Application Pools]**.
1. Selecteer **[!UICONTROL Add Application Pool…]**in het **[!UICONTROL Actions]** menu aan het recht.
1. In de **[!UICONTROL Add Application Pool]** vorm, gebruik het dashboard voor de naam en selecteer .NET Kader v.4.0.xxxxxx als uw .NET Versie van het Kader.
1. Laat andere velden als de standaardvelden staan en klik op **[!UICONTROL OK]** om de toepassingspool te maken.
1. Implementeer de dashboardtoepassing.
1. Open de IIS Manager-console.
1. Vouw **[!UICONTROL Default Web Site]** uit en bekijk de map die u hebt gemaakt in c:\inetpub\wwwroot\dashboard by default.
1. Klik met de rechtermuisknop op de map en selecteer **[!UICONTROL Convert to Application]**.
1. Selecteer **[!UICONTROL Application Pool]**gecreeerd in Stap 2 (bijvoorbeeld, &quot;Dashboard&quot;).
1. Klik onder **[!UICONTROL Sites]** met de rechtermuisknop op de website waarop u wilt implementeren (bijvoorbeeld &quot;Standaardwebsite&quot;).
1. Selecteer **[!UICONTROL Deploy]** > **[!UICONTROL Import Application]**.
1. Blader naar en selecteer het dashboardimplementatiebestand van Adobe.
1. Klik **[!UICONTROL Next]** tweemaal om aan het Enter scherm van de Informatie van de Toepassing te werk te gaan.
1. Vanuit dit scherm kunt u de implementatie van het dashboard aanpassen.
1. Voer bij **[!UICONTROL Application Path]** de eerder geselecteerde mapnaam in.
1. Voer onder **[!UICONTROL Disable Automatic Database Upgrade]** `False` in, aangezien dit een nieuwe installatie is.
1. Pas indien nodig de verbindingstekenreeks aan. Bijvoorbeeld:

   ```
   Data Source=.;Initial Catalog=thinclientdb;Integrated Security=SSPI;Connect Timeout=30; 
   Application Name=Insight Dashboard;MultipleActiveResultSets=true;
   ```

1. Klik **[!UICONTROL Next]** en IIS zal beginnen de toepassing te installeren.
1. Nadat de installatie is voltooid, ziet u geen fouten in het installatielogboekbestand.
