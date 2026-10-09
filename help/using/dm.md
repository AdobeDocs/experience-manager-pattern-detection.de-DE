---
title: DM
description: Erfahren Sie, wie der Mustererkennungs-Code die Verwendung von AEM Assets – Dynamic Media identifiziert.
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 100%
---
# DM {#dm}

Dynamic Media

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="DM-Code kennzeichnet die Nutzung von AEM Assets Dynamic Media in Ihrer aktuellen Implementierung. Der Ausführungsmodus erkennt den Dynamic Media-Modus."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="AEM-Entwicklung – Richtlinien und Best Practices"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Entwicklungsrichtlinien für AEM as a Cloud Service"

`DM` (Dynamic Media) erkennt die Verwendung von AEM Assets Dynamic Media. Der Ausführungsmodus erkennt den Dynamic Media-Modus.

Bei diesem Code wird ein Untertyp verwendet:

* `dynamic.media.runmode`: Der zugehörige Wert dieses Untertyps, sofern vorhanden, lautet entweder:
  * `dynamicmedia`: Dynamic Media – Hybridmodus oder
  * `dynamicmedia_scene7`: Dynamic Media – Scene7-Modus

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* `dynamic.media.runmode`
  * Bei Upgrades kann es Probleme im Zusammenhang mit Dynamic Media geben.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Implementierungsleitlinien"
>abstract="AEM as a Cloud Service unterstützt nur den Ausführungsmodus dynamicmedia_scene7. Bitte überprüfen Sie die aktuellen Einstellungen und wenden Sie sich an das Adobe-Support-Team, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media" text="Einrichten von Dynamic Media"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"


* `dynamic.media.runmode`
  * Weitere Informationen finden Sie unter [Einrichten von Dynamic Media](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media).

* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
