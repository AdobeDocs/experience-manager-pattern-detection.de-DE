---
title: IOI
description: Mustererkennungscode Hilfeseite.
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 68%

---

# IOI {#ioi}

Interner Oak-Import

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Interner Oak-Import"
>abstract="IOI-Code kennzeichnet die Verwendung interner Oak-Packages durch den Kunden und den Import über OSGi. Sie werden ohne eine bestimmte Version exportiert und sind nur für den Verbrauch durch andere Oak-Pakete oder einfache AEM bestimmt."

`IOI`  Identifiziert den Kundeneinsatz interner Oak-Pakete und importiert sie über OSGi. Sie werden ohne eine bestimmte Version exportiert und sind nur für den Verbrauch durch andere Oak-Pakete oder einfache AEM bestimmt.

Einige davon werden von `com.adobe.granite.repository` verwendet, das während des Starts ein Repository für AEM einrichtet. Ein weiteres Beispiel ist das Adobe-Bundle `com.adobe.granite.maintenance.oak`, das Oak-Wartungsaufgaben umschließt und bereitstellt.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* In einer zukünftigen AEM-Version könnten interne Exporte entfernt werden, was zu unterbrochenen Abhängigkeiten und inaktiven Bundles führt, die direkt von Oak abhängen.
* Die API in internen Exporten kann sich ändern.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Implementierungsleitlinien"
>abstract="Kunden sollten ihren benutzerdefinierten Code überprüfen, um die Verwendung solcher APIs zu erkennen, und sie umstrukturieren, damit sie mit AEM as a Cloud Service kompatibel sind. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Verwenden Sie die Sling Resource-API (oder die JCR-API) anstelle des Zugriffs auf untergeordnetem Niveau.
* Vermeiden Sie es, sich auf interne Packages zu verlassen, die nicht Teil einer öffentlichen API oder SPI sind.
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
