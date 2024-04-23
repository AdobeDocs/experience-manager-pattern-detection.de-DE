---
title: REP
description: Mustererkennungscode Hilfeseite.
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 74%

---

# [!DNL REP] {#rep}

Replikationsagent

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Replikationsagent"
>abstract="REP kennzeichnet aktivierte Replikationsagenten. Diese werden aufgrund potenzieller Probleme gemeldet, die beim Upgrade auf AEM as a Cloud Service behoben werden sollten. AEM as a Cloud Service verwendet Sling Content Distribution, um Inhalte von der Autorenumgebung an Veröffentlichungsumgebungen zu verteilen. Dies erfolgt außerhalb der AEM Laufzeit mithilfe des Pipeline-Diensts von Adobe I/O Runtime auf Adobe Developer. Dies wird automatisch in der bereitgestellten AEM as a Cloud Service Umgebung konfiguriert."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents" text="Wesentliche Änderungen – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents" text="Entwicklungsrichtlinien"

REP kennzeichnet aktivierte Replikationsagenten. Diese werden aufgrund potenzieller Probleme gemeldet, die beim Upgrade auf AEM as a Cloud Service behoben werden sollten.

Um die verschiedenen Arten von Informationen zu unterscheiden, werden folgende Untertypen verwendet:

* `forward.replication`: Identifizieren Sie die aktivierten Agenten für die Vorwärtsreplikation.
* `reverse.replication`: Identifizieren Sie die aktivierten Agenten für Rückwärtsreplikation.
* `standard.replication.agent.modification`: Identifizieren Sie die aktivierten standardmäßigen Replikationsagenten, die geändert werden.
* `custom.replication.agent.detection`: Identifizieren Sie die aktivierten benutzerdefinierten Replikationsagenten.

AEM as a Cloud Service verwendet [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html), um Inhalte von der Autorenumgebung an Veröffentlichungsumgebungen zu verteilen. Dies erfolgt außerhalb der AEM Laufzeit mithilfe des Pipeline-Diensts von Adobe I/O Runtime auf Adobe Developer. Dies wird automatisch in der bereitgestellten AEM as a Cloud Service Umgebung konfiguriert.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Konfiguration der Replikation hat sich mit AEM as a Cloud Service geändert. Alle aktuellen Replikationsagenten sollten überprüft werden, um festzustellen, welche durch die Standardfunktionalität ersetzt werden, welche Konfigurationen in den Code verschoben werden müssen und welche nicht unterstützt werden.
* Jede Verwendung von Replikationsagenten in benutzerdefiniertem Code oder Workflows sollte beim Upgrade auf AEM as a Cloud Service überprüft werden.
* Die umgekehrte Replikation wird in AEM as a Cloud Service zunächst nicht unterstützt.
* Es ist nicht erforderlich, einen separaten Dispatcher-Flush-Agenten zu konfigurieren. Dieser wird automatisch in der AEM as a Cloud Service-Umgebung konfiguriert.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, benutzerdefinierte Funktionalität, die direkt von Replikationsagenten abhängt, zu überprüfen, zu refaktorisieren und zu optimieren und mit AEM as a Cloud Service kompatibel zu machen. Wenden Sie sich an den Adobe-Support , um Hilfe oder Erläuterungen zu erhalten."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication" text="Replikation – AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Siehe die [Entwicklungsrichtlinien](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents) für AEM as a Cloud Service und die Versionshinweise für [Replikationsagenten](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents).
* Um Geschäftsaufgaben durchzuführen, sollten Sie Funktionen, die direkt von Replikationsagenten abhängig sind, überprüfen, umarbeiten und optimieren.
* Sehen Sie, wie sich die Bereitstellung in AEM as a Cloud Service auf die [Replikation](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication) auswirkt.
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
