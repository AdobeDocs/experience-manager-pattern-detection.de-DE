---
title: LUI
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 4%

---


# LUI {#lui}

Alte Benutzeroberfläche

## Hintergrund {#background}

`LUI` identifiziert die Verwendung veralteter Benutzeroberflächenelemente, die in späteren Versionen von AEM und in AEM als Cloud Service nicht empfohlen oder nicht unterstützt werden.

Untertypen werden verwendet, um die verschiedenen Typen von Elementen der Benutzeroberfläche zu identifizieren, die aktualisiert werden sollten oder müssen:

* `legacy.dialog.classic`: Classic UI-Dialogfelder, die auf ExtJS basieren, müssen in Koral geändert werden.
   * Dies wird erkannt, wenn der Name des Dialogfelds &quot;dialog&quot;oder &quot;design_dialog&quot;lautet und wenn
der Wert der Eigenschaft `jcr:primaryType` oder der Wert der Eigenschaft `xtype` lautet &quot;cq:Dialog&quot;.
* `legacy.dialog.coral2`: Koral 2 Dialoge, sollten aktualisiert werden, um Coral 3 zu verwenden.
   * Dies wird erkannt, wenn der Dialog und die zugehörigen Node-Namen für den untergeordneten Inhalt &quot;cq:dialog/content&quot;sind.
&quot;cq:design_dialog/content&quot;, &quot;cq:dialog.coral2/content&quot;oder &quot;cq:design_dialog.coral2/content&quot;
und der `sling:resourceType`-Eigenschaftswert enthält nicht
&quot;granite/ui/components/coral/foundation&quot;.
* `legacy.custom.component`: Komponenten, die von  `foundation/components`übernehmen, sollten aktualisiert werden, um Kernkomponenten zu verwenden.
   * Dies wird erkannt, wenn der `jcr:primaryType`-Eigenschaftswert &quot;cq:Component&quot;und der Wert
      `sling:resourceSuperType` Eigenschaftswert enthält &quot;Stiftung/Komponenten&quot;oder eine der
      `sling:resourceSuperType` Eigenschaftswerte der Kette von Komponenten des Supertyps enthalten &quot;Stiftung/Komponenten&quot;.
* `legacy.static.template`: Statische Vorlagen sollten auf Bearbeitbare Vorlagen aktualisiert werden.
   * Dies wird erkannt, wenn der `jcr:primaryType`-Eigenschaftswert &quot;cq:Template&quot;lautet.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die klassische Benutzeroberfläche ist in AEM als Cloud Service nicht mehr verfügbar. Die Standard-Benutzeroberfläche für das Authoring ist die Touch-fähige Benutzeroberfläche.
* Die Nutzung älterer benutzerdefinierter Komponenten kann die Wartungskosten im Laufe der Zeit erhöhen.

## Mögliche Lösungen {#solutions}

* Verwenden Sie die [AEM Moderationstools-Suite](https://opensource.adobe.com/aem-modernize-tools/), um den für die Modernisierung Ihrer AEM Sites-Implementierungen erforderlichen Aufwand zu reduzieren. Diese Tools umfassen die Konvertierung von:
   * Classic-Dialoge (ExtJS) zu Coral-Dialogen
   * Foundation-Komponenten in Kernkomponenten
   * Statische Vorlagen und Spaltensteuerung für bearbeitbare Vorlagen und interaktives Raster
   * Entwürfe und Designdialoge zu Richtlinien für bearbeitbare Vorlagen
* Überprüfen Sie nach Möglichkeit die benutzerdefinierte Komponentenbibliothek und Transition Ihres Projekts auf den Satz standardisierter [Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=de), um die Entwicklungszeit zu beschleunigen und die Wartungskosten Ihrer Anwendungen zu reduzieren.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
