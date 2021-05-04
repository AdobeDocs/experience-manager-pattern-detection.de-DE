---
title: DOPI
description: Hilfeseite zum Mustererkennungs-Code
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 55%

---

# DOPI {#dopi}

Veralteter Index für sortierte Eigenschaften

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Veralteter Index für sortierte Eigenschaften"
>abstract="Der DOPI-Code identifiziert die Verwendung der Indexdefinitionen für die geordnete Eigenschaft (primaryType=oak:QueryIndexDefinition AND type=&quot;ordered&quot;), die seit 6.1 nicht mehr unterstützt und in 6.2 entfernt wurden."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=en#the-ordered-index" text="Geordneter Index - veraltet"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=de" text="Indexierung - AEM als Cloud Service"

`DOPI` steht für die Verwendung von Indexdefinitionen für sortierte Eigenschaften (`primaryType=oak:QueryIndexDefinition` UND `type="ordered"`), die seit 6.1 veraltet sind und in 6.2 entfernt wurden.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Durchführungsleitlinien"
>abstract="Best Practice ist, alle nicht mehr unterstützten Indizes zu überprüfen und sie in unterstützte Form von lucene-Indizes zu verschieben, um wesentliche Leistungsprobleme oder nicht funktionierende Kundenanforderungen zu vermeiden."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/practices/best-practices-for-queries-and-indexing.html" text="Best Practices - Abfragen und Indizierung"

* Einige Abfragen reagieren möglicherweise nicht.
* Kundenspezifische Funktionen funktionieren möglicherweise nicht korrekt.
* Überschreitungs-Warnungen oder sogar -Fehler und erhebliche Performance-Einbußen, da die veralteten Indizes keine Wirkung haben.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Tools und Ressourcen"
>abstract="Prüfen Sie das WKND-Legacy-Projekt, um zu verstehen, wie DOPI-Verletzungen mit AEM Cloud Service kompatibel gemacht werden können. Sehen Sie sich auch das Beispiel für eine DOPI-Verletzung auf Github an, um zu verstehen, wie Legacy-Indizes in Lucene-basierte Indizes konvertiert werden können, die in AEM als Cloud Service unterstützt werden."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="WKND-Legacy-Projekt"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Beispiel für eine DOPI-Verletzung - Github"

* Ändern Sie die Indexdefinition so, dass sie zu einer unterstützten Indexdefinition wird, oder ersetzen Sie sie durch eine solche. (Siehe [Oak-Abfragen und Indizierung](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=de)).
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) und verstehen Sie, wie [DOPI-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
