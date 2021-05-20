---
title: CAV
description: Hilfeseite zum Mustererkennungs-Code
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 1966a3e83ab6b2247d9f1095c8965eac399e3b6e
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 100%

---

# CAV {#cav}

Inhaltsbereichsverletzung

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Inhaltsbereichsverletzung"
>abstract="CAV-Code kennzeichnet das Muster, bei dem verschiedene Inhaltsbereiche in einer Weise verwendet werden, die gegen die Regeln der Inhaltsklassifizierung verstößt. Diese Verletzung würde Ihnen einen Überblick über Überlagerungen und eingeschränkte Inhalte geben, die möglicherweise geändert werden müssen, sobald der Wechsel zu AEM as a Cloud Service erfolgt."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=de#platform" text="Sling Resource Merger"

`CAV` kennzeichnet das Muster, bei dem verschiedene Inhaltsbereiche in einer Weise verwendet werden, die gegen die Regeln der Inhaltsklassifizierung verstößt.

Die Verarbeitung von Sling-Anfragen definiert, wie der Inhalt einer Ressource, insbesondere deren `sling:resourceType`-Eigenschaft, zur Bestimmung des Skripts verwendet wird, das zum Rendern des Inhalts verwendet wird. Weitere Informationen finden Sie unter [Auffinden des Skripts](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html?lang=de#locating-the-script). Sling bietet auch Techniken für den Zugriff auf und das Zusammenführen von Ressourcen durch „Überlagerungen“ und „Überschreibungen“. Diese werden als Teil von [Sling Resource Merger](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=de) und in [Überlagerungen](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=de) beschrieben.

Um es sicherer und für den Kunden verständlicher zu machen, welche Bereiche von `/libs` sicher verwendet und überlagert werden können, wurde der Inhalt in `/libs` mit „Mixin“-Eigenschaften klassifiziert: Öffentlich, Abstrakt, Final und Intern. Jede Klassifizierung beinhaltet Regeln darüber, wie der Inhalt verwendet, vererbt oder überlagert werden darf. Eine ausführliche Beschreibung finden Sie unter [Nachhaltige Aktualisierungen](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=de).

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Ein AEM-Upgrade kann zu Problemen beim Rendering von Seiten und anderen unerwünschten Verhaltensweisen führen.
* Sicherheits-Updates wirken sich nicht aus.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Implementierungsleitlinien"
>abstract="Die mit CAS ermittelten Muster, bei denen eine Verletzung verschiedener Inhaltsbereiche vorliegt, sollten überprüft werden. Abschließende und interne Inhaltsklassifizierungsbereiche sollten vermieden werden. Wenden Sie sich an den Adobe Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html" text="Nachhaltige Aktualisierungen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Minimieren Sie die Verwendung von Inhaltsüberlagerungen auf die Fälle, in denen sie benötigt werden.
* Vermeiden Sie insbesondere das Überlagern von eingeschränkten Inhalten (Klassifizierungen „Final“ und „Intern“).
* Erwägen Sie die Anpassung von Änderungen, die nach AEM-Upgrades, ServicePack- oder CumulativeFixPack-Installationen aus `/libs` kommen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
