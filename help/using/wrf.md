---
title: WRF
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 36578498-d5b2-46d1-a274-a1646ceaa764
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
# WRF {#wrf}

## Hintergrund {#background}

WRF kennzeichnet eine We-Retail-Nutzung, die mit AEM 6.5 LTS nicht kompatibel ist.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Mögliche Lösungen {#solutions}

Finden Sie die möglichen Lösungen für die verschiedenen Untertypen unten:

* `weretail.bundles.detected` - Diese Bundles werden während des Upgrades deinstalliert
* `weretail.packages.detected`: Diese Pakete werden während des Upgrades gelöscht
* `weretail.configs.detected` - Verwenden Sie keine We.Retail-Konfigurationseigenschaften in Ihrem benutzerdefinierten Code
* `weretail.packages.dependency` - Entfernen der Abhängigkeit von einem benutzerdefinierten Paket auf We.Retail
* `weretail.paths.detected` - Diese We.Retail-Pfade können gelöscht werden, nachdem sichergestellt wurde, dass Sie keine Social Media verwenden
* `weretail.resource.type.detected` - We.Retail-Ressourcentypverwendung entfernen
* `weretail.usage` - Entfernen von We.Retail-APIs aus Ihrem benutzerdefinierten Code.
