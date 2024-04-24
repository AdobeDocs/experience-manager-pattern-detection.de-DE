---
title: DM
description: Erfahren Sie, wie der Mustererkennungscode die Verwendung von AEM Assets - Dynamic Media identifiziert.
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 52%

---

# DM {#dm}

Dynamic Media

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="DM-Code kennzeichnet die Nutzung von AEM Assets Dynamic Media in Ihrer aktuellen Implementierung. Der Dynamic Media-Modus wird vom Ausführungsmodus erkannt."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="AEM-Entwicklung – Richtlinien und Best Practices"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Entwicklungsrichtlinien für AEM as a Cloud Service"

`DM` (Dynamic Media) Gibt die Verwendung von AEM Assets Dynamic Media an. Der Dynamic Media-Modus wird vom Ausführungsmodus erkannt.

Bei diesem Code wird ein Untertyp verwendet:

* `dynamic.media.runmode`: Der zugehörige Wert dieses Untertyps, sofern vorhanden, lautet entweder:
   * `dynamicmedia`: Dynamic Media – Hybridmodus oder
   * `dynamicmedia_scene7`: Modus Dynamic Media - Scene7

## Mögliche Implikationen und Risiken {#implications-and-risks}

* `dynamic.media.runmode`
   * Bei Upgrades kann es Probleme im Zusammenhang mit Dynamic Media geben.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Implementierungsleitlinien"
>abstract="AEM as a Cloud Service unterstützt nur den Ausführungsmodus dynamicmedia_scene7 . Überprüfen Sie die aktuellen Einstellungen und wenden Sie sich an das Adobe Support-Team, um Hilfe und Erläuterungen zu erhalten."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media" text="Einrichten von Dynamic Media"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"


* `dynamic.media.runmode`
   * Weitere Informationen unter [Einrichten von Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media).

* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) wenn Sie Klarstellungen oder angesprochene Bedenken benötigen.
