---
title: WRK
description: Mustererkennungscode Hilfeseite.
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 62%

---

# WRK {#wrk}

Workflow

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Workflow"
>abstract="WRK-Code kennzeichnet ein Ergebnis im Zusammenhang mit einem Workflow-Modell oder Launcher. Diese werden gemeldet, weil benutzerdefinierte Asset-Workflow-Modelle beim Upgrade auf AEM as a Cloud Service migriert werden müssen. Mit AEM as a Cloud Service wird die Verarbeitung von Assets jetzt von Asset-Microservices durchgeführt."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview" text="Asset-Microservices"

WRK identifiziert ein Ergebnis im Zusammenhang mit einem Workflow-Modell oder Starter. Diese werden gemeldet, weil benutzerdefinierte Asset-Workflow-Modelle beim Upgrade auf AEM as a Cloud Service migriert werden müssen.

Um die Art des aktuell erkannten Workflow-Problems zu benennen, wird folgender Untertyp verwendet.

* `custom.asset.workflow`: Erkennung eines benutzerdefinierten Asset-Workflow-Modells oder Starters.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Implementierungsleitlinien"
>abstract="Standard-Asset-Workflows werden von meinen Asset-Microservices automatisch unterstützt. Daher empfiehlt es sich, alle benutzerdefinierten Asset-Workflow-Modelle oder den Starter zu überprüfen, um festzustellen, ob sie nach der Umstellung auf AEM as a Cloud Service erforderlich sind. Anpassungen an Asset-Workflows erfordern eine Migration, damit sie mithilfe des Asset Workflow Migration Tool mit AEM as a Cloud Service verwendet werden können"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use" text="Erste Schritte – Asset-Microservices"

* Die Asset-Bearbeitung wurde traditionell mit Asset-Workflows durchgeführt, die auf der AEM-Autoreninstanz ausgeführt wurden. Mit AEM as a Cloud Service wird die Verarbeitung von Assets jetzt von Asset-Microservices durchgeführt. Siehe [Übersicht über Asset-Microservices](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview) für weitere Informationen.
* Standard-Asset-Workflows werden automatisch von „Meine Asset-Microservices“ unterstützt.
* Anpassungen an Asset-Workflows erfordern eine Migration, damit sie mit AEM as a Cloud Service funktionieren.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Tools und Ressourcen"
>abstract="Prüfen und planen Sie die Ausführung des Asset-Workflow-Migrations-Tools, sobald ein benutzerdefiniertes Asset-Workflow-Modell oder ein Launcher bestimmt ist. Wenden Sie sich an den Adobe-Support , um Hilfe oder Erläuterungen zu erhalten."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool" text="Asset-Workflow-Migrations-Tool"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Wenn ein benutzerdefiniertes Asset-Workflow-Modell oder ein Starter erkannt wird, planen Sie die Ausführung des [Asset-Workflow-Migrations-Tools](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool).
* Weitere Informationen finden Sie unter [Erste Schritte mit Asset-Microservices](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use).
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
