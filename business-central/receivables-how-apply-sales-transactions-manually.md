---
title: Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Buch.-Blatt oder von Debitorenposten
description: 'Beschreibt, wie Debitorenzahlungseingänge oder -Erstattungen mit einem oder mehreren offenen Debitorenposten angewendet werden. Dies ist Teil der Abstimmung von Kundenzahlungen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '25, 255'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="reconcile-customer-payments-with-the-cash-receipt-journal-or-from-customer-ledger-entries" />Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Buch.-Blatt oder von Debitorenposten

Wenn Sie eine Barzahlung von einem Kunden erhalten oder eine Barrückerstattung leisten, können Sie die Zahlung oder Rückerstattung verwenden, um offene Lastschriften oder Gutschriften zu schließen. Sie können den Betrag angeben, den Sie anwenden möchten. Beispielsweise können Sie Teilzahlungen für die Debitorenposten übernehmen. Der Abschluss von Kundenbucheinträgen hält Debitorenstatistiken, Kontoauszüge, Finanzierungskosten usw. auf dem neuesten Stand.

> [!TIP]  
>   Auf der Seite **Debitorenposten** bedeutet die rote Schriftart, dass die entsprechende Zahlung nach dem Fälligkeitsdatum liegt. Wenn fällige Zahlungen ein Problem werden, können wir Ihnen dabei helfen, die Häufigkeit zu verringern. Sie können die Funktionen **Zahlungsverzug-Vorhersagen** Erweiterung aktivieren, die ein vorbestimmtes Modell verwendet, das wir in Azure Machine Learning erstellten, um die zeitliche Steuerung der Zahlungen vorauszusagen. Diese Vorhersagen helfen Ihnen, ausstehende Forderungen zu reduzieren und die Sammlungsstrategie abzustimmen. Wenn beispielsweise vorausgesagt wird, dass eine Zahlung zu spät erfolgen wird, können Sie sich entschieden, die Zahlungsfristen oder die Zahlungsform für den Debitor anzupassen. Weitere Informationen finden Sie unter [Vorhersage verspätete Zahlung](ui-extensions-late-payment-prediction.md).  

Sie können Debitorenposten auf mehrere Arten übernehmen:

* Durch die Eingabe von Informationen über dedizierte Seiten:
    * Die Seite **Zahlungsabstimmungsbuch.-Blatt**. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).
    * Die Seite **Zahlungsregistrierung**. Weitere Informationen finden Sie unter [Debitoren-Zahlungen aus einer Liste mit unbezahlten Verkaufsbelegen abstimmen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)
    * Das **Zahlungseingangs Buch.-Blatt**. Diese Option wird nachfolgend beschrieben.
* Durch das Ausfüllen des Felds **Ausgleich mit Belegnr.** in Verkaufsgutschriftsbelegen. Diese Option wird nachfolgend beschrieben.
* Mit der **Ausgleichs-ID setzen**-Aktion in Debitorenposten. Diese Option wird nachfolgend beschrieben.
* Indem Sie die Aktion **Buchungen zuweisen** auf der Seite **Bankeinzahlung** verwenden und dann die Rechnungsnummer in das Feld **Gilt für ID** eingeben. Weitere Informationen finden Sie unter [Bankeinzahlungen erstellen](bank-create-bank-deposits.md).

> [!NOTE]  
>   Wenn das Feld **Ausgleichsmethode** auf der Debitorenkarte **Auf älteste anwenden** festgelegt ist, dann wird die Zahlung automatisch mit der ältesten offenen Rechnung abgeglichen, wenn Sie nicht explizit manuell einen Eintrag definieren. Ist die Ausgleichsmethode eines Debitors auf **Manuell** festgelegt, müssen die Posten immer manuell ausgeglichen werden.

## <a name="to-fill-and-post-a-cash-receipt-journal" />So füllen Sie ein Zahlungseingangs Buch.-Blatt aus und buchen dieses
Ein Zahlungseingangs Buch.-Blatt ist eine Art allgemeines Journal. Sie können damit Transaktionen auf Sach-, Bank-, Debitoren-, Kreditoren- und Anlagekonten buchen. Daher können Sie die Zahlungen beim Buchen auf einen oder mehrere Sollposten anwenden. Sie können sich auch später aus den veröffentlichten Einträgen bewerben.
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Zahlungseingangs Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
3. Wählen Sie im Feld **Buch.-Blattname** das relevante Buch.-Blatt aus.
4. Füllen Sie das Feld **Buchungsdatum** auf.  
5. Wählen Sie im Feld **Belegart** die Option **Zahlung** aus.

    Das Feld **Belegnr.** wird anhand der Nummernserie ausgefüllt, die dem Buch.-Blatt zugeordnet wurde.  
6. Verwenden Sie das Feld **Externe Belegnummer**, um eine Kennung wie die Schecknummer des Debitors, zu speichern.
7. Wählen Sie im Feld **Kontoart** die Option **Kreditor** aus.
8. Wählen Sie im Feld **Bankkontonummer** den entsprechenden Bankkontocode aus.
9. Falls Sie den Ausgleich gleichzeitig mit dem Buch.-Blatt buchen möchten, führen Sie einen der folgenden Schritte durch.
10. Wählen Sie im Feld **Gegenkontoart** das **Sachkonto** für Barzahlungen und das **Bankkonto** für sonstige Zahlungen aus.
11. Wählen Sie im Feld **Gegenkontonr.** das Barkonto für Barzahlungen oder das zutreffende Bankkonto für sonstige Zahlungen aus.
12. Buchen Sie die Buch.-Blattzeile.

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry" />So gleichen Sie einen einzelnen Debitorenposten mit einer Zahlung aus:
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Zahlungseingangs Buch.-Blatt** ein und wählen Sie den zugehörigen Link.
2. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
3. Geben Sie in der ersten Buch.-Blattzeile die entsprechenden Informationen zu dem auszugleichenden Posten ein.
4. Wählen Sie im Feld **Belegart** die Option **Zahlung** aus.
5. Wählen Sie im Feld **Kontoart** die Option **Kreditor** aus.
6. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.
7. Im Feld **Ausgleich mit Belegnr.** wählen Sie das Feld aus, um die Seite **Debitorenpostenausgleich** zu öffnen.
8. Wählen Sie auf der Seite **Debitorenpostenausgleich** die Zeilen mit den Posten aus, die Sie mit der Zahlung ausgleichen möchten.
9. Geben Sie in jeder Zeile im Feld **Anzuwendender Betrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten. Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen.

    Am unteren Rand der Seite **Debitorenpostenausgleich** sehen Sie einen spezifischen Betrag im Fenster **Angewendeter Betrag** und auch, ob die Buchung ausgeglichen ist.  
10. Wählen Sie die Schaltfläche **OK** aus. Die Seite **Zahlungseingangsbuch.-Blatt** zeigt nun die Einträge unter **Ausgleich mit Belegart** und auf **Ausgleich mit Belegnr.**.
11. Buchen Sie das Zahlungseingangs-Buch.-Blatt.

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries" />So gleichen Sie mehrere Debitorenposten mit einer Zahlung aus:
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Zahlungseingangs Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
3. Geben Sie in der ersten Buch.-Blattzeile die entsprechenden Informationen zu dem auszugleichenden Posten ein.
4. Wählen Sie im Feld **Belegart** die Option **Zahlung** aus.
5. Wählen Sie im Feld **Kontoart** die Option **Kreditor** aus.
6. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.
7. Geben Sie im Feld **Betrag** die vollständige Zahlung als negativen Betrag ein.
8. Wenn Sie die Zahlung bei der Buchung mit mehreren Kreditorenposten ausgleichen möchten, klicken Sie auf die Aktionen **Einträge anwenden**.  
9. Wählen Sie die Zeilen mit den Posten aus, die mit dem Ausgleichsposten ausgeglichen werden sollen, und klicken Sie anschließend auf **Ausgleichs-ID setzen anwenden**.  
10. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten. Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen.

    Am unteren Rand der Seite **Debitorenpostenausgleich** sehen Sie einen spezifischen Betrag im Fenster **Angewendeter Betrag** und auch, ob die Buchung ausgeglichen ist.  
11. Wählen Sie die Schaltfläche **OK**.
12. Buchen Sie das Zahlungseingangs-Buch.-Blatt.

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry" />So gleichen Sie einen einzelnen Debitorenposten mit einer Gutschrift aus:
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Verkaufsgutschriften** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die relevante Verkaufsgutschrift.
3. Wenn Sie beim Buchen einen einzelnen Debitorenposten mit einer Gutschrift ausgleichen möchten, klicken Sie auf das Inforegister **Anwendung im Feld** , und wählen Sie den Posten, den Sie mit der Zahlung ausgleichen möchten.
4. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten.  

    Wenn Sie keinen Betrag eingeben, wird die Anwendung automatisch mit dem Höchstbetrag angewendet. Am unteren Rand der Seite **Debitorenpostenausgleich** sehen Sie einen spezifischen Betrag im Fenster **Angewendeter Betrag** und auch, ob die Buchung ausgeglichen ist.    
5. Wählen Sie die Schaltfläche **OK**. Die Seite **Verkaufsgutschrift** zeigt nun die von Ihnen ausgewählten Einträge unter **Ausgleich mit Belegart** und auf **Ausgleich mit Belegnr.**. Und den Betrag der zu buchenden Gutschrift an, wobei mögliche Skonti berücksichtigt werden.
6. Buchen Sie die Gutschrift.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries" />So gleichen Sie mehrere Debitorenposten mit einer Gutschrift aus:
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Verkaufsgutschriften** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die relevante Verkaufsgutschrift.
3. Wenn Sie die Zahlung bei der Buchung mit mehreren Kreditorenposten ausgleichen möchten, klicken Sie auf die Aktionen **Einträge anwenden**.
4. Wählen Sie die Zeilen mit den Posten aus, die mit dem Ausgleichsposten ausgeglichen werden sollen, und klicken Sie anschließend auf **Ausgleichs-ID setzen anwenden**.
5. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten. Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen.  

    Am unteren Rand der Seite **Debitorenpostenausgleich** sehen Sie einen spezifischen Betrag im Fenster **Angewendeter Betrag** und auch, ob die Buchung ausgeglichen ist.  
6. Wählen Sie die Schaltfläche **OK**. Die Seite **Verkaufsgutschrift** zeigt nun den Betrag der zu buchenden Gutschrift an, wobei gegebenenfalls Skonto berücksichtigt wird.
7. Buchen Sie die Gutschrift.

## <a name="to-apply-posted-customer-ledger-entries" />So gleichen Sie gebuchte Debitorenposten aus:
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Debitorenkarte für den Debitor mit den Posten, die Sie ausgleichen möchten.
3. Klicken Sie auf **Einträge** und wählen dann die Zeile mit dem Posten aus, den Sie ausgleichen möchten.
4. Wählen Sie die Aktion **Posten ausgleichen...** aus. Auf der Seite **Debitorenpostenausgleich** werden die offenen Posten für den Debitor angezeigt.
5. Wählen Sie die Zeilen mit den Posten aus, die mit dem Ausgleichsposten ausgeglichen werden sollen, und klicken Sie anschließend auf **Ausgleichs-ID setzen anwenden**. Aktion
6. Geben Sie in jeder Zeile im Feld **Ausgleichsbetrag** den Betrag ein, mit dem Sie den entsprechenden Posten ausgleichen möchten. Wenn Sie keinen Betrag eingeben, wird automatisch mit dem Höchstbetrag ausgeglichen.  

    Am unteren Rand der Seite **Debitorenpostenausgleich** wird im Feld **Ausgleichsbetrag** der spezifische Betrag angezeigt.  
7. Wählen Sie die Aktion **Ausgleich buchen** aus. Die Seite **Ausgleich buchen** wird mit der Belegnummer des Ausgleichspostens und dem Buchungsdatum des Postens angezeigt, der das aktuellste Buchungsdatum aufweist.  
8. Klicken Sie auf die Schaltfläche **OK**, um den Ausgleich zu buchen.

    Wenn der gebuchte Ausgleich abgeschlossene Debitorenposten zur Folge hat, wird für diese Posten im Feld **Offen** kein Häkchen mehr angezeigt.    
9. Um die Sachkonto-Einträge zu sehen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link. Wechseln Sie zur Karte für den jeweiligen Debitor, um die Buchungsposten zu sehen.  

Sie können in der Liste der Posten sehen, dass in der Zeile mit dem vollständig ausgeglichenen Posten das Feld **Offen** nicht aktiviert ist.  

> [!NOTE]  
>   Nachdem Sie auf der Seite **Debitorenpostenausgleich** einen Posten oder mehrere Posten durch **Festlegen der Ausgleichs-ID** ausgewählt haben, enthält das Feld **Ausgleichsbetrag** die Summe der Restbeträge für die ausgewählten gebuchten Posten, es sei denn, das Feld enthält bereits Informationen. Wenn Sie **Auf Älteste Anwenden** im Feld **Anwendungsmethode** auf der Debitorenkarte auswählen, tritt die Anwendung automatisch auf.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another" />So gleichen Sie Debitorenposten in verschiedenen Währungen untereinander aus:
Wenn Sie an einen Debitor in einer Währung verkaufen und die Zahlung in einer anderen Währung erhalten, können Sie dennoch die Rechnung mit der Zahlung ausgleichen.  

Im Folgenden finden Sie ein Beispiel. Sie wenden Eintrag 1 in einer Währung auf Eintrag 2 in einer anderen Währung an. Das Buchungsdatum in Eintrag 1 wird verwendet, um den Wechselkurs zu ermitteln, der zum Umrechnen der Beträge in Eintrag 2 verwendet werden soll. Den relevanten Wechselkurs finden Sie auf der Seite **Währungswechselkurse**.  

Das Ausgleichen von Debitorenposten in verschiedenen Währungen muss aktiviert sein. Weitere Informationen finden Sie unter [ Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren](finance-how-enable-application-ledger-entries-different-currencies.md)  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Zlg.-Eing. Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie das gewünschte Buch.-Blatt, und füllen Sie unter Verwendung eines Währungscodes die erste Zeile aus.
3. Wählen Sie die Aktion **Posten ausgleichen...** aus.
4. Klicken Sie auf die Zeile mit dem Posten, mit dem Sie den Posten im Zahlungsausgangs-Buch.-Blatt ausgleichen möchten. Klicken Sie dann auf **Ausgleichs-ID festlegen** und wählen Sie den auszugleichenden Posten aus.
5. Wählen Sie die Schaltfläche **OK**, um zum Barzahlungseingangsbuch zurückzukehren.
6. Buchen Sie das Verkaufs Buch.-Blatt.  

> [!IMPORTANT]  
>   Wenn Sie Posten in verschiedenen Währungen miteinander ausgleichen, rechnet die Anwendung die Beträge in USD um. Selbst wenn der Wechselkurs fest ist, z. B. zwischen USD und EUR, kann es zu Rundungsdifferenzen kommen, wenn diese Fremdwährungsbeträge in USD umgerechnet werden. Diese Rundungsdifferenzen werden als Gewinne und Verluste auf die Konten gebucht, die in den Feldern **Kursgewinn realisiert** oder **Kursverlust realisiert** der Seite **Währungen** angegeben sind. Außerdem werden die Beträge im Feld **Betrag (USD)** der entsprechenden Kreditorenposten angepasst.  

## <a name="to-correct-an-application-of-customer-entries" />So heben Sie den Ausgleich von Debitoren- oder Kreditorenposten auf
Wenn Sie einen Antrag korrigieren, werden Korrekturbuchungen für alle Buchungen erstellt und gebucht. Die Korrektureinträge sind die gleichen wie die Originale, haben aber ein entgegengesetztes Protokoll im **Menge**-Bereich. Die Korrekturbuchungen umfassen alle aus der Anwendung abgeleiteten Hauptbucheinträge. Zum Beispiel Skonto und Währungsgewinne/-verluste. Die von der Anwendung geschlossenen Posten werden erneut geöffnet.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die relevante Debitorenkarte.
3. Wählen Sie die Aktion **Posten** aus.
4. Wählen Sie den entsprechenden Posten aus, und wählen Sie die Aktionen **Ausgleich aufheben**.
5. Alternativ wählen Sie die Aktion **Detaillierte Posten** aus.
6. Wählen Sie den entsprechenden Ausgleichsposten aus, und wählen Sie die Aktionen **Ausgleich aufheben**.
7. Füllen Sie die Felder im Kopf aus, und wählen Sie dann die Aktion **Aufheben** aus.  

> [!IMPORTANT]  
>   Wenn ein Posten durch mehrere Ausgleichsposten ausgeglichen wurde, müssen Sie zuerst den Ausgleich des letzten Ausgleichspostens aufheben.  

## <a name="see-also" />Weitere Informationen
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
