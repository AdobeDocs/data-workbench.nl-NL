---
description: Alvorens het dashboard kan werken, moet u het toestaan om tot de SQL Server toegang te hebben.
title: De SQL Server configureren
uuid: bdd5f9f5-a69f-4001-9f80-901bd7eae129
exl-id: 16116cc8-f539-4cf0-ab1d-f2bddd39b38c
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Het vormen van SQL Server{#configuring-the-sql-server}

Alvorens het dashboard kan werken, moet u het toestaan om tot de SQL Server toegang te hebben.

1. Open de SQL Studio van het Beheer als Beheerder.
1. Voeg een nieuwe login toe door **[!UICONTROL Logins]** met de rechtermuisknop aan te klikken en **[!UICONTROL New Login]** te selecteren.
1. Voer de volledige naam van de toepassingpool in.

   Standaard krijgt de identiteit van de toepassingspool een naam na de toepassingspool. Als u `dashboard` kiest, dan zal de identiteit `IIS AppPool\dashboard` worden genoemd. 1. Selecteer **[!UICONTROL Server Roles]** en controleer de rol **[!UICONTROL dbcreator]**.
1. Klik **[!UICONTROL OK]** om de nieuwe gebruiker toe te voegen.
