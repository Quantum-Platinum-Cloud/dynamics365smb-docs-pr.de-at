---
title: Intercompany-Ein- und -Ausgangstransaktionen verwalten
description: 'Intercompanytransaktionen, die Sie von Intercompanypartnern empfangen, werden im IC-Eingang aufgelistet, in dem Sie sie manuell oder automatisch bearbeiten.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
ms.date: 03/09/2022
ms.author: edupont
---
# <a name="manage-the-intercompany-inbox-and-outbox" />Intercompany-Ein- und -Ausgangstransaktionen verwalten
Alle Intercompanytransaktionen, die Sie auf elektronischem Wege von Intercompanypartnern empfangen, werden im Intercompanyeingang aufgelistet.  

Je nachdem, wie Intercompany für Ihr Unternehmen eingerichtet ist, werden einige Transaktionen jedoch automatisch an die relevanten Intercompany-Partner repliziert. Ab dem 1. Veröffentlichungszyklus 2022 können Sie das Unternehmen für die automatische Erstellung empfangener Intercompany-Transaktionen von Intercompany-Partnern einrichten, die über das Intercompany-Hauptbuch gebucht werden. Weitere Informationen finden Sie unter [Intercompany-Buch.-Blätter ausfüllen und buchen](intercompany-how-work-documents-journals.md#to-fill-in-and-post-an-intercompany-journal).  

## <a name="organizing-the-inbox" />Strukturieren des Eingangs
 Mit Hilfe der Filterfelder im oberen Bereich des Fensters Eingang können Sie festlegen, welche Transaktionen auf der Seite angezeigt werden. Wenn Sie beispielsweise nur die von einem bestimmten Partner erstellten Transaktionen anzeigen möchten, können Sie die entsprechenden Filterkriterien in den Feldern **Transaktionsursprung** und **Intercompanypartnercode** festlegen.  

### <a name="transaction-source" />Transaktionsursprung
Welche Möglichkeiten Sie bei der Verwendung einer Transaktion haben, ist davon abhängig ob es sich dabei um eine Transaktion handelt, die:  

- Vom intercompanypartner erstellt oder  
- Vom intercompanypartner abgelehnt und an Sie zurückgesandt wurde.  

Das Feld **Transaktionsursprung anzeigen** kann zum Filtern der Transaktionen im Fenster **Intercompany-Eingangstransaktionen** verwendet werden, sodass auf dieser Seite nur Transaktionen des festgelegten Typs angezeigt werden. (Darüber hinaus können Sie nach Intercompanypartner oder nach dem Inhalt des Feldes **Zeilenaktion** filtern.)  

#### <a name="created-by-intercompany-partner" />Vom Intercompanypartner erstellt
 Wenn Sie eine neue Transaktion empfangen, die vom Partner erstellt wurde, haben Sie folgende Möglichkeiten:

- Transaktion akzeptieren  
- Transaktion ablehnen (an Partner zurücksenden)  
- Transaktion abbrechen (löschen, ohne sie an den Partner zurückzusenden)  

#### <a name="returned-from-intercompany-partner" />Von Intercompanypartner zurückgesendete Transaktion
 Wenn die Transaktion vom Intercompanypartner abgelehnt wurde, können Sie sie nur im Eingang abbrechen. Anschließend müssen Sie Korrekturzeilen erstellen oder das Buch.-Blatt oder den Beleg im Unternehmen stornieren.  

## <a name="recreating-inbox-entries" />Neuerstellen von Eingangsposten
 Wenn Sie eine Transaktion im Eingang akzeptiert, anschließend aber den Beleg oder das Buch.-Blatt gelöscht haben, statt diese zu buchen, können Sie den Eingangsposten neu erstellen und erneut akzeptieren.  

## <a name="get-an-overview-of-intercompany-transactions-for-a-period" />Anzeigen einer Übersicht über die Intercompanytransaktionen eines bestimmten Zeitraums
 Die Intercompanytransaktionen, die Sie in einem bestimmten Zeitraum empfangen oder versendet haben, können in einer Übersicht angezeigt werden. Im Bericht **Intercompanytransaktionen** werden alle Intercompanysachposten, Debitorenposten und Kreditorenposten aufgelistet.

 > [!NOTE]  
 > Wenn die Intercompanypartner sich in derselben Datenbank befinden, werden Transaktionen übertragen, ohne dass Dateien oder E-Mail erforderlich sind. Siehe Feld **Transfertyp** auf der Seite **Intercompanypartner**. <br /><br />
In diesem Fall können Sie eine Überbrückung des Eingangs und Ausgangs durch das System festlegen, indem Sie das Kontrollkästchen **Transaktionen autom. akzeptieren** auf der Seite **Intercompanypartner** und das Kontrollkästchen **Transaktionen autom. senden** auf der Seite **Intercompanyeinrichtung** auswählen. Eingehende Intercompanytransaktionen können nur dann automatisch akzeptiert werden, wenn der Aufgabenplaner aktiviert ist. Weitere Informationen finden Sie unter [Business Central Server konfigurieren – Aufgabenplanungseinstellungen](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Task).

## <a name="import-intercompany-transactions-from-a-file" />Intercompanytransaktionen aus einer Datei importieren

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Wenn einer der Intercompanypartner sich nicht in derselben Datenbank wie das eigene Unternehmen befindet, können die Intercompanytransaktionen von diesem Partner in einer XML-Datei empfangen werden. Anschließend werden die Transaktionen in den Eingang importiert.  

1. Speichern Sie die Datei in dem Verzeichnis, das Sie im Feld **Intercompanyeingangsdetails** angegeben haben, als Sie Intercompany eingerichtet haben.  
2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Intercompany-Eingangstransaktionen** ein und wählen Sie dann den zugehörigen Link.
3. Wählen Sie auf der Seite **Intercompany-Eingangstransaktionen** die **Transaktionsdatei importieren**-Aktion aus.  
4. Wählen Sie auf der angezeigten Seite die XML-Datei mit den Transaktionen aus, und wählen Sie dann **Öffnen**.  

Die Transaktionen werden in den Eingang importiert und können nun verarbeitet werden.

## <a name="process-incoming-intercompany-transactions" />So verarbeiten Sie eingehende Intercompanytransaktionen
Wenn Intercompanypartner Intercompanytransaktionen an Sie senden, werden diese Transaktionen im Intercompanyeingang abgelegt. Sie müssen die einzelnen Transaktionen im Eingang bewerten und entsprechend verarbeiten.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Intercompany-Eingangstransaktionen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Intercompany-Eingangstransaktionen** eine Zeile aus, und wählen Sie anschließend eine Aktion, wie **Akzeptieren** aus, um die Zeile zu verarbeiten.
3. Füllen Sie auf der Seite **IC-Eingangsvorgang abschl.** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die Schaltfläche **OK**.  

Für Zeilen, die bei der Aktion **Akzeptieren** verarbeitet wurden, werden Beleg- oder Buch.-Blattzeilen in Ihrem Unternehmen erstellt. Öffnen Sie die Belege oder Buch.-Blätter, nehmen Sie die erforderlichen Änderungen vor, und buchen Sie sie anschließend.  

Zeilen, die Sie mit der **n Partner zurück**-Aktion verarbeitet haben, werden in den Ausgang verschoben, von dem aus diese dann an Ihren Partner gesendet werden kann.

Für Zeilen, die Sie mit der Aktion **Zurückgesendet durch Partner** verarbeitet haben, müssen Sie nun eine Korrektur in die ursprünglich in Ihrem Unternehmen gebuchte Transaktion buchen.

## <a name="to-process-outgoing-intercompany-transactions" />So verarbeiten Sie ausgehende Intercompanytransaktionen
Wenn Sie Intercompany-Buch.-Blätter oder -Belege buchen oder Intercompanybestellbestätigungen senden, werden die Transaktionen an den Intercompanyausgang gesendet. Damit sie an die Intercompanypartner gesendet werden, müssen Sie den Ausgang öffnen und die Transaktionen verarbeiten.  

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Intercompany-Ausgangstransaktionen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Intercompany-Ausgangstransaktionen** eine Zeile aus, und wählen Sie anschließend eine Aktion, wie **Zurück in Eingang** aus, um die Zeile zu verarbeiten.

Zeilen, die Sie mit der **An Intercompanypartner senden**-Aktion verarbeiten, werden an den Eingang des Partners gesendet.

Zeilen, die Sie mit der **Zurück in Eingang**-Aktion verarbeiten, werden in den Eingang verschoben, wo Sie sie akzeptieren können, um Belege oder Buch.-Blattzeilen in Ihrem Unternehmen zu erstellen.  

Für Zeilen, die Sie mit der Aktion **Abbrechen** verarbeitet haben, müssen Sie nun eine Korrektur in die ursprünglich in Ihrem Unternehmen gebuchte Transaktion buchen.  

## <a name="recreate-intercompany-inbox-transactions" />So erstellen Sie Intercompanyeingangstransaktionen neu
Gelegentlich sollten Sie eine Transaktion im Ein- oder Ausgang neu erstellen. Wenn Sie z. B. eine Transaktion im Eingang akzeptiert, den Beleg oder das Buch.-Blatt anschließend jedoch statt zu buchen gelöscht haben, können Sie den Eingangsposten erneut erstellen und akzeptieren.  

In der folgenden Schrittfolge wird beschrieben, wie Eingangstransaktionen neu erstellt werden. Bei Ausgangstransaktionen wird jedoch gleichermaßen verfahren.

  1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Bearbeitete IC-Eingangstransaktionen** ein und wählen Sie dann den zugehörigen Link.  

  2.  Wählen Sie auf der Seite **Bearbeitete IC-Eingangstrans.** die Zeile mit der Transaktion aus, die im Eingang neu erstellt werden soll, und wählen Sie dann die Aktion **Eingangstransaktion neu erstellen** aus.  

## <a name="see-also" />Siehe auch
[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
