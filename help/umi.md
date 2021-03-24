---
title: UMI
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# UMI {#umi}

Problem mit der Aktualisierung

## Hintergrund {#background}

`UMI` identifiziert Änderungen bestimmter OSGi-Konfigurationen, die Probleme bei der Aktualisierung verursachen, einschließlich einer fehlgeschlagenen Aktualisierung oder eingeschränkter Funktionalität.

Die folgenden Konfigurationen werden auf Änderung überprüft:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Das Ändern oder Entfernen von Konfigurationen kann zu folgenden Problemen führen:
   * Die Aktualisierung kann hängen bleiben (zum Beispiel `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` fehlt, ist aber in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids` vorhanden).
   * Autorisierungsprobleme können nach der Aktualisierung auftreten (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Bestimmte Funktionen funktionieren möglicherweise nicht wie erwartet. Eine Änderung von `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` kann zum Beispiel dazu führen, dass einige JSP-Dateien nicht kompiliert werden, was letztendlich zu Funktionsverlusten führt.

## Mögliche Lösungen {#solutions}

* Ändern oder entfernen Sie nicht die vier oben genannten Konfigurationen.
* Wenn Konfigurationen geändert wurden, sollten sie auf ihre erwarteten Werte zurückgesetzt werden. Diese Werte sind in den `UMI`-Meldungen angegeben.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
