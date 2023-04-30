# tintin_silberland

Tintin Einstellungen für das österreichische MUD Silberland

## Welt anlegen

Bei einer frischen Installation der Skriptsammlung sollte eine neue 'Welt' für
den Login angelegt werden. Wobei Weltname und Charaktername meist übereinstimmen.

    addworld <Weltname> <Hostname> <Port> [Charaktername] [Passwort]

Charaktername und PAsswort sind optional und müssen nicht gesetzt werden.
Wenn sie jedoch gesetzt sind, werden sie bei einem Sessionstart automatisch ans
Mud übermittelt.

Beispiel:

    addworld zonk mud.silberland.at 4711 zonk geheim

## Welt verbinden

Um sich mit einer Welt zu verbinden, also eine Session aufzubauen nutzt man das
Kommando **connect**.

    connect [Weltname]

Sollte man nur connect eingeben werden die gespeicherten Weltdaten angezeigt.

    connect

    ====={ WORLD LIST }=====                                
    zonk                 mud.silberland.at   4711   zonk

## Welt löschen

Man kann die Weltdaten einzelner Welten auch wieder löschen.

    deleteworld zonk

## Konfiguration nach Login

Mit dem Befehl **config** können nach dem Login weitere Einstellungen vorgenommen
werden. So sollte zum Beispiel die derzeitige Gilde gesetzt werden.  
Zum Beispiel:

    config gilde paladine

Die Anzeige der Kampfmeldungen kann auf zwei Modi gestellt werden.  
Im ersten Modus sind die Kampfmeldungen lediglich farblich hervorgehoben.  
Der zweite Modus verändert die Meldungen so, dass weniger Scroll entsteht und
die Meldungen immer möglichst in eine Zeile zusammengefasst werden.

    config kampf 2

Dies ist allerdings noch in Arbeit und wird wohl demnächst durch einen
config-wizard ersetzt werden.

## Charakterskripte

Für kleine Zusatzskripte wird bei der Welterstellung eine Datei **\<Weltname>.tin**
im **/chars** Ordner erstellt. Diese wird beim Login automatisch mitgeladen.