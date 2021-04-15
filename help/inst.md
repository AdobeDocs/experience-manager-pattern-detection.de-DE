---
title: INST
description: Hilfeseite zum Mustererkennungs-Code
translation-type: ht
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: ht
source-wordcount: '315'
ht-degree: 100%

---


# INST {#inst}

Installiertes Artefakt

## Hintergrund {#background}

`INST` stellt benutzerdefinierte Packages und Bundles von Drittanbietern fest, die vom Kunden in AEM installiert wurden. Diese werden berichtet, um dabei zu helfen, den Zustand des Systems und den allgemeinen Umfang eines Upgrades zu charakterisieren.

Wenn mehrere Versionen eines Package installiert wurden, wird nur die neueste Version gemeldet.

Packages und Bundles, die erkannt werden, sind nicht unbedingt für AEM as a Cloud Service optimiert worden. Jedes Package eines Drittanbieters sollte bei seinem Ersteller oder bei Adobe auf Kompatibilität mit AEM as a Cloud Service überprüft werden.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `custom.bundle`: Ein in AEM installiertes Bundle.
* `custom.package`: Ein in AEM installiertes Package.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Installation von Packages von Drittanbietern mithilfe von CRX Package Manager ist in AEM as a Cloud Service nicht möglich.
* Programme, die von Packages von Drittanbietern abhängig sind, funktionieren möglicherweise nicht wie erwartet, bis sie korrekt für die Arbeit mit AEM as a Cloud Service implementiert wurden.
* Packages von Drittanbietern, die nicht für AEM as a Cloud Service optimiert sind, können zu unerwünschtem Verhalten führen.

## Mögliche Lösungen {#solutions}

* Packages von Drittanbietern sollten als Teil des Projekts mithilfe des Cloud Manager-[Implementierungsprozesses](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html?lang=de#deployment-process) in AEM implementiert werden.
* Überprüfen Sie, wie die [Einbettung von Drittanbieter-Packages](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de#embedding-3rd-party-packages) in Ihr Projekt für AEM as a Cloud Service erfolgt.
* Packages von Drittanbietern müssen die Richtlinien von AEM as a Cloud Service für die [Entwicklung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=de) und [Bündelung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html?lang=de) einhalten.
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) und verstehen Sie, wie [INST-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
