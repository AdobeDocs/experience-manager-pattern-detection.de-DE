---
title: LUI
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 49%

---

# LUI {#lui}

Alte Benutzeroberfläche

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Alte Benutzeroberfläche"
>abstract="LUI identifiziert die Verwendung veralteter Elemente der Benutzeroberfläche. Diese Elemente werden in späteren Versionen von AEM und in AEM as a Cloud Service nicht empfohlen oder nicht unterstützt."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Wesentliche Änderungen – AEM as a Cloud Service"

`LUI`  Gibt die Verwendung veralteter Elemente der Benutzeroberfläche an. Diese Elemente werden in späteren Versionen von AEM und in AEM as a Cloud Service nicht empfohlen oder nicht unterstützt.

Um die verschiedenen Arten von Elementen der Benutzeroberfläche zu unterscheiden, die aktualisiert werden sollen oder müssen, werden folgende Untertypen verwendet:

* `legacy.dialog.classic`: Die auf ExtJS basierenden Dialogfelder der klassischen Benutzeroberfläche müssen in Coral geändert werden.
   * Dieser Untertyp wird erkannt, wenn der Name des Dialogfelds `dialog` oder `design_dialog` und wenn die `jcr:primaryType` -Eigenschaftswert oder `xtype` Eigenschaftswert ist `cq:Dialog`.
* `legacy.dialog.coral2`: `Coral 2`-Dialogfelder sollten aktualisiert werden, damit sie `Coral 3` benutzen.
   * Dieser Untertyp wird erkannt, wenn das Dialogfeld und die Namen der untergeordneten Inhaltsknoten
      * `cq:dialog/content`,
      * `cq:design_dialog/content`,
      * `cq:dialog.coral2/content`,
      * oder `cq:design_dialog.coral2/content`
und `sling:resourceType` Eigenschaftswert enthält nicht `granite/ui/components/coral/foundation`.
* `legacy.custom.component`: Komponenten, die von `foundation/components` erben, sollten auf die Verwendung von Kernkomponenten aktualisiert werden.
   * Dieser Untertyp wird erkannt, wenn die `jcr:primaryType` Eigenschaftswert ist `cq:Component` und
     `sling:resourceSuperType` Eigenschaftswert enthält &quot;foundation/components&quot;. Oder wenn einer der
     `sling:resourceSuperType` Eigenschaftswerte der Kette von Komponenten des Supertyps enthalten &quot;foundation/components&quot;.
* `legacy.static.template`: Statische Vorlagen sollten in bearbeitbare Vorlagen aktualisiert werden.
   * Dieser Untertyp wird erkannt, wenn die `jcr:primaryType` Eigenschaftswert ist `cq:Template`.
* `content.fragment.template`: Inhaltsfragmentvorlagen sollten Fragmentmodelle erstellen, die die Fragmentvorlagen ersetzen.
   * Inhaltsfragmentvorlagen befinden sich in den folgenden Speicherorten:
      * Vorkonfigurierte Inhaltsfragmentvorlagen werden in `/libs/settings/dam/cfm/templates` gespeichert.
      * Sie können in `/apps/settings/dam/cfm/templates` oder `/conf/.../settings/dam/cfm/templates`(... = global oder „tenant“) überlagert werden.
* `translation.dictionary`: `I18n` Wörterbuch, das unter `/apps`.
   * `/apps` ist zur Laufzeit unveränderlich und translator.html wäre in AEM as a Cloud Service nicht mehr verfügbar.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Implementierungsleitlinien"
>abstract="Die klassische Benutzeroberfläche ist in AEM as a Cloud Service nicht mehr verfügbar und die Standardoberfläche für das Authoring ist die Touch-fähige Benutzeroberfläche. Best Practice ist, alle nicht unterstützten Schnittstellen und verknüpften Anpassungen auf neuere Funktionen und Funktionen zu verschieben, die mit AEM as a Cloud Service kompatibel sind. Kundinnen und Kunden können die bestehende AEM-Modernisierungs-Suite nutzen, um den Aufwand für die Modernisierung der AEM Sites-Implementierungen zu reduzieren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-Modernisierungs-Tools"

* Die klassische Benutzeroberfläche ist in AEM as a Cloud Service nicht mehr verfügbar. Die Standardoberfläche für das Authoring ist die Touch-optimierte Benutzeroberfläche.
* Die weitere Verwendung von veralteten, kundenspezifischen Komponenten kann die Wartungskosten mit der Zeit erhöhen.
* Inhaltsfragmentvorlagen ersetzten Inhaltsfragmentmodelle in AEM 6.3. Bei der Migration von Inhaltsfragmenten, die auf älteren Vorlagen basieren, AEM as a Cloud Service werden diese Fragmente als funktionsfähig beibehalten. Es ist jedoch nicht möglich, Fragmente basierend auf der alten Vorlage zu erstellen. Es ist auch nicht möglich, diese Fragmente mit AEM GraphQL bereitzustellen, was Inhaltsfragmentmodelle als Schemata erfordert.
* „/apps“ ist zur Laufzeit unveränderlich und „translator.html“ wäre in AEM as a Cloud Service nicht mehr verfügbar. Daher `I18n` Die Wörterbücher müssen von Git über die CI/CD-Pipeline stammen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Tools und Ressourcen"
>abstract="Mithilfe der AEM Modernization Suite können Kunden Classic(ExtJS)-Dialoge in Coral-Dialoge konvertieren. Dies soll Kunden dabei helfen, von den nicht unterstützten oder veralteten Funktionen zu den robusten, modernen AEM-Angeboten zu wechseln. Diese Tools sind konfigurierbar, konfigurationsabhängig und erweiterbar. Probieren Sie auch den Ersatz von benutzerdefinierten Komponenten durch den Satz standardisierter Kernkomponenten aus, um die Entwicklungszeit zu beschleunigen und die Wartungskosten Ihrer Programme zu reduzieren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Komponentenkonvertierer"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-core-components/using/introduction" text="Kernkomponenten"

* Um den für die Modernisierung Ihrer AEM Sites-Implementierungen erforderlichen Aufwand zu reduzieren, verwenden Sie die [AEM Modernisierungs-Tools-Suite](https://opensource.adobe.com/aem-modernize-tools/). Diese Tools umfassen die Konvertierung von:
   * Dialogen der klassischen Oberfläche (ExtJS) zu Coral-Dialogenn
   * Basiskomponenten zu Kernkomponenten
   * Statische Vorlagen und Spaltensteuerung für bearbeitbare Vorlagen und responsives Raster
   * Entwürfe und Designdialogfelder für Richtlinien für bearbeitbare Vorlagen
* Überprüfen Sie die Bibliothek der benutzerdefinierten Komponenten Ihres Projekts und wechseln Sie, wenn möglich, zum Satz der standardisierten [Kernkomponenten](https://experienceleague.adobe.com/de/docs/experience-manager-core-components/using/introduction), um die Entwicklungszeit zu beschleunigen und die Wartungskosten für Ihre Programme zu reduzieren.
* Erstellen Sie Inhaltsfragmentmodelle mit entsprechenden Funktionen für die älteren Vorlagen und verwenden Sie diese Modelle für die zukünftige Erstellung von Inhaltsfragmenten. Weitere Informationen finden Sie unter [Inhaltsfragmentmodelle](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models).
* `I18n` Die Wörterbücher müssen über die CI/CD-Pipeline von Git stammen. [Dokumentation](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
