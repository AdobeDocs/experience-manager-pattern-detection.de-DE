---
title: ACV
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 72%

---

# ACV {#acv}

Assets Content Validator

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets Content Validator"
>abstract="ACV identifiziert die fehlenden obligatorischen Knoten in Assets-Inhalten."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/overview" text="Wesentliche Änderungen – Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Experience Manager as a Cloud Service – Versionshinweise"

`ACV` (Asset-Inhaltsvalidator) Identifiziert die fehlenden obligatorischen Knoten und Verstöße im Asset-Inhalt. Solche Dinge könnten dazu führen, dass bestimmte Assets-Funktionen auf dem Experience Manager as a Cloud Service fehlschlagen.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden unter anderem folgende Untertypen verwendet:

* `missing.jcrcontent`: Identifizieren Sie die Ordner mit fehlenden obligatorischen Knoten im Repository. Die Identifizierung fehlender Inhalte im Repository hilft dabei, fehlerhafte Funktionen oder Anwendungsfälle zu vermeiden.
* `missing.original.rendition`: Identifizieren Sie die Assets mit fehlender obligatorischer Original-Ausgabedarstellung im Repository. Die Vorschau von PDF-Seiten erfordert keine Erstellung von Unter-Assets in AEMaa. Daher wird bei PDF-Assets die Berichterstellung für Teil-Assets, denen die ursprüngliche Ausgabedarstellung fehlt, unterdrückt.
* `metadata.descendants.violation`: Identifizieren Sie die Assets mit mehr als 100 untergeordneten Elementen unter dem Metadatenknoten des Assets im Repository.
* `conflict.node`: Identifizieren Sie das Vorhandensein von Konfliktknoten im Repository unter dem Pfad /content/dam/.
* `psb.file.large`: Identifizieren Sie große PSB-Dateien (`dc:format : application/vnd.3gpp.pic-bw-small`) größer als 2 GB sein.
* `invalid.asset.name`: Identifizieren von Assets mit ungültigen Zeichen[`* / : [ \ ] | # % { } ? &`] im Namen.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* Möglicherweise führt dies zu einem Fehler bei bestimmten Assets-Funktionen, die von geerbten Eigenschaften in Experience Manager as a Cloud Service abhängen.
* AEM Assets benötigt die vorhandene Original-Ausgabedarstellung. Die Asset-Verarbeitung in Cloud Service bleibt in einer Schleife hängen, wenn die Original-Ausgabedarstellung fehlt. Die Generierung von Teil-Assets wird in AEMaaCS nicht unterstützt.
* Eine hohe Anzahl untergeordneter Elemente unter einem Metadatenknoten kann das Herunterladen von Ordnern mit verletzenden Assets verlangsamen.
* Das Vorhandensein von Konfliktknoten kann as a Cloud Service zu einem Erfassungsfehler AEM.
* Experience Manager kann PSB-Dateien mit hohen Auflösungen möglicherweise nicht verarbeiten. Kundinnen und Kunden, die ImageMagick für die Verarbeitung großer Dateien verwenden, müssen möglicherweise mit Leistungseinbußen rechnen, wenn der Experience Manager-Server nicht ordnungsgemäß getestet wird.
* Ungültige Zeichen im Namen des Assets können zu Fehlern bei der Migration zu AEM as a Cloud Service führen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Implementierungsleitlinien"
>abstract="Adobe empfiehlt, die Inhaltsstruktur zu überprüfen, um fehlerhafte Workflows zu verhindern, die von übernommenen Eigenschaften abhängig sind. Wenden Sie sich für Hilfe an die Kundenunterstützung."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Analysieren Sie einen Ordner, wenn ein untergeordneter Knoten fehlt. Erstellen Sie die Knoten manuell, wenn die Anzahl der Ordner überschaubar ist. Verwenden Sie andernfalls ein Skript.
* Wenn bei Assets die Original-Ausgabedarstellung fehlt, laden Sie das Asset vor der Migration entweder erneut hoch oder löschen Sie es.
* Für fehlende Original-Ausgabeformate von Teil-Assets ist keine Aktion erforderlich.
* Wenn es Konfliktknoten gibt, sollten diese vor der Migration zu AEM as a Cloud Service aufgelöst oder gelöscht werden.
* Wenden Sie sich an den Adobe-Support, wenn Sie viele große PSD- oder PSB-Dateien verarbeiten möchten. Experience Manager verarbeitet möglicherweise keine PSB-Dateien mit hoher Auflösung, die mehr als 30.000 x 23.000 Pixel umfassen. [Siehe Dokumentation](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/assets/extending/best-practices-for-imagemagick).
* Wenden Sie sich an unser [Experience Manager-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
