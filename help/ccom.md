---
title: CCOM
description: Hilfeseite zum Mustererkennungs-Code
translation-type: ht
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: ht
source-wordcount: '201'
ht-degree: 100%

---


# CCOM {#ccom}

Benutzerdefinierte Komponente

## Hintergrund {#background}

`CCOM` steht für benutzerdefinierte Komponenten, die in AEM installiert wurden. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt.

Ein Untertyp wird mit diesem Code verwendet, um die Kategorie der Komponente zu unterscheiden:

* `custom.core`: Ein Übertyp in der Kette der Übertypen der Komponente enthält „core/wcm/components/“ und zeigt damit an, dass er von einer Kernkomponente erbt.
* `custom.foundation`: Ein Übertyp in der Kette der Übertypen der Komponente enthält „core/wcm/components/“ und zeigt damit an, dass er von einer Kernkomponente erbt.
* `custom.overlay.foundation`: Der Komponentenpfad enthält „wcm/foundation/components/“ oder „foundation/components/“ und zeigt damit an, dass er eine Basiskomponente überlagert.
* `custom`: Die benutzerdefinierte Komponente übernimmt oder überlagert keine Kern- oder Basiskomponente.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Best Practice ist es, die Anzahl der benutzerdefinierten Komponenten zu minimieren, Kernkomponenten zu nutzen und Kernkomponenten mit dem Stilsystem zu verwenden, um technische Altlasten zu reduzieren.

## Mögliche Lösungen {#solutions}

* Weitere Informationen zu Kernkomponenten finden Sie unter [Einführung in Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=de).
* Weitere Informationen zum Stilsystem finden Sie unter [Verwenden des Stilsystems](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=de#page-authoring).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
