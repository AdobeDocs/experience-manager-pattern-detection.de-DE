---
title: IOI
description: Hilfeseite zum Mustererkennungs-Code
translation-type: ht
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: ht
source-wordcount: '152'
ht-degree: 100%

---


# IOI {#ioi}

Interner Oak-Import

## Hintergrund {#background}

`IOI` Steht für die Verwendung interner Oak-Packages durch den Kunden und den Import über OSGi. Sie werden normalerweise ohne eine bestimmte Version exportiert und sind nur für den Verbrauch durch andere Oak-Bundles oder AEM-Services auf untergeordnetem Niveau vorgesehen.

Einige davon werden von `com.adobe.granite.repository` verwendet, das während des Starts ein Repository für AEM einrichtet. Ein weiteres Beispiel ist das Adobe-Bundle `com.adobe.granite.maintenance.oak`, das Oak-Wartungsaufgaben umschließt und bereitstellt.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* In einer zukünftigen AEM-Version könnten interne Exporte entfernt werden, was zu unterbrochenen Abhängigkeiten und inaktiven Bundles führt, die direkt von Oak abhängen.
* Die API in internen Exporten kann sich ändern.

## Mögliche Lösungen {#solutions}

* Verwenden Sie die Sling Resource-API (oder die JCR-API) anstelle des Zugriffs auf untergeordnetem Niveau.
* Vermeiden Sie es, sich auf interne Packages zu verlassen, die nicht Teil einer öffentlichen API oder SPI sind.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.