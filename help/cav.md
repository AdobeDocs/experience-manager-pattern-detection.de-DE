---
title: CAV
description: Hilfeseite zum Mustererkennungs-Code
translation-type: ht
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: ht
source-wordcount: '257'
ht-degree: 100%

---


# CAV {#cav}

Inhaltsbereichsverletzung

## Hintergrund {#background}

`CAV` steht für das Muster, bei dem verschiedene Inhaltsbereiche in einer Weise verwendet werden, die gegen die Regeln der Inhaltsklassifizierung verstößt.

Die Verarbeitung von Sling-Anfragen definiert, wie der Inhalt einer Ressource, insbesondere deren `sling:resourceType`-Eigenschaft, zur Bestimmung des Skripts verwendet wird, das zum Rendern des Inhalts verwendet wird. (Weitere Informationen finden Sie unter [Auffinden des Skripts](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html?lang=de#locating-the-script).) Sling bietet auch Techniken für den Zugriff auf und das Zusammenführen von Ressourcen durch „Überlagerungen“ und „Überschreibungen“. Diese werden als Teil von [Sling Resource Merger](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=de) und in [Überlagerungen](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=de) beschrieben.

Um es sicherer und für den Kunden verständlicher zu machen, welche Bereiche von `/libs` sicher verwendet und überlagert werden können, wurde der Inhalt in `/libs` mit „Mixin“-Eigenschaften klassifiziert: Öffentlich, Abstrakt, Final und Intern. Jede Klassifizierung beinhaltet Regeln darüber, wie der Inhalt verwendet, vererbt oder überlagert werden darf. Eine ausführliche Beschreibung finden Sie unter [Nachhaltige Aktualisierungen](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=de).

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Ein AEM-Upgrade kann zu Problemen beim Rendering von Seiten und anderen unerwünschten Verhaltensweisen führen.
* Sicherheits-Updates wirken sich nicht aus.

## Mögliche Lösungen {#solutions}

* Minimieren Sie die Verwendung von Inhaltsüberlagerungen auf die Fälle, in denen sie benötigt werden.
* Vermeiden Sie insbesondere das Überlagern von eingeschränkten Inhalten (Klassifizierungen „Final“ und „Intern“).
* Erwägen Sie die Anpassung von Änderungen, die nach AEM-Upgrades, ServicePack- oder CumulativeFixPack-Installationen aus `/libs` kommen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
