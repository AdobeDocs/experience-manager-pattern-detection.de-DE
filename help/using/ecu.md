---
title: ECU
description: Hilfeseite zum Mustererkennungs-Code
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '264'
ht-degree: 100%

---

# ECU {#ecu}

NICHT MEHR UNTERSTÜTZT: Verwendung fremder Inhalte (ersetzt durch CAV, Content Area Violation – Inhaltsbereichsverletzung)

## Hintergrund {#background}

`ECU` kennzeichnet das Muster, bei dem verschiedene Inhaltsbereiche in einer Weise verwendet werden, die gegen die Regeln der Inhaltsklassifizierung verstößt.

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
