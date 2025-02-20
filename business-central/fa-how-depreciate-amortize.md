---
title: FA abschreiben oder amortisieren
description: 'Sie müssen definieren, wie Sie jede Ihrer Anlagen, wie z. B. Maschinen und Geräte, über ihre Abschreibungsdauer abschreiben, abwerten oder amortisieren.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.search.form: '5610, 5611, 5629, 5633, 5659, 5660, 5663, 5619, 5666'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="depreciate-or-amortize-fixed-assets" />Anlagen abschreiben oder amortisieren

Abschreibung wird verwendet, um die Anschaffungskosten von Anlagen wie Maschinen und Ausrüstung über die Nutzungsdauer zu verteilen. Sie müssen für jede Anlage definieren, wie diese abgeschrieben wird.  

 Es gibt zwei Wege, Abschreibungen zu buchen:  

* Automatisch durch Ausführen der Stapelverarbeitung **AfA berechnen**  
* Manuell, unter Verwendung des Anlagen Fibu Buch.-Blattes.  

[!INCLUDE[prod_short](includes/prod_short.md)] kann tägliche Abschreibungen berechnen, sodass Sie Abschreibungen für beliebige Perioden berechnen können. Sie können damit das aktuelle operative Ergebnis beispielsweise auf monatlicher, quartalsweiser oder jährlicher Basis analysieren. Die Berechnungen verwendet ein standardisiertes Jahr mit 360 Tagen und einen standardisierten Monat mit 30 Tagen. Weitere Informationen finden Sie unter [AfA-Methoden](fa-depreciation-methods.md).  

Falls eine Anlage von verschiedenen Abteilungen verwendet wird, kann die AfA automatisch entsprechend einer benutzerdefinierten Tabelle auf diese Abteilungen verteilt werden.  

Sie können falsche AfA-Posten aus einem AfA-Buch mit Hilfe der Stapelverarbeitung **Anlagenposten stornieren** stornieren. Danach können Sie die korrekten Beträge buchen, indem Sie die Stapelverarbeitung **AfA berechnen** erneut ausführen. Wenn Sie Fehler korrigieren, werden diese als Anlagenstornoposten gebucht.  

Die Indexierung wird verwendet, um die Werte allgemeinen Preisänderungen anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um die AfA-Beträge neu zu berechnen.  

## <a name="to-calculate-depreciation-automatically" />So berechnen Sie AfA automatisch

Einmal monatlich oder in beliebigen anderen Intervallen können Sie die Stapelverarbeitung **AfA berechnen** ausführen. Der Stapelverarbeitungsjob ignoriert Anlagen, die verkauft wurden, auf der Anlagenkarte gesperrt oder inaktiv sind, und Anlagen, die die AfA-Methode "Manuell" verwenden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **AfA berechnen** ein, und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie die Schaltfläche **OK** aus.  

    Die Stapelverarbeitung berechnet die AfA und erstellt Zeilen im Anlagen Fibu Buch.-Blatt.

4. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen Fibu Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link.  

    Auf der Seite **Anlagen-Fibu Buch.-Blatt** können Sie im Feld **Anzahl AfA-Tage** sehen, wie viele AfA-Tage berechnet wurden.  
5. Wählen Sie die Aktion **Buchen** aus.  

> [!NOTE]
> Bekannte Einschränkung: Wenn Sie das Feld **Anzahl der Tage erzwingen** auf Ja festlegen und das Feld **Anzahl der Tage erzwingen** auf einen Wert festgelegt ist, bei dem **Buchungsdatum** minus **Anzahl der Tage** ein Datum im vorherigen Kalenderjahr ergibt, lässt das System Sie die Abschreibung nicht buchen.
> Sie können dies vermeiden, indem Sie das Feld **Anzahl der Tage** auf höchstens die berechneten Tage bis zum Buchungsdatum mit 30 Tagen/Monat reduzieren ODER das Flag **Geschäftsjahr 365 Tage** im AfA-Buch festlegen.
> Wir empfehlen die erste Option, da Sie die Verwendung von 30 Tagen/Monaten für die Abschreibung möglicherweise nicht ändern möchten. Weitere Informationen finden Sie unter [Feld 365 Tage Geschäftsjahr Abschreibung](fa-how-setup-depreciation.md#fiscal-year-365-days-field-depreciation).


## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal" />So buchen Sie eine AfA aus dem Anlagen Fibu Buch.-Blatt

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen-Fibu Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2. Erstellen Sie eine ursprüngliche Buch.-Blattzeile und füllen Sie die notwendigen Felder aus.  
3. Wählen Sie im Feld **Anlagenbuchungsart** die **AfA**.  
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die AfA-Buchung eingerichtet ist. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Wählen Sie die Aktion **Buchen**, um das Journal zu buchen.  

Das Feld **Buchwert** auf der Seite **Anlagenkarte** wird entsprechend aktualisiert.

Falls Sie Anlagenverteilungsschlüssel eingerichtet haben, um Beträge auf verschiedene Kostenstellen und/oder Kostenträger zu verteilen, werden die Beträge während der Buchung zugeordnet. Weitere Informationen finden Sie unter [Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).  

## <a name="to-manage-the-ending-book-value" />So werden Erinnerungswerte verwaltet

Im Feld **Erinnerungswert** auf der Seite **Anlagenabschreibungsbücher** können Sie den Buchwert angeben, den Ihre Anlage im aktuellen Abschreibungsbuch haben soll, nachdem es vollständig abgeschrieben wurde. Sie können dies manuell tun oder Sie können das Feld **Standarderinnerungswert** auf der zugehörigen Seite **AfA-Buch** ausfüllen, womit dann das Feld automatisch ausgefüllt wird.

> [!NOTE]
> Wenn die letzte Abschreibung bedeutet, dass das Feld **Buchwert** auf der Seite **Anlagenkarte** null ist, wird die letzte Abschreibung automatisch um diesen Betrag reduziert.<br /><br />
> Wenn der Wert im Feld **Buchwert** nach der letzten Abschreibung größer als null ist, beispielsweise wegen eines Rundungsproblems oder weil ein Restwert besteht, wird der Wert im Feld **Erinnerungswert** auf der Seite **Anlagen-AfA-Bücher** ignoriert. Weitere Informationen finden Sie unter [Wie der Restwert zusammen mit den Anschaffungskosten gebucht wird](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal" />So berechnen Sie Verteilungen in Anlagen Fibu Buch.-Blättern

Falls eine Anlage von verschiedenen Kostenstellen verwendet wird, kann die AfA automatisch entsprechend einer benutzerdefinierten Tabelle auf diese Kostenstellen verteilt werden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Anlagen-Fibu Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2. Erstellen Sie eine ursprüngliche Zeile und füllen Sie die notwendigen Felder aus.
3. Wählen Sie im Feld **Anlagenbuchungsart** die **Verteilung**.  
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die Buchung einer Verteilung eingerichtet wird.  
5. Wählen Sie die Aktion **Buchen**, um das Journal zu buchen.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books" />Kopiervorgänge zum Vorbereiten von Buchungen in mehrere AfA-Bücher verwenden

Ausfüllen der Zeilen in einem Buch.-Blatt für die Buchung auf ein AfA-Buch und anschließendes Kopieren der Zeilen in ein anderes Buch.-Blatt, von wo aus sie auf ein anderes AfA-Buch gebucht werden können Weitere Informationen finden Sie unter [So buchen Sie Posten auf verschiedene Abschreibungsbücher](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Afa-Bücher** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie das entsprechende AfA-Buch aus und aktivieren Sie dann das Kontrollkästchen **Teil des Kopiervorgangs**.  

> [!IMPORTANT]  
>   Wenn Sie das Feld **Kopiervorgang aktivieren** aktiviert haben, dürfen Sie im Buch.-Blatt keine Nummernserien verwenden. Der Grund dafür ist, dass die Nummernserie für das Anlagen Fibu Buch.-Blatt nicht der Nummernserie im Anlagen Buch.-Blatt entspricht.  

## <a name="to-post-entries-to-different-depreciation-books" />So buchen Sie Posten auf verschiedene AfA-Bücher

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Anlagen-Fibu Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2. Aktivieren Sie im Buch.-Blatt, das Sie zum Buchen der AfA verwenden möchten, das Kontrollkästchen **Kopiervorgang aktivieren**.  
3. Füllen Sie die verbleibenden Felder je nach Bedarf aus.  
4. Wählen Sie die Aktion **Buchen** aus.  
5. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **FA-Erfassungen Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.  

    > [!NOTE]  
    >   Auf der Seite **Anlagen Buch.-Blatt** enthält neue Zeilen für verschiedene AfA-Bücher entsprechend der Verdopplungsliste.  
6. Prüfen oder bearbeiten Sie die Zeilen, und wählen Sie dann die Aktion **Buchen** aus.  

    > [!NOTE]  
    >   Eine andere Art, einen Posten in ein anderes Buch zu kopieren, ist es, einen AfA-Buchcode in dem Feld **In AfA-Buch kopieren** anzugeben, wenn Sie eine Buch.-Blattzeile ausfüllen.  

Sie können mit Hilfe der Stapelverarbeitung **AfA-Buch kopieren** Posten von einem AfA-Buch in ein anderes AfA-Buch kopieren. Die Stapelverarbeitung erstellt Buch.-Blattzeilen in dem Buch.-Blatt, das Sie auf der Seite **Anlagen Buch.-Blatt Einr.** für das AfA-Buch angegeben haben, aus dem Sie kopieren möchten. Weitere Informationen finden Sie in der folgenden Prozedur.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books" />So kopieren Sie Anlagenposten zwischen AfA-Büchern

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Afa-Bücher** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die entsprechende AfA-Buch - Karte und wählen Sie dann die Aktion **AfA-Buch kopieren**.  
3. Füllen Sie im Inforegister **AfA-Buchkarte kopieren** die Seite nach Bedarf aus.  
4. Wählen Sie die Schaltfläche **OK**.  

Die kopierten Zeilen werden entweder in einem Anlagen Fibu Buch.-Blatt oder im Anlagen Buch.-Blatt erstellt. Dies hängt davon ab, ob das AfA-Buch, das Sie kopieren, in der Finanzbuchhaltung aktiviert wurde.  

## <a name="see-related-microsoft-trainingtrainingmodulescalculate-post-depreciations" />Siehe verwandte [Microsoft Schulungen](/training/modules/calculate-post-depreciations/)

## <a name="see-also" />Siehe auch

[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
