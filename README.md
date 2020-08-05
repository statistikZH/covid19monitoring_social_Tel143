![](https://opendata.swiss/content/uploads/2016/02/kt_zh.png)

# Datenanalyse Dargebotene Hand

**Datenquelle:** [Dargebotene Hand](https://www.143.ch/)  
**Mitteilung**: [Corona verändert Alltagssorgen nur wenig](zh.ch)  
**Code**: [R Markdown]()  

## Projektbeschreibung

Dieses Repository enthält Daten und Code um die Mitteilung [Corona verändert Alltagssorgen nur wenig](zh.ch) des Statistischen Amt des Kantons Zürich zu reproduzieren. Daten wurden von dem Schweizer Sorgentelefon «Dargebotene Hand» zur Verfügung gestellt. Die bereinigten Rohdaten werden gemeinsam mit dem Source Skript im R Markdown (Rmd) Format zur Verfügung gestellt. 

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

R version 4.0.0 (2020-04-24) (2018-04-23)  
RStudio version 1.3.959  

Dependencies:

|          |package   |loadedversion |
|:---------|:---------|:-------------|
|devtools  |devtools  |2.3.1         |
|dplyr     |dplyr     |1.0.0         |
|ggplot2   |ggplot2   |3.3.2         |
|knitr     |knitr     |1.29          |
|lubridate |lubridate |1.7.9         |
|magrittr  |magrittr  |1.5           |
|readr     |readr     |1.3.1         |
|rmarkdown |rmarkdown |2.3           |
|statR     |statR     |0.0.0.9000    |
|tidyr     |tidyr     |1.1.0         |
|usethis   |usethis   |1.6.1         |

## Mitwirkende

Vielen Dank an folgende Personen die mitgewirkt haben: 

[@kalakaru](https://github.com/kalakaru)
[@larnsce](https://github.com/larnsce)

## Kontakt

Lars Schöbitz  
lars.schoebitz@statistik.ji.zh.ch  
+41 43 259 75 68  

Katharina Kälin  
katharina.kaelin@statistik.ji.zh.ch  
+41 43 259 75 08  

![Twitter Follow](https://img.shields.io/twitter/follow/statistik_zh?style=social)

## Lizenzen

Dieses Projekt untersteht folgenden Lizenzen: <br>
- Datenlizenz: [Attribution 4.0 International](https://github.com/statistikZH/STAT_Schablone/blob/master/LICENSE_data)
- Codelizenz: [Copyright (c) <2019> <Statistisches Amt Kanton Zürich>](https://github.com/statistikZH/STAT_Schablone/blob/master/LICENSE_code)

## Richtlinien für Beiträge
Wir begrüßen Beiträge. Bitte lesen Sie unsere [CONTRIBUTING.md](https://github.com/statistikZH/STAT_Schablone/blob/master/CONTRIBUTING.md) Datei, wenn sie daran interessiert sind. Hier finden Sie Informationen die zeigen wie Sie beitragen können. 

Bitte beachten Sie, dass dieses Projekt mit einem [Verhaltenskodex](https://github.com/statistikZH/STAT_Schablone/blob/master/CodeOfConduct.md) veröffentlicht wird. Mit Ihrer Teilnahme an diesem Projekt erklären Sie sich mit dessen Bedingungen einverstanden.


