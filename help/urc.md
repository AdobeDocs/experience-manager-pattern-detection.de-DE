---
title: URC
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 63%

---

# URC {#urc}

Nicht unterstützte Ausführungsmodus-Konfiguration

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Nicht unterstützte Ausführungsmodus-Konfiguration"
>abstract="URC identifiziert die Verwendung von Konfigurationen, die auf einem Runmode-Namen basieren, der in AEM als Cloud Service nicht unterstützt wird."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes" text="Unterstützte Runmodi"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#runmodes" text="Ausführungsmodi"

`URC` steht für die Verwendung von Konfigurationen, die auf einem Ausführungsmodus-Namen basieren, der in AEM as a Cloud Service nicht unterstützt wird.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Durchführungsleitlinien"
>abstract="Die bewährte Methode besteht darin, zu überprüfen, ob alle in Ihrer Anwendung verwendeten Ausführungsmodi unterstützt werden, und sicherzustellen, dass sie den Richtlinien für die Auflösung des Ausführungsmodus entsprechen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#deploying" text="Richtlinien für die Runmode-Auflösung"

* Die Menge der Namen, die für Ausführungsmodi in AEM as a Cloud Service verwendet werden können, ist begrenzt.
* Konfigurationen, die auf nicht unterstützten Ausführungsmodus-Namen basieren, haben keine Auswirkungen, wenn sie in AEM as a Cloud Service bereitgestellt werden.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Tools und Ressourcen"
>abstract="Prüfen Sie das WKND-Legacy-Projekt, um zu verstehen, wie URC-Verletzungen mit AEM Cloud Service kompatibel gemacht werden können. Überprüfen Sie außerdem das Beispiel für eine URL-Verletzung auf Github, um zu verstehen, wie benutzerdefinierte runmode-basierte OSGi-Konfigurationen aktualisiert werden können, um AEM als Cloud Service einzuhalten."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="WKND-Legacy-Projekt"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Beispiel für URC-Verletzung - Github"

* Überprüfen Sie die Verwendung dieser Konfiguration, um festzustellen, ob sie erforderlich ist.
* Benennen Sie die Konfiguration um, um einen der unterstützten [Ausführungsmodus-Namen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de#custom-runmodes) zu verwenden, und befolgen Sie die [Richtlinien für die Ausführungsmodus-Auflösung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=de#runmode-resolution).
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) und verstehen Sie, wie [URC-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
