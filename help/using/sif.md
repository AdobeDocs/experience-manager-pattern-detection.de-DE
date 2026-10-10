---
title: SIF
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: c0a5c565-16e7-407b-befc-5a2966089da1
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
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
