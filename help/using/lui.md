---
title: LUI
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 100%

---

# LUI {#lui}

Alte Benutzeroberfläche

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Alte Benutzeroberfläche"
>abstract="LUI identifiziert die Verwendung veralteter Elemente der Benutzeroberfläche. Die Verwendung dieser Elemente wird in späteren Versionen von AEM und in AEM as a Cloud Service nicht empfohlen oder nicht unterstützt."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Wesentliche Änderungen – AEM as a Cloud Service"

`LUI` identifiziert die Verwendung veralteter Elemente der Benutzeroberfläche. Die Verwendung dieser Elemente wird in späteren Versionen von AEM und in AEM as a Cloud Service nicht empfohlen oder nicht unterstützt.

Um die verschiedenen Arten von Elementen der Benutzeroberfläche zu unterscheiden, die aktualisiert werden sollen oder müssen, werden folgende Untertypen verwendet:

* `legacy.dialog.classic`: Dialogfelder aus der klassischen Benutzeroberfläche, die auf ExtJS basieren, müssen auf Coral umgestellt werden.
   * Dieser Untertyp wird erkannt, wenn der Name des Dialogfelds `dialog` oder `design_dialog` ist und wenn
die Eigenschaft `jcr:primaryType` oder die Eigenschaft `xtype` den Wert `cq:Dialog` aufweist.
* `legacy.dialog.coral2`: `Coral 2`-Dialogfelder sollten aktualisiert werden, damit sie `Coral 3` benutzen.
   * Dieser Untertyp wird erkannt, wenn der Name des Dialogfelds und die Namen der untergeordneten Inhaltsknoten
      * `cq:dialog/content`,
      * `cq:design_dialog/content`,
      * `cq:dialog.coral2/content`,
      * oder `cq:design_dialog.coral2/content`
sind und der Wert der Eigenschaft `sling:resourceType` nicht `granite/ui/components/coral/foundation` enthält.
* `legacy.custom.component`: Komponenten, die von `foundation/components` erben, sollten auf die Verwendung von Kernkomponenten aktualisiert werden.
   * Dieser Untertyp wird erkannt, wenn die Eigenschaft `jcr:primaryType` den Wert `cq:Component` aufweist und
     die Eigenschaft `sling:resourceSuperType` den Wert „foundation/components“ enthält. Oder wenn einer der
     Eigenschaftswerte von `sling:resourceSuperType` der Kette vom Supertyp „Komponenten“
„foundation/components“ enthält.
* `legacy.static.template`: Statische Vorlagen sollten in bearbeitbare Vorlagen aktualisiert werden.
   * Dieser Supertyp wird erkannt, wenn die Eigenschaft `jcr:primaryType` den Wert `cq:Template` aufweist.
* `content.fragment.template`: Inhaltsfragmentvorlagen sollten Fragmentmodelle erstellen, um die Fragmentvorlagen zu ersetzen.
   * Inhaltsfragmentvorlagen befinden sich in den folgenden Speicherorten:
      * Vorkonfigurierte Inhaltsfragmentvorlagen werden in `/libs/settings/dam/cfm/templates` gespeichert.
      * Sie können in `/apps/settings/dam/cfm/templates` oder `/conf/.../settings/dam/cfm/templates`(... = global oder „tenant“) überlagert werden.
* `translation.dictionary`: `I18n`-Wörterbuch, das unter `/apps` vorhanden ist.
   * `/apps` ist zur Laufzeit unveränderlich und „translator.html“ wäre in AEM as a Cloud Service nicht mehr verfügbar.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Implementierungsleitlinien"
>abstract="Die klassische Benutzeroberfläche ist in AEM as a Cloud Service nicht mehr verfügbar und die Standardoberfläche für das Authoring ist die Touch-fähige Benutzeroberfläche. Best Practice ist es, alle nicht unterstützten Oberflächen zu verschieben. Verknüpfte Anpassungen sollten auf neuere Funktionen und Funktionalitäten umgearbeitet werden, die mit AEM as a Cloud Service kompatibel sind. Kundinnen und Kunden können die bestehende AEM-Modernisierungs-Suite nutzen, um den Aufwand für die Modernisierung der AEM Sites-Implementierungen zu reduzieren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-Modernisierungs-Tools"

* Die klassische Benutzeroberfläche ist in AEM as a Cloud Service nicht mehr verfügbar. Die Standardoberfläche für das Authoring ist die Touch-optimierte Benutzeroberfläche.
* Die weitere Verwendung von veralteten, kundenspezifischen Komponenten kann die Wartungskosten mit der Zeit erhöhen.
* Inhaltsfragmentvorlagen wurden in AEM 6.3 durch Inhaltsfragmentmodelle abgelöst. Bei der Migration von Inhaltsfragmenten, die auf veralteten Vorlagen basieren, in AEM as a Cloud Service bleiben diese Fragmente funktionsfähig. Es ist jedoch nicht möglich, neue Fragmente auf der Basis der veralteten Vorlage zu erstellen. Es ist auch nicht möglich, diese Fragmente mit AEM GraphQL bereitzustellen, da dies Inhaltsfragmentmodelle als Schemata erfordert.
* „/apps“ ist zur Laufzeit unveränderlich und „translator.html“ wäre in AEM as a Cloud Service nicht mehr verfügbar. Daher müssen `I18n`-Wörterbücher unter Verwendung der CI/CD-Pipeline aus Git stammen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Tools und Ressourcen"
>abstract="Mithilfe der AEM Modernization Suite können Kunden Classic(ExtJS)-Dialoge in Coral-Dialoge konvertieren. Dies soll Kunden dabei helfen, von den nicht unterstützten oder veralteten Funktionen zu den robusten, modernen AEM-Angeboten zu wechseln. Diese Tools sind konfigurierbar, konfigurationsabhängig und erweiterbar. Probieren Sie auch den Ersatz von benutzerdefinierten Komponenten durch den Satz standardisierter Kernkomponenten aus, um die Entwicklungszeit zu beschleunigen und die Wartungskosten Ihrer Programme zu reduzieren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Komponentenkonvertierer"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-core-components/using/introduction" text="Kernkomponenten"

* Um den für die Modernisierung Ihrer AEM Sites-Implementierungen erforderlichen Aufwand zu reduzieren, verwenden Sie die [Suite an AEM-Modernisierungs-Tools](https://opensource.adobe.com/aem-modernize-tools/). Diese Tools umfassen die Konvertierung von:
   * Dialogen der klassischen Oberfläche (ExtJS) zu Coral-Dialogenn
   * Basiskomponenten zu Kernkomponenten
   * statischen Vorlagen und Spaltensteuerung zu bearbeitbaren Vorlagen und responsivem Raster
   * Designs und Design-Dialogfeldern zu Richtlinien für bearbeitbare Vorlagen
* Überprüfen Sie die Bibliothek der benutzerdefinierten Komponenten Ihres Projekts und wechseln Sie, wenn möglich, zum Satz der standardisierten [Kernkomponenten](https://experienceleague.adobe.com/de/docs/experience-manager-core-components/using/introduction), um die Entwicklungszeit zu beschleunigen und die Wartungskosten für Ihre Programme zu reduzieren.
* Erstellen Sie Inhaltsfragmentmodelle mit entsprechenden Funktionen für die älteren Vorlagen und verwenden Sie diese Modelle für die zukünftige Erstellung von Inhaltsfragmenten. Weitere Informationen finden Sie unter [Inhaltsfragmentmodelle](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models).
* `I18n`-Wörterbücher müssen unter Verwendung der CI/CD-Pipeline aus Git stammen. [Dokumentation](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
