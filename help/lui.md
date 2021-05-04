---
title: LUI
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
translation-type: tm+mt
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 68%

---

# LUI {#lui}

Alte Benutzeroberfläche

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Alte Benutzeroberfläche"
>abstract="LUI identifiziert die Verwendung veralteter Benutzeroberflächenelemente, die in späteren Versionen von AEM und in AEM nicht empfohlen oder nicht unterstützt werden."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de" text="Bemerkenswerte Änderungen - AEM als Cloud Service"

`LUI` steht für die Verwendung veralteter Benutzeroberflächenelemente, die in späteren Versionen von AEM und in AEM as a Cloud Service nicht empfohlen oder nicht unterstützt werden.

Um die verschiedenen Arten von Elementen der Benutzeroberfläche, die aktualisiert werden sollen oder müssen, zu unterscheiden, werden folgende Untertypen verwendet:

* `legacy.dialog.classic`: Dialoge aus der klassischen Benutzeroberfläche, die auf ExtJS basieren, müssen auf Coral umgestellt werden.
   * Dies wird erkannt, wenn der Name des Dialogs „dialog“ oder „design_dialog“ ist und wenn der Wert der Eigenschaft `jcr:primaryType` oder der Wert der Eigenschaft `xtype` „cq:Dialog“ lautet.
* `legacy.dialog.coral2`: Coral 2-Dialoge, die zur Verwendung von Coral 3 aktualisiert werden sollten.
   * Dies wird erkannt, wenn der Dialog und seine untergeordneten Inhaltsknotennamen „cq:dialog/content“,
„cq:design_dialog/content“, „cq:dialog.coral2/content“ oder „cq:design_dialog.coral2/content“ sind
und der Eigenschaftswert von `sling:resourceType` nicht
„granite/ui/components/coral/foundation“ enthält.
* `legacy.custom.component`: Komponenten, die von `foundation/components` erben, sollten aktualisiert werden, sodass sie Kernkomponenten verwenden.
   * Dies wird erkannt, wenn der Eigenschaftswert von `jcr:primaryType` „cq:Component“ und der
      Eigenschaftswert von `sling:resourceSuperType` „foundation/components“ enthält oder einer der
      Eigenschaftswerte von `sling:resourceSuperType` der Kette vom Übertyp „Komponenten“ „foundation/components“ enthält.
* `legacy.static.template`: Statische Vorlagen, die zu bearbeitbaren Vorlagen aktualisiert werden sollten.
   * Dies wird erkannt, wenn der Eigenschaftswert von `jcr:primaryType` „cq:Template“ lautet.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Durchführungsleitlinien"
>abstract="Die klassische Benutzeroberfläche ist in AEM als Cloud Service nicht mehr verfügbar und die Standard-Benutzeroberfläche für das Authoring ist die Touch-aktivierte Benutzeroberfläche. Best Practice ist, alle nicht unterstützten Schnittstellen zu verschieben und verknüpfte Anpassungen sollten auf neuere Funktionen/Funktionen umgestaltet werden, die mit AEM als Cloud Service kompatibel sind. Kunden können die vorhandene AEM Modernisierungssuite nutzen, um den für die Modernisierung der AEM Sites-Implementierungen erforderlichen Aufwand zu reduzieren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-Modernisierungs-Tools"

* Die klassische Benutzeroberfläche ist in AEM as a Cloud Service nicht mehr verfügbar. Die Standardoberfläche für das Authoring ist die Touch-optimierte Benutzeroberfläche.
* Die weitere Verwendung von veralteten, kundenspezifischen Komponenten kann die Wartungskosten mit der Zeit erhöhen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Tools und Ressourcen"
>abstract="Mithilfe der AEM Modernisierungssuite können Kunden Classic(ExtJS)-Dialoge in Coral-Dialoge konvertieren. Ziel ist es, Kunden dabei zu unterstützen, von den nicht unterstützten oder älteren Funktionen zu den robusten, modernen AEM zu wechseln. Diese Tools sind konfigurierbar, konfigurationsbewusst und erweiterbar. Darüber hinaus sollten Sie die Ersetzung benutzerdefinierter Komponenten durch den Satz standardisierter Kernkomponenten prüfen, um die Entwicklungszeit zu beschleunigen und die Wartungskosten Ihrer Anwendungen zu reduzieren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/component.html" text="Komponentenkonverter"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html" text="Kernkomponenten"

* Verwenden Sie die [AEM-Modernisierungs-Tool-Suite](https://opensource.adobe.com/aem-modernize-tools/), um den für die Modernisierung Ihrer AEM Sites-Implementierungen erforderlichen Aufwand zu reduzieren. Diese Tools umfassen die Konvertierung von:
   * Dialogen der klassischen Oberfläche (ExtJS) zu Coral-Dialogenn
   * Basiskomponenten zu Kernkomponenten
   * Statischen Vorlagen und Spaltensteuerung zu bearbeitbaren Vorlagen und responsivem Raster
   * Designs und Design-Dialogen zu Richtlinien für bearbeitbare Vorlagen
* Überprüfen Sie die Bibliothek der benutzerdefinierten Komponenten Ihres Projekts und wechseln Sie, wenn möglich, zum Satz der standardisierten [Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=de), um die Entwicklungszeit zu beschleunigen und die Wartungskosten für Ihre Programme zu reduzieren.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
