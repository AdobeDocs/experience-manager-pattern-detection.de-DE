---
title: ASO
description: Hilfeseite zum Mustererkennungs-Code
translation-type: ht
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: ht
source-wordcount: '198'
ht-degree: 100%

---


# ASO {#aso}

AEM-System-Überblick

## Hintergrund {#background}

`ASO` Steht für allgemeine Informationen zur AEM-Instanz. Jedes Ergebnis liefert einen Wert eines bestimmten Typs von Systeminformationen.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `aem.version`: Die AEM-Version.
* `aem.product`: Erkennung der Verwendung eines AEM-Produkts (Commerce, Forms usw.).
* `node.count`: Die ungefähre Knotenanzahl eines bestimmten Typs (Seite, Asset usw.).
* `node.store`: Der Speicherimplementierungstyp des Knotens (SegmentNodeStore, DocumentNodeStore).
* `data.store`: Der Speicherimplementierungstyp der Daten (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Eine Wartungsaufgabe.
* `slow.query`: Eine langsame Abfrage.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Implementierungstypen „AEM-Version“, „Knotenanzahl“, „Knotenspeicher“ und „Datenspeicher“ werden zu Informationszwecken bereitgestellt.
* Das benutzerdefinierte Programm kann auf Produkte oder Funktionen zurückgreifen, die nicht in AEM as a Cloud Service verfügbar sind.
* Ein Upgrade mit nicht unterstützten Funktionen kann zu einem fehlgeschlagenen Upgrade und einem nicht funktionsfähigen Programm führen.

## Mögliche Lösungen {#solutions}

* AEM-Upgrades mit nicht unterstützten Produkten oder Funktionen werden nicht empfohlen und möglicherweise nicht unterstützt.
* Lesen Sie die [Versionshinweise](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de), um mehr über die neuesten Änderungen in AEM as a Cloud Service zu erfahren.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
