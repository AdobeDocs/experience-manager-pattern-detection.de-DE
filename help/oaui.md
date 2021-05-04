---
title: OAUI
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 48%

---

# OAUI {#oaui}

OAuth-Benutzerinstanz

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth-Benutzerinstanz"
>abstract="OAUI-Code identifiziert das Muster, bei dem mindestens ein OAuth-bezogener konfigurierter Benutzer vorhanden ist, der eine korrekte Migration erfordert. OAuth ist für Benutzer konfiguriert, wenn sich eine Unterknoten namens oauth direkt unter einem Knoten rep:AuthorizableId im Format /home/user-path/user-node/oauth befindet"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de" text="AEM als Cloud Service - Versionshinweise"

`OAUI` steht für das Muster, bei dem mindestens ein OAuth-bezogener konfigurierter Benutzer vorhanden ist, der eine korrekte Migration erfordert.

OAuth ist für Benutzer konfiguriert, wenn ein Unterknoten mit dem Namen `oauth` direkt unter einem `rep:AuthorizableId`-Knoten in der Form von `/home/user-path/user-node/oauth` vorhanden ist.

Ein Beispiel: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Externe Benutzer, die mit OAuth konfiguriert wurden, können sich erst dann in Autoren-/Veröffentlichungsinstanzen anmelden, wenn sie mit dem folgenden Verfahren neu konfiguriert wurden.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Durchführungsleitlinien"
>abstract="Externe Benutzer, die mit OAuth konfiguriert wurden, können sich erst dann in Autor-/Veröffentlichungsinstanzen anmelden, wenn sie neu konfiguriert wurden, um als Cloud Service mit AEM kompatibel zu sein. AEM als Cloud Service-Angebote IMS-Authentifizierungsunterstützung nur für Autoren-, Admin- und Dev-Benutzer und SAML-basierte Integration für die Veröffentlichungs-Umgebung. Support zur Adobe für Hilfe und Klarstellungen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=de" text="IMS-Unterstützung - AEM als Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/personalization/user-and-group-sync-for-publish-tier.html?lang=en#integration-with-an-idp" text="SAML-Integration - Veröffentlichen"

* Wenden Sie sich an Ihren Adobe-Kundenbetreuer, um die Optionen für die Benutzermigration zu besprechen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
