---
title: Erstellen von eingehenden Belegen
description: 'Verwenden Sie verschiedene Funktionen auf der Seite Eingehende Belege, um Spesenbelege zu prüfen, OCR-Aufgaben zu verwalten, eingehende Beleg-Dateien zu konvertieren und externe Dateien anzuhängen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="create-incoming-document-records" />Erstellen von eingehenden Belegen

Auf der Seite **Eingehende Belege** können Sie verschiedene Funktionen zum Überprüfen von Ausgabenbelegen, Verwalten von OCR-Aufgaben und Konvertieren eingehender Belege, manuell oder automatisch, in den entsprechenden Belegen oder Buch.-Blattzeilen verwenden. Die externen Dateien können jeder Prozessphase zugeordnet werden, auch gebuchten Belegen und den resultierenden Kreditoren-, Debitoren- und Sachposten.

Um ein externes Dokument in [!INCLUDE[prod_short](includes/prod_short.md)] zu erfassen, erstellen oder vervollständigen Sie zunächst einen Datensatz für ein eingehendes Dokument. Sie können diese Aufgaben manuell erledigen oder ein Foto des externen Dokuments machen, um den Datensatz für eingehende Dokumente mit angehängter Bilddatei zu erstellen.

Bevor Sie die Funktion **Eingehende Belege** verwenden können, müssen Sie die erforderlichen Einstellungen vornehmen. Weitere Informationen finden Sie unter [Eingehende Belege einrichten](across-how-setup-income-documents.md).

## <a name="approve-or-reject-an-incoming-document" />So können Sie einen eingehenden Beleg genehmigen oder ablehnen

Wenn Sie die Funktion **Eingehende Belege** so festgelegt haben, dass für das Erstellen von Dokumenten eine Genehmigung erforderlich ist, müssen Benutzer mit den entsprechenden Rechten die Datensätze genehmigen, bevor sie verarbeitet werden. Weitere Informationen finden Sie unter [Einrichten von Genehmigern für eingehende Datensätze](across-how-setup-income-documents.md#to-set-up-approvers-of-incoming-document-records).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Eingehende Belege** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Zeile mit dem Beleg, den Sie genehmigen oder ablehnen möchten, und wählen Sie dann die Aktion **Genehmigen** oder **Ablehnen** aus.

Das Kontrollkästchen **Freigegeben** in der Zeile für den Eingangsbeleg ist aktiviert, wenn dieser genehmigt wurde. Der jeweilige Benutzer, beispielsweise der für das Erstellen von Einkaufsrechnungen zuständige, kann dann fortfahren, den Datensatz zu verarbeiten.

## <a name="create-an-incoming-document-record-by-taking-a-photo" />So erstellen Sie Eingangsbelegdatensätze indem Sie ein Foto machen

> [!NOTE]  
> Das folgende Verfahren gilt nur für die [!INCLUDE[prod_short](includes/prod_short.md)] Tablet- und Telefon-Clients.

1. Wählen Sie im Rollencenter die Kachel **Eingehende Belege von Kamera erstellen** und gehen Sie dann zu Schritt 4.
2. Wählen Sie alternativ die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Eingehende Belege** ein und wählen Sie dann den zugehörigen Link.
3. Wählen Sie auf der Seite **Eingehende Belege** die Option **Neu** und dann **Erstellen aus Kamera**. Die Kamera im Tablet oder dem Smartphone wird aktiviert.
4. Machen Sie ein Foto von einem Dokument, z.B. einem Kaufbeleg, das Sie als eingehendes Dokument verarbeiten möchten, und wählen Sie dann die Schaltfläche **Verwenden**.

    Es wird ein neuer Datensatz für eingehende Dokumente erstellt, an den das Bild angehängt wird.

## <a name="attach-an-image-to-an-incoming-document-record-by-taking-a-photo" />So hängen Sie ein Bild an ein Eingangsbelegdatensatz an, indem Sie ein Foto machen

> [!NOTE]  
> Das folgende Verfahren gilt nur für die [!INCLUDE[prod_short](includes/prod_short.md)] Tablet- und Telefon-Clients.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Eingehende Belege** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Karte eines vorhandenen eingehenden Belegsdatensatzes.
3. Wählen Sie auf der Seite mit dem Datensatz des Dokuments **Verarbeiten** und dann **Bild von Kamera anhängen**. Die Kamera im Tablet oder dem Smartphone wird aktiviert.
4. Machen Sie ein Foto von einem Dokument, z.B. einem Kaufbeleg, das Sie als eingehendes Dokument verarbeiten möchten, und wählen Sie dann die Schaltfläche **Verwenden**.

    Das Bild wurde dem Datensatz des eingehenden Beleges angehängt.

## <a name="create-an-incoming-document-record-manually" />Eingehende Belege manuell erstellen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Eingehende Belege** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Neu**, und dann die Aktion **Erstellen aus Datei**.  
3. Wählen Sie auf der Seite **Datei einfügen** eine Datei aus und wählen Sie dann **Offen** aus. Die Datei wird automatisch angehängt.
4. Wählen Sie alternativ die Aktion **Neu** aus.
5. Um eine Datei anzuhängen, wählen Sie **Verarbeiten** und dann die Aktion **Datei anhängen**.
6. Auf der Seite **Datei einfügen** wählen Sie die Datei, die den jeweiligen eingehenden Beleg darstellt, und wählen Sie die Schaltfläche **Öffnen**.
7. Füllen Sie auf der Seite **Eingehende Belege** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-microsoft-trainingtrainingmodulesincoming-documents-dynamics-365-business-central" />Siehe verwandte [Microsoft Schulungen](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Mit OCR PDF- und Bilddateien in elektronische Belege umwandeln](across-how-use-ocr-pdf-images-files.md)
[Eingehende Belege direkt aus Dokumenten und Einträgen erstellen](across-how-connect-disconnect-income-document-records.md)
[Gebuchte Belege ohne eingehende Belege suchen](across-how-find-posted-documents-without-income-document-records.md)
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
