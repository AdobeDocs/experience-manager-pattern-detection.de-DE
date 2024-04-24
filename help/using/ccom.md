---
title: CCOM
description: Mustererkennungscode Hilfeseite.
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 66%

---

# CCOM {#ccom}

Benutzerdefinierte Komponente

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Benutzerdefinierte Komponente"
>abstract="CCOM kennzeichnet benutzerdefinierte Komponenten, die in AEM installiert wurden. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt"

`CCOM` Identifiziert benutzerdefinierte Komponenten, die auf AEM installiert wurden. Diese Informationen werden zum Zweck der Bewertung von Best Practices bereitgestellt.

Ein Untertyp wird mit diesem Code verwendet, um die Kategorie der Komponente zu unterscheiden:

* `custom.core`: Ein Übertyp in der Kette der Übertypen der Komponente enthält „core/wcm/components/“ und zeigt damit an, dass er von einer Kernkomponente erbt.
* `custom.foundation`: Ein Übertyp in der Kette der Übertypen der Komponente enthält „core/wcm/components/“ und zeigt damit an, dass er von einer Kernkomponente erbt.
* `custom.overlay.foundation`: Der Komponentenpfad enthält „wcm/foundation/components/“ oder „foundation/components/“ und zeigt damit an, dass er eine Basiskomponente überlagert.
* `custom`: Die benutzerdefinierte Komponente übernimmt oder überlagert keine Kern- oder Basiskomponente.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Best Practice ist, die Anzahl der benutzerdefinierten Komponenten zu minimieren, Kernkomponenten zu verwenden und Kernkomponenten mit dem Stilsystem zu verwenden, damit Sie technische Schulden reduzieren können.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist, die Anzahl der benutzerdefinierten Komponenten zu minimieren, Kernkomponenten zu verwenden und Kernkomponenten mit dem Stilsystem zu verwenden, um technische Schulden zu reduzieren."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-core-components/using/introduction" text="Kernkomponenten"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring" text="Stilsystem"

* Weitere Informationen zu Kernkomponenten finden Sie unter [Einführung in Kernkomponenten](https://experienceleague.adobe.com/de/docs/experience-manager-core-components/using/introduction).
* Weitere Informationen zum Stilsystem finden Sie unter [Verwenden des Stilsystems](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring).
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
