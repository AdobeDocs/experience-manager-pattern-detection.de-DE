---
title: FORMULAR
description: Hilfeseite zum Mustererkennungs-Code
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
translation-type: tm+mt
source-git-commit: cbd43bca20831c19eb30703cc1ec528c75f2a2ef
workflow-type: tm+mt
source-wordcount: '1136'
ht-degree: 41%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Hintergrund {#background}

`FORMS` Identifiziert potenzielle Probleme im Zusammenhang mit der Migration von  [!DNL Adobe Experience Manager Forms] zu  [!DNL Adobe Experience Manager Form]s als  [!DNL Cloud Service]. Beheben Sie diese Probleme, bevor Sie zu [!DNL Cloud Service] migrieren.

Die folgenden Untertypen helfen Ihnen, die verschiedenen Arten von Problemen zu unterscheiden:

* `modified.feature`: Diese Funktionen, Assets oder APIs wurden für Cloud Service aktualisiert oder geändert. Führen Sie vor der Migration zu Cloud Service das Migrationsdienstprogramm aus, um diese Funktionen und Assets mit Cloud Service kompatibel zu machen.
* `unavailable.feature`: Ihre Umgebung verfügt über Funktionen und Assets, die nicht verfügbar sind oder aus Cloud Service entfernt wurden. Migrieren Sie solche Funktionen oder Assets nicht in eine Cloud Service-Umgebung.
* `unsupported.feature`: Ihre Umgebung verwendet einige Funktionen, die von Cloud Service noch nicht unterstützt werden. Migrieren Sie solche Funktionen oder Assets nicht in eine Cloud Service-Umgebung. In den monatlichen Versionshinweisen finden Sie Informationen zur Verfügbarkeit der Funktionen.
* `unsupported.api`: Ihre Umgebung enthält einige APIs, die von Cloud Service noch nicht unterstützt werden. Deaktivieren, ersetzen oder entfernen Sie diese APIs aus Ihrem Code, bevor Sie zu Cloud Service migrieren. In den monatlichen Versionshinweisen finden Sie Informationen zur Verfügbarkeit der Funktionen.

In den Abschnitten [Mögliche Implikationen und Risiken](#implications-and-risks) und [Mögliche Lösungen](#solutions) finden Sie Informationen zu Ersetzungen und anderen Maßnahmen, die erforderlich sind, um einige Funktionen und APIs mit Cloud Service kompatibel zu machen.

## Mögliche Implikationen und Risiken {#implications-and-risks}

Beheben Sie die folgenden Probleme, bevor Sie zu [!DNL Adobe Experience Manager Forms as a Cloud Service] migrieren. Wenn die unten aufgeführten Implikationen und Risiken nicht beachtet werden, funktionieren einige Funktionen in der Cloud Service-Umgebung nicht wie erwartet.

* Die Funktionalität zum Ändern von Code im Regeleditor ist nicht verfügbar. (CODE_EDITOR)

* Die E-Mail-Unterstützung (SMTP-Port) ist standardmäßig deaktiviert. (EMAIL_SERVICE_CONFIGURATION)

* Die Übermittlungsaktion **[!UICONTROL E-Mail-PDF]** ist nicht verfügbar.(EMAIL_PDF_SUBMIT_ACTION)

* XFA-basiertes adaptives Forms werden noch nicht unterstützt. (XFA_BASED_FORM, XDP_BASED_FORM)

* Eine Übermittlungsaktion wird sofort beim Senden des Formulars aufgerufen, anstatt darauf zu warten, dass alle Unterzeichner die Unterschrift abschließen. Die an Unterzeichner gesendete Adobe Sign-Vereinbarung-PDF steht daher nicht zur Verwendung oder Verarbeitung von Übermittlungsaktionen zur Verfügung. (FORM_SIGN_INTEGRATION)

* Der Unterschriftsschritt ist nicht verfügbar. (SIGNATURE_STEP)

* Der Verifizierungsschritt ist nicht verfügbar. (VERIFY_STEP)

* Die Funktion &quot;Forms Portal&quot;und **[!UICONTROL Forms Portal-Übermittlungsaktion]** sind noch nicht verfügbar. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Die Übermittlungsaktion **[!UICONTROL An Forms Workflow senden]** ist nicht verfügbar. Bei [!DNL AEM 6.5 Forms] und früheren Versionen wurde die Übermittlungsaktion verwendet, um adaptive Formulardaten an ältere Workflows und LiveCycle Workflow zu senden. [!DNL AEM Forms on JEE] (LC_WORKFLOW_SUBMISSION)

* Die Funktion „Interaktive Kommunikationen“ ist nicht verfügbar.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Die Funktionen **[!UICONTROL Als Entwurf speichern]** und **[!UICONTROL Automatische Speicherung]** für adaptive Formulare werden derzeit nicht unterstützt. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Metadaten-Akkordeon ist nicht verfügbar. (METADATA_ACCORDION_FORM_CONTAINER)

* Die CAPTCHA-Komponente verwendet jetzt standardmäßig den reCAPTCHA-Service von Google zur Validierung von CAPTCHA. Die Option, mit Adobe Experience Manager CAPTCHA zu validieren, wird nicht mehr unterstützt. (FORMS_CAPTCHA)

* [!DNL AEM Forms] App ist nicht verfügbar für  [!DNL Cloud Services]. (AEM_FORMS_APP)

* [Dokument ](https://experienceleague.adobe.com/docs/experience-manager-65/forms/install-aem-forms/osgi-installation/install-configure-document-services.html?lang=en#deployment-topology) Services-Schritte sind in AEM Workflows nicht verfügbar. (WORKFLOW_DOCSERVICES)

## Mögliche Lösungen {#solutions}

* Verwenden Sie das Migrationsdienstprogramm, um alle Regelskripte in Ihrer Umgebung in wiederverwendbare Funktionen umzuwandeln. Sie können die wiederverwendbaren Funktionen mit dem Visual Rule Editor verwenden, um weiterhin Ergebnisse zu erhalten, die mit Regelskripten erzielt wurden. (CODE_EDITOR)

* Wenden Sie sich an das Supportteam, um die E-Mail-Funktionalität (offener SMTP-Port) für Ihre Umgebung zu aktivieren. Standardmäßig sind nur ausgehende HTTP- und HTTPS-Verbindungen aktiviert. (EMAIL_SERVICE_CONFIGURATION, E-Mail-Schritt)

* Verwenden Sie **[!UICONTROL E-Mail]** Übermittlungsaktion anstelle von **[!UICONTROL E-Mail-PDF]**. Die Übermittlungsaktion **[!UICONTROL E-Mail]** bietet Optionen zum Senden von Anlagen und zum Anhängen von Dokument aus Datensatz (DoR) mit E-Mail. (EMAIL_PDF_SUBMIT_ACTION)

* Gesendete Daten enthalten die Adobe Sign-Vertrag-ID. Sie können die Sign-Vereinbarungs-ID verwenden, um bei Bedarf eine Sign-Vereinbarungs-PDF abzurufen.  (FORM_SIGN_INTEGRATION)

* Entfernen Sie den Unterschriftsschritt aus einem vorhandenen adaptiven Formular. Konfigurieren Sie Ihr adaptives Formular für die Verwendung von [in-Browser-Signatur](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Es zeigt die Adobe Sign-Vereinbarung an, die Vereinbarung beim Senden eines adaptiven Formulars im Browser zu unterzeichnen. Das Signieren im Browser erleichtert das Signieren und spart Zeit für den Unterzeichner. (SIGNATURE_STEP)

* Entfernen Sie den Überprüfungsschritt aus dem vorhandenen adaptiven Forms, bevor Sie diese Formulare in eine [!DNL Cloud Service]-Umgebung verschieben. (VERIFY_STEP)

* Ändern Sie Ihre vorhandenen adaptiven Formulare so, dass [An REST-Endpunkt senden](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-to-rest-endpoint), [E-Mail senden](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#send-email), [Senden mit Formulardatenmodell](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-using-form-data-model) und [Einen AEM Workflow](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Übermittlungsaktionen aufrufen. Forms Portal- und Forms Portal-Übermittlungsaktion sind noch nicht verfügbar. In den monatlichen Versionshinweisen finden Sie Informationen zur Verfügbarkeit der Funktionen. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL)

* Sie können einen AEM Workflow entwickeln und Ihre vorhandenen adaptiven Formulare ändern, um mithilfe von [AEM Workflow](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Übermittlungsaktion Daten an einen AEM Workflow zu senden, anstatt die Übermittlungsaktion **[!UICONTROL An Forms Workflow senden]** zu verwenden. Sie können eine benutzerdefinierte Übermittlungsaktion entwickeln, um Daten, Anlagen oder Dokumente aus Datensatz (DoR) an einen LiveCycle-Prozess zu senden, anstatt [!UICONTROL An Forms Workflow senden] zu verwenden. (LC_WORKFLOW_SUBMISSION)

* In den monatlichen Versionshinweisen finden Sie Informationen zur Verfügbarkeit der Funktion Interaktive Kommunikation. Migrieren Sie Ihre interaktiven Kommunikations-, Briefe- und zugehörigen Wörterbücher nicht in eine Umgebung des Cloud Service, bis die Funktion nicht verfügbar ist. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Deaktivieren Sie die Optionen **[!UICONTROL Als Entwurf speichern]** und **[!UICONTROL Automatisches Speichern unter]** aktivieren, bevor Sie sie in den Cloud Service migrieren. Sie können diese Optionen aktivieren, sobald die Formularportal-Funktion für Cloud Service freigegeben ist. In den monatlichen Versionshinweisen finden Sie Informationen zur Verfügbarkeit der Funktionen. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Es gibt keinen Ersatz für das Metadaten-Akkordeon. Entfernen Sie es aus Ihren Formularen, bevor Sie sie zu Cloud Service migrieren. (METADATA_ACCORDION_FORM_CONTAINER)

* Verwenden Sie das Google reCAPTCHA anstelle des von Adobe Experience Manager bereitgestellten CAPTCHA-Services. (FORMS_CAPTCHA)

* Adaptives Forms-Angebot ein reaktionsfähiges Design. Diese Formulare ändern Aussehen, Design und Interaktivität je nach zugrunde liegendem Gerät. Sie können das adaptive Forms auf Mobilgeräten weiterhin verwenden. In den monatlichen Versionshinweisen finden Sie Informationen zur Verfügbarkeit der [!DNL AEM Forms]-App. (AEM_FORMS_APP)

* Migrieren Sie kein AEM Workflow-Modell, das einen Dokument Services Workflow-Schritt verwendet. Migrieren oder aktualisieren Sie außerdem kein adaptives Forms, das Benutzerdaten an ein Workflow-Modell sendet, das Dokument Services-Arbeitsablaufschritte verwendet, oder ändern Sie die Übermittlungsaktion in eine unterstützte Aktion, bevor Sie das Formular migrieren. [](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html) (WORKFLOW_DOCSERVICES)

* Die Unterstützung für XFA-basierte adaptive Forms ist nicht standardmäßig verfügbar. Wenn Sie XFA-basiertes adaptives Forms verwenden möchten, wenden Sie sich an den Support der Adobe mit Einzelheiten zu Ihrem Anwendungsfall und spezifischen Anforderungen.(XFA_BASED_FORM, XDP_BASED_FORM)

Wenden Sie sich an den [Adobe Support](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
