---
title: INST
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 90%

---

# INST {#inst}

Installiertes Artefakt

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Installiertes Artefakt"
>abstract="INST kennzeichnet benutzerdefinierte Pakete und Bundles von Drittanbietern, die von der Kundschaft in AEM installiert wurden. Diese Pakete und Bundles helfen, den Zustand des Systems und den allgemeinen Umfang eines Upgrades zu charakterisieren. Pakete von Drittanbietern müssen die Richtlinien von AEM as a Cloud Service für die Entwicklung und Bündelung einhalten."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Entwicklungsrichtlinien – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package" text="Bündelungsrichtlinien – AEM as a Cloud Service"

`INST` identifiziert benutzerdefinierte Pakete und Bundles von Drittanbietern, die von der Kundschaft in AEM installiert wurden. Diese Pakete und Bundles helfen, den Zustand des Systems und den allgemeinen Umfang eines Upgrades zu charakterisieren.

Wenn mehrere Versionen eines Package installiert wurden, wird nur die neueste Version gemeldet.

Packages und Bundles, die erkannt werden, sind nicht unbedingt für AEM as a Cloud Service optimiert worden. Jedes Package eines Drittanbieters sollte bei seinem Ersteller oder bei Adobe auf Kompatibilität mit AEM as a Cloud Service überprüft werden.

Um die verschiedenen Arten von Informationen zu erkennen, werden folgende Untertypen verwendet:

* `custom.bundle`: Ein in AEM installiertes Bundle.
* `custom.package`: Ein in AEM installiertes Package.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Implementierungsleitlinien"
>abstract="Kundinnen und Kunden können keine Pakete von Drittanbietern mehr mit dem CRX Package Manager installieren. Diese installierten Artefakte sollten überprüft werden und müssen für das Funktionieren mit AEM as a Cloud Service strukturiert und optimiert werden. Überprüfen Sie jedes Paket von Drittanbietern entweder bei seiner Erstellerin bzw. seinem Ersteller oder bei Adobe auf Kompatibilität mit AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embeddeds" text="Einbetten von Unterpaketen in das Container-Paket"


* Die Installation von Packages von Drittanbietern mithilfe von CRX Package Manager ist in AEM as a Cloud Service nicht möglich.
* Programme, die von Packages von Drittanbietern abhängig sind, funktionieren möglicherweise nicht wie erwartet, bis sie korrekt für die Arbeit mit AEM as a Cloud Service bereitgestellt wurden.
* Packages von Drittanbietern, die nicht für AEM as a Cloud Service optimiert sind, können zu unerwünschtem Verhalten führen.

Erwägen Sie außerdem, auf diese speziellen Untertypen zu achten:

* `guava.bundle` - Guava wird in AEM 6.5 LTS nicht standardmäßig unterstützt und das Bundle ist nach dem Upgrade nicht mehr verfügbar.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Tools und Ressourcen"
>abstract="Überprüfen Sie das Projekt WKND-legacy, um zu verstehen, wie INST-Verletzungen korrigiert und mit AEM Cloud Service kompatibel gemacht werden können. Schauen Sie sich außerdem das Beispiel für INST-Verletzungen auf GitHub an, um zu überblicken, wie dieses Problem korrigiert und die Bereitstellung in AEM as a Cloud Service erfolgen kann."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="WKND-Legacy-Projekt"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Beispiel für INST-Verletzungen – GitHub"

* Packages von Drittanbietern sollten als Teil des Projekts mithilfe des Cloud Manager-[Bereitstellungsprozesses](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deployment-process) in AEM bereitgestellt werden.
* Überprüfen Sie, wie die [Einbettung von Drittanbieter-Packages](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embedding-3rd-party-packages) in Ihr Projekt für AEM as a Cloud Service erfolgt.
* Packages von Drittanbietern müssen die Richtlinien von AEM as a Cloud Service für die [Entwicklung](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines) und [Bündelung](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package) einhalten.
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) und verstehen Sie, wie [INST-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
* Für den `guava.bundle`-Untertyp installieren Sie entweder Guava oder entfernen Sie die Verwendung, wenn Guava in Ihrem benutzerdefinierten Code verwendet wird.
