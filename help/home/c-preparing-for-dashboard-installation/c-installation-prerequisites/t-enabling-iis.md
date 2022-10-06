---
description: De eerste stap is de rol IIS op uw dashboardserver toe te laten.
title: IIS inschakelen
uuid: fbd194db-3307-41ae-8ece-05eb261d74ad
exl-id: 0d431302-1e69-49b6-8757-9823fd70a3b4
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# IIS inschakelen{#enabling-iis}

{{eol}}

De eerste stap is de rol IIS op uw dashboardserver toe te laten.

1. Onder **[!UICONTROL Administrative Tools]**, opent u de **[!UICONTROL Server Manager]**.
1. Klik met de rechtermuisknop op de menuoptie Rollen in het linkergedeelte van het dialoogvenster **[!UICONTROL Server Manager]** venster.
1. Selecteren **[!UICONTROL Add Roles]**.
1. Selecteren **[!UICONTROL Web Server (IIS)]** en doorgaan met de **[!UICONTROL Add Roles Wizard]**. Zorg ervoor dat de volgende Diensten van de Rol worden toegelaten:

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
