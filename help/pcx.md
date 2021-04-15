---
title: PCX
description: Hilfeseite zum Mustererkennungs-Code
translation-type: ht
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: ht
source-wordcount: '149'
ht-degree: 100%

---


# PCX {#pcx}

Seitenkomplexität

## Hintergrund {#background}

`PCX` Steht für Seiten, die eine große Anzahl von Knoten in ihrer Struktur enthalten.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `page.complexity.medium`: Eine Seite enthält eine mäßig hohe Anzahl von Knoten, was die Rendering-Leistung beeinträchtigen kann.
* `page.complexity.high`: Eine Seite enthält eine sehr hohe Anzahl von Knoten, was sich wahrscheinlich auf die Rendering-Leistung auswirken wird.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Eine große Anzahl von Knoten innerhalb einer Seite kann deren Rendering-Leistung beeinträchtigen.

## Mögliche Lösungen {#solutions}

* Ergreifen Sie Maßnahmen, um die Gesamtzahl der Knoten innerhalb einer Seite zu reduzieren, darunter:
   * Stellen Sie sicher, dass es keine unnötigen Container gibt.
   * Testen Sie, ob dasselbe Layout mit weniger Containern erreicht werden kann.
   * Vereinfachen Sie den Seiteninhalt.
   * Verringern Sie die Tiefe der Knotenstruktur.
   * Refaktorisieren Sie der Einfachheit halber alle enthaltenen Experience Fragments.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
