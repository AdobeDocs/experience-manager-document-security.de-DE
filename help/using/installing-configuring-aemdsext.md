---
title: Installieren und Konfigurieren von AEM Document Security Extension for Microsoft Office
description: Dieses Dokument erläutert die Installation und Konfiguration von Adobe Experience Manager Document Security Extension 6.2 for Microsoft Office.
uuid: 9d7eb6bb-4780-4d82-8657-7c6c6d523af0
content-type: reference
topic-tags: installing
discoiquuid: f1cdf344-efe4-4cb5-9fc3-47ee4ba5faf4
exl-id: 88759737-d57f-4354-951e-ad9f62d0a872
source-git-commit: 69abd3e49fcf79b8bf2a7f344abeeae250b1479f
workflow-type: ht
source-wordcount: '2845'
ht-degree: 100%

---

# Installieren und Konfigurieren von AEM Document Security Extension for Microsoft Office{#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

Dieses Dokument erläutert die Installation und Konfiguration von Adobe Experience Manager Document Security Extension for Microsoft Office.

Dieses Dokument enthält Informationen zu den folgenden Aufgaben:

* Installieren von Document Security Extension for Microsoft Office.
* Vorkonfigurieren des Installationsprogramms, um auf LiveCycle Rights Management ES2 oder höher und das Document Security-Add-on für AEM 6.0 Forms oder höher zu verweisen.
* Konfigurieren der automatischen Anwendung der Standardrichtlinie.

## Vor der Installation {#before-you-install}

Bevor Sie Document Security Extension for Microsoft Office installieren, stellen Sie Folgendes sicher:

* Sie haben die [Versionshinweise](document-security-extension-release-notes.md) gelesen.
* Microsoft Office ist aktiviert. Aktivierungsdialogfeld wird nicht angezeigt beim Öffnen von Microsoft Office-Programmen.
* Neueste Service Packs für Microsoft Windows und Microsoft Office sind installiert.
* Wenn Sie Document Security for Microsoft Office für eine nicht unterstützte Sprache installieren, müssen Sie das Office-Programm mindestens einmal öffnen.

>[!NOTE]
>
>Installieren Sie die Software nicht in einem Ordner, dessen Name Doppel-Byte-Zeichen enthält. Wenn Sie dies tun, wird das AEM Document Security-Menü nicht in Microsoft Office angezeigt.

>[!NOTE]
>
>Die Installation einer 32-Bit-Version von Document Security Extension auf einem 64-Bit-Betriebssystem wird unterstützt, der umgekehrte Fall aber nicht. Sie können einer 64-Bit-Version von Document Security Extension for Microsoft Office nicht auf einem 32-Bit-Betriebssystem installieren.

### Deaktivieren von McAfee VirusScan {#disable-mcafee-virusscan}

Deaktivieren Sie in der McAfee VirusScan-Konsole die Option für den Pufferüberlaufschutz. Dadurch wird sichergestellt, dass Office-Anwendungen sich reibungslos auf einem Computer starten lassen, auf dem Document Security Extension installiert ist. Außerdem ist McAfee VirusScan On-Access Scan aktiviert. Diese Anpassungen helfen dabei, Konflikte zu vermeiden, die den Startprozess behindern könnten.

### Deinstallieren von Plug-ins von Drittanbietern {#uninstall-third-party-plug-ins}

AEM Document Security Extension for Microsoft Office unterstützt keine Plug-ins von Drittanbietern für Microsoft Office-Programme. Da diese Erweiterung mit Plug-ins von Drittanbietern im Konflikt steht, deinstallieren Sie alle Plug-ins von Drittanbietern für Microsoft Office, bevor Sie Document Security for Microsoft Office installieren. Adobe unterstützt Document Security for Microsoft Office nicht, wenn Plug-ins von Drittanbietern installiert sind.

## Systemanforderungen {#system-requirements}

### Document Security Extension-Client {#document-security-extension-client}

Stellen Sie sicher, dass die folgenden Mindestkonfigurationen für die Installation der Document Security Extension verwendet werden:

* 32-Bit- oder 64-Bit-Versionen von Microsoft Office 2019 Professional Plus unter Microsoft Windows 11 auf Englisch, Französisch, Deutsch, Japanisch, Italienisch, Spanisch, Portugiesisch (Brasilien), Koreanisch, Chinesisch (vereinfacht oder traditionell).

* 32-Bit- oder 64-Bit-Versionen von Microsoft Windows 10 auf Englisch, Französisch, Deutsch, Japanisch, Italienisch, Spanisch, Portugiesisch (Brasilien), Koreanisch, Chinesisch (vereinfacht oder traditionell).

  **Hinweis:** *Es wird erwartet, dass Document Security Extension for Microsoft Office auf Microsoft Surface-Geräten funktioniert.*

* 32-Bit- oder 64-Bit-Versionen von Microsoft Office 2016, 2019 und Microsoft Office Desktop-Anwendungen, die als Teil von Office 365 auf Englisch, Französisch, Deutsch, Japanisch, Italienisch, Spanisch, Portugiesisch (Brasilien), Koreanisch oder Chinesisch (vereinfacht und traditionell) installiert sind.

  **Hinweis**: *AEM Document Security Extension for Microsoft Office unterstützt keine Plug-ins von Drittanbietern für Microsoft Office-Programme. Da Konflikte zwischen Plug-ins von Drittanbietern und dieser Erweiterung auftreten können, müssen Sie vor der Installation von Document Security Extension for Microsoft Office alle Plug-ins für Microsoft Office-Programme deinstallieren, die nicht von Adobe stammen. Adobe unterstützt Document Security Extension for Microsoft Office nicht, wenn Plug-ins von Drittanbietern installiert sind.*

* Prozessor mit 1,3 GHz oder höher
* 2 GB RAM
* 100 MB verfügbarer Festplattenspeicher

### Document Security {#document-security}

Um Document Security Extension zu verwenden, stellen Sie sicher, dass Sie eine Verbindung zu Adobe LiveCycle Rights Management ES2 und höher oder Document Security-Add-on für AEM 6.0 Forms oder höher herstellen können.

## Installieren von Document Security Extension for Microsoft Office {#installing-document-security-extension-for-microsoft-office}

Sie können das Installationsprogramm von der [Download-Seite](download-installer.md) herunterladen. Sie können die ausführbare Datei des Installationsprogramms nicht direkt anpassen, sie kann jedoch interaktiv oder im Hintergrund installiert werden. Melden Sie sich zur Installation der Software bei Windows als Admin an.

Separate Installationsprogramme sind für 32-Bit- und 64-Bit-Versionen von Microsoft Office verfügbar. Laden Sie für eine 32-Bit-Version von Microsoft Office die Datei „DocumentSecurityExtensionforMicrosoftOffice.exe“ herunter. Laden Sie für eine 64-Bit-Version von Microsoft Office die Datei „DocumentSecurityExtensionforMicrosoftOffice64.exe“ herunter.

>[!NOTE]
>
>In diesem Dokument wird die 32-Bit-Installationsdatei (DocumentSecurityExtensionforMicrosoftOffice.exe) verwendet, um verschiedene Befehle und Optionen zu erklären. Wenn Sie eine 64-Bit-Version von Microsoft Office nutzen, verwenden Sie die 64-Bit-Installationsdatei (DocumentSecurityExtensionforMicrosoftOffice64.exe), um die in diesem Dokument genannten Vorgänge auszuführen.

### Installation im Hintergrund {#install-in-silent-mode}

Verwenden Sie ein Dienstprogramm zum Extrahieren von Dateien, wie z. B. WinZip, um die Datei `DocumentSecurityExtensionforMicrosoftOffice.exe` aus der Installationsdatei zu extrahieren. Öffnen Sie die Eingabeaufforderung, navigieren Sie zum Ordner, der die Setup-Datei enthält, und geben Sie den folgenden Text ein:

`DocumentSecurityExtensionforMicrosoftOffice.exe -s -a -s -v" /qn"`

Das Installationsprogramm steht auch als MSI-Datei zur Verfügung, die zur Anpassung verwendet werden kann.

### Installieren einer MSI-Datei im Hintergrund {#install-an-msi-file-in-silent-mode}

1. Verwenden Sie ein Dienstprogramm zum Extrahieren von Dateien, wie z. B. WinZip, um die Datei `DocumentSecurityExtensionforMicrosoftOffice.msi` aus der ZIP-Datei zu extrahieren.

1. Öffnen Sie die Eingabeaufforderung, navigieren Sie zum Ordner, der die MSI-Datei enthält, und geben Sie den folgenden Text ein:

   `msiexec /I DocumentSecurityExtensionforMicrosoftOffice.msi /qn`

## Vorkonfigurieren des Installationsprogramms für die Verbindung mit Document Security {#preconfiguring-the-installer-to-connect-to-document-security}

Sie können Document Security Extension für das Microsoft Office-Installationsprogramm so vorkonfigurieren, dass auf einen LiveCycle- oder AEM-Server verwiesen wird. Dadurch wird sichergestellt, dass Benutzende, die Document Security Extension for Microsoft Office installieren, die Funktionen verwenden können, ohne eine Verbindung konfigurieren zu müssen. Damit können Benutzer geschützte Dokumente öffnen, ohne dass eine Konfiguration erforderlich ist. Sie können jedoch keine neuen Dokumente schützen, bis sie den Client für die Verwendung eines bestimmten Servers konfigurieren.

Im Folgenden werden die Schritte zum Erstellen und Konfigurieren einer MSI-Datei beschrieben. Diese MSI-Datei enthält die Registrierungswerte. Diese Werte sind erforderlich, um das Document Security Extension for Microsoft Office-Installationsprogramm auf dem in Ihrem Unternehmen installierten LiveCycle- oder AEM-Server vorkonfigurieren zu können.

### Voraussetzungen für die Anpassung des Installationsprogramms {#prerequisites-for-customizing-the-installer}

Verwenden Sie den Orca-Datenbank-Editor, um das Installationsprogramm anzupassen. Die folgenden Schritte beschreiben, wie Sie eine benutzerdefinierte MSI-Datei erstellen, indem Sie eine Kopie der MSI-Installationsdatei mit dem Orca-Datenbank-Editor bearbeiten. Orca ist als Teil des Windows SDK für Windows Server 2008 und .NET Framework 3.5 verfügbar.

<!--

For more information about how to edit Microsoft Windows&reg; Installer files using Orca, see [Microsoft Support](http://support.microsoft.com/kb/255905/EN-US/).

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
   <td><p>Zeigt Ihren Namen an.</p> </td>
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

Als Teil der Konfiguration können Sie die automatische Anwendung einer Standardrichtlinie konfigurieren, damit Document Security Extension für Microsoft Office jedes gespeicherte Dokument schützt.

Sie können eine der folgenden Optionen angeben:

* Alle Dokumente mit einer Standardrichtlinie schützen.
* Zulassen, dass Benutzende optional eine Datei in einem ungeschützten Format speichern können, wenn keine Server-Verbindung möglich ist. Diese Flexibilität ermöglicht es Ihnen, Fälle zu berücksichtigen, in denen Benutzer Dokumente erstellen, während sie vom Netzwerk getrennt sind (z. B. im Flugzeug).

Nachdem Sie die Funktion „Richtlinie automatisch anwenden“ aktiviert haben, wird das Dokument in den folgenden Fällen mit der Standardrichtlinie geschützt:

* Eine Benutzerin oder ein Benutzer bearbeitet und speichert ein neu erstelltes Dokument.
* Eine Benutzerin oder ein Benutzer bearbeitet und speichert ein ungeschütztes Dokument.
* Eine Benutzerin oder ein Benutzer öffnet eine Anwendung, die mit einem Standarddokument geöffnet wird, bearbeitet das Dokument und speichert es anschließend.

### Konfigurieren der Funktion zum automatischen Anwenden von Richtlinien in der MSI-Datei {#configure-the-auto-apply-policy-feature-in-the-msi-file}

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
   <td><p>Aktiviert oder deaktiviert die Funktion zum automatischen Anwenden von Richtlinien.</p> <p><code>1</code>: Aktivieren</p> <p>0: Deaktivieren</p> </td>
   <td><p>0</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_POLICY_I D</code></p> </td>
   <td><p>Die Richtlinien-GUID, die beim Speichern neuer Dokumente verwendet werden soll. Dieser Wert gilt für die Funktion zum automatischen Anwenden von Richtlinien.</p> </td>
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
>Die Option `AUTO_APPLY_POLICY_ALLOW_UN PROTECTED_SAVE` ist nützlich, wenn Sie Kundinnen und Kunden daran erinnern möchten, alle Dokumente zu schützen, ohne sie dazu zu zwingen. Dies ist auch nützlich, wenn Sie wissen, dass Benutzende Dokumente erstellen, während sie vom Netzwerk getrennt sind. Sie möchten sie nicht daran hindern, Dokumente zu erstellen und zu speichern.

1. Speichern Sie die bearbeitete Datei in demselben Verzeichnis, in dem sich die ursprüngliche MSI-Datei befindet.

   >[!NOTE]
   >
   >Üblicherweise wird derselbe Dateiname wie die ursprüngliche MSI-Datei verwendet (zum Beispiel `DocumentSecurityExtensionforMicrosoftOffice.msi`).

## Aktivieren des automatischen Schutzes neuer Dokumente {#enabling-automatic-protection-of-new-documents}

Administratorseitig kann die Möglichkeit zum automatischen Schutz jedes Dokuments, das eine Benutzerin oder ein Benutzer speichert, aktiviert werden. Die Admins konfigurieren die Funktion „Richtlinie automatisch anwenden“ im Installationsprogramm für Document Security Extension für Microsoft Office.

Wenn die Option zum automatischen Anwenden von Richtlinien aktiviert ist, werden alle benutzerseitig gespeicherten Dokumente mit der Standardrichtlinie geschützt. Diese Aktion gilt in folgenden Situationen:

* Wenn ein Benutzer ein neues Dokument erstellt, es bearbeitet und speichert.
* Wenn ein Benutzer ein ungeschütztes Dokument öffnet, bearbeitet und speichert.

Informationen zum Konfigurieren der automatischen Anwendung von Richtlinien finden Sie unter [Konfigurieren der automatischen Anwendung der Standardrichtlinie](installing-configuring-aemdsext.md#p-configuring-automatic-application-of-a-default-policy-p).

## Aktivieren der Benutzeroberfläche ohne Menüband {#enable-ribbon-less-user-interface}

Sie können die Benutzeroberfläche ohne Menüband aktivieren/deaktivieren, indem Sie die Einstellungen in der Windows-Registrierung ändern. Führen Sie die folgenden Schritte aus, um die Registrierung zu aktualisieren und die Benutzeroberfläche ohne Menüband zu aktivieren:

1. Erstellen Sie ein Backup der Windows-Registrierung, bevor Sie Änderungen daran vornehmen. Ausführliche Anweisungen finden Sie unter [Wie ändere ich die Windows-Registrierung](https://learn.microsoft.com/de-de/troubleshoot/windows-server/performance/windows-registry-advanced-users).
1. Navigieren Sie im Registrierungs-Editor zu HKEY_CURRENT_USER\Software\Adobe\LiveCycle Rights Management ES4\11.0.0 oder HKEY_LOCAL_MACHINE\Software\Adobe\LiveCycle Rights Management ES4\11.0.0
1. Erstellen Sie einen neuen Dword-Wert (32 Bit) mit dem Namen **HidePluginUI**.

1. Legen Sie den Wert der Eigenschaft **HidePluginUI** auf „1“ fest, um die Benutzeroberfläche ohne Menüband zu aktivieren.

1. Schließen Sie den Registrierungseditor.

## Aktivieren des Wasserzeichens zum Drucken in Microsoft Excel {#enable-watermark-for-printing-in-microsoft-excel}

Sie können die Einstellungen in der Windows-Registrierung ändern, damit ein dynamisches Wasserzeichen gleichzeitig mit vorhandenen Kopf- und Fußzeilen verwendet werden kann. Die Registrierungseinstellungen machen das Wasserzeichen nur während des Druckens verfügbar. Führen Sie die folgenden Schritte aus, um die Registrierung zu aktualisieren und Wasserzeichen während des Druckens zu aktivieren:

1. Erstellen Sie ein Backup der Windows-Registrierung, bevor Sie Änderungen daran vornehmen. Ausführliche Anweisungen finden Sie unter [Wie ändere ich die Windows-Registrierung](https://learn.microsoft.com/de-de/troubleshoot/windows-server/performance/windows-registry-advanced-users).
1. Navigieren Sie im Registrierungs-Editor zu HKEY_CURRENT_USER\Software\Adobe\LiveCycle Rights Management ES4\11.0.0 oder HKEY_LOCAL_MACHINE\WOW6432NODE\Software\Adobe\LiveCycle Rights Management ES4\11.0.0
1. Erstellen Sie einen neuen Registrierungsschlüssel namens **WatermarkMode**.
1. Erstellen Sie im WatermarkMode-Registrierungsschlüssel ein DWORD **WatermarkMode** und legen Sie den Wert des DWORD **WatermarkMode** auf **1** fest.

1. Schließen Sie den Registrierungseditor.

>[!NOTE]
>
>In Windows Explorer können Sie das Dateimenü oder Kontextmenü verwenden, um ein Microsoft Excel-Dokument zu erstellen. Bei Dokumenten, die mit angegebenen Methoden erstellt wurden, kann das Druckdatum nicht abgerufen oder geändert werden. Dies ist eine Einschränkung von Microsoft Excel. AEM-Dokumentensicherheits-Wasserzeichen hängen von dem Druckdatum des Dokuments ab. Bei solchen Dokumenten wird das Wasserzeichen also auf ein vorheriges Datum zurückgesetzt. Außerdem werden Kopf- und Fußzeilen nicht beibehalten.

## Eine benutzerdefinierte Titelseite hinzufügen {#coverpage}

Eine Benutzerin oder ein Benutzer kann versuchen, das geschützte Dokument auf einem Computer zu öffnen, auf dem kein AEM Document Security for Microsoft Office-Plug-in installiert ist. Solche Computer können das Dokument nicht öffnen. Auf solchen Computern können Sie eine Titelseite anzeigen, die Anweisungen zum Verwenden von AEM Document Security for Microsoft Office-Plug-in und anderen Informationen enthalten.

### Vor der Konfiguration der Titelseite {#before-you-configure-a-cover-page}

* Erstellen Sie ein Backup der Datei „CommonResources.dll“. Der Standardpfad lautet:

   * **(Für 32-Bit-Office auf 32-Bit-Computern)** C:\Programme\Adobe\Adobe Experience Manager Forms\Document Security Extension

   * **(Für 32-Bit Office auf 64-Bit Computern)** C:\Program Files (x86)\Adobe\Adobe Experience Manager Forms\Document Security Extension

   * **(Für 64-Bit-Office auf 64-Bit-Computern)** C:\Programme\Adobe\Adobe Experience Manager Forms\Document Security Extension

* Stellen Sie sicher, dass Microsoft Visual Studio 2008 oder höher installiert ist. Sie können auch ein anderes Dienstprogramm zum Bearbeiten von DLL-Dateien verwenden.
* Entpacken Sie das templates.zip-Archiv. Das Archiv enthält Vorlagen für die Titelseite vom Typ .xlsx, .docx und .pptx. Verwenden Sie nur bereitgestellte Vorlagen für die Dateitypen .xlsx, .docx und .pptx. Sie können auch Ihre eigenen Vorlagen für andere Dateitypen erstellen. Passen Sie Vorlagen an, um benutzerdefinierte Nachrichten und Anweisungen einzubeziehen. Die Datei „template.zip“ finden Sie unter:

[Datei laden](assets/templates.zip)

### Struktur der Datei „CommonResources.dll“ {#structure-of-the-commonresources-dll-file}

Die Datei „CommonResources.dll“ enthält Informationen zu den Ressourcenvorlagen. Sie enthält zwei Namenskennungen: „TEMPLATE_FILE“ und „RT_MANIFEST“. Um eine benutzerdefinierte Titelseite zu aktivieren, wird die Namenskennung „TEMPLATE_FILE“ geändert. Die Namenskennung „TEMPLATE_FILE“ verfügt über sechs Ressourcen:

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
   >Wenn die Datei nicht im Fenster „Projektmappen-Explorer“ angezeigt wird, öffnen Sie die Datei erneut mit der Option „Öffnen mit“. Wählen Sie den Ressourcen-Editor als Editor aus.

1. Erweitern Sie im „Solution Explorer“-Fenster, das Verzeichnis „TEMPLATE_FILE“ und löschen Sie Ressourcen „101“.

1. Fügen Sie die Ressourcen hinzu:

   1. Wenn ein Projekt im Projektmappen-Explorer ausgewählt ist, klicken Sie im Menü „Projekt“ auf „Voreinstellungen“.
   1. Wählen Sie die Registerkarte „Ressourcen“.
   1. Auf der Resourcen-Designer-Symbolleiste fahren Sie mit der Maus über „Ressource hinzufügen“ und klicken Sie auf den Pfeil. Wählen Sie als Ressourcentyp „TEMPLATE_FILE“ und klicken Sie auf „Importieren“.
   1. Navigieren Sie im Dialogfeld **`Add existing file to resources`** zur Datei „Resource.xlsx“ und klicken Sie dann auf „Öffnen“. Die Datei wird dem Verzeichnis „TEMPLATE_FILE“ hinzugefügt.

   >[!NOTE]
   >
   >Stellen Sie sicher, dass die Spracheinstellungen korrekt sind. Löschen Sie die Ressource mit neutraler Sprache.

1. Wiederholen Sie die Schritte 2 und 3 für alle Ressourcentypen.

   >[!NOTE]
   >
   >Löschen Sie keine Ressourcentypen und fügen Sie sie in zufälliger Reihenfolge hinzu. Nach „101“, konfigurieren Sie „102“ usw.

### Verpacken Sie die benutzerdefinierte Datei „CommonResources.dll“ mit dem Installationsprogramm von AEM Document Security Extension for Microsoft Office {#package-custom-commonresources-dll-file-with-the-installer-of-aem-document-security-extension-for-microsoft-office}

Sie können die Datei „CommonResources.dll“ anpassen, um eine benutzerdefinierte Titelseite hinzuzufügen. Nach dem Anpassen der Datei können Sie die Originaldatei auf allen Computern manuell durch die benutzerdefinierte Datei ersetzen oder eine automatische Methode zum Ersetzen der Datei wählen.

In einer großen Umgebung ist es schwierig und mühsam, die Standarddatei `CommonResources.dll file` durch eine benutzerdefinierte Datei `CommonResources.dll` manuell zu ersetzen. Sie können ein Selbstextraktions- und Verpackungs-Tool (zum Beispiel WinZip Self-Extractor) verwenden, um die benutzerdefinierte Datei „CommonResources.dll“ zusammen mit dem AEM Document Security Extension-Installationsprogramm für Microsoft Office zu verpacken. Später können Sie das benutzerdefinierte Installationsprogramm an alle Computer verteilen. Diese Methode reduziert die Zeit, die benötigt wird, um die Standarddatei `CommonResources.dll` durch eine benutzerdefinierte Datei zu ersetzen. Außerdem wird sichergestellt, dass alle Computer die erforderliche CommonResources.dll-Datei haben. Das Tool zum Selbstextrahieren und Verpacken ist nur eine der vielen möglichen Methoden zum automatischen Ersetzen einer Datei. Sie können die Methode wählen, die für Sie und Ihre Umgebung geeignet ist.

Sie können die folgenden Schritte ausführen, um die benutzerdefinierte `CommonResources.dll`-Datei mit dem Installationsprogramm der AEM Document Security Extension for Microsoft Office zu verpacken:

1. Installieren Sie ein Selbstextraktions- und Verpackungs-Tool. Beispielsweise WinZip Self-Extractor.
1. Erstellen Sie einen neuen Ordner. Beispielsweise „IHR_ORDNER_NAME“
1. Platzieren Sie das ursprüngliche AEM Document Security Extension-Installationsprogramm und die benutzerdefinierte Datei „CommonResources.dll“ in den neu erstellten Ordner.
1. Erstellen Sie eine Batch-Datei im Ordner. Beispielsweise IHR_ORDNER_NAME\Installer.bat
1. Öffnen Sie die Batch-Datei zur Bearbeitung und fügen Sie ihr den folgenden Code hinzu:

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

   * (LiveCycle® Rights Management ES2 und Version 9.0): *HKLM\SOFTWARE\Adobe/LiveCycle* *Rights Management ES2\9.0 *
   * (LiveCycle® Rights Management ES3 und Version 10.0)
   * (LiveCycle® Rights Management ES4 und Version 11.0) HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0
   * (AEM 6.0 Forms on JEE und höher) HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0

1. Ersetzen Sie im obigen Code alle Instanzen von „IHR_ORDNER_NAME“ durch den Namen des Ordners, den Sie in Schritt 2 erstellt haben.
1. **(Nur für das AEM Document Security Extension for Microsoft Office-Installationsprogramm mit .exe-Erweiterung)** Ersetzen Sie die folgende Code-Zeile:

   `msiexec /i YOUR_FOLDER_NAME\MSI_NAME.msi`
durch

   `START /w YOUR_FOLDER_NAME\APPLICATION_NAME.exe`

1. Speichern und schließen Sie die Batch-Datei.
1. Verwenden Sie ein Selbstextraktions- und Verpackungs-Tool, um den Ordner zu packen, der Folgendes enthält:

   * die benutzerdefinierte Datei „CommonResources.dll“
   * das ursprüngliche AEM Document Security Extension for Microsoft Office-Installationsprogramm
   * die Batch-Datei

   >[!NOTE]
   >
   >Stellen Sie sicher, dass das selbstextrahierende Paket so eingestellt ist, dass es als Admin ausgeführt wird und
   >die Batch-Datei nach Abschluss der Extraktion automatisch ausgeführt wird.

Jetzt packt das selbstextrahierende AEM Document Security Extension for Microsoft Office-Installationsprogramm die benutzerdefinierte Datei „CommonResources.dll“ und steht zur Bereitstellung bereit.
