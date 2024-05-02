---
title: MI
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 95%

---

# MI {#mi}

Fehlerhafte Konfiguration

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Fehlerhafte Konfiguration"
>abstract="MI identifiziert Konfigurationsprobleme in einer AEM-Instanz"

`MI` (Fehler bei der Konfiguration) Identifiziert Konfigurationsprobleme in AEM Instanz.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden unter anderem folgende Untertypen verwendet:

* `sling.job.max.parallel`: Identifizieren Sie die Sling-Aufträge, bei denen die maximale parallele Konfiguration auf -1 festgelegt ist.
* `missing.maintenance.configuration`: Ermitteln Sie fehlende Konfigurationen für Wartungsaufgaben.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* `sling.job.max.parallel`
   * Der Wert -1 wird durch die Anzahl der verfügbaren Prozessoren ersetzt. Dies kann zu Leistungsproblemen in der AEM-Instanz führen.
* `missing.maintenance.configuration`
   * Fehlende Konfigurationen für Wartungsaufgaben können zu Leistungseinbußen oder zu Beschädigungen der Instanz führen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Implementierungsleitlinien"
>abstract="Wenden Sie sich für Hilfe an die Kundenunterstützung."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* `sling.job.max.parallel`
   * Adobe empfiehlt, den Wert auf 0,5 festzulegen, um die Hälfte der verfügbaren Prozessoren zu nutzen.
* `missing.maintenance.configuration`
   * Revisionsbereinigung: Siehe [Revisionsbereinigung](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup). Den wichtigen Teil zur Konfiguration finden Sie hier: [Revisionsbereinigung – Konfigurieren der Longtail- und vollständigen Komprimierung](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup).
   * Lucene-Binärdateien-Bereinigung: Siehe [Vorgangs-Dashboard – Lucene-Binärdateien-Bereinigung](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/sites/administering/operations/operations-dashboard#lucene-binaries-cleanup).
   * Datenspeicherbereinigung: Siehe [Datenspeicherbereinigung](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/sites/administering/operations/data-store-garbage-collection).
   * Workflow-Bereinigung: Siehe [Regelmäßige Bereinigung von Workflow-Instanzen](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/sites/administering/operations/workflows-administering#regular-purging-of-workflow-instances).
   * AuditLog-Wartungsaufgabe: Siehe [AuditLog-Wartungsaufgabe](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/sites/administering/operations/operations-audit-log).
* Wenden Sie sich an unser [Experience Manager-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
