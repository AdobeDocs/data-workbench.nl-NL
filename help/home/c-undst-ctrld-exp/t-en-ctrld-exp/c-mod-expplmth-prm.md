---
description: De parameter ExpPartialMatch wijzigen (optioneel)
title: De parameter ExpPartialMatch wijzigen (optioneel)
uuid: 15ed33cc-5ec8-45b2-a4eb-d1941962ca9d
exl-id: 8ad45368-85a4-4865-b66b-52c29c28799c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# De parameter ExpPartialMatch wijzigen (optioneel){#modifying-the-exppartialmatch-parameter-optional}

{{eol}}

Als u gecontroleerde experimenten wilt toelaten om uw volledige website of een volledige subdirectory van uw website aan een andere plaats opnieuw in kaart te brengen, kunt u de parameter ExpPartialMatch in plaatsen [!DNL txlogd.conf] bestand aan &quot;on.&quot; De standaardwaarde is &quot;uit&quot;.

Hieronder ziet u een voorbeeld van de parameter ExpPartialMatch:

[!DNL ExpPartialMatch off]

Wees zeer voorzichtig wanneer u deze parameter instelt op &quot;on&quot;, omdat dit kan leiden tot een onbedoelde hertoewijzing van uw gehele website.
