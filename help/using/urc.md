---
title: URC
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 77%

---

# URC {#urc}

Nicht unterstützte Konfiguration des Ausführungsmodus

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Nicht unterstützte Konfiguration des Ausführungsmodus"
>abstract="URC erkennt die Verwendung von Konfigurationen, die auf dem Namen eines Ausführungsmodus basieren, der in AEM as a Cloud Service nicht unterstützt wird."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Unterstützte Ausführungsmodi"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Ausführungsmodi"

`URC` identifiziert die Verwendung von Konfigurationen, die auf einem Namen eines Ausführungsmodus basieren, der in AEM as a Cloud Service nicht unterstützt wird.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist, zu überprüfen, ob alle in Ihrer Anwendung verwendeten Ausführungsmodi unterstützt werden. Und stellen Sie sicher, dass sie den Richtlinien für die Ausführungsmodusauflösung entsprechen"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Richtlinien für die Auflösung des Ausführungsmodus"

* Die Menge der Namen, die für die Ausführung verschiedener Modi in AEM as a Cloud Service verwendet werden können, ist begrenzt.
* Konfigurationen, die auf nicht unterstützten Namen für Ausführungsmodi basieren, haben keinen Effekt, wenn sie in AEM as a Cloud Service bereitgestellt werden.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Tools und Ressourcen"
>abstract="Überprüfen Sie das Projekt WKND-legacy und verstehen Sie, wie URC-Verletzungen korrigiert und mit AEM Cloud Service kompatibel gemacht werden können. Sehen Sie sich auch das Beispiel für eine URL-Verletzung auf GitHub an, um zu verstehen, wie benutzerdefinierte Run-Modus-basierte OSGi-Konfigurationen aktualisiert werden können, um AEM as a Cloud Service einzuhalten."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="WKND-Legacy-Projekt"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Beispiel für URC-Verstoß – Github"

* Überprüfen Sie die Verwendung dieser Konfiguration, um festzustellen, ob sie erforderlich ist.
* Benennen Sie die Konfiguration mit einem der unterstützten [Namen für Ausführungsmodi](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) um und folgen Sie den [Richtlinien zur Auflösung des Ausführungsmodus](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) und verstehen Sie, wie [URC-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
