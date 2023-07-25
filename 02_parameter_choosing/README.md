# 01_parameter_choosing

After retrieving all data and creating the german_stop_words / other stopwords, we needed to define the parameters in which each set of documents would be modeled on. 
The parameters refer to BERtopics building blocks, namely UMAP and hbdscan.

- UMAP : o que faz UMAP
- hdbscan: o que faz esse segundo bloco

Qual é a diferenca entre escolher um ou outro parâmetro? O que pode resultar nos tópicos finais?

Other works (quote) do not explain how they choosed the parameters that lead to the final model with which they perform their analisys. In this work, it is one of our goals to stablish a methodology for parameter choosing with minimal subjectivity

In this part of the repository, we are running routines in order to establish parameter for the following sets of laws and normative documents:

1. EU Daten and AI regulation
2. EU Circular economy, green deal and Timber regulation
3. AT Daten and AI regulation
4. AT Circular economy, green deal and Timber regulation
5. DE Daten and AI regulation
6. DE Circular economy, green deal and Timber regulation

## Method

For parameter choosing we are first running 60 models based on 60 diferent combinations of the parameters: ```umap::n_neighbors``` [5, 7, 10, 20], ```umap::min_dist``` [0.0, 0.1, 0.25] , and ```hdbscan::min_cluster_size``` and ```min_samples``` {10: 2.5, 15: 3.75, 20: 5.0, 25: 6.25, 30: 7.5}  . Esses parametros baseiam-se nas documentacoes do BERTopic , HDBSCAN e UMAP . Decidimos permanecer com os valores default para outros importantes parametros como ```umap::n_components``` (5),  ```CountVectorizer::n_gram_range``` (1,1), ```BERTopic::min_topic_size``` (10) e automático ```BERTopic::nr_topics```

(corrigir os valores acima)

For each model, we calculated:

- agv_similarity: average of similarity coeficient between topics. This matrix is obtained within the Bertopic and tells how a topic differenciate itself from other topics
- topic coherence: using the library XXX , the topic coherence for each model was calculated.

(explicar melhor)

With these metrics, we plot a dispersion graphic to analize the better combinations, considering also a suitable number of topics (usually nr_topics > 4 and < 25).
An example of this graphic:

![output example EU Daten und KI](C:/Users/JVoigt/OneDrive - Universität für Weiterbildung Krems/Dokumente/PythonScripts/new_champions/02_parameter_choosing/output_example.png)

After choosing the ranges for agv_similarity and topic coherence, we plot the remaining models and, to select the best model, we consider the following visualizations: Similarity Matrix and Blabla (pegar o nome)

![similarity_matrix](C:/Users/JVoigt/OneDrive - Universität für Weiterbildung Krems/Dokumente/Python Scripts/new_champions/02_parameter_choosing/similarity_matrix.jpg)

![distance_topics](C:/Users/JVoigt/OneDrive - Universität für Weiterbildung Krems/Dokumente/Python Scripts/new_champions/02_parameter_choosing/distance_topics.jpg)

And after analizing the plots, we drawn conclusion based on the topics available. In this case, we search for topics that relate with possible themes within each set of normative documents. 