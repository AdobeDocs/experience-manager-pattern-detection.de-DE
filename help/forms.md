---
title: Forms
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: a6ba6e93c89644160650882ecbf17028bec35068
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---


# [!DNL FORMS] {#forms}

[!DNL Adobe Experience Manager Forms]

## Hintergrund {#background}

`FORMS` potenzielle Probleme im Zusammenhang mit der Migration von Adobe Experience Manager Forms nach Adobe Experience Manager Forms als Cloud Service ermittelt. Beheben Sie diese Probleme, bevor Sie zu Cloud Service migrieren.

Die folgenden Untertypen helfen Ihnen, die verschiedenen Arten von Problemen zu identifizieren:

* `modified.feature`: Diese Funktionen, Assets oder APIs wurden zum Cloud Service aktualisiert oder geändert. Führen Sie vor der Migration auf den Cloud Service das Migrationsdienstprogramm aus, um diese Funktionen und Elemente mit dem Cloud Service kompatibel zu machen.
* `unavailable.feature`: Ihre Umgebung enthält Funktionen und Elemente, die nicht verfügbar sind oder aus dem Cloud Service entfernt wurden. Migrieren Sie solche Funktionen oder Assets nicht in eine Cloud Service-Umgebung.
* `unsupported.feature`: Ihre Umgebung verwendet einige Funktionen, die auf Cloud Service noch nicht unterstützt werden. Migrieren Sie solche Funktionen oder Assets nicht in eine Cloud Service-Umgebung. Sehen Sie sich die monatlichen Versionshinweise zur Verfügbarkeit der Funktionen an.
* `unsupported.api`: Ihre Umgebung enthält einige APIs, die auf dem Cloud Service noch nicht unterstützt werden. Bevor Sie auf den Cloud Service migrieren, deaktivieren, ersetzen oder entfernen Sie diese APIs aus Ihrem Code. Sehen Sie sich die monatlichen Versionshinweise zur Verfügbarkeit der Funktionen an.

Weitere Informationen zu Ersetzungen und anderen erforderlichen Maßnahmen, um einige Funktionen und APIs mit dem Cloud Service kompatibel zu machen, finden Sie unter [Mögliche Implikationen und Risiken](#implications-and-risks) und [Mögliche Lösungen](#solutions).

## Mögliche Implikationen und Risiken {#implications-and-risks}

Beheben Sie die folgenden Probleme, bevor Sie als Cloud Service nach Adobe Experience Manager Forms migrieren. Wenn die unten aufgeführten Implikationen und Risiken nicht behoben werden, funktionieren einige Funktionen nicht wie in der Umgebung des Cloud Service erwartet.

* Die Codeeditorfunktion der Regeleditorfunktion ist nicht verfügbar. (CODE_EDITOR)

* Die E-Mail-Unterstützung (SMTP-Anschluss) ist standardmäßig deaktiviert. (EMAIL_SERVICE_CONFIGURATION)

* Die Übermittlungsaktion **[!UICONTROL E-Mail-PDF]** ist nicht verfügbar.(EMAIL_PDF_SUBMIT_ACTION)

* XDP-basierte adaptive Formulare werden noch nicht unterstützt. (XDP_BASED_FORM)

* Eine Übermittlungsaktion wird sofort beim Senden des Formulars aufgerufen, anstatt darauf zu warten, dass alle Unterzeichner die Unterschrift abschließen. Das Dokument für die Signatur des adaptiven Formulars (Adobe Sign Agreement PDF an Unterzeichner gesendet) steht daher nicht zur Verwendung oder Verarbeitung von Übermittlungsaktionen zur Verfügung. (FORM_SIGN_INTEGRATION)

* Der Unterschriftsschritt ist nicht verfügbar. (SIGNATURE_STEP)

* Der Schritt Überprüfen ist nicht verfügbar. (VERIFY_STEP)

* Die Forms Portal-Funktion und die Übermittlungsaktion **[!UICONTROL Forms Portal]** sind nicht verfügbar. Sie können Forms Portal nicht zum Listen von Formularen, zum Speichern von Entwürfen oder zum Anzeigen gesendeter Formulare verwenden. Sie können keine Daten senden (verwenden Sie **[!UICONTROL Forms Portal-Übermittlungsaktion]**), die an ein adaptives Formular an ein Forms Portal gesendet werden. [!UICONTROL Die Funktionen zum Speichern als ] Entwurf und zum  [!UICONTROL automatischen ] Speichern adaptiver Formulare werden derzeit nicht unterstützt. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Die Übermittlungsaktion **[!UICONTROL An Forms-Workflow übermitteln]** ist nicht verfügbar. In AEM 6.5 Forms und früheren Versionen wurde die Übermittlungsaktion zum Übermitteln adaptiver Formulardaten an ältere AEM Forms on JEE-Workflows und -LiveCycle Workflow verwendet. (LC_WORKFLOW_SUBMISSION)

* Die Funktion für interaktive Kommunikation ist nicht verfügbar.  (FP_PROFIL_INTERACTIVE_COMMUNICATIONS).

* **[!UICONTROL Die Funktionen zum Speichern als]** Entwurf und zum  **[!UICONTROL automatischen]** Speichern adaptiver Formulare werden derzeit nicht unterstützt. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Metadaten-Akkordeon ist nicht verfügbar. (METADATA_ACCORDION_FORM_CONTAINER)

* Die CAPTCHA-Komponente verwendet jetzt den Google reCAPTCHA-Dienst, um CAPTCHA standardmäßig zu validieren. Die Option zur Verwendung von Adobe Experience Manager zur Validierung von CAPTCHA ist nicht verfügbar. (FORMS_CAPTCHA)

## Mögliche Lösungen {#solutions}

* Verwenden Sie das Migrationsdienstprogramm, um alle Regelskripte auf Ihrer Umgebung in wiederverwendbare Funktionen zu konvertieren. Sie können die wiederverwendbaren Funktionen mit dem Visual Rule Editor verwenden, um weiterhin Ergebnisse zu erhalten, die mit Regelskripten erzielt wurden. (CODE_EDITOR)

* Wenden Sie sich an das Supportteam, um die E-Mail-Funktion (SMTP-Anschluss öffnen) für Ihre Umgebung zu aktivieren. Standardmäßig sind nur ausgehende HTTP- und HTTPS-Verbindungen aktiviert. (EMAIL_SERVICE_CONFIGURATION)

* Verwenden Sie die Übermittlungsaktion **[!UICONTROL E-Mail]** anstelle von **[!UICONTROL E-Mail-PDF]**. Die Übermittlungsaktion **[!UICONTROL E-Mail]** bietet Optionen zum Senden von Anlagen und zum Anhängen von Dokument aus Datensatz (DoR) an E-Mail. (EMAIL_PDF_SUBMIT_ACTION)

* Migrieren Sie keine XDP-basierten adaptiven Formulare in eine Cloud Service-Umgebung. Sehen Sie sich die monatlichen Versionshinweise zur Verfügbarkeit der Funktionen an. (XDP_BASED_FORM)

* Gesendete Daten enthalten die Signaturvereinbarung-ID. Sie können bei Bedarf die Signiervereinbarung-ID verwenden, um eine PDF-Datei mit einer Signiervereinbarung abzurufen.  (FORM_SIGN_INTEGRATION)

* Ersetzen Sie den Signaturschritt in Ihren adaptiven Formularen durch die Option zum Signieren eines Beitrags zum Senden eines adaptiven Formulars im selben Fenster. Damit können Sie weiterhin ein [In-Browser-Signaturerlebnis](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684) bereitstellen. (SIGNATURE_STEP)

* Entfernen Sie den Überprüfungsschritt aus Ihren vorhandenen adaptiven Formularen, bevor Sie diese Formulare in eine Cloud Service-Umgebung verschieben. (VERIFY_STEP)

* Es gibt keine Alternative zur Übermittlungsaktion **[!UICONTROL Forms Portal]**. Sie können diese Übermittlungsaktion verwenden, sobald die Forms Portal-Funktion für den Cloud Service veröffentlicht wurde. Sehen Sie sich die monatlichen Versionshinweise zur Verfügbarkeit der Funktionen an. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL)

* Es gibt keine andere Übermittlungsaktion für die Übermittlungsaktionen **[!UICONTROL An Forms-Workflow senden]**. Sie können eine benutzerdefinierte Übermittlungsaktion entwickeln, um Daten, Anlagen oder Dokumente aus Datensatz (DoR) an einen LiveCycle-Prozess zu senden. (LC_WORKFLOW_SUBMISSION)

* Migrieren Sie Ihre interaktiven Kommunikations-, Briefe- und verwandten Wörterbücher nicht in eine Cloud Service-Umgebung. (FP_PROFIL_INTERACTIVE_COMMUNICATIONS)

* Deaktivieren Sie die Optionen **[!UICONTROL Als Entwurf speichern]** und **[!UICONTROL Automatisches Speichern unter]** aktivieren, bevor Sie sie in den Cloud Service migrieren. Sie können diese Optionen aktivieren, sobald die Forms Portal-Funktion für den Cloud Service veröffentlicht wurde. Sehen Sie sich die monatlichen Versionshinweise zur Verfügbarkeit der Funktionen an. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Metadaten-Akkordeon wird nicht ersetzt. Entfernen Sie sie aus Ihren Formularen, bevor Sie sie in Cloud Service migrieren.(METADATA_ACCORDION_FORM_CONTAINER)

* Verwenden Sie Google reCaptcha anstelle des von Adobe Experience Manager bereitgestellten CAPTCHA-Dienstes. (FORMS_CAPTCHA)

Wenden Sie sich an den [Support für Adoben](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um Klarstellungen zu erhalten oder Bedenken auszuräumen.
