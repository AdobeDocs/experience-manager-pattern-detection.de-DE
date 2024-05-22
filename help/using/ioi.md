---
title: IOI
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 60%

---

# IOI {#ioi}

Interner Oak-Import

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Interner Oak-Import"
>abstract="IOI-Code identifiziert den Kundeneinsatz interner Oak-Pakete und importiert sie über OSGi. Sie werden ohne eine bestimmte Version exportiert. Oak-Bundles oder AEM Dienste auf niedriger Ebene nutzen sie nur."

`IOI` identifiziert die Verwendung von internen Oak-Packages durch Kundinnen und Kunden und importiert sie über OSGi. Sie werden ohne eine bestimmte Version exportiert. Oak-Bundles oder AEM Dienste auf niedriger Ebene nutzen sie nur.
Einige dieser Bereiche werden von `com.adobe.granite.repository`, wodurch ein Repository für AEM während des Starts eingerichtet wird. Ein weiteres Beispiel ist das Adobe-Bundle `com.adobe.granite.maintenance.oak`, das Oak-Wartungsaufgaben umschließt und bereitstellt.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* In einer zukünftigen AEM werden möglicherweise interne Exporte entfernt, was zu fehlerhaften Abhängigkeiten und inaktiven Bundles führt, die direkt von Oak abhängig sind.
* Die API in internen Exporten kann sich ändern.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Implementierungsleitlinien"
>abstract="Kunden sollten ihren benutzerdefinierten Code überprüfen, um die Verwendung solcher APIs zu erkennen, und sie umstrukturieren, damit sie mit AEM as a Cloud Service kompatibel sind. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Verwenden Sie die Sling Resource-API (oder die JCR-API) anstelle des Zugriffs auf untergeordnetem Niveau.
* Vermeiden Sie es, sich auf interne Packages zu verlassen, die nicht Teil einer öffentlichen API oder SPI sind.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
