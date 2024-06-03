---
title: DOPI
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 100%

---

# DOPI {#dopi}

Veralteter Index für sortierte Eigenschaften

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Veralteter Index für sortierte Eigenschaften"
>abstract="Der DOPI-Code identifiziert die Verwendung von Definitionen für den Index für sortierte Eigenschaften (`primaryType=oak:QueryIndexDefinition` UND `type="ordered"`). Die Definition wurde in AEM 6.1 eingestellt und in AEM 6.2 entfernt."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing#the-ordered-index" text="Sortierter Index – veraltet"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/operations/indexing" text="Indizierung – AEM as a Cloud Service"

`DOPI` Identifiziert die Verwendung für den geordneten Index für sortierte Eigenschaften (`primaryType=oak:QueryIndexDefinition` UND `type="ordered"`). Die Definition wurde in AEM 6.1 eingestellt und in AEM 6.2 entfernt.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, alle veralteten sortierten Indizes zu überprüfen und sie zu einer unterstützten Form von Lucene-Indizes zu verschieben, um signifikante Performance-Probleme oder nicht funktionale Kundenanforderungen zu vermeiden."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/practices/best-practices-for-queries-and-indexing" text="Best Practices – Abfragen und Indizierung"

* Einige Abfragen reagieren möglicherweise nicht.
* Kundenspezifische Funktionen funktionieren möglicherweise nicht korrekt.
* Überschreitungs-Warnungen oder sogar -Fehler und erhebliche Performance-Einbußen, da die veralteten Indizes keine Wirkung haben.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Tools und Ressourcen"
>abstract="Überprüfen Sie das Projekt WKND-legacy, um zu verstehen, wie DOPI-Verletzungen korrigiert und mit AEM Cloud Service kompatibel gemacht werden können. Sehen Sie sich auch das Beispiel für DOPI-Verstoß auf GitHub an. Es kann Ihnen helfen zu verstehen, wie veraltete geordnete Indizes in Lucene-basierte Indizes konvertiert werden können, die in AEM as a Cloud Service unterstützt werden."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="WKND-Legacy-Projekt"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Beispiel für DOPI-Verstoß – Github"

* Ändern Sie die Indexdefinition so, dass sie zu einer unterstützten Indexdefinition wird oder den Index durch eine solche ersetzt. (Siehe [Oak-Abfragen und Indizierung](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing)).
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) und verstehen Sie, wie [DOPI-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
