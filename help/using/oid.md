---
title: OID
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 99%

---

# OID {#oid}

Oak-Indexdefinition

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Oak-Indexdefinition"
>abstract="OID kennzeichnet Probleme im Zusammenhang mit Oak-Indexdefinitionen. Es kennzeichnet Änderungen, die an Standard-Oak-Indexdefinitionen vorgenommen wurden. Außerdem kennzeichnet es benutzerdefinierte Oak-Indexdefinitionen, die mit AEM as a Cloud Service nicht kompatibel sind. Die Meldung für jedes OID-Ergebnis bezeichnet den Index und liefert zusätzliche Informationen."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/operations/indexing#how-to-use" text="Richtlinien für die Indizierung von Inhalten"

`OID` identifiziert Probleme im Zusammenhang mit Oak-Indexdefinitionen. Es kennzeichnet Änderungen, die an Standard-Oak-Indexdefinitionen vorgenommen wurden. Außerdem kennzeichnet es benutzerdefinierte Oak-Indexdefinitionen, die mit AEM as a Cloud Service nicht kompatibel sind. Die Meldung für jeden `OID`-Fund identifiziert den Index und bietet zusätzliche Informationen.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `index.rule.violation`: Ein benutzerdefinierter Oak-Index ist mit AEM as a Cloud Service nicht kompatibel
* `standard.index.modification`: Eine Änderung an einem Standard-Oak-Index.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, alle benutzerdefinierten Indizes zu überprüfen und gemäß den Richtlinien zur Indizierung von Inhalten neu zu erstellen. Verwenden Sie den Index Converter, um vorhandene benutzerdefinierte Oak-Indexdefinitionen in mit AEM as a Cloud Service kompatible benutzerdefinierte Oak-Indexdefinitionen zu migrieren."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#oak-indexes" text="Richtlinien für das Erstellen von Paketen"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools" text="Index Converter"

* Änderungen an den Standard-Oak-Indexdefinitionen können bei einem AEM-Upgrade verloren gehen.
* Oak-Definitionen sind unveränderlich, sollten mit dem Code des Kundenprojekts gebündelt werden und nur mit Cloud Manager bereitgestellt werden.
* Alle Oak-Indexdefinitionen sollten der Benennungskonvention und anderen Regeln für Oak-Indizes in AEM as a Cloud Service folgen. Andernfalls kann es zu unerwünschtem Verhalten kommen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Tools und Ressourcen"
>abstract="Prüfen Sie das WKND-Legacy-Projekt, um zu verstehen, wie OID-Verletzungen in Ihrem Projekt behoben werden können. Überprüfen Sie außerdem das Beispiel einer OID-Verletzung auf GitHub, um zu verstehen, wie alte Indizes mithilfe des Tools Index Converter konvertiert und mit AEM as a Cloud Service kompatibel gemacht werden können."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="WKND-Legacy-Projekt"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Beispiel für OID-Verletzungen – GitHub"

* Beheben Sie die in der Meldung angegebenen Verstöße gegen die Indexregel.
* Um neue oder benutzerdefinierte Oak-Indexdefinitionen bereitzustellen, befolgen Sie die [Richtlinien zur Paketerstellung](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) von AEM as a Cloud Service.
* Angepasste AEM-Standardindizes und neue benutzerdefinierte Oak-Indexdefinitionen sollten den [Richtlinien zur Inhaltsindizierung](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/operations/indexing#preparing-the-new-index-definition) für AEM as a Cloud Service folgen.
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid), um zu verstehen, wie [OID-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
* Nutzen Sie den [Index Converter](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools), um vorhandene benutzerdefinierte Oak-Indexdefinitionen in mit AEM as a Cloud Service kompatible benutzerdefinierte Oak-Indexdefinitionen zu migrieren.
