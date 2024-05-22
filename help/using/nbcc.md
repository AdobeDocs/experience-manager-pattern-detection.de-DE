---
title: NBCC
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 67%

---

# NBCC {#nbcc}

NICHT MEHR UNTERSTÜTZT: Nicht abwärtskompatible Änderungen (ersetzt durch NCC, nicht kompatible Änderungen)

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Nicht abwärtskompatible Änderungen"
>abstract="NBCC identifiziert die Situation, in der einige JCR-Knoten oder -Bundles auf nicht kompatible Weise geändert werden. Es kann sein, dass die Kundin bzw. der Kunde vor einem Upgrade nichts von dieser Änderung weiß. "
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Wesentliche Änderungen – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Versionshinweise – AEM as a Cloud Service"

`NBCC`  Identifiziert die Situation, in der einige JCR-Knoten oder -Bundles auf nicht kompatible Weise geändert werden. Es kann sein, dass die Kundin bzw. der Kunde vor einem Upgrade nichts von dieser Änderung weiß. 

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* Die Funktionalität, die von einer Komponente abhängt, die nicht abwärtskompatible Änderungen verwendet, kann fehlschlagen und möglicherweise nicht richtig aufgelöst werden.
* Einige Funktionen des Programms des Kunden oder einige AEM-Funktionen funktionieren nach einem Upgrade möglicherweise nicht mehr richtig.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, benutzerdefinierten Code zu überprüfen und sicherzustellen, dass nur abwärtskompatible Sling-Komponenten überlagert oder referenziert werden. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Überlagerungen"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Überlagern oder referenzieren Sie nur abwärtskompatible Sling-Komponenten.
* Überlegen Sie, welche Ressourcen aus `/libs` oder Bundles nach einem AEM.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
