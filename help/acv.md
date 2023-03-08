---
title: ACV
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: bbeb7193e198a32a9bc966e1821b1058dbbc8c02
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 81%

---

# ACV {#acv}

Assets Content Validator

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets Content Validator"
>abstract="ACV identifiziert die fehlenden obligatorischen Knoten in Assets-Inhalten."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html?lang=de" text="Wesentliche Änderungen – Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de" text="Experience Manager as a Cloud Service – Versionshinweise"

`ACV` Assets Content Validator identifiziert die fehlenden obligatorischen Knoten und Verstöße in Asset-Inhalten. Dies kann zu Fehlern bei bestimmten Assets-Funktionen in Experience Manager as a Cloud Service führen.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden unter anderem folgende Untertypen verwendet:

* `missing.jcrcontent`: Identifizieren Sie die Ordner mit fehlenden obligatorischen Knoten im Repository. Die Identifizierung fehlender Inhalte im Repository hilft dabei, fehlerhafte Funktionen oder Anwendungsfälle zu vermeiden.
* `missing.original.rendition`: Identifizieren Sie die Assets mit fehlender obligatorischer Original-Ausgabedarstellung im Repository. Beachten Sie, dass für die Vorschau von PDF-Seiten keine Generierung von Teil-Assets in AEMaaCS erforderlich ist. Daher wird bei PDF-Assets die Berichterstellung für Teil-Assets ohne ursprüngliche Ausgabedarstellung unterdrückt.
* `metadata.descendants.violation`: Identifizieren Sie die Assets mit mehr als 100 untergeordneten Elementen unter dem Metadatenknoten des Assets im Repository.
* `conflict.node`: Identifizieren Sie das Vorhandensein von Konfliktknoten im Repository unter dem Pfad /content/dam/.
* `psb.file.large`: Identifizieren Sie große PSB-Dateien (dc:format : application/vnd.3gpp.pic-bw-small) mit einer Größe größer als 2 Gigabyte.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Dies kann zu Fehlern bei bestimmten Assets-Funktionen in Experience Manager as a Cloud Service führen, die von übernommenen Eigenschaften abhängig sind.
* AEM Assets benötigt die vorhandene Original-Ausgabedarstellung. Die Asset-Verarbeitung in Cloud Service bleibt in einer Schleife hängen, wenn die Original-Ausgabedarstellung fehlt. Die Generierung von Teil-Assets wird in AEMaaCS nicht unterstützt.
* Eine hohe Anzahl untergeordneter Elemente unter dem Metadatenknoten kann das Laden von Ordnern verlangsamen, die aus Assets bestehen, die dies verletzen.
* Das Vorhandensein von Konfliktknoten kann zu einem Aufnahmefehler bei AEM as a Cloud Service führen.
* Experience Manager verarbeitet möglicherweise keine PSB-Dateien mit hoher Auflösung. Kunden, die ImageMagick zur Verarbeitung großer Dateien verwenden, können die Leistung beeinträchtigen, wenn kein ordnungsgemäßes Benchmarking des Experience Manager-Servers durchgeführt wird.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Implementierungsleitlinien"
>abstract="Adobe empfiehlt, die Inhaltsstruktur zu überprüfen, um fehlerhafte Workflows zu verhindern, die von übernommenen Eigenschaften abhängig sind. Wenden Sie sich für Hilfe an die Kundenunterstützung."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Analysieren Sie einen Ordner, wenn ein untergeordneter Knoten fehlt. Erstellen Sie die Knoten manuell, wenn die Anzahl der Ordner überschaubar ist. Verwenden Sie andernfalls ein Skript.
* Wenn bei Assets die Original-Ausgabedarstellung fehlt, laden Sie das Asset vor der Migration entweder erneut hoch oder löschen Sie es.
* Keine Aktion erforderlich bei fehlender Original-Ausgabedarstellung von Teil-Assets.
* Im Falle von Konfliktknoten sollten diese entweder aufgelöst oder gelöscht werden, bevor Sie zu AEM as a Cloud Service migrieren.
* Wenden Sie sich an den Adobe-Support, wenn Sie viele große PSD- oder PSB-Dateien verarbeiten möchten. Experience Manager verarbeiten möglicherweise keine sehr hochauflösenden PSB-Dateien mit mehr als 30000 x 23000 Pixel. Siehe [Dokumentation](https://experienceleague.adobe.com/docs/experience-manager-64/assets/extending/best-practices-for-imagemagick.html).
* Wenden Sie sich an unser [Experience Manager-Support-Team](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder Probleme zu besprechen.
