---
description: De eerste stap is de rol IIS op uw dashboardserver toe te laten.
title: IIS inschakelen
uuid: fbd194db-3307-41ae-8ece-05eb261d74ad
exl-id: 0d431302-1e69-49b6-8757-9823fd70a3b4
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# IIS{#enabling-iis} inschakelen

De eerste stap is de rol IIS op uw dashboardserver toe te laten.

1. Open **[!UICONTROL Administrative Tools]** onder **[!UICONTROL Server Manager]**.
1. Klik met de rechtermuisknop op het menu-item Rollen in het linkergedeelte van het venster **[!UICONTROL Server Manager]**.
1. Selecteer **[!UICONTROL Add Roles]**.
1. Selecteer **[!UICONTROL Web Server (IIS)]** en ga met **[!UICONTROL Add Roles Wizard]** verder. Zorg ervoor dat de volgende Diensten van de Rol worden toegelaten:

   | Algemene HTTP-functies |
   |---|
   | Statische inhoud |
   | Standaarddocument |
   | Bladeren door mappen |
   | HTTP-fouten |
   | HTTP omleiden |

   | Ontwikkeling van toepassingen |
   |---|
   | ASP.NET |
   | .NET-uitbreidbaarheid |
   | ISAPI-extensies |
   | ISAPI-filters |

   | Gezondheid en diagnose |
   |---|
   | HTTP-registratie |
   | Logboekgereedschappen |
   | Aanvraagmonitor |
   | Overtrekken |
   | Aangepaste logboekregistratie |

   | Beveiliging |
   |---|
   | Basisverificatie |
   | Windows-verificatie |
   | URL-verificatie |
   | Verzoek filteren |
   | IP- en domeinbeperkingen |

   | Beheertools |
   |---|
   | IIS Management Console |
   | IIS Management Script en Tools |
   | Beheerservice |

1. Volg de Tovenaar om de installatie te voltooien.
