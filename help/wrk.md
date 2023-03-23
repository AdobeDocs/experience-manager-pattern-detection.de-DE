---
title: WRK
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 100%

---

# WRK {#wrk}

Workflow

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Workflow"
>abstract="WRK-Code kennzeichnet ein Ergebnis im Zusammenhang mit einem Workflow-Modell oder Launcher. Diese werden gemeldet, weil benutzerdefinierte Asset-Workflow-Modelle beim Upgrade auf AEM as a Cloud Service migriert werden müssen. Mit AEM as a Cloud Service wird die Verarbeitung von Assets jetzt von Asset-Microservices durchgeführt."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=de" text="Asset-Microservices"

`WRK` kennzeichnet eine Suche im Zusammenhang mit einem Workflow-Modell oder Starter. Diese werden gemeldet, weil benutzerdefinierte Asset-Workflow-Modelle beim Upgrade auf AEM as a Cloud Service migriert werden müssen.

Um die Art des aktuell erkannten Workflow-Problems zu benennen, wird folgender Untertyp verwendet.

* `custom.asset.workflow`: Erkennung eines benutzerdefinierten Asset-Workflow-Modells oder Starters.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Implementierungsleitlinien"
>abstract="Da Standard-Asset-Workflows automatisch von Asset-Microservices unterstützt werden, ist es Best Practice, alle benutzerdefinierten Asset-Workflow-Modelle oder Launcher zu überprüfen. So wird festgestellt, ob sie bei der Umstellung auf AEM as a Cloud Service benötigt werden. Anpassungen von Asset-Workflows müssen mithilfe des Asset-Workflow-Migrations-Tools migriert werden, damit sie mit AEM as a Cloud Service funktionieren."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html?lang=de" text="Erste Schritte – Asset-Microservices"

* Die Asset-Bearbeitung wurde traditionell mit Asset-Workflows durchgeführt, die auf der AEM-Autoreninstanz ausgeführt wurden. Mit AEM as a Cloud Service wird die Verarbeitung von Assets jetzt von Asset-Microservices durchgeführt. (Weitere Informationen finden Sie in der [Übersicht über Asset-Microservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=de).)
* Standard-Asset-Workflows werden automatisch von „Meine Asset-Microservices“ unterstützt.
* Anpassungen an Asset-Workflows erfordern eine Migration, damit sie mit AEM as a Cloud Service funktionieren.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Tools und Ressourcen"
>abstract="Prüfen und planen Sie die Ausführung des Asset-Workflow-Migrations-Tools, sobald ein benutzerdefiniertes Asset-Workflow-Modell oder ein Launcher bestimmt ist. Wenden Sie sich an den Adobe Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html?lang=de" text="Asset-Workflow-Migrations-Tool"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Wenn ein benutzerdefiniertes Asset-Workflow-Modell oder ein Starter erkannt wird, planen Sie die Ausführung des [Asset-Workflow-Migrations-Tools](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html?lang=de).
* Weitere Informationen finden Sie unter [Erste Schritte mit Asset-Microservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html?lang=de).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
