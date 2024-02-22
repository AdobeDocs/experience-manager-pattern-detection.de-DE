---
title: URC
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '258'
ht-degree: 100%

---

# URC {#urc}

Nicht unterstützte Ausführungsmodus-Konfiguration

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Nicht unterstützte Ausführungsmodus-Konfiguration"
>abstract="URC kennzeichnet die Verwendung von Konfigurationen, die auf einem Ausführungsmodus-Namen basieren, der in AEM as a Cloud Service nicht unterstützt wird."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de#custom-runmodes" text="Unterstützte Ausführungsmodi"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=de#runmodes" text="Ausführungsmodi"

`URC` kennzeichnet die Verwendung von Konfigurationen, die auf einem Ausführungsmodus-Namen basieren, der in AEM as a Cloud Service nicht unterstützt wird.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, zu überprüfen, ob alle in Ihrem Programm verwendeten Ausführungsmodi unterstützt werden, und sicherzustellen, dass sie den Richtlinien zur Auflösung von Ausführungsmodi entsprechen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=de#deploying" text="Richtlinien für die Ausführungsmodus-Auflösung"

* Die Menge der Namen, die für Ausführungsmodi in AEM as a Cloud Service verwendet werden können, ist begrenzt.
* Konfigurationen, die auf nicht unterstützten Ausführungsmodus-Namen basieren, haben keine Auswirkungen, wenn sie in AEM as a Cloud Service bereitgestellt werden.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Tools und Ressourcen"
>abstract="Überprüfen Sie das Projekt WKND-legacy und verstehen Sie, wie URC-Verletzungen korrigiert und mit AEM Cloud Service kompatibel gemacht werden können. Lesen Sie auch das Beispiel für eine URC-Verletzung auf Github, um zu verstehen, wie benutzerdefinierte Ausführungsmodus-basierte OSGi-Konfigurationen aktualisiert werden können, damit sie mit AEM as a Cloud Service übereinstimmen."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="WKND-Legacy-Projekt"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Beispiel für URC-Verletzung – Github"

* Überprüfen Sie die Verwendung dieser Konfiguration, um festzustellen, ob sie erforderlich ist.
* Benennen Sie die Konfiguration um, um einen der unterstützten [Ausführungsmodus-Namen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de#custom-runmodes) zu verwenden, und befolgen Sie die [Richtlinien für die Ausführungsmodus-Auflösung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=de#runmode-resolution).
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) und verstehen Sie, wie [URC-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
