---
title: NBCC
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# NBCC {#nbcc}

Nicht rückwärtskompatible Änderungen

## Hintergrund {#background}

`NBCC` identifiziert die Situation, in der einige JCR-Knoten oder -Bundles nicht kompatibel geändert werden. Dem Kunden ist diese Änderung möglicherweise vor einem Upgrade nicht bekannt.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Funktionalität, die von einer Komponente abhängt, die nicht abwärtskompatible Änderungen verwendet, kann beschädigt werden und kann möglicherweise nicht korrekt aufgelöst werden.
* Einige Funktionen der Kundenanwendung oder AEM Funktionen funktionieren nach einem Upgrade möglicherweise nicht ordnungsgemäß.

## Mögliche Lösungen {#solutions}

* Überlagern oder verweisen Sie nur auf abwärtskompatible Sling-Komponenten.
* Erwägen Sie die Anpassung von Ressourcen, die nach einer AEM Aktualisierung von `/libs` oder Bundles stammen.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
