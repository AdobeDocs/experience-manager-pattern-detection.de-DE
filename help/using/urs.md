---
title: URS
description: Hilfeseite zum Mustererkennungs-Code
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '436'
ht-degree: 100%

---

# URS {#urs}

Nicht unterstützte Repository-Struktur

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Nicht unterstützte Repository-Struktur"
>abstract="URS identifiziert Fälle nicht unterstützter Repository-Struktur sowie Knotencharakteristika. Dadurch werden Informationen zur Vermeidung von Konflikten zwischen AEM-Produkt-Code und Kunden-Code, zur Umstrukturierung von Inhalten aus /etc in andere Ordner im Repository und mehr angezeigt."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html?lang=de" text="Repository-Neustrukturierung"

## Hintergrund {#background}

`URS` identifiziert Fälle nicht unterstützter Repository-Struktur sowie Knotencharakteristika. Ab AEM 6.4 wurden Leitlinien für die Umstrukturierung von Repository-Inhalten festgelegt. Durch die klare Abgrenzung von Hierarchien für AEM-Produkt-Code und Kunden-Code und die Vermeidung von Konflikten zwischen ihnen werden Inhalte aus `/etc` in andere Ordner im Repository umstrukturiert, wobei die folgenden allgemeinen Regeln befolgt werden:

* AEM-Produkt-Code wird immer im Ordner `/libs` abgelegt, der nicht durch benutzerdefinierten Code überschrieben werden darf.
* Benutzerdefinierter Code sollte in `/apps`, `/content` und `/conf` gespeichert werden.
* AEM as a Cloud Service unterstützt keine langen Knotennamen (>150 Byte).
* Es wird dringend empfohlen, dass diese Richtlinien für AEM as a Cloud Service befolgt werden.

Um die spezifischen Arten von Repository-Problemen, die behandelt werden sollten, zu unterscheiden, werden folgende Untertypen verwendet:
* `clientlibs.location`: Eine Client-Bibliothek, die auf `/etc` über den Pfad verweist.
* `file.location`: Eine Datei unter `/etc`, die seit der Installation geändert wurde.
* `node.location`: Ein Knoten, unter `/etc`, der seit der Installation geändert wurde.
* `workflow.location`: Ein Workflow-Modell oder Starter unter `/etc/workflow`.
* `package.structure`: Ein Package, das sowohl veränderlichen als auch unveränderlichen Inhalt enthält.
* `node.name.length`: Ein Knotenname mit nicht unterstützter Länge.
* `node.size`: Ein Knoten mit nicht unterstützter Größe.

## Mögliche Implikationen und Risiken {#implications-and-risks}

* Benutzerdefinierter Code, der sich auf ältere Pfade stützt, kann unerwünschtes Verhalten verursachen und die Produktfunktionalität beeinträchtigen.
* Packages, die sowohl veränderliche als auch unveränderliche Inhalte enthalten, werden wahrscheinlich Probleme bei der Bereitstellung verursachen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, Ihr Code-Projekt zu überprüfen und sicherzustellen, dass es den Richtlinien für die AEM-Projektstruktur entspricht, und Code zu vermeiden, der auf älteren/nicht unterstützten Repository-Pfaden basiert, die unerwünschtes Verhalten in AEM as a Cloud Service verursachen können. Wenden Sie sich an den Adobe Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de" text="Richtlinien zur Struktur von AEM-Projekten"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Eine Anleitung zur Vorbereitung auf AEM as a Cloud Service finden Sie unter [Repository-Neustrukturierung](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html?lang=de).
* Weitere Informationen zu veränderlichen und unveränderlichen Bereichen des Repositorys finden Sie unter [AEM-Projektstruktur](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um nähere Informationen zu erhalten oder um Bedenken auszuräumen.
* Nutzen Sie den [Repository-Modernisierer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html?lang=de#refactoring-tools), um vorhandene Projekt-Packages umzustrukturieren, indem Sie Inhalte und Code in einzelne Packages trennen, damit sie mit der für Adobe Experience Manager as a Cloud Service definierten Projektstruktur kompatibel sind.
