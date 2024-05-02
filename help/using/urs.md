---
title: URS
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 74%

---

# URS {#urs}

Nicht unterstützte Repository-Struktur

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Nicht unterstützte Repository-Struktur"
>abstract="URS identifiziert Fälle nicht unterstützter Repository-Struktur sowie Knotencharakteristika. Dadurch werden Informationen zur Vermeidung von Konflikten zwischen AEM-Produkt-Code und Kunden-Code, zur Umstrukturierung von Inhalten aus /etc in andere Ordner im Repository und mehr angezeigt."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Repository-Neustrukturierung"

## Hintergrund {#background}

`URS`  Identifiziert Fälle nicht unterstützter Repository-Struktur und Knotenmerkmale. Ab AEM 6.4 wurden Leitlinien für die Umstrukturierung von Repository-Inhalten festgelegt. Durch die klare Abgrenzung von Hierarchien für AEM-Produkt-Code und Kunden-Code und die Vermeidung von Konflikten zwischen ihnen werden Inhalte aus `/etc` in andere Ordner im Repository umstrukturiert, wobei die folgenden allgemeinen Regeln befolgt werden:

* AEM Produktcode wird immer in `/libs`, die nicht durch benutzerdefinierten Code überschrieben werden dürfen.
* Benutzerspezifischer Code sollte in `/apps`, `/content`, und `/conf`.
* Es wird dringend empfohlen, dass diese Richtlinien für AEM as a Cloud Service befolgt werden.

Um die spezifischen Arten von Repository-Problemen, die behandelt werden sollten, zu unterscheiden, werden folgende Untertypen verwendet:

* `clientlibs.location`: Eine Client-Bibliothek, die auf `/etc` über den Pfad verweist.
* `file.location`: Eine Datei unter `/etc`, die seit der Installation geändert wurde.
* `node.location`: Ein Knoten, unter `/etc`, der seit der Installation geändert wurde.
* `workflow.location`: Ein Workflow-Modell oder Starter unter `/etc/workflow`.
* `package.structure`: Ein Package, das sowohl veränderlichen als auch unveränderlichen Inhalt enthält.
* `node.size`: Ein Knoten mit nicht unterstützter Größe.

## Mögliche Auswirkungen und Risiken {#implications-and-risks}

* Benutzerdefinierter Code, der sich auf ältere Pfade stützt, kann unerwünschtes Verhalten verursachen und die Produktfunktionalität beeinträchtigen.
* Pakete, die sowohl veränderliche als auch unveränderliche Inhalte enthalten, können während der Bereitstellung wahrscheinlich Probleme verursachen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, Ihr Code-Projekt zu überprüfen. Best Practice ist es, Ihr Code-Projekt zu überprüfen und sicherzustellen, dass es den Richtlinien für die AEM-Projektstruktur entspricht, und Code zu vermeiden, der auf älteren/nicht unterstützten Repository-Pfaden basiert, die unerwünschtes Verhalten in AEM as a Cloud Service verursachen können. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="Richtlinien zur Struktur von AEM-Projekten"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Eine Anleitung zur Vorbereitung auf AEM as a Cloud Service finden Sie unter [Repository-Restrukturierung](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring).
* Siehe auch [AEM Projektstruktur](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) , wenn Sie mehr über veränderliche und unveränderliche Bereiche des Repositorys erfahren möchten.
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
* Verwenden Sie die [Repository Modernizer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools) bestehende Projektpakete neu zu strukturieren, indem Inhalt und Code in separate Pakete aufgeteilt werden, um mit der für Adobe Experience Manager as a Cloud Service definierten Projektstruktur kompatibel zu sein.
