---
title: SCR
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 13b14cc2-f70b-45ff-a62d-dee647311d84
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%
---
# SCR {#scr}

## Hintergrund {#background}

SIF kennzeichnet eine AEM Screens-Nutzung, die mit AEM 6.5 LTS nicht kompatibel ist.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Mögliche Lösungen {#solutions}

Finden Sie die möglichen Lösungen für die verschiedenen Untertypen unten:

* `screens.bundles.detected` - Diese Bundles werden während des Upgrades deinstalliert.
* `screens.packages.detected`: Diese Pakete werden während des Upgrades gelöscht.
* `screens.packages.dependency`: Entfernen Sie alle Abhängigkeiten von Screens aus Ihren benutzerdefinierten Paketen.
* `screens.configs.detected`: Stellen Sie sicher, dass Sie in Ihrem benutzerdefinierten Code keine Screens-Konfigurationseigenschaften verwenden.
* `screens.users.detected`: Stellen Sie sicher, dass Sie keine Screens-Dienstbenutzer in benutzerdefiniertem Code verwenden.
* `screens.paths.detected` - Entfernen Sie Screens-Pfade, nachdem Sie sichergestellt haben, dass sie nicht in AEM verwendet werden.
* `screens.resource.type.detected` - Entfernen Sie die Verwendung des Screens-Ressourcentyps.
* `screens.usage`: Entfernen von Screens-APIs aus Ihrem benutzerdefinierten Code.
