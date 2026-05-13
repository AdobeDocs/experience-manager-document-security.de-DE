---
title: Fehlerbehebung für AEM Document Security Extension for Microsoft Office
description: Wenn Sie Probleme bei der Installation, Konfiguration oder Verwendung von AEM Document Security Extension for Microsoft Office haben, folgen Sie den Anweisungen in diesem Dokument.
uuid: 61001ca8-a25a-4879-98ac-563a6eb126e7
contentOwner: khsingh
content-type: reference
topic-tags: using
discoiquuid: bdc3f174-e417-4d3e-b3af-972cdcc10133
exl-id: 98f24032-0774-47f8-bcc5-1ee37b417833
TQID: https://experienceleague.adobe.com/3YVMcSeYDXCWkVeG8HmlJOgja9OwLqs1gpPWP8rhhs0
product_v2:
  - id: e8f6de9b-cf88-4405-8d10-15efa08c230e
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: fd5d26fd-7180-407d-bbd8-5f8a17f9c0b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: b2df949228acdc23ca7f2c55b72e62c1dba130b8
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 100%

---

# Fehlerbehebung für AEM Document Security Extension for Microsoft Office{#troubleshooting-aem-document-security-extension-for-microsoft-office}

## Fehlerbehebung bei Installations- und Konfigurationsproblemen {#troubleshootinginstallationandconfiguration}

Wenn Sie Probleme bei der Installation und Konfiguration von AEM Document Security Extension for Microsoft Office haben, stellen Sie sicher, dass Sie die Anweisungen im Abschnitt „Vor der Installation“ des Artikels [Installation](installing-configuring-aemdsext.md) sorgfältig befolgt haben.

Wenn Sie alles gemäß der Dokumentation installiert und konfiguriert haben, finden Sie in den folgenden Abschnitten Beschreibungen zu Problemen, die Ihrer Situation ggf. ähneln.

### Document Security Extension kann für Microsoft Office-Anwendungen nicht geladen werden {#document-security-extension-fails-to-load-for-microsoft-office-applications}

Die LoadBehavior-Eigenschaft in der Windows-Registrierung gibt das Laufzeitverhalten des Document Security-Plug-ins an. Wenn die LoadBehavior-Eigenschaft auf 3 festgelegt ist, werden alle Plug-ins automatisch geladen. Bevor Sie Document Security Extension für Microsoft Office installieren, stellen Sie sicher, dass die LoadBehavior-Eigenschaft auf den Wert „3“ gesetzt ist.

1. Erstellen Sie ein Backup der Windows-Registrierung, bevor Sie Änderungen daran vornehmen. Ausführliche Anweisungen finden Sie unter [Wie ändere ich die Windows-Registrierung](https://learn.microsoft.com/de-de/troubleshoot/windows-server/performance/windows-registry-advanced-users).
1. Navigieren Sie im Registrierungs-Editor zu HKEY_CURRENT_USER\Software\Microsoft\Office\Word\Addins\Adobe.DRMIntegration.WordAddin oder HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Word\Addins\Adobe.DRM.
1. Legen Sie den Wert der **LoadBehavior**-Eigenschaft auf „3“ fest.

1. Schließen Sie den Registrierungseditor.

Ausführliche Informationen zu LoadBehavior finden Sie im Artikel [Registrierungseinträge für VSTO-Add-Ins](https://learn.microsoft.com/de-de/visualstudio/vsto/registry-entries-for-vsto-add-ins?view=vs-2022&redirectedfrom=MSDN#LoadBehavior).

## Fehlerbehebung zu Administrationsaufgaben {#admintasks}

In diesem Abschnitt werden mögliche Probleme mit Ihrer installierten AEM Document Security Extension behandelt.

### Microsoft Office-Programme starten nicht ordnungsgemäß beim Installieren von Document Security Extension {#microsoft-office-applications-dont-start-smoothly-on-installing-document-security-extension}

Wenn Sie einen reibungslosen Start von Office-Anwendungen auf Computern mit Document Security Extension-Installation und aktivierter McAfee VirusScan On-Access-Scan-Funktion sicherstellen möchten, deaktivieren Sie in der McAfee VirusScan-Konsole die Option für den Pufferüberlaufschutz.
