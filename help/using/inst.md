---
title: INST
description: Mustererkennungscode Hilfeseite.
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 73%

---

# INST {#inst}

Installiertes Artefakt

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Installiertes Artefakt"
>abstract="INST kennzeichnet benutzerdefinierte Pakete und Bundles von Drittanbietern, die vom Kunden in AEM installiert wurden. Diese sollen helfen, den Zustand des Systems und den allgemeinen Umfang eines Upgrades zu charakterisieren. Pakete von Drittanbietern müssen die Richtlinien von AEM as a Cloud Service für die Entwicklung und Bündelung einhalten."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Entwicklungsrichtlinien – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package" text="Bündelungsrichtlinien – AEM as a Cloud Service"

`INST`  Identifiziert benutzerdefinierte Pakete und Pakete von Drittanbietern, die vom Kunden in AEM installiert wurden. Diese sollen helfen, den Zustand des Systems und den allgemeinen Umfang eines Upgrades zu charakterisieren.

Wenn mehrere Versionen eines Package installiert wurden, wird nur die neueste Version gemeldet.

Packages und Bundles, die erkannt werden, sind nicht unbedingt für AEM as a Cloud Service optimiert worden. Jedes Package eines Drittanbieters sollte bei seinem Ersteller oder bei Adobe auf Kompatibilität mit AEM as a Cloud Service überprüft werden.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `custom.bundle`: Ein in AEM installiertes Bundle.
* `custom.package`: Ein in AEM installiertes Package.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Implementierungsleitlinien"
>abstract="Kunden können Pakete von Drittanbietern nicht mehr mit CRX Package Manager installieren. Kunden sollten diese installierten Artefakte überprüfen, die strukturiert sein müssen, und sie so optimieren, dass sie mit AEM as a Cloud Service funktionieren. Überprüfen Sie jedes Drittanbieterpaket entweder mit dem Ersteller oder mit Adobe auf Kompatibilität mit AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embeddeds" text="Einbetten von Unterpaketen in das Container-Paket"


* Die Installation von Packages von Drittanbietern mithilfe von CRX Package Manager ist in AEM as a Cloud Service nicht möglich.
* Programme, die von Packages von Drittanbietern abhängig sind, funktionieren möglicherweise nicht wie erwartet, bis sie korrekt für die Arbeit mit AEM as a Cloud Service bereitgestellt wurden.
* Packages von Drittanbietern, die nicht für AEM as a Cloud Service optimiert sind, können zu unerwünschtem Verhalten führen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Tools und Ressourcen"
>abstract="Überprüfen Sie das Projekt WKND-legacy und verstehen Sie, wie INST-Verletzungen korrigiert und mit AEM Cloud Service kompatibel gemacht werden können. Sehen Sie sich auch das Beispiel einer INST-Verletzung auf GitHub an, um zu verstehen, wie dies in AEM as a Cloud Service korrigiert und bereitgestellt werden kann."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="WKND-Legacy-Projekt"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Beispiel einer INST-Verletzung - GitHub"

* Packages von Drittanbietern sollten als Teil des Projekts mithilfe des Cloud Manager-[Bereitstellungsprozesses](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deployment-process) in AEM bereitgestellt werden.
* Überprüfen Sie, wie die [Einbettung von Drittanbieter-Packages](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embedding-3rd-party-packages) in Ihr Projekt für AEM as a Cloud Service erfolgt.
* Packages von Drittanbietern müssen die Richtlinien von AEM as a Cloud Service für die [Entwicklung](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines) und [Bündelung](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package) einhalten.
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) und verstehen Sie, wie [INST-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
