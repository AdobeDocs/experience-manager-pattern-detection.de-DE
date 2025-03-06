---
title: SCR
description: Hilfeseite zum Mustererkennungs-Code.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
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