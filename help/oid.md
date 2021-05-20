---
title: OID
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 100%

---

# OID {#oid}

Oak-Indexdefinition

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Oak-Indexdefinition"
>abstract="OID kennzeichnet Probleme im Zusammenhang mit Oak-Indexdefinitionen. Es kennzeichnet Änderungen, die an Standard-Oak-Indexdefinitionen vorgenommen wurden. Außerdem kennzeichnet es benutzerdefinierte Oak-Indexdefinitionen, die mit AEM as a Cloud Service nicht kompatibel sind. Die Meldung für jedes OID-Ergebnis bezeichnet den Index und liefert zusätzliche Informationen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=de#how-to-use" text="Richtlinien für die Indizierung von Inhalten"

`OID` kennzeichnet Probleme im Zusammenhang mit Oak-Indexdefinitionen. Es kennzeichnet Änderungen, die an Standard-Oak-Indexdefinitionen vorgenommen wurden. Außerdem kennzeichnet es benutzerdefinierte Oak-Indexdefinitionen, die mit AEM as a Cloud Service nicht kompatibel sind. Die Meldung für jedes `OID`-Ergebnis bezeichnet den Index und liefert zusätzliche Informationen.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `custom.index.violation`: Ein benutzerdefinierter Oak-Index ist mit AEM as a Cloud Service nicht kompatibel.
* `standard.index.modification`: Eine Änderung an einem Standard-Oak-Index.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, alle benutzerdefinierten Indizes zu überprüfen und gemäß den Richtlinien zur Indizierung von Inhalten neu zu erstellen. Nutzen Sie den Index Converter, um vorhandene benutzerdefinierte Oak-Indexdefinitionen in mit AEM as a Cloud Service kompatible benutzerdefinierte Oak-Indexdefinitionen zu migrieren."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de#oak-indexes" text="Richtlinien für das Erstellen von Paketen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools" text="Index Converter"

* Änderungen an den Standard-Oak-Indexdefinitionen können bei einem AEM-Upgrade verloren gehen.
* Oak-Definitionen sind unveränderlich, sollten mit dem Code des Kundenprojekts gebündelt werden und nur mit Cloud Manager implementiert werden.
* Alle Oak-Indexdefinitionen sollten der Benennungskonvention und anderen Regeln für Oak-Indizes in AEM as a Cloud Service folgen. Diejenigen, die dies nicht tun, können unerwünschtes Verhalten verursachen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Tools und Ressourcen"
>abstract="Prüfen Sie das WKND-Legacy-Projekt, um zu verstehen, wie OID-Verletzungen in Ihrem Projekt behoben werden können. Überprüfen Sie außerdem das Beispiel einer OID-Verletzung auf Github, um zu verstehen, wie alte Indizes mithilfe des Tools Index Converter konvertiert und mit AEM as a Cloud Service kompatibel gemacht werden können."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="WKND-Legacy-Projekt"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Beispiel einer OID-Verletzung – Github"

* Beheben Sie die in der Meldung angegebenen Verstöße gegen die Indexregel.
* Befolgen Sie die [Bündelungsrichtlinien](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de) von AEM as a Cloud Service, um neue oder benutzerdefinierte Oak-Indexdefinitionen zu implementieren.
* Angepasste AEM-Standardindizes und neue benutzerdefinierte Oak-Indexdefinitionen sollten den [Richtlinien zur Inhaltsindizierung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=de#preparing-the-new-index-definition) für AEM as a Cloud Service folgen.
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) und verstehen Sie, wie [OID-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
* Nutzen Sie [Index Converter](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html?lang=de#refactoring-tools), um vorhandene benutzerdefinierte Oak-Indexdefinitionen in mit AEM as a Cloud Service kompatible benutzerdefinierte Oak-Indexdefinitionen zu migrieren.
