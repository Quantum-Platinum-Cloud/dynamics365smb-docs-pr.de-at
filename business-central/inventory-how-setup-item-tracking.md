---
title: 'Artikelverfolgung mit Serien-, Chargen- und Paketnummern einrichten'
description: 'Artikelverfolgung mit Seriennummern, Chargennummern und Paketnummern einrichten'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/31/2021
ms.author: edupont
---
# <a name="set-up-item-tracking-with-serial-lot-and-package-numbers" />Artikelverfolgung mit Serien-, Chargen- und Paketnummern einrichten

Behalten Sie den Überblick über Lagerartikel auch in komplexen Lagerkonfigurationen mit Nummern, die für jeden Artikel spezifisch sind, entweder als einzelnes Objekt, als Charge oder als Paket. Mit der Artikelverfolgung können Sie Artikel über interne Lagerbewegungen sowie ausgehende und eingehende Dokumente verfolgen.

Gibt gebuchte Serien- und Chargennummern an, die in einer Lieferkette vorwärts oder rückwärts verfolgt werden können. Dies ist für allgemeine Maßnahmen für die Qualitätssicherung und für Rückrufe eines fehlerhaften Produktes nützlich. Weitere Informationen finden Sie unter [Nachverfolgte Artikel reservieren](inventory-how-to-trace-item-tracked-items.md).  

> [!TIP]
> Schalten Sie im 1. Veröffentlichungszyklus 2021 und später die Funktionsaktualisierung *Verwenden Sie die Nachverfolgung nach Paketnummer im Reservierungs‑ und Nachverfolgungssystem* ein, wenn Sie mit Paketnummern sowie Serien‑ und Chargennummern arbeiten möchten. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](admin-feature-management.md). Sobald die Funktion aktiviert ist, können Sie ausgehenden und eingehenden Dokumenten Paketnummern zuweisen, ähnlich wie Sie mit Chargennummern arbeiten können.  

## <a name="numbers-and-item-tracking" />Zahlen‑ und Artikelverfolgung

Im Rahmen Ihrer Lagerprozesse können Sie Ihren Lagerbestand in Paketen, Kartons, Containern usw. bündeln. Um den Überblick über die Artikel zu behalten, weisen Sie eindeutige Nummern als Identifikation zu. Sie stellen beispielsweise einen Stuhl mit der Artikelnummer *1900-S* her und verkaufen ihn. Jeder einzelne Stuhl hat eine Seriennummer, *1001*, aber Sie bündeln auch vier Stühle zu einer Charge, *LOT0001*, und Sie versenden die Stühle in einem Container mit der Paketnummer *CONTAINER010*. Das schließt auch andere Elemente ein, wie z. B. *LOT0100* mit Beistelltischen und *LOT200* mit Lampen.  

Abhängig von Ihrer Konfiguration verwenden Sie diese unterschiedlichen Nummern, um den Lagerbestand in [!INCLUDE [prod_short](includes/prod_short.md)] in den verschiedenen Phasen des Einkaufs, Verkaufs, Lagerbetriebs usw. zu verfolgen.

## <a name="to-set-up-item-tracking-codes" />Um Artikelverfolgungscodes einzurichten

Ein Artikelverfolgungscode spiegelt die unterschiedlichen Betrachtungen wider, die ein Unternehmen bezüglich der Verwendung von Serien- und Chargennummern von Artikeln anstellt, die sich durch das Lager bewegen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Artikelverfolgungen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. In den Inforegistern **Seriennr.**, **Chargennr.**, und der **Paketnr.** definieren Sie die Vorgehensweisen zur Artikelverfolgung nach Serien-, Chargen‑ und Paketnummern.  

> [!NOTE]  
> Wenn Sie bestimmte Artikel oder bestimmte Chargen während der Lebensdauer verfolgen möchten, müssen Sie die Felder **Seriennr.-spezifische Verf.** und **Chargennr.-spezifische Verf.** auswählen, fest. Wenn Sie eine ausgehende Einheit eines Artikels mit dem Artikelverfolgungscode verarbeiten, müssen Sie immer angeben, welche vorhandene Seriennummer oder welche vorhandene Chargennummer betroffen sein soll. Das bedeutet, dass der Artikel, von dem eine gewissen Menge verkauft wird, aus einem bestimmten Bereich von Seriennummern im Lagerbestand entnommen werden muss. Mit anderen Worten: die Seriennummer, die einem Artikel beim Wareneingang zugewiesen wurde, muss genau derjenigen beim Warenausgang entsprechen.

Da dieses Einrichtungsfeld alle möglichen Transaktionen für den Artikel abdeckt, werden die einzelnen Felder für Eingang und Ausgang ebenfalls mit Häkchen versehen. Die einzelnen Eingangs- und Ausgangsfelder haben aber nichts mit dem Ausgleich innerhalb des Lagers zu tun – sondern sie haben lediglich die Aufgabe, den Arbeitsablauf eines Unternehmens bezüglich der Zuweisung von Artikelverfolgungsnummern abzubilden.  

> [!NOTE]  
> Um Artikelverfolgungsnummern bei Lageraktivitäten zuzuordnen, müssen die Felder **Seriennr.-Verf. Lager** und **Chargennr.-Verf. Lager** auf der Karte des Artikels ausgewählt werden.  

## <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers" />Regeln für den Ablauf von Serien- oder Chargennummern einrichten:

Für einige Artikel möchten Sie möglicherweise spezielle Ablaufdaten und Regeln in dem Artikelverfolgungscode festlegen. Diese Funktionalität ermöglicht Ihnen nachzuvollziehen, wann bestimmte Serien- und Chargennummern ablaufen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Artikelverfolgungen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie einen bestehenden Artikelverfolgungscode aus bestehenden Artikelkarten aus, und wählen die Aktion **Bearbeiten**.  
3. Aktivieren Sie im Inforegister **Sonst.** die folgenden Felder:  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Fixes Ablaufdatum**|Gibt an, dass ein Ablaufdatum, das der Artikelverfolgungsnummer beim Wareneingang zugewiesen wurde, beim Warenausgang berücksichtigt werden muss.|  
    |**Ablaufdatumseintrag anfordern**|Gibt an, dass Sie in der Artikelverfolgungszeile ein Ablaufdatum eingeben müssen.|  
    |**Ablaufdatumsangaben verwenden**|Gibt an, dass Sie keine Ablaufdatumsangaben berechnen möchten. |  

## <a name="to-set-up-warranties-for-serial-or-lot-numbers" />Garantien für Serien- oder Chargennummern einrichten:

Für einige Artikel möchten Sie möglicherweise spezielle Garantievereinbarungen in dem Artikelverfolgungscode festlegen. Diese Funktionalität ermöglicht Ihnen nachzuvollziehen, wann die Garantien auf spezielle Serien- oder Chargennummern in Ihrem Lager auslaufen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Artikelverfolgungen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie einen bestehenden Artikelverfolgungscode aus bestehenden Artikelkarten aus, und wählen die Aktion **Bearbeiten**.  
3. Füllen Sie im Inforegister **Sonstiges** das Feld **Garantiedatumsformel** aus, und markieren Sie die Felder wie folgt:  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Garantiedatumsformel**|Gibt das letzte Garantiedatum für den Artikel an.|  
    |**Garantiedatumseintrag anfordern**|Zeigt an, dass Sie in der Artikelverfolgungszeile manuell ein Garantiedatum eingeben müssen.|  


## <a name="to-set-up-items-for-tracking-with-the-correct-item-tracking-codes" />So richten Sie Artikel für die Verfolgung mit den richtigen Artikelverfolgungscodes ein

Um die Artikelverfolgung zu aktivieren, müssen Sie einem Artikel zunächst die Artikelverfolgungscodes zuweisen. Es gibt zwei Möglichkeiten, Artikelverfolgungscodes hinzuzufügen, indem Sie den Code aus einer vordefinierten Liste auswählen oder einen neuen eindeutigen Code zuweisen. Zeigen Sie mit der Maus auf die Felder, um eine Kurzbeschreibung zu lesen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Element** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie einen vorhandenen Artikel aus der Liste aus, und öffnen Sie die Seite **Artikelkarte**.  
3. Weisen Sie im Inforegister **Artikelverfolgung** die entsprechenden Artikelverfolgungscodes zu, und wählen Sie den **Artikelverfolgungscode**, die **Seriennummern** und die **Chargennummern** aus.
    1. Alternativ können Sie auch einen neuen Artikelverfolgungscode erstellen, indem Sie die Aktion **Neu** auswählen.

## <a name="to-specify-opening-balances-for-the-items-you-track" />Um Anfangssalden für die von Ihnen verfolgten Artikel anzugeben

Sie können Anfangssalden für die von Ihnen verfolgten Artikel erstellen. Da Sie verschiedene Lagerkonfigurationen wählen können, gibt es zwei Möglichkeiten:

* Aktivieren Sie bestimmte Stapel auf der Seite **Artikel Buch.-Blatt**, auf der Serien-, Chargen- und Verpackungsdaten direkt in Buchungsblattzeilen eingeben können.
* Für Standorte, an denen der Umschalter **Gezieltes Einlagern und Kommissionieren** eingeschaltet ist, verwenden Sie die Seite **Logistik Inventur Buch.-Blatt** , um alle Artikelverfolgungsfelder verfügbar zu machen. Zu den verfügbaren Feldern gehören die Felder **Garantiedatum** und **Ablaufdatum**.

### <a name="item-journals" />Artikel-Blätter

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Element Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Feld **Name** aus, um eine Liste der Artikel Buch.-Blattnamen zu öffnen.
3. Wählen Sie **Neu**, um einen neuen Stapel zu erstellen, und schalten Sie dann den Umschalter **Artikelverfolgung auf Positionen** ein.
4. Wählen Sie **OK**, um den von Ihnen erstellten Stapel auszuwählen.
5. Füllen Sie die Felder auf der Artikel Buch.-Blattzeile wie erforderlich aus. Beachten Sie, dass die Felder **Chargennr.**, **Seriennr.**, **Ablaufdatum**, **Garantiedatum** und **Paketnr.** zur Verfügung stehen, (wenn das Feature aktiviert ist).
6. Wählen Sie die Aktion **Buchen** aus, um das Lager zu regulieren.

> [!NOTE] 
> [!INCLUDE [prod_short](includes/prod_short.md)] führt einige kleinere Überprüfungen durch, wenn Sie Daten eingeben oder importieren. Eine umfassendere Prüfung findet statt, wenn Sie Daten aus Buchuchungsblattzeilen auf das **Artikelverfolgungsfenster** buchen oder übertragen. Letzteres geschieht automatisch, wenn Sie die Seite **Artikelverfolgungsfenster** aus der Artikel Buch.-Blattzeile öffnen oder Sie die Aktion **Artikel Buch.-Blattzeilen aktualisieren**.

### <a name="warehouse-physical-inventory-journal-for-locations-where-directed-pick-and-put-away-is-turned-on" />Logistik Inventur Buch.-Blatt für Standorte, für welche dir direkte Kommissionierung und Einlagerung aktiviert ist

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Geben Sie **Logistik Inventur Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder auf der Artikel Buch.-Blattzeile wie erforderlich aus. Beachten Sie, dass die Felder **Chargennr.**, **Seriennr.**, **Ablaufdatum**, **Garantiedatum** und **Paketnr.** zur Verfügung stehen, (wenn das Feature aktiviert ist).
3. Wählen Sie die Aktion **Journal** aus, die Lagerregulierungen vorzunehmen. Denken Sie daran, dass die korrigierten Lagerplatzposten mit den entsprechenden Artikelposten synchronisieren müssen. Um mehr zu erfahren, gehen Sie zu [Die korrigierten Lagerplatzeinträge synchronisieren](/dynamics365/business-central/inventory-how-count-adjust-reclassify#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

Verwenden Sie für Massenimporte Konfigurationspakete, um Daten in die Blätter zu importieren.

> [!NOTE]
> Sie können **In Excel bearbeiten** nicht verwenden, um Buchungsblattzeilen mit Nachverfolgungsinformationen zu erstellen.

## <a name="see-related-microsoft-trainingtrainingmodulesprepare-item-tracking" />Siehe verwandte [Microsoft Schulungen](/training/modules/prepare-item-tracking/)

## <a name="see-also" />Siehe auch

[Arbeiten mit Chargennummern und Seriennummern](inventory-how-work-item-tracking.md)  
[Verfolgen von Artikeln mit Artikelverfolgung](inventory-how-to-trace-item-tracked-items.md)  
[Bestand](inventory-manage-inventory.md)  
[Designdetails: Artikelnachverfolgung](design-details-item-tracking.md)  
[Designdetails: Artikelverfolgung und Reservierungen](design-details-item-tracking-and-reservations.md)  
[Artikel reservieren](inventory-how-to-reserve-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
