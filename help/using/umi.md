---
title: UMI
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 100%

---

# UMI {#umi}

Problem mit Fehlkonfiguration beim Upgrade

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problem mit Fehlkonfiguration beim Upgrade"
>abstract="UMI kennzeichnet Änderungen an bestimmten OSGi-Konfigurationen, die beim Upgrade zu Problemen führen, einschließlich eines fehlgeschlagenen Upgrades oder eingeschränkter Funktionalität."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Wesentliche Änderungen – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service – Versionshinweise"

`UMI` identifiziert Änderungen an bestimmten OSGi-Konfigurationen, die beim Upgrade Probleme verursachen, einschließlich eines fehlgeschlagenen Upgrades oder eingeschränkter Funktionalität.

Die folgenden Konfigurationen werden auf Änderungen überprüft:

* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`
* `org.apache.sling.commons.log.LogManager.factory.config`: Ermitteln Sie, ob die Eigenschaft `org.apache.sling.commons.log.file` der benutzerdefinierten Protokollierung auf eine andere Datei als `logs/error.log` verweist.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* Das Ändern oder Entfernen von Konfigurationen kann zu folgenden Problemen führen:
   * Das Upgrade kann hängen bleiben (zum Beispiel `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` fehlt, ist aber in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids` vorhanden).
   * Autorisierungsprobleme können nach dem Upgrade auftreten (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Bestimmte Funktionen arbeiten möglicherweise nicht wie erwartet. Die Änderung von `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` kann z. B. dazu führen, dass einige JSP-Dateien nicht kompiliert werden, was letztendlich zu einem Verlust der Funktionalität führt.
   * Die Werte der Externalizer-Konfiguration `com.day.cq.commons.impl.ExternalizerImpl` werden in AEM as a Cloud Service von Cloud Manager-Umgebungsvariablen festgelegt.
   * AEM as a Cloud Service unterstützt keine benutzerdefinierten Protokolldateien. Auf Protokolle, die in Protokollen mit benutzerdefinierten Namen geschrieben werden, kann von AEM as a Cloud Service nicht zugegriffen werden.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, Ihre aktuellen Konfigurationen zu überprüfen und alle Änderungen rückgängig zu machen, die an den genannten Konfigurationen vorgenommen wurden, um zukünftige Probleme beim Upgrade zu vermeiden. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Ändern oder entfernen Sie die vier oben genannten Konfigurationen nicht.
   * Wenn der folgende Verstoß vorliegt:\
     „Erforderliche Eigenschaften für die OSGi-Konfiguration `xyz-configuration` fehlen: ‚[property-1, property-2 …]‘.“\
     Überprüfen Sie, ob diese Löschungen rechtmäßig sind oder nicht, da diese OSGi-Konfigurationen vorkonfiguriert sind und möglicherweise noch nie im OSGi-Konfigurations-Manager geändert/gespeichert wurden.
* Wenn Konfigurationen geändert wurden, sollten sie auf ihre erwarteten Werte zurückgesetzt werden. Diese Werte sind in den `UMI`-Meldungen angegeben.
* Lesen Sie zu `com.day.cq.commons.impl.ExternalizerImpl` die [Dokumentation](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer) zum Festlegen der Externalizer-Konfiguration mithilfe von Cloud Manager-Umgebungsvariablen in AEM as a Cloud Service.
* Ändern Sie für `org.apache.sling.commons.log.LogManager.factory.config` die OSGI-Konfiguration, um den benutzerdefinierten Logger an die Datei `logs/error.log` zu senden. Lesen Sie die [Dokumentation](https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs) für das Verweisen auf die Datei `logs/error.log`.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
