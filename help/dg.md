---
title: DG
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
source-git-commit: 9bc04f53b6c6c91a528f3c77ea1c702127a6b7df
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# DG {#dg}

Entwicklungsrichtlinien

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="Entwicklungsrichtlinien"
>abstract="DG-Code kennzeichnet Abweichungen von ausgewählten Entwicklungsrichtlinien für AEM 6.5 und AEM as a Cloud Service. Die Einhaltung der Best Practices kann die Wartungsfreundlichkeit und Leistung Ihres Systems verbessern. Obwohl einige dieser Abweichungen im Kontext anderer Programme, einschließlich früherer Versionen von AEM, möglicherweise kein Problem darstellen, können sie bei der Verwendung von AEM as a Cloud Service Probleme verursachen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html?lang=de" text="AEM-Entwicklung – Richtlinien und Best Practices"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=de" text="Entwicklungsrichtlinien für AEM as a Cloud Service"


`DG` kennzeichnet Abweichungen von ausgewählten Entwicklungsrichtlinien für [AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html?lang=de) und [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=de). Die Einhaltung der Best Practices kann die Wartungsfreundlichkeit und Leistung Ihres Systems verbessern. Obwohl einige dieser Abweichungen im Kontext anderer Programme, einschließlich früherer Versionen von AEM, möglicherweise kein Problem darstellen, können sie bei der Verwendung von AEM as a Cloud Service Probleme verursachen.

Um die verschiedenen Arten von erkannten Verstößen zu unterscheiden, werden folgende Untertypen verwendet:

* `java.io.inputstream`: Die Verwendung von `java.io.InputStream` im Programm-Code.
* `maintenance.task.configuration`: Die Konfiguration einer bestimmten regelmäßigen Wartungsaktivität.
* `sling.commons.scheduler`: Die Verwendung der Sling Commons Scheduler-API für eine geplante Aufgabe.
* `unsupported.asset.api`: Die Verwendung nicht unterstützter Asset Manager-APIs im Programm-Code.
* `javax.jcr.observation.EventListener`: Die Verwendung des Ereignis-Listeners im Programm-Code.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* `java.io.inputstream`
   * Das Streaming binärer Daten mit `java.io.InputStream` kann Speicherressourcen bis zu dem Punkt beanspruchen, an dem die Leistung beeinträchtigt wird. Dies ist insbesondere auf den begrenzten Speicherplatz zurückzuführen, der in Containern zur Verfügung steht, die in AEM as a Cloud Service verwendet werden.

* `maintenance.task.configuration`
   * Einige Wartungsaufgaben, die zuvor explizit konfiguriert werden mussten, werden jetzt automatisch in AEM as a Cloud Service konfiguriert und verwaltet.
   * Die Konfiguration der Wartungsaufgaben in AEM as a Cloud Service muss in die Quell-Code-Verwaltung verschoben werden.

* `sling.commons.scheduler`
   * Programme, die von Hintergrundaufgaben abhängig sind, die [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) verwenden, funktionieren möglicherweise nicht wie erwartet, da die Ausführung in AEM as a Cloud Service nicht garantiert werden kann.
   * Die Entwicklungsrichtlinien von AEM as a Cloud Service für [Hintergrundaufgaben und lang laufende Aufträge](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=de#background-tasks-and-long-running-jobs) legen nahe, dass der als geplante Aufgabe ausgeführte Code davon ausgehen muss, dass die Instanz, auf der er ausgeführt wird, jederzeit heruntergefahren werden kann. Daher muss der Code stabil und vor allem wiederaufnehmbar sein.

* `unsupported.asset.api`
   * Die folgenden APIs von AssetManager werden auf AEM as a Cloud Service als nicht unterstützt markiert.
      * createAssetForBinary
      * getAssetForBinary
      * removeAssetForBinary
      * createAsset

* `javax.jcr.observation.EventListener`
   * Vom Ereignis-Listener abhängige Programme funktionieren möglicherweise nicht erwartungsgemäß, da die Ausführung nicht garantiert werden kann.


## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="Implementierungsleitlinien"
>abstract="Gemäß den AEM-Entwicklungsrichtlinien und Best Practices sollten Kunden ihre Implementierungen auf die Verwendung von Sling Commons Scheduler überprüfen und in Sling Jobs umstrukturieren, ihre Systemwartungsaufgaben umstrukturieren, das Streaming von Binärdaten überprüfen und ihren Code überarbeiten, sodass er mit AEM as a Cloud Service kompatibel ist."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Sling Jobs"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html?lang=de" text="Wartungsaufgaben in AEM as a Cloud Service"

* `java.io.inputstream`
   * Verwenden Sie einen direkt-binären Ansatz zum Hochladen, bei dem die Binärdatei direkt zum Datenspeicher hinzugefügt wird.
   * Für Anwendungsfälle von Assets verwenden Sie [aem-upload](https://github.com/adobe/aem-upload). Für andere Arten von Binärdateien kann die benutzerdefinierte Upload-Logik nach demselben Muster modelliert werden.

* `maintenance.task.configuration`
   * Lesen Sie die Dokumention von AEM as a Cloud Service zu [Wartungsaufgaben](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html?lang=de).
   * Stellen Sie sicher, dass die [Konfiguration der Wartungsaufgaben](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=de#maintenance-tasks-configuration-in-source-control) in der Quell-Code-Verwaltung ist.

* `sling.commons.scheduler`
   * Ersetzen Sie die Verwendung von [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) durch [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), die mindestens eine einmalige Ausführung garantieren.
   * Lang laufende Aufträge sollten möglichst vermieden werden.

* `unsupported.asset.api`
   * Verwenden Sie bitte [aem-upload](https://github.com/adobe/aem-upload) anstelle der nicht unterstützten APIs von Asset Manager.

* `javax.jcr.observation.EventListener`
   * Anstatt den Ereignis-Listener zu verwenden, wird empfohlen, den Mechanismus zum Umgang mit Ereignissen in [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing) zu refaktorieren, um die Verarbeitung zu garantieren.
* Wenden Sie sich an unser [AEM-Support-Team](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
