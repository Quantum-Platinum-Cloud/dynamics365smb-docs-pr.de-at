---
title: Serviceverträge einrichten
description: 'Erfahren Sie, wie Sie Serviceverträge mit den erforderlichen Voraussetzungen festlegen, einschließlich Servicevertragsgruppen, Vertragsvorlagen und Debitorenvorlagen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'service, cost, service order'
ms.date: 06/23/2021
ms.author: edupont
---

# <a name="set-up-service-contracts" />Serviceverträge einrichten
Um mit Verträgen arbeiten zu können, müssen Sie Folgendes einrichten: 

* Die Tabelle **Servicevertragsgruppe** enthält eine Gruppe von Serviceverträgen, die miteinander in Verbindung stehen.
* Sie können **Servicevertragskontengruppen** verwenden, um Serviceverträge zu gruppieren. Diese Gruppen können dann für die Servicerechnungen von Serviceverträgen verwendet werden. Sie können diese Gruppen anschließend Ihren Serviceverträgen zuordnen.  
* Sie können **Vertragsvorlagen** als eine vordefinierte Grundlage für Serviceverträge verwenden, die die gängigsten Servicevertragsdetails enthält. Wenn Sie Servicevertragsangebote erstellen, können Sie diese unter Verwendung dieser Vorlagen erstellen. Wenn Sie ein neues Vertragsangebot erstellen, enthalten die Felder automatisch den Inhalt der Vorlagenfelder.
* **Debitorenvorlagen** , mit denen Sie Angebote für Kontakte oder potenzielle Debitoren erstellen können, die nicht als Debitoren in [!INCLUDE[prod_short](includes/prod_short.md)]registriert sind.  

## <a name="to-set-up-a-service-contract-group" />So richten Sie Servicevertragsgruppen ein
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Servicevertragsgruppen** ein, und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Aktivieren Sie das Feld **Rabatt nur auf Vertr.-Aufträge**, wenn Vertrags- oder Servicerabatte nur für Vertragsaufträge, wie z. B. Wartung, gültig sein sollen.  

## <a name="to-set-up-a-service-contract-account-group" />So richten Sie eine Servicevertragskontengruppe ein
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Serv. Vertragskontogruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Servicevertragskontengruppe.   
3. Füllen Sie die Felder **Code** und **Beschreibung** aus. Diese Felder beschreiben die Servicekontengruppe.  
4. Füllen Sie das Feld  **Nicht vorausbez. Vertragskonto** aus. Dieses Feld enthält die Sachkontennummer des Kontos, auf das nicht vorausbezahlte Beträge gebucht werden.  
5. Füllen Sie das Feld  **Nicht vorausbez. Vertragskonto** aus. Dieses Feld enthält die Sachkontennummer des Kontos, auf das nicht vorausbezahlte Beträge gebucht werden.  

## <a name="to-set-up-a-contract-template" />So richten Sie Vertragsvorlagen ein
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Servicevertragsvorlagen** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Servicevertragsvorlage.  
3. Geben Sie im Feld **Nr.** eine Nummer für die Vertagsvorlage ein.  
  
     Wenn Sie Nummernserien für Vertragsvorlagen auf der Seite **Service Einrichtung** definiert haben, wählen Sie die <kbd>EINGABETASTE</kbd>, damit die nächste verfügbare Vertragsvorlagennummer eingefügt wird. Füllen Sie die anderen Felder aus, falls diese benötigt werden.  
  
4. Füllen Sie im Inforegister **Rechnung** das Feld **Servicevertragskonto-Gruppencode** aus und geben Sie das **Fakturierungsintervall** usw. an. Füllen Sie die anderen Felder aus, falls diese benötigt werden.  
5. Wählen Sie die **Servicerabatte** Aktion aus, um Vertragsrabatte hinzuzufügen.  

## <a name="to-set-up-a-customer-template" />So richten Sie Debitorenvorlagen ein
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Kundenvorlagen** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Debitorenvorlagenkarte.  
3. Geben Sie auf dem Inforegister **Allgemein** der Debitorenvorlagenkarte im Feld **Code** einen Code und im Feld **Beschreibung** eine Beschreibung für die Debitorenvorlage ein. 
4. Die anderen Felder, z. B. **Länder-/Regionscode**, **Gebietscode** und **Sprachcode**, werden als Suchkriterien verwendet und können ausgefüllt werden.  
5. Die Felder  **Geschäftsbuchungsgruppe** und  **Debitorenbuchungsgruppe** müssen ausgefüllt werden.  

## <a name="see-also" />Siehe auch
[Einrichten der Serviceverwaltung](service-setup-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
