---
title: WRK
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 64%

---

# WRK {#wrk}

Workflow

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Workflow"
>abstract="WRK-Code kennzeichnet ein Ergebnis im Zusammenhang mit einem Workflow-Modell oder Launcher. Diese Identifizierungen werden gemeldet, da benutzerdefinierte Asset-Workflow-Modelle beim Aktualisieren auf AEM as a Cloud Service migriert werden müssen. Mit AEM as a Cloud Service führen Asset-Microservices die Asset-Verarbeitung durch."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview" text="Asset-Microservices"

`WRK` identifiziert ein Ergebnis, das sich auf ein Workflow-Modell oder einen Launcher bezieht. Diese Identifizierungen werden gemeldet, da benutzerdefinierte Asset-Workflow-Modelle beim Aktualisieren auf AEM as a Cloud Service migriert werden müssen.

Um die Art des aktuell erkannten Workflow-Problems zu benennen, wird folgender Untertyp verwendet.

* `custom.asset.workflow`: Erkennung eines benutzerdefinierten Asset-Workflow-Modells oder Starters.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Implementierungsleitlinien"
>abstract="Standard-Asset-Workflows werden automatisch von „Meine Asset-Microservices“ unterstützt. Daher empfiehlt es sich, alle benutzerdefinierten Asset-Workflow-Modelle oder den Starter zu überprüfen. Bei der Überprüfung können Sie sehen, ob sie nach der Umstellung auf AEM as a Cloud Service erforderlich sind. Anpassungen an Asset-Workflows erfordern eine Migration, damit sie mithilfe des Asset Workflow Migration Tool mit AEM as a Cloud Service verwendet werden können"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use" text="Erste Schritte – Asset-Microservices"

* Die Asset-Bearbeitung wurde traditionell mit Asset-Workflows durchgeführt, die auf der AEM-Autoreninstanz ausgeführt wurden. Mit AEM as a Cloud Service führen Asset-Microservices die Asset-Verarbeitung durch. Weitere Informationen finden Sie in der [Übersicht über Asset-Microservices](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview).
* Standard-Asset-Workflows werden automatisch von „Meine Asset-Microservices“ unterstützt.
* Anpassungen an Asset-Workflows erfordern eine Migration, damit sie mit AEM as a Cloud Service funktionieren.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Tools und Ressourcen"
>abstract="Prüfen und planen Sie, das Asset Workflow Migration Tool auszuführen, nachdem benutzerdefinierte Asset-Workflow-Modelle oder Launcher identifiziert wurden. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool" text="Asset-Workflow-Migrations-Tool"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Wenn ein benutzerdefiniertes Asset-Workflow-Modell oder ein Starter erkannt wird, planen Sie die Ausführung des [Asset-Workflow-Migrations-Tools](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool).
* Weitere Informationen finden Sie unter [Erste Schritte mit Asset-Microservices](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
