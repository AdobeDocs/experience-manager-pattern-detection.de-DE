---
title: OAUI
description: Hilfeseite zum Mustererkennungs-Code
translation-type: ht
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: ht
source-wordcount: '107'
ht-degree: 100%

---


# OAUI {#oaui}

OAuth-Benutzerinstanz

## Hintergrund {#background}

`OAUI` steht für das Muster, bei dem mindestens ein OAuth-bezogener konfigurierter Benutzer vorhanden ist, der eine korrekte Migration erfordert.

OAuth ist für Benutzer konfiguriert, wenn ein Unterknoten mit dem Namen `oauth` direkt unter einem `rep:AuthorizableId`-Knoten in der Form von `/home/user-path/user-node/oauth` vorhanden ist.

Ein Beispiel: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Externe Benutzer, die mit OAuth konfiguriert wurden, können sich erst dann in Autoren-/Veröffentlichungsinstanzen anmelden, wenn sie mit dem folgenden Verfahren neu konfiguriert wurden.

## Mögliche Lösungen {#solutions}

* Wenden Sie sich an Ihren Adobe-Kundenbetreuer, um die Optionen für die Benutzermigration zu besprechen.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
