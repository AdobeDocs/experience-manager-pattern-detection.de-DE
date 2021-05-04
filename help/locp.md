---
title: LOCP
description: Hilfeseite zum Mustererkennungs-Code
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 55%

---

# LOCP {#locp}

/libs Überschreiben benutzerdefinierter Pakete

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Überschreiben benutzerdefinierter Pakete"
>abstract="LOCP identifiziert die Erkennung eines benutzerdefinierten Pakets, das Inhalte an /libs liefert. Dies ist ein Anti-Muster (außer im Fall von ACLs)."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=de" text="Nachhaltige Aktualisierungen "
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html#platform" text="Sling Resource Merger"

`LOCP` steht für die Erkennung eines benutzerdefinierten Pakets, das Inhalte an `/libs` bereitstellt. Dies ist ein Anti-Muster (außer im Fall von ACLs).

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Der Kunden-Code kann bei allen CFP-, SP- oder größeren AEM-Upgrades gelöscht oder ersetzt werden.
* In einigen Fällen wird der neue Inhalt möglicherweise nicht ordnungsgemäß installiert.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Durchführungsleitlinien"
>abstract="Kunden sollten ihren benutzerspezifischen Code und ihre Pakete überprüfen, um herauszufinden, ob Inhalte an /libs bereitgestellt werden, und ihn neu umgestalten, um den Inhalt unter /apps zu überlagern und ihn mit AEM als Cloud Service kompatibel zu machen. Support zur Adobe für Hilfe und Klarstellungen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Überlagerungen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-Support"

* Benutzerdefinierte Pakete sollten Inhalte für `/apps` anstatt für `/libs` bereitstellen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
