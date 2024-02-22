---
title: OAUI
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '231'
ht-degree: 100%

---

# OAUI {#oaui}

OAuth-Benutzerinstanz

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth-Benutzerinstanz"
>abstract="OAUI-Code kennzeichnet das Muster, bei dem mindestens ein OAuth-bezogener konfigurierter Benutzer vorhanden ist, der eine korrekte Migration erfordert. OAuth ist für Benutzer konfiguriert, wenn es einen Unterknoten namens oauth direkt unter einem rep:AuthorizableId-Knoten in der Form /home/user-path/user-node/oauth gibt."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=de" text="AEM as a Cloud Service – Versionshinweise"

`OAUI` kennzeichnet das Muster, bei dem mindestens ein OAuth-bezogener konfigurierter Benutzer vorhanden ist, der eine korrekte Migration erfordert.

OAuth ist für Benutzer konfiguriert, wenn ein Unterknoten mit dem Namen `oauth` direkt unter einem `rep:AuthorizableId`-Knoten in der Form von `/home/user-path/user-node/oauth` vorhanden ist.

Ein Beispiel: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Externe Benutzende, die mit OAuth konfiguriert wurden, können sich erst dann in Autoren-/Veröffentlichungsinstanzen anmelden, wenn sie mit dem folgenden Verfahren neu konfiguriert wurden.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Implementierungsleitlinien"
>abstract="Externe Benutzer, die mit OAuth konfiguriert sind, können sich nicht bei Autoren-/Veröffentlichungsinstanzen anmelden, bis diese neu konfiguriert wurden, damit sie mit AEM as a Cloud Service kompatibel sind. AEM as a Cloud Service bietet IMS-Authentifizierungsunterstützung nur für Autoren-, Administrator- und Entwicklungsbenutzer und SAML-basierte Integration für die Publishing-Umgebungen. Wenden Sie sich an den Adobe Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=de" text="IMS-Unterstützung – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/personalization/user-and-group-sync-for-publish-tier.html?lang=de#integration-with-an-idp" text="SAML-Integration – Veröffentlichen"

* Wenden Sie sich an Ihren Adobe-Kundenbetreuer, um die Optionen für die Benutzermigration zu besprechen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
