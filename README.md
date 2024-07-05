# tintin_silberland

Tintin Einstellungen für das deutschsprachige MUD Silberland

## Welt anlegen

Bei einer frischen Installation der Skriptsammlung sollte eine neue 'Welt' für
den Login angelegt werden. Wobei Weltname und Charaktername meist übereinstimmen.

```    
addworld <Weltname> <Hostname> <Port> [Charaktername] [Passwort]
```

Charaktername und PAsswort sind optional und müssen nicht gesetzt werden.
Wenn sie jedoch gesetzt sind, werden sie bei einem Sessionstart automatisch ans
Mud übermittelt.

Beispiel:

```
addworld zonk mud.silberland.at 4711 zonk geheim
```

## Welt verbinden

Um sich mit einer Welt zu verbinden, also eine Session aufzubauen nutzt man das
Kommando `connect`.

```
connect [Weltname]
```

Sollte man nur connect eingeben werden die gespeicherten Weltdaten angezeigt.

```
connect

====={ WORLD LIST }=====                                
zonk                 mud.silberland.at   4711   zonk
```

## Welt löschen

Man kann die Weltdaten einzelner Welten auch wieder löschen.

```
deleteworld zonk
```

## Konfiguration nach Login

Mit dem Befehl `config` können nach dem Login weitere Einstellungen 
vorgenommen werden. Die Einstellungen werden dann in einer Art config-Wizard vorgenommen.

## Hilfeseiten zu Befehlen

Mit `help` kann man sich eine Übersicht über alle Hilfeseiten zu den einzelnen
Befehlen anzeigen lassen. Mit `help kategorie [Kategorie]` gibt es eine
Übersicht über die Hilfeseiten einer bestimmten Kategorie. Mit `help
<Befehl>` erhält man schließlich eine Hilfeseite zu einem bestimmten Befehl.

## Charakterskripte

Für kleine Zusatzskripte wird bei der Welterstellung eine Datei `<Weltname>.tin`
im `/chars` Ordner erstellt. Diese wird beim Login automatisch mitgeladen.