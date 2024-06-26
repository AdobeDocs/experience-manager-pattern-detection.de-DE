---
title: FORM
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 100%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="FORMS"
>abstract="FORMS-Code identifiziert potenzielle Probleme im Zusammenhang mit der Migration von AEM (Adobe Experience Manager) Forms zu AEM Forms as a Cloud Service. Prüfen Sie die möglichen Auswirkungen und Risiken, die damit verbunden sind, und gehen Sie diese Probleme an, bevor Sie zu Cloud Service migrieren."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-pattern-detection/table-of-contents/forms#implications-and-risks" text="Mögliche Auswirkungen und Risiken"

`FORMS` identifiziert potenzielle Probleme im Zusammenhang mit der Migration von [!DNL Adobe Experience Manager Forms] zu [!DNL Adobe Experience Manager Forms] as a [!DNL Cloud Service]. Beheben Sie diese Probleme, bevor Sie zu [!DNL Cloud Service] migrieren.

Die folgenden Untertypen helfen Ihnen, die verschiedenen Arten von Problemen zu unterscheiden:

* `modified.feature`: Diese Funktionen, Assets oder APIs wurden für Cloud Service aktualisiert oder geändert. Führen Sie vor der Migration zu Cloud Service das Migrationsdienstprogramm aus, um diese Funktionen und Assets mit Cloud Service kompatibel zu machen.
* `unavailable.feature`: Ihre Umgebung verfügt über Funktionen und Assets, die nicht verfügbar sind oder aus Cloud Service entfernt wurden. Migrieren Sie solche Funktionen oder Assets nicht in eine Cloud Service-Umgebung.
* `unsupported.feature`: Ihre Umgebung verwendet einige Funktionen, die von Cloud Service noch nicht unterstützt werden. Migrieren Sie solche Funktionen oder Assets nicht in eine Cloud Service-Umgebung. In den monatlichen Versionshinweisen finden Sie Informationen zur Verfügbarkeit der Funktionen.
* `unsupported.api`: Ihre Umgebung enthält einige APIs, die von Cloud Service noch nicht unterstützt werden. Deaktivieren, ersetzen oder entfernen Sie diese APIs aus Ihrem Code, bevor Sie zu Cloud Service migrieren. In den monatlichen Versionshinweisen finden Sie Informationen zur Verfügbarkeit der Funktionen.

In den Abschnitten [Mögliche Implikationen und Risiken](#implications-and-risks) und [Mögliche Lösungen](#solutions) finden Sie Informationen zu Ersetzungen und anderen Maßnahmen, die erforderlich sind, um einige Funktionen und APIs mit Cloud Service kompatibel zu machen.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

Beheben Sie die folgenden Probleme, bevor Sie zu [!DNL Adobe Experience Manager Forms as a Cloud Service] migrieren. Wenn die unten aufgeführten Implikationen und Risiken nicht beachtet werden, funktionieren einige Funktionen in der Cloud Service-Umgebung nicht wie erwartet.

* Die Funktionalität zum Ändern von Code im Regeleditor ist nicht verfügbar. (CODE_EDITOR)

* Die E-Mail-Unterstützung (SMTP-Port) ist standardmäßig deaktiviert. (EMAIL_SERVICE_CONFIGURATION)

* Die Übermittlungsaktion **[!UICONTROL PDF per E-Mail senden]** ist nicht verfügbar.  (EMAIL_PDF_SUBMIT_ACTION)

* XFA-basierte adaptive Formulare werden noch nicht unterstützt. (XFA_BASED_FORM, XDP_BASED_FORM)

* Eine Übermittlungsaktion wird sofort beim Absenden eines Formulars aufgerufen, anstatt zu warten, bis alle Unterzeichner das Signieren abgeschlossen haben. Die Adobe Sign-Vereinbarungs-PDF, die an die Unterzeichner gesendet wird, steht daher nicht für die Verwendung oder Verarbeitung von Übermittlungsaktionen zur Verfügung. (FORM_SIGN_INTEGRATION)

* Der Unterschriftsschritt ist nicht verfügbar. (SIGNATURE_STEP)

* Der Verifizierungsschritt ist nicht verfügbar. (VERIFY_STEP)

* Die Übermittlungsaktion **[!UICONTROL An Forms Workflow übermitteln]** ist nicht verfügbar. In AEM 6.5 Forms und früheren Versionen wurde die Übermittlungsaktion verwendet, um Daten aus adaptiven Formularen an ältere AEM Forms auf JEE-Workflows und LiveCycle-Workflows zu übermitteln. (LC_WORKFLOW_SUBMISSION)

* Die Funktion „Interaktive Kommunikationen“ ist nicht verfügbar. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* Metadaten-Akkordeon ist nicht verfügbar. (METADATA_ACCORDION_FORM_CONTAINER)

* Die CAPTCHA-Komponente verwendet jetzt standardmäßig den reCAPTCHA-Service von Google zur Validierung von CAPTCHA. Die Option zur Verwendung von Adobe Experience Manager zur Validierung von CAPTCHA ist nicht mehr verfügbar. (FORMS_CAPTCHA)

* Die Mobile App von [!DNL AEM Forms] ist für [!DNL Cloud Services] nicht verfügbar. (AEM_FORMS_APP)

* [Dokumentendienst](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/forms/install-aem-forms/osgi-installation/install-configure-document-services#deployment-topology)-Schritte sind in AEM-Workflows nicht verfügbar. (WORKFLOW_DOCSERVICES)

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="Implementierungsleitlinien"
>abstract="Informationen, die über den Code FORMS bereitgestellt werden, können Hinweise auf Ersetzungen und andere Maßnahmen geben, die erforderlich sind, um einige Funktionen und APIs mit Cloud Service kompatibel zu machen. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Verwenden Sie ein Migrationsdienstprogramm, um alle Regelskripte in Ihrer Umgebung in wiederverwendbare Funktionen umzuwandeln. Sie können die wiederverwendbaren Funktionen mit dem visuellen Regeleditor verwenden, um weiterhin Ergebnisse zu erhalten, die mit Regelskripten erzielt wurden. (CODE_EDITOR)

* Wenden Sie sich an das Supportteam, um die E-Mail-Funktion für Ihre Umgebung zu aktivieren (SMTP-Port öffnen). Standardmäßig sind nur ausgehende HTTP- und HTTPS-Verbindungen aktiviert. (EMAIL_SERVICE_CONFIGURATION, E-Mail-Schritt)

* Verwenden Sie die Übermittlungsaktion **[!UICONTROL E-Mail]** anstelle von **[!UICONTROL PDF per E-Mail senden]**. Die Übermittlungsaktion **[!UICONTROL E-Mail]** bietet Optionen zum Senden von Anhängen und zum Anhängen von Belegdokumenten (Document of Record, DoR) per E-Mail. (EMAIL_PDF_SUBMIT_ACTION)

* Übermittelte Daten enthalten die Adobe Sign-Vereinbarungs-ID. Sie können die Sign-Vereinbarungs-ID verwenden, um bei Bedarf eine Sign-Vereinbarungs-PDF abzurufen. (FORM_SIGN_INTEGRATION)

* Entfernen Sie den Unterschriftsschritt aus einem vorhandenen adaptiven Formular. Konfigurieren Sie Ihr adaptives Formular so, dass es [im Browser signiert werden kann](https://blog.developer.adobe.com/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Nach der Übermittlung eines adaptiven Formulars wird die Adobe Sign-Vereinbarung im Browser zur Unterzeichnung angezeigt. Die In-Browser-Signatur ermöglicht ein schnelleres Unterzeichnen und spart dem Unterzeichner Zeit. (SIGNATURE_STEP)

* Entfernen Sie den Verifizierungsschritt aus Ihren vorhandenen adaptiven Formularen, bevor Sie solche Formulare in eine [!DNL Cloud Service]-Umgebung verschieben. (VERIFY_STEP)

* Bearbeiten Sie Ihre vorhandenen adaptiven Formulare so, dass Sie die Übermittlungsaktionen [An REST-Endpunkt übermitteln](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-to-rest-endpoint), [E-Mail senden](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#send-email), [Senden mit Formulardatenmodell](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-using-form-data-model) und [Aufrufen eines AEM-Workflows](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) verwenden können.

* Sie können einen AEM-Workflow entwickeln und Ihre vorhandenen adaptiven Formulare bearbeiten, sodass sie die Übermittlungsaktion [AEM-Workflow](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) anstatt der Übermittlungsaktion **[!UICONTROL An Formular-Workflow übermitteln]** verwendet, um Daten an einen AEM-Workflow zu senden. Sie können eine benutzerdefinierte Übermittlungsaktion entwickeln, um Daten, Anlagen oder Belegdokumente (DoR) an einen LiveCycle-Prozess zu senden, anstatt den [!UICONTROL An Forms Workflow übermitteln] zu verwenden. (LC_WORKFLOW_SUBMISSION)

* In den monatlichen Versionshinweisen finden Sie Informationen zur Verfügbarkeit der Funktion „Interaktive Kommunikation“. Migrieren Sie Ihre interaktiven Kommunikationen, Briefe und zugehörigen Wörterbücher nicht in eine Cloud Service-Umgebung, solange die Funktion nicht verfügbar ist. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Es gibt keinen Ersatz für das Metadaten-Akkordeon. Entfernen Sie es aus Ihren Formularen, bevor Sie sie zu Cloud Service migrieren. (METADATA_ACCORDION_FORM_CONTAINER)

* Verwenden Sie das Google reCAPTCHA anstelle des von Adobe Experience Manager bereitgestellten CAPTCHA-Services. (FORMS_CAPTCHA)

* Migrieren Sie nicht zu einem AEM-Workflow-Modell, das einen Dokumentendienste-Workflow-Schritt verwendet. Migrieren oder aktualisieren Sie außerdem keine adaptiven Formulare, die Benutzerdaten an ein Workflow-Modell senden, das Workflow-Schritte der Dokumentendienste verwendet, oder ändern Sie **`Submit Action`** in eine [unterstützte Aktion](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions), bevor Sie das Formular migrieren. (WORKFLOW_DOCSERVICES)

* Adaptive Formulare bieten ein responsives Design. Diese Formulare ändern Erscheinungsbild, Design und Interaktivität je nach zugrunde liegendem Gerät. Sie können adaptive Formulare weiterhin auf einem Mobilgerät verwenden. Achten Sie auf die monatlichen Versionshinweise für Informationen zur Verfügbarkeit der [!DNL AEM Forms]-App. (AEM_FORMS_APP)

* Die Unterstützung für XFA-basierte adaptive Formulare ist nicht standardmäßig. Wenn Sie XFA-basierte adaptive Formulare verwenden möchten, wenden Sie sich mit den Details zu Ihrem Anwendungsfall und den spezifischen Anforderungen an den Adobe-Support.(XFA_BASED_FORM, XDP_BASED_FORM)

Sollten Sie Fragen oder Probleme haben, wenden Sie sich an den [Adobe-Support](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html).
