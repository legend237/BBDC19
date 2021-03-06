# BBDC19
Bremen Big Data Challenge

## :pencil: Aufgabe Bechreibung:

In der Bremen Big Data Challenge 2019 geht es darum, verschiedene alltägliche und sportliche Bewegungen zu klassifizieren. Dafür stehen Sensordaten, die an einem Bein oberhalb und unterhalb des Knies aufgenommen wurden, zur Verfügung. Der Trainingsdatensatz enthält die Daten von 15 Proband*innen, vier weitere werden zum Auswerten eurer Lösungen verwendet.

In den Daten gibt es folgende 22 Bewegungen:

 * Rennen ('run').
 * Gehen ('walk').
 * Stehen ('stand').
 * Sitzen ('sit').
 * Aufstehen sowie Hinsetzen ('sit-to-stand',  'stand-to-sit').
 * Treppe herauf- sowie heruntersteigen ('stair-up', 'stair-down').
 * Springen auf einem oder beiden Beinen ('jump-one-leg', 'jump-two-leg').
 * Links- oder Rechtskurve laufen ('curve-left-step',  'curve-right-step').
 * Auf der Stelle links oder rechts drehen, linker oder rechter Fuß zuerst ('curve-left-spin-Lfirst', 'curve-left-spin-Rfirst', 'curve-right-spin-Lfirst', 'curve-right-spin-Rfirst').
 * Seitwärtsschritte nach links oder rechts ('lateral-shuffle-left', 'lateral-shuffle-right').
 * Richtungswechsel beim Laufen nach rechts oder links, linker oder rechter Fuß zuerst ('v-cut-left-Lfirst', 'v-cut-left-Rfirst', 'v-cut-right-Lfirst', 'v-cut-right-Rfirst')

Darüber hinaus sind andere, möglicherweise falsch gelabelte Bewegungen in den Daten vorhanden. Für die Aufgabe der BBDC 2019 sind nur die 22 gelisteten Bewegungen relevant.

Alle Daten liegen als CSV-Dateien (comma separated values) vor. Die ersten drei Zeilen der Trainingsdaten (train.csv) sehen wie folgt aus:

 Subject,Datafile,Label
 Subject02,Subject02/Subject02_Aufnahme000.csv,curve-left-step
 Subject02,Subject02/Subject02_Aufnahme001.csv,curve-left-step
 Subject02,Subject02/Subject02_Aufnahme002.csv,stand-to-sit

Jede Zeile entspricht einer Aufnahme einer Bewegung. Die Spalten haben die folgenden Bedeutungen:
 
 * Subject: Die ID des Probanden
 * Datafile: Pfad der Datei mit den Sensordaten für diese Aufnahme. Für jeden Probanden gibt es einen Ordner, in dem in einzelnen Dateien die Sensordaten für einzelne Bewegungsaufnahmen liegen.
 * Label: Die Bewegung, die aufgenommen wurde

Die Testdaten (challenge.csv) haben folgendes Format:

 Subject,Datafile,Label
 Subject01,Subject01/Subject01_Aufnahme000.csv,X
 Subject01,Subject01/Subject01_Aufnahme001.csv,X
 Subject01,Subject01/Subject01_Aufnahme002.csv,X

Dabei haben die Spalten dieselbe Bedeutung wie in train.csv. Die Spalte "Label" enthält konstant den Buchstaben X, um anzuzeigen, dass dieser Wert nicht vorliegt. Wenn ihr Lösungen einreicht, dann soll eure Abgabe genau den Testdaten entsprechen, wobei jedes X durch ein Label ersetzt wurde. Dieses Label entspricht eurem Klassifikationsergebnis für diese Bewegung. Dabei ist es wichtig, dass die Schreibweise (inkl. Groß-/Kleinschreibung) der textuellen Labels mit der Schreibweise der Labels in den Trainingsdaten exakt übereinstimmt.

Die Datendateien sehen z.B. wie folgt aus (Beispiel: Subject02_Aufnahme000.csv)

 32688,32224,32991,32609,32790,33048,37168,34610,27374,29068,29264,28408,31784,28133,29295,29244,33216,37140,34736
 32744,32571,32935,32279,32863,33048,37168,34610,27374,29068,29264,28408,31784,28133,29295,29244,33216,37140,34736
 32788,32934,32767,32624,32899,33048,37168,34610,27374,29068,29264,28408,31784,28133,29295,29244,33216,37140,34736
 
Dabei steht jede Zeile für die zu einem Zeitpunkt gemessenen Sensorwerte (Abgetastet mit 1000Hz). Die Spalten stehen für die einzelnen Sensoren:

 0. EMG1
 1. EMG2
 2. EMG3
 3. EMG4
 4. Airborne
 5. ACC upper X
 6. ACC upper Y
 7. ACC upper Z
 8. Goniometer X
 9. ACC lower X
 10. ACC lower Y
 11. ACC loewr Z
 12. Goniometer Y
 13. Gyro upper X
 14. Gyro upper Y
 15. Gyro upper Z
 16. Gyro lower X
 17. Gyro lower Y
 18. Gyro lower Z

(Siehe auch die beiliegende Datei SensorPlacement.png)

--

Jede Abgabe wird mittels eines Scores bewertet, um das Ranking der Teilnehmer zu ermitteln. Dabei gilt: Je höher der Score, desto besser der Rang der Einreichung. Als Score benutzen wir die Erkennungsrate:

 Accuracy = \frac{anzahl richig zugewiesene labels}{anzahl labels insgesamt}




## :bookmark: Technologies

###  Verwandete Modele 

- K-neirest Neighbors(Knn) 
- Logistic regration
- Neural network


## :bug: Issues


## :pencil: Documentation 

See (https://bbdc.csl.uni-bremen.de/)

## :construction_worker: AndroX Contributors 

- Arnol Namegni (djomonam@uni-bremen.de) 
- Belona Sonna ()

