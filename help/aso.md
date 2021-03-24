---
title: ASO
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 4%

---


# ASO {#aso}

AEM

## Hintergrund {#background}

`ASO` identifiziert allgemeine Informationen zur AEM Instanz. Jede Suche liefert einen Wert einer bestimmten Art von Systeminformationen.

Untertypen werden zur Identifizierung verschiedener Arten von Informationen verwendet:

* `aem.version`: Die AEM Version.
* `aem.product`: Erkennung der Verwendung eines AEM Produkts (Handel, Forms usw.).
* `node.count`: Die ungefähre Knotenanzahl eines bestimmten Typs (Seite, Asset usw.).
* `node.store`: Der Implementierungstyp des Knotenspeichers (SegmentNodeStore, DocumentNodeStore).
* `data.store`: Der Implementierungstyp für den Datenspeicher (FileDataStore, S3DataStore, AzurblaseDataStore).
* `maintenance.task`: Eine Wartungs-Aufgabe.
* `slow.query`: Eine langsame Abfrage.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Implementierungstypen AEM Version, Knotenzählung, Knotenspeicher und Datenspeicher werden zu Informationszwecken bereitgestellt.
* Die benutzerdefinierte Anwendung kann auf Produkten oder Funktionen basieren, die in AEM als Cloud Service nicht verfügbar sind.
* Die Aktualisierung mit nicht unterstützten Funktionen kann zu einer fehlgeschlagenen Aktualisierung und einer nicht funktionierenden Anwendung führen.

## Mögliche Lösungen {#solutions}

* AEM Upgrades mit nicht unterstützten Produkten oder Funktionen werden nicht empfohlen und werden möglicherweise nicht unterstützt.
* Lesen Sie die [Versionshinweise](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de), um mehr über die neuesten Änderungen in AEM als Cloud Service zu erfahren.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
