---
title: NBCC
description: Hilfeseite zum Mustererkennungs-Code
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 100%

---

# NBCC {#nbcc}

NICHT MEHR UNTERSTÜTZT: Nicht abwärtskompatible Änderungen (ersetzt durch NCC, nicht kompatible Änderungen)

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Nicht abwärtskompatible Änderungen"
>abstract="NBCC kennzeichnet die Situation, in der einige JCR-Knoten oder -Bundles in einer nicht kompatiblen Weise geändert werden. Es kann sein, dass der Kunde bis zu einem Upgrade von dieser Änderung nichts weiß."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de" text="Wesentliche Änderungen – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de" text="Versionshinweise – AEM as a Cloud Service"

`NBCC` kennzeichnet die Situation, in der einige JCR-Knoten oder -Bundles in einer nicht kompatiblen Weise geändert werden. Es kann sein, dass der Kunde bis zu einem Upgrade von dieser Änderung nichts weiß.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Funktionalität, die von einer Komponente abhängt, die nicht abwärtskompatible Änderungen verwendet, kann fehlerhaft sein und möglicherweise nicht korrekt aufgelöst werden.
* Einige Funktionen des Programms des Kunden oder einige AEM-Funktionen funktionieren nach einem Upgrade möglicherweise nicht mehr richtig.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, benutzerdefinierten Code zu überprüfen und sicherzustellen, dass nur abwärtskompatible Sling-Komponenten überlagert oder referenziert werden. Wenden Sie sich an den Adobe Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=de#platform" text="Überlagerungen"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Überlagern oder referenzieren Sie nur abwärtskompatible Sling-Komponenten.
* Erwägen Sie die Anpassung von Ressourcen, die nach einem AEM-Upgrade aus `/libs` oder Bundles stammen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
