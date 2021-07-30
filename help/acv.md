---
title: ACV
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a5
source-git-commit: d61fbb28fdf91fd9b356654d5cd2d50b156398c4
workflow-type: ht
source-wordcount: '219'
ht-degree: 100%

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

`ACV` Assets Content Validator identifiziert die fehlenden obligatorischen Knoten in Asset-Inhalten. Dies kann zu Fehlern bei bestimmten Assets-Funktionen in Experience Manager as a Cloud Service führen.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden unter anderem folgende Untertypen verwendet:

* `assets.sanity.missing.jcrcontent`: Identifizieren Sie die Ordner mit fehlenden obligatorischen Knoten im Repository. Die Identifizierung fehlender Inhalte im Repository hilft dabei, fehlerhafte Funktionen oder Anwendungsfälle zu vermeiden.

## Mögliche Implikationen und Risiken {#implications-and-risks}

Dies kann zu Fehlern bei bestimmten Assets-Funktionen in Experience Manager as a Cloud Service führen, die von übernommenen Eigenschaften abhängig sind.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Implementierungsleitlinien"
>abstract="Adobe empfiehlt, die Inhaltsstruktur zu überprüfen, um fehlerhafte Workflows zu verhindern, die von übernommenen Eigenschaften abhängig sind. Wenden Sie sich für Hilfe an die Kundenunterstützung.&quot;
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Analysieren Sie einen Ordner, wenn ein untergeordneter Knoten fehlt. Erstellen Sie die Knoten manuell, wenn die Anzahl der Ordner überschaubar ist. Verwenden Sie andernfalls ein Skript.
* Wenden Sie sich an unser [Experience Manager-Kundenunterstützungs-Team](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder Probleme zu besprechen.
