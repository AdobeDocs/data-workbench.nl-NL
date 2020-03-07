---
description: Stappen om het dashboard in IIS op te stellen.
solution: Analytics
title: Het Dashboard implementeren
topic: Data workbench
uuid: e9a5d62e-9d59-448a-9728-8087aec0fdec
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het Dashboard implementeren{#deploying-the-dashboard}

Stappen om het dashboard in IIS op te stellen.

1. Creeer een installatieomslag om het dashboard, zoals te installeren [!DNL c:\inetpub\wwwroot\dashboard].
1. Creeer de de toepassingspool van het dashboard in IIS.
1. Open de Console van de Manager IIS.
1. Ga naar **[!UICONTROL Application Pools]**.
1. Selecteer **[!UICONTROL Add Application Pool…]**in het **[!UICONTROL Actions]** menu aan het recht.
1. In de **[!UICONTROL Add Application Pool]** vorm, gebruik het dashboard voor de naam en selecteer .NET Kader v.4.0.xxxxxx als uw .NET Versie van het Kader.
1. Verlaat andere gebieden als hun gebrek en klik **[!UICONTROL OK]** om de toepassingspool tot stand te brengen.
1. Stel de dashboardtoepassing op.
1. Open de Console van de Manager IIS.
1. Breid uit **[!UICONTROL Default Web Site]**, zou u de omslag moeten zien u in c:\inetpub\wwwroot\dashboard by default creeerde.
1. Klik de omslag met de rechtermuisknop aan en selecteer **[!UICONTROL Convert to Application]**.
1. Selecteer **[!UICONTROL Application Pool]**gecreeerd in Stap 2 (bijvoorbeeld, &quot;Dashboard&quot;).
1. Onder **[!UICONTROL Sites]**, klik de website met de rechtermuisknop aan waaraan u wenst op te stellen (bijvoorbeeld, &quot;StandaardWebsite&quot;).
1. Selecteer **[!UICONTROL Deploy]** > **[!UICONTROL Import Application]**.
1. Doorblader aan en selecteer het dashboardplaatsingsdossier dat door Adobe wordt verstrekt.
1. Klik **[!UICONTROL Next]** tweemaal om aan het Enter scherm van de Informatie van de Toepassing te werk te gaan.
1. Van dit scherm, kunt u verkiezen om uw dashboardplaatsing aan te passen.
1. Voor **[!UICONTROL Application Path]**, ga de eerder geselecteerde omslagnaam in.
1. Onder **[!UICONTROL Disable Automatic Database Upgrade]**, ga binnen `False`, aangezien dit een nieuwe installatie is.
1. Pas uw verbindingskoord aan, indien nodig. Bijvoorbeeld:

   ```
   Data Source=.;Initial Catalog=thinclientdb;Integrated Security=SSPI;Connect Timeout=30; 
   Application Name=Insight Dashboard;MultipleActiveResultSets=true;
   ```

1. Klik **[!UICONTROL Next]** en IIS zal beginnen installerend de toepassing.
1. Zodra de installatie heeft voltooid, zou u geen fouten in het installatielogboek moeten zien.
