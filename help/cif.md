---
title: CIF
description: Hilfeseite zum Mustererkennungs-Code
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: d50f278a5b74b625b650bca7af67dfd77283ad9e
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 100%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifiziert die Nutzung der klassischen Version von Commerce Integration Framework, die mit AEM as a Cloud Service nicht kompatibel ist."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html?lang=de" text=" Content und Commerce"

`CIF` CIF identifiziert die Nutzung der klassischen Version von Commerce Integration Framework, die mit AEM as a Cloud Service nicht kompatibel ist. Die Meldung für jede gefundene `CIF`-Version enthält Angaben zur Nutzung und liefert zusätzliche Informationen.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `commerce.integration.framework.detected`: Inkompabilität einer klassischen Version von Commerce Integration Framework mit AEM as a Cloud Service.


## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist, jede Nutzung der klassischen Versionen von Commerce Integration Framework zu überprüfen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html?lang=de" text="Wesentliche Änderungen an CIF"

* Die klassische Version von Commerce Integration Framework wird von AEM as a Cloud Service nicht mehr unterstützt. Sie verhindert das Upgrade auf AEM as a Cloud Service.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Tools und Ressourcen"
>abstract="Dieses Handbuch hilft bei der Identifizierung der Bereiche, die Sie für die Migration zu Experience Manager Cloud Service aktualisieren müssen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html?lang=de" text="Migrationshandbuch für CIF"

* Für Experience Manager as a Cloud Service ist das CIF-Add-on die einzige unterstützte Commerce-Integrationslösung für Adobe Commerce und Commerce-Lösungen von Drittanbietern. Das CIF-Add-on wird für Kunden automatisch für Experience Manager as a Cloud Service bereitgestellt. Es ist keine manuelle Implementierung erforderlich. Weitere Informationen finden Sie in [Erste Schritte mit AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html?lang=de).
* Zur Unterstützung von Projekten, die CIF nutzen, stellt Adobe [AEM-CIF-Kernkomponenten](https://github.com/adobe/aem-core-cif-components) bereit.
* Das CIF-Add-on ist auch für AEM 6.5 über das [Software Distribution-Portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) verfügbar. Es ist kompatibel und bietet dieselben Funktionen wie das CIF-Add-on für Experience Manager as a Cloud Service. Es sind keine Anpassungen erforderlich.
* Die klassische Version von CIF und davon abhängige Lösungen sind nicht mehr verfügbar. Code, der auf dieser CIF-Version basiert und die Java-APIs com.adobe.cq.commerce.api verwendet, muss an das CIF-Add-On und seine Regeln angepasst werden.
