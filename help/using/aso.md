---
title: ASO
description: Mustererkennungscode Hilfeseite.
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 52%

---

# ASO {#aso}

AEM-System-Überblick

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="AEM-System-Überblick"
>abstract="ASO-Code kennzeichnet allgemeine Informationen zur AEM-Instanz. Jedes Ergebnis liefert einen Wert einer bestimmten Art von Systeminformationen, die bei der Migrationsplanung und beim Refactoring hilfreich sein können."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service – Versionshinweise"

ASO identifiziert allgemeine Informationen zur AEM Instanz. Jedes Ergebnis liefert einen Wert eines bestimmten Typs von Systeminformationen.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `aem.version`: Die AEM-Version.
* `aem.product`: Erkennung der Verwendung eines AEM Produkts (Commerce, Forms usw.).
* `node.count`: Die ungefähre Knotenanzahl eines bestimmten Typs (Seite, Asset usw.) und die Gesamtanzahl der Knoten.
* `node.store`: Der Implementierungstyp des Knotenspeichers (SegmentNodeStore, DocumentNodeStore) und seine Größe.
* `data.store`: Der Speicherimplementierungstyp der Daten (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Eine Wartungsaufgabe.
* `slow.query`: Eine langsame Abfrage.
* `group.membership`: Die Anzahl der Benutzer und Untergruppen ( nur direkte/deklarierte Mitglieder ) in einer Gruppe.
* `cqtag.count`: Die Anzahl der mit CQ-Tags versehenen Assets.
* `smarttag.count`: Die Anzahl der mit Smart-Tags versehenen Assets.
* `ccom.version`: Die Version des Kernkomponenten-Pakets.
* `instance.type`: Der AEM-Instanztyp (author|publish).
* `unprocessed.asset.count`: Die Anzahl der nicht verarbeiteten Assets.
* `vanity.url.count`: Die Anzahl der Vanity-URLs.
* `index.size`: Gesamtgröße des migrierbaren Lucene-Index.
* `workflow.count`: Die Anzahl der laufenden und veralteten Author-Workflows.
* `jvm.arguments`: Die JVM-Argumente, die beim Starten von AEM zur Befehlszeile hinzugefügt wurden.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die AEM-Version, die Anzahl der Knoten, die Gruppenmitgliedschaft, der Knotenspeicher, die Implementierungstypen für Datenspeicher, die CQ-Tag-Anzahl, die Anzahl der Smart-Tags, die Kernkomponenten-Version, AEM Instanztyp und die Anzahl nicht verarbeiteter Assets werden zu Informationszwecken bereitgestellt.
* Die höhere Anzahl von Vanity-URLs (>1000) kann den Dispatcher und die Veröffentlichungs-Server mit teuren Abfragen belasten.
* Das benutzerdefinierte Programm kann auf Produkte oder Funktionen zurückgreifen, die nicht in AEM as a Cloud Service verfügbar sind.
* Ein Upgrade mit nicht unterstützten Funktionen kann zu einem fehlgeschlagenen Upgrade und einem nicht funktionsfähigen Programm führen.
* Eine hohe Anzahl von Author-Workflows im laufenden oder veralteten Zustand könnte die Leistung beeinträchtigen.
* Langsame Abfragen können die Systemleistung beeinträchtigen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Implementierungsleitlinien"
>abstract="Informationen, die über ASO-Code verfügbar gemacht werden, enthalten allgemeine Informationen für Ihre AEM-Umgebung, einschließlich Version, Produkt-Add-ons und Systeminformationen. Überprüfen Sie sie auf nicht unterstützte Produkte oder Funktionen in AEM as a Cloud Service. Wenden Sie sich an den Adobe-Support , um Hilfe oder Erläuterungen zu erhalten."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* AEM Aktualisierungen mit nicht unterstützten Produkten oder Funktionen werden nicht empfohlen und werden möglicherweise nicht unterstützt.
* Die nicht verarbeiteten Assets müssen verarbeitet werden und die `dam:assetState` -Eigenschaft auf `jcr:content` -Knoten des Assets muss auf &quot;verarbeitet&quot;eingestellt sein. Alternativ sollten Sie diese Assets aus dem Migrationssatz entfernen, bevor Sie zu AEMaaCS migrieren.
* Vanity-URLs können durch Apache-Neuschreibungen ersetzt werden.
* Siehe [Dokumentation](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/bestpractices/troubleshooting-slow-queries) für die Fehlerbehebung bei langsamen Abfragen.
* Siehe [Versionshinweise](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current) , wenn Sie mehr über die neuesten Änderungen in AEM as a Cloud Service erfahren möchten.
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
