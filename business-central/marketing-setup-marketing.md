---
title: Marketing- und Kontaktmanagement-Informationen festlegen
description: 'Sie können Marketings- und Kontaktverwaltung in Business Central einrichten, um Verbindungen mit potentiellen Debitoren oder Debitoren zu optimieren und Kampagnen und Promotionen zu verbessern.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect, client, customer, campaign, promo'
ms.search.forms: '5172, 5173, 5170, 5094, 429'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setting-up-relationship-management" />Marketing &amp; Vertrieb einrichten

Bevor mit Ihren Kontakten und Marketinginteressen arbeiten, gibt es einige Entscheidungen und Schritte, die Sie zur Einrichtung der Verwaltung bestimmter Aspekte Ihrer Kontakte durch den Marketingbereich durchführen sollen. Beispielsweise können Sie entscheiden, ob die Kontaktkarte mit der Debitorenkarte, der Kreditorenkarte und der Bankkontokarte synchronisiert wir, wie Nummernkreise definieren werden oder welche Anrede im Schriftverkehr mit Ihren Kontakten verwendet wird.

Die Verwaltung von Kontakten und die Verfolgung einer Strategie zum Identifizieren, Gewinnen und Binden von Debitoren tragen zu einer Optimierung des Unternehmens sowie zu einer Steigerung der Kundenzufriedenheit bei. Ein gutes Kontaktverwaltungssystem ermöglicht zudem das Knüpfen und Pflegen von Kundenbeziehungen. Die Kommunikation ist bei einer solchen Beziehung besonders wichtig. So ist denn auch die Möglichkeit, die Kommunikation exakt auf die jeweiligen Anforderungen von Interessenten, bestehenden Debitoren, Kreditoren und Geschäftspartnern zuschneiden zu können, für den Erfolg eines Unternehmens unverzichtbar. Einer der ersten Schritte besteht darin, eine Strategie auszuarbeiten und zu definieren, wie Kontaktinformationen im Unternehmen verwendet werden sollen. Da diese Informationen innerhalb des Unternehmens einer Vielzahl von Gruppen zur Verfügung stehen, empfiehlt sich die Verwendung eines durchdachten Systems, um eine höhere Produktivität der einzelnen Beteiligten zu erzielen.

Sie richten die Marketing- und Kontaktverwaltung über die Seite **Marketingeinrichtung** ein. Um die Seite **Marketing Einrichtung** zu öffnen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Marketing Einrichtung** ein, und wählen Sie dann den zugehörigen Link.

## <a name="automatically-copying-specific-information-from-contact-companies-to-contact-persons" />Automatisches Kopieren bestimmter Informationen aus den Kontaktunternehmen zu den Kontaktpersonen
Einige Informationen über die Kontaktunternehmen stimmen mit denen über die Kontaktpersonen bei diesen Unternehmen überein, wie z. B. die Adresse. Im **Übernahme**-Abschnitt der Seite **Marketingeinrichtung** können Sie die Anwendung so einrichten, das bestimmte Felder automatisch von der Kontaktunternehmenskarte in die Kontaktpersonenkarte kopieren werden, wenn Sie eine Kontaktperson für ein Kontaktunternehmen erstellen. Beispielsweise können Sie auswählen, dass Verkäufercode, Adressendaten (Adresse, Adresse 2, Ort, PLZ und Bundesgebiet), Kommunikationsdetails (Faxnummer, Telex und Telefonnummer) kopiert werden.

Wenn Sie eines dieser Felder auf der Kontaktunternehmenskarte ändern, wird die Anwendung automatisch das Feld der Kontaktpersonenkarte ändern (es sei denn, Sie haben das Feld auf der Kontaktpersonenkarte manuell geändert).

Weitere Informationen finden Sie unter [Kontakte erstellen](marketing-create-contact-companies.md).

## <a name="use-predefined-defaults-on-new-contacts" />Vordefinierte Standards für neue Kontakte nutzen
Sie können festlegen, dass jedem neuen Kontakt bei seiner Erstellung automatisch ein bestimmter Sprachcode, Gebietscode, Verkäufercode und Länder-/Regionscode als Vorgabe zugeordnet wird. Außerdem können Sie einen Vorgabewert für einen Verkaufsprozesscode eingeben, dem die Anwendung automatisch jede Verkaufschance zuweist, die Sie erstellen.

Durch die Übernahme von Feldern werden die Vorgabewerte überschrieben, die Sie eingerichtet haben. Wenn Sie z. B. Englisch als Vorgabesprache eingerichtet haben, die Sprache des Kontaktunternehmens jedoch Deutsch ist, wird den Kontaktpersonen dieses Unternehmens automatisch die Sprache Deutsch von der Anwendung zugewiesen.

<!--You can also setup a default salutation that application automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, application will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-recording-interactions" />Aktivitäten automatisch speichern
[!INCLUDE[prod_short](includes/prod_short.md)]Die Anwendung kann Verkaufs- und Einkaufsbelege (z. B. Aufträge, Rechnungen, Lieferungen usw.) sowie E-Mails, Telefonanrufe und Deckblätter automatisch speichern.

Weitere Informationen finden Sie unter [Aktivitäten mit Kontakten automatisch aufzeichnen](marketing-auto-record-interactions.md).

## <a name="synchronizing-contacts-with-customers-and-more" />Synchronisieren von Kontakten mit Debitoren und anderen
Um die Kontaktkarte mit der Debitoren-, der Kreditoren- und der Bankkontenkarte zu synchronisieren, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten auswählen. Sie können z. B. einen Kontakt nur mit einem bestehenden Debitor verknüpfen, wenn Sie auf der Seite **Marketingeinrichtung** einen Geschäftsbeziehungscode für Debitoren ausgewählt haben.

Weitere Informationen finden Sie unter [Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).  

## <a name="assigning-a-number-series-to-contacts-and-opportunities" />Zuweisen von Nummernserien zu Kontakten und Verkaufschancen
Sie können Nummernserien für Kontakte und Verkaufschancen einrichten. Wenn Sie eine Nummernserie für Kontakte eingerichtet haben, wählen Sie beim Erstellen eines Kontakts <kbd>Eingeben</kbd> im Feld auf der Kontaktkarte, die Anwendung fügt die nächste verfügbare Kontaktnummern automatisch ein.

Weitere Informationen über Nummernserien finden Sie unter [Erstellen von Nummernserien](ui-create-number-series.md)

## <a name="searching-for-duplicate-contacts-when-contacts-are-created" />Suche nach Kontaktdubletten, wenn Kontakte erstellt werden
Sie können einrichten, dass jede Anwendung automatisch nach Dubletten sucht, wenn Sie ein neues Kontaktunternehmen erstellen, oder Sie können dies manuell vornehmen, nachdem Sie Kontakte erstellt haben. Sie können auch einstellen, dass die Anwendung bei jeder Veränderung der Informationen über den Kontakt oder bei seiner Erstellung automatisch die Suchtexte aktualisiert. Sie können den Prozentsatz der Übereinstimmung festlegen, d. h., den Prozentsatz der Suchtexte, der zwischen den beiden Kontakten identisch sein muss, damit sie von der Anwendung als Dubletten erkannt werden.

## <a name="see-also" />Weitere Informationen
[Kontakte verwalten](marketing-contacts.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
