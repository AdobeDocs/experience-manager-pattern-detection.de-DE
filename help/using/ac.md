---
title: AC
description: Hilfeseite zum Mustererkennungs-Code.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---

# AC {#ac}

## Hintergrund {#background}

AC kennzeichnet die Verwendung von Assets-Bundles, die mit AEM 6.5 LTS nicht kompatibel ist

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Mögliche Lösungen {#solutions}

Finden Sie die möglichen Lösungen für die verschiedenen Untertypen unten:

* `asset.bundles.detected` - Dieses Bundle wird während des Upgrades deinstalliert.
* `asset.usage` - Entfernen Sie alle Abhängigkeiten von Asset-Bewertungen und Asset-Katalog-Komponenten aus benutzerdefiniertem Code. Ändern Sie gegebenenfalls den Code, um die neue API `List<Scene7ConfigSetting>` `com.day.cq.dam.scene7.api.model.Scene7ViewerConfig#getSettingsList()` zu verwenden.
* `asset.overlays.detected` - Überlagerungen, die für Assets-Bewertungs- und Katalogkomponenten erstellt wurden, müssen entfernt werden.
* `asset.resource.type.detected` - Entfernen Sie alle Verwendungszwecke des Assets-Bewertungskomponenten-Ressourcentyps in Ihrem benutzerdefinierten Code.
* `asset.paths.detected`: Verschieben Sie alle Kundeninhalte, die unter diesen Pfaden vorhanden sind, und entfernen Sie diese Pfade, nachdem Sie sichergestellt haben, dass sie nicht in AEM verwendet werden.