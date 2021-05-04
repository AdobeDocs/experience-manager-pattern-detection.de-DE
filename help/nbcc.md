---
title: NBCC
description: Hilfeseite zum Mustererkennungs-Code
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 69%

---

# NBCC {#nbcc}

Nicht abwärtskompatible Änderungen

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Nicht abwärtskompatible Änderungen"
>abstract="NBCC identifiziert die Situation, in der einige JCR-Knoten oder -Bundles auf nicht kompatible Weise geändert werden. Es kann sein, dass der Kunde bis zu einem Upgrade von dieser Änderung nichts weiß."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=de" text="Bemerkenswerte Änderungen - AEM als Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de" text="Versionshinweise - AEM als Cloud Service"

`NBCC` steht für die Situation, in der einige JCR-Knoten oder -Bundles in einer nicht kompatiblen Weise geändert werden. Es kann sein, dass der Kunde bis zu einem Upgrade von dieser Änderung nichts weiß.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Die Funktionalität, die von einer Komponente abhängt, die nicht abwärtskompatible Änderungen verwendet, kann fehlerhaft sein und möglicherweise nicht korrekt aufgelöst werden.
* Einige Funktionen des Programms des Kunden oder einige AEM-Funktionen funktionieren nach einem Upgrade möglicherweise nicht mehr richtig.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Durchführungsleitlinien"
>abstract="Best Practice ist die Überprüfung des benutzerdefinierten Codes und stellen sicher, dass nur abwärtskompatible Sling-Komponenten überlagert oder referenziert werden. Support zur Adobe für Hilfe und Klarstellungen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Überlagerungen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-Support"

* Überlagern oder referenzieren Sie nur abwärtskompatible Sling-Komponenten.
* Erwägen Sie die Anpassung von Ressourcen, die nach einem AEM-Upgrade aus `/libs` oder Bundles stammen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
