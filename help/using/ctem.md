---
title: CTEM
description: Mustererkennungscode Hilfeseite.
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 68%

---

# CTEM {#ctem}

Benutzerdefinierte Vorlage

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Benutzerdefinierte Vorlage"
>abstract="CTEM kennzeichnet benutzerdefinierte Komponenten, die in AEM installiert wurden. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt"

CTEM identifiziert benutzerdefinierte Vorlagen, die auf AEM installiert wurden. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt.

Vorlagen werden durch einen Primärtyp-Wert von `cq:Template`. Um die Kategorien der Vorlage zu unterscheiden, werden Untertypen mit diesen Codes verwendet:

* `custom.editable.template`: Der Pfad der Vorlage beginnt nicht mit „/apps“.
* `custom.static.template`: Der Pfad der Vorlage beginnt mit „/apps“.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, alle statischen Vorlagen in bearbeitbare Vorlagen zu verschieben. Kunden können vorhandene AEM-Modernisierungs-Tools verwenden, um statische Vorlagen zu bearbeitbaren Vorlagen zu migrieren."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/templates/templates" text="Bearbeitbare Vorlagen"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-Modernisierungs-Tools"

* Best Practice ist es, alle statischen Vorlagen in bearbeitbare Vorlagen zu verschieben.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Tools und Ressourcen"
>abstract="Mit Hilfe der AEM Modernization Suite können Kunden die Struktur einer Seite von einer statischen Definition hin zu einer bearbeitbaren Vorlage verändern. Dies soll Kunden dabei helfen, von den begrenzten Möglichkeiten der alten Funktionen zu den robusten, modernen AEM-Angeboten zu wechseln. Diese Tools sind konfigurierbar, konfigurationsabhängig und erweiterbar. Wenden Sie sich an den Adobe-Support , um Hilfe oder Erläuterungen zu erhalten."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/structure/about.html" text="Seitenstrukturkonvertierer"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Verwenden Sie die [AEM Modernisierungs-Tools](https://opensource.adobe.com/aem-modernize-tools/) Migration von statischen Vorlagen zu bearbeitbaren Vorlagen.
* Weitere Informationen zu bearbeitbaren Vorlagen finden Sie unter [Vorlagen](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/templates/templates).
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
