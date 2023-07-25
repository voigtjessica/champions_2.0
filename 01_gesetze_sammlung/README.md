# 01_gesetze_sammlung

Retrieving guidelines, strategic papers, laws, usw from EU, DE and AT under the theme AI and Data

Goal of this scripts:
- to import all the documents in one single object
- save this as pickle or json, still didn'T decided

## Documents:

EU Circular Economy Action Plan	<br>
AT Bioökonomiestrategie und Aktionsplan Bioökonomie	<br>
AT Kreislaufwirtschaftsstrategie und ihre Ziele	<br>
	
    - Ziel 1: Reduktion des inländischen Ressourcenverbrauchs <br>
	- Ziel 2: Steigerung der Ressourceneffizienz der österreichischen Wirtschaft <br>
	- Ziel 3: Steigerung der Circular Material Use Rate um 40 % bis 2030 (Basisjahr 2017) <br>
	- Ziel 4: Reduktion des Abfallaufkommens aus dem privaten Konsum um 10 % bis 2030. <br>

<br>

FTI Initiative Kreislaufwirtschaft	<br>
AT Mobilitätsmasterplan 2030 https://www.bmk.gv.at/themen/mobilitaet/mobilitaetsmasterplan/mmp2030.html	<br>
FTI – Strategie für Luftfahrt	<br>
FTI-Strategie Mobilität & FTI-Agenda Mobilität 2026	<br>

### EU
Data Governance Act  - Law <br> 
Data Act - Law <br>
Green Deal (Daten) - Set of laws  <br>
KI Strategie<br>
Horizon Europe<br>
Data Spaces<br>


### AT
KI Strategie<br>
Regierungsprogramm<br>
AT KI-Strategie sowie Roadmap Daten durchdringen<br>

## What will entail each documment?

The goal is that each document (for the TM) eintails one "theme" of the law. So we will use the structure of the law to subdivide it in topics.
EU laws and Austrian and German laws have different structures. After studing the structure of both, we concluded that the Artikle (EU) / Paragraph (AT and DE) would have to many subjects to be one document. Therefore we decided that the documents will have the following structure:

## For EU Law:

Artikel + Absatzt - number with () + Buchstaben - if it is the case

OR

(for Artickels without Absatzt)

Artikel + Nummer - number without () + Buchstaben - if it is the case <br>


## For DE and AT:

Absatz - number with () + Nummer - number without () + Buchstaben - if it is the case<br>

OR

Absatz - number with () + Buchstaben - if it is the case<br>


---

## Explanation of script names:

- name_retrieve = the code in which I build the laws dfs
