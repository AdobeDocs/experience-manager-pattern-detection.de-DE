---
title: IOI
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# IOI {#ioi}

Interner Oak-Import

## Hintergrund {#background}

`IOI` identifiziert die Verwendung interner Oak-Pakete durch den Kunden und importiert sie über OSGi. Sie werden in der Regel ohne eine bestimmte Version exportiert und sind nur für den Verbrauch durch andere Oak-Pakete oder Low-Level-AEM bestimmt.

Einige davon werden von `com.adobe.granite.repository` verwendet, das ein Repository für AEM während des Starts einrichtet. Ein weiteres Beispiel ist das `com.adobe.granite.maintenance.oak` Adobe Bundle, das Oak Maintenance Aufgaben umschließt und bereitstellt.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* In einer zukünftigen AEM können interne Exporte entfernt werden, was zu beschädigten Abhängigkeiten und inaktiven Bündeln führt, die direkt von Oak abhängen.
* Die API in internen Exporten kann sich ändern.

## Mögliche Lösungen {#solutions}

* Verwenden Sie die Sling Resource API (oder die JCR-API) anstelle des Zugriffs auf einfache Ebenen.
* Vermeiden Sie es, sich auf interne Pakete zu verlassen, die nicht Teil einer öffentlichen API oder SPI sind.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.