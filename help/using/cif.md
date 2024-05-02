---
title: CIF
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 70%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifiziert die Nutzung der klassischen Version von Commerce Integration Framework, die mit AEM as a Cloud Service nicht kompatibel ist."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/content-and-commerce/introduction" text=" Content and Commerce"

`CIF`  Identifiziert die klassische Version der Commerce integration framework-Nutzung, die mit AEM as a Cloud Service nicht kompatibel ist. Die Nachricht für jede `CIF` Finden Sie die Verwendung und geben Sie zusätzliche Informationen an.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `commerce.integration.framework.detected`: Inkompabilität einer klassischen Version von Commerce Integration Framework mit AEM as a Cloud Service.


## Mögliche Auswirkungen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist, jede Nutzung der klassischen Versionen von Commerce Integration Framework zu überprüfen."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/content-and-commerce/changes" text="Wesentliche Änderungen an CIF"

* Die klassische Version von Commerce Integration Framework wird von AEM as a Cloud Service nicht mehr unterstützt. Sie verhindert das Upgrade auf AEM as a Cloud Service.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Tools und Ressourcen"
>abstract="Dieser Leitfaden hilft bei der Identifizierung von Bereichen, die für die Experience Manager Cloud Service-Migration aktualisiert werden müssen."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/content-and-commerce/migration" text="Migrationshandbuch für CIF"

* Für Experience Manager as a Cloud Service ist das CIF Add-on die einzige unterstützte Commerce-Integrationslösung für Adobe Commerce- und Drittanbieter-Commerce-Lösungen. Das CIF-Add-on wird für Kunden automatisch für Experience Manager as a Cloud Service bereitgestellt. Es ist keine manuelle Implementierung erforderlich. Siehe [Erste Schritte mit AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/storefront/getting-started).
* Um Projekte mit CIF-Bereitstellung zu unterstützen, stellt Adobe die [AEM CIF-Kernkomponenten](https://github.com/adobe/aem-core-cif-components) bereit.
* CIF Add-on ist auch für AEM 6.5 über die [Software Distribution-Portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html). Es ist kompatibel und bietet dieselben Funktionen wie das CIF-Add-on für Experience Manager as a Cloud Service. Es sind keine Anpassungen erforderlich.
* Das klassische CIF mit seinen Abhängigkeiten ist nicht mehr verfügbar. Code, der auf diese CIF Version mithilfe von com.adobe.cq.commerce.api Java™-APIs basiert, muss an das CIF Add-on und dessen Prinzipien angepasst werden.
