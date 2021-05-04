---
title: PCX
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 74%

---

# PCX {#pcx}

Seitenkomplexität

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Seitenkomplexität"
>abstract="PCX identifiziert Seiten, die eine große Anzahl von Knoten in ihrer Struktur enthalten."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de" text="Bemerkenswerte Änderungen - AEM als Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de" text="AEM als Cloud Service - Versionshinweise"

`PCX` Steht für Seiten, die eine große Anzahl von Knoten in ihrer Struktur enthalten.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `page.complexity.medium`: Eine Seite enthält eine mäßig hohe Anzahl von Knoten, was die Rendering-Leistung beeinträchtigen kann.
* `page.complexity.high`: Eine Seite enthält eine sehr hohe Anzahl von Knoten, was sich wahrscheinlich auf die Rendering-Leistung auswirken wird.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Eine große Anzahl von Knoten innerhalb einer Seite kann deren Rendering-Leistung beeinträchtigen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Durchführungsleitlinien"
>abstract="Best Practice ist die Inhaltsstruktur überprüfen, um die Komplexität der Seite zu reduzieren. Dies würde wiederum zur Verbesserung der Seitenwiedergabeleistung beitragen. Support zur Adobe für Hilfe und Klarstellungen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-Support"

* Ergreifen Sie Maßnahmen, um die Gesamtzahl der Knoten innerhalb einer Seite zu reduzieren, darunter:
   * Stellen Sie sicher, dass es keine unnötigen Container gibt.
   * Testen Sie, ob dasselbe Layout mit weniger Containern erreicht werden kann.
   * Vereinfachen Sie den Seiteninhalt.
   * Verringern Sie die Tiefe der Knotenstruktur.
   * Refaktorisieren Sie der Einfachheit halber alle enthaltenen Experience Fragments.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
