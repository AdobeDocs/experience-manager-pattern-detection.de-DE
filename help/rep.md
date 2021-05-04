---
title: REP
description: Hilfeseite zum Mustererkennungs-Code
exl-id: e788deba-a301-404f-8e90-51f721409e69
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 86%

---

# [!DNL REP] {#rep}

Replikationsagent

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Replikationsagent"
>abstract="REP identifiziert aktivierte Replizierungsagenten. Diese werden aufgrund potenzieller Probleme gemeldet, die beim Upgrade auf AEM as a Cloud Service behoben werden sollten. AEM as a Cloud Service verwendet Sling Content Distribution, um Inhalte von der Autorenumgebung an Veröffentlichungsumgebungen zu verteilen. Dies geschieht außerhalb der AEM-Laufzeit mithilfe des Pipeline-Service von Adobe I/O. Dieser wird automatisch in der bereitgestellten AEM as a Cloud Service-Umgebung konfiguriert."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents" text="Bemerkenswerte Änderungen - AEM als Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents" text="Entwicklungsrichtlinien"

`REP` kennzeichnet für aktivierte Replikationsagenten. Diese werden aufgrund potenzieller Probleme gemeldet, die beim Upgrade auf AEM as a Cloud Service behoben werden sollten.

AEM as a Cloud Service verwendet [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html), um Inhalte von der Autorenumgebung an Veröffentlichungsumgebungen zu verteilen. Dies geschieht außerhalb der AEM-Laufzeit mithilfe des Pipeline-Service von Adobe I/O. Dieser wird automatisch in der bereitgestellten AEM as a Cloud Service-Umgebung konfiguriert.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Konfiguration der Replikation hat sich mit AEM as a Cloud Service geändert. Alle aktuellen Replikationsagenten sollten überprüft werden, um festzustellen, welche durch die Standardfunktionalität ersetzt werden, welche Konfigurationen in den Code verschoben werden müssen und welche nicht unterstützt werden.
* Jede Verwendung von Replikationsagenten in benutzerdefiniertem Code oder Workflows sollte beim Upgrade auf AEM as a Cloud Service überprüft werden.
* Die umgekehrte Replikation wird in AEM as a Cloud Service zunächst nicht unterstützt.
* Es ist nicht erforderlich, einen separaten Dispatcher-Flush-Agent zu konfigurieren. Dieser wird automatisch in der AEM as a Cloud Service-Umgebung konfiguriert.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Durchführungsleitlinien"
>abstract="Best Practice ist, benutzerdefinierte Funktionen direkt von Replizierungsagenten abhängig zu überprüfen, zu refaktorieren und zu optimieren und sie mit AEM als Cloud Service kompatibel zu machen. Support zur Adobe für Hilfe und Klarstellungen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication" text="Replikation - AEM als Cloud Service"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-Support"

* Siehe die [Entwicklungsrichtlinien](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=de#no-reverse-replication-agents) für AEM as a Cloud Service und die Versionshinweise für [Replikationsagenten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de#replication-agents).
* Um Geschäftsaufgaben durchzuführen, sollten Sie Funktionen, die direkt von Replikationsagenten abhängig sind, überprüfen, umarbeiten und optimieren.
* Sehen Sie, wie sich die Bereitstellung in AEM as a Cloud Service auf die [Replikation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=de#replication) auswirkt.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
