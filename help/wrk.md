---
title: WRK
description: Hilfeseite zum Mustererkennungs-Code
translation-type: ht
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: ht
source-wordcount: '197'
ht-degree: 100%

---


# WRK {#wrk}

Workflow

## Hintergrund {#background}

`WRK` steht für eine Suche im Zusammenhang mit einem Workflow-Modell oder Starter. Diese werden gemeldet, weil benutzerdefinierte Asset-Workflow-Modelle beim Upgrade auf AEM as a Cloud Service migriert werden müssen.

Um die Art des aktuell erkannten Workflow-Problems zu benennen, wird folgender Untertyp verwendet.

* `custom.asset.workflow`: Erkennung eines benutzerdefinierten Asset-Workflow-Modells oder Starters.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Asset-Bearbeitung wurde traditionell mit Asset-Workflows durchgeführt, die auf der AEM-Autoreninstanz ausgeführt wurden. Mit AEM as a Cloud Service wird die Verarbeitung von Assets jetzt von Asset-Microservices durchgeführt. (Weitere Informationen finden Sie in der [Übersicht über Asset-Microservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=de).)
* Standard-Asset-Workflows werden automatisch von „Meine Asset-Microservices“ unterstützt.
* Anpassungen an Asset-Workflows erfordern eine Migration, damit sie mit AEM as a Cloud Service funktionieren.

## Mögliche Lösungen {#solutions}

* Wenn ein benutzerdefiniertes Asset-Workflow-Modell oder ein Starter erkannt wird, planen Sie die Ausführung des [Asset-Workflow-Migrations-Tools](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html?lang=de).
* Weitere Informationen finden Sie unter [Erste Schritte mit Asset-Microservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html?lang=de).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
