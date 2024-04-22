---
title: OAUI
description: Mustererkennungscode Hilfeseite .
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 47%

---

# OAUI {#oaui}

OAuth-Benutzerinstanz

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth-Benutzerinstanz"
>abstract="OAUI-Code kennzeichnet das Muster, bei dem mindestens ein OAuth-bezogener konfigurierter Benutzer vorhanden ist, der eine korrekte Migration erfordert. OAuth ist für Benutzer konfiguriert, wenn es einen Unterknoten namens oauth direkt unter einem rep:AuthorizableId-Knoten in der Form /home/user-path/user-node/oauth gibt."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service – Versionshinweise"

OAUI identifiziert das Muster, bei dem mindestens ein OAuth-bezogener konfigurierter Benutzer vorhanden ist, der eine korrekte Migration erfordert.

OAuth ist für Benutzer konfiguriert, wenn ein Unterknoten mit dem Namen `oauth` direkt unter einem `rep:AuthorizableId`-Knoten in der Form von `/home/user-path/user-node/oauth` vorhanden ist.

Ein Beispiel: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Externe Benutzer, die mit OAuth konfiguriert wurden, können sich erst bei Autoren-/Veröffentlichungsinstanzen anmelden, nachdem sie mit dem folgenden Verfahren neu konfiguriert wurden.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Implementierungsleitlinien"
>abstract="Externe Benutzer, die mit OAuth konfiguriert wurden, können sich erst bei Autoren-/Veröffentlichungsinstanzen anmelden, nachdem sie neu konfiguriert wurden, um mit AEM as a Cloud Service kompatibel zu sein. AEM as a Cloud Service bietet IMS-Authentifizierungsunterstützung nur für Autoren-, Admin- und Entwickler-Benutzer und SAML-basierte Integration für die Veröffentlichungsumgebungen. Wenden Sie sich an den Adobe Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support" text="IMS-Unterstützung – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/personalization/user-and-group-sync-for-publish-tier#integration-with-an-idp" text="SAML-Integration – Veröffentlichen"

* Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, wenn Sie Optionen für die Benutzermigration besprechen müssen.
* Wenden Sie sich an den [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) um Klarstellungen zu erhalten oder um Bedenken auszuräumen.
