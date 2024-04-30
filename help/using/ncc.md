---
title: NCC
description: Mustererkennungscode Hilfeseite.
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 82%

---

# NCC {#ncc}

Nicht kompatible Änderungen

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Nicht kompatible Änderungen"
>abstract="NCC kennzeichnet die Situation, in der einige JCR-Knoten oder -Bundles in einer nicht kompatiblen Weise geändert werden. Es kann sein, dass die Kundin bzw. der Kunde vor einem Upgrade von dieser Änderung nichts weiß."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Wesentliche Änderungen – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Versionshinweise – AEM as a Cloud Service"

`NCC`  Identifiziert die Situation, in der einige JCR-Knoten oder -Bundles auf nicht kompatible Weise geändert werden. Es kann sein, dass die Kundin bzw. der Kunde vor einem Upgrade von dieser Änderung nichts weiß.

## Mögliche Implikationen und Risiken {#implications-and-risks}

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
* Erwägen Sie die Anpassung von Ressourcen, die nach einem AEM-Upgrade aus `/libs` oder Bundles stammen.
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
