---
title: PCX
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# PCX {#pcx}

Seitenkomplexität

## Hintergrund {#background}

`PCX` identifiziert Seiten, die eine große Anzahl von Knoten in ihrer Struktur enthalten.

Untertypen werden zur Identifizierung der verschiedenen Arten von Informationen verwendet:

* `page.complexity.medium`: Eine Seite enthält eine relativ hohe Anzahl von Knoten, die die Renderleistung beeinträchtigen können.
* `page.complexity.high`: Eine Seite enthält eine sehr hohe Anzahl von Knoten, die sich wahrscheinlich auf die Renderleistung auswirken werden.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Eine große Anzahl von Knoten auf einer Seite kann sich auf ihre Renderleistung auswirken.

## Mögliche Lösungen {#solutions}

* Führen Sie Schritte zur Verringerung der Gesamtzahl von Knoten auf einer Seite durch, darunter:
   * Stellen Sie sicher, dass es keine unnötigen Container gibt.
   * Testen Sie, ob dasselbe Layout mit weniger Containern erreicht werden kann.
   * Vereinfachen Sie den Seiteninhalt.
   * Verringern Sie die Tiefe der Knotenstruktur.
   * Machen Sie alle enthaltenen Erlebnisfragmente zur Einfachheit neu.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
