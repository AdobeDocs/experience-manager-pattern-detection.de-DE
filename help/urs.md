---
title: URS
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 78%

---

# URS {#urs}

Nicht unterstützte Repository-Struktur

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Nicht unterstützte Repository-Struktur"
>abstract="URS identifiziert Fälle nicht unterstützter Repository-Struktur. Dadurch werden Informationen überdeckt, um Konflikte zwischen AEM Produktcode und Kundencode zu vermeiden, Inhalte, die aus /etc in andere Ordner im Repository umstrukturiert werden, und mehr."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html" text="Repository-Neustrukturierung"

## Hintergrund {#background}

`URS` steht für Fälle nicht unterstützter Repository-Struktur. Ab AEM 6.4 wurden Leitlinien für die Umstrukturierung von Repository-Inhalten festgelegt. Durch die klare Abgrenzung von Hierarchien für AEM-Produkt-Code und Kunden-Code und die Vermeidung von Konflikten zwischen ihnen werden Inhalte aus `/etc` in andere Ordner im Repository umstrukturiert, wobei die folgenden allgemeinen Regeln befolgt werden:

* AEM-Produkt-Code wird immer in `/libs` platziert und darf nicht durch benutzerdefinierten Code überschrieben werden. Benutzerspezifischer Code sollte in `/apps`, `/content` und `/conf` platziert werden.
* Es wird dringend empfohlen, dass diese Richtlinien für AEM as a Cloud Service befolgt werden.

Um die spezifischen Arten von Repository-Problemen, die behandelt werden sollten, zu unterscheiden, werden folgende Untertypen verwendet:
* `clientlibs.location`: Eine Client-Bibliothek, die auf `/etc` über den Pfad verweist.
* `file.location`: Eine Datei unter `/etc`, die seit der Installation geändert wurde.
* `node.location`: Ein Knoten, unter `/etc`, der seit der Installation geändert wurde.
* `workflow.location`: Ein Workflow-Modell oder Starter unter `/etc/workflow`.
* `package.structure`: Ein Package, das sowohl veränderlichen als auch unveränderlichen Inhalt enthält.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Benutzerdefinierter Code, der sich auf ältere Pfade stützt, kann unerwünschtes Verhalten verursachen und die Produktfunktionalität beeinträchtigen.
* Packages, die sowohl veränderliche als auch unveränderliche Inhalte enthalten, werden wahrscheinlich Probleme bei der Implementierung verursachen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Durchführungsleitlinien"
>abstract="Es empfiehlt sich, das Codeprojekt zu überprüfen und sicherzustellen, dass es den AEM Richtlinien für die Projektstruktur entspricht, und zu vermeiden, dass Code auf älteren/nicht unterstützten Repository-Pfaden basiert, der in AEM als Cloud Service unerwünschtes Verhalten hervorrufen kann. Support zur Adobe für Hilfe und Klarstellungen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html" text="AEM Leitlinien für die Projektstruktur"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-Support"

* Eine Anleitung zur Vorbereitung auf AEM as a Cloud Service finden Sie unter [Repository-Neustrukturierung](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html?lang=de).
* Weitere Informationen zu veränderlichen und unveränderlichen Bereichen des Repositorys finden Sie unter [AEM-Projektstruktur](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
* Nutzen Sie den [Repository-Modernisierer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html?lang=de#refactoring-tools), um vorhandene Projekt-Packages umzustrukturieren, indem Sie Inhalte und Code in einzelne Packages trennen, damit sie mit der für Adobe Experience Manager as a Cloud Service definierten Projektstruktur kompatibel sind.
