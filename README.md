# champions_2.0
In this repository, I collect, slice and perform a topic modeling analisys using BERTopic with normative documents from the EU, Germany and Austria. In this repository Prof. Dr. Thomas Lampoltshammer and I elaborated a methodology for parameter searching for BERTopic. This is the coding for the iDSC Paper 2023
<br><br>
## Folder: 00_communicados, 00_gesetze_pdf<br>
Sources: normative documents and laws from EU, DE and AT
<br><br>
## Folder: 01_gesetze_sammlung<br>
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
<br><br>
## Folder: 02_parameter_choosing <br>
We grouped the normative documents into "Daten und KI" and "Timber" to analising it with BERTopic. However, we were not sure what the right parameter for ```n_neighbors```, ```min_dist```, ```min_cluster``` and ```min_sample``` should be. To choose the right group of parameters, we performed tests with different parameters combination and then looked at the avg_similarity, topics visualizations and, finally, the topics itself (this is better explained in the iDSC paper). The scripts are:
- ```parameter_choosing_at.ipynb``` : First attempt to work with Austrian documents. I didn't use this file at the end
- ```parameter_choosing_at_daten_ki.ipynb``` : Normative documents for Data and AI in Austria
- ```parameter_choosing_at_regierung.ipynb``` :  Austrian government program
- ```parameter_choosing_at_timber.ipynb``` : Normative documents for timber / forest , climate and land in Austria

  <br><br>
  All the visualizations were saved in the respective folders (AT_DATEN_KI) and so on. Then we manually analyzed these files and selected the best visualization (therefore the OK after the folder name, showing that we inspect it). 
- ```parameter_choosing_de_daten_ki.ipynb``` : Normative documents for Data and AI in Germany
- ```parameter_choosing_de_regierung.ipynb``` :  German government program
- ```parameter_choosing_de_timber_kl.ipynb```: Normative documents for timber / forest , climate and land in Germany
- ```parameter_choosing_eu3.ipynb``` : Parameter settings - EU Daten und KI
- ```parameter_choosing_eu_klimatimber.ipynb``` : Normative documents for timber / forest , climate and land in EU

The visualizations were saved in the respective folders ("AT_DATEN_KI", etc.) and we manually look into each visualization to see which one fits the research's purposes. These folders are marked with an "OK" after it, and each of them contain the file with the visualization with the best parameters and another folder called "old", with the other excluded set of parameters.
