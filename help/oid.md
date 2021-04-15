---
title: OID
description: Hilfeseite zum Mustererkennungs-Code
translation-type: ht
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: ht
source-wordcount: '298'
ht-degree: 100%

---


# OID {#oid}

Oak-Indexdefinition

## Hintergrund {#background}

`OID` steht für Probleme im Zusammenhang mit Oak-Indexdefinitionen. Es identifiziert Änderungen, die an Standard-Oak-Indexdefinitionen vorgenommen wurden. Außerdem identifiziert es benutzerdefinierte Oak-Indexdefinitionen, die mit AEM as a Cloud Service nicht kompatibel sind. Die Meldung für jedes `OID`-Ergebnis bezeichnet den Index und liefert zusätzliche Informationen.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `custom.index.violation`: Ein benutzerdefinierter Oak-Index ist mit AEM as a Cloud Service nicht kompatibel.
* `standard.index.modification`: Eine Änderung an einem Standard-Oak-Index.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Änderungen an den Standard-Oak-Indexdefinitionen können bei einem AEM-Upgrade verloren gehen.
* Oak-Definitionen sind unveränderlich, sollten mit dem Code des Kundenprojekts gebündelt werden und nur mit Cloud Manager implementiert werden.
* Alle Oak-Indexdefinitionen sollten der Benennungskonvention und anderen Regeln für Oak-Indizes in AEM as a Cloud Service folgen. Diejenigen, die dies nicht tun, können unerwünschtes Verhalten verursachen.

## Mögliche Lösungen {#solutions}

* Beheben Sie die in der Meldung angegebenen Verstöße gegen die Indexregel.
* Befolgen Sie die [Bündelungsrichtlinien](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de) von AEM as a Cloud Service, um neue oder benutzerdefinierte Oak-Indexdefinitionen zu implementieren.
* Angepasste AEM-Standardindizes und neue benutzerdefinierte Oak-Indexdefinitionen sollten den [Richtlinien zur Inhaltsindizierung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=de#preparing-the-new-index-definition) für AEM as a Cloud Service folgen.
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) und verstehen Sie, wie [OID-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
* Nutzen Sie [Index Converter](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html?lang=de#refactoring-tools), um vorhandene benutzerdefinierte Oak-Indexdefinitionen in mit AEM as a Cloud Service kompatible benutzerdefinierte Oak-Indexdefinitionen zu migrieren.
