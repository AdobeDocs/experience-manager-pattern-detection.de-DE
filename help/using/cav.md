---
title: CAV
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 74%

---

# CAV {#cav}

Inhaltsbereichsverletzung

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Inhaltsbereichsverletzung"
>abstract="CAV-Code kennzeichnet das Muster, bei dem verschiedene Inhaltsbereiche in einer Weise verwendet werden, die gegen die Regeln der Inhaltsklassifizierung verstößt. Dieser Verstoß gibt Ihnen einen Überblick über Überlagerungen, eingeschränkte Inhalte, die möglicherweise geändert werden müssen, nachdem sie auf AEM as a Cloud Service verschoben wurden."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sling Resource Merger"

`CAV` identifiziert das Muster, bei dem verschiedene Inhaltsbereiche in einer Weise verwendet werden, die gegen die Regeln der Inhaltsklassifizierung verstößt.

Die Verarbeitung von Sling-Anfragen definiert, wie der Inhalt einer Ressource, insbesondere deren Eigenschaft `sling:resourceType`, zur Bestimmung des Skripts verwendet wird, das zum Rendern des Inhalts genutzt wird. Weitere Informationen finden Sie unter [Auffinden des Skripts](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script). Sling bietet außerdem Techniken zum Zugriff auf und Zusammenführen von Ressourcen über Überlagerungen und Überschreibungen. Diese Techniken werden im Rahmen der [Sling Resource Merger](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) und [Überlagerungen](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/platform/overlays).

So können Kunden leichter nachvollziehen, welche Bereiche von `/libs` sind sicher zu verwenden und zu überlagern, der Inhalt in `/libs` wird mit &quot;mixin&quot;-Eigenschaften klassifiziert:

* Öffentlich
* Abstrakt
* Endgültig
* intern

Jede Klassifizierung beinhaltet Regeln darüber, wie der Inhalt verwendet, vererbt oder überlagert werden darf. Eine ausführliche Beschreibung finden Sie unter [Nachhaltige Aktualisierungen](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades).

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* Ein AEM-Upgrade kann zu Problemen beim Rendering von Seiten und anderen unerwünschten Verhaltensweisen führen.
* Sicherheits-Updates wirken sich nicht aus.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Implementierungsleitlinien"
>abstract="Die mit CAS ermittelten Muster, bei denen verschiedene Inhaltsbereichsverstöße vorliegen, sollten überprüft werden. Abschließende und interne Inhaltsklassifizierungsbereiche sollten vermieden werden. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Nachhaltige Aktualisierungen"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Minimieren Sie die Verwendung von Inhaltsüberlagerungen auf die Fälle, in denen sie benötigt werden.
* Vermeiden Sie insbesondere das Überlagern von eingeschränkten Inhalten (Klassifizierungen „Final“ und „Intern“).
* Erwägen Sie die Anpassung von Änderungen aus `/libs` nach AEM-Aktualisierungen sowie Service Pack- oder Cumulative Fix Pack-Installationen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
