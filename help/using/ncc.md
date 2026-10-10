---
title: NCC
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 100%
---
# NCC {#ncc}

Nicht kompatible Änderungen

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Nicht kompatible Änderungen"
>abstract="NCC kennzeichnet die Situation, in der einige JCR-Knoten oder -Pakete in einer nicht kompatiblen Weise geändert werden. Es kann sein, dass die Kundin bzw. der Kunde vor einem Upgrade nichts von dieser Änderung weiß."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Wesentliche Änderungen – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Versionshinweise – AEM as a Cloud Service"

`NCC` identifiziert die Situation, in der einige JCR-Knoten oder -Pakete in einer nicht kompatiblen Weise geändert werden. Es kann sein, dass die Kundin bzw. der Kunde vor einem Upgrade nichts von dieser Änderung weiß.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* Die Funktionen, die von einer Komponente abhängen, die nicht kompatible Änderungen verwendet, können fehlerhaft sein und möglicherweise nicht korrekt aufgelöst werden.
* Einige Funktionen des Programms des Kunden oder einige AEM-Funktionen funktionieren nach einem Upgrade möglicherweise nicht mehr richtig.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, benutzerdefinierten Code zu überprüfen und sicherzustellen, dass nur kompatible Sling-Komponenten überlagert oder referenziert werden. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Überlagerungen"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Überlagern oder referenzieren Sie nur kompatible Sling-Komponenten.
* Erwägen Sie die Anpassung von Ressourcen, die nach einem AEM-Upgrade aus `/libs` oder aus Paketen stammen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
