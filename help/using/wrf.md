---
title: WRF
description: Hilfeseite zum Mustererkennungs-Code.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '90'
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