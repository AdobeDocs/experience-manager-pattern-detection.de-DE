---
title: CCOM
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---


# CCOM {#ccom}

Benutzerdefinierte Komponente

## Hintergrund {#background}

`CCOM` identifiziert benutzerdefinierte Komponenten, die auf AEM installiert wurden. Diese Informationen werden für die Zwecke der Bewertung bewährter Verfahren bereitgestellt.

Ein Untertyp wird mit diesem Code zur Identifizierung der Kategorie der Komponente verwendet:

* `custom.core`: Ein Supertyp in der Kette der Supertypen der Komponente enthält &quot;core/wcm/components/&quot;, was anzeigt, dass er von einer Kernkomponente übernommen wird.
* `custom.foundation`: Ein Supertyp in der Kette der Supertypen der Komponente enthält &quot;core/wcm/components/&quot;, was anzeigt, dass er von einer Kernkomponente übernommen wird.
* `custom.overlay.foundation`: Der Komponentenpfad enthält &quot;wcm/foundation/components/&quot;oder &quot;foundation/components/&quot;, was angibt, dass eine Basiskomponente überlagert wird.
* `custom`: Die benutzerdefinierte Komponente übernimmt oder überlagert keine Kern- oder Basiskomponente.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Best Practice ist die Minimierung der Anzahl von benutzerdefinierten Komponenten, die Nutzung von Kernkomponenten und die Verwendung von Kernkomponenten mit dem Stilsystem, um technische Schulden zu reduzieren.

## Mögliche Lösungen {#solutions}

* Weitere Informationen zu Kernkomponenten finden Sie unter [Einführung zu Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=de).
* Weitere Informationen zum Stilsystem finden Sie unter [Verwenden des Stilsystems](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring).
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
