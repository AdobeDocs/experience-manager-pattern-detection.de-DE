---
title: LUI
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 1553f13b8d6b92363a80298b4d05bd885c6f3a6a
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 100%

---

# LUI {#lui}

Alte Benutzeroberfläche

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Alte Benutzeroberfläche"
>abstract="LUI kennzeichnet die Verwendung veralteter Benutzeroberflächenelemente, die in späteren Versionen von AEM und in AEM as a Cloud Service nicht empfohlen oder nicht unterstützt werden."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de" text="Wesentliche Änderungen – AEM as a Cloud Service"

`LUI` kennzeichnet die Verwendung veralteter Benutzeroberflächenelemente, die in späteren Versionen von AEM und in AEM as a Cloud Service nicht empfohlen oder nicht unterstützt werden.

Um die verschiedenen Arten von Elementen der Benutzeroberfläche, die aktualisiert werden sollen oder müssen, zu unterscheiden, werden folgende Untertypen verwendet:

* `legacy.dialog.classic`: Dialoge aus der klassischen Benutzeroberfläche, die auf ExtJS basieren, müssen auf Coral umgestellt werden.
   * Dies wird erkannt, wenn der Name des Dialogs „dialog“ oder „design_dialog“ ist und wenn der Wert der Eigenschaft `jcr:primaryType` oder der Wert der Eigenschaft `xtype` „cq:Dialog“ lautet.
* `legacy.dialog.coral2`: Coral 2-Dialoge sollten auf die Verwendung von Coral 3 aktualisiert werden.
   * Dies wird erkannt, wenn der Name des Dialogs bzw. seiner untergeordneten Inhaltsknoten „cq:dialog/content“,
„cq:design_dialog/content“, „cq:dialog.coral2/content“ oder „cq:design_dialog.coral2/content“ lautet
und der Eigenschaftswert von `sling:resourceType` nicht
„granite/ui/components/coral/foundation“ enthält.
* `legacy.custom.component`: Komponenten, die von `foundation/components` erben, sollten auf die Verwendung von Kernkomponenten aktualisiert werden.
   * Dies wird erkannt, wenn der Eigenschaftswert von `jcr:primaryType` „cq:Component“ und der
      Eigenschaftswert von `sling:resourceSuperType` „foundation/components“ enthält oder einer der
      Eigenschaftswerte von `sling:resourceSuperType` der Kette vom Übertyp „Komponenten“ „foundation/components“ enthält.
* `legacy.static.template`: Statische Vorlagen sollten in bearbeitbare Vorlagen aktualisiert werden.
   * Dies wird erkannt, wenn der Eigenschaftswert von `jcr:primaryType` „cq:Template“ lautet.
* `content.fragment.template`: Inhaltsfragmentvorlagen sollten Fragmentmodelle erstellen, um die Fragmentvorlagen zu ersetzen.
   * Inhaltsfragmentvorlagen befinden sich in den folgenden Speicherorten:
      * Vorkonfigurierte Inhaltsfragmentvorlagen werden in `/libs/settings/dam/cfm/templates` gespeichert.
      * Sie können in `/apps/settings/dam/cfm/templates` oder `/conf/.../settings/dam/cfm/templates`(... = global oder „tenant“) überlagert werden.
* `translation.dictionary`: I18n-Wörterbuch, das unter „/apps“ vorhanden ist.
   * „/apps“ ist zur Laufzeit unveränderlich und „translator.html“ wäre in AEM as a Cloud Service nicht mehr verfügbar.

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Implementierungsleitlinien"
>abstract="Die klassische Benutzeroberfläche ist in AEM as a Cloud Service nicht mehr verfügbar und die Standardoberfläche für das Authoring ist die Touch-fähige Benutzeroberfläche. Best Practice ist es, alle nicht unterstützten Oberflächen zu verschieben. Verknüpfte Anpassungen sollten auf neuere Funktionen/Funktionalitäten umgearbeitet werden, die mit AEM as a Cloud Service kompatibel sind. Kunden können die bestehende AEM Modernization Suite nutzen, um den Aufwand für die Modernisierung der AEM Sites-Implementierungen zu reduzieren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-Modernisierungs-Tools"

* Die klassische Benutzeroberfläche ist in AEM as a Cloud Service nicht mehr verfügbar. Die Standardoberfläche für das Authoring ist die Touch-optimierte Benutzeroberfläche.
* Die weitere Verwendung von veralteten, kundenspezifischen Komponenten kann die Wartungskosten mit der Zeit erhöhen.
* Inhaltsfragmentvorlagen wurden in AEM 6.3 durch Inhaltsfragmentmodelle abgelöst. Bei der Migration von Inhaltsfragmenten, die auf veralteten Vorlagen zu AEM as a Cloud Service basieren, werden diese Fragmente als funktional beibehalten. Es ist aber nicht möglich, neue Fragmente auf der Basis der veralteten Vorlage zu erstellen. Es ist auch nicht möglich, diese Fragmente mit AEM GraphQL bereitzustellen, was Inhaltsfragmentmodelle als Schemas erfordert.
* „/apps“ ist zur Laufzeit unveränderlich und „translator.html“ wäre in AEM as a Cloud Service nicht mehr verfügbar. I18n-Wörterbücher müssen folglich von Git über die CI/CD-Pipeline kommen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Tools und Ressourcen"
>abstract="Mithilfe der AEM Modernization Suite können Kunden Classic(ExtJS)-Dialoge in Coral-Dialoge konvertieren. Dies soll Kunden dabei helfen, von den nicht unterstützten oder veralteten Funktionen zu den robusten, modernen AEM-Angeboten zu wechseln. Diese Tools sind konfigurierbar, konfigurationssensitiv und erweiterbar. Probieren Sie auch den Ersatz von benutzerdefinierten Komponenten durch den Satz standardisierter Kernkomponenten aus, um die Entwicklungszeit zu beschleunigen und die Wartungskosten Ihrer Programme zu reduzieren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Komponentenkonvertierer"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=de" text="Kernkomponenten"

* Verwenden Sie die [AEM-Modernisierungs-Tool-Suite](https://opensource.adobe.com/aem-modernize-tools/), um den für die Modernisierung Ihrer AEM Sites-Implementierungen erforderlichen Aufwand zu reduzieren. Diese Tools umfassen die Konvertierung von:
   * Dialogen der klassischen Oberfläche (ExtJS) zu Coral-Dialogenn
   * Basiskomponenten zu Kernkomponenten
   * Statischen Vorlagen und Spaltensteuerung zu bearbeitbaren Vorlagen und responsivem Raster
   * Designs und Design-Dialogen zu Richtlinien für bearbeitbare Vorlagen
* Überprüfen Sie die Bibliothek der benutzerdefinierten Komponenten Ihres Projekts und wechseln Sie, wenn möglich, zum Satz der standardisierten [Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=de), um die Entwicklungszeit zu beschleunigen und die Wartungskosten für Ihre Programme zu reduzieren.
* Es wird empfohlen, Inhaltsfragmentmodelle mit den gleichen Funktionen wie die veralteten Vorlagen zu erstellen und diese künftig für die Erstellung von Inhaltsfragmenten zu verwenden. Weitere Einzelheiten finden Sie unter [Inhaltsfragmentmodelle](https://experienceleague.adobe.com/docs/experience-manager-65/assets/content-fragments/content-fragments-models.html?lang=de).
* I18n-Wörterbücher müssen von Git über die CI/CD-Pipeline kommen. [Dokumentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes.html?lang=de#apps-libs-immutable).
* Wenden Sie sich an unser [AEM-Support-Team](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
