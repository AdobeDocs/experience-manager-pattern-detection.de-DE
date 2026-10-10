---
title: SPI
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 39f2d04e-c6e4-4da6-b000-0115bc2b87bf
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
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
