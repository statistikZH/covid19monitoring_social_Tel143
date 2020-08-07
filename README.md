![](https://opendata.swiss/content/uploads/2016/02/kt_zh.png)

# Datenanalyse Dargebotene Hand

**Datenquelle:** [Dargebotene Hand](https://www.143.ch/)  
**Mitteilung**: [Corona verändert Alltagssorgen nur wenig](https://www.zh.ch/de/news-uebersicht/mitteilungen/2020/politik-staat/statistik/corona-veraendert-alltagssorgen-nur-wenig.html)  
**Code**: [R Markdown](https://github.com/statistikZH/covid19monitoring_social_Tel143/blob/main/article/Social_Tel143_article.Rmd)  

## Projektbeschreibung

Dieses Repository enthält Daten und Quellcode um die Mitteilung «[Corona verändert Alltagssorgen nur wenig](https://www.zh.ch/de/news-uebersicht/mitteilungen/2020/politik-staat/statistik/corona-veraendert-alltagssorgen-nur-wenig.html)» des Statistischen Amt des Kantons Zürich zu reproduzieren. Daten wurden von dem Schweizer Sorgentelefon «[Dargebotene Hand](https://www.143.ch/)» zur Verfügung gestellt. Die bereinigten Rohdaten werden gemeinsam mit dem Quellcode im R Markdown (.Rmd) Format zur Verfügung gestellt. 

## Rohdaten

### ../data/raw_data/

Hier sind die bereinigten Rohdaten zu finden. 

**Social_Tel143_nach_monat.csv**

Für die Jahre 2019 und 2020 stehen hier monatliche Daten zur Verfügung. 

|Spaltenname   |Beschreibung                                                                                 |Format |
|:-------------|:--------------------------------------------------------------------------------------------|:------|
|`kategorie`     |Kategorien zu welchen bei einem Anruf Informationen aufgenommen werden                       |Text   |
|`sub_kategorie` |Jeweilige Subkategorie für die einzelnen Kategorien                                          |Text   |
|`wert`          |Wert für die jeweiligen Subkategorien (siehe 'Wichtige Anmerkung' für Details zu Kategorien) |Zahl   |
|`einheit`       |Einheit des Werts                                                                            |Text   |
|`jahr`          |Kalenderjahr                                                                                 |Zahl   |
|`monat`         |Monat des Kalenderjahres                                                                     |Zahl   |

**Social_Tel143_nach_quartal.csv**

Für die Jahre 2019 und 2020 stehen hier quartalsweise Daten zur Verfügung. Im Gegensatz zu den monatlichen Daten stehen hier die `variable` "Schicht", "Geschlecht", "Kontakthäufigkeit", "Beratungsinahlt", "Zusätzliche Beanspruchung" sowie "Gesprächsdauer" stehen hier für jede Altersklasse zur Verfügung. 

|Spaltenname   |Beschreibung                                                                              |Format |
|:-------------|:-----------------------------------------------------------------------------------------|:------|
|`kategorie`     |Kategorien zu welchen bei einem Anruf Informationen aufgenommen werden                    |Text   |
|`sub_kategorie` |Jeweilige Subkategorie für die einzelnen Kategorien                                       |Text   |
|`altersklasse`  |Kreuzung der Kategorien nach Alterklassen                                                 |Text   |
|`wert`          |Wert für die jeweiligen Kategorien (siehe 'Wichtige Anmerkung' für Details zu Kategorien) |Zahl   |
|`einheit`       |Einheit des Werts                                                                         |Text   |
|`jahr`         |Kalenderjahr                                                                              |Zahl   |
|`quartal`      |Quartal des Kalenderjahres                                                                |Text   |

**Wichtige Anmerkung** 

- Zu beachten ist, dass das Summieren des Attributs `wert` nach `variable` nicht für jede `variable` dieselbe Summe gibt. Grund hierfür ist, dass für verschobene Gespräche, Schweigeanrufe, Fehlanrufe und Juxanrufe (`variable` = "Zusätzliche Beanspruchung") keine Informationen für die `variable` "Alter", "Geschlecht" und "Kontakthäufigkeit" erfasst werden. Die Anzahl totaler Anrufe errechnet sich durch das Aufsummieren der `variable` "Schicht" oder duch das Aufsummieren der 'variable' Alter" und "Zusätzliche Beanspruchung".
- `variable` "Gesprächsdauer": Median und Mittelwert der Gesprächsdauer 
- `variable` "Beratungsinhalt": Pro Anruf können mehrere Beratungsinhalte gewählt werden

## Plots

### ../data/derived_data/

Hier sind die aufbereiteten Daten für die drei Grafiken der «[Medienmitteilung](https://www.zh.ch/de/news-uebersicht/mitteilungen/2020/politik-staat/statistik/corona-veraendert-alltagssorgen-nur-wenig.html)». Der Quellcode für die Daten ist in diesem [Skript](https://github.com/statistikZH/covid19monitoring_social_Tel143/blob/main/article/Social_Tel143_article.Rmd) zu finden. 

### ../plots/

Hier sind die Grafiken der «[Medienmitteilung](https://www.zh.ch/de/news-uebersicht/mitteilungen/2020/politik-staat/statistik/corona-veraendert-alltagssorgen-nur-wenig.html)» als *.png* abgelegt.

## Skript

### ../article/Social_Tel143_article.Rmd 

Hier ist das Skript der «[Medienmitteilung](https://www.zh.ch/de/news-uebersicht/mitteilungen/2020/politik-staat/statistik/corona-veraendert-alltagssorgen-nur-wenig.html)» als *.Rmd* abgelegt. Mit diesem Skript kann der gesame Artikel mit den folgenden Vorraussetzungen reproduziert werden. 

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

[@kalakaru](https://github.com/kalakaru) | [@larnsce](https://github.com/larnsce) | [@thomhofer](https://github.com/thomhofer) | [Matthias Herren (143.ch)](https://zuerich.143.ch/Organisation/Team) | [Urs Kälin (143.ch)](https://zuerich.143.ch/Organisation/Team)

## Kontakt

Lars Schöbitz  
lars.schoebitz@statistik.ji.zh.ch  
+41 43 259 75 68  

Katharina Kälin  
katharina.kaelin@statistik.ji.zh.ch  
+41 43 259 75 08  

![Twitter Follow](https://img.shields.io/twitter/follow/statistik_zh?style=social)

## Lizenzen

Dieses Projekt untersteht folgenden Lizenzen:  

- Datenlizenz: [Attribution 4.0 International](https://github.com/statistikZH/STAT_Schablone/blob/master/LICENSE_data)
- Codelizenz: [Copyright (c) <2019> <Statistisches Amt Kanton Zürich>](https://github.com/statistikZH/STAT_Schablone/blob/master/LICENSE_code)

## Richtlinien für Beiträge

Wir begrüßen Beiträge. Bitte lesen Sie unsere [CONTRIBUTING.md](https://github.com/statistikZH/STAT_Schablone/blob/master/CONTRIBUTING.md) Datei, wenn sie daran interessiert sind. Hier finden Sie Informationen die zeigen wie Sie beitragen können. 

Bitte beachten Sie, dass dieses Projekt mit einem [Verhaltenskodex](https://github.com/statistikZH/STAT_Schablone/blob/master/CodeOfConduct.md) veröffentlicht wird. Mit Ihrer Teilnahme an diesem Projekt erklären Sie sich mit dessen Bedingungen einverstanden.


