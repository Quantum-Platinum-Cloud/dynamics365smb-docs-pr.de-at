---
title: E-Mail-Protokollierung einr.
description: 'Erfahren Sie, wie Sie E-Mail-Interaktionen zwischen Verkäufern und Kunden in echte Verkaufschancen verwandeln können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: dcenic
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect, opportunity, email'
ms.search.form: '1680, 1811, 5076'
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts" />Verfolgen Sie den Austausch von E-Mail-Nachrichten zwischen Verkäufern und Kontakten

Machen Sie mehr aus der Kommunikation zwischen Ihren Verkäufern und Kunden, indem Sie den E-Mail-Verkehr in umsetzbare Verkaufsmöglichkeiten verwandeln. [!INCLUDE[prod_short](includes/prod_short.md)] kann mit Exchange Online arbeiten, um ein Protokoll der eingehenden und ausgehenden Nachrichten zu erhalten. Sie können den Inhalt jeder Nachricht auf der Seite **Aktivitätenprotokollposten** anzeigen und analysieren.

> [!IMPORTANT]
> Für [!INCLUDE[prod_short](includes/prod_short.md)] online müssen sich [!INCLUDE[prod_short](includes/prod_short.md)] und Exchange Online auf demselben Mandanten befinden.

## <a name="to-set-up-email-logging" />So richten Sie E-Mail-Protokollierung ein

### <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online" />Öffentliche Ordner und Regeln für die E-Mail-Anmeldung in Exchange Online einrichten

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Als nächstes verbinden Sie [!INCLUDE[prod_short](includes/prod_short.md)] mit Exchange Online.

### <a name="set-up-a-shared-mailbox-and-rules-for-email-logging-in-exchange-online" />Einrichten eines freigegebenen Postfachs und Regeln für die E-Mail-Protokollierung in Exchange Online

> [!NOTE]
> Für diese Schritte ist Administratorzugriff für Exchange Online erforderlich.

Bereiten Sie ein freigegebenes Postfach im Exchange Admin Center vor. Alternativ können Sie auch Exchange Online PowerShell verwenden. Weitere Informationen finden Sie unter [Ein freigegebenes Postfach erstellen](/microsoft-365/admin/email/create-a-shared-mailbox) oder [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Wenn Sie Exchange Management PowerShell verwenden, sind Ihre Änderungen mit einer Verzögerung im Exchange Admin Center verfügbar. Die Verzögerung kann mehrere Stunden betragen.

### <a name="add-a-user-account-for-members-of-the-shared-mailbox" />Fügen Sie ein Benutzerkonto für Mitglieder des freigegebenen Postfachs hinzu

Das Konto, das Sie für die E-Mail-Protokollierung verwenden, ist ein Exchange Online-Konto. Der geplante Auftrag verwendet das Konto, um eine Verbindung mit dem freigegebenen Postfach herzustellen und E-Mails zu verarbeiten. Dieses Konto sollte keiner bestimmten Person zugeordnet werden. Fügen Sie das E-Mail-Konto den Mitgliedern für das freigegebene Postfach hinzu. Weitere Informationen finden Sie unter [Exchange Admin Center verwenden, um die Delegierung freigegebener Postfächer zu bearbeiten](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### <a name="allow-other-users-to-see-logged-emails" />Erlauben Sie anderen Benutzern, protokollierte E-Mails zu sehen

Sie können einem anderen Benutzer erlauben, eine E-Mail-Nachricht in Exchange zu öffnen, die sich auf einen Interaktionsprotokolleintrag von [!INCLUDE[prod_short](includes/prod_short.md)] bezieht. Geben Sie dazu dem Benutzer ``Read``-Rechte für den **Archiv**-Ordner im freigegebenen Postfach. Weitere Informationen finden Sie unter [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### <a name="create-mail-flow-rules" />E-Mail-Fluss-Regeln erstellen

Nachrichtenflussregeln suchen nach bestimmten Bedingungen für Nachrichten und ergreifen entsprechende Maßnahmen. Erstellen Sie zwei neue E-Mail-Fluss-Regeln für öffentliche Ordner basierend auf den Informationen in der folgenden Tabelle. Weitere Informationen finden Sie unter [E-Mail-Fluss-Regeln in Exchange Online verwalten](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) und [Aktionen für E-Mail-Fluss-Regeln in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Zweck  |Name  |Diese Regel anwenden, wenn...  |Führen Sie die folgenden Schritte aus...  |
|---------|---------|---------|---------|
|Regel für eingehende E-Mails     |An diese Organisation gesendete E-Mails protokollieren|Der Absender befindet sich außerhalb der Organisation und der Empfänger befindet sich innerhalb der Organisation|Das für das freigegebene Postfach festgelegte E-Mail-Konto mit Bcc senden.|
|Regel für ausgehende E-Mails     |Von dieser Organisation gesendete E-Mails protokollieren|Der Absender befindet sich innerhalb der Organisation und der Empfänger befindet sich außerhalb der Organisation.|Das für das freigegebene Postfach festgelegte E-Mail-Konto mit Bcc senden.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] verarbeitet nur Nachrichten im Posteingangsordner im freigegebenen Postfach. Wenn eine Regel Nachrichten aus dem Posteingang in einen anderen Ordner verschiebt, werden diese Nachrichten nicht verarbeitet. Außerdem werden Nachrichten im Junk-E-Mail-Ordner ebenfalls ignoriert.

## <a name="set-up-includeprodshortincludesprodshortmd-to-log-email-messages" />[!INCLUDE[prod_short](includes/prod_short.md)] zum Protokollieren von E-Mail-Nachrichten einrichten

Beginnen Sie mit der E-Mail-Protokollierung in zwei einfachen Schritten:

1. Verbinden Sie [!INCLUDE[prod_short](includes/prod_short.md)] mit Exchange Online für Ihr Microsoft 365-Abonnement. Exchange Online verarbeitet Ihre E-Mail-Nachrichten. Wir haben diesen Schritt vereinfacht, indem wir eine Anleitung für Unterstützte Einrichtung bereitgestellt haben. Sie benötigen lediglich Ihre Administratoranmeldeinformationen für Ihr Administratorkonto in Microsoft 365. Um die Anleitung zu starten, wechseln Sie zu **Unterstützte Einrichtung**, und wählen Sie dann die Anleitung **E-Mail-Protokollierung einrichten** aus.  

2. Stellen Sie sicher, dass die E-Mail-Adressen Ihrer Vertriebsmitarbeiter und Kontakte in [!INCLUDE[prod_short](includes/prod_short.md)] gültig sind. Öffnen Sie dazu für jeden Kunden oder Verkäufer die Karte **Kontakt**oder **Verkäufer/Käufer**, und überprüfen Sie das Feld **E-Mail**.

    > [!Tip]
    > Nachdem Sie die Schritte in der Anleitung ausgeführt haben, können Sie überprüfen, ob die Verbindung erfolgreich war. Suchen Sie nach **E-Mail-Protokollierung**, wählen Sie **Aktionen** und dann **Einrichtung überprüfen** aus.

## <a name="view-email-message-exchanges-in-the-interaction-log" />Anzeigen des E-Mail-Nachrichtenaustauschs im Aktivitätenprotokoll

[!INCLUDE[prod_short](includes/prod_short.md)] erstellt einen Eintrag auf der Seite **Aktivitätenprotokoll**, jedes Mal, wenn ein Verkäufer und ein Kontakt eine E-Mail-Nachricht austauschen. Um das Interaktionsprotokoll anzuzeigen, öffnen Sie die Karte **Kontakt** für die Person, und wählen Sie **Zugehörig**, dann **Verlauf** und anschließend **Interaktionsprotokollposten** aus. Es gibt einige Dinge, die Sie mit jedem Eintrag im Protokoll tun können, zum Beispiel:

* Zeigen Sie den Inhalt der E-Mail-Nachricht an, die ausgetauscht wurde, indem Sie **Verarbeiten** und dann **Dateianhänge anzeigen** auswählen.
* Verwandeln Sie einen E-Mail-Austausch in eine Verkaufsmöglichkeit. Wenn ein Eintrag vielversprechend aussieht, können Sie ihn in eine Verkaufschance verwandeln und dann den Fortschritt in Richtung Verkauf steuern. Um einen E-Mail-Austausch in eine Chance zu verwandeln, wählen Sie den Eintrag, dann **Prozess** und dann **Gelegenheit schaffen** aus. Weitere Informationen finden Sie unter [Verkaufschancen verwalten](marketing-manage-sales-opportunities.md).

## <a name="mailbox-and-folder-limits-in-exchange-online" />Postfach- und Ordnerbeschränkungen in Exchange Online

Es gibt Postfach- und Ordnerbeschränkungen in Exchange Online, darunter Beschränkungen für Ordnergrößen und Anzahl der Nachrichten. Weitere Informationen finden Sie unter [Exchange Online-Beschränkungen](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) und [Einschränkungen für öffentliche Ordner in Exchange Server](/Exchange/collaboration/public-folders/limits?view=exchserver-2019&preserve-view=true).

[!INCLUDE[prod_short](includes/prod_short.md)] speichert protokollierte E-Mail-Nachrichten in einem Ordner in Exchange Online. [!INCLUDE[prod_short](includes/prod_short.md)] speichert auch einen Link zu jeder protokollierten Nachricht. Die Links öffnen die protokollierten Nachrichten in Exchange Online auf den Seiten „Interaktionsprotokollposten“, „Kontaktkarte“ und „Verkäuferkarte“ in [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn eine protokollierte Nachricht in einen anderen Ordner verschoben wird, wird der Link beschädigt. Beispielsweise kann eine Nachricht manuell verschoben werden, oder Exchange Online kann AutoSplit automatisch starten, wenn ein Speicherlimit erreicht ist.

Anhand der folgenden Schritte können Sie verhindern, dass Links zu Nachrichten in Exchange Online beschädigt werden.

1. Verschieben Sie vorhandene Nachrichten nicht in einen anderen Ordner, nachdem Sie die Einstellungen für Ihre E-Mail-Protokollierung geändert haben. Wenn Sie vorhandene Nachrichten dort belassen, wo sie sind, bleiben die Links erhalten. Links zu Nachrichten im neuen Ordner sind gültig.
2. Vermeiden Sie das Erreichen der Postfach- und Ordnerbeschränkungen. Wenn Sie kurz davor sind, eine Beschränkung zu erreichen, führen Sie die folgenden Schritte aus:
    1. Ein neues freigegebenes Postfach in Exchange Online einrichten.
    2. Aktualisieren Sie Ihre E-Mail-Flow-Regeln in Exchange Online.
    3. Aktualisieren Sie die Einrichtung der E-Mail-Protokollierung in Business Central entsprechend.

## <a name="connect-on-premises-versions-to-microsoft-exchange" />Lokale Versionen mit Microsoft Exchange verbinden

Sie können eine Verbindung mit [!INCLUDE[prod_short](includes/prod_short.md)] lokal zum Austausch lokal oder für die Exchange Online Protokollierung verbinden. Für beide Exchange-Versionen sind die Einstellungen für die Verbindung auf der Seite **Marketing-Einrichtung** verfügbar. Für Exchange Online können Sie auch eine unterstützte Einrichtungsanleitung verwenden.

<!-- [!IMPORTANT]
> The new experience doesn't support a connection to Exchange on-premises. If you must use Exchange on-premises, do not enable the feature update for the new experience.

## <a name="connect-to-exchange-on-premises" />Connect to Exchange on-premises
<!--
## [Current Experience](#tab/current-experience)
To connect [!INCLUDE[prod_short](includes/prod_short.md)] on-premises to Exchange on-premises, on the **Marketing Setup** page, you can use **Basic** as the **Authentication Type**, and then enter credentials for the user account for Exchange on-premises. Then turn on the **Enabled** toggle to start logging email.

## [New Experience](#tab/new-experience)
The new experience does not support connections to Exchange on-premises.
-->
## <a name="connect-to-exchange-online" />Mit Exchange Online verbinden

Um Exchange Online zu verbinden, müssen Sie eine Anwendung in Azure Active Directory registrieren. Geben Sie die Anwendungs-ID, das Geheimnis des Schlüsseltresors und die Umleitungs-URL an, die für die Registrierung verwendet werden soll. Die Umleitungs-URL ist bereits festgelegt und sollte für die meisten Installationen funktionieren. Weitere Informationen finden Sie unter [So registrieren Sie eine Anwendung in Azure AD für die Verbindung von Business Central mit Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Sie müssen auch **OAuth2** als **Authentifizierungstyp** verwenden. Sie müssen auch eine Anwendung in registrieren Azure Active Directory. Geben Sie die Anwendungs-ID, das Geheimnis des Schlüsseltresors und die Umleitungs-URL an, die für die Registrierung verwendet werden soll. Die Umleitungs-URL ist bereits ausgefüllt und sollte für die meisten Installationen funktionieren. Weitere Informationen finden Sie weiter unten unter „So registrieren Sie eine Anwendung in Azure AD für die Verbindung von Business Central mit Exchange Online“.

Sie müssen Ihre Installation für die Verwendung von HTTPS einrichten. Weitere Informationen finden Sie unter [Konfigurieren von SSL zum Sichern der Business Central Web Client-Verbindung ](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Wenn Sie Ihren Server für eine andere Homepage einrichten, können Sie die URL jederzeit ändern. Der geheime Clientschlüssel wird als verschlüsselte Zeichenfolge in Ihrer Datenbank gespeichert.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online" />So registrieren Sie eine Anwendung in Azure AD, um eine Verbindung mit Exchange Online über Business Central herzustellen

Bei den folgenden Schritten wird davon ausgegangen, dass Sie Azure Active Directory verwenden, um Identitäten und den Zugriff zu verwalten. Weitere Informationen finden Sie unter [Schnellstart: Registrieren einer Anwendung mit der Microsoft-Identitätsplattform](/azure/active-directory/develop/quickstart-register-app). 

1. Wählen Sie im Navigationsbereich von Azure-Portal unter **Verwalten** die Option **Authentifizierung** aus.
2. Fügen Sie unter **URL umleiten** die Umleitungs-URL hinzu, die auf der Seite **E-Mail-Protokollierung** in [!INCLUDE[prod_short](includes/prod_short.md)] vorgeschlagen wird. Wenn das URL-Feld auf der Seite E-Mail-Protokollierung leer ist, finden Sie die vorgeschlagene Weiterleitungs-URL auf der Seite **Unterstützung Einrichtung**. Um die Seite zu öffnen, wählen Sie auf der **E-Mail-Protokollierung**-Seite **Aktionen** und dann **Unterstützte Einrichtung** aus.

    > [!NOTE]
    > Wenn Sie die Umleitungs-URL nicht angeben, können Sie dies später durch Auswahl von **Fügen Sie eine Plattform hinzu** tun und dann **Internet** wählen, um die Webanwendung und die Weiterleitungs-URL hinzuzufügen.

3. Unter **Verwalten** wählen Sie **API-Berechtigungen** und dann **Microsoft Graph** und dann aus **Delegierte Berechtigungen**.
4. Verwenden Sie das Suchfeld, um **Mail** zu suchen und auszuwählen, und fügen Sie dann die **Mail.ReadWrite.Shared**-Berechtigung hinzu. 
5. Wählen Sie unter **Verwalten** die Option **Zertifikate & Geheimnisse** aus, und erstellen Sie dann einen neuen geheimen Schlüssel für Ihre App. Sie verwenden das Geheimnis entweder im **Client-Geheimnis**-Feld auf der **E-Mail-Protokollierung**-Seite in [!INCLUDE[prod_short](includes/prod_short.md)].
6. Wählen Sie **Übersicht** aus, und suchen Sie dann den Wert **Anwendungs-(Client-)ID**. Dies ist die Client-ID Ihrer Anwendung. Sie müssen es entweder im **Client-ID**-Feld auf der **E-Mail-Protokollierung**-Seite eingeben.
7. Unter [!INCLUDE[prod_short](includes/prod_short.md)] richten Sie die E-Mail-Protokollierung auf der Seite **E-Mail-Protokollierung** ein oder verwenden Sie die **Unterstützte Einrichtung** für Unterstützung bei diesem Prozess.

### <a name="use-another-identity-and-access-management-service" />Verwenden eines anderen Identitäts- und Zugriffsverwaltungsdienstes

Wenn Sie Azure Active Directory nicht verwenden, um Identitäten und den Zugriff zu verwalten, benötigen Sie die Hilfe eines Entwicklers. Wenn Sie die App-ID und den geheimen Schlüssel lieber an einem anderen Ort speichern möchten, können Sie die Felder „Client-ID“ und „Geheimer Clientschlüssel“ leer lassen und eine Erweiterung schreiben, um die ID und den geheimen Schlüssel von diesem Speicherort abzurufen. Sie können den geheimen Clientschlüssel zur Laufzeit bereitstellen, indem Sie die Ereignisse OnGetEmailLoggingClientId und OnGetEmailLoggingClientSecret in Codeunit 1641 E-Mail-Protokollierung einrichten abonnieren.

## <a name="to-start-logging-email" />E-Mail-Protokollierung starten

1. Um die E-Mail-Protokollierung zu starten, aktivieren Sie auf der Seite **E-Mail-Protokollierung** den Schalter **Aktiviert**.
2. Melden Sie sich mit dem Exchange Online-Konto an, das der geplante Auftrag für die Verbindung mit dem freigegebenen Postfach und die Verarbeitung von E-Mails verwenden soll.

    > [!NOTE]
    > Wenn Sie nicht aufgefordert werden, sich bei Ihrem Exchange Online-Konto anzumelden, liegt das möglicherweise daran, dass Ihr Browser Popups blockiert. Erlauben Sie Popups von https://login.microsoftonline.com, um sich anzumelden.

## <a name="to-stop-logging-email" />E-Mail-Protokollierung beenden

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **E-Mail-Protokollierung** ein und wählen Sie dann den zugehörigen Link.
2. Umschaltung **Aktiviert** ausschalten.

## <a name="to-change-the-user-account-used-for-email-logging" />Zum Ändern des für die E-Mail-Protokollierung verwendeten Benutzerkontos

### <a name="includeprodshortincludesprodshortmd-online" />[!INCLUDE[prod_short](includes/prod_short.md)] Online

1. Melden Sie sich mit dem [!INCLUDE[prod_short](includes/prod_short.md)]-Konto an, das der geplante Auftrag für die Verbindung mit dem freigegebenen Postfach und die Verarbeitung von E-Mails verwenden soll. Dieses Konto muss Zugriff auf [!INCLUDE[prod_short](includes/prod_short.md)] und Exchange Online haben.
2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **E-Mail-Protokollierung** ein und wählen Sie dann den zugehörigen Link. 
3. Wählen Sie **Verwandt** und dann **Aufgabenwarteschlangenposten**.
4. Starten Sie die **E-Mail-Protokollierung**-Aufgabe neu.

### <a name="includeprodshortincludesprodshortmd-on-premises" />[!INCLUDE[prod_short](includes/prod_short.md)] On-Premises

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **E-Mail-Protokollierung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Aktionen** und dann **Token erneuern**.
3. Melden Sie sich mit dem Exchange Online-Konto an, das der geplante Auftrag für die Verbindung mit dem freigegebenen Postfach und die Verarbeitung von E-Mails verwenden soll.

## <a name="see-also" />Weitere Informationen
[Verwalten von Beziehungen](marketing-relationship-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
