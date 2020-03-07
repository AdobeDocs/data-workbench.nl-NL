---
description: De eerste stap is de rol IIS op uw dashboardserver toe te laten.
solution: Analytics
title: IIS inschakelen
topic: Data workbench
uuid: fbd194db-3307-41ae-8ece-05eb261d74ad
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# IIS inschakelen{#enabling-iis}

De eerste stap is de rol IIS op uw dashboardserver toe te laten.

1. Onder **[!UICONTROL Administrative Tools]**, open de **[!UICONTROL Server Manager]**.
1. Klik het het menupunt van Rollen in het linkergedeelte van het **[!UICONTROL Server Manager]** venster met de rechtermuisknop aan.
1. Selecteer **[!UICONTROL Add Roles]**.
1. Selecteer **[!UICONTROL Web Server (IIS)]** en ga met **[!UICONTROL Add Roles Wizard]** verder. Zorg ervoor dat de volgende Diensten van de Rol worden toegelaten:

   | Gemeenschappelijke HTTP-kenmerken |
   |---|
   | Statische inhoud |
   | Standaarddocument |
   | Directory Browsen |
   | HTTP-fouten |
   | HTTP-omleiding |

   | Ontwikkeling van toepassingen |
   |---|
   | ASP.NET |
   | .NET-uitbreidbaarheid |
   | ISAPI-uitbreidingen |
   | ISAPI-filters |

   | Gezondheid en diagnose |
   |---|
   | HTTP-registratie |
   | Logboektools |
   | Beeldscherm aanvragen |
   | Tracering |
   | Aangepaste logboekregistratie |

   | Beveiliging |
   |---|
   | Basisverificatie |
   | Windows-verificatie |
   | URL-verificatie |
   | Aanvraagfiltering |
   | IP- en domeinbeperkingen |

   | Beheertools |
   |---|
   | IIS Management Console |
   | IIS Management Script en tools |
   | Management Service |

1. Volg de wizard om de installatie te voltooien.
