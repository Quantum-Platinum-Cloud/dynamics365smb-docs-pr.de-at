---
title: Einrichtung der Buchungsgruppe
description: 'Übersicht der Buchungsgruppen, die Sie verwenden können, um die Zeit zu sparen und Fehler zu vermeiden, wenn Sie Transaktionen buchen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'posting setup, initialize'
ms.search.form: '312, 313'
ms.date: 08/26/2022
ms.author: bholtorf
---
# <a name="set-up-posting-groups" />Buchungsgruppen einrichten

Buchungsgruppen bilden Entitäten auf Hauptbuchkonten ab. Beispiele für Entitäten sind Debitoren, Kreditoren, Artikel, Ressourcen sowie Verkaufs- und Einkaufsdokumente. Buchungsgruppen sparen Zeit und helfen, Fehler zu vermeiden, wenn Sie Transaktionen buchen. Die Umsatzwerte wechseln zu den Konten, die in der Buchungsgruppe für diese bestimmte Einheit angegeben werden. Die einzige Anforderung ist, dass Sie einen Kontenplan haben. Weitere Informationen finden Sie unter [Einrichten des Kontenplans](finance-setup-chart-accounts.md).  

Buchungsgruppen werden unter drei Schlüsseln abgedeckt:  

* Allgemein

  Definiert, an wen Sie verkaufen und von wem Sie kaufen und was Sie verkaufen und was Sie kaufen. Sie können Gruppen kombinieren, um Elemente wie die GuV-Konten festzulegen, um zu buchen, oder Sie verwenden Gruppen Berichte zum Filtern.  
* Ausgewählt

  Auf diese Weise erhalten Sie die Möglichkeit, beispielsweise Verkaufsbelege zu verwenden, statt die Posten direkt in der Finanzbuchhaltung zu buchen. Wenn Debitorenposten erstellt werden, wird durch die Buchungsgruppen gewährleistet, dass die entsprechenden Posten in der Finanzbuchhaltung gebucht werden.  
* Steuer

  Definieren Sie die Steuerprozentsätze und -Berechnungsarten, die anwenden, an wen Sie verkaufen und kaufen und was Sie verkaufen und was Sie kaufen.

In den folgenden Abschnitten werden die Buchungsgruppen nach Schlüsseln beschrieben.  

## <a name="general-posting-groups" />Allgemeine Buchungsgruppen

In der folgenden Tabelle werden die allgemeinen Buchungsgruppen beschrieben.

| Typ | Beschreibung |
| --- | --- |
| Allgemeine Geschäftsbuchungsgruppen |Weisen Sie diese Gruppen den Debitoren und Kreditoren zu, um anzugeben, von wem Sie kaufen und an wen Sie verkaufen. Richten Sie diese Buchungsgruppen auf der Seite **Geschäftsbuchungsgruppen** ein. Wenn Sie dies tun, überlegen Sie, in wie viele Gruppen die Verkäufe und Einkäufe aufgeschlüsselt werden müssen. Beispielsweise Gruppendebitoren und Kreditoren nach bestimmten Feld oder nach Art des Geschäfts. |
| Allgemeine Produktbuchungsgruppen |Weisen Sie diese Gruppe Artikeln und Ressourcen zu, um festzulegen, was Sie verkaufen und was Sie kaufen. Richten Sie diese Buchungsgruppen auf der Seite **Produktbuchungsgruppen** ein. Wenn Sie dies tun, berücksichtigen Sie die Gruppen, in die Sie Verkäufe nach Produkt (Artikel und Ressourcen) und Verkäufe nach Artikeln aufschlüsseln müssen. Beispielsweise  teilen Sie diese Gruppen nach Rohmaterial, Einzelhandel, Ressourcen, Kapazität, usw. auf. |
| Buchungsmatrix Einrichtung |Kombinieren von Geschäfts- und Produktbuchungsgruppen, und aktivieren Sie die Konten, um zu buchen. Jeder Kombination aus Geschäfts- und Produktbuchungsgruppen können Sie einen anderen Satz von Sachkonten zuweisen. Sie können z. B. den Verkauf desselben Artikels auf verschiedene Hauptbuchkonten buchen, da die Kunden verschiedenen Geschäftsbuchungsgruppen zugeordnet sind. Richten Sie diese Konfigurationen auf der Seite **Buchungsmatrix Einrichtung** ein. |

## <a name="specific-posting-groups" />Spezielle Buchungsgruppen

In der folgenden Tabelle werden die Buchungsgruppen beschrieben, die sich auf bestimmte Datentypen beziehen.

|Typ | Beschreibung |
| --- | --- |
| Debitorenbuchungsgruppen |Definieren Sie die Konten, die verwendet werden, wenn Sie buchen. Wenn Sie den Bestand mit Forderungen verwenden, werden die Konten, auf die die Kundenauftragszeilen gebucht werden, durch die allgemeine Geschäftsbuchungsgruppe, die Ihrem Kunden zugeordnet ist, und die allgemeine Produktbuchungsgruppe, die dem Bestandsartikel zugeordnet ist, bestimmt. Weitere Informationen finden Sie unter *Allgemeine Geschäftsbuchungsgruppen* und *Allgemeine Produktbuchungsgruppen* im Abschnitt [Allgemeine Buchungsgruppen](#general-posting-groups). Richten Sie diese Buchungsgruppen auf der Seite **Kundenbuchungsgruppen** ein. |
| Kreditorenbuchungsgruppen |Definieren Sie, wo Transaktionen für Kreditorensammelkonten, Servicegebührenkonten und Skontokonten gebucht werden. Dieses ist gleich wie bei den Debitorenbuchungsgruppen. Richten Sie diese Buchungsgruppen auf der Seite **Kreditorenbuchungsgruppen** ein. |
| Lagerbuchungsgruppen |Definieren Sie Lagerbuchungsgruppen, die Sie dann mit den entsprechenden Sachkonten auf der Seite **Lagerbuchungseinrichtung** verknüpfen. Wenn Sie dann Posten erzeugen, die einen Artikel betreffen, wird das System auf das Sachkonto buchen, das für die Kombination aus Lagerbuchungsgruppe und Lagerort eingerichtet ist, die mit dem Artikel verknüpft ist. Lagerbuchungsgruppen stellen darüber hinaus eine gute Möglichkeit dar, das Lager zu organisieren, sodass Sie beim Generieren von Berichten Artikel anhand ihrer Lagergruppen voneinander trennen können. Richten Sie diese Buchungsgruppen auf der Seite **Bestandsbuchungsgruppen** ein. |
| Bankkontobuchungsgruppen |Definieren Sie die Sachkonten, in die Bankkontoposten gebucht werden. Beispielsweise kann dies die Vorgänge für die Nachverfolgung von Transaktions- und Ausgleichsbankonten vereinfachen, Richten Sie diese Buchungsgruppen auf der Seite **Bankkonto-Buchungsgruppen** ein. Wir empfehlen, das Feld **Direktbuchung** dieser Sachkonten auf *Nein* festzulegen. |
| Anlagenbuchungsgruppen |Sie legen die Konten für die Anschaffungskosten, die kumulierten Abschreibungsbeträge, die Anschaffungskosten bei Verkauf, die kumulierte Abschreibung bei Verkauf, den Gewinn bei Verkauf, den Wartungsaufwand und den Abschreibungsaufwand fest. Richten Sie diese Buchungsgruppen auf der Seite **Anlagenbuchungsgruppen** ein. |

### <a name="allowing-substitute-customer-or-vendor-posting-groups-on-documents" />Zulassen von Ersatzbuchungsgruppen für Debitoren oder Kreditoren in Belegen

[!INCLUDE [preview](includes/preview.md)]

Sie können Benutzern ermöglichen, andere Debitoren- und Kreditorenbuchungsgruppen als die Standardgruppen auszuwählen, wenn sie mit Verkaufs- oder Einkaufsdokumenten und Erfassungen arbeiten.

Um Änderungen an Kundenbuchungsgruppen zuzulassen, wählen Sie **Mehrere Buchungsgruppen zulassen** auf den **Einrichtung von Verkäufen und Forderungen**- und **Service Einrichtung**-Seiten und die **Kreditoren & Einkauf Einr.**-Seite für Kreditorenbuchungsgruppenänderungen.

Auf den Seiten **Debitorenbuchungsgruppen** oder **Kreditorenbuchungsgruppen** können Sie die Buchungsgruppen angeben, die als Stellvertreter zugelassen werden sollen, indem Sie **Ersatzartikel** auswählen. Ersatzbuchungsgruppen können die standardmäßigen Debitoren- oder Kreditorenbuchungsgruppen ersetzen, die für einen Debitor oder Kreditor angegeben sind.

Nachdem Sie dies eingerichtet haben, können Sie aus den zulässigen Ersatzbuchungsgruppen auswählen und die Debitoren- oder Kreditorenbuchungsgruppe ändern, wenn Sie Verkaufs- oder Einkaufsbelege und Journale buchen. Die Debitoren- oder Kreditoren-Ersatzbuchungsgruppen werden in gebuchte Belege und Journale kopiert, und Sachposten für Verbindlichkeiten oder Forderungen werden auf die Sachkonten gebucht, die für die Ersatzpersonen angegeben sind.

Wenn Sie beispielsweise eine Rechnung und eine Zahlung anwenden, die mit unterschiedlichen Debitoren- oder Kreditorenbuchungsgruppen (unterschiedliche Sachkonten) gebucht werden, überträgt [!INCLUDE[prod_short](includes/prod_short.md)] die Beträge zwischen den Sachkonten, um sie auszugleichen.

## <a name="tax-posting-groups" />Steuerbuchungsgruppen

In der folgenden Tabelle werden die steuerbezogenen Buchungsgruppen beschrieben.

| Typ | Beschreibung |
| --- | --- |
| Geschäftssteuerbuchungsgruppen |Bestimmen, wie Verkaufssteuer für Debitoren und Kreditoren berechnet und gebucht werden. Richten Sie diese Buchungsgruppen auf der Seite **Geschäftssteuerbuchungsgruppen** ein. Wenn Sie dies tun, überlegen Sie, wieviele Gruppen Sie benötigen. Dies ist von verschiedenen Faktoren wie der hiesigen Gesetzgebung ab und ob Sie sowohl im Inland als auch im Ausland Handel treiben. |
| Steuerproduktbuchungsgruppen |Geben Sie die Steuerberechnungen an, die für die Arten von  Artikeln oder Ressourcen erforderlich ist, die Sie kaufen oder verkaufen. |
| Steuerbuchung einrichten |Zeigt Kombinationen aus MwSt.-Geschäftsbuchungsgruppen und MwSt.-Produktbuchungsgruppen an. Wenn Sie eine Buch.-Blattzeile, eine Einkaufszeile bzw. Verkaufszeile ausfüllen, schauen wir die Kombination an, um die zu verwendenden Konten zu identifizieren. |

Wenn Ihr Land Mehrwertsteuer (MwSt.) erhebt, finden Sie Informationen unter [Berechnungen und Buchungsmethoden für die Mehrwertsteuer festlegen](finance-setup-vat.md).  

## <a name="example-of-linking-posting-groups" />Beispiel für die Verknüpfung von Buchungsgruppen

Hier ist ein Szenario.  

Diese Buchungsgruppen werden auf der Debitorenkarte aktiviert:  

* Allgemeine Geschäftsbuchungsgruppe
* Debitorenbuchungsgruppe  

Diese Buchungsgruppen werden auf der Artikelkarte aktiviert:  

* Allgemeine Produktbuchungsgruppen  
* Lagerbuchungsgruppe  

Wenn ein Verkaufsbeleg erstellt wird, werden die Informationen auf der Debitorenkarte in den Verkaufskopf übernommen, und die Informationen auf der Artikelkarte werden in die Verkaufszeilen eingefügt.  

* Die Buchung der Einnahmen (GuV-Konten) wird durch die Kombination der allgemeinen Geschäftsbuchungsgruppe und der allgemeinen Produktbuchungsgruppe bestimmt.  
* Die Debitorenbuchung (Bilanz) wird durch die Debitorenbuchungsgruppe bestimmt.  
* Die Lagerbuchung (Bilanz) wird durch die Lagerbuchungsgruppe bestimmt.  
* Die Buchung der Kosten für verkaufte Waren (GuV) wird durch die Kombination der allgemeinen Geschäftsbuchungsgruppe und der allgemeinen Produktbuchungsgruppe bestimmt.  

Ihre Einrichtung legt fest, wann die Buchung erfolgt. Beispielsweise wird die zeitliche Steuerung tangiert, wenn Sie "Periodische Aktivitäten" durchführen, wie Buchungslagerkosten oder Anpassung von Kostenfaktorposten.

## <a name="copying-posting-setup-lines" />Kopieren von Buchungsmatrix-Einrichtungszeilen

Je mehr Produkt- und Geschäftsbuchungsgruppen vorhanden sind, um so mehr Zeilen werden auf der Seite **Buchungsmatrix Einrichtung** angezeigt. Für die Einrichtung der Buchungsmatrix des Unternehmens kann daher unter Umständen eine umfangreiche Dateneingabe erforderlich sein. Während unter Umständen viele verschiedene Kombinationen von Geschäfts- und Produktbuchungsgruppen vorhanden sind, buchen möglicherweise unterschiedliche Kombinationen weiterhin auf dieselben Sachkonten. Um den Umfang der erforderlichen manuellen Dateneingabe einzuschränken, kopieren Sie die Sachkonten aus einer vorhandenen Zeile auf der Seite **Buchungsmatrix Einrichtung.**

## <a name="set-up-posting-groups-on-the-go" />Buchungsgruppen von unterwegs aus festlegen

Um den Benutzern einen schnelleren Einstieg zu ermöglichen, kann [!INCLUDE[prod_short](includes/prod_short.md)] Benachrichtigungen über fehlende Sachkonten in verschiedenen Buchungsgruppen-Einrichtungen anzeigen. Um diese Benachrichtigungen zu erhalten, stellen Sie sicher, dass die Benachrichtigung **Sachkonto fehlt in Buchungsgruppe oder Einrichtung** auf der Seite **Meine Benachrichtigungen** ausgewählt ist, auf die Sie über das Feld **Ändern, wenn ich Benachrichtigungen erhalte** auf der Seite **Meine Einstellungen** zugreifen können.  

Auf diese Weise erhalten Sie eine Benachrichtigung, wenn Sie an einem Beleg arbeiten, der eine Buchungsgruppe oder eine Einrichtung verwendet, in der ein erforderliches Hauptbuchkonto fehlt. Wählen Sie den Link in der Benachrichtigung, um eine Seite zu öffnen, auf der Sie die entsprechenden Änderungen vornehmen können, sofern Sie die Berechtigung dazu haben.  

> [!NOTE]
> Um Sie direkt zu der Buchungsgruppe oder Einrichtung zu führen, in der ein Hauptbuchkonto fehlt, erstellt [!INCLUDE[prod_short](includes/prod_short.md)] eine Platzhalter-Buchungsgruppe oder Einrichtung. Buchungsgruppen und -einstellungen sind eine Möglichkeit für den Buchhalter zu steuern, wie Buchungen in das Allgemeine Hauptbuch gebucht werden, so dass eine solche Just-in-Time-Erstellung von Buchungsgruppen und -einstellungen in Ihrem Unternehmen möglicherweise nicht zugelassen ist.  
>
> Deaktivieren Sie in diesem Fall die Meldung *Sachkonto fehlt in Buchungsgruppe oder Einrichtung* und nehmen Sie dann gemeinsam mit Ihrem Buchhalter die entsprechenden Änderungen an der Buchungsgruppe, der Einrichtung oder Ihrem Beleg vor. Dies ist ein wichtiger Schritt, denn sobald Belege gebucht sind, können falsch verwendete Buchungsgruppen oder Einrichtungen nicht mehr gelöscht werden, da für sie Hauptbucheinträge erstellt wurden.

Ab dem 1. Veröffentlichungszyklus 2022 können Sie das **Gesperrt**-Feld auf der Seite **Buchungsmatrix Einrichtung** verwenden, um zu verhindern, dass Benutzer versehentlich ein Setup verwenden, das für neue Buchungen nicht mehr relevant ist.  

## <a name="troubleshooting-posting-group-errors" />Problembehandlung von Fehlern bei Buchungsgruppen

Buchungsgruppen sind eines der fortgeschritteneren Konzepte, die Sie in [!INCLUDE[prod_short](includes/prod_short.md)] festlegen können. Wenn sie nicht korrekt eingerichtet sind, können beim Buchen von Belegen oder Buchungsblattzeilen Fehler auftreten. Diese Fehler werden in der Regel durch einen Fehler bei der Zuordnung von Hauptbuch-Konten oder bei der Kombination von Buchungsgruppen verursacht.

Wenn etwas nicht stimmt, zeigt [!INCLUDE[prod_short](includes/prod_short.md)] die Seite **Fehlermeldungen** an. Die Seite **Fehlermeldungen** kann es Ihnen erleichtern, das Problem zu identifizieren und zu beheben. Die Seite bietet eine Beschreibung des Fehlers, die auf die Einrichtung der Buchungsgruppe hinweist, die beachtet werden muss. Die Nachricht könnte zum Beispiel lauten: „Für das Konto Umsatzvorauszahlung fehlt eine Allgemeine Buchungsmatrixeinrichtung.“ Es gibt auch einen Link, über den Sie die Seite öffnen können, von der das Problem ausgeht, sodass Sie es schnell beheben können.  

> [!NOTE]
> Die oben beschriebene Fehlerbehandlung ist nicht verfügbar für Artikel-, Ressourcen-, Mitarbeiter- und Anlage-Fibu Buch.-Blätter oder für Sachkonten, die in lokalen Versionen von Buchungsgruppen hinzugefügt wurden.

## <a name="see-related-microsoft-trainingtrainingmodulesposting-groups-dynamics-365-business-central" />Siehe verwandte [Microsoft Schulungen](/training/modules/posting-groups-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Finance einrichten](finance-setup-finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
