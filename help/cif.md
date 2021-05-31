---
title: CIF
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: 84aea5b24e51ce5672826bad4ec126074bf24a09
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 10%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifiziert die klassische Version der Commerce Integration Framework-Verwendung, die mit AEM als Cloud Service inkompatibel ist."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html" text=" Inhalt und Handel"

`CIF` CIF identifiziert die klassische Version der Commerce Integration Framework-Verwendung, die mit AEM als Cloud Service inkompatibel ist. Die Meldung für jedes `CIF`-Ergebnis identifiziert die Verwendung und stellt zusätzliche Informationen bereit.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `commerce.integration.framework.detected`: Eine klassische Version des Commerce Integration Framework ist mit AEM as a Cloud Service inkompatibel.


## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist, alle klassischen Versionen der Verwendung des Commerce Integration Framework zu überprüfen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html" text="Wesentliche Änderungen an CIF"

* Die klassische Version des Commerce Integration Framework wird von AEM als Cloud Service nicht mehr unterstützt. Dadurch würde das Upgrade auf AEM als Cloud Service blockiert.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Tools und Ressourcen"
>abstract="Dieses Handbuch hilft dabei, die Bereiche zu identifizieren, die für die Migration von Experience Manager Cloud Services aktualisiert werden müssen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html" text="Migrationshandbuch für CIF"

* Für Experience Manager as a Cloud Service ist das CIF-Add-on die einzige unterstützte Commerce-Integrationslösung für Adobe Commerce- und Drittanbieter-Commerce-Lösungen. Das CIF-Add-on wird automatisch für Kunden auf dem Experience Manager als Cloud Service bereitgestellt. Es ist keine manuelle Bereitstellung erforderlich. Siehe [Erste Schritte mit AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html).
* Zur Unterstützung von Projekten, die CIF-Adobe bereitstellen, stellt [AEM CIF-Kernkomponenten](https://github.com/adobe/aem-core-cif-components) bereit.
* Das CIF-Add-on ist auch für AEM 6.5 über das [Software Distribution-Portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) verfügbar. Es ist kompatibel und bietet dieselben Funktionen wie das CIF-Add-on für Experience Manager als Cloud Service - es sind keine Anpassungen erforderlich.
* Classic CIF mit seinen Abhängigkeiten ist nicht mehr verfügbar. Code, der sich auf diese CIF-Version mithilfe von com.adobe.cq.commerce.api Java-APIs stützt, muss an das CIF-Add-on und dessen Prinzipien angepasst werden.
