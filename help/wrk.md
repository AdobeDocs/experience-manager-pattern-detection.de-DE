---
title: WRK
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 7%

---


# WRK {#wrk}

Workflow

## Hintergrund {#background}

`WRK` identifiziert eine Suche im Zusammenhang mit einem Workflow-Modell oder Starter. Diese werden berichtet, weil benutzerdefinierte Asset-Workflow-Modelle migriert werden müssen, wenn Sie ein Upgrade auf AEM als Cloud Service durchführen.

Ein Untertyp wird verwendet, um den Typ des Workflow-Problems zu identifizieren, das derzeit erkannt wird.

* `custom.asset.workflow`: Erkennung eines benutzerdefinierten Asset-Workflow-Modells oder Starters.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Asset-Verarbeitung wurde bisher durchgeführt, während Assets Workflows auf der AEM Author-Instanz ausgeführt wurden. Mit AEM als Cloud Service wird die Verarbeitung von Assets jetzt von Asset-Mikrodiensten durchgeführt. (Weitere Informationen finden Sie unter [Übersicht über Asset-Mikrodienste](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=de).
* Standard-Asset-Workflows werden automatisch von meinen Asset-Mikrodiensten unterstützt.
* Anpassungen an Assets Workflows Migration erforderlich, um mit AEM als Cloud Service arbeiten zu können.

## Mögliche Lösungen {#solutions}

* Wenn ein benutzerdefiniertes Asset-Workflow-Modell oder Starter identifiziert wird, führen Sie das [Asset Workflow-Migrationswerkzeug](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html) aus.
* Weitere Informationen finden Sie unter [Erste Schritte mit Asset Microservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html?lang=de).
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
