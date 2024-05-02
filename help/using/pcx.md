---
title: PCX
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 95%

---

# PCX {#pcx}

Seitenkomplexität

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Seitenkomplexität"
>abstract="PCX kennzeichnet Seiten, die eine große Anzahl von Knoten in ihrer Struktur enthalten."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Wesentliche Änderungen – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service – Versionshinweise"

`PCX`  Identifiziert Seiten, die viele Knoten in ihrer Struktur enthalten.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `page.complexity.medium`: Eine Seite enthält eine mäßig hohe Anzahl von Knoten, was die Rendering-Leistung beeinträchtigen kann.
* `page.complexity.high`: Eine Seite enthält eine hohe Anzahl von Knoten, was die Rendering-Leistung wahrscheinlich beeinträchtigt.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* Eine große Anzahl von Knoten innerhalb einer Seite kann deren Rendering-Leistung beeinträchtigen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, die Inhaltsstruktur zu überprüfen, um die Komplexität der Seite zu reduzieren, was wiederum dazu beiträgt, die Leistung des Seiten-Renderings zu verbessern. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Reduzieren Sie die Gesamtzahl der Knoten auf einer Seite durch die folgenden Schritte:
   * Stellen Sie sicher, dass es keine unnötigen Container gibt.
   * Testen Sie, ob dasselbe Layout mit weniger Containern erreicht werden kann.
   * Vereinfachen Sie den Seiteninhalt.
   * Verringern Sie die Tiefe der Knotenstruktur.
   * Refaktorisieren Sie der Einfachheit halber alle enthaltenen Experience Fragments.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
