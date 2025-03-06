---
title: SIF
description: Hilfeseite zum Mustererkennungs-Code.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 7%

---

# SIF {#sif}

## Hintergrund {#background}

SIF kennzeichnet eine Social-Media-Nutzung, die mit AEM 6.5 LTS nicht kompatibel ist.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Mögliche Lösungen {#solutions}

Finden Sie die möglichen Lösungen für die verschiedenen Untertypen unten:

* `social.bundles.detected` - Diese Bundles werden während des Upgrades deinstalliert
* `social.packages.detected`: Diese Pakete werden während des Upgrades gelöscht
* `social.packages.dependency` - Bitte die Paketabhängigkeit von Social aus benutzerdefinierten Paketen entfernen
* `social.nodes.detected` - Benutzerdefinierten Code aktualisieren, um keine sozialen Knoten zu erstellen
* `social.configs.detected` - Keine Eigenschaften der Social-Media-Konfiguration im benutzerdefinierten Code verwenden
* `social.users.detected` - Verwenden Sie keine Social-Media-Benutzer in benutzerdefiniertem Code
* `social.overlays.detected` - Verwendung von sozialen Überlagerungen entfernen
* `social.paths.detected` - Entfernen Sie Social-Media-Pfade, nachdem Sie sichergestellt haben, dass diese Pfade in AEM nicht verwendet werden.
* `social.resource.type.detected` - Verwendung von Social-Media-Ressourcen entfernen
* `social.usage` - Entfernen von Social-APIs aus benutzerdefiniertem Code.