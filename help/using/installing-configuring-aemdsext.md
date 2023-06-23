---
title: Installieren und Konfigurieren von AEM Document Security Extension for Microsoft Office
description: Dieses Dokument erläutert die Installation und Konfiguration von Adobe Experience Manager Document Security Extension 6.2 for Microsoft Office.
uuid: 9d7eb6bb-4780-4d82-8657-7c6c6d523af0
content-type: reference
topic-tags: installing
discoiquuid: f1cdf344-efe4-4cb5-9fc3-47ee4ba5faf4
exl-id: 88759737-d57f-4354-951e-ad9f62d0a872
source-git-commit: 28137f26afc024d411857d44887bf69fe1ee2b81
workflow-type: tm+mt
source-wordcount: '2764'
ht-degree: 65%

---

# Installieren und Konfigurieren von AEM Document Security Extension for Microsoft Office{#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

Dieses Dokument erläutert die Installation und Konfiguration von Adobe Experience Manager Document Security Extension for Microsoft Office.

Dieses Dokument enthält Informationen zu den folgenden Aufgaben:

* Installieren von Document Security Extension for Microsoft Office
* Vorkonfigurieren des Installationsprogramms, um auf LiveCycle Rights Management ES2 und höher und Document Security-Add-on für AEM 6.0 Forms oder höher zu verweisen.
* Konfigurieren der automatischen Anwendung der Standardrichtlinie

## Vor der Installation {#before-you-install}

Bevor Sie Document Security Extension for Microsoft Office installieren, stellen Sie Folgendes sicher:

* Sie haben die [Versionshinweise](document-security-extension-release-notes.md).
* Microsoft Office ist aktiviert. Aktivierungsdialogfeld wird nicht angezeigt beim Öffnen von Microsoft Office-Programmen.
* Neueste Service Packs für Microsoft Windows und Microsoft Office sind installiert.
* Wenn Sie Document Security for Microsoft Office für eine nicht unterstützte Sprache installieren, müssen Sie das Office-Programm mindestens einmal öffnen.

>[!NOTE]
>
>Installieren Sie die Software nicht in einem Ordner, dessen Name Doppelbyte-Zeichen enthält. Wenn Sie dies tun, wird das Menü AEM Document Security nicht in Microsoft Office angezeigt.

>[!NOTE]
>
>Die Installation einer 32-Bit-Version der Document Security-Erweiterung auf einem 64-Bit-Betriebssystem wird unterstützt, die umgekehrte Methode wird jedoch nicht unterstützt. Sie können die 64-Bit-Version der Document Security-Erweiterung für Microsoft Office nicht auf einem 32-Bit-Betriebssystem installieren.

### Deaktivieren von McAfee VirusScan {#disable-mcafee-virusscan}

Wenn Sie außerdem einen reibungslosen Start von Office-Programmen auf Computern mit installierter Document Security Extension und aktiviertem McAfee VirusScan mit Überprüfung bei Zugriff sicherstellen möchten, deaktivieren Sie die Option „Pufferüberlaufschutz“ in der McAfee VirusScan-Konsole.

### Deinstallieren von Plug-ins von Drittanbietern {#uninstall-third-party-plug-ins}

AEM Document Security Extension for Microsoft Office unterstützt keine Plug-ins von Drittanbietern für Microsoft Office-Programme. Da diese Erweiterung mit Plug-ins von Drittanbietern im Konflikt steht, deinstallieren Sie alle Plug-ins von Drittanbietern für Microsoft Office, bevor Sie Document Security for Microsoft Office installieren. Adobe unterstützt Document Security for Microsoft Office nicht, wenn Plug-ins von Drittanbietern installiert sind.

## Systemanforderungen {#system-requirements}

### Document Security Extension-Client {#document-security-extension-client}

Stellen Sie sicher, dass die folgenden Mindestkonfigurationen für die Installation der Document Security Extension verwendet werden:

* 32-Bit- oder 64-Bit-Versionen von Microsoft Windows 7 oder Windows 10 auf Englisch, Französisch, Deutsch, Japanisch, Italienisch, Spanisch, Portugiesisch (Brasilien), Koreanisch, Chinesisch (vereinfacht) oder Chinesisch (traditionell).
   **Hinweis:** *Es wird erwartet, dass Document Security Extension for Microsoft Office auf Microsoft Surface-Geräten funktioniert.*

* 32-Bit- oder 64-Bit-Versionen Microsoft Office 2013, 2016, 2019 und Microsoft Office Desktop-Programmen, die als Teil von Office 365 auf Englisch, Französisch, Deutsch, Japanisch, Italienisch, Spanisch, Portugiesisch (Brasilien), Koreanisch oder Chinesisch (vereinfacht und traditionell) installiert sind.

   **Hinweis**: *AEM Document Security Extension for Microsoft Office unterstützt keine Plug-ins von Drittanbietern für Microsoft Office-Programme. Da Konflikte zwischen Plug-ins von Drittanbietern und dieser Erweiterung auftreten können, müssen Sie vor der Installation von Document Security Extension for Microsoft Office alle Plug-ins für Microsoft Office-Programme deinstallieren, die nicht von Adobe stammen. Adobe unterstützt Document Security Extension for Microsoft Office nicht, wenn Plug-ins von Drittanbietern installiert sind.*

* Prozessor mit 1,3 GHz oder höher
* 2 GB RAM
* 100 MB verfügbarer Festplattenspeicher

### Document Security {#document-security}

Um Document Security Extension zu verwenden, stellen Sie sicher, dass Sie eine Verbindung zu Adobe LiveCycle Rights Management ES2 und höher oder Document Security-Add-on für AEM 6.0 Forms oder höher herstellen können.

## Installieren von Document Security Extension for Microsoft Office {#installing-document-security-extension-for-microsoft-office}

Sie können das Installationsprogramm von der [Download-Seite](download-installer.md) herunterladen. Sie können die ausführbare Datei des Installationsprogramms nicht direkt anpassen, sie kann jedoch interaktiv oder im Hintergrund installiert werden. Melden Sie sich zur Installation der Software bei Windows als Administrator an.

Separate Installationsprogramme sind für 32-Bit- und 64-Bit-Versionen von Microsoft Office verfügbar. Laden Sie für die 32-Bit-Version von Microsoft Office DocumentSecurityExtensionforMicrosoftOffice.exe herunter. Für die 64-Bit-Version von Microsoft Office laden Sie DocumentSecurityExtensionforMicrosoftOffice64.exe herunter.

>[!NOTE]
>
>In diesem Dokument wird die 32-Bit-Installationsdatei (DocumentSecurityExtensionforMicrosoftOffice.exe) verwendet, um verschiedene Befehle und Optionen zu erklären. Wenn Sie die 64-Bit-Version von Microsoft Office verwenden, verwenden Sie die 64-Bit Installationsdatei (DocumentSecurityExtensionforMicrosoftOffice64.exe), um Vorgänge auszuführen, die in diesem Dokument aufgeführt sind.

### Installation im Hintergrund {#install-in-silent-mode}

Verwenden Sie ein Dienstprogramm zum Extrahieren von Dateien, wie z. B. WinZip, um die Datei `DocumentSecurityExtensionforMicrosoftOffice.exe` aus der Installationsdatei zu extrahieren. Öffnen Sie die Eingabeaufforderung, navigieren Sie zum Ordner, der die Setup-Datei enthält, und geben Sie den folgenden Text ein:

`DocumentSecurityExtensionforMicrosoftOffice.exe -s -a -s -v" /qn"`

Das Installationsprogramm steht auch als MSI-Datei zur Verfügung, die zur Anpassung verwendet werden kann.

### Installieren einer MSI-Datei im Hintergrund {#install-an-msi-file-in-silent-mode}

1. Verwenden Sie ein Dienstprogramm zum Extrahieren von Dateien, wie z. B. WinZip, um die Datei `DocumentSecurityExtensionforMicrosoftOffice.msi` aus der ZIP-Datei zu extrahieren.

1. Öffnen Sie die Eingabeaufforderung, navigieren Sie zum Ordner, der die MSI-Datei enthält, und geben Sie den folgenden Text ein:

   `msiexec /I DocumentSecurityExtensionforMicrosoftOffice.msi /qn`

## Vorkonfigurieren des Installationsprogramms für die Verbindung mit Document Security {#preconfiguring-the-installer-to-connect-to-document-security}

Sie können das Installationsprogramm für Document Security Extension for Microsoft Office so konfigurieren, dass es auf einen LiveCycle- oder AEM-Server verweist, damit Benutzer, die Document Security Extension for Microsoft Office installieren, diese Funktionen verwenden können, ohne eine Verbindung zu konfigurieren. Damit können Benutzer geschützte Dokumente öffnen, ohne dass eine Konfiguration erforderlich ist. Sie können jedoch keine neuen Dokumente schützen, bis sie den Client für die Verwendung eines bestimmten Servers konfigurieren.

Im Folgenden werden die Schritte zum Erstellen und Konfigurieren einer MSI-Datei beschrieben. Diese MSI-Datei enthält die Registrierungswerte, die erforderlich sind, um das Installationsprogramm von Document Security Extension for Microsoft Office auf dem in Ihrem Unternehmen installierten LiveCycle- oder AEM-Server vorkonfigurieren zu können.

### Voraussetzungen für die Anpassung des Installationsprogramms {#prerequisites-for-customizing-the-installer}

Verwenden Sie den Orca-Datenbank-Editor, um das Installationsprogramm anzupassen. Die folgenden Schritte beschreiben, wie Sie eine benutzerdefinierte MSI-Datei erstellen, indem Sie eine Kopie der MSI-Installationsdatei mit dem Orca-Datenbank-Editor bearbeiten. Orca ist als Teil des Windows SDK für Windows Server 2008 und .NET Framework 3.5 verfügbar.

<!--

For more information about how to edit Microsoft Windows® Installer files using Orca, see [Microsoft Support](http://support.microsoft.com/kb/255905/EN-US/).

-->

>[!NOTE]
>
>Es wird empfohlen, eine vollständige Sicherung aller Installer-Dateien zu erstellen, bevor Sie die benutzerdefinierte MSI-Datei erstellen.

#### Installieren von Orca {#install-orca}

1. Laden Sie das Windows SDK für Windows Server 2008 und .NET Framework 3.5 herunter.
1. Doppelklicken Sie auf die Datei „Orca.msi“ im Ordner „\Microsoft SDK\bin“.

   Sie benötigen auch die MSI-Variante der Installationsdatei. Wenden Sie sich an den Adobe-Support, um die neueste Version des MSI-Installationsprogramms zu erhalten.

   >[!NOTE]
   >
   >Schließen Sie immer die Datei „DocumentSecurityExtensionforMicrosoftOffice.msi“, bevor Sie das Installationsprogramm ausführen. Sie können das Installationsprogramm nicht ausführen, wenn Orca die MSI-Datei verwendet.

### Erstellen und Konfigurieren der MSI-Datei {#create-and-configure-the-msi-file}

1. Klicken Sie auf **[!UICONTROL Start > Programme > Orca]**.

1. Klicken Sie auf **[!UICONTROL Datei > Öffnen]** und navigieren Sie dann zur Datei `DocumentSecurityExtensionforMicrosoftOffice.msi`.

1. Wählen Sie die Eigenschaft aus der Tabellenliste (links) aus.

1. Bearbeiten Sie die folgenden Schlüsselnamenwerte, sofern sie auf Ihre Unternehmensinstallation von Rights Management oder Document Security zutreffen.

<table>
 <tbody>
  <tr>
   <td><p><strong></strong><strong></strong><strong>Schlüsselname</strong></p> </td>
   <td><p><strong>Beschreibung</strong></p> </td>
   <td><p><strong>Standardwert </strong><strong></strong><strong>des Schlüssels</strong></p> </td>
  </tr>
  <tr>
   <td><p><code>APS_SERVER_NAME</code></p> </td>
   <td><p>Anzeigename.</p> </td>
   <td><p>Standard-Server</p> </td>
  </tr>
  <tr>
   <td><p><code>APS_SERVER_URL</code></p> </td>
   <td><p>Host-Server-URL.</p> </td>
   <td><p>https://default.corp.com:1234</p> </td>
  </tr>
 </tbody>
</table>

1. Wählen Sie die Registrierung aus der Tabellenliste (links) aus.

1. Bearbeiten Sie den folgenden Schlüsselnamenwert.

   | **Schlüsselname** | **Beschreibung** | **Standardwert des Schlüssels** |
   |---|---|---|
   | `IsDefault` | Der standardmäßige APS-Server. | Standard-Server |

1. Speichern Sie die bearbeitete Datei in demselben Verzeichnis, in dem sich das ursprüngliche MSI-Installationsprogramm befindet.

   >[!NOTE]
   >
   >Üblicherweise wird derselbe Dateiname wie die ursprüngliche MSI-Datei verwendet (zum Beispiel `DocumentSecurityExtensionforMicrosoftOffice.msi`).

## Konfigurieren der automatischen Anwendung einer Standardrichtlinie {#configuring-automatic-application-of-a-default-policy}

Als Teil der Konfiguration können Sie die automatische Anwendung einer Standardrichtlinie konfigurieren, damit Document Security Extension for Microsoft Office jedes gespeicherte Dokument schützt.

Sie können eine der folgenden Optionen angeben:

* Alle Dokumente mit einer Standardrichtlinie schützen.
* Benutzer können optional eine Datei in einem ungeschützten Format speichern, wenn sie keine Verbindung zum Server herstellen können. Diese Flexibilität ermöglicht es Ihnen, Fälle zu berücksichtigen, in denen Benutzer Dokumente erstellen, während sie vom Netzwerk getrennt sind (z. B. im Flugzeug).

Nachdem Sie die Funktion „Richtlinie automatisch anwenden“ aktiviert haben, wird das Dokument in den folgenden Fällen mit der Standardrichtlinie geschützt:

* Benutzer bearbeitet und speichert ein neu erstelltes Dokument.
* Benutzer bearbeitet und speichert ein ungeschütztes Dokument.
* Benutzer öffnet ein Programm, das mit einem Standarddokument geöffnet wird, bearbeitet das Dokument und speichert es anschließend.

### Konfigurieren der Funktion zum automatischen Anwenden von Richtlinien in der MSI-Datei  {#configure-the-auto-apply-policy-feature-in-the-msi-file}

Nehmen Sie zuerst eine Vorkonfiguration des Installationsprogramms vor, um auf den LiveCycle- oder AEM Forms-Server zu verweisen (wie zuvor in diesem Artikel beschrieben).

1. Klicken Sie auf **[!UICONTROL Start > Programme > Orca]**.

1. Klicken Sie auf **[!UICONTROL Datei > Öffnen]** und navigieren Sie dann zur Datei `DocumentSecurityExtensionforMicrosoftOffice.msi`.

1. Wählen Sie die Eigenschaft aus der Tabellenliste (links) aus.

1. Bearbeiten Sie die folgenden Schlüsselnamenwerte, sofern sie auf Ihre Unternehmensinstallation von Rights Management oder Document Security zutreffen.

<table>
 <tbody>
  <tr>
   <td><p><strong>Schlüsselname</strong></p> </td>
   <td><p><strong>Beschreibung</strong></p> </td>
   <td><p><strong>Standardwert </strong><strong></strong><strong>des Schlüssels</strong></p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_IS_AUTO_ APPLY</code></p> </td>
   <td><p>Aktivieren oder deaktivieren Sie die Funktion zum automatischen Anwenden von Richtlinien.</p> <p><code>1</code>: Aktivieren</p> <p>0: Deaktivieren</p> </td>
   <td><p>0</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_POLICY_I D</code></p> </td>
   <td><p>Die Richtlinien-GUID, die beim Speichern neuer Dokumente verwendet werden soll. Gilt für die Funktion zum automatischen Anwenden von Richtlinien.</p> </td>
   <td><p>Hexadezimale Richtlinien-ID, wie sie auf dem RM-Server sichtbar ist</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_SERVER_U RL</code></p> </td>
   <td><p>Server-URL.</p> </td>
   <td><p>default.corp.com</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_SERVER_P ORT_NO</code></p> </td>
   <td><p>Serverport-Nummer.</p> </td>
   <td><p>1234</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_ALLOW_UN PROTECTED_SAVE</code></p> </td>
   <td><p>Legt fest, ob Dokumente ohne Document Security-Schutz erstellt werden können, wenn der Client den Server nicht kontaktieren kann, um das Dokument beim ersten Speichern zu schützen.</p> <p>1: Ungeschütztes Speichern zulassen </p> <p>0: Die Erstellung neuer Dokumente verhindern, wenn der Client den Server nicht zum Speichern des Dokuments kontaktieren kann.</p> </td>
   <td><p>0</p> </td>
  </tr>
 </tbody>
</table>

>[!NOTE]
>
>Die Option `AUTO_APPLY_POLICY_ALLOW_UN PROTECTED_SAVE` ist nützlich, wenn Sie Kunden daran erinnern wollen, alle Dokumente zu schützen, ohne sie dazu zu zwingen. Dies ist auch nützlich, wenn Sie wissen, dass Benutzer Dokumente erstellen, während sie vom Netzwerk getrennt sind. Sie möchten sie nicht daran hindern, Dokumente zu erstellen und zu speichern.

1. Speichern Sie die bearbeitete Datei in demselben Verzeichnis, in dem sich die ursprüngliche MSI-Datei befindet.

   >[!NOTE]
   >
   >Üblicherweise wird derselbe Dateiname wie die ursprüngliche MSI-Datei verwendet (zum Beispiel `DocumentSecurityExtensionforMicrosoftOffice.msi`).

## Aktivieren des automatischen Schutzes neuer Dokumente {#enabling-automatic-protection-of-new-documents}

Der Administrator kann die Möglichkeit zum automatischen Schutz jedes Dokuments aktivieren, das ein Benutzer speichert. Der Administrator konfiguriert die Funktion „Richtlinie automatisch anwenden“ im Installationsprogramm für Document Security Extension for Microsoft Office.

Wenn die Option „Richtlinie automatisch anwenden“ aktiviert ist, werden alle vom Benutzer gespeicherten Dokumente mit der Standardrichtlinie geschützt. Diese Aktion gilt in folgenden Situationen:

* Wenn ein Benutzer ein neues Dokument erstellt, es bearbeitet und speichert.
* Wenn ein Benutzer ein ungeschütztes Dokument öffnet, bearbeitet und speichert.

Informationen zum Konfigurieren der automatischen Anwendung von Richtlinien finden Sie unter [Automatische Anwendung der Standardrichtlinie konfigurieren](installing-configuring-aemdsext.md#p-configuring-automatic-application-of-a-default-policy-p).

## Benutzeroberfläche ohne Menüband aktivieren {#enable-ribbon-less-user-interface}

Sie können die Benutzeroberfläche ohne Menüband aktivieren/deaktivieren, indem Sie die Einstellungen in der Windows Registry ändern. Führen Sie die folgenden Schritte aus, um die Registry zu aktualisieren und die Benutzeroberfläche ohne Menüband zu aktivieren:

1. Erstellen Sie eine Sicherungskopie von Windows Registry, bevor Sie Änderungen daran vornehmen. Detaillierte Anweisungen finden Sie unter [Ändern der Windows Registry](https://support.microsoft.com/de-de/kb/136393).
1. Navigieren Sie im Registrierungs-Editor zu HKEY_CURRENT_USER\Software\Adobe\LiveCycle Rights Management ES4\11.0.0 oder HKEY_LOCAL_MACHINE\Software\Adobe\LiveCycle Rights Management ES4\11.0.0
1. Erstellen Sie einen neuen Dword-Wert (32 Bit) mit dem Namen **HidePluginUI**.

1. Legen Sie den Wert der Eigenschaft **HidePluginUI** auf 1 fest, um die Benutzeroberfläche ohne Menüband zu aktivieren.

1. Schließen Sie den Registrierungseditor.

## Aktivieren des Wasserzeichens zum Drucken in Microsoft Excel {#enable-watermark-for-printing-in-microsoft-excel}

Sie können die Einstellungen der Windows-Registrierung ändern, damit dynamische Wasserzeichen zusammen mit vorhandenen Kopf- und Fußzeilen vorhanden sind. Die Registrierungseinstellungen machen das Wasserzeichen nur während des Druckens verfügbar. Führen Sie die folgenden Schritte aus, um die Registrierung zu aktualisieren und Wasserzeichen während des Druckens zu aktivieren:

1. Erstellen Sie eine Sicherungskopie von Windows Registry, bevor Sie Änderungen daran vornehmen. Detaillierte Anweisungen finden Sie unter [Ändern der Windows Registry](https://support.microsoft.com/de-de/kb/136393).
1. Navigieren Sie im Registrierungs-Editor zu HKEY_CURRENT_USER\Software\Adobe\LiveCycle Rights Management ES4\11.0.0 oder HKEY_LOCAL_MACHINE\WOW6432NODE\Software\Adobe\LiveCycle Rights Management ES4\11.0.0
1. Neuen Registrierungsschlüssel erstellen **WatermarkMode**.
1. Erstellen Sie im WatermarkMode-Registrierungsschlüssel ein DWORD **WatermarkMode** und legen Sie den Wert von DWORD fest **WatermarkMode** nach **1**.

1. Schließen Sie den Registrierungs-Editor.

>[!NOTE]
>
>In Windows Explorer können Sie das Menü Datei oder das Kontextmenü verwenden, um ein Microsoft Excel-Dokument zu erstellen. Bei Dokumenten, die mit angegebenen Methoden erstellt wurden, kann das Druckdatum nicht abgerufen oder geändert werden. Dies ist eine Einschränkung von Microsoft Excel. AEM Document Security-Wasserzeichen hängen vom Druckdatum des Dokuments ab. Bei solchen Dokumenten wird das Wasserzeichen also auf ein vorheriges Datum zurückgesetzt. Außerdem werden Kopf- und Fußzeilen nicht beibehalten.

## Eine benutzerdefinierte Titelseite hinzufügen {#coverpage}

Ein Benutzer kann versuchen, das geschützte Dokument auf einem Computer zu öffnen, das keine AEM Document Security for Microsoft Office-Plug-in installiert hat. Solche Computer können das Dokument nicht öffnen. Auf solchen Computern können Sie eine Titelseite anzeigen, die Anweisungen zum Verwenden von AEM Document Security for Microsoft Office-Plug-in und anderen Informationen enthalten.

### Vor der Konfiguration der Titelseite {#before-you-configure-a-cover-page}

* Erstellen Sie eine Sicherungskopie der Datei „CommonResources.dll“. Der Standardpfad lautet:

   * **(Für 32-Bit Office auf 32-Bit-Computern)** C:\Program Files\Adobe\Adobe Experience Manager Forms\Document Security Extension

   * **(Für 32-Bit Office auf 64-Bit Computern)** C:\Program Files (x86)\Adobe\Adobe Experience Manager Forms\Document Security Extension

   * **(Für 64-Bit Office auf 64-Bit-Computern)** C:\Program Files\Adobe\Adobe Experience Manager Forms\Document Security Extension

* Stellen Sie sicher, dass Microsoft Visual Studio 2008 oder höher installiert ist. Sie können auch jedes andere Dienstprogramm verwenden, um die DLL-Dateien zu bearbeiten.
* Extrahieren Sie das templates.zip-Archiv. Das Archiv enthält .xlsx-, .docx- und .pptx-Vorlagen für die Titelseite. Verwenden Sie nur bereitgestellte Vorlagen für Dateitypen .xlsx, .docx und .pptx. Sie können eigene Vorlagen für andere Dateitypen erstellen. Passen Sie Vorlagen an, um benutzerdefinierte Nachrichten und Anweisungen einzuschließen. Die Datei „template.zip“ finden Sie unter:

[Datei laden](assets/templates.zip)

### Struktur der Datei „CommonResources.dll“ {#structure-of-the-commonresources-dll-file}

Die Datei CommonResources.dll enthält Informationen zu den Ressourcenvorlagen. Es enthält zwei Namenskennungen TEMPLATE_FILE und RT_MANIFEST. Um eine benutzerdefinierte Titelseite zu aktivieren, wird die TEMPLATE_FILE-Namenskennung geändert. Der TEMPLATE_FILE-Namensbezeichner verfügt über sechs Ressourcen:

<table>
 <tbody>
  <tr>
   <td><p><strong>Ressource</strong></p> </td>
   <td><p><strong>Repräsentiert </strong></p> </td>
  </tr>
  <tr>
   <td><p>101 </p> </td>
   <td><p>.xls</p> </td>
  </tr>
  <tr>
   <td><p>102</p> </td>
   <td><p>.doc</p> </td>
  </tr>
  <tr>
   <td><p>103 </p> </td>
   <td><p>.ppt</p> </td>
  </tr>
  <tr>
   <td><p>104 </p> </td>
   <td><p>.xlsx</p> </td>
  </tr>
  <tr>
   <td><p>105</p> </td>
   <td><p>.docx</p> </td>
  </tr>
  <tr>
   <td><p>106</p> </td>
   <td><p>.pptx</p> </td>
  </tr>
 </tbody>
</table>

#### Konfigurieren der Vorlage als Titelseite {#configure-the-template-as-a-cover-page}

1. Öffnen Sie Microsoft Visual Studio. Öffnen Sie die Datei „CommonResources.dll“, um sie zu bearbeiten.

   >[!NOTE]
   >
   >Wenn die Datei nicht im Projektmappen-Explorer-Fenster angezeigt wird, öffnen Sie die Datei mit der Option Öffnen mit erneut. Wählen Sie den Ressourcen-Editor als Editor aus.

1. Erweitern Sie im „Solution Explorer“-Fenster, das Verzeichnis „TEMPLATE_FILE“ und löschen Sie Ressourcen „101“.

1. Fügen Sie die Ressourcen hinzu:

   1. Klicken Sie bei in Solution Explorer ausgewähltem Projekt im Menü Projekt auf Eigenschaften .
   1. Wählen Sie die Registerkarte Ressourcen .
   1. Zeigen Sie in der Symbolleiste &quot;Resource Designer&quot;auf &quot;Ressource hinzufügen&quot;und klicken Sie auf den Pfeil. Wählen Sie als Ressourcentyp TEMPLATE_FILE und klicken Sie auf &quot;Importieren&quot;.
   1. Navigieren Sie im Dialogfeld Vorhandene Datei zu Ressourcen hinzufügen zur Datei Resource.xlsx und klicken Sie auf &quot;Öffnen&quot;. Die Datei wird dem Verzeichnis TEMPLATE_FILE hinzugefügt.

   >[!NOTE]
   >
   >Stellen Sie sicher, dass die Spracheinstellungen korrekt sind. Löschen Sie die Ressource in neutraler Sprache.

1. Wiederholen Sie die Schritte 2 und 3 für alle Ressourcentypen.

   >[!NOTE]
   >
   >Löschen und fügen Sie Ressourcentypen nicht in zufälliger Reihenfolge hinzu. Nach „101“, konfigurieren Sie „102“ usw.

### Verpacken Sie die benutzerdefinierte Datei „CommonResources.dll“ mit dem Installationsprogramm von AEM Document Security Extension for Microsoft Office  {#package-custom-commonresources-dll-file-with-the-installer-of-aem-document-security-extension-for-microsoft-office}

Sie können die Datei „CommonResources.dll“ anpassen, um eine benutzerdefinierte Titelseite einzubeziehen. Nach dem Anpassen der Datei können Sie die Originaldatei mit der benutzerdefinierten Datei auf allen Computern manuell ersetzen oder eine automatische Methode zum Ersetzen der Datei wählen.

In einer großen Umgebung ist es schwierig und mühsam, die Standarddatei `CommonResources.dll file` durch eine benutzerdefinierte Datei `CommonResources.dll` manuell zu ersetzen. Sie können ein selbstentpackendes und Verpackungswerkzeug verwenden (z. B. WinZip Self-Extractor), um die benutzerdefinierte CommonResources.dll-Datei mit AEM Document Security Extension for Microsoft Office-Installationsprogramm zu verpacken. Später können Sie das benutzerdefinierte Installationsprogramm an alle Workstations verteilen. Diese Methode reduziert die Zeit, die benötigt wird, um die Standarddatei `CommonResources.dll` durch eine benutzerdefinierte Datei zu ersetzen. Außerdem wird sichergestellt, dass alle Computer die erforderliche CommonResources.dll-Datei haben. Das Tool zum Selbstextrahieren und Verpacken ist nur eine der vielen möglichen Methoden zum automatischen Ersetzen einer Datei. Sie können die Methode wählen, die für Sie und Ihre Umgebung geeignet ist.

Sie können die folgenden Schritte ausführen, um die benutzerdefinierte `CommonResources.dll`-Datei mit dem Installationsprogramm der AEM Document Security Extension for Microsoft Office zu verpacken:

1. Installieren Sie ein selbstentpackendes und Verpackungswerkzeug. Beispiel: WinZip Self-Extractor.
1. Erstellen Sie einen neuen Ordner. Beispiel: YOUR_FOLDER_NAME
1. Platzieren Sie das ursprüngliche Installationsprogramm AEM Document Security-Erweiterung und die benutzerdefinierte CommonResources.dll-Datei in den neu erstellten Ordner.
1. Erstellen Sie eine Batch-Datei im Ordner . Beispiel: YOUR_FOLDER_NAME\Installer.bat
1. Öffnen Sie die Batch-Datei zur Bearbeitung und fügen Sie der Batch-Datei den folgenden Code hinzu:

   ```shell
    @echo off
   
    setlocal EnableDelayedExpansion
   
    msiexec /i YOUR_FOLDER_NAME\MSI_NAME.exe
   
   
    FOR /F "tokens=2,*" %%A IN ('REG query "HKLM\HARDWARE\DESCRIPTION\System\CentralProcessor\0" /v "Identifier"') DO set "IDENTIFIER=%%B"
   
    set IDENTIFIER= %IDENTIFIER: =%
   
    if not %IDENTIFIER:x86=%==%IDENTIFIER% (
   
    REM Fetching install path for 32 bit machine.
   
    FOR /F "tokens=2,*" %%A IN ('REG query "HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0" /v "InstallPath"') DO set "INSTALLPATH=%%B"
   
    ) else (
   
        REM Fetching install path for 64 bit machine.
   
            FOR /F "tokens=2,*" %%A IN ('REG query "HKLM\SOFTWARE\Wow6432Node\Adobe\LiveCycle Rights Management ES4\11.0.0" /v "InstallPath"') DO set "INSTALLPATH=%%B"
   
        )
   
    COPY "YOUR_FOLDER_NAME\CommonResources.dll" "%INSTALLPATH%"
   
    endlocal
   ```

   Wenn Sie eine andere Version von LiveCycle oder AEM Forms on JEE außer LiveCycle Rights Management ES4 und Version 11.0.0 verwenden, ersetzen Sie den Pfad des Registrierungsschlüssels wie folgt:

   * (LiveCycle Rights Management ES2 und Version 9.0): *HKLM\SOFTWARE\Adobe/LiveCycle* *Rights Management ES2\9.0 *
   * (LiveCycle Rights Management ES3 und Version 10.0)
   * (LiveCycle Rights Management ES4 und Version 11.0) HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0
   * (AEM 6.0 Forms on JEE und höher) HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0

1. Ersetzen Sie im obigen Code alle Instanzen von YOUR_FOLDER_NAME durch den Namen des Ordners, den Sie in Schritt 2 erstellt haben.
1. **(AEM Document Security Extension for Microsoft Office-Installationsprogramm nur mit der Erweiterung .exe )** Ersetzen Sie die folgende Codezeile:

   `msiexec /i YOUR_FOLDER_NAME\MSI_NAME.msi`
durch

   `START /w YOUR_FOLDER_NAME\APPLICATION_NAME.exe`

1. Speichern und schließen Sie die Batch-Datei.
1. Sie können ein selbstentpackendes und Verpackungs-Tool verwenden, um den Ordner, der die benutzerdefinierte CommonResources.dll-Datei, das Originalinstallationsprogramm von AEM Document Security Extension for Microsoft Office und die Batch-Datei enthält, zu verpacken.

   >[!NOTE]
   >
   >Stellen Sie sicher, dass das selbstextrahierende Paket so eingestellt ist, dass es als Administrator ausgeführt wird und
   >die Batch-Datei nach Abschluss der Extraktion automatisch ausgeführt wird.

Jetzt komprimiert das selbstentpackende Installationsprogramm der AEM Document Security Extension for Microsoft Office-Pakete die benutzerdefinierte CommonResources.dll-Datei und steht zur Bereitstellung bereit.