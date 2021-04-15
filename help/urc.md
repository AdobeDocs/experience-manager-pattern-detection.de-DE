---
title: URC
description: Hilfeseite zum Mustererkennungs-Code
translation-type: ht
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: ht
source-wordcount: '176'
ht-degree: 100%

---


# URC {#urc}

Nicht unterstützte Ausführungsmodus-Konfiguration

## Hintergrund {#background}

`URC` steht für die Verwendung von Konfigurationen, die auf einem Ausführungsmodus-Namen basieren, der in AEM as a Cloud Service nicht unterstützt wird.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Menge der Namen, die für Ausführungsmodi in AEM as a Cloud Service verwendet werden können, ist begrenzt.
* Konfigurationen, die auf nicht unterstützten Ausführungsmodus-Namen basieren, haben keine Auswirkungen, wenn sie in AEM as a Cloud Service bereitgestellt werden.

## Mögliche Lösungen {#solutions}

* Überprüfen Sie die Verwendung dieser Konfiguration, um festzustellen, ob sie erforderlich ist.
* Benennen Sie die Konfiguration um, um einen der unterstützten [Ausführungsmodus-Namen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de#custom-runmodes) zu verwenden, und befolgen Sie die [Richtlinien für die Ausführungsmodus-Auflösung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=de#runmode-resolution).
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) und verstehen Sie, wie [URC-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
