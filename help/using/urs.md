---
title: URS
description: Hilfeseite zum Mustererkennungs-Code.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 66%

---

# URS {#urs}

Nicht unterstützte Repository-Struktur

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Nicht unterstützte Repository-Struktur"
>abstract="URS identifiziert Fälle von URS (Nicht unterstützte Repository-Struktur) und Knoteneigenschaften. Auf dieser Seite werden Informationen erläutert, um Konflikte zwischen AEM Produkt-Code und Kundencode zu vermeiden, wobei Inhalte aus `/etc` zu anderen Ordnern im Repository und mehr."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Repository-Neustrukturierung"

## Hintergrund {#background}

`URS`  Identifiziert Fälle von URS (Nicht unterstützte Repository-Struktur) und Knoteneigenschaften. Ab AEM 6.4 wurden Leitlinien für die Umstrukturierung von Repository-Inhalten festgelegt. Indem Sie Hierarchien für AEM Produkt-Code und Kundencode klar definieren und Konflikte zwischen ihnen alle vermeiden, werden Inhalte aus `/etc` in andere Ordner im Repository. Befolgen Sie dabei die folgenden allgemeinen Regeln:

* AEM Produktcode wird immer in `/libs` dass benutzerdefinierter Code nicht überschreiben darf.
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
>abstract="Best Practice ist es, Ihr Code-Projekt zu überprüfen. Vergewissern Sie sich, dass die AEM Richtlinien für die Projektstruktur eingehalten wird, und vermeiden Sie Code, der auf ältere oder nicht unterstützte Repository-Pfade angewiesen ist, was in AEM as a Cloud Service zu unerwünschtem Verhalten führen kann. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen oder Fragen haben."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="Richtlinien zur Struktur von AEM-Projekten"
>additional-url="https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html" text="Support für Experience Cloud"

* Eine Anleitung zur Vorbereitung auf AEM as a Cloud Service finden Sie unter [Repository-Restrukturierung](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring).
* Weitere Informationen zu veränderlichen und unveränderlichen Bereichen des Repositorys finden Sie unter [AEM-Projektstruktur](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure).
* Wenden Sie sich an unser [AEM-Supportteam](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html), um weitere Informationen zu erhalten oder um Anliegen vorzubringen.
* Verwenden Sie das Tool [Repository Modernizer](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools), um bestehende Projektpakete neu zu strukturieren, indem Inhalt und Code in separate Pakete aufgeteilt werden. So gewährleisten Sie die Kompatibilität der Pakete mit der Projektstruktur, die für Adobe Experience Manager as a Cloud Service definiert wurde.
