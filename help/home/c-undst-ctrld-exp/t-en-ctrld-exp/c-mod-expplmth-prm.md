---
description: De parameter ExpPartialMatch wijzigen (optioneel)
title: De parameter ExpPartialMatch wijzigen (optioneel)
uuid: 15ed33cc-5ec8-45b2-a4eb-d1941962ca9d
exl-id: 8ad45368-85a4-4865-b66b-52c29c28799c
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# De parameter ExpPartialMatch wijzigen (optioneel){#modifying-the-exppartialmatch-parameter-optional}

Als u gecontroleerde experimenten wilt toelaten om uw volledige website of een volledige subdirectory van uw website aan een andere plaats opnieuw toe te wijzen, kunt u de parameter ExpPartialMatch in het [!DNL txlogd.conf] dossier aan &quot;plaatsen.&quot; De standaardwaarde is &quot;uit&quot;.

Hieronder ziet u een voorbeeld van de parameter ExpPartialMatch:

[!DNL ExpPartialMatch off]

Wees zeer voorzichtig wanneer u deze parameter instelt op &quot;on&quot;, omdat dit kan leiden tot een onbedoelde hertoewijzing van uw gehele website.
