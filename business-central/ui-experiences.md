---
title: 'Ändern, welche Funktionen angezeigt werden'
description: 'Erfahren Sie, was die Essential- und Premium-Stufen der Benutzerfreundlichkeit für die Benutzerschnittstelle, Anwendungsbereiche und Ihr Unternehmen bedeutet.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'essential, basic, user interface, application area, experience'
ms.search.form: 1
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="change-which-features-are-displayed" />Funktionen, die angezeigt werden ändern
[!INCLUDE[prod_short](includes/prod_short.md)] wurde entwickelt, um Ihnen zu helfen, Ihr Unternehmen unabhängig von Größe und Komplexität zu führen. Im Mittelpunkt des Produkts stehen wesentliche Funktionen wie Finanzberichterstattung, Vertrieb, Einkauf und Lagerverwaltung. Mit zunehmender Komplexität des Unternehmens können Sie z.B. Funktionen für das Fertigungs- und Servicemanagement aktivieren.

Sie können die Produktkomplexität und damit die Funktionen definieren, auf die die Benutzer des Unternehmens Zugriff erhalten, indem Sie die Einstellung **Erfahrung** auf der Seite **Firmeninformationen** ändern. Beachten Sie, dass die Erfahrungseinstellung auch geändert werden kann, indem Sie bestimmte Erweiterungen von AppSource hinzufügen. Weitere Informationen finden Sie unter [Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)]](ui-extensions.md) mithilfe der Erweiterungen .

Die verfügbaren Optionen werden in der folgenden Tabelle beschrieben.

| Erfahrung | Auswirkungen auf Benutzeroberfläche |
| --- | --- |
| **Essential** |Zeigt alle Aktionen und Felder für alle verfügbaren Geschäftsfunktionalitäten an.|
| **Premium** |Zeigt alle Aktionen und Felder für alle Geschäftsfunktionalität einschließlich, Produktion und Dienstleistungs-Verwaltung an.|

Die unter [!INCLUDE[prod_short](includes/prod_short.md)] wählbaren Erfahrungen spiegeln die für das Produkt definierten Lösungslizenzen, sogenannte Pläne, wider. Informationen zu den Plänen Essential und Premium finden Sie unter [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) auf der Microsoft Dynamics 365 Marketing-Seite. Siehe auch [[!INCLUDE[prod_short](includes/prod_short.md)] Lizenzierungshandbuch](https://go.microsoft.com/fwlink/?linkid=2068931).

> [!IMPORTANT]  
> Alle regulären Benutzer in einer Lösung müssen demselben Plan, Basis oder Premium zugewiesen sein, bevor die Erfahrung für das Unternehmen ausgewählt werden kann. Entsprechend kann ein Benutzer auf erstklassige Funktionen zugreifen, wenn eine oder mehrere andere Benutzer nur auf  b wichtige Funktion nur zugreifen können. Dies ist nicht der Fall für reguläre Benutzer der Art Teammitglieder, interner Administrator, externer Buchhalter und delegierter Administrator, dem jeder ein unterschiedlicher Plan als bei anderen Benutzern in der Lösung zugeordnet werden können.<br /><br /> Nur Benutzer vom Typ Evaluation oder Premium können den Wert im Feld **Erfahrung** von Essential auf Premium ändern.

Bevor Sie die Benutzereinstellungen eines Unternehmens definieren, definieren Sie den Zugriff der Benutzer auf bestimmte Funktionen und Seiten, indem Sie Berechtigungen zuweisen. Weitere Informationen finden Sie unter [Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).

Die Einstellung **Erfahrung** gilt für alle Benutzer in einem Unternehmen, aber jeder Benutzer kann seine eigene Erfahrung durch Ändern von Seitenlayouts und Inhalten weiter personalisieren. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan" />Erstklassige Funktionen ausführen, nachdem ein Plan aktualisiert wurde
Benutzer werden Plänen in Microsoft 365 Admin Center in Verbindung mit allgemeiner Arbeit zugewiesen, um Business Central Benutzer zu erstellen. Weitere Informationen finden Sie unter [Fügen Sie Benutzer hinzu und weisen Sie gleichzeitig Lizenzen zu](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### <a name="to-update-plan-changes-in-users-groups" />Um Planänderungen der Benutzergruppen zu aktualisieren

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Wenn Sie eine Änderung in den Benutzerplänen im Microsoft 365 Admin Center gemacht haben, wie mehr Benutzer dem Premium Plan hinzuzufügen, muss die Änderung in [!INCLUDE[prod_short](includes/prod_short.md)] aktualisiert werden.

1. Als Administrator anmelden.
2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Benutzer** ein, und wählen Sie dann den entsprechenden Link.
3. Wählen Sie auf der Seite **Benutzer** die Aktion **Benutzer aus Microsoft 365 aktualisieren** aus.

### <a name="to-select-the-premium-experience" />Die Premium-Umgebung auswählen
Sie können jetzt fortfahren, die neuen Benutzeroberfläche auszuwählen.
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Unternehmensdaten** ein, und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Unternehmensinformation** können Sie die **Benutzerfreundlichkeit** für Ihren Mandanten im Feld **Inforegister** festlegen.

## <a name="help-assumes-premium-experience" />Die Hilfe geht von der Premium-Umgebung aus
Alle Funktionsbeschreibungen in der Dokumentation behandeln [!INCLUDE[prod_short](includes/prod_short.md)] die **Premium**-Umgebung, decken also den gesamten Umfang der Benutzeroberflächenelemente ab.

## <a name="see-also" />Siehe auch
[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Business Central anpassen](ui-customizing-overview.md)  
[Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  
[Neue Unternehmen anlegen](about-new-company.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Lizenzierungshandbuches](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
