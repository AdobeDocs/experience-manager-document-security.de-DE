---
title: Fehlerbehebung für AEM Document Security Extension for Microsoft Office
description: Wenn Sie Probleme bei der Installation, Konfiguration oder Verwendung von AEM Document Security Extension for Microsoft Office haben, folgen Sie den Anweisungen in diesem Dokument.
uuid: 61001ca8-a25a-4879-98ac-563a6eb126e7
contentOwner: khsingh
content-type: reference
topic-tags: using
discoiquuid: bdc3f174-e417-4d3e-b3af-972cdcc10133
exl-id: 98f24032-0774-47f8-bcc5-1ee37b417833
source-git-commit: 3b6a686966fb8d006bed8cc4a4bf5eebe0dfb030
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 49%

---

# Fehlerbehebung für AEM Document Security Extension for Microsoft Office{#troubleshooting-aem-document-security-extension-for-microsoft-office}

## Fehlerbehebung bei Installations- und Konfigurationsproblemen {#troubleshootinginstallationandconfiguration}

Wenn Sie Probleme beim Installieren und Konfigurieren der AEM Document Security Extension for Microsoft Office haben, folgen Sie den Anweisungen im Abschnitt &quot;- vor der Installation -&quot;des Artikels &quot;[Installation](installing-configuring-aemdsext.md)&quot;.

Wenn Sie alles gemäß der Dokumentation installiert und konfiguriert haben, lesen Sie die folgenden Abschnitte, um Probleme ähnlich den aktuellen Problemen zu finden.

### Document Security Extension for Microsoft Office kann nicht geladen werden {#document-security-extension-fails-to-load-for-microsoft-office-applications}

Die Eigenschaft &quot;LoadBehavior&quot;in Windows Registry gibt das Laufzeitverhalten des Document Security-Plug-ins an. Wenn die LoadBehavior-Eigenschaft auf 3 festgelegt ist, werden alle Plug-ins automatisch geladen. Stellen Sie vor der Installation der Document Security Extension for Microsoft Office sicher, dass die Eigenschaft &quot;LoadBehavior&quot;auf 3 gesetzt ist.

1. Erstellen Sie eine Sicherungskopie der Windows-Registrierung, bevor Sie Änderungen daran vornehmen. Ausführliche Anweisungen finden Sie unter [Wie ändere ich die Windows-Registrierung](https://learn.microsoft.com/en-us/troubleshoot/windows-server/performance/windows-registry-advanced-users).
1. Navigieren Sie im Registrierungs-Editor zu HKEY_CURRENT_USER\Software\Microsoft\Office\Word\Addins\Adobe.DRMIntegration.WordAddin oder HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Word\Addins\Adobe.DRM.
1. Legen Sie den Wert der Eigenschaft **LoadBehavior** auf 3 fest.

1. Schließen Sie den Registrierungseditor.

Ausführliche Informationen zu LoadBehavior finden Sie im Artikel [Registrierungseinträge für VSTO-Add-Ins](https://learn.microsoft.com/en-us/visualstudio/vsto/registry-entries-for-vsto-add-ins?view=vs-2022&amp;redirectedfrom=MSDN#LoadBehavior).

## Fehlerbehebung zu Administrationsaufgaben {#admintasks}

In diesem Abschnitt werden mögliche Probleme mit Ihrer installierten AEM Document Security Extension behandelt.

### Microsoft Office-Programme starten nicht ordnungsgemäß beim Installieren von Document Security Extension {#microsoft-office-applications-dont-start-smoothly-on-installing-document-security-extension}

Um sicherzustellen, dass Office-Anwendungen reibungslos mit installierter Document Security Extension und aktiviertem McAfee VirusScan mit On-Access Scan beginnen, deaktivieren Sie den Pufferüberlaufschutz in der McAfee VirusScan-Konsole.
