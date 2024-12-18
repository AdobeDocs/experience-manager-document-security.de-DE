---
title: Einführung in die AEM Document Security-Erweiterung für Microsoft® Office
description: Mithilfe von Document Security Extension for Microsoft&reg; Office können Sie vordefinierte Vertraulichkeitseinstellungen auf Ihre Microsoft&reg; Office-Dateien anwenden.
uuid: a5428c50-fae3-4823-9e6f-0f5306e7248f
content-type: reference
topic-tags: using
discoiquuid: cf93f9f5-1fb6-4909-815e-0ffb8c6ea6d1
exl-id: 3e07c031-3f88-4bde-bdb3-b136ef5f9527
source-git-commit: 3b6a686966fb8d006bed8cc4a4bf5eebe0dfb030
workflow-type: tm+mt
source-wordcount: '1248'
ht-degree: 100%

---

# Einführung in die AEM Document Security Extension for Microsoft® Office{#introduction-to-aem-document-security-extension-for-microsoft-office}

Adobe® Experience Manager Document Security Extension for Microsoft® Office stellt sicher, dass nur von Ihnen autorisierte Benutzerinnen und Benutzer mit Word-, Excel- und PowerPoint-Dateien arbeiten dürfen, die Ihr geistiges Eigentum enthalten. Durch den Einsatz der Document Security Extension for Microsoft® Officekönnen Sie vordefinierte Vertraulichkeitseinstellungen auf Ihre Dateien anwenden.

Document Security Extension for Microsoft® Office verbessert LiveCycle Rights Management und Document Security für Adobe Experience Manager Forms. Diese Erweiterung schützt Office-Dateien und ermöglicht autorisierten Benutzenden, auf richtliniengeschützte Dateien gemäß den festgelegten Vertraulichkeitseinstellungen zuzugreifen.

## Schutz von geistigem Eigentum mit Document Security {#how-document-security-protects-intellectual-property}

Document Security stellt sicher, dass nur die von Ihnen autorisierten Personen auf Dateien zugreifen können, die Ihr geistiges Eigentum enthalten. Mit Document Security können Sie Dateien mithilfe von Vertraulichkeitsrichtlinien schützen. Eine *Richtlinie* ist eine Zusammenstellung von Informationen, die unter anderem Vertraulichkeitseinstellungen und eine Liste der berechtigten Benutzenden umfasst. Die Einstellungen, die Sie in einer Richtlinie angeben, bestimmen, wie ein Empfänger eine Datei nutzen darf, auf die Sie die Richtlinie anwenden. Sie können beispielsweise angeben, ob Empfänger Text drucken oder kopieren oder Änderungen speichern können.

Document Security-Administratoren und -Benutzer erstellen Richtlinien. Administratoren erstellen Organisationsrichtlinien, die allen autorisierten Benutzern zur Verfügung stehen. Administratoren oder Richtliniensatzkoordinatoren können auch Gruppen von Richtlinien mit der Bezeichnung *Richtliniensätze* erstellen, die einer Untergruppe von Benutzern zur Verfügung stehen. Benutzer können eigene Richtlinien erstellen, die nur sie verwenden können. Admins, Richtliniensatzkoordinierende und Benutzende erstellen Richtlinien mithilfe der Document Security-Web-Seiten.

Die Richtlinien sind zwar in Document Security gespeichert, Sie können sie aber über Word, Excel oder PowerPoint auf Dateien anwenden. Wenn Sie eine Richtlinie auf eine Datei anwenden, werden die in der Datei enthaltenen Informationen durch die in der Richtlinie angegebenen Vertraulichkeitseinstellungen geschützt. Wenn Sie die richtliniengeschützte Datei verteilen, können nur autorisierte Empfängerinnen und Empfänger auf deren Inhalt zugreifen.

Durch das Schützen einer Datei mit einer Richtlinie behalten Sie die Kontrolle über die Datei, auch nachdem sie verteilt wurde. Sie können Ereignisse prüfen, um zu verfolgen, wann und wie Empfängerinnen und Empfänger Ihre Datei verwenden. Sie können auch Änderungen an der Richtlinie vornehmen, Benutzende daran hindern, weiterhin auf die Datei zuzugreifen, und die der Datei beigefügte Richtlinie ändern.

## Funktionsweise von Richtlinien {#how-policies-work}

Richtlinien enthalten Informationen zu den autorisierten Benutzenden und den Vertraulichkeitseinstellungen, die für geistiges Eigentum gelten. Document Security erkennt Benutzende, die in einer verknüpften LDAP- oder Active Directory-Liste enthalten sind. Benutzer können auch Personen sein, die zur Registrierung bei Document Security eingeladen wurden oder für die der Administrator ein Konto erstellt hat.

Die Vertraulichkeitseinstellungen in einer Richtlinie bestimmen, wie die Empfänger Dateien verwenden können, die durch die Richtlinie geschützt sind. Richtlinien geben beispielsweise an, ob Empfänger Dateien drucken, Inhalte in andere Dateien kopieren oder Änderungen an geschützten Dateien speichern können. Richtlinien können auch unterschiedliche Vertraulichkeitseinstellungen für verschiedene Benutzer festlegen.

Wenn Sie eine Richtlinie auf eine Datei anwenden, werden die in der Datei enthaltenen Informationen durch die in der Richtlinie angegebenen Vertraulichkeitseinstellungen geschützt. Wenn Sie die Datei verteilen, authentifiziert Document Security die Empfänger, die versuchen, die Datei zu öffnen, und autorisiert den Zugriff entsprechend den in der Richtlinie festgelegten Berechtigungen.

Nachdem eine Richtlinie auf eine Datei angewendet wurde, können die Vertraulichkeitseinstellungen der Richtlinie jederzeit geändert werden. Sie können autorisierte Benutzende hinzufügen oder entfernen oder die Berechtigungen für Benutzende ändern, nachdem diese die Datei erhalten haben. Die auf die Datei angewendete Richtlinie kann geändert werden. Außerdem kann der Zugriff auf die Datei widerrufen werden, sodass sie von keiner Person mit einer Kopie der Datei mehr geöffnet werden kann.

Wenn die Richtlinie den Offline-Zugriff zulässt, können die Empfänger richtliniengeschützte Dateien auch offline (ohne aktive Internet- oder Netzwerkverbindung) für den in der Richtlinie angegebenen Zeitraum verwenden.

## Funktionsweise richtliniengeschützter Dateien {#how-policy-protected-files-work}

Damit eine Benutzerin oder ein Benutzer richtliniengeschützte Word-, Excel- und PowerPoint-Dateien öffnen und verwenden kann, muss die Richtlinie die Benutzerin oder den Benutzer als empfangende Person enthalten. Oder sie muss anonymen Zugriff zulassen. Außerdem muss Document Security Extension for Microsoft® Office installiert sein. Um eine richtliniengeschützte Datei einer Person zur Verfügung zu stellen, die nicht über Document Security Extension for Microsoft® Office verfügt, können Sie dieser eine Kopie der Software geben. Oder Sie können ihr mitteilen, wie ein Download über Ihre Website möglich ist. Wenn Sie das Installationsprogramm nicht haben, können Sie es von der [Download-Seite](https://experienceleague.adobe.com/de/docs/experience-manager-document-security/using/download-installer) herunterladen.

Wenn jemand versucht, eine richtliniengeschützte Datei zu öffnen, stellt Document Security Extension for Microsoft® Office eine Verbindung zu Document Security her, um die Person zu authentifizieren. Wenn Document Security für die Prüfung der Dateinutzung konfiguriert ist, wird dem Benutzer eine Benachrichtigung angezeigt, dass die Dateinutzung geprüft wird. Document Security bestimmt, welche Dateiberechtigungen dem Benutzer gewährt werden sollen, und der Benutzer kann dann die Datei gemäß den Richtlinieneinstellungen unter diesen Bedingungen verwenden:

* Für die in der Richtlinie angegebene Gültigkeitsdauer.
* Bis ein Administrator oder die Person, die die Richtlinie angewendet hat, entweder den Zugriff auf die Datei widerruft oder die Richtlinie ändert.

  Wenn die Person, die die Richtlinie angewendet hat, die Richtlinie ändert oder den Zugriff auf die Datei widerruft, werden die Berechtigungen der Benutzerin bzw. des Benutzers für die Datei geändert oder entfernt, auch wenn diese Person die Datei bereits besitzt. Wenn die Datei selbst widerrufen wurde, kann der Benutzerin bzw. dem Benutzer eine URL zur Verfügung gestellt werden, um eine aktualisierte Kopie zu erhalten.

  Wenn die Richtlinie Offline-Zugriff zulässt, können Benutzende richtliniengeschützte Dateien während der festgelegten Offline-Nutzungsdauer ohne Internet- oder Netzwerkverbindung öffnen. Wenn die Offline-Nutzungsdauer endet, muss die Person online gehen und mit Document Security synchronisieren, wodurch eine neue Nutzungsdauer beginnt.

  Wenn die Richtlinie Offline-Zugriff zulässt, können Benutzende richtliniengeschützte Dateien während der festgelegten Offline-Nutzungsdauer ohne Internet- oder Netzwerkverbindung öffnen. Ereignisse, wie z. B. Versuche, die neue Datei zu öffnen, werden ebenfalls geprüft und aufgezeichnet, genau wie bei der Originaldatei.

## Verwendung von Document Security zum Schutz Ihrer Dateien {#using-document-security-to-protect-your-files}

Sie können Richtlinien verwenden, um Ihre Dateien in verschiedenen Situationen zu schützen.

Beispiel: Ein Hersteller nimmt Angebote von Anbietern entgegen, die Teile für ein neues Produkt liefern sollen. Der Hersteller muss den Anbietern geschützte Informationen zur Verfügung stellen, die sie zur Fertigstellung ihrer Angebote benötigen. Der Hersteller verwendet Document Security zum Schutz der Dateien mit einer Richtlinie, die es den Bietern erlaubt, die Dateien zu öffnen und die Informationen anzuzeigen. Die Bieter werden jedoch daran gehindert, die Dateien zu ändern, zu drucken oder zu kopieren, und alle, die keine Berechtigung haben, werden daran gehindert, die Dateien zu öffnen.

Nach Annahme eines Gebots aktualisiert der Hersteller die Richtlinie, um der oder dem erfolgreichen Bietenden Berechtigungen zum lokalen Drucken, Kopieren und Speichern von Änderungen zu erteilen. Der Hersteller entfernt auch die nicht erfolgreichen Bietenden und widerruft ihre Berechtigung zum Öffnen der Dateien.

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
   <td><p><a href="https://experienceleague.adobe.com/de/docs/experience-manager-65/content/forms/administrator-help/get-started/configure-general-aem-forms-settings">Admin-Hilfe</a> oder klicken Sie auf den Administrationsseiten von Document Security in der rechten oberen Ecke auf den Hilfe-Link.</p> </td>
  </tr>
  <tr>
   <td><p>Patch-Updates, technische Hinweise und zusätzliche Informationen zu dieser Produktversion</p> </td>
   <td><p><a href="https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=home&amp;lang=de#support">Technischer Support für Experience Cloud</a></p> </td>
  </tr>
 </tbody>
</table>
