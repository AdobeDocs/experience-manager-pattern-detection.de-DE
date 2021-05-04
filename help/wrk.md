---
title: WRK
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 70%

---

# WRK {#wrk}

Workflow

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Arbeitsablauf"
>abstract="WRK-Code identifiziert eine Suche im Zusammenhang mit einem Workflow-Modell oder Starter. Diese werden gemeldet, weil benutzerdefinierte Asset-Workflow-Modelle beim Upgrade auf AEM as a Cloud Service migriert werden müssen. Mit AEM as a Cloud Service wird die Verarbeitung von Assets jetzt von Asset-Microservices durchgeführt."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html" text="Asset-Microservices"

`WRK` steht für eine Suche im Zusammenhang mit einem Workflow-Modell oder Starter. Diese werden gemeldet, weil benutzerdefinierte Asset-Workflow-Modelle beim Upgrade auf AEM as a Cloud Service migriert werden müssen.

Um die Art des aktuell erkannten Workflow-Problems zu benennen, wird folgender Untertyp verwendet.

* `custom.asset.workflow`: Erkennung eines benutzerdefinierten Asset-Workflow-Modells oder Starters.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Durchführungsleitlinien"
>abstract="Da Standard-Asset-Workflows automatisch von meinen Asset-Mikrodiensten unterstützt werden, besteht die Best Practice darin, alle benutzerdefinierten Asset-Workflow-Modelle oder Starter zu überprüfen, um zu sehen, ob sie benötigt werden, sobald die Transition erfolgt, als Cloud Service AEM. Anpassungen an Assets Workflows Migration erforderlich, um mit AEM als Cloud Service mit dem Asset Workflow Migration Tool arbeiten zu können"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html" text="Erste Schritte - Asset Microservices"

* Die Asset-Bearbeitung wurde traditionell mit Asset-Workflows durchgeführt, die auf der AEM-Autoreninstanz ausgeführt wurden. Mit AEM as a Cloud Service wird die Verarbeitung von Assets jetzt von Asset-Microservices durchgeführt. (Weitere Informationen finden Sie in der [Übersicht über Asset-Microservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=de).)
* Standard-Asset-Workflows werden automatisch von „Meine Asset-Microservices“ unterstützt.
* Anpassungen an Asset-Workflows erfordern eine Migration, damit sie mit AEM as a Cloud Service funktionieren.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Tools und Ressourcen"
>abstract="Überprüfen und planen Sie, das Asset Workflow-Migrationswerkzeug auszuführen, sobald ein benutzerdefiniertes Asset-Workflow-Modell oder Starter identifiziert wurde. Support zur Adobe für Hilfe und Klarstellungen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html" text="Asset-Workflow-Migrations-Tool"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-Support"

* Wenn ein benutzerdefiniertes Asset-Workflow-Modell oder ein Starter erkannt wird, planen Sie die Ausführung des [Asset-Workflow-Migrations-Tools](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html?lang=de).
* Weitere Informationen finden Sie unter [Erste Schritte mit Asset-Microservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html?lang=de).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
