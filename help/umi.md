---
title: UMI
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
translation-type: tm+mt
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 70%

---

# UMI {#umi}

Problem mit Upgrade-Fehlkonfiguration

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problem mit Upgrade-Fehlkonfiguration"
>abstract="UMI identifiziert Änderungen bestimmter OSGi-Konfigurationen, die Probleme bei der Aktualisierung verursachen, einschließlich einer fehlgeschlagenen Aktualisierung oder eingeschränkter Funktionalität."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de" text="Bemerkenswerte Änderungen - AEM als Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de" text="AEM als Cloud Service - Versionshinweise"

`UMI` steht für Änderungen an bestimmten OSGi-Konfigurationen, die beim Upgrade zu Problemen führen, einschließlich eines fehlgeschlagenen Upgrades oder eingeschränkter Funktionalität.

Die folgenden Konfigurationen werden auf Änderungen überprüft:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Das Ändern oder Entfernen von Konfigurationen kann zu folgenden Problemen führen:
   * Das Upgrade kann hängen bleiben (zum Beispiel `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` fehlt, ist aber in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids` vorhanden).
   * Autorisierungsprobleme können nach dem Upgrade auftreten (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Bestimmte Funktionen arbeiten möglicherweise nicht wie erwartet. Die Änderung von `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` kann z. B. dazu führen, dass einige JSP-Dateien nicht kompiliert werden, was letztendlich zu einem Verlust der Funktionalität führt.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Durchführungsleitlinien"
>abstract="Best Practice ist, Ihre aktuellen Konfigurationen zu überprüfen und alle Änderungen, die an den erwähnten Konfigurationen vorgenommen wurden, rückgängig zu machen, um zukünftige Aktualisierungsprobleme zu vermeiden. Support zur Adobe für Hilfe und Klarstellungen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-Support"

* Ändern oder entfernen Sie die vier oben genannten Konfigurationen nicht.
* Wenn Konfigurationen geändert wurden, sollten sie auf ihre erwarteten Werte zurückgesetzt werden. Diese Werte sind in den `UMI`-Meldungen angegeben.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
