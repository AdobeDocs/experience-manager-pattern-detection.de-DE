---
title: DM
description: Erfahren Sie, wie der Mustererkennungs-Code die Verwendung von AEM Assets – Dynamic Media identifiziert.
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '173'
ht-degree: 100%

---

# DM {#dm}

Dynamic Media

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="DM-Code kennzeichnet die Nutzung von AEM Assets Dynamic Media in Ihrer aktuellen Implementierung. Der Dynamic Media-Modus wird vom Ausführungsmodus erkannt."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="AEM-Entwicklung – Richtlinien und Best Practices"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Entwicklungsrichtlinien für AEM as a Cloud Service"

`DM` (Dynamic Media) erkennt die Verwendung von AEM Assets Dynamic Media. Der Dynamic Media-Modus wird vom Ausführungsmodus erkannt.

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
>abstract="AEM as a Cloud Service unterstützt nur den Ausführungsmodus dynamicmedia_scene7. Überprüfen Sie die aktuellen Einstellungen und wenden Sie sich an das Adobe-Supportteam, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media" text="Einrichten von Dynamic Media"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"


* `dynamic.media.runmode`
   * Weitere Informationen finden Sie unter [Einrichten von Dynamic Media](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media).

* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
