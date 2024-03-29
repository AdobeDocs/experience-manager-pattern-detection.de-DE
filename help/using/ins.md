---
title: INS
description: Hilfeseite zum Mustererkennungs-Code
exl-id: d89e1589-3195-4b2d-98f4-136bedaecb0b
source-git-commit: 07af2303583072effbaaf23de1878e4d0dcfd2bd
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

`INS` Ungültiger Namespace identifiziert Namespace-Probleme auf AEM-Instanz.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden unter anderem folgende Untertypen verwendet:

* `uri`: Identifizieren des ungültigen Namespace-URI in AEM.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Inhalte können (über die gesamte Ebene hinweg) nicht repliziert oder (über ENV hinweg – via `/crx/packMgr` oder Inhaltskopie) nicht kopiert werden.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_guidance"
>title="Implementierungsleitlinien"
>abstract="Wenden Sie sich für Hilfe an die Kundenunterstützung."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Korrigieren Sie die Namespace-Definitionen gemäß der [JCR-Spezifikation](https://developer.adobe.com/experience-manager/reference-materials/spec/jcr/1.0/4.5_Namespaces.html). Befolgen Sie die [hier](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/how-can-i-delete-a-namespace-created-in-crx/td-p/225163) erwähnten Schritte.
* Wenden Sie sich an unser [Experience Manager-Support-Team](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder Probleme zu besprechen.
