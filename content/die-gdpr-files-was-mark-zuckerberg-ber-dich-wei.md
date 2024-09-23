---
tags:
  - publish
title: 
slug: 
path: 
Related:
  - "[The GDPR Files - What Mark Zuckerberg knows about you](articles/the-gdpr-files-what-mark-zuckerberg-knows-about-you)"
---
Die Allgemeine Datenschutzverordnung der Europäischen Union ("GDPR") ist die umfassendste Datenschutzverordnung der Welt. Wenn du hier bist, weißt du wahrscheinlich schon, dass du eine Kopie aller Daten anfordern kannst, die ein Unternehmen über dich besitzt. Aber hast du es schon einmal selbst versucht? Falls ja, findest du hier einige überraschende Dinge, auf die du stoßen könntest.

Dieser Artikel ist in drei Abschnitte unterteilt, die sich jeweils mit einem der drei Ebenen der Datensammlung befassen. Je weiter wir dieses 'Dateneisberg' hinabsteigen, desto undurchsichtiger werden die Mittel der Datensammlung und die Zwecke, für die die resultierenden Informationen verwendet werden.

![dataiceberg.png](/assets/dataiceberg-bd15aa0a6b9c62e2be4768f159fec7d6.png)

Die Spitze des Eisbergs: Facebook und Google wissen alles, was du ihnen explizit über dich selbst erzählst. Dies umfasst in der Regel mindestens deinen Namen, deine E-Mail-Adresse und dein Geburtsdatum. Einige Nutzer:innen entscheiden sich jedoch möglicherweise dafür, eine ganze Reihe zusätzlicher Informationen freiwillig bereitzustellen, die weit über das hinausgehen, was von den Online-Plattformen benötigt wird, um ihre Dienste bereitzustellen: Adressen, Berufliche Details oder sogar Beziehungsstatus sind alle ziemlich üblich auf Plattformen wie LinkedIn oder Facebook.

Diese Art von Informationen ist normalerweise auf deinem Profil verfügbar oder du kannst sie in den Seiteneinstellungen anzeigen und bearbeiten. Während sensiblere Details wie dein Geburtsdatum oder deine Adresse oft standardmäßig privat bleiben, könnten viele der bereitgestellten Informationen öffentlich für jeden sichtbar sein, je nach deinen Datenschutzeinstellungen.

# Ebene 2: Gesammelte Daten

Es sollte nicht überraschen, dass Internetplattformen die Daten, die du ihnen freiwillig übermittelst, speichern und nutzen. Die Dinge werden jedoch viel undurchsichtiger, wenn es um die Daten geht, die sie über dich aus deinen Aktivitäten und der Nutzung von Apps sammeln. Alles, was du suchst, anklickst oder ansiehst, wird gespeichert. Die meisten Navigationsdienste speichern auch deinen gesamten Standortverlauf. Mein Mitgründer Jakob hat kürzlich seine Google Maps-Daten angesehen und festgestellt, dass der Dienst etwa 38,8 Millionen Zeilen GPS-Daten aufgezeichnet hatte. Wenn man das ausdrucken würde, würde es mehr als 1.000 Bücher so dick wie die Bibel ergeben.

Aber das ist noch nicht alles: Wusstest du, dass viele Dienste alles verfolgen, was du auf ihrer Website machst, auch wenn du auf nichts klickst? Die resultierenden Daten werden oft verwendet, um die Benutzerfreundlichkeit einer Website zu optimieren oder herauszufinden, welche Art von Inhalten du dir am längsten ansiehst. So sieht es aus, wenn wir Sitzungswiederholungen in unserem Website-Analysetool (PostHog) aktivieren. Du siehst Jakob, wie er versucht, sich zum zweiten Mal für unseren Newsletter anzumelden, weil der einfach so verdammt gut ist. 

![posthog_recordings.gif](/assets/posthog-recordings-ca83333520590cf15d6670a547d1b3fb.gif)

Einige Analysetools speichern auch die Informationen, die du in ein Textfeld eingibst, selbst wenn du keinen Knopf drückst, um sie zu senden. Sei also vorsichtig, wenn du Passwörter oder sensiblen Informationen in Felder eingibst, die nicht explizit als Passwortfelder gekennzeichnet sind oder auf einer Website, der du nicht vertraust.

> Hinweis: Datapods hat kein Interesse an deinen persönlichen Informationen. Wir versuchen, so wenig Daten wie möglich über dich zu speichern. Die Datapods-App verwendet hochmoderne Verschlüsselung und dezentrales Schlüsselmanagement, um unbefugten Zugriff auf deine Daten zu verhindern, einschließlich durch Datapods selbst. Auf diese Weise behältst du immer die volle Kontrolle darüber, wer was weiß.

Unternehmen verwenden diese Art von Informationen, um ihre Dienste zu verbessern, herauszufinden, was du magst, und personalisierte Werbung zu schalten. Für Benutzer ist es jedoch normalerweise nicht so einfach, darauf zuzugreifen. Während du oft eine Zusammenfassung bestimmter gesammelter Informationen wie Reaktionen, Kommentare oder deinen Suchverlauf anzeigen kannst, bleiben andere Informationen verborgen. Hier kommen die EU und die Datenschutz-Grundverordnung (DSGVO) ins Spiel. Die DSGVO ermöglicht es dir, eine Kopie deiner Daten anzufordern. Das heißt, jede Information, die auf dich zurückgeführt werden kann. Dies umfasst die meisten Arten von gesammelten Daten.

Der Prozess der Anforderung dieser Informationen kann etwas aufwändiger sein und mehrere Tage dauern (nach der DSGVO müssen Unternehmen innerhalb von 30 Tagen reagieren). Die resultierenden Daten müssen in einem "maschinenlesbaren Format" bereitgestellt werden, wie z. B. einer JSON-Datei. Obwohl das wahrscheinlich eine echt fesselnde Lektüre wäre, wenn dein Name C-3PO ist, ist das Vergnügen bei menschlichen Lesern oft begrenzt. Das bedeutet nicht, dass du Einsen und Nullen sehen wirst, aber wenn du durch 38,8 Millionen Zeilen roher GPS-Koordinaten blätterst, könnte das genauso gut der Fall sein.

Nehmen wir jedoch an, du hast bereits eine Kopie deiner Daten bei einem Dienst wie Facebook oder Google angefordert. Hier sind einige der Dinge, die noch interessant sein könnten: Facebook speichert z. B. deinen letzten Standort (`last_known_location.json`), die über die App getätigten Käufe (`payment_history.html`) und die Anzeigen, die du dir angesehen hast.

Hast du dich jemals gefragt, warum du manchmal auf Facebook Anzeigen für Artikel siehst, die du auf einer völlig anderen Website angesehen hast? Unter `advertisers_using_your_information.html` listet Facebook alle Unternehmen auf, die deine persönlichen Informationen verwenden, um dir gezielte Anzeigen zu zeigen. Diese Unternehmen haben bereits Informationen über dich in sogenannten "Audience-Listen", die sie selbst gesammelt oder gekauft haben, zum Beispiel ob du einen Artikel auf ihrer Website angesehen hast. Facebook kombiniert dann diese Informationen mit seinen eigenen Daten, um die Anzeigen noch hyperpersonalisierter zu machen. Bei mir ist diese Liste etwa 120 Unternehmen lang und umfasst verschiedene Datenbroker.

Aber es geht noch weiter: Ich habe kürzlich eine Kopie meiner Daten von Payback angefordert, dem von Master Card betriebenen Einzelhandelsbonusprogramm. Erhalten habe ich den gesamten Datensatz meiner Einkäufe im Geschäft, die ich mit meiner Bonuskarte getätigt habe, sowie eine detaillierte Historie, wann ich mich in der Nähe eines Partnergeschäftes befunden habe. 

Oder versuchst du dich zu erinnern, welchen Song du am 9. Mai 2022 um 6:28 Uhr gehört hast? Keine Sorge, Spotify hat eine komplette Streaming-Historie für dich.

```json
{
	"endTime" : "2022-05-09 06:28",
	"artistName" : "alt-J",
	"trackName" : "Breezeblocks",
	"msPlayed" : 1340
},
{
	"endTime" : "2022-05-09 06:28",
	"artistName" : "Monolink",
	"trackName" : "Return to Oz - ARTBAT Remix",
	"msPlayed" : 260493
},
```

