---
title: CTEM
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 4%

---


# CTEM {#ctem}

Benutzerdefinierte Vorlage

## Hintergrund {#background}

`CTEM` identifiziert benutzerdefinierte Vorlagen, die auf AEM installiert wurden. Diese Informationen werden für die Zwecke der Bewertung bewährter Verfahren bereitgestellt.

Vorlagen werden durch den primären Typwert &quot;cq:Template&quot;identifiziert. Mit diesem Code wird ein Untertyp verwendet, um die Kategorie der Vorlage zu identifizieren:

* `custom.editable.template`: Der Pfad der Vorlage wird nicht mit &quot;/apps&quot;Beginn.
* `custom.static.template`: Der Pfad der Vorlagen-Beginn mit &quot;/apps&quot;.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Best Practice ist, alle statischen Vorlagen in bearbeitbare Vorlagen zu verschieben.

## Mögliche Lösungen {#solutions}

* Verwenden Sie die [AEM Moderationstools](https://opensource.adobe.com/aem-modernize-tools/), um statische Vorlagen zu bearbeitbaren Vorlagen zu migrieren.
* Weitere Informationen zu bearbeitbaren Vorlagen finden Sie unter [Vorlagen](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html).
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
