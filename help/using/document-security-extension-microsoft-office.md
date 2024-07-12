---
title: Einführung in die AEM Document Security-Erweiterung für Microsoft® Office
description: Mithilfe der Document Security-Erweiterung für Microsoft® Office können Sie vordefinierte Vertraulichkeitseinstellungen auf Ihre Microsoft® Office-Dateien anwenden.
uuid: a5428c50-fae3-4823-9e6f-0f5306e7248f
content-type: reference
topic-tags: using
discoiquuid: cf93f9f5-1fb6-4909-815e-0ffb8c6ea6d1
exl-id: 3e07c031-3f88-4bde-bdb3-b136ef5f9527
source-git-commit: 28137f26afc024d411857d44887bf69fe1ee2b81
workflow-type: tm+mt
source-wordcount: '1288'
ht-degree: 100%

---

# Einführung in die AEM Document Security Extension for Microsoft® Office{#introduction-to-aem-document-security-extension-for-microsoft-office}

Adobe® Experience Manager Document Security Extension for Microsoft® Office stellt sicher, dass nur von Ihnen autorisierte Benutzerinnen und Benutzer mit Word-, Excel- und PowerPoint-Dateien arbeiten dürfen, die Ihr geistiges Eigentum enthalten. Durch den Einsatz der Document Security Extension for Microsoft® Officekönnen Sie vordefinierte Vertraulichkeitseinstellungen auf Ihre Dateien anwenden.

Document Security Extension for Microsoft® Office erweitert das LiveCycle Rights Management- und Document Security-Add-on für Adobe Experience Manager Forms. Dadurch können Word-, Excel- und PowerPoint-Dateien geschützt werden, und autorisierte Benutzende, die diese Software installiert haben, können entsprechend den in der Richtlinie festgelegten Vertraulichkeitseinstellungen geschützte Dateien verwenden.

## Schutz von geistigem Eigentum mit Document Security {#how-document-security-protects-intellectual-property}

Document Security stellt sicher, dass nur die von Ihnen autorisierten Personen auf Dateien zugreifen können, die Ihr geistiges Eigentum enthalten. Mit Document Security können Sie Dateien mithilfe von Vertraulichkeitsrichtlinien schützen. Eine *Richtlinie* ist eine Zusammenstellung von Informationen, die unter anderem Vertraulichkeitseinstellungen und eine Liste der berechtigten Benutzenden umfasst. Die Einstellungen, die Sie in einer Richtlinie angeben, bestimmen, wie ein Empfänger eine Datei nutzen darf, auf die Sie die Richtlinie anwenden. Sie können beispielsweise angeben, ob Empfänger Text drucken oder kopieren oder Änderungen speichern können.

Document Security-Administratoren und -Benutzer erstellen Richtlinien. Administratoren erstellen Organisationsrichtlinien, die allen autorisierten Benutzern zur Verfügung stehen. Administratoren oder Richtliniensatzkoordinatoren können auch Gruppen von Richtlinien mit der Bezeichnung *Richtliniensätze* erstellen, die einer Untergruppe von Benutzern zur Verfügung stehen. Benutzer können eigene Richtlinien erstellen, die nur sie verwenden können. Administratoren, Richtliniensatzkoordinatoren und Benutzer erstellen Richtlinien auf den Document Security-Web-Seiten.

Die Richtlinien sind zwar in Document Security gespeichert, Sie wenden sie aber über Word, Excel oder PowerPoint auf Dateien an. Wenn Sie eine Richtlinie auf eine Datei anwenden, werden die in der Datei enthaltenen Informationen durch die in der Richtlinie angegebenen Vertraulichkeitseinstellungen geschützt. Wenn Sie die richtliniengeschützte Datei verteilen, können nur von der Richtlinie autorisierte Empfängerinnen und Empfänger auf den Dateiinhalt zugreifen.

Durch das Schützen einer Datei mit einer Richtlinie behalten Sie die Kontrolle über die Datei, auch nachdem sie verteilt wurde. Sie können Ereignisse überprüfen, um zu verfolgen, wann und wie Empfänger Ihre Datei verwenden, Änderungen an der Richtlinie vornehmen, Benutzer am weiteren Zugriff auf die Datei hindern und die mit der Datei verbundene Richtlinie ändern.

## Funktionsweise von Richtlinien {#how-policies-work}

Richtlinien enthalten Informationen zu den autorisierten Benutzern und den Vertraulichkeitseinstellungen, die für geistiges Eigentum gelten. Benutzer können alle Benutzer sein, die von Document Security durch Aufnahme in eine verknüpfte LDAP- oder Active Directory-Liste erkannt werden. Benutzer können auch Personen sein, die zur Registrierung bei Document Security eingeladen wurden oder für die der Administrator ein Konto erstellt hat.

Die Vertraulichkeitseinstellungen in einer Richtlinie bestimmen, wie die Empfänger Dateien verwenden können, die durch die Richtlinie geschützt sind. Richtlinien geben beispielsweise an, ob Empfänger Dateien drucken, Inhalte in andere Dateien kopieren oder Änderungen an geschützten Dateien speichern können. Richtlinien können auch unterschiedliche Vertraulichkeitseinstellungen für verschiedene Benutzer festlegen.

Wenn Sie eine Richtlinie auf eine Datei anwenden, werden die in der Datei enthaltenen Informationen durch die in der Richtlinie angegebenen Vertraulichkeitseinstellungen geschützt. Wenn Sie die Datei verteilen, authentifiziert Document Security die Empfänger, die versuchen, die Datei zu öffnen, und autorisiert den Zugriff entsprechend den in der Richtlinie festgelegten Berechtigungen.

Nachdem eine Richtlinie auf eine Datei angewendet wurde, können die Vertraulichkeitseinstellungen der Richtlinie jederzeit geändert werden. Auf diese Weise können Sie autorisierte Benutzende hinzufügen oder entfernen, oder die Berechtigungen für Benutzende ändern, nachdem diese die Datei erhalten haben. Die auf die Datei angewendete Richtlinie kann geändert werden, und der Zugriff auf die Datei kann gesperrt werden, damit sie nicht mehr von jedem geöffnet werden kann, der über eine Kopie der Datei verfügt.

Wenn die Richtlinie den Offline-Zugriff zulässt, können die Empfänger richtliniengeschützte Dateien auch offline (ohne aktive Internet- oder Netzwerkverbindung) für den in der Richtlinie angegebenen Zeitraum verwenden.

## Funktionsweise richtliniengeschützter Dateien {#how-policy-protected-files-work}

Damit eine Benutzerin bzw. ein Benutzer richtliniengeschützte Word-, Excel- und PowerPoint-Dateien öffnen und verwenden kann, muss die Richtlinie die Person als Empfängerin bzw. Empfänger einschließen oder anonymen Zugriff erlauben. Außerdem muss die Person Document Security Extension for Microsoft® Office installiert haben. Wenn Sie eine richtliniengeschützte Datei an eine Person weitergeben möchten, die nicht über Document Security Extension for Microsoft® Office verfügt, geben Sie ihr entweder eine Kopie der Software oder teilen Sie ihr mit, wie sie diese von Ihrer Website herunterladen kann. Wenn Sie das Installationsprogramm nicht haben, können Sie es von der [Download-Seite](https://experienceleague.adobe.com/docs/experience-manager-document-security/using/download-installer.html?lang=de) herunterladen.

Wenn eine Benutzerin oder ein Benutzer versucht, eine richtliniengeschützte Datei zu öffnen, stellt Document Security Extension for Microsoft® Office eine Verbindung zu Document Security her, um die Benutzerin bzw. den Benutzer zu authentifizieren. Wenn Document Security für die Prüfung der Dateinutzung konfiguriert ist, wird dem Benutzer eine Benachrichtigung angezeigt, dass die Dateinutzung geprüft wird. Document Security bestimmt, welche Dateiberechtigungen dem Benutzer gewährt werden sollen, und der Benutzer kann dann die Datei gemäß den Richtlinieneinstellungen unter diesen Bedingungen verwenden:

* Für die in der Richtlinie angegebene Gültigkeitsdauer.
* Bis ein Administrator oder die Person, die die Richtlinie angewendet hat, entweder den Zugriff auf die Datei widerruft oder die Richtlinie ändert.

  Wenn die Person, die die Richtlinie angewendet hat, die Richtlinie ändert oder den Zugriff auf die Datei widerruft, werden die Berechtigungen der Benutzerin bzw. des Benutzers für die Datei geändert oder entfernt, auch wenn diese Person die Datei bereits besitzt. Wenn die Datei selbst widerrufen wurde, kann der Benutzerin bzw. dem Benutzer eine URL zur Verfügung gestellt werden, um eine aktualisierte Kopie zu erhalten.

  Richtliniengeschützte Dateien können offline (ohne Internet- oder Netzwerkverbindung) geöffnet werden, wenn die Richtlinie den Offline-Zugriff zulässt, und zwar während der in der Richtlinie angegebenen Offline-Nutzungsdauer. Wenn die Offline-Nutzungsdauer endet, muss der Benutzer online gehen und mit Document Security synchronisieren, wodurch eine neue Nutzungsdauer beginnt.

  Wenn die Richtlinie das Speichern der Datei zulässt und ein Benutzer eine Kopie der richtliniengeschützten Datei speichert, wird die Richtlinie automatisch für die gespeicherte Datei angewendet und durchgesetzt. Ereignisse, wie z. B. Versuche, die neue Datei zu öffnen, werden ebenfalls geprüft und aufgezeichnet, genau wie bei der Originaldatei.

## Verwendung von Document Security zum Schutz Ihrer Dateien {#using-document-security-to-protect-your-files}

Sie können Richtlinien verwenden, um Ihre Dateien in verschiedenen Situationen zu schützen.

Beispiel: Ein Hersteller nimmt Angebote von Anbietern entgegen, die Teile für ein neues Produkt liefern sollen. Der Hersteller muss den Anbietern geschützte Informationen zur Verfügung stellen, die sie zur Fertigstellung ihrer Angebote benötigen. Der Hersteller verwendet Document Security zum Schutz der Dateien mit einer Richtlinie, die es den Bietern erlaubt, die Dateien zu öffnen und die Informationen anzuzeigen. Die Bieter werden jedoch daran gehindert, die Dateien zu ändern, zu drucken oder zu kopieren, und alle, die keine Berechtigung haben, werden daran gehindert, die Dateien zu öffnen.

Nachdem er eines der Angebote akzeptiert hat, aktualisiert der Hersteller die Richtlinie, um dem erfolgreichen Bieter die Berechtigung zum Drucken, Kopieren und lokalen Speichern von Änderungen zu erteilen und die nicht erfolgreichen Bieter zu entfernen, sodass sie keine Berechtigung mehr zum Öffnen der Dateien haben.

Während der Arbeit mit dem erfolgreichen Anbieter ändern die Ingenieurinnen und Ingenieure des Herstellers einige der Konstruktionsspezifikationen in den Dateien. Um die neuen Spezifikationen zu veröffentlichen, entzieht der Hersteller den Zugriff auf einige der Dateien und veröffentlicht neue Versionen. Wenn die Ingenieure des erfolgreichen Bieters versuchen, die Datei zu öffnen, sehen sie eine Meldung, dass der Zugriff auf die Datei widerrufen wurde. Die Meldung enthält eine URL, unter der sie eine neue Version der Datei herunterladen können.

## Zusätzliche Informationen {#additional-information}

Die Ressourcen in dieser Tabelle können Ihnen dabei helfen, mehr über AEM Document Security zu erfahren:

<table >
 <tbody>
  <tr>
   <th><p>Informationen</p> </th>
   <th><p>Siehe</p> </th>
  </tr>
  <tr>
   <td><p>Hilfe für AEM Forms-Admins</p> </td>
   <td><p><a href="https://experienceleague.adobe.com/docs/experience-manager-65/forms/administrator-help/get-started/configure-general-aem-forms-settings.html?lang=de">Admin-Hilfe</a> oder klicken Sie auf den Administrationsseiten von Document Security in der rechten oberen Ecke auf den Hilfe-Link.</p> </td>
  </tr>
  <tr>
   <td><p>Patch-Updates, technische Hinweise und zusätzliche Informationen zu dieser Produktversion</p> </td>
   <td><p><a href="https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=home&amp;lang=de#support">Technischer Support für Experience Cloud</a></p> </td>
  </tr>
 </tbody>
</table>
