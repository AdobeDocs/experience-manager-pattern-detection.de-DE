---
title: CDW
description: Hilfeseite zum Mustererkennungs-Code
exl-id: a9e9dae8-0aa2-4679-a3c1-418cab01cfda
source-git-commit: d12f2613493d9bf379464d9c089ad376532c4de2
workflow-type: ht
source-wordcount: '185'
ht-degree: 100%

---

# CDW {#cdw}

Benutzerdefiniertes Dialog-Widget

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="Benutzerdefiniertes Dialog-Widget"
>abstract="CDW identifiziert die benutzerdefinierten Dialog-Widgets, die aktualisiert werden sollten, damit sie mit AEM as a Cloud Service kompatibel sind."

`CDW` Benutzerdefinierte Dialog-Widgets identifizieren die benutzerdefinierten CoralUI- und klassischen Dialog-Widgets. Diese sollten aktualisiert werden, damit sie mit AEM as a Cloud Service kompatibel sind.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden unter anderem folgende Untertypen verwendet:

* `custom.coral.widget`: Identifizieren Sie die benutzerdefinierten Dialog-Widgets basierend auf CoralUI 2 oder CoralUI 3.
* `custom.classic.widget`: Identifizieren Sie die benutzerdefinierten Dialog-Widgets basierend auf ExtJs.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die klassische Benutzeroberfläche ist in AEM as a Cloud Service nicht mehr verfügbar. Die Standardoberfläche für das Authoring ist die Touch-optimierte Benutzeroberfläche.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="Implementierungsleitlinien"
>abstract="Wenden Sie sich für Hilfe an die Kundenunterstützung."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Benutzerdefinierte klassische Dialog-Widgets sollten von ExtJS in [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html) konvertiert werden.
* Benutzerdefinierte Coral-Dialog-Widgets sollten bezüglich einer Aktualisierung auf CoralUI 3 ausgewertet werden.
* Wenden Sie sich an unser [Experience Manager-Support-Team](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder Probleme zu besprechen.
