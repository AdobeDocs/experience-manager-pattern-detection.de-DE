---
title: INST
description: Mustererkennungscode Hilfeseite.
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 96%

---

# INST {#inst}

Installiertes Artefakt

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Installiertes Artefakt"
>abstract="INST kennzeichnet benutzerdefinierte Pakete und Bundles von Drittanbietern, die vom Kunden in AEM installiert wurden. Diese sollen helfen, den Zustand des Systems und den allgemeinen Umfang eines Upgrades zu charakterisieren. Pakete von Drittanbietern müssen die Richtlinien von AEM as a Cloud Service für die Entwicklung und Bündelung einhalten."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=de" text="Entwicklungsrichtlinien – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html?lang=de" text="Bündelungsrichtlinien – AEM as a Cloud Service"

`INST` kennzeichnet benutzerdefinierte Pakete und Bundles von Drittanbietern, die vom Kunden in AEM installiert wurden. Diese sollen helfen, den Zustand des Systems und den allgemeinen Umfang eines Upgrades zu charakterisieren.

Wenn mehrere Versionen eines Package installiert wurden, wird nur die neueste Version gemeldet.

Packages und Bundles, die erkannt werden, sind nicht unbedingt für AEM as a Cloud Service optimiert worden. Jedes Package eines Drittanbieters sollte bei seinem Ersteller oder bei Adobe auf Kompatibilität mit AEM as a Cloud Service überprüft werden.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `custom.bundle`: Ein in AEM installiertes Bundle.
* `custom.package`: Ein in AEM installiertes Package.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Implementierungsleitlinien"
>abstract="Kunden können mit CRX Package Manager keine Pakete von Drittanbietern mehr installieren. Kunden sollten diese installierten Artefakte überprüfen und müssen sie für das Funktionieren mit AEM as a Cloud Service strukturieren und optimieren. Jedes Package eines Drittanbieters sollte bei seinem Ersteller oder bei Adobe auf Kompatibilität mit AEM as a Cloud Service überprüft werden."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de#embeddeds" text="Einbetten von Unterpaketen in das Container-Paket"


* Die Installation von Packages von Drittanbietern mithilfe von CRX Package Manager ist in AEM as a Cloud Service nicht möglich.
* Programme, die von Packages von Drittanbietern abhängig sind, funktionieren möglicherweise nicht wie erwartet, bis sie korrekt für die Arbeit mit AEM as a Cloud Service bereitgestellt wurden.
* Packages von Drittanbietern, die nicht für AEM as a Cloud Service optimiert sind, können zu unerwünschtem Verhalten führen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Tools und Ressourcen"
>abstract="Überprüfen Sie das Projekt WKND-legacy und verstehen Sie, wie INST-Verletzungen korrigiert und mit AEM Cloud Service kompatibel gemacht werden können. Prüfen Sie außerdem das Beispiel für INST-Verletzungen auf Github, um zu verstehen, wie dies korrigiert und in AEM as a Cloud Service bereitgestellt werden kann."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="WKND-Legacy-Projekt"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Beispiel für INST-Verletzungen – Github"

* Packages von Drittanbietern sollten als Teil des Projekts mithilfe des Cloud Manager-[Bereitstellungsprozesses](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html?lang=de#deployment-process) in AEM bereitgestellt werden.
* Überprüfen Sie, wie die [Einbettung von Drittanbieter-Packages](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de#embedding-3rd-party-packages) in Ihr Projekt für AEM as a Cloud Service erfolgt.
* Packages von Drittanbietern müssen die Richtlinien von AEM as a Cloud Service für die [Entwicklung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=de) und [Bündelung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html?lang=de) einhalten.
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) und verstehen Sie, wie [INST-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
