---
title: URC
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# URC {#urc}

Nicht unterstützte Runmode-Konfiguration

## Hintergrund {#background}

`URC` identifiziert die Verwendung von Konfigurationen, die auf einem Runmode-Namen basieren, der in AEM als Cloud Service nicht unterstützt wird.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Der Namenssatz, der in AEM als Cloud Service für die Ausführungsmodi verwendet werden kann, ist begrenzt.
* Konfigurationen, die auf nicht unterstützten Ausführungsmodusnamen basieren, haben keine Auswirkung, wenn sie als Cloud Service AEM bereitgestellt werden.

## Mögliche Lösungen {#solutions}

* Überprüfen Sie die Verwendung dieser Konfiguration, um festzustellen, ob sie erforderlich ist.
* Benennen Sie die Konfiguration um, um einen der unterstützten [runmode-Namen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) zu verwenden, und folgen Sie den [Richtlinien für die Auflösung im Ausführungsmodus](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution).
* Überprüfen Sie das Projekt [work-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) und verstehen Sie, wie [URC-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) korrigiert und mit AEM als Cloud Service kompatibel gemacht werden können.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
