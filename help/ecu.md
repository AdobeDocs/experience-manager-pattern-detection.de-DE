---
title: ECU
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---


# ECU {#ecu}

VERALTET: Verwendung fremder Inhalte (ersetzt durch CAV, Inhaltsbereichsverletzung)

## Hintergrund {#background}

`ECU` identifiziert das Muster, bei dem verschiedene Inhaltsbereiche in einer Weise verwendet werden, die gegen die Regeln der Inhaltsklassifizierung verstößt.

Die Verarbeitung von Sling-Anforderungen definiert, wie der Inhalt einer Ressource, insbesondere deren `sling:resourceType`-Eigenschaft, zur Bestimmung des Skripts verwendet wird, das zum Rendern des Inhalts verwendet wird. (Weitere Informationen finden Sie unter [Suchen des Skripts](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script).) Sling bietet außerdem Techniken zum Zugriff und Zusammenführen von Ressourcen über &quot;Overlays&quot;und &quot;Overrides&quot;. Diese werden als Teil des [Sling Resource Merger](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html) und in [Overlays](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html) beschrieben.

Damit es für Kunden sicherer und einfacher ist zu verstehen, welche Bereiche von `/libs` sicher zu verwenden sind und die Überlagerung des Inhalts in `/libs` wurde mit &quot;mixin&quot;-Eigenschaften klassifiziert: Öffentlich, abstrakt, endgültig und intern. Jede Klassifizierung beinhaltet Regeln darüber, wie der Inhalt vom Benutzer geerbt oder überlagert werden kann. Eine ausführliche Beschreibung finden Sie unter [Nachhaltige Upgrades](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html).

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Ein AEM Upgrade kann zu Problemen beim Seitenrendern und anderen unerwünschten Verhaltensweisen führen.
* Sicherheitsaktualisierungen sind nicht wirksam.

## Mögliche Lösungen {#solutions}

* Minimieren Sie die Verwendung von Inhaltsüberlagerungen auf die Fälle, in denen sie benötigt werden.
* Vermeiden Sie insbesondere das Überlagern von eingeschränkten Inhalten (endgültige und interne Klassifizierung).
* Erwägen Sie die Anpassung von Änderungen, die von `/libs` nach AEM Aktualisierungen, ServicePack- oder CumulativeFixPack-Installationen kommen.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
