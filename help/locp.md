---
title: LOCP
description: Hilfeseite zur Mustererkennung
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 1%

---


# LOCP {#locp}

/libs Überschreiben benutzerdefinierter Pakete

## Hintergrund {#background}

`LOCP` identifiziert die Erkennung eines benutzerdefinierten Pakets, das Inhalte an  `/libs`bereitstellt. Dies ist ein Anti-Muster (außer im Fall von ACLs).

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Der Kundencode kann bei allen CFP-, SP- oder AEM-Upgrades gelöscht oder ersetzt werden.
* In einigen Fällen wird der neue Inhalt möglicherweise nicht ordnungsgemäß installiert.

## Mögliche Lösungen {#solutions}

* Kundenpakete sollten Inhalte für `/apps` anstatt für `/libs` bereitstellen.
* Bitte wenden Sie sich an unser [AEM Supportteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
