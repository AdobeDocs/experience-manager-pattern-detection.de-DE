---
title: LOCP
description: Hilfeseite zum Mustererkennungs-Code
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
translation-type: ht
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: ht
source-wordcount: '203'
ht-degree: 100%

---

# LOCP {#locp}

/libs Überschreiben benutzerdefinierter Pakete

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Überschreiben benutzerdefinierter Pakete"
>abstract="LOCP kennzeichnet die Erkennung eines benutzerdefinierten Pakets, das Inhalte an /libs bereitstellt. Dies ist ein Anti-Muster (außer im Fall von ACLs)."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=de" text="Nachhaltige Aktualisierungen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=de#platform" text="Sling Resource Merger"

`LOCP` kennzeichnet die Erkennung eines benutzerdefinierten Pakets, das Inhalte an `/libs` bereitstellt. Dies ist ein Anti-Muster (außer im Fall von ACLs).

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Der Kunden-Code kann bei allen CFP-, SP- oder größeren AEM-Upgrades gelöscht oder ersetzt werden.
* In einigen Fällen wird der neue Inhalt möglicherweise nicht ordnungsgemäß installiert.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Implementierungsleitlinien"
>abstract="Kunden sollten ihren benutzerdefinierten Code und ihre Pakete überprüfen, um festzustellen, ob der Inhalt unter /libs bereitgestellt wird, und ihn so umgestalten, dass der Inhalt unter /apps überlagert wird, und ihn mit AEM as a Cloud Service kompatibel machen. Wenden Sie sich an den Adobe Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=de#platform" text="Überlagerungen"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Benutzerdefinierte Pakete sollten Inhalte für `/apps` anstatt für `/libs` bereitstellen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
