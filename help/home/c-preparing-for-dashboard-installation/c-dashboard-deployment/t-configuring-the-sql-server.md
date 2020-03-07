---
description: Alvorens het dashboard kan werken, moet u het toestaan om tot de SQL Server toegang te hebben.
solution: Analytics
title: Het vormen van de SQL Server
topic: Data workbench
uuid: bdd5f9f5-a69f-4001-9f80-901bd7eae129
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het vormen van de SQL Server{#configuring-the-sql-server}

Alvorens het dashboard kan werken, moet u het toestaan om tot de SQL Server toegang te hebben.

1. Open de SQL Studio van het Beheer als Beheerder.
1. Voeg nieuwe login toe door met de rechtermuisknop te klikken **[!UICONTROL Logins]** en te selecteren **[!UICONTROL New Login]**.
1. Voer de volledige naam van de toepassingspool in.

   Door gebrek, wordt de identiteit van de toepassingspool genoemd na de toepassingspool. Als u kiest `dashboard`, dan zal de identiteit worden genoemd `IIS AppPool\dashboard`. 1. Selecteer **[!UICONTROL Server Roles]** en controleer de **[!UICONTROL dbcreator]** rol.
1. Klik **[!UICONTROL OK]** om de nieuwe gebruiker toe te voegen.
