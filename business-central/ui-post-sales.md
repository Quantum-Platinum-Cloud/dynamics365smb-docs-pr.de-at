---
title: Verkaufsbelege buchen
description: Erfahren Sie mehr über die verschiedenen Buchungsfunktionen zum Buchen von Verkaufsbelegen und wie Sie gebuchte Belege aktualisieren können.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: '130, 142, 1350'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="posting-sales" />Verkäufe buchen

Unter dem Menü **Buchen** in einem Verkaufsbeleg auswählen können Sie zwischen den folgenden Buchungsfunktionen auswählen:

* **Veröffentlichen**
* **Buchen und neu**
* **Buchen und senden**
* **Buchungsvorschau**
* **Stapelbuchung**
* **Testbericht**

> [!NOTE]
> Bei Kundenaufträgen werden auch Optionen für die Vorauszahlungsfunktion angezeigt. Weitere Informationen finden Sie unter [Vorauszahlungen in Rechnung stellen](finance-invoice-prepayments.md).

Wenn Sie alle Zeilen ausgefüllt und alle Daten des Verkaufsauftrags eingegeben haben, können Sie ihn buchen. Dies erstellt eine Lieferung und eine Rechnung.

Wenn eine Verkaufsbestellung gebucht wird, wird das Debitorenkonto, die Finanzbuchhaltung und die Artikelposten aktualisiert.

Für jeden Verkaufsauftrag wird ein Verkaufsposten in der Tabelle **Sachposten** erzeugt. Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Sachposten im entsprechenden Einkaufskonto. Zusätzlich kann das Buchen in einem MwSt.-Posten und einem Sachposten für den Rabattbetrag resultieren. Ob ein Posten für Rabatt gebucht wird, hängt von den Einstellungen im Feld **Rabattbuchung** auf der Seite **Debitoren & Verkauf Einr.** ab.

Für jede Zeile des Verkaufsauftrags wird ein Artikelposten in der Tabelle **Artikelposten** erzeugt (wenn die Verkaufszeilen Artikelnummern enthalten) oder es wird ein Sachposten in der Tabelle **Sachposten** erzeugt (wenn die Verkaufszeilen Sachkonten enthalten). Zusätzlich dazu werden Verkaufsaufträge immer in den Tabellen **Verkaufslieferkopf** und **Verkaufsrechnungskopf** gespeichert.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Sie können entweder buchen oder buchen und senden. Wenn Sie die Option wählen, zu buchen und zu senden, wird eine PDF-Datei generiert, die Sie dann senden können. Sie können auch die Funktion **Stapelbuchen** wählen, mit der Sie mehrere Aufträge gleichzeitig buchen können. Weitere Informationen finden Sie unter [Mehrere Dokumente gleichzeitig bereitstellen ](ui-batch-posting.md).

## <a name="viewing-ledger-entries" />Anzeigen von Posten

Wenn die Buchung vollständig ist, werden die gebuchten Verkaufszeilen aus der Bestellung entfernt. Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist. Im Anschluss können Sie die gebuchten Posten auf den verschiedenen Seiten einsehen, die gebuchte Posten enthalten, einschließlich **Debitorenposten**, **Sachposten**, **Artikelposten**, **Lagerplatzposten**, **Geb. Verkaufsrechnung**.  

In den meisten Fällen können Sie Posten von der betroffenen Karte oder dem betroffenen Beleg aus öffnen. Auf der Seite **Debitorenkarte** wählen Sie beispielsweise die Aktion **Posten** aus.

## <a name="editing-ledger-entries" />Bearbeiten von Posten

Sie können bestimmte Felder in gebuchten Einkaufsbelegen bearbeiten, z. B. die **Paketverfolgungsnr.** Feld eingetragen. Weitere Informationen finden Sie unter [Gebuchte Belege bearbeiten](across-edit-posted-document.md). Bei kritischeren Feldern, die sich auf den Überwachungspfad auswirken, müssen Sie die Buchung stornieren oder rückgängig machen. Weitere Informationen finden Sie unter [Buchungen stornieren und Belege/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md).

## <a name="see-related-microsoft-trainingtrainingmodulesship-invoice-items-dynamics-365-business-centralindex" />Siehe verwandte [Microsoft Schulungen](/training/modules/ship-invoice-items-dynamics-365-business-central/index)

## <a name="see-also" />Siehe auch

[Verkauf](sales-manage-sales.md)  
[Mehrere Dokumente gleichzeitig buchen](ui-batch-posting.md)  
[Gebuchte Belege bearbeiten](across-edit-posted-document.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Ändern oder Löschen einer unbezahlten Verkaufsrechnung](sales-how-correct-cancel-sales-invoice.md)  
[Suchen von Seiten und Informationen mit Wie möchten Sie weiter verfahren](ui-search.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
