# Eniac – A/B-Testing mit Chi-Quadrat-Test

## Projektbeschreibung

In diesem Projekt werden vier verschiedene Varianten (A, B, C und D) einer Website des spanischen Elektronikhändlers Eniac untersucht.

Ziel der Analyse ist es, die Auswirkungen unterschiedlicher Button-Gestaltungen und Beschriftungen auf das Klickverhalten der Website-Besucher zu vergleichen.

Mithilfe statistischer Methoden wird geprüft, ob die beobachteten Unterschiede zwischen den vier Varianten statistisch signifikant sind.

## Zielsetzung

Die zentrale Fragestellung lautet:

Welche der vier Website-Varianten erzielt die höchste Click-Through-Rate (CTR), und sind die Unterschiede zwischen den Varianten statistisch signifikant?

Dabei werden folgende Aspekte untersucht:

- Vergleich der vier Button-Varianten
- Berechnung und Analyse der CTR
- Durchführung paarweiser Chi-Quadrat-Tests
- Anwendung der Bonferroni-Korrektur
- Statistische Bewertung der Ergebnisse
- Ableitung einer Handlungsempfehlung

## Untersuchte Varianten

| Version | Button-Gestaltung |
|---|---|
| A | Weißer Button „JETZT KAUFEN“ |
| B | Roter Button „JETZT KAUFEN“ |
| C | Weißer Button „ANGEBOTE ANSEHEN“ |
| D | Roter Button „ANGEBOTE ANSEHEN“ |

## Verwendete Technologien

- Python
- Google Colab / Jupyter Notebook
- Pandas
- NumPy
- SciPy
- Statistische Hypothesentests
- Chi-Quadrat-Test

## Methodik

### 1. Datenaufbereitung

Die vier Datensätze (A, B, C und D) wurden geladen, überprüft und für die vergleichende Analyse vorbereitet.

### 2. Explorative Datenanalyse

Die Daten wurden untersucht, um die Verteilung der Klicks und die Unterschiede zwischen den Website-Varianten zu verstehen.

### 3. CTR-Berechnung

Die Click-Through-Rate (CTR) wurde für jede Variante berechnet und miteinander verglichen.

### 4. Statistische Hypothesentests

Zur Überprüfung der Unterschiede wurden paarweise Chi-Quadrat-Tests durchgeführt.

Insgesamt wurden sechs Vergleiche untersucht:

- A vs. B
- A vs. C
- A vs. D
- B vs. C
- B vs. D
- C vs. D

### 5. Bonferroni-Korrektur

Aufgrund der sechs paarweisen Vergleiche wurde eine Bonferroni-Korrektur angewendet, um das Risiko eines Fehlers erster Art bei multiplen Tests zu berücksichtigen.

Das angepasste Signifikanzniveau beträgt:

α = 0,05 / 6 = 0,00833

## Ergebnisse

| Version | CTR |
|---|---:|
| A | 2,02 % |
| B | 1,14 % |
| C | 2,12 % |
| D | 0,76 % |

Version C erzielt die höchste beobachtete CTR, gefolgt von Version A.

### Ergebnisse der paarweisen Vergleiche

- Zwischen A und C besteht kein statistisch signifikanter Unterschied.
- C ist statistisch signifikant besser als B und D.
- A ist ebenfalls statistisch signifikant besser als B und D.

Die vollständige Übersicht der sechs paarweisen Vergleiche ist hier dargestellt:

[Chi-Quadrat-Vergleich – Ergebnistabelle](reports/Chi_Quadrat_Vergleich.png)

## Fazit und Handlungsempfehlung

Version C weist mit 2,12 % die höchste beobachtete Click-Through-Rate auf. Allerdings besteht kein statistisch signifikanter Unterschied zwischen Version A und Version C.

Beide Varianten schneiden signifikant besser ab als B und D.

Daher können A und C als die leistungsstärksten Varianten betrachtet werden. Ein eindeutiger statistischer Gewinner lässt sich jedoch nicht bestimmen.

Für weitere Tests sollten insbesondere die Varianten A und C berücksichtigt werden.

## Einschränkungen der Analyse

- Die Analyse basiert auf den verfügbaren aggregierten Daten.
- Die Klickzahlen auf HTML-Elemente entsprechen nicht zwangsläufig der Anzahl eindeutiger Nutzer.
- Statistische Signifikanz ist nicht automatisch mit wirtschaftlicher Relevanz gleichzusetzen.
- Für weiterführende Untersuchungen wären vollständige nutzerbezogene Conversion-Daten hilfreich.

## Projektdateien

**Jupyter Notebook**

[Eniac_AB_testing_chi_square_test.ipynb](notebooks/Eniac_AB_testing_chi_square_test.ipynb)

**Quelldaten**

- [Version A](data/raw/eniac_a.csv)
- [Version B](data/raw/eniac_b.csv)
- [Version C](data/raw/eniac_c.csv)
- [Version D](data/raw/eniac_d.csv)

**Auswertung und Ergebnisse**

- [Ergebnisse und Fazit](reports/Ergebnisse_und_Fazit.md)
- [Chi-Quadrat-Vergleich](reports/Chi_Quadrat_Vergleich.png)

## Autorin JuliaAltmann

Data Analytics Portfolio Project

Schwerpunkte: Python, Datenanalyse, statistische Hypothesentests und Business Analytics.
