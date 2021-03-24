---
title: INST
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---


# INST {#inst}

Installiertes Artefakt

## Hintergrund {#background}

`INST` identifiziert benutzerdefinierte Pakete und Pakete von Drittanbietern, die vom Kunden in AEM installiert wurden. Diese werden berichtet, um den Zustand des Systems im allgemeinen Umfang eines Aktualisierungsaufwands zu charakterisieren.

Wenn mehrere Versionen eines Pakets installiert wurden, wird nur die neueste Version gemeldet.

Pakete und Pakete, die erkannt werden, wurden nicht unbedingt für AEM als Cloud Service optimiert. Alle Pakete von Drittanbietern sollten mit ihrem Ersteller oder ihrer Adobe auf Kompatibilität mit AEM als Cloud Service überprüft werden.

Untertypen werden zur Identifizierung verschiedener Arten von Informationen verwendet:

* `custom.bundle`: Ein in AEM installiertes Bundle.
* `custom.package`: Ein in AEM installiertes Paket.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Installation von Paketen von Drittanbietern mit CRX Package Manager ist in AEM als Cloud Service nicht möglich.
* Anwendungen, die von Drittanbieterpaketen abhängig sind, funktionieren möglicherweise erst erwartungsgemäß, wenn sie ordnungsgemäß bereitgestellt wurden, um mit AEM als Cloud Service zu arbeiten.
* Pakete von Drittanbietern, die nicht für AEM als Cloud-Dienst optimiert sind, können zu unerwünschtem Verhalten führen.

## Mögliche Lösungen {#solutions}

* Pakete von Drittanbietern sollten mit dem Cloud Manager [Bereitstellungsprozess](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html#deployment-process) als Teil des Projekts AEM bereitgestellt werden.
* Überprüfen Sie, wie Sie [Drittanbieter-Pakete](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embedding-3rd-party-packages) in Ihr Projekt einbetten, um AEM als Cloud Service zu verwenden.
* Drittanbieterpakete müssen die AEM als Cloud Service [development](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) und [processing](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html)-Richtlinien einhalten.
* Überprüfen Sie das Projekt [work-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) und verstehen Sie, wie [INST-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) korrigiert und mit AEM als Cloud Service kompatibel gemacht werden können.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
