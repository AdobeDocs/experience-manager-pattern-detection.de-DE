---
title: ECU
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 100%

---

# ECU {#ecu}

NICHT MEHR UNTERSTÜTZT: Verwendung fremder Inhalte (ersetzt durch CAV, Content Area Violation – Inhaltsbereichsverletzung)

## Hintergrund {#background}

`ECU` identifiziert das Muster, bei dem verschiedene Inhaltsbereiche in einer Weise verwendet werden, die gegen die Regeln der Inhaltsklassifizierung verstößt.

Die Verarbeitung von Sling-Anfragen definiert, wie der Inhalt einer Ressource, insbesondere deren Eigenschaft `sling:resourceType`, zur Bestimmung des Skripts verwendet wird, das zum Rendern des Inhalts genutzt wird. (Weitere Informationen finden Sie unter [Auffinden des Skripts](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script).) Sling bietet auch Techniken für den Zugriff auf und das Zusammenführen von Ressourcen durch Überlagerungen und Überschreibungen. Diese Techniken werden als Teil von [Sling Resource Merger](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) und in [Überlagerungen](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/platform/overlays) beschrieben.

Um es sicherer und für die Kundschaft verständlicher zu machen, welche Bereiche von `/libs` sicher verwendet und überlagert werden können, wurde der Inhalt in `/libs` mit „Mixin“-Eigenschaften klassifiziert:

* Öffentlich
* Abstrakt
* Fertig
* Intern

Jede Klassifizierung beinhaltet Regeln darüber, wie der Inhalt verwendet, vererbt oder überlagert werden darf. Eine ausführliche Beschreibung finden Sie unter [Nachhaltige Aktualisierungen](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades).

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* Ein AEM-Upgrade kann zu Problemen beim Rendering von Seiten und anderen unerwünschten Verhaltensweisen führen.
* Sicherheits-Updates wirken sich nicht aus.

## Mögliche Lösungen {#solutions}

* Minimieren Sie die Verwendung von Inhaltsüberlagerungen auf die Fälle, in denen sie benötigt werden.
* Vermeiden Sie insbesondere das Überlagern von eingeschränkten Inhalten (Klassifizierungen „Final“ und „Intern“).
* Erwägen Sie die Anpassung von Änderungen aus `/libs` nach AEM-Aktualisierungen sowie Service Pack- oder Cumulative Fix Pack-Installationen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
