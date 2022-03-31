---
title: ASO
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: a6bb7df8d0fbad0a233db6972bbb82902aa60c4b
workflow-type: ht
source-wordcount: '369'
ht-degree: 100%

---

# ASO {#aso}

AEM-System-Überblick

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="AEM-System-Überblick"
>abstract="ASO-Code kennzeichnet allgemeine Informationen zur AEM-Instanz. Jedes Ergebnis liefert einen Wert einer bestimmten Art von Systeminformationen, die bei der Migrationsplanung und beim Refactoring hilfreich sein können."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de" text="AEM as a Cloud Service – Versionshinweise"

`ASO` kennzeichnet allgemeine Informationen zur AEM-Instanz. Jedes Ergebnis liefert einen Wert eines bestimmten Typs von Systeminformationen.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `aem.version`: Die AEM-Version.
* `aem.product`: Erkennung der Verwendung eines AEM-Produkts (Commerce, Forms usw.).
* `node.count`: Die ungefähre Knotenanzahl eines bestimmten Typs (Seite, Asset usw.) und die Gesamtsumme der Knoten.
* `node.store`: Der Implementierungstyp des Knotenspeichers (SegmentNodeStore, DocumentNodeStore) und seine Größe.
* `data.store`: Der Speicherimplementierungstyp der Daten (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Eine Wartungsaufgabe.
* `slow.query`: Eine langsame Abfrage.
* `group.membership`: Die Anzahl der Benutzer und Untergruppen (nur direkte/deklarierte Mitglieder) in einer Gruppe.
* `cqtag.count`: Die Anzahl der mit CQ-Tags versehenen Assets.
* `smarttag.count`: Die Anzahl der mit Smart-Tags versehenen Assets.
* `ccom.version`: Die Version des Kernkomponenten-Pakets.
* `instance.type`: Der AEM-Instanztyp (author|publish).
* `unprocessed.asset.count`: Die Anzahl der nicht verarbeiteten Assets.
* `vanity.url.count`: Die Anzahl der Vanity-URLs.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die AEM-Version, die Anzahl der Knoten, die Gruppenmitgliedschaft, der Knotenspeicher, die Implementierungstypen des Datenspeichers, die Anzahl der CQ-Tags, die Anzahl der Smart-Tags, die Kernkomponenten-Version und der AEM-Instanztyp werden zu Informationszwecken bereitgestellt.
* Das benutzerdefinierte Programm kann auf Produkte oder Funktionen zurückgreifen, die nicht in AEM as a Cloud Service verfügbar sind.
* Ein Upgrade mit nicht unterstützten Funktionen kann zu einem fehlgeschlagenen Upgrade und einem nicht funktionsfähigen Programm führen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Implementierungsleitlinien"
>abstract="Informationen, die über den ASO-Code bereitgestellt werden, bieten allgemeine Informationen für Ihre AEM-Umgebung, einschließlich Version, Produkt-Add-ons und Informationen auf Systemebene. Diese sollten auf nicht unterstützte Produkte oder Funktionen in AEM as a Cloud Service überprüft werden. Wenden Sie sich an den Adobe Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* AEM-Upgrades mit nicht unterstützten Produkten oder Funktionen werden nicht empfohlen und möglicherweise nicht unterstützt.
* Lesen Sie die [Versionshinweise](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de), um mehr über die neuesten Änderungen in AEM as a Cloud Service zu erfahren.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
