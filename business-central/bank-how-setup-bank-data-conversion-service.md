---
title: Bankdatenkonvertierung einrichten
description: 'Sie können Bankkonten einrichten, um Geschäftsvorfälle und Import- oder Ausfuhrbankfeeds, wie Yodlee zu verwalten.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer'
ms.search.form: '304, 20106, 20105, 20100, 20101, 20107, 20109'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-the-amc-banking-365-fundamentals-extension" />Einrichten der AMC Banking 365 Fundamentals-Erweiterung
Ein globaler Diensteanbieter, der Bankdaten in das Dateiformat konvertiert, das Ihre Bank verlangt, ist in [!INCLUDE[prod_short](includes/prod_short.md)] eingebunden und kann aktiviert werden. Dies wird in [!INCLUDE[prod_short](includes/prod_short.md)] als die AMC Banking 365 Fundamentals-Erweiterung bezeichnet.

Sie können Zahlungspositionen aus der Seite **Zahlungsausgangs Buch.-Blatt** in einen Datenstream oder eine Datei exportieren, den Sie dann für Ihre Bank automatische zum Verarbeiten hochladen, sodass Sie elektronische Zahlungen nicht einzeln ausführen müssen. Weitere Informationen finden Sie unter [Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Sie können Bankkontoauszugsdateien in das **Zahlungsabstimmungsbuch.-Blatt** importieren, indem Sie die AMC Banking 365 Fundamentals-Erweiterung verwenden, um eine Datei zu erstellen, die Sie von Ihrer Bank mit einem Datenstream erhalten, die in [!INCLUDE[prod_short](includes/prod_short.md)] importiert werden kann. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Als Alternative zum Importieren von Bankkontoauszügen mit der AMC Banking 365 Fundamentals-Erweiterung können Sie den Dienst Envestnet Yodlee Bank Feeds verwenden. Weitere Informationen finden Sie unter [Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md).

Um Bankdateien zu importieren oder zu exportieren, müssen Sie Ihre eigenen Bankkonten und jene des Kreditors einrichten. Weitere Informationen finden Sie unter [So geht's: Einrichten von Bankkonten](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> Die AMC Banking 365 Fundamentals-Erweiterung legt möglicherweise einen Höchstwert für die Anzahl der Zeilen fest, die in einer Datei exportiert werden können. Sie erhalten eine Fehlermeldung, wenn der Grenzwert überschritten wird. Es wird empfohlen, dass Bankkontoauszugsdateien 1.000-Zeilen nicht überschreiten, da sich die Verarbeitungszeit in der AMC Banking 365 Fundamentals-Erweiterung andernfalls erheblich erhöht.

## <a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension" />So registrieren Sie Ihr Unternehmen für die AMC Banking 365 Fundamentals-Erweiterung
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Bank Data Conv. Service Einrichtung** ein, und wählen Sie dann den entsprechenden Link.  
2. Die Seite **Einrichtung Bankdaten-Konvertierungsservice** wird geöffnet und zeigt drei Felder an, die mit relevanten URLs des Anbieters der AMC Banking 365 Fundamentals-Erweiterung vorab ausgefüllt sind.

    > [!NOTE]  
    >   In der Demodatenbank von CRONUS International Ltd. werden die Felder „Benutzername“ und „Kennwort“ vorab mit Demoanmeldungsinformationen ausgefüllt, die Sie durch die tatsächlichen Informationen Ihres Unternehmens ersetzen müssen, wenn Sie sich für die AMC Banking 365 Fundamentals-Erweiterung registrieren.
3. Wählen Sie im Feld **Registrierungs-URL** die Browserschaltfläche, um die Registrierungsseite des Dienstanbieters zu öffnen.  
4. Geben Sie auf der Registrierungsseite des Bankdatendienstanbieters den Benutzernamen und das Kennwort für das Abonnement Ihres Unternehmens ein, und schließen Sie dann die Anmeldung ab, wie von dem Dienstanbieter angewiesen.

    Ihr Unternehmen ist nun für die AMC Banking 365 Fundamentals-Erweiterung registriert. Fahren Sie fort, um den Benutzernamen und das Kennwort einzugeben, die Sie für den Service für die verknüpften Einrichtungsfeldern in [!INCLUDE[prod_short](includes/prod_short.md)] angegeben haben.

5. auf der Seite **Einrichtung Bankdaten-Konvertierungsservice** geben Sie im Feld **Benutzername** den gleichen Wert ein, den Sie als Benutzername auf der Seite des Dienstanbieters in Schritt 4 eingegeben haben.
6. Geben Sie im Feld **Kennwort** denselben Wert ein, den Sie im Feld **Kennwort** auf der Seite des Dienstanbieters in Schritt 4 angegeben haben.

> [!NOTE]  
> Sie informieren Daten werden verschlüsselt automatisch an.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats" />Um die Liste der gerade unterstützten Bankdatenformate anzeigen oder zu aktualisieren
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Bankdaten Konv. Service Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Einrichtung Bankdaten-Konvertierungsservice** die Aktion **Bankname – Datenkonvertierungsübersicht**, um die Liste der Banknamen zu öffnen, die die Bankdatenformate darstellen, die von dem Konvertierungs-Service unterstützt werden.
3. Wählen Sie auf der Seite **Bankname – Datenkonvertierungsübersicht** die Aktion **Banknamenübersicht aktualisieren** aus.

Die Liste der Bankdatenformate, die von der AMC Banking 365 Fundamentals Erweiterung unterstützt werden, wurde aktualisiert. Dies ist die Liste der Banknamen, gefiltert nach den Ländern/Regionen, die Sie im Feld **Bankname – Datenkonvertierung** auf der Seite **Bankkontokarte** auswählen können.

> [!NOTE]  
>   Die Aktualisierung der unterstützten Bankdatenformate erfolgt auch, wenn Sie einen Wert im Feld **Bankname – Datenkonvertierung** des Bankkontos auswählen oder dort einen Wert eingeben.

Sie haben sich nun für die AMC Banking 365 Fundamentals-Erweiterung registriert. Fahren Sie fort, die Registrierungsinformationen über jedes Bankkonto wiederzugeben, das der Service verwendet.

## <a name="see-also" />Weitere Informationen
[Einrichten von Banken](bank-setup-banking.md)  
[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
