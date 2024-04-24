---
title: URC
description: Mustererkennungscode Hilfeseite.
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 24%

---

# URC {#urc}

Konfiguration des nicht unterstützten Ausführungsmodus

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Nicht unterstützte Ausführungsmodus-Konfiguration"
>abstract="URC identifiziert die Verwendung von Konfigurationen, die auf einem Ausführungsmodusnamen basieren, der AEM as a Cloud Service nicht unterstützt wird."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Unterstützte Ausführungsmodi"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Ausführungsmodi"

`URC`  Identifiziert die Verwendung von Konfigurationen, die auf einem Ausführungsmodusnamen basieren, der AEM as a Cloud Service nicht unterstützt wird.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist, zu überprüfen, ob alle in Ihrer Anwendung verwendeten Ausführungsmodi unterstützt werden, und sicherzustellen, dass sie den Richtlinien für die Runmode-Auflösung entsprechen."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Richtlinien für die Ausführungsmodus-Auflösung"

* Der Namenssatz, der für die Ausführung verschiedener Modi in AEM as a Cloud Service verwendet werden kann, ist begrenzt.
* Konfigurationen, die auf nicht unterstützten Ausführungsmodusnamen basieren, haben keine Auswirkung, wenn sie auf AEM as a Cloud Service bereitgestellt werden.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Tools und Ressourcen"
>abstract="Überprüfen Sie das Projekt WKND-legacy und verstehen Sie, wie URC-Verletzungen korrigiert und mit AEM Cloud Service kompatibel gemacht werden können. Sehen Sie sich auch das Beispiel für eine URL-Verletzung auf GitHub an, um zu verstehen, wie benutzerdefinierte Runmode-basierte OSGi-Konfigurationen aktualisiert werden können, um AEM as a Cloud Service einzuhalten."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="WKND-Legacy-Projekt"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Beispiel für eine URL-Verletzung - GitHub"

* Überprüfen Sie die Verwendung dieser Konfiguration, damit Sie feststellen können, ob sie erforderlich ist.
* Benennen Sie die Konfiguration mit einer der unterstützten [Ausführungsmodusnamen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) und folgen [Richtlinien zur Auflösung des Ausführungsmodus](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) und verstehen Sie, wie [URC-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
