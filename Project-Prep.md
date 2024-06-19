# 1. Project Preperations

#### 1. We start our idea for the project with the question on *how to find items in the collections?*
##### To retrieve pairs of the collections and their items, we **LIMIT** with 100. First	we started from the example on Arco website:

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

The code looks for cultural entity collections and finds their members. The result includes the collection and each item that is a member of that collection.

To show that the code works, here is our result, this was also done with LIMIT.

> 💡 We display only **10 items** as an **example** in the tables, instead of all the results. 

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

##### 1.1 We eliminate the duplicates with **DISTINCT**

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

##### 2. We want to know which items are part of Collezione Marsili and Aldrovandi

We look for the items separately in the two queries.

> We use the keywords FILTER and REGEX for the query and `i` to ignore capital letters.

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

#### 3. We want to apply **DISTINCT** to eliminate the duplicates

> We use the keyword DISTINCT, FILTER and REGEX on both collections.

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

Now we have the raw basis for our project, as we were looking for cultural entity collections, we now have the items of the two collections of *Collezione Marsili* and *Collezione Aldrovandi*.



Summary: We found the relations and properties to Palazzo Poggi, now we will continue investigating these pages more in detail to find items that are related to Collezione Marsili and Collezione Aldrovandi.

> 🧭 
> - [Next ⏭](Poggi.md) 
> - [Home 🏠](index.md)

