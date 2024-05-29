---
title: URS
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: ht
source-wordcount: '380'
ht-degree: 100%

---

# URS {#urs}

Nicht unterstützte Repository-Struktur

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Nicht unterstützte Repository-Struktur"
>abstract="URS (Unsupported Repository Structure) identifiziert Fälle nicht unterstützter Repository-Struktur sowie Knotencharakteristika. Dadurch werden Informationen zur Vermeidung von Konflikten zwischen AEM-Produkt-Code und Kunden-Code, zur Umstrukturierung von Inhalten aus `/etc` in andere Ordner im Repository und mehr angezeigt."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Repository-Neustrukturierung"

## Hintergrund {#background}

`URS` URS identifiziert Fälle nicht unterstützter Repository-Struktur sowie Knotencharakteristika. Ab AEM 6.4 wurden Leitlinien für die Umstrukturierung von Repository-Inhalten festgelegt. Durch die klare Abgrenzung von Hierarchien für AEM-Produkt-Code und Kunden-Code und die Vermeidung von Konflikten zwischen ihnen werden Inhalte aus `/etc` in anderen Ordnern im Repository in umstrukturierter Form abgelegt. Befolgen Sie dabei die folgenden allgemeinen Regeln:

* AEM-Produkt-Code befindet sich immer in `/libs` und darf nicht durch benutzerdefinierten Code überschrieben werden.
* Benutzerdefinierter Code sollte in `/apps`, `/content` und `/conf` eingefügt werden.
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
* Pakete, die sowohl veränderliche als auch unveränderliche Inhalte enthalten, werden wahrscheinlich Probleme bei der Bereitstellung verursachen.

## Mögliche Lösungen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Implementierungsleitlinien"
>abstract="Best Practice ist es, Ihr Code-Projekt zu überprüfen. Stellen Sie sicher, dass es den Richtlinien für die AEM-Projektstruktur entspricht und dass Code nicht auf älteren oder nicht unterstützten Repository-Pfaden basiert, was unerwünschtes Verhalten in AEM as a Cloud Service verursachen kann. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="Richtlinien zur Struktur von AEM-Projekten"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Eine Anleitung zur Vorbereitung auf AEM as a Cloud Service finden Sie unter [Repository-Restrukturierung](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring).
* Weitere Informationen zu veränderlichen und unveränderlichen Bereichen des Repositorys finden Sie unter [AEM-Projektstruktur](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
* Verwenden Sie das Tool [Repository Modernizer](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools), um bestehende Projektpakete neu zu strukturieren, indem Inhalt und Code in separate Pakete aufgeteilt werden. So gewährleisten Sie die Kompatibilität der Pakete mit der Projektstruktur, die für Adobe Experience Manager as a Cloud Service definiert wurde.
