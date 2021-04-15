---
title: CTEM
description: Hilfeseite zum Mustererkennungs-Code
translation-type: ht
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: ht
source-wordcount: '140'
ht-degree: 100%

---


# CTEM {#ctem}

Benutzerdefinierte Vorlage

## Hintergrund {#background}

`CTEM` steht für benutzerdefinierte Vorlagen, die in AEM installiert wurden. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt.

Vorlagen werden durch einen primären Typwert von „cq:Template“ identifiziert. Um die Kategorien der Vorlage zu unterscheiden, werden Untertypen mit diesen Codes verwendet:

* `custom.editable.template`: Der Pfad der Vorlage beginnt nicht mit „/apps“.
* `custom.static.template`: Der Pfad der Vorlage beginnt mit „/apps“.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Best Practice ist, alle statischen Vorlagen in bearbeitbare Vorlagen zu verschieben.

## Mögliche Lösungen {#solutions}

* Nutzen Sie die [AEM-Modernisierungs-Tools](https://opensource.adobe.com/aem-modernize-tools/), um statische Vorlagen zu bearbeitbaren Vorlagen zu migrieren.
* Weitere Informationen zu bearbeitbaren Vorlagen finden Sie unter [Vorlagen](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html?lang=de).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
