# champions_2.0
In this repository, I collect, slice and perform a topic modeling analisys using BERTopic with normative documents from the EU, Germany and Austria. In this repository Prof. Dr. Thomas Lampoltshammer and I elaborated a methodology for parameter searching for BERTopic. This is the coding for the iDSC Paper 2023
<br><br>
Folder: 00_communicados, 00_gesetze_pdf<br>
Sources: normative documents and laws from EU, DE and AT
<br><br>
01_gesetze_sammlung<br>
In this folder are located the first part of our reserach. 
- ```eu_gesetzt_code_explanation.ipynb```, ```eu_gesetzt_retrieve.ipynb``` : in this files I explain how I created the routine that I'll use to retrieve the information from the normative documents
<br><br>
The following scripts retrieve laws and transform them in data:
- ```data_act_retrieve.ipynb```
- ```de_scrap.ipynb```
- ```eu_clima_law_retrieve.ipynb```
- ```eu_cybersicherheitsstrategie.ipynb```
- ```eu_digital_markets_act.ipynb```
- ```eu_gruene_deal.ipynb```
- ```eu_horizon.ipynb```
- ```eu_land_use_change.ipynb```
- ```eu_regulation_ai.ipynb```
- ```eu_timber_regulation.ipynb```
<br><br>
I consolidate the EU data in the following scripts:
- ```consolidacao_eu.ipynb```
And I created the file ```eu_laws_concatenado.json```
<br><br>Finally, I created the stopwords to use later:
- ```austria_stopwords.ipynb``` , file ```austrian_stopwords.json``` : stopwords to use with documents from Austria
- ```german_bund_stopwords.ipynb```, file ```german_bund_stopwords.json``` : stopwords to use with documents from Germany
- ```german_stopwords.ipynb``` , file: ```german_stopwords.json``` : stopwords to use with documents from EU in german
