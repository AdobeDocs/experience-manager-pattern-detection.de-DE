---
title: DM
description: Hilfeseite zum Mustererkennungs-Code
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 100%

---

# DM {#dm}

Dynamic Media

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="DM-Code kennzeichnet die Nutzung von AEM Assets Dynamic Media in Ihrer aktuellen Implementierung. Der Dynamic Media-Modus wird vom Ausführungsmodus erkannt."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html?lang=de" text="AEM-Entwicklung – Richtlinien und Best Practices"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=de" text="Entwicklungsrichtlinien für AEM as a Cloud Service"

`DM` kennzeichnet die Verwendung von AEM Assets Dynamic Media. Der Dynamic Media-Modus wird vom Ausführungsmodus erkannt.

Bei diesem Code wird ein Untertyp verwendet:

* `dynamic.media.runmode`: Der zugehörige Wert dieses Untertyps, sofern vorhanden, lautet entweder:
   * `dynamicmedia`: Dynamic Media – Hybridmodus oder
   * `dynamicmedia_scene7`: Dynamic Media – Scene7-Modus

## Mögliche Implikationen und Risiken {#implications-and-risks}

* `dynamic.media.runmode`
   * Bei Upgrades kann es Probleme im Zusammenhang mit Dynamic Media geben.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Implementierungsleitlinien"
>abstract="AEM as a Cloud Service unterstützt nur den Ausführungsmodus dynamicmedia_scene7. Überprüfen Sie die aktuellen Einstellungen und wenden Sie sich an das Adobe Support-Team, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html?lang=de" text="Einrichten von Dynamic Media"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"


* `dynamic.media.runmode`
   * Weitere Informationen finden Sie unter [Einrichten von Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html?lang=de).

* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
