---
title: CCOM
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 60%

---

# CCOM {#ccom}

Benutzerdefinierte Komponente

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Benutzerdefinierte Komponente"
>abstract="CCOM identifiziert benutzerdefinierte Komponenten, die auf AEM installiert sind. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt"

`CCOM` Identifiziert benutzerdefinierte Komponenten, die auf AEM installiert sind. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt.

Ein Untertyp wird mit diesem Code verwendet, um die Kategorie der Komponente zu unterscheiden:

* `custom.core`: Ein Supertyp in der Kette der Supertypen der Komponente enthält `core/wcm/components/`, was angibt, dass es von einer Kernkomponente erbt.
* `custom.foundation`: Ein Supertyp in der Kette der Supertypen der Komponente enthält &quot;`core/wcm/components/`, was angibt, dass es von einer Kernkomponente erbt.
* `custom.overlay.foundation`: Der Komponentenpfad enthält `wcm/foundation/components/` oder `foundation/components/`, wodurch angegeben wird, dass eine Foundation-Komponente überlagert wird.
* `custom`: Die benutzerdefinierte Komponente übernimmt oder überlagert keine Kern- oder Basiskomponente.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* Best Practice ist, die Anzahl der benutzerdefinierten Komponenten zu minimieren, Kernkomponenten zu verwenden und Kernkomponenten mit dem Stilsystem zu verwenden, damit Sie technische Schulden reduzieren können.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, die Anzahl der benutzerdefinierten Komponenten zu minimieren, Kernkomponenten zu nutzen und Kernkomponenten mit dem Stilsystem zu verwenden, um technische Altlasten zu reduzieren."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-core-components/using/introduction" text="Kernkomponenten"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring" text="Stilsystem"

* Weitere Informationen zu Kernkomponenten finden Sie unter [Einführung in Kernkomponenten](https://experienceleague.adobe.com/de/docs/experience-manager-core-components/using/introduction).
* Weitere Informationen zum Stilsystem finden Sie unter [Verwenden des Stilsystems](https://experienceleague.adobe.com/de/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
