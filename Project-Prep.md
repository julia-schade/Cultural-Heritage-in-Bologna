# 1. Project Preparations

 <img src="https://www.guidobarbi.it/wp-content/uploads/2023/04/Bartolomeo-Triachini-Cortile-dErcole-con-statua-dErcole-di-Angelo-Pio-copia-a-Palazzo-Poggi-a-Bologna.jpg"
         alt="Palazzo Poggi">
         
         

#### 1. We started our idea for the project with the question *What cultural properties are members of the collection X?* that we found on Arco website.
##### To retrieve pairs of the collections and their items, we used the keyword **LIMIT 100**. 

```SPARQL
PREFIX arco-cd: <https://w3id.org/arco/ontology/context-description/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
SELECT ?collection ?item
WHERE {
 ?collection a cis:CollectionCulEnt.
 ?collection arco-cd:isCollectionIn ?collectionmemb.
 ?collectionmemb arco-cd:hasMemberOfCollection ?item.
} LIMIT 100
```

The code retrieves a list of cultural collections and their respective items from a specified dataset, limiting the results to 100.

To prove that the codes work, we created a table for each query to show the results.

> 💡 On the website we are going to display only **10 items** as an **example** in the tables, but we actually worked with all the results! 

<table width="200" height="300">
  <tbody><tr>
    <th>collection</th>
    <th>item</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-strumentaria-medica-siena-fisiologia">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-strumentaria-medica-siena-fisiologia</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0900753118">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0900753118</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-strumentaria-medica-siena-fisiologia">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-strumentaria-medica-siena-fisiologia</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0900753173">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0900753173</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-strumentaria-medica-siena-fisiologia">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-strumentaria-medica-siena-fisiologia</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0900753176">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0900753176</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688526">https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688526</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688537">https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688537</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691113">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691113</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691114">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691114</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691115">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691115</a></td>
  </tr>
</tbody></table>

##### 1.1 We eliminated the potential duplicates with **DISTINCT**

`SELECT DISTINCT ?collection ?item:` Adding DISTINCT ensures that each combination of `?collection` and `?item` in the result set is unique, thereby removing duplicates.

```SPARQL
PREFIX arco-cd: <https://w3id.org/arco/ontology/context-description/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
SELECT DISTINCT ?collection ?item
WHERE {
 ?collection a cis:CollectionCulEnt.
 ?collection arco-cd:isCollectionIn ?collectionmemb.
 ?collectionmemb arco-cd:hasMemberOfCollection ?item.
} LIMIT 100
```

<table width="200" height="300">
  <tbody><tr>
    <th>collection</th>
    <th>item</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-strumentaria-medica-siena-fisiologia">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-strumentaria-medica-siena-fisiologia</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0900753118">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0900753118</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-strumentaria-medica-siena-fisiologia">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-strumentaria-medica-siena-fisiologia</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0900753173">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0900753173</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-strumentaria-medica-siena-fisiologia">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-strumentaria-medica-siena-fisiologia</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0900753176">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0900753176</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688526">https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688526</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688537">https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688537</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691113">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691113</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691114">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691114</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691115">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691115</a></td>
  </tr>
</tbody></table>

##### 2. We wanted to know which items are part of Collezione Marsili and Aldrovandi

We looked for the items in two separate queries.

> We used the keywords FILTER, REGEX, and `i` to ignore capital letters.

##### 2.1 Collezione Marsili

```SPARQL
PREFIX arco-cd: <https://w3id.org/arco/ontology/context-description/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
SELECT ?collection ?item
WHERE {
  ?collection a cis:CollectionCulEnt.
  ?collection arco-cd:isCollectionIn ?collectionmemb.
  ?collectionmemb arco-cd:hasMemberOfCollection ?item.
  ?collection rdfs:label ?collectionLabel.
  FILTER (REGEX(?collectionLabel, "collezione marsili", "i"))
} LIMIT 100
```

<table width="200" height="300">
  <tbody><tr>
    <th>collection</th>
    <th>item</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691113">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691113</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691113">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691113</a></td>
  </tr>
</tbody></table>

##### 2.2 Collezione Aldrovandi

```SPARQL
PREFIX arco-cd: <https://w3id.org/arco/ontology/context-description/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
SELECT ?collection ?item
WHERE {
  ?collection a cis:CollectionCulEnt.
  ?collection arco-cd:isCollectionIn ?collectionmemb.
  ?collectionmemb arco-cd:hasMemberOfCollection ?item.
  ?collection rdfs:label ?collectionLabel.
  FILTER (REGEX(?collectionLabel, "collezione aldrovandi", "i"))
} LIMIT 100
```

<table width="200" height="300">
  <tbody><tr>
    <th>collection</th>
    <th>item</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688526">https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688526</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688526">https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688526</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688537">https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688537</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688537">https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688537</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688401">https://w3id.org/arco/resource/NaturalHeritage/0800688401</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688401">https://w3id.org/arco/resource/NaturalHeritage/0800688401</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688402">https://w3id.org/arco/resource/NaturalHeritage/0800688402</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688402">https://w3id.org/arco/resource/NaturalHeritage/0800688402</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688403">https://w3id.org/arco/resource/NaturalHeritage/0800688403</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688403">https://w3id.org/arco/resource/NaturalHeritage/0800688403</a></td>
  </tr>
</tbody></table>

#### 3. We applied **DISTINCT** to eliminate the potential duplicates

> We used the keyword DISTINCT, FILTER and REGEX on both collections.

##### 3.1 DISTINCT for Collezione Marsili

```SPARQL
PREFIX arco-cd: <https://w3id.org/arco/ontology/context-description/> 
PREFIX cis: <http://dati.beniculturali.it/cis/> 
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#> 
SELECT DISTINCT ?collection ?item 
WHERE { 
?collection a cis:CollectionCulEnt. 
?collection arco-cd:isCollectionIn ?collectionmemb. 
?collectionmemb arco-cd:hasMemberOfCollection ?item. 
?collection rdfs:label ?collectionLabel. 
FILTER (REGEX(?collectionLabel, "collezione marsili", "i")) 
} LIMIT 100
```

<table width="200" height="300">
  <tbody><tr>
    <th>collection</th>
    <th>item</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691111</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691112</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691113">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691113</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691114">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691114</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691115">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691115</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691116">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691116</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691117">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691117</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691118">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691118</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691119">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691119</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili</a></td>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691120">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800691120</a></td>
  </tr>
</tbody></table>

##### 3.2 DISTINCT for Collezione Aldrovandi

```SPARQL
PREFIX arco-cd: <https://w3id.org/arco/ontology/context-description/> 
PREFIX cis: <http://dati.beniculturali.it/cis/> 
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#> 
SELECT DISTINCT ?collection ?item 
WHERE { ?collection a cis:CollectionCulEnt. 
?collection arco-cd:isCollectionIn ?collectionmemb. 
?collectionmemb arco-cd:hasMemberOfCollection ?item. 
?collection rdfs:label 
?collectionLabel. 
FILTER (REGEX(?collectionLabel, "collezione aldrovandi", "i")) 
} LIMIT 100
```

<table width="200" height="300">
  <tbody><tr>
    <th>collection</th>
    <th>item</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688526">https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688526</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688537">https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688537</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688401">https://w3id.org/arco/resource/NaturalHeritage/0800688401</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688402">https://w3id.org/arco/resource/NaturalHeritage/0800688402</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688403">https://w3id.org/arco/resource/NaturalHeritage/0800688403</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688404">https://w3id.org/arco/resource/NaturalHeritage/0800688404</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688405">https://w3id.org/arco/resource/NaturalHeritage/0800688405</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688406">https://w3id.org/arco/resource/NaturalHeritage/0800688406</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688407">https://w3id.org/arco/resource/NaturalHeritage/0800688407</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi">https://w3id.org/arco/resource/CollectionCulEnt/museo-di-palazzo-poggi-bologna-collezione-aldrovandi</a></td>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688408">https://w3id.org/arco/resource/NaturalHeritage/0800688408</a></td>
  </tr>
</tbody></table>

Now we have the raw basis for our project, as we were looking for *Collezione Marsili* and *Collezione Aldrovandi* and the items related to them. Exploring the Arco knowledge graph we discovered that all the items are collected in [Palazzo Poggi](https://w3id.org/arco/resource/MonumentalArea/palazzo-poggiAN)



Summary: We found the objects and properties related to Palazzo Poggi, now we will continue investigating these pages more in detail to find items belonging to Collezione Marsili and Collezione Aldrovandi.

> 🧭 
> - [Next ⏭](Poggi.md) 
> - [Home 🏠](index.md)

