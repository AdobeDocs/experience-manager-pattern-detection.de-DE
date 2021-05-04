---
title: CTEM
description: Hilfeseite zum Mustererkennungs-Code
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 67%

---

# CTEM {#ctem}

Benutzerdefinierte Vorlage

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Benutzerdefinierte Vorlage"
>abstract="CTEM identifiziert benutzerdefinierte Komponenten, die auf AEM installiert wurden. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt"

`CTEM` steht für benutzerdefinierte Vorlagen, die in AEM installiert wurden. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt.

Vorlagen werden durch einen primären Typwert von „cq:Template“ identifiziert. Um die Kategorien der Vorlage zu unterscheiden, werden Untertypen mit diesen Codes verwendet:

* `custom.editable.template`: Der Pfad der Vorlage beginnt nicht mit „/apps“.
* `custom.static.template`: Der Pfad der Vorlage beginnt mit „/apps“.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Durchführungsleitlinien"
>abstract="Best Practice ist, alle statischen Vorlagen in bearbeitbare Vorlagen zu verschieben. Kunden können vorhandene AEM Modernisierungstools nutzen, um statische Vorlagen zu bearbeitbaren Vorlagen zu migrieren."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html" text="Bearbeitbare Vorlagen"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-Modernisierungs-Tools"

* Best Practice ist, alle statischen Vorlagen in bearbeitbare Vorlagen zu verschieben.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Tools und Ressourcen"
>abstract="Mithilfe der AEM Moderations Suite können Kunden die Struktur einer Seite von einer statischen Definition bis zu einer bearbeitbaren Vorlage bearbeiten. Ziel ist es, Kunden dabei zu unterstützen, von den eingeschränkten Funktionen der alten Funktionen zu den robusten, modernen AEM zu wechseln. Diese Tools sind konfigurierbar, konfigurationsbewusst und erweiterbar. Support zur Adobe für Hilfe und Klarstellungen"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/page-structure.html" text="Seitenstrukturkonverter"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-Support"

* Nutzen Sie die [AEM-Modernisierungs-Tools](https://opensource.adobe.com/aem-modernize-tools/), um statische Vorlagen zu bearbeitbaren Vorlagen zu migrieren.
* Weitere Informationen zu bearbeitbaren Vorlagen finden Sie unter [Vorlagen](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html?lang=de).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
