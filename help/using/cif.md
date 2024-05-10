---
title: CIF
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '307'
ht-degree: 100%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifiziert die Nutzung der klassischen Version von Commerce Integration Framework, die mit AEM as a Cloud Service nicht kompatibel ist."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/content-and-commerce/introduction" text=" Content and Commerce"

`CIF` identifiziert die Nutzung der klassischen Version von Commerce Integration Framework, die mit AEM as a Cloud Service nicht kompatibel ist. Die Meldung für jeden `CIF`-Fund identifiziert die Verwendung und bietet zusätzliche Informationen.

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

* Für Experience Manager as a Cloud Service ist das CIF-Add-on die einzige unterstützte Commerce-Integrationslösung für Adobe Commerce und Commerce-Lösungen von Drittanbietern. Das CIF-Add-on wird für Kunden automatisch für Experience Manager as a Cloud Service bereitgestellt. Es ist keine manuelle Implementierung erforderlich. Siehe [Erste Schritte mit AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/content-and-commerce/storefront/getting-started).
* Um Projekte mit CIF-Bereitstellung zu unterstützen, stellt Adobe die [AEM CIF-Kernkomponenten](https://github.com/adobe/aem-core-cif-components) bereit.
* Das CIF-Add-on ist auch für AEM 6.5 über das [Software-Verteilungsportal](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) verfügbar. Es ist kompatibel und bietet dieselben Funktionen wie das CIF-Add-on für Experience Manager as a Cloud Service. Es sind keine Anpassungen erforderlich.
* Das klassische CIF mit seinen Abhängigkeiten ist nicht mehr verfügbar. Code, der auf dieser CIF-Version basiert und die Java™-APIs com.adobe.cq.commerce.api verwendet, muss an das CIF-Add-On und seine Regeln angepasst werden.
