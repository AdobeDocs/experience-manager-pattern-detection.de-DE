---
title: OID
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---


# OID {#oid}

Oak-Indexdefinition

## Hintergrund {#background}

`OID` identifiziert Probleme im Zusammenhang mit Oak-Indexdefinitionen. Er identifiziert Änderungen, die an den Standarddefinitionen für Oak-Indizes vorgenommen wurden. Er identifiziert außerdem benutzerdefinierte Oak-Indexdefinitionen, die mit AEM als Cloud Service unvereinbar sind. Die Meldung für jede `OID` Suche identifiziert den Index und stellt zusätzliche Informationen bereit.

Untertypen werden zur Identifizierung der verschiedenen Arten von Informationen verwendet:

* `custom.index.violation`: Ein benutzerdefinierter Oak-Index ist mit AEM als Cloud Service nicht kompatibel.
* `standard.index.modification`: Eine Änderung an einem Standard-Oak-Index.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Änderungen an Standarddefinitionen für Oak-Indizes gehen möglicherweise während einer AEM Aktualisierung verloren.
* Eichendefinitionen sind unveränderlich, sollten mit dem Kundenprojektcode verpackt und nur mit Cloud Manager bereitgestellt werden.
* Alle Oak-Indexdefinitionen sollten der Benennungsregel und anderen Regeln für Oak-Indizes in AEM als Cloud Service folgen. Diejenigen, die nicht zu unerwünschtem Verhalten führen können.

## Mögliche Lösungen {#solutions}

* Beheben Sie die in der Meldung angegebenen Verstöße gegen die Indexregel.
* Befolgen Sie AEM als Cloud Service [Verpackungsrichtlinien](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html), um neue oder benutzerdefinierte Oak-Indexdefinitionen bereitzustellen.
* Für benutzerdefinierte AEM und neue benutzerdefinierte Oak-Indexdefinitionen gelten die [Inhaltsindizierungsrichtlinien](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition) für AEM als Cloud Service.
* Überprüfen Sie das Projekt [work-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) und verstehen Sie, wie [OID-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) korrigiert und mit AEM als Cloud Service kompatibel gemacht werden können.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
* Verwenden Sie den [Indexkonverter](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools), um vorhandene Custom Oak Index-Definitionen zu migrieren, um sie als Cloud Service-kompatible Custom Oak Index-Definitionen zu AEM.
