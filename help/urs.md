---
title: URS
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# URS {#urs}

Nicht unterstützte Repository-Struktur

## Hintergrund {#background}

`URS` identifiziert Fälle nicht unterstützter Repository-Struktur. Ab AEM 6.4 wurden Leitlinien für die Umstrukturierung von Repository-Inhalten festgelegt. Indem Hierarchien für AEM Produktcode und Kundencode klar definiert und Konflikte zwischen ihnen vermieden werden, werden Inhalte aus `/etc` in andere Ordner im Repository umstrukturiert, wobei die folgenden Regeln auf hoher Ebene beachtet werden:

* AEM Produktcode wird immer in `/libs` platziert, der nicht durch benutzerdefinierten Code überschrieben werden darf Benutzerspezifischer Code sollte in `/apps`, `/content` und `/conf` platziert werden.
* Es wird dringend empfohlen, dass diese Leitlinien AEM Cloud Service befolgt werden.

Untertypen werden verwendet, um die spezifischen Typen von Repository-Problemen zu identifizieren, die behandelt werden sollten:
* `clientlibs.location`: Eine Client-Bibliothek, die auf  `/etc` den Pfad verweist.
* `file.location`: Eine Datei,  `/etc` die seit der Installation geändert wurde.
* `node.location`: Ein Knoten, unter  `/etc` dem seit der Installation Änderungen vorgenommen wurden.
* `workflow.location`: Ein Workflow-Modell oder Starter unter  `/etc/workflow`.
* `package.structure`: Ein Paket, das sowohl veränderlichen als auch unveränderlichen Inhalt enthält.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Benutzerspezifischer Code, der auf älteren Pfaden basiert, kann unerwünschtes Verhalten verursachen und die Produktfunktionalität beeinträchtigen.
* Pakete, die sowohl veränderlichen als auch unveränderlichen Inhalt enthalten, verursachen bei der Bereitstellung wahrscheinlich Probleme.

## Mögliche Lösungen {#solutions}

* Eine Anleitung zur Vorbereitung auf AEM als Cloud Service finden Sie unter [Repository Restructuring](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html).
* Weitere Informationen zu veränderlichen und unveränderlichen Bereichen des Repositorys finden Sie unter [AEM Projektstruktur](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html).
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
* Nutzen Sie den [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools), um bestehende Projektpakete umzustrukturieren, indem Sie Inhalt und Code in separate Pakete unterteilen, um mit der Projektstruktur kompatibel zu sein, die für Adobe Experience Manager als Cloud Service definiert wurde.