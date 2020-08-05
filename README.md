![](https://opendata.swiss/content/uploads/2016/02/kt_zh.png)

# Projekt Name

## Projektbeschreibung

Beschreibe hier das Projekt: Einführung, Methodik, Ergebnisse, empfohlene Zitierform etc. <br>
Bedenke, dass github der Ort ist, an dem wir Code austauschen. Dies ist also der Ort, an dem interessierte Personen nach Anweisungen suchen. Interessierte möchen hier z.B: informationen zu folgenden Themen finden: Wie die Analyse durchgeführt wurde? Was muss beim Ausführen des Codes beachtet werden? Was bedeuten die Variablennamen? Ein schönes Beispiel ist hier zu finden: https://github.com/tamedia-ddj/SUV_Analyse_Schweiz

## Daten

### raw_data

**Social_Tel143_nach_monat.csv**

|Spaltenname |Beschreibung                                                                                      |Format |
|:-----------|:-------------------------------------------------------------------------------------------------|:------|
|variable    |Variablen zu welchen bei einem Anruf Informationen aufgenommen werden                             |Text   |
|kategorie   |Jeweilige Kategorien für die einzelnen Variablen                                                  |Text   |
|wert        |Wert für die jeweiligen Kategorien (siehe 'Wichtige Anmerkung' für wichtige Details zu Variablen) |Zahl   |
|jahr        |Kalenderjahr                                                                                      |Zahl   |
|monat       |Monat des Kalenderjahres                                                                          |Zahl   |


**Social_Tel143_nach_quartal.csv**

|Spaltenname  |Beschreibung                                                                             |Format |
|:------------|:----------------------------------------------------------------------------------------|:------|
|variable     |Variablen zu welchen bei einem Anruf Informationen aufgenommen werden                    |Text   |
|kategorie    |Jeweilige Kategorien für die einzelnen Variablen                                         |Text   |
|altersklasse |Kreuzung der variablen nach Alterklassen                                                 |Text   |
|wert         |Wert für die jeweiligen Kategorien (siehe 'Wichtige Anmerkung' für Details zu Variablen) |Zahl   |
|jahr         |Kalenderjahr                                                                             |Zahl   |
|quartal      |Quartal des Kalenderjahres                                                               |Text   |

**Wichtige Anmerkung** Zu beachten ist, dass `wert` summiert nach `variable` nicht die gleiche Summe für jede Variable ergibt. Die totale Anzahl Anrufe ist die Summe der `variable` "Schicht". Falls ein Anruf in die `variable` "Zusätzliche Beanspruchung" fällt, werden keine weiteren Details für `variable` "Alter", "Geschlecht" und "Kontakthäufigkeit" aufgenommen. Zum Beispiel: die Summe aus `wert` für "Alter" und "Zusätzliche Beanspruchung" ist gleich der Summe aus `wert` für "Schicht". Die `variable` "Gesprächsdauer" gibt den median und mittelwert an. Die `variable` "Beratungsinhalt" ist die Anzahl der Inhalte, welche aufgenommen wurde. Pro Anruf können mehrere Beratungsinhalte gewählt werden.

### derived_data

Tabellen in diesem Ordner sind zusammengefasste Hintergrunddaten der drei Grafiken. Der Code für die Daten ist in `article/Social_Tel143_article.Rmd` enthalten. 

## Voraussetzungen

z.B.: 

R version 3.5.0 (2018-04-23) <br>
RStudio version 1.1.453 <br>
Deppendencies: <br>
|package name | version number |
| ------------- | ------------- | 
|dplyr     |    0.8.3 |
|sf     |    0.8-1 |


R Code um die obigen Informationen zu erhalten: 

```R 
# R version
print(version[['version.string']])
# R Studio Version
require(rstudioapi)
RStudioversionInfo <- versionInfo()
print(paste("RStudio version", RStudioversionInfo$version))
# list names of loaded libraries with version number
print(subset(data.frame(sessioninfo::package_info()), attached==TRUE, c(package, loadedversion)),  row.names = FALSE)
```

## Mitwirkende

Vielen Dank an folgende Personen die mitgewirkt haben: 

[@kalakaru](https://github.com/kalakaru)
[@mmznrSTAT](https://github.com/mmznrSTAT)

## Kontakt

Vorname Nachname  <br>
vorname.nachname@statistik.ji.zh.ch <br>
Telefonnummer <br>

![Twitter Follow](https://img.shields.io/twitter/follow/statistik_zh?style=social)

## Lizenzen

Dieses Projekt untersteht folgenden Lizenzen: <br>
- Datenlizenz: [Attribution 4.0 International](https://github.com/statistikZH/STAT_Schablone/blob/master/LICENSE_data)
- Codelizenz: [Copyright (c) <2019> <Statistisches Amt Kanton Zürich>](https://github.com/statistikZH/STAT_Schablone/blob/master/LICENSE_code)

## Richtlinien für Beiträge
Wir begrüßen Beiträge. Bitte lesen Sie unsere [CONTRIBUTING.md](https://github.com/statistikZH/STAT_Schablone/blob/master/CONTRIBUTING.md) Datei, wenn sie daran interessiert sind. Hier finden Sie Informationen die zeigen wie Sie beitragen können. 

Bitte beachten Sie, dass dieses Projekt mit einem [Verhaltenskodex](https://github.com/statistikZH/STAT_Schablone/blob/master/CodeOfConduct.md) veröffentlicht wird. Mit Ihrer Teilnahme an diesem Projekt erklären Sie sich mit dessen Bedingungen einverstanden.


