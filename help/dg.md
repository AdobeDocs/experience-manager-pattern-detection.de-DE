---
title: GD
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 2%

---


# DG {#dg}

Entwicklerhandbuch

## Hintergrund {#background}

`DG` stellt Abweichungen von ausgewählten Entwicklungsrichtlinien für  [AEM 6.5 ](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html) und  [AEM als Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) fest. Die Einhaltung der Best Practices kann die Wartungsfreundlichkeit und Leistung Ihres Systems verbessern. Auch wenn einige dieser Abweichungen in anderen Anwendungsversionen, auch in früheren Kontexten von AEM, möglicherweise nicht problematisch sind, können sie bei Verwendung von AEM als Cloud Service zu Problemen führen.

Untertypen werden zur Identifizierung der verschiedenen Arten erkannter Verstöße verwendet:

* `java.io.inputstream`: Die Verwendung von  `java.io.InputStream` im Anwendungscode.
* `maintenance.task.configuration`: Die Konfiguration einer bestimmten Aktivität zur regelmäßigen Wartung.
* `sling.commons.scheduler`: Die Verwendung der Sling Commons Planung API für eine geplante Aufgabe.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* `java.io.inputstream`
   * Das Streaming binärer Daten mit `java.io.InputStream` kann Speicherressourcen bis zu dem Punkt beanspruchen, an dem die Leistung beeinträchtigt wird. Dies ist insbesondere auf den begrenzten Arbeitsspeicher zurückzuführen, der in Containern zur Verfügung steht, die in AEM als Cloud Service verwendet werden.

* `maintenance.task.configuration`
   * Einige Wartungs-Aufgaben, die zuvor explizit konfiguriert werden mussten, werden jetzt automatisch in AEM als Cloud Service konfiguriert und verwaltet.
   * Die Konfiguration der Maintenance-Aufgabe in AEM als Cloud Service muss in die Quellcodeverwaltung verschoben werden.

* `sling.commons.scheduler`
   * Anwendungen, die von Hintergrundanwendungen mit der Planung [Sling Commons](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) abhängig sind, funktionieren möglicherweise nicht wie erwartet, da die Ausführung in AEM als Cloud Service nicht garantiert werden kann.
   * AEM als Cloud Service-Entwicklungsrichtlinien für [Hintergrund-Aufgaben und Aufträge mit langer Ausführung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#background-tasks-and-long-running-jobs) legen nahe, dass der als geplante Aufgabe ausgeführte Code davon ausgehen muss, dass die Instanz, auf der er ausgeführt wird, jederzeit heruntergefahren werden kann. Daher muss der Code widerstandsfähig und wiederverwendbar sein.

## Mögliche Lösungen {#solutions}

* `java.io.inputstream`
   * Verwenden Sie einen direkten binären Upload-Ansatz, bei dem die Binärdatei direkt zum Datenspeicher hinzugefügt wird.
   * Verwenden Sie für Assets [aem-upload](https://github.com/adobe/aem-upload). Bei anderen Binärtypen kann die benutzerdefinierte Logik für das Hochladen nach demselben Muster modelliert werden.

* `maintenance.task.configuration`
   * Lesen Sie die AEM als Cloud Service [Maintenance-Aufgabe](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html).
   * Stellen Sie sicher, dass [Konfiguration der Maintenance-Aufgabe](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#maintenance-tasks-configuration-in-source-control) in der Quellcodeverwaltung ist.

* `sling.commons.scheduler`
   * Ersetzen Sie die Verwendung von [Sling Commons Planung](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) durch [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), die eine mindestens einmal ausgeführte Garantie haben.
   * Langfristige Aufträge sollten möglichst vermieden werden.

* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
