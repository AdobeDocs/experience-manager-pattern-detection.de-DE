---
title: OCU
description: Mustererkennungscode Hilfeseite.
exl-id: cb28c727-415d-436c-ab74-cf7f1f34f7c7
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 64%

---

# OCU {#ocu}

NICHT MEHR UNTERSTÜTZT: Veraltete Code-Nutzung (ersetzt durch OU, veraltete Verwendung)

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_overview"
>title="Verwendung von veraltetem Code"
>abstract="OCU kennzeichnet die Situation, in der einige JCR-Knoten, z. B. Sling- oder AEM-Komponenten oder API OSGi-Exporte, auf nicht kompatible Weise geändert oder entfernt werden. Dem Kunden ist diese Änderung möglicherweise vor einem Upgrade nicht bekannt. Er kann ein Upgrade auf eine nicht kompatible Version erhalten oder es ist überhaupt nicht verfügbar."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Wesentliche Änderungen – AEM as a Cloud Service"

`OCU`  Gibt die Situation an, in der einige JCR-Knoten, wie z. B. Sling- oder AEM-Komponenten oder API-OSGi-Exporte, auf nicht kompatible Weise geändert oder entfernt werden. Dem Kunden ist diese Änderung möglicherweise vor einem Upgrade nicht bekannt. Er kann ein Upgrade auf eine nicht kompatible Version erhalten oder es ist überhaupt nicht verfügbar.

Da die alten Versionen standardmäßig nicht installiert sind, funktioniert das Programm des Kunden möglicherweise nicht korrekt.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Funktionalität, die von einer Komponente abhängt, die veraltete Komponenten oder APIs verwendet, kann fehlerhaft sein und wird nach einem Upgrade möglicherweise nicht korrekt aufgelöst.
* Einige Funktionen des Programms des Kunden oder einige AEM-Funktionen funktionieren möglicherweise nicht richtig oder sind nach einem Upgrade nicht mehr aktiv.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, den Kunden-Code zu überprüfen und anzupassen, um die neueste Version der AEM-Komponenten oder -APIs zu verwenden. Wenden Sie sich an den Adobe-Support , um Hilfe oder Erläuterungen zu erhalten."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="Adobe Experience Manager SDK API"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Kurzfristig: Die Installation des Kompatibilitätspakets kann helfen.
* Langfristig: Passen Sie den Kundencode an, um die neueste Version AEM Komponenten oder APIs zu verwenden.
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
