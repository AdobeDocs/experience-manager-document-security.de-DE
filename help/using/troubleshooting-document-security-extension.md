---
title: Fehlerbehebung für AEM Document Security Extension for Microsoft Office
description: Wenn Sie Probleme bei der Installation, Konfiguration oder Verwendung von AEM Document Security Extension for Microsoft Office haben, folgen Sie den Anweisungen in diesem Dokument.
uuid: 61001ca8-a25a-4879-98ac-563a6eb126e7
contentOwner: khsingh
content-type: reference
topic-tags: using
discoiquuid: bdc3f174-e417-4d3e-b3af-972cdcc10133
exl-id: 98f24032-0774-47f8-bcc5-1ee37b417833
source-git-commit: 28137f26afc024d411857d44887bf69fe1ee2b81
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 100%

---

# Fehlerbehebung für AEM Document Security Extension for Microsoft Office{#troubleshooting-aem-document-security-extension-for-microsoft-office}

## Fehlerbehebung bei Installations- und Konfigurationsproblemen {#troubleshootinginstallationandconfiguration}

Wenn Sie Probleme bei der Installation und Konfiguration von AEM Document Security Extension for Microsoft Office haben, stellen Sie sicher, dass Sie die Anweisungen im Abschnitt „Vor der Installation“ des Artikels [Installation](installing-configuring-aemdsext.md) sorgfältig befolgt haben.

Wenn Sie alles gemäß der Dokumentation installiert und konfiguriert haben, finden Sie in den folgenden Abschnitten Probleme, die den aktuellen Problemen ggf. ähneln.

### Document Security Extension for Microsoft Office kann nicht geladen werden {#document-security-extension-fails-to-load-for-microsoft-office-applications}

Die LoadBehavior-Eigenschaft in der Windows-Registrierung gibt das Laufzeit-Verhalten des Document Security-Plug-in an. Wenn die LoadBehavior-Eigenschaft auf 3 festgelegt ist, werden alle Plug-ins automatisch geladen. Bevor Sie Document Security Extension for Microsoft Office installieren, stellen Sie sicher, dass die LoadBehavior-Eigenschaft auf 3 gesetzt ist.

1. Erstellen Sie ein Backup der Windows-Registrierung, bevor Sie Änderungen daran vornehmen. Ausführliche Anweisungen finden Sie unter [Wie ändere ich die Windows-Registrierung](https://support.microsoft.com/de-de/kb/136393).
1. Navigieren Sie im Registrierungs-Editor zu HKEY_CURRENT_USER\Software\Microsoft\Office\Word\Addins\Adobe.DRMIntegration.WordAddin oder HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Word\Addins\Adobe.DRM.
1. Legen Sie den Wert der Eigenschaft **LoadBehavior** auf 3 fest.

1. Schließen Sie den Registrierungseditor.

Ausführliche Informationen zu LoadBehavior finden Sie im Artikel [Registrierungseinträge für VSTO-Add-Ins](https://msdn.microsoft.com/de-de/library/bb386106.aspx#LoadBehavior).

## Fehlerbehebung zu Administrationsaufgaben {#admintasks}

In diesem Abschnitt werden mögliche Probleme mit Ihrer installierten AEM Document Security Extension behandelt.

### Microsoft Office-Programme starten nicht ordnungsgemäß beim Installieren von Document Security Extension {#microsoft-office-applications-dont-start-smoothly-on-installing-document-security-extension}

Wenn Sie außerdem einen reibungslosen Start von Office-Programmen auf Computern mit installierter Document Security Extension und aktiviertem McAfee VirusScan mit Überprüfung bei Zugriff sicherstellen möchten, deaktivieren Sie die Option „Pufferüberlaufschutz“ in der McAfee VirusScan-Konsole.
