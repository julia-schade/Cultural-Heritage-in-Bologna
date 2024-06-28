# Conclusion

This project aimed to enhance the cultural heritage of the University of Bologna, with a particular focus on the ancient collections of *Palazzo Poggi*, once the seat of the ancient Istituto delle Scienze. We sought to accomplish this objective by bringing together three institutions that are closely linked to the past and present of Palazzo Poggi and that house an important cultural treasure: *Istituto delle Scienze*, *Museo Palazzo Poggi*, and *Museo della Specola*. For each of these institutions, we aimed to explore the items they currently preserve and their possible connections with other elements and figures. Specifically, we focused on the contributions of two collectors, *Ulisse Aldrovandi* and *Luigi Ferdinando Marsili*, to the collections currently housed at Palazzo Poggi. Additionally, we wanted to provide examples of these precious objects by including some photos at the end of the pages dedicated to each museum.

To achieve this, we divided the work and used various tools that proved essential for the success of the project: 
1. Julia used GitHub to create the current webpage and access all data and content in a fast and organized way;
2. Chiara and Gianluca used SPARQL to obtain all the information, data, and photos of objects present on ARCO that could be useful for the project;
3. Aleksandra and Angelita used and compared three different LLMs to provide descriptions for our site and identify potential elements to expand in the ARCO knowledge graph.

To conclude, this project turned out to be extremely interesting and challenged us in a field that may seem very distant from our studies, but it enriched our  linguistic knowledge with a different approach that could be very useful in our future, especially for those who wish to continue working in the academic field. We strongly believe that this project can be useful for expanding and improving the ARCO knowledge graph and enhancing the cultural heritage of the University of Bologna, starting with Palazzo Poggi, which is too often underestimated.

## Limitations

1. Structuring the queries due to the fact that we did not understand how to properly use the prefixes. We discovered that ChatGPT and the other LLMs sometimes "invent" properties that do not exist on Arco. So we found out that we could check the prefixes on the namespaces tables available on Virtuoso.
2. While for Aldrovandi collection all the items were directly linked to it, for Marsili collection there was not a direct link: we had to pass through a middle step "rdf: type a-cd: CollectionMembership". For this reason, we had to explore the knowledge graph to get the pictures and the categories of the items (e.g. ScientificandTechnologicalHeritage, and HistoricOrArtisticProperty). --> proposal of expansion
3. After struggling because of many discrepancies in Collezione Marsili, we discovered that the items were archived in two different collections: [Collezione Marsili](https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili) and [Collezioni Marsili](https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezioni-marsili).
4. As regards Large Language Models, we tried to use Llama by Meta and at first it was working, but at some point it started to ask if we were human. Therefore, we couldn’t use it.
5. We found problems with completeness and accuracy in all models, especially in Mistral and Gemini. For example, when we asked for specific items from the collections under analysis, none of the models were able to give us complete answers, instead they were too vague.
6. Furthermore, when trying to use the self-consistency prompt, we noticed that the answers given were never the same as each other and were not precise. So, we have verified that LLMs are not 100% reliable.
7. Github was a great plattform in simplifying the workload of creating a webpage, but it took a lot of time to study the guides and to learn the mechanism e. g. how it receives different coding languages. Thus, it was necessary to define our coding style beforehand.
8. Another limitation for us was the lack of simultaneousness, compared to google docs where simultanious work is possible, here only one person was able to wok on one page at a time, it would not save the new update if another person edited before the own update. Our only solution for this was to communicate more to prevent setbacks and reimplementation of content, which was rather time extensive.


> 🧭
> - [Next ⏭](Sources.md) 
> - [Previous ⏮](Large-Language-Models.md) 
> - [Home ⏮](index.md) 
