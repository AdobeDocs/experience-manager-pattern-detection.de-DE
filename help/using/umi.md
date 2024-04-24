---
title: UMI
description: Mustererkennungscode Hilfeseite.
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 41%

---

# UMI {#umi}

Problem mit Upgrade-Fehlkonfiguration

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problem mit Upgrade-Fehlkonfiguration"
>abstract="UMI identifiziert Änderungen an bestimmten OSGi-Konfigurationen, die Probleme bei der Aktualisierung verursachen, einschließlich einer fehlgeschlagenen Aktualisierung oder eingeschränkter Funktionalität."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Wesentliche Änderungen – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service – Versionshinweise"

`UMI`  Identifiziert Änderungen an bestimmten OSGi-Konfigurationen, die Probleme bei der Aktualisierung verursachen, einschließlich einer fehlgeschlagenen Aktualisierung oder eingeschränkter Funktionalität.

Die folgenden Konfigurationen werden auf Änderungen überprüft:

* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`
* `org.apache.sling.commons.log.LogManager.factory.config`: Identifizieren Sie, ob die `org.apache.sling.commons.log.file`-Eigenschaft der benutzerdefinierten Logger auf eine andere als die `logs/error.log`-Datei verweist.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Das Ändern oder Entfernen von Konfigurationen kann zu folgenden Problemen führen:
   * Das Upgrade kann hängen bleiben (zum Beispiel `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` fehlt, ist aber in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids` vorhanden).
   * Autorisierungsprobleme können nach dem Upgrade auftreten (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Bestimmte Funktionen arbeiten möglicherweise nicht wie erwartet. Beispiel für eine Änderung `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` kann dazu führen, dass einige JSP-Dateien nicht kompiliert werden, was letztendlich zu Funktionsverlust führt.
   * Die Werte der Externalizer-Konfiguration `com.day.cq.commons.impl.ExternalizerImpl` werden von Cloud Manager-Umgebungsvariablen in AEM as a Cloud Service festgelegt.
   * AEM as a Cloud Service unterstützt keine benutzerdefinierten Protokolldateien. Protokolle, die in benutzerspezifische Protokolle geschrieben wurden, sind von AEM as a Cloud Service nicht zugänglich.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Implementierungsleitlinien"
>abstract="Es empfiehlt sich, Ihre aktuellen Konfigurationen zu überprüfen und alle Änderungen rückgängig zu machen, die an den genannten Konfigurationen vorgenommen wurden, um zukünftige Probleme bei der Aktualisierung zu vermeiden. Wenden Sie sich an den Adobe-Support , um Hilfe oder Erläuterungen zu erhalten."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Ändern oder entfernen Sie die vier oben genannten Konfigurationen nicht.
   * Wenn die folgende Verletzung vorliegt:\
     &quot;Erforderliche Eigenschaften für die OSGi-Konfiguration `xyz-configuration` fehlen: &#39;[property-1,property-2...]&quot;.&quot;\
     Bestätigen Sie, ob diese Löschungen rechtmäßig sind oder nicht, weil diese OSGi-Konfigurationen OOTB sind und möglicherweise noch nie im OSGi Config Manager geändert/gespeichert wurden.
* Wenn Konfigurationen geändert wurden, sollten sie auf ihre erwarteten Werte zurückgesetzt werden. Diese Werte sind in den `UMI`-Meldungen angegeben.
* Für `com.day.cq.commons.impl.ExternalizerImpl`, siehe [Dokumentation](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer) zum Festlegen der Externalizer-Konfiguration mithilfe von Cloud Manager-Umgebungsvariablen in AEM as a Cloud Service.
* Für `org.apache.sling.commons.log.LogManager.factory.config` ändern Sie die OSGI-Konfiguration, um den benutzerdefinierten Logger an die `logs/error.log`-Datei zu senden. Siehe [Dokumentation](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs) , um erneut auf die `logs/error.log` -Datei.
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
