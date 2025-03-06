---
title: SPI
description: Hilfeseite zum Mustererkennungs-Code.
source-git-commit: e050b9190f67fd6ccfac31490c4bf2a60d47731f
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 8%

---

# SPI {#spi}

## Hintergrund {#background}

SIF identifiziert die Verwendung von Search and Promote, die mit AEM 6.5 LTS nicht kompatibel ist.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Mögliche Lösungen {#solutions}

Finden Sie die möglichen Lösungen für die verschiedenen Untertypen unten:

* `searchpromote.bundles.detected` - Diese Bundles werden während des Upgrades deinstalliert
* `earchpromote.packages.detected`: Diese Pakete werden während des Upgrades gelöscht
* `searchpromote.packages.dependency` - Entfernen Sie alle Such- und Promote-Abhängigkeiten, die Ihre benutzerdefinierten Pakete möglicherweise haben.
* `searchpromote.usage` - Entfernen von Search- und Promote-APIs aus Ihrem benutzerdefinierten Code
* `searchpromote.users.detected` - Verwenden Sie keine Search and Promote-Service-Benutzer in benutzerdefiniertem Code
* `searchpromote.configs.detected` - Verwenden Sie keine Search- und Promote-Konfigurationseigenschaften in Ihrem benutzerdefinierten Code.