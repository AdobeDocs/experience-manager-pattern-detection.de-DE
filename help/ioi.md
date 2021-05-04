---
title: IOI
description: Hilfeseite zum Mustererkennungs-Code
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 78%

---

# IOI {#ioi}

Interner Oak-Import

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Interner Oak-Import"
>abstract="IOI-Code identifiziert die Verwendung interner Oak-Pakete durch den Kunden und importiert sie über OSGi. Sie werden normalerweise ohne eine bestimmte Version exportiert und sind nur für den Verbrauch durch andere Oak-Bundles oder AEM-Services auf untergeordnetem Niveau vorgesehen."

`IOI` Steht für die Verwendung interner Oak-Packages durch den Kunden und den Import über OSGi. Sie werden normalerweise ohne eine bestimmte Version exportiert und sind nur für den Verbrauch durch andere Oak-Bundles oder AEM-Services auf untergeordnetem Niveau vorgesehen.

Einige davon werden von `com.adobe.granite.repository` verwendet, das während des Starts ein Repository für AEM einrichtet. Ein weiteres Beispiel ist das Adobe-Bundle `com.adobe.granite.maintenance.oak`, das Oak-Wartungsaufgaben umschließt und bereitstellt.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* In einer zukünftigen AEM-Version könnten interne Exporte entfernt werden, was zu unterbrochenen Abhängigkeiten und inaktiven Bundles führt, die direkt von Oak abhängen.
* Die API in internen Exporten kann sich ändern.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Durchführungsleitlinien"
>abstract="Kunden sollten ihren benutzerspezifischen Code überprüfen, um die Verwendung solcher APIs zu identifizieren und sie neu zu fakturieren, damit sie mit AEM als Cloud Service kompatibel sind. Support zur Adobe für Hilfe und Klarstellungen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-Support"

* Verwenden Sie die Sling Resource-API (oder die JCR-API) anstelle des Zugriffs auf untergeordnetem Niveau.
* Vermeiden Sie es, sich auf interne Packages zu verlassen, die nicht Teil einer öffentlichen API oder SPI sind.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
