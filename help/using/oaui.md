---
title: OAUI
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 88%

---

# OAUI {#oaui}

OAuth-Benutzerinstanz

## Hintergrund {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth-Benutzerinstanz"
>abstract="OAUI-Code kennzeichnet das Muster, bei dem mindestens ein OAuth-bezogener konfigurierter Benutzer vorhanden ist, der eine korrekte Migration erfordert. OAuth wird für Benutzer konfiguriert, wenn ein Unterknoten namens OAuth direkt unter einem Knoten rep:AuthorizableId im Format /home/user-path/user-node/oauth vorhanden ist."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service – Versionshinweise"

`OAUI` identifiziert das Muster, bei dem es mindestens eine OAuth-bezogene konfigurierte Person gibt, die korrekt migriert werden muss.

OAuth ist für Benutzer konfiguriert, wenn ein Unterknoten mit dem Namen `oauth` direkt unter einem `rep:AuthorizableId`-Knoten in der Form von `/home/user-path/user-node/oauth` vorhanden ist.

Ein Beispiel: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* Externe Benutzende, die mit OAuth konfiguriert wurden, können sich erst dann in Autoren-/Veröffentlichungsinstanzen anmelden, sobald diese mit dem folgenden Verfahren neu konfiguriert wurden.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Implementierungsleitlinien"
>abstract="Externe Benutzende, die mit OAuth konfiguriert sind, können sich erst dann in Autoren-/Veröffentlichungsinstanzen anmelden, sobald diese so neu konfiguriert wurden, dass sie mit AEM as a Cloud Service kompatibel sind. AEM as a Cloud Service bietet IMS-Authentifizierungsunterstützung nur für Autoren-, Admin- und Entwicklungsbenutzende und SAML-basierte Integration für die Veröffentlichungsumgebungen. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/security/ims-support" text="IMS-Unterstützung – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/authoring/personalization/user-and-group-sync-for-publish-tier#integration-with-an-idp" text="SAML-Integration – Veröffentlichen"

* Wenden Sie sich an den Adobe-Support, um die Optionen für die Benutzermigration zu besprechen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
