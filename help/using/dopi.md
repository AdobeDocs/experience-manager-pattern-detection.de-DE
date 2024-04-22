---
title: DOPI
description: Mustererkennungscode Hilfeseite.
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 44%

---

# DOPI {#dopi}

Veralteter Index für sortierte Eigenschaften

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Veralteter Index für sortierte Eigenschaften"
>abstract="DOPI-Code identifiziert die Verwendung von sortierten Eigenschafts-Indexdefinitionen (`primaryType=oak:QueryIndexDefinition` AND type=&quot;ordered&quot;), die seit 6.1 veraltet sind und in 6.2 entfernt wurden."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing#the-ordered-index" text="Sortierter Index – veraltet"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/operations/indexing" text="Indizierung – AEM as a Cloud Service"

DOPI identifiziert die Verwendung geordneter Eigenschaftenindex-Definitionen (`primaryType=oak:QueryIndexDefinition` UND `type="ordered"`), die seit 6.1 veraltet sind und in 6.2 entfernt wurden.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist, alle veralteten sortierten Indizes zu überprüfen und sie in die unterstützte Form von Lucene-Indizes zu verschieben, um signifikante Leistungsprobleme oder nicht funktionierende Kundenanforderungen zu vermeiden."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/practices/best-practices-for-queries-and-indexing" text="Best Practices – Abfragen und Indizierung"

* Einige Abfragen reagieren möglicherweise nicht.
* Kundenspezifische Funktionen funktionieren möglicherweise nicht korrekt.
* Überschreitungs-Warnungen oder sogar -Fehler und erhebliche Performance-Einbußen, da die veralteten Indizes keine Wirkung haben.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Tools und Ressourcen"
>abstract="Überprüfen Sie das Projekt WKND-legacy und verstehen Sie, wie DOPI-Verletzungen korrigiert und mit AEM Cloud Service kompatibel gemacht werden können. Sehen Sie sich auch das Beispiel einer DOPI-Verletzung auf GitHub an, um zu erfahren, wie ältere geordnete Indizes in Lucene-basierte Indizes konvertiert werden können, die in AEM as a Cloud Service unterstützt werden."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="WKND-Legacy-Projekt"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Beispiel für eine DOPI-Verletzung - GitHub"

* Ändern Sie die Indexdefinition so, dass sie zu einer unterstützten Indexdefinition wird oder den Index durch ersetzt. (Siehe [Oak-Abfragen und Indizierung](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing)).
* Überprüfen Sie das Projekt [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) und verstehen Sie, wie [DOPI-Verletzungen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) korrigiert und mit AEM as a Cloud Service kompatibel gemacht werden können.
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
