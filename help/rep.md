---
title: REP
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: 7d05067fc624571e6fe520e2a1addd5dff8acbd8
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 2%

---


# [!DNL REP] {#rep}

Replikationsagent

## Hintergrund {#background}

`REP` Identifiziert aktivierte Replizierungsagenten. Diese werden aufgrund des Potenzials von Problemen gemeldet, die bei der Aktualisierung auf AEM als Cloud Service behoben werden sollten.

AEM als Cloud Service verwendet [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html), um Inhalte vom Autor für Veröffentlichungsinhalte zu verteilen. Dies geschieht außerhalb der AEM Laufzeit mithilfe des Pipeline-Dienstes der Adobe I/O. Dies wird automatisch in der bereitgestellten AEM als Cloud Service-Umgebung konfiguriert.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Konfiguration der Replikation hat sich mit AEM als Cloud Service geändert. Alle aktuellen Replizierungsagenten sollten überprüft werden, um festzustellen, welche durch die Standardfunktion ersetzt werden, welche Konfigurationen in den Code verschoben werden müssen und welche nicht unterstützt werden.
* Jede Verwendung von Replizierungsagenten im benutzerdefinierten Code oder Workflows sollte während der Aktualisierung auf AEM als Cloud Service überprüft werden.
* Die umgekehrte Replizierung wird in AEM als Cloud Service zunächst nicht unterstützt.
* Es ist nicht erforderlich, einen separaten Dispatcher-Flush-Agent zu konfigurieren. Dies wird im AEM automatisch als Cloud Service-Umgebung konfiguriert.

## Mögliche Lösungen {#solutions}

* Siehe AEM als Cloud Service [Entwicklungsrichtlinien](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents) und Versionshinweise für [Replizierungsagenten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents).
* Überprüfen, refaktorieren und optimieren Sie Funktionen, die direkt von Replizierungsagenten abhängen, um geschäftliche Aufgaben durchzuführen.
* Sehen Sie, wie sich die Bereitstellung in AEM als Cloud Service auf [Replikation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication) auswirkt.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
