---
title: AEM Document Security for Microsoft Office - Versionshinweise
description: Lesen Sie die Versionshinweise, bevor Sie AEM Document Security 6.2 Extension for Microsoft Office installieren.
uuid: f6ab73d4-ac4e-4fff-9bb8-917b75401653
content-type: reference
topic-tags: installing
discoiquuid: c9342c28-8289-4831-a613-4bc03431f557
exl-id: 582f10bb-60d2-46ed-b81d-5818a040edc6
source-git-commit: 28137f26afc024d411857d44887bf69fe1ee2b81
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 100%

---

# AEM Document Security for Microsoft Office - Versionshinweise{#aem-document-security-for-microsoft-office-release-notes}

## Neue Funktionen in AEM Document Security for Microsoft Office {#whats-new-in-aem-document-security-for-microsoft-office}

* **Unterstützung für Office 2019**: Document Security Extension für Microsoft Office unterstützt jetzt Microsoft Office 2019. Es wird überdies erwartet, dass es mit Microsoft Office 2019 Desktop-Programmen als Teil von Office. 365 funktioniert.

>[!NOTE]
>
>Das Dokument verwendet austauschbar Adobe Experience Manager Document Security for Microsoft Office, Adobe Experience Manager Document Security Extension for Microsoft Office und Document Security Extension for Microsoft Office.

## Installieren und Konfigurieren von AEM Document Security Extension for Microsoft Office {#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

Diese Version von Document Security Extension for Microsoft Office ist mit Adobe LiveCycle Rights Management ES2 und höher und Document Security-Add-on für AEM Forms kompatibel.

Prüfen Sie die Informationen in diesem Dokument, bevor Sie AEM Document Security Extension for Microsoft Office installieren. Detaillierte Installationsanweisungen finden Sie unter [Installieren und Konfigurieren von AEM Document Security Extension for Microsoft Office](installing-configuring-aemdsext.md).

## Behobene Probleme {#fixed-issues}

* Zeichenfolgen werden vertikal angezeigt und dem Inhalt werden falsche Zeilenumbrüche hinzugefügt. (Referenznummer CQ-4201054)

## Bekannte Probleme {#known-issues}

### Plug-ins von Drittanbietern werden nicht unterstützt {#third-party-plug-ins-not-supported}

AEM Document Security Extension for Microsoft Office funktioniert nicht mit Plug-ins von Drittanbietern. Deinstallieren Sie alle Plug-ins von Drittanbietern für Microsoft Office, bevor Sie Document Security Extension for Microsoft Office installieren.

### Deaktivieren Sie Menüoptionen in Microsoft Word, Excel und PowerPoint {#disabled-menu-options-in-microsoft-word-excel-and-powerpoint}

AEM Document Security Extension for Microsoft Office verwendet integrierte Schutzfunktionen, um Dokumente, Arbeitsmappen und Präsentationen zu schützen. Dadurch werden einige Menüoptionen in Excel, Word und PowerPoint deaktiviert.

### Einschränkungen für Microsoft Excel 2013, 2016 und 2019 {#restrictions-for-microsoft-office}

In Microsoft Office sind während einer geschützten Sitzung die folgenden Optionen nicht verfügbar:

* Microsoft Office 2016 oder Microsoft Office 2019

   * Datei > Speichern unter
   * Datei > Verlauf
   * Datei > Freigeben
   * Datei > Exportieren
   * Datei > Veröffentlichen
   * Datei > Konto
   * Datei > Informationen > Dokument/Arbeitsmappe/Präsentation schützen > Mit Kennwort verschlüsseln
   * Datei > Informationen > Dokument schützen > Digitale Signatur hinzufügen
   * Datei > Informationen > Dokument schützen > Als abgeschlossen kennzeichnen
   * Freigabeoption oben rechts

* Microsoft Office 2013

   * Datei > Speichern unter
   * Datei > Freigeben
   * Datei > Exportieren
   * Datei > Konto
   * Datei > Informationen > Dokument/Arbeitsmappe/Präsentation schützen > Mit Kennwort verschlüsseln
   * Datei > Informationen > Dokument schützen > Digitale Signatur hinzufügen
   * Datei > Informationen > Dokument schützen > Als abgeschlossen kennzeichnen

### Öffnen eines geschützten Dokuments vom SharePoint-Server aus {#opening-a-protected-document-from-sharepoint-server}

Öffnen des geschützten Dokuments: Wenn Sie versuchen, ein geschütztes Dokument von SharePoint Server aus in Document Security Extension for Microsoft Office zu öffnen, ohne zuvor das mit dem Dateityp verknüpfte Microsoft Office-Programm zu öffnen, z. B. Microsoft Word, Microsoft Excel oder Microsoft PowerPoint, wird das Dokument möglicherweise nicht geöffnet. Es wird eine Fehlermeldung angezeigt, die darauf hinweist, dass Sie das entsprechende Plug-in installieren müssen. Es wird daher empfohlen, das zugehörige Microsoft Office-Programm zu öffnen, bevor Sie ein geschütztes Dokument in Document Security Extension for Microsoft Office über SharePoint Server öffnen.

(Optional) Es wird empfohlen, den Cache-Ordner zu leeren, bevor Sie ein geschütztes Dokument in Document Security Extension for Microsoft Office von SharePoint Server aus öffnen.

Wenn Sie ein geschütztes Dokument über SharePoint Server öffnen, werden alle Berechtigungen für das Dokument deaktiviert, unabhängig von der angewendeten Richtlinie.

### Anwenden von Richtlinien mit dynamischem Wasserzeichen auf Microsoft Excel 2013, Microsoft Excel 2016 und Microsoft Excel 2019-Dateien, wenn kein Drucker installiert ist {#apply-a-policy-with-a-dynamic-watermark-to-microsoft-excel-microsoft-excel-and-microsoft-excel-file-with-no-printer-installed}

Wenn Sie auf einem Computer, bei dem kein Drucker installiert ist, eine Richtlinie mit dynamischem Wasserzeichen auf eine Excel 2013-, Microsoft Excel 2016- und Microsoft Excel 2019-Datei anwenden und diese Datei speichern, wird folgende Fehlermeldung angezeigt: „Interner Fehler beim Anwenden des dynamischen Wasserzeichens.“ Dieser Fehler wird auch angezeigt, wenn Sie die geschützte Datei erneut öffnen. Das Wasserzeichen wird nicht angewendet und ist in „Ansicht“ > „Seitenlayout“ nicht sichtbar.

### Deaktivieren Sie Windows Data Execution Prevention für unterstützte Office-Programme {#disable-windows-data-execution-prevention-for-supported-office-applications}

Es wird empfohlen, dass Sie bei der Verwendung von Microsoft Office-Programmen, die von Document Security Extension unterstützt werden, die Einstellungen der Windows Data Execution Prevention (DEP) deaktivieren.

### Freigegebene Microsoft Office-Dateien können nicht mit Document Security Extension geschützt werden {#shared-microsoft-office-files-cannot-be-protected-using-document-security-extension}

Wenn Sie gemeinsam genutzte Microsoft Office-Dateien mit Document Security Extension schützen, tritt ein Fehler auf und die Dateifreigabe wird nicht gesichert.

### Starten von Office-Programmen auf einem Computer, auf dem Document Security Extension for Microsoft Office und McAfee VirusScan installiert sind {#starting-office-applications-on-a-machine-containing-document-security-extension-for-microsoft-office-and-mcafee-virusscan}

Wenn Sie außerdem einen reibungslosen Start von Office-Programmen auf Computern mit installierter Document Security und aktiviertem McAfee VirusScan mit Überprüfung bei Zugriff sicherstellen möchten, deaktivieren Sie die Option „Pufferüberlaufschutz“ in der McAfee VirusScan-Konsole.

### Installieren von Document Security Extension for Microsoft Office auf einem Computer mit einer nicht unterstützten Microsoft Office-Sprache {#installing-document-security-extension-for-microsoft-office-on-a-machine-with-an-unsupported-microsoft-office-language}

Bevor Sie Document Security Extension for Microsoft Office auf einem Computer installieren, auf dem eine Microsoft Office-Anwendung mit einer nicht unterstützten Sprache installiert ist, öffnen Sie das Office-Programm mindestens einmal.

### Die Schaltfläche „Offline synchronisieren“ ist selbst dann aktiviert, wenn ein Benutzer keine Offline-Berechtigungen hat {#synchronize-offline-button-is-enabled-even-when-a-user-does-not-have-offline-permissions}

Die Schaltfläche „Offline synchronisieren“ ist verfügbar, obwohl der Benutzer keine Offline-Berechtigung für dieses Dokument hat. Das Klicken auf die Schaltfläche bleibt jedoch wirkungslos.

### Keine Unterstützung für Testversionen von Microsoft Office {#no-support-for-trial-versions-of-microsoft-office}

AEM Document Security Extension for Microsoft Office unterstützt keine Testversionen von Microsoft Office. Vor der Installation der Erweiterung müssen Sie sicherstellen, dass eine lizenzierte Kopie von Microsoft Office auf Ihrem Computer installiert und aktiviert ist.

### Geschützte Microsoft Office-Dateien können nicht geöffnet werden {#unable-to-open-a-protected-microsoft-office-files}

Wenn die geschützte Ansicht von Microsoft Office aktiviert ist, kann Rights Management Extension keine geschützten Microsoft Excel-Dateien (XLS, XLSX) und keine geschützten Microsoft PowerPoint (PPT)-Dateien von einem Remote-Standort aus öffnen.

### Zellen eines Microsoft Excel-Dokuments, die ein Bild oder eine Hintergrundfarbe enthalten, erscheinen vor dem Wasserzeichen {#cells-of-microsoft-excel-document-containing-an-image-or-background-color-appear-on-top-of-watermark}

Wenn eine Zelle eines Microsoft Excel-Dokuments ein Bild enthält oder mit einer Hintergrundfarbe befüllt ist und eine dynamische Wasserzeichenrichtlinie auf das Dokument angewendet wird, wird das Bild bzw. die Hintergrundfarbe vor dem Wasserzeichen angezeigt, sodass das Wasserzeichen davon überdeckt wird.

### Bedienungsproblem mit mehreren Zertifikaten {#usability-issue-with-multiple-certificates}

Wenn mehrere Zertifikate auf einem Client-Computer vorhanden sind und der Benutzer das Dialogfeld für die Zertifikatauswahl abbricht, wird das Dialogfeld noch einmal angezeigt und der Benutzer muss es zweimal abbrechen.

### Microsoft PowerPoint ermöglicht das Bearbeiten von geschützten Dokumenten {#microsoft-powerpoint-allows-editing-protected-documents}

Beim Versuch, ein geschütztes Dokument zu bearbeiten, zeigt Microsoft PowerPoint die Meldung „Sie dürfen dieses Dokument nicht ändern. Sie können Ihre Änderungen nicht speichern.“ Nach dem Schließen der Meldung können Benutzende weiterhin Text hinzufügen oder das Dokument bearbeiten. Die Änderungen an den geschützten Dokumenten werden jedoch nicht gespeichert.

Das oben genannte Verhalten ist in PowerPoint 2013, PowerPoint 2016 und PowerPoint 2019 erwartungsgemäß.
