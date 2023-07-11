---
title: MI
description: Hilfeseite zum Mustererkennungs-Code
source-git-commit: aa05ebcb54c6945a903c76add4f31e3279cd05b5
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 36%

---

# MI {#mi}

Fehlerhafte Konfiguration

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Fehlerhafte Konfiguration"
>abstract="MI identifiziert Konfigurationsprobleme in einer AEM-Instanz"

`MI`  Fehlkonfigurationsproblem identifiziert Konfigurationsprobleme in AEM Instanz.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden unter anderem folgende Untertypen verwendet:

* `sling.job.max.parallel`: Identifizieren Sie die Sling-Aufträge, bei denen die maximale parallele Konfiguration auf -1 festgelegt ist.
* `missing.maintenance.configuration`: Ermitteln Sie fehlende Konfigurationen von Wartungsaufgaben.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* `sling.job.max.parallel`
   * Der Wert -1 wird durch die Anzahl der verfügbaren Prozessoren ersetzt. Dies kann Leistungsprobleme in AEM Instanz verursachen.
* `missing.maintenance.configuration`
   * Fehlende Konfigurationen von Wartungsaufgaben können zu Leistungseinbußen oder zu Beschädigungen der Instanz führen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Implementierungsleitlinien"
>abstract="Wenden Sie sich für Hilfe an die Kundenunterstützung."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* `sling.job.max.parallel`
   * Es wird empfohlen, den Wert auf 0,5 festzulegen, um die Hälfte der verfügbaren Prozessoren zu nutzen.
* `missing.maintenance.configuration`
   * Revisionsbereinigung: Siehe [Revisionsbereinigung](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=de). Der wichtige Teil zur Konfiguration ist hier: [Revisionsbereinigung - Konfigurieren der Zeitleiste und vollständigen Komprimierung](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html#how-to-configure-full-and-tail-compaction).
   * Lucene-Binärdateien-Bereinigung: Siehe [Vorgangs-Dashboard - Bereinigung der Lucene-Binärdateien](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-dashboard.html#lucene-binaries-cleanup).
   * Datenspeicherbereinigung: Siehe [Datenspeicherbereinigung](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/data-store-garbage-collection.html?lang=de).
   * Workflow-Bereinigung: Siehe [Regelmäßiges Bereinigen von Workflow-Instanzen](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/workflows-administering.html?lang=de#regular-purging-of-workflow-instances).
   * AuditLog-Wartungsaufgabe: Siehe [Auditprotokoll-Wartung](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-audit-log.html).
* Wenden Sie sich an unser [Experience Manager-Support-Team](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder Probleme zu besprechen.