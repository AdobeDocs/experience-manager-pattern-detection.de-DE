---
title: ECU
description: Mustererkennungscode Hilfeseite.
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 50%

---

# ECU {#ecu}

NICHT MEHR UNTERSTÜTZT: Verwendung fremder Inhalte (ersetzt durch CAV, Content Area Violation – Inhaltsbereichsverletzung)

## Hintergrund {#background}

`ECU`  Identifiziert das Muster, bei dem verschiedene Inhaltsbereiche so verwendet werden, dass die Regeln der Inhaltsklassifizierung verletzt werden.

Die Verarbeitung von Sling-Anfragen definiert, wie der Inhalt einer Ressource und ihre `sling:resourceType` -Eigenschaft verwendet wird, um das Skript zu bestimmen, das zum Rendern des Inhalts verwendet wird. (Weitere Informationen finden Sie unter [Auffinden des Skripts](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script).) Sling bietet auch Techniken für den Zugriff auf und das Zusammenführen von Ressourcen durch „Überlagerungen“ und „Überschreibungen“. Diese werden als Teil von [Sling Resource Merger](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) und in [Überlagerungen](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays) beschrieben.

So können Kunden leichter nachvollziehen, welche Bereiche von `/libs` sicher sind, den Inhalt in zu verwenden und zu überlagern `/libs` wurde mit &quot;Mixin&quot;-Eigenschaften klassifiziert: &quot;Öffentlich&quot;, &quot;Abstrakt&quot;, &quot;Abgeschlossen&quot;und &quot;Intern&quot;. Jede Klassifizierung beinhaltet Regeln darüber, wie der Inhalt verwendet, vererbt oder überlagert werden darf. Eine ausführliche Beschreibung finden Sie unter [Nachhaltige Aktualisierungen](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades).

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Ein AEM-Upgrade kann zu Problemen beim Rendering von Seiten und anderen unerwünschten Verhaltensweisen führen.
* Sicherheits-Updates wirken sich nicht aus.

## Mögliche Lösungen {#solutions}

* Minimieren Sie die Verwendung von Inhaltsüberlagerungen auf die Fälle, in denen sie benötigt werden.
* Vermeiden Sie insbesondere das Überlagern von eingeschränkten Inhalten (Klassifizierungen „Final“ und „Intern“).
* Erwägen Sie die Anpassung von Änderungen aus `/libs` nach AEM Aktualisierungen, Service Pack- oder Cumulative Fix Pack-Installationen.
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
