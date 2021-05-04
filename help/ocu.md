---
title: OCU
description: Hilfeseite zum Mustererkennungs-Code
exl-id: cb28c727-415d-436c-ab74-cf7f1f34f7c7
translation-type: tm+mt
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 73%

---

# OCU {#ocu}

Verwendung von veraltetem Code

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_overview"
>title="Verwendung von veraltetem Code"
>abstract="OCU identifiziert die Situation, in der einige JCR-Knoten, wie Sling- oder AEM-Komponenten oder API-OSGi-Exporte, auf eine nicht kompatible Weise geändert oder entfernt werden. Es kann sein, dass der Kunde bis zu einem Upgrade von dieser Änderung nichts weiß. Er kann ein Upgrade auf eine nicht kompatible Version erhalten oder es ist überhaupt nicht verfügbar."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de" text="Bemerkenswerte Änderungen - AEM als Cloud Service"

`OCU` steht für die Situation, in der einige JCR-Knoten, z. B. Sling- oder AEM-Komponenten oder API OSGi-Exporte, auf nicht kompatible Weise geändert oder entfernt werden. Es kann sein, dass der Kunde bis zu einem Upgrade von dieser Änderung nichts weiß. Er kann ein Upgrade auf eine nicht kompatible Version erhalten oder es ist überhaupt nicht verfügbar.

Da die alten Versionen standardmäßig nicht installiert sind, funktioniert das Programm des Kunden möglicherweise nicht korrekt.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Funktionalität, die von einer Komponente abhängt, die veraltete Komponenten oder APIs verwendet, kann fehlerhaft sein und wird nach einem Upgrade möglicherweise nicht korrekt aufgelöst.
* Einige Funktionen des Programms des Kunden oder einige AEM-Funktionen funktionieren möglicherweise nicht richtig oder sind nach einem Upgrade nicht mehr aktiv.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_guidance"
>title="Durchführungsleitlinien"
>abstract="Best Practice ist, den Kundencode zu überprüfen und anzupassen, um die neueste Version AEM Komponenten oder APIs zu verwenden. Wenden Sie sich an Adobe Support für Hilfe und Klarstellungen."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="Adobe Experience Manager SDK API"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-Support"

* Kurzfristig: Die Installation des Kompatibilitätspakets könnte helfen.
* Langfristig: Passen Sie den Kunden-Code an, sodass er die neueste Version von AEM-Komponenten oder -APIs verwendet.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
