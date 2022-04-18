---
title: LUI
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 1dbb239f23986f11c0dd6bfa883d8ab9124c0b52
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 73%

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

* `legacy.dialog.classic`: Die auf ExtJS basierenden Dialogfelder der klassischen Benutzeroberfläche müssen in Coral geändert werden.
   * Dies wird erkannt, wenn der Name des Dialogs „dialog“ oder „design_dialog“ ist und wenn der Wert der Eigenschaft `jcr:primaryType` oder der Wert der Eigenschaft `xtype` „cq:Dialog“ lautet.
* `legacy.dialog.coral2`: Coral 2-Dialogfelder sollten für die Verwendung von Coral 3 aktualisiert werden.
   * Dies wird erkannt, wenn der Dialog und seine untergeordneten Inhaltsknotennamen „cq:dialog/content“,
„cq:design_dialog/content“, „cq:dialog.coral2/content“ oder „cq:design_dialog.coral2/content“ sind
und der Eigenschaftswert von `sling:resourceType` nicht
„granite/ui/components/coral/foundation“ enthält.
* `legacy.custom.component`: Komponenten, die von erben `foundation/components` sollte aktualisiert werden, um Kernkomponenten zu verwenden.
   * Dies wird erkannt, wenn der Eigenschaftswert von `jcr:primaryType` „cq:Component“ und der
      Eigenschaftswert von `sling:resourceSuperType` „foundation/components“ enthält oder einer der
      Eigenschaftswerte von `sling:resourceSuperType` der Kette vom Übertyp „Komponenten“ „foundation/components“ enthält.
* `legacy.static.template`: Statische Vorlagen sollten auf bearbeitbare Vorlagen aktualisiert werden.
   * Dies wird erkannt, wenn der Eigenschaftswert von `jcr:primaryType` „cq:Template“ lautet.
* `content.fragment.template`: Inhaltsfragmentvorlagen sollten Fragmentmodelle erstellen, um die Fragmentvorlagen zu ersetzen.
   * Inhaltsfragmentvorlagen finden Sie in den folgenden Verzeichnissen:
      * Vordefinierte Inhaltsfragmentvorlagen werden in `/libs/settings/dam/cfm/templates`
      * Sie können in  `/apps/settings/dam/cfm/templates`  oder  `/conf/.../settings/dam/cfm/templates`(... = global oder &quot;tenant&quot;)

## Mögliche Implikationen und Risiken {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Implementierungsleitlinien"
>abstract="Die klassische Benutzeroberfläche ist in AEM as a Cloud Service nicht mehr verfügbar und die Standardoberfläche für das Authoring ist die Touch-fähige Benutzeroberfläche. Best Practice ist es, alle nicht unterstützten Oberflächen zu verschieben. Verknüpfte Anpassungen sollten auf neuere Funktionen/Funktionalitäten umgearbeitet werden, die mit AEM as a Cloud Service kompatibel sind. Kunden können die bestehende AEM Modernization Suite nutzen, um den Aufwand für die Modernisierung der AEM Sites-Implementierungen zu reduzieren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-Modernisierungs-Tools"

* Die klassische Benutzeroberfläche ist in AEM as a Cloud Service nicht mehr verfügbar. Die Standardoberfläche für das Authoring ist die Touch-optimierte Benutzeroberfläche.
* Die weitere Verwendung von veralteten, kundenspezifischen Komponenten kann die Wartungskosten mit der Zeit erhöhen.
* Inhaltsfragmentvorlagen wurden in AEM 6.3 durch Inhaltsfragmentmodelle ersetzt. Durch die Migration von Inhaltsfragmenten, die auf älteren Vorlagen basieren, auf AEM as a Cloud Service erhalten Sie diese Fragmente als funktionsfähig. Es ist jedoch nicht möglich, neue Fragmente basierend auf der alten Vorlage zu erstellen. Es ist auch nicht möglich, diese Fragmente mit AEM GraphQL bereitzustellen, was Inhaltsfragmentmodelle als Schemas erfordert.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Tools und Ressourcen"
>abstract="Mithilfe der AEM Modernization Suite können Kunden Classic(ExtJS)-Dialoge in Coral-Dialoge konvertieren. Dies soll Kunden dabei helfen, von den nicht unterstützten oder veralteten Funktionen zu den robusten, modernen AEM-Angeboten zu wechseln. Diese Tools sind konfigurierbar, konfigurationssensitiv und erweiterbar. Probieren Sie auch den Ersatz von benutzerdefinierten Komponenten durch den Satz standardisierter Kernkomponenten aus, um die Entwicklungszeit zu beschleunigen und die Wartungskosten Ihrer Programme zu reduzieren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/component.html" text="Komponentenkonvertierer"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html" text="Kernkomponenten"

* Verwenden Sie die [AEM-Modernisierungs-Tool-Suite](https://opensource.adobe.com/aem-modernize-tools/), um den für die Modernisierung Ihrer AEM Sites-Implementierungen erforderlichen Aufwand zu reduzieren. Diese Tools umfassen die Konvertierung von:
   * Dialogen der klassischen Oberfläche (ExtJS) zu Coral-Dialogenn
   * Basiskomponenten zu Kernkomponenten
   * Statischen Vorlagen und Spaltensteuerung zu bearbeitbaren Vorlagen und responsivem Raster
   * Designs und Design-Dialogen zu Richtlinien für bearbeitbare Vorlagen
* Überprüfen Sie die Bibliothek der benutzerdefinierten Komponenten Ihres Projekts und wechseln Sie, wenn möglich, zum Satz der standardisierten [Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=de), um die Entwicklungszeit zu beschleunigen und die Wartungskosten für Ihre Programme zu reduzieren.
* Es wird empfohlen, Inhaltsfragmentmodelle zu erstellen, die den älteren Vorlagen gleichwertige Funktionen aufweisen, und diese Modelle künftig für die Erstellung von Inhaltsfragmenten zu verwenden. Weitere Informationen finden Sie unter [Inhaltsfragmentmodelle](https://experienceleague.adobe.com/docs/experience-manager-65/assets/content-fragments/content-fragments-models.html?lang=en) für weitere Details.
* Bitte wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
