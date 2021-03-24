---
title: OCU
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# OCU {#ocu}

Veraltete Code-Verwendung

## Hintergrund {#background}

`OCU` identifiziert die Situation, in der einige JCR-Knoten, wie Sling- oder AEM-Komponenten oder API-OSGi-Exporte, auf eine nicht kompatible Weise geändert oder entfernt werden. Dem Kunden ist diese Änderung möglicherweise vor einem Upgrade nicht bekannt. Sie können auf eine nicht kompatible Version aktualisiert werden oder gar nicht verfügbar sein.

Da die alten Versionen nicht standardmäßig installiert sind, funktioniert die Kundenanwendung möglicherweise nicht ordnungsgemäß.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Funktionen, die von einer Komponente abhängen, die veraltete Komponenten oder APIs verwendet, können beschädigt werden und nach einer Aktualisierung möglicherweise nicht mehr richtig aufgelöst werden.
* Einige Funktionen der Kundenanwendung oder AEM Funktionen funktionieren möglicherweise nicht oder sind nach einem Upgrade möglicherweise nicht aktiv.

## Mögliche Lösungen {#solutions}

* Kurzfristig: Die Installation des Kompatibilitätspakets kann helfen.
* Langfristig: Passen Sie den Kundencode an, um die neueste Version AEM Komponenten oder APIs zu verwenden.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
