---
title: LUI
description: Mustererkennungscode Hilfeseite.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 58%

---

# LUI {#lui}

Alte Benutzeroberfläche

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Alte Benutzeroberfläche"
>abstract="LUI kennzeichnet die Verwendung veralteter Benutzeroberflächenelemente, die in späteren Versionen von AEM und in AEM as a Cloud Service nicht empfohlen oder nicht unterstützt werden."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Wesentliche Änderungen – AEM as a Cloud Service"

LUI kennzeichnet die Verwendung veralteter Benutzeroberflächenelemente, die in späteren Versionen von AEM und in AEM as a Cloud Service nicht empfohlen oder nicht unterstützt werden.

Um die verschiedenen Arten von Elementen der Benutzeroberfläche, die aktualisiert werden sollen oder müssen, zu unterscheiden, werden folgende Untertypen verwendet:

* `legacy.dialog.classic`: Dialoge aus der klassischen Benutzeroberfläche, die auf ExtJS basieren, müssen auf Coral umgestellt werden.
   * Dies wird erkannt, wenn der Dialogfeldname &quot;dialog&quot;oder &quot;design_dialog&quot;lautet und wenn die `jcr:primaryType` -Eigenschaftswert oder `xtype` Eigenschaftswert ist `cq:Dialog`.
* `legacy.dialog.coral2`: `Coral 2` -Dialogfelder sollten aktualisiert werden, um `Coral 3`.
   * Dies wird erkannt, wenn das Dialogfeld und die Namen der untergeordneten Inhaltsknoten `cq:dialog/content`,
     `cq:design_dialog/content`, `cq:dialog.coral2/content`&quot;, oder `cq:design_dialog.coral2/content`
und `sling:resourceType` Der Eigenschaftswert enthält nicht &quot;granite/ui/components/coral/foundation&quot;.
* `legacy.custom.component`: Komponenten, die von `foundation/components` erben, sollten auf die Verwendung von Kernkomponenten aktualisiert werden.
   * Dies wird erkannt, wenn die `jcr:primaryType` property value is &quot;`cq:Component`&quot; und
     `sling:resourceSuperType` Eigenschaftswert enthält &quot;foundation/components&quot;. Oder: die
     Eigenschaftswerte von `sling:resourceSuperType` der Kette vom Übertyp „Komponenten“ „foundation/components“ enthält.
* `legacy.static.template`: Statische Vorlagen sollten in bearbeitbare Vorlagen aktualisiert werden.
   * Dies wird erkannt, wenn die `jcr:primaryType` property value is &quot;`cq:Template`&quot;.
* `content.fragment.template`: Inhaltsfragmentvorlagen sollten Fragmentmodelle erstellen, um die Fragmentvorlagen zu ersetzen.
   * Inhaltsfragmentvorlagen befinden sich in den folgenden Speicherorten:
      * Vorkonfigurierte Inhaltsfragmentvorlagen werden in `/libs/settings/dam/cfm/templates` gespeichert.
      * Sie können in `/apps/settings/dam/cfm/templates` oder `/conf/.../settings/dam/cfm/templates`(... = global oder „tenant“) überlagert werden.
* `translation.dictionary`: `I18n` Wörterbuch, das unter /apps vorhanden ist.
   * „/apps“ ist zur Laufzeit unveränderlich und „translator.html“ wäre in AEM as a Cloud Service nicht mehr verfügbar.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Implementierungsleitlinien"
>abstract="Die klassische Benutzeroberfläche ist in AEM as a Cloud Service nicht mehr verfügbar und die Standardoberfläche für das Authoring ist die Touch-fähige Benutzeroberfläche. Best Practice ist, alle nicht unterstützten Schnittstellen und verknüpften Anpassungen auf neuere Funktionen/Funktionen zu verschieben, die mit AEM as a Cloud Service kompatibel sind. Kunden können die vorhandene AEM Modernization Suite verwenden, um den für die Modernisierung der AEM Sites-Implementierungen erforderlichen Aufwand zu reduzieren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-Modernisierungs-Tools"

* Die klassische Benutzeroberfläche ist in AEM as a Cloud Service nicht mehr verfügbar. Die Standardoberfläche für das Authoring ist die Touch-optimierte Benutzeroberfläche.
* Die weitere Verwendung von veralteten, kundenspezifischen Komponenten kann die Wartungskosten mit der Zeit erhöhen.
* Inhaltsfragmentvorlagen wurden in AEM 6.3 durch Inhaltsfragmentmodelle ersetzt. Beim Migrieren von Inhaltsfragmenten, die auf älteren Vorlagen basieren, AEM as a Cloud Service behalten Sie diese Fragmente als funktionsfähig bei, aber es ist nicht möglich, Fragmente basierend auf der alten Vorlage zu erstellen. Es ist auch nicht möglich, diese Fragmente mit AEM GraphQL bereitzustellen, für die Inhaltsfragmentmodelle als Schemata erforderlich sind.
* „/apps“ ist zur Laufzeit unveränderlich und „translator.html“ wäre in AEM as a Cloud Service nicht mehr verfügbar. Daher `I18n` -Wörterbücher müssen über die CI/CD-Pipeline von Git stammen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Tools und Ressourcen"
>abstract="Mithilfe der AEM Modernization Suite können Kunden Classic(ExtJS)-Dialoge in Coral-Dialoge konvertieren. Dies soll Kunden dabei helfen, von den nicht unterstützten oder veralteten Funktionen zu den robusten, modernen AEM-Angeboten zu wechseln. Diese Tools sind konfigurierbar, konfigurationsabhängig und erweiterbar. Probieren Sie auch den Ersatz von benutzerdefinierten Komponenten durch den Satz standardisierter Kernkomponenten aus, um die Entwicklungszeit zu beschleunigen und die Wartungskosten Ihrer Programme zu reduzieren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Komponentenkonvertierer"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-core-components/using/introduction" text="Kernkomponenten"

* Um den für die Modernisierung Ihrer AEM Sites-Implementierungen erforderlichen Aufwand zu reduzieren, verwenden Sie [AEM Modernisierungs-Tools-Suite](https://opensource.adobe.com/aem-modernize-tools/). Diese Tools umfassen die Konvertierung von:
   * Dialogen der klassischen Oberfläche (ExtJS) zu Coral-Dialogenn
   * Basiskomponenten zu Kernkomponenten
   * Statischen Vorlagen und Spaltensteuerung zu bearbeitbaren Vorlagen und responsivem Raster
   * Designs und Design-Dialogen zu Richtlinien für bearbeitbare Vorlagen
* Überprüfen Sie die Bibliothek der benutzerdefinierten Komponenten Ihres Projekts und wechseln Sie, wenn möglich, zum Satz der standardisierten [Kernkomponenten](https://experienceleague.adobe.com/de/docs/experience-manager-core-components/using/introduction), um die Entwicklungszeit zu beschleunigen und die Wartungskosten für Ihre Programme zu reduzieren.
* Erstellen Sie Inhaltsfragmentmodelle mit entsprechenden Funktionen für die älteren Vorlagen und verwenden Sie diese Modelle für die zukünftige Erstellung von Inhaltsfragmenten. Siehe [Inhaltsfragmentmodelle](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models) für weitere Details.
* `I18n` -Wörterbücher müssen über die CI/CD-Pipeline von Git stammen. [Dokumentation](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
