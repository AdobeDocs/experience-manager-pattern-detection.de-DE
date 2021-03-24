---
title: DOPI
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# DOPI {#dopi}

Veralteter Index für bestellte Eigenschaften

## Hintergrund {#background}

`DOPI` identifiziert die Verwendung von Indexdefinitionen für die geordnete Eigenschaft (`primaryType=oak:QueryIndexDefinition` AND  `type="ordered"`), die seit 6.1 nicht mehr unterstützt und in 6.2 entfernt wurden.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Einige Abfragen reagieren möglicherweise nicht.
* Die Kundenfunktionalität funktioniert möglicherweise nicht ordnungsgemäß.
* Traversal Warnungen oder sogar Fehler und erhebliche Leistungsstrafen, da die veralteten Indizes keine Auswirkungen haben.

## Mögliche Lösungen {#solutions}

* Ändern Sie die Indexdefinition so, dass sie zu einer unterstützten Indexdefinition wird oder durch sie ersetzt wird. (Siehe [Oak-Abfragen und Indizierung](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html)).
* Überprüfen Sie das Projekt [work-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) und verstehen Sie, wie [DOPI-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) korrigiert und mit AEM als Cloud Service kompatibel gemacht werden können.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
