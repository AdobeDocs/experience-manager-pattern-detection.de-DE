---
title: INS
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: d89e1589-3195-4b2d-98f4-136bedaecb0b
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 100%

---

# INS {#ins}

Ungültiger Namespace

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_overview"
>title="Ungültiger Namespace"
>abstract="INS identifiziert Namespace-Probleme auf AEM-Instanz"

`INS` (Ungültiger Namespace) identifiziert Namespace-Probleme auf der AEM-Instanz.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden unter anderem folgende Untertypen verwendet:

* `uri`: Identifizieren des ungültigen Namespace-URI in AEM.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* Inhalt kann nicht repliziert (über die Ebene hinweg) oder kopiert werden (über `env` hinweg, mittels `/crx/packMgr`, oder Inhaltskopie).

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_guidance"
>title="Implementierungsleitlinien"
>abstract="Wenden Sie sich für Hilfe an die Kundenunterstützung."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Korrigieren Sie die Namespace-Definitionen gemäß der [JCR-Spezifikation](https://developer.adobe.com/experience-manager/reference-materials/spec/jcr/1.0/4.5_Namespaces.html). Führen Sie die [hier](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/how-can-i-delete-a-namespace-created-in-crx/td-p/225163?profile.language=de) erwähnten Schritte aus.
* Wenden Sie sich an unser [Experience Manager-Kundenunterstützungs-Team](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
