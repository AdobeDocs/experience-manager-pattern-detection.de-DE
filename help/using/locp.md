---
title: LOCP
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 100%

---

# LOCP {#locp}

/libs überschreiben benutzerdefinierter Pakete

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs überschreiben benutzerdefinierter Pakete"
>abstract="LOCP kennzeichnet die Erkennung eines benutzerdefinierten Pakets, das Inhalte an `/libs` sendet. Dies ist ein Anti-Muster (außer, wenn es sich um ACLs handelt)."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Nachhaltige Aktualisierungen"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sling Resource Merger"

`LOCP` identifiziert die Erkennung eines benutzerdefinierten Pakets, das Inhalte an `/libs` bereitstellt. Dies ist ein Anti-Muster (außer im Fall von ACLs).

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* Der Kunden-Code kann bei allen CFP-, SP- oder größeren AEM-Upgrades gelöscht oder ersetzt werden.
* In einigen Fällen wird der neue Inhalt möglicherweise nicht ordnungsgemäß installiert.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Implementierungsleitlinien"
>abstract="Kundinnen und Kunden sollten ihren benutzerdefinierten Code und ihre Pakete überprüfen, um festzustellen, ob Inhalte an `/libs` übermittelt werden.  Falls erforderlich, überarbeiten Sie ihn, um den Inhalt unter /apps zu überlagern, und machen Sie ihn mit AEM as a Cloud Service kompatibel. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Überlagerungen"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Benutzerdefinierte Pakete sollten Inhalte für `/apps` anstatt für `/libs` bereitstellen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
