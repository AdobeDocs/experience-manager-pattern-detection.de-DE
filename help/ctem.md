---
title: CTEM
description: Hilfeseite zum Mustererkennungs-Code
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 100%

---

# CTEM {#ctem}

Benutzerdefinierte Vorlage

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Benutzerdefinierte Vorlage"
>abstract="CTEM kennzeichnet benutzerdefinierte Komponenten, die in AEM installiert wurden. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt"

`CTEM` kennzeichnet benutzerdefinierte Vorlagen, die in AEM installiert wurden. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt.

Vorlagen werden durch einen primären Typwert von „cq:Template“ identifiziert. Um die Kategorien der Vorlage zu unterscheiden, werden Untertypen mit diesen Codes verwendet:

* `custom.editable.template`: Der Pfad der Vorlage beginnt nicht mit „/apps“.
* `custom.static.template`: Der Pfad der Vorlage beginnt mit „/apps“.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, alle statischen Vorlagen in bearbeitbare Vorlagen zu verschieben. Kunden können vorhandene AEM-Modernisierungs-Tools nutzen, um statische Vorlagen zu bearbeitbaren Vorlagen zu migrieren."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html" text="Bearbeitbare Vorlagen"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-Modernisierungs-Tools"

* Best Practice ist es, alle statischen Vorlagen in bearbeitbare Vorlagen zu verschieben.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Tools und Ressourcen"
>abstract="Mit Hilfe der AEM Modernization Suite können Kunden die Struktur einer Seite von einer statischen Definition hin zu einer bearbeitbaren Vorlage verändern. Dies soll Kunden dabei helfen, von den begrenzten Möglichkeiten der alten Funktionen zu den robusten, modernen AEM-Angeboten zu wechseln. Diese Tools sind konfigurierbar, konfigurationssensitiv und erweiterbar. Wenden Sie sich an den Adobe Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/page-structure.html" text="Seitenstrukturkonvertierer"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Nutzen Sie die [AEM-Modernisierungs-Tools](https://opensource.adobe.com/aem-modernize-tools/), um statische Vorlagen zu bearbeitbaren Vorlagen zu migrieren.
* Weitere Informationen zu bearbeitbaren Vorlagen finden Sie unter [Vorlagen](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html?lang=de).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
