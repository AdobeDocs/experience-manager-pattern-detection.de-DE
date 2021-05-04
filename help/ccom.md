---
title: CCOM
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 95%

---

# CCOM {#ccom}

Benutzerdefinierte Komponente

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Benutzerdefinierte Komponente"
>abstract="CCOM identifiziert benutzerdefinierte Komponenten, die auf AEM installiert wurden. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt"

`CCOM` steht für benutzerdefinierte Komponenten, die in AEM installiert wurden. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt.

Ein Untertyp wird mit diesem Code verwendet, um die Kategorie der Komponente zu unterscheiden:

* `custom.core`: Ein Übertyp in der Kette der Übertypen der Komponente enthält „core/wcm/components/“ und zeigt damit an, dass er von einer Kernkomponente erbt.
* `custom.foundation`: Ein Übertyp in der Kette der Übertypen der Komponente enthält „core/wcm/components/“ und zeigt damit an, dass er von einer Kernkomponente erbt.
* `custom.overlay.foundation`: Der Komponentenpfad enthält „wcm/foundation/components/“ oder „foundation/components/“ und zeigt damit an, dass er eine Basiskomponente überlagert.
* `custom`: Die benutzerdefinierte Komponente übernimmt oder überlagert keine Kern- oder Basiskomponente.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Best Practice ist es, die Anzahl der benutzerdefinierten Komponenten zu minimieren, Kernkomponenten zu nutzen und Kernkomponenten mit dem Stilsystem zu verwenden, um technische Altlasten zu reduzieren.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Durchführungsleitlinien"
>abstract="Best Practice ist es, die Anzahl der benutzerdefinierten Komponenten zu minimieren, Kernkomponenten zu nutzen und Kernkomponenten mit dem Stilsystem zu verwenden, um technische Altlasten zu reduzieren."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html" text="Kernkomponenten"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring" text="Stilsystem"

* Weitere Informationen zu Kernkomponenten finden Sie unter [Einführung in Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=de).
* Weitere Informationen zum Stilsystem finden Sie unter [Verwenden des Stilsystems](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=de#page-authoring).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
