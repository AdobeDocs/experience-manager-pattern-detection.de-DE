---
title: MI
description: Hilfeseite zum Mustererkennungs-Code
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: efb06dc7e00f91d4c080553df3153deb90b093f2
workflow-type: ht
source-wordcount: '210'
ht-degree: 100%

---

# MI {#mi}

Fehlerhafte Konfiguration

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Fehlerhafte Konfiguration"
>abstract="MI identifiziert Konfigurationsprobleme in einer AEM-Instanz"

`MI` Misconfiguration Issue hat Konfigurationsprobleme in AEM-Instanz erkannt.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden unter anderem folgende Untertypen verwendet:

* `sling.job.max.parallel`: Identifizieren Sie die Sling-Aufträge, bei denen die maximale parallele Konfiguration auf -1 festgelegt ist.
* `missing.maintenance.configuration`: Ermitteln Sie fehlende Konfigurationen für Wartungsaufgaben.

## Mögliche Implikationen und Risiken {#implications-and-risks}

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
   * Es wird empfohlen, den Wert auf 0,5 festzulegen, um die Hälfte der verfügbaren Prozessoren nutzen zu können.
* `missing.maintenance.configuration`
   * Revisionsbereinigung: Siehe [Revisionsbereinigung](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=de). Den wichtigen Teil zur Konfiguration finden Sie hier: [Revisionsbereinigung – Konfigurieren der Tail- und vollständigen Komprimierung](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=de#how-to-configure-full-and-tail-compaction).
   * Lucene-Binärdateien-Bereinigung: Siehe [Vorgangs-Dashboard – Lucene-Binärdateien-Bereinigung](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-dashboard.html?lang=de#lucene-binaries-cleanup).
   * Datenspeicherbereinigung: Siehe [Datenspeicherbereinigung](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/data-store-garbage-collection.html?lang=de).
   * Workflow-Bereinigung: Siehe [Regelmäßige Bereinigung von Workflow-Instanzen](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/workflows-administering.html?lang=de#regular-purging-of-workflow-instances).
   * AuditLog-Wartungsaufgabe: Siehe [AuditLog-Wartungsaufgabe](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-audit-log.html?lang=de).
* Wenden Sie sich an unser [Experience Manager-Support-Team](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder Probleme zu besprechen.
