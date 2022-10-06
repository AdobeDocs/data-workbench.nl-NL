---
description: Alvorens het dashboard kan werken, moet u het toestaan om tot de SQL Server toegang te hebben.
title: De SQL Server configureren
uuid: bdd5f9f5-a69f-4001-9f80-901bd7eae129
exl-id: 16116cc8-f539-4cf0-ab1d-f2bddd39b38c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# De SQL Server configureren{#configuring-the-sql-server}

{{eol}}

Alvorens het dashboard kan werken, moet u het toestaan om tot de SQL Server toegang te hebben.

1. Open de SQL Studio van het Beheer als Beheerder.
1. Nieuwe aanmelding toevoegen door met de rechtermuisknop te klikken **[!UICONTROL Logins]** en selecteren **[!UICONTROL New Login]**.
1. Voer de volledige naam van de toepassingpool in.

   Standaard krijgt de identiteit van de toepassingspool een naam na de toepassingspool. Als u `dashboard`, wordt de naam van de identiteit gewijzigd `IIS AppPool\dashboard`. 1. Selecteren **[!UICONTROL Server Roles]** en de **[!UICONTROL dbcreator]** rol.
1. Klikken **[!UICONTROL OK]** om de nieuwe gebruiker toe te voegen.
