---
title: UMI
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: b19818f3f043641328b68adfe37a9c9cb09d1143
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 86%

---

# UMI {#umi}

Problem mit Upgrade-Fehlkonfiguration

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problem mit Upgrade-Fehlkonfiguration"
>abstract="UMI kennzeichnet Änderungen an bestimmten OSGi-Konfigurationen, die beim Upgrade zu Problemen führen, einschließlich eines fehlgeschlagenen Upgrades oder eingeschränkter Funktionalität."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de" text="Wesentliche Änderungen – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de" text="AEM as a Cloud Service – Versionshinweise"

`UMI` kennzeichnet Änderungen an bestimmten OSGi-Konfigurationen, die beim Upgrade zu Problemen führen, einschließlich eines fehlgeschlagenen Upgrades oder eingeschränkter Funktionalität.

Die folgenden Konfigurationen werden auf Änderungen überprüft:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Das Ändern oder Entfernen von Konfigurationen kann zu folgenden Problemen führen:
   * Das Upgrade kann hängen bleiben (zum Beispiel `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` fehlt, ist aber in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids` vorhanden).
   * Autorisierungsprobleme können nach dem Upgrade auftreten (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Bestimmte Funktionen arbeiten möglicherweise nicht wie erwartet. Die Änderung von `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` kann z. B. dazu führen, dass einige JSP-Dateien nicht kompiliert werden, was letztendlich zu einem Verlust der Funktionalität führt.
   * Die Werte der Externalizer-Konfiguration `com.day.cq.commons.impl.ExternalizerImpl` werden von Cloud Manager-Umgebungsvariablen in AEM as a Cloud Service festgelegt.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, Ihre aktuellen Konfigurationen zu überprüfen und alle Änderungen, die an den genannten Konfigurationen vorgenommen wurden, rückgängig zu machen, um zukünftige Upgrade-Probleme zu vermeiden. Wenden Sie sich an den Adobe Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Ändern oder entfernen Sie die vier oben genannten Konfigurationen nicht.
   * Im Falle des folgenden Verstoßes :\
      &quot;Erforderliche Eigenschaften für die OSGi-Konfiguration &quot;xyz-configuration&quot;fehlen: &#39;[property-1,property-2...]&quot;.&quot;\
      Bitte überprüfen Sie, ob diese Löschungen rechtmäßig sind oder nicht, da diese OSGi-Konfigurationen OOTB sind und möglicherweise noch nie im OSGi Config Manager geändert/gespeichert wurden.
* Wenn Konfigurationen geändert wurden, sollten sie auf ihre erwarteten Werte zurückgesetzt werden. Diese Werte sind in den `UMI`-Meldungen angegeben.
* Lesen Sie für `com.day.cq.commons.impl.ExternalizerImpl` die [Dokumentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/externalizer.html?lang=de) zum Festlegen der Externalizer-Konfiguration mithilfe von Cloud Manager-Umgebungsvariablen in AEM as a Cloud Service.
* Bitte wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
