---
title: ACV
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a5
source-git-commit: 57e33b97aba253bad62cf95dcca9ef6885d263e6
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 7%

---

# ACV {#acv}

Asset Content Validator

## Hintergrund {#background}

>[!INFO]
>id=&quot;aemcloud_bpa_acv_overview&quot;
>title=&quot;Asset Content Validator&quot;
>abstract=&quot;ACV identifiziert die fehlenden obligatorischen Knoten im Asset-Inhalt.&quot;
>additional-url=&quot;https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html&quot; text=&quot;Wesentliche Änderungen - Experience Manager als Cloud Service&quot;
>additional-url=&quot;https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html&quot; text=&quot;Experience Manager als Cloud Service - Versionshinweise&quot;

`ACV`  Der Content Validator von Assets identifiziert die fehlenden erforderlichen Knoten im Asset-Inhalt. Dies könnte zu Fehlern bestimmter Assets-Funktionen auf Experience Manager as a Cloud Service führen.

Untertypen werden verwendet, um die verschiedenen Arten von Informationen zu identifizieren, z. B.:

* `assets.sanity.missing.jcrcontent`: Identifizieren Sie die Ordner mit fehlenden obligatorischen Knoten im Repository. Die Identifizierung fehlender Inhalte im Repository hilft dabei, fehlerhafte Funktionen oder Anwendungsfälle zu vermeiden.

## Mögliche Implikationen und Risiken {#implications-and-risks}

Dies kann zum Fehlschlagen bestimmter Assets-Funktionen führen, die von geerbten Eigenschaften in Experience Manager as a Cloud Service abhängen.

## Mögliche Lösungen {#solutions}

>[!INFO]
>id=&quot;aemcloud_bpa_acv_guide&quot;
>title=&quot;Implementierungsleitfaden&quot;
>abstract=&quot;Adobe empfiehlt, die Inhaltsstruktur zu überprüfen, um fehlerhafte Workflows zu verhindern, die von geerbten Eigenschaften abhängig sind. Wenden Sie sich für Hilfe an die Kundenunterstützung .&quot;
>additional-url=&quot;https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html&quot; text=&quot;Experience Cloud-Support&quot;

* Analysieren Sie einen Ordner, wenn er einen fehlenden untergeordneten Knoten hat. Erstellen Sie die Knoten manuell, wenn die Anzahl der Ordner verwaltbar ist. Verwenden Sie andernfalls ein Skript.
* Wenden Sie sich an unser [Experience Manager-Kundenunterstützungs-Team](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
