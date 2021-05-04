---
title: ASO
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
translation-type: tm+mt
source-git-commit: 449288e567adda9998a89e0ad5198fd5a4e93f35
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 71%

---

# ASO {#aso}

AEM-System-Überblick

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="AEM-System-Überblick"
>abstract="ASO-Code identifiziert allgemeine Informationen zur AEM Instanz. Jede Suche bietet einen Wert eines bestimmten Typs von Systeminformationen, der Ihnen bei der Migrationsplanung und -umgestaltung hilft."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM als Cloud Service - Versionshinweise"

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

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Durchführungsleitlinien"
>abstract="Informationen, die über ASO-Code offen gelegt werden, enthalten allgemeine Informationen zu Ihrer AEM Umgebung, einschließlich Version, Produkt-Add-ons, Informationen auf Systemebene. Diese Informationen sollten in AEM als Cloud Service auf nicht unterstützte Produkte oder Funktionen überprüft werden. Wenden Sie sich an Adobe Support für Hilfe und Klarstellungen."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-Support"

* AEM-Upgrades mit nicht unterstützten Produkten oder Funktionen werden nicht empfohlen und möglicherweise nicht unterstützt.
* Lesen Sie die [Versionshinweise](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de), um mehr über die neuesten Änderungen in AEM as a Cloud Service zu erfahren.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
