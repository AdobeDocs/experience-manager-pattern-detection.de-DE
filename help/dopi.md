---
title: DOPI
description: Hilfeseite zum Mustererkennungs-Code
translation-type: ht
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: ht
source-wordcount: '143'
ht-degree: 100%

---


# DOPI {#dopi}

Veralteter Index für sortierte Eigenschaften

## Hintergrund {#background}

`DOPI` steht für die Verwendung von Indexdefinitionen für sortierte Eigenschaften (`primaryType=oak:QueryIndexDefinition` UND `type="ordered"`), die seit 6.1 veraltet sind und in 6.2 entfernt wurden.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Einige Abfragen reagieren möglicherweise nicht.
* Kundenspezifische Funktionen funktionieren möglicherweise nicht korrekt.
* Überschreitungs-Warnungen oder sogar -Fehler und erhebliche Performance-Einbußen, da die veralteten Indizes keine Wirkung haben.

## Mögliche Lösungen {#solutions}

* Ändern Sie die Indexdefinition so, dass sie zu einer unterstützten Indexdefinition wird, oder ersetzen Sie sie durch eine solche. (Siehe [Oak-Abfragen und Indizierung](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=de)).
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) und verstehen Sie, wie [DOPI-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
