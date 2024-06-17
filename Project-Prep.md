# Project Preperations

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

> 💡 We display only **10 items** as an **example** in the tables. 

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

## Our Starting Point

#### 4. We want to know which pages are related to the Monumental Area labeled as *Palazzo Poggi*?

```SPARQL
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT DISTINCT ?site  ?label
WHERE {
?site ?property <https://w3id.org/arco/resource/MonumentalArea/palazzo-poggi>.
?site rdfs:label  ?label.
}
```
We filter with `?site` and with `?label`

<table width="200" height="300">
  <tbody><tr>
    <th>site</th>
    <th>label</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/Site/10030365c1d4a267a4e7cbf031bd1a6b">https://w3id.org/arco/resource/Site/10030365c1d4a267a4e7cbf031bd1a6b</a></td>
    <td><pre>"Isituto delle Scienze"</pre></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/Site/253f678523ccc14d563964cd30d0097a">https://w3id.org/arco/resource/Site/253f678523ccc14d563964cd30d0097a</a></td>
    <td><pre>"Università degli Studi di Bologna"</pre></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/Site/27641117e6d58e7482a605fdf544a034">https://w3id.org/arco/resource/Site/27641117e6d58e7482a605fdf544a034</a></td>
    <td><pre>"Palazzo Poggi"</pre></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/Site/4dd253f16ef2760bc43d80e96d3118e2">https://w3id.org/arco/resource/Site/4dd253f16ef2760bc43d80e96d3118e2</a></td>
    <td><pre>"Istituto delle Scienze"</pre></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/Site/a5e73b25845521559dceef201110b92e">https://w3id.org/arco/resource/Site/a5e73b25845521559dceef201110b92e</a></td>
    <td><pre>"Istituto delle Scienze"</pre></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/Site/dd3f107c04684f40f1f413a3955937d5">https://w3id.org/arco/resource/Site/dd3f107c04684f40f1f413a3955937d5</a></td>
    <td><pre>"Isitituto delle Scienze"</pre></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/Site/f6654877c6622d13203734d2b2b2333f">https://w3id.org/arco/resource/Site/f6654877c6622d13203734d2b2b2333f</a></td>
    <td><pre>"Istituto delle Scienze"</pre></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/Site/f6bb041c26283b0c4af2edd0ed2caef6">https://w3id.org/arco/resource/Site/f6bb041c26283b0c4af2edd0ed2caef6</a></td>
    <td><pre>"Museo di Palazzo Poggi"</pre></td>
  </tr>
</tbody></table>

5. Now we want to know what are the distinct **properties and objects** related to the resource?

```SPARQL
PREFIX rdfs: <https://w3id.org/arco/resource/Site/27641117e6d58e7482a605fdf544a034>
SELECT DISTINCT ?property ?object
WHERE {
  <https://w3id.org/arco/resource/Site/27641117e6d58e7482a605fdf544a034> ?property ?object.
}
ORDER BY ?property
```
> Here we used the keyword **ORDER BY** to find the properties.

<table width="200" height="300">
  <tbody><tr>
    <th>property</th>
    <th>object</th>
  </tr>
  <tr>
    <td><a href="http://dati.beniculturali.it/cis/isPartOf">http://dati.beniculturali.it/cis/isPartOf</a></td>
    <td><a href="https://w3id.org/arco/resource/MonumentalArea/palazzo-poggi">https://w3id.org/arco/resource/MonumentalArea/palazzo-poggi</a></td>
  </tr>
  <tr>
    <td><a href="http://dati.beniculturali.it/cis/isSiteOf">http://dati.beniculturali.it/cis/isSiteOf</a></td>
    <td><a href="https://w3id.org/arco/resource/CulturalInstituteOrSite/746195e222fec1e6b02657ea1fdc6aae">https://w3id.org/arco/resource/CulturalInstituteOrSite/746195e222fec1e6b02657ea1fdc6aae</a></td>
  </tr>
  <tr>
    <td><a href="http://dati.beniculturali.it/cis/isSiteOf">http://dati.beniculturali.it/cis/isSiteOf</a></td>
    <td><a href="https://w3id.org/arco/resource/CulturalInstituteOrSite/b2cb8c69f90c9fd17e6d7ee956a99ab9">https://w3id.org/arco/resource/CulturalInstituteOrSite/b2cb8c69f90c9fd17e6d7ee956a99ab9</a></td>
  </tr>
  <tr>
    <td><a href="http://dati.beniculturali.it/cis/siteAddress">http://dati.beniculturali.it/cis/siteAddress</a></td>
    <td><a href="https://w3id.org/arco/resource/Address/d9098b0d8115b1d8e0b00d5c9b1d1008">https://w3id.org/arco/resource/Address/d9098b0d8115b1d8e0b00d5c9b1d1008</a></td>
  </tr>
  <tr>
    <td><a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#type">http://www.w3.org/1999/02/22-rdf-syntax-ns#type</a></td>
    <td><a href="http://dati.beniculturali.it/cis/Site">http://dati.beniculturali.it/cis/Site</a></td>
  </tr>
  <tr>
    <td><a href="http://www.w3.org/2000/01/rdf-schema#label">http://www.w3.org/2000/01/rdf-schema#label</a></td>
    <td><pre>"Palazzo Poggi"</pre></td>
  </tr>
  <tr>
    <td><a href="http://www.w3.org/2002/07/owl#deprecated">http://www.w3.org/2002/07/owl#deprecated</a></td>
    <td><pre>"true"^^&lt;http://www.w3.org/2001/XMLSchema#boolean&gt;</pre></td>
  </tr>
  <tr>
    <td><a href="http://www.w3.org/2002/07/owl#sameAs">http://www.w3.org/2002/07/owl#sameAs</a></td>
    <td><a href="http://dati.beniculturali.it/iccd/cf/resource/CulturalInstituteOrSite/ICCD_CF_0189237996461">http://dati.beniculturali.it/iccd/cf/resource/CulturalInstituteOrSite/ICCD_CF_0189237996461</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/ontology/location/hasSiteType">https://w3id.org/arco/ontology/location/hasSiteType</a></td>
    <td><a href="https://w3id.org/arco/resource/SiteType/palazzo">https://w3id.org/arco/resource/SiteType/palazzo</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/ontology/location/hasSiteType">https://w3id.org/arco/ontology/location/hasSiteType</a></td>
    <td><a href="https://w3id.org/arco/resource/SiteType/palazzo-senatorio">https://w3id.org/arco/resource/SiteType/palazzo-senatorio</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/italia/onto/l0/name">https://w3id.org/italia/onto/l0/name</a></td>
    <td><pre>"Palazzo Poggi"</pre></td>
  </tr>
</tbody></table>

We see that the results are related to Palazzo Poggi (monumental Area): 
- Istituto delle Scienze
- Museo della SPECOLA
- Museo di PALAZZO POGGI

Summary: We found the relations and properties to Palazzo Poggi, now we will continue investigating these pages more in detail to find items that are related to Collezione Marsili and Collezione Aldrovandi.

> 💡 to continue reading click on to [*Next Chapter*](Museo-di-Palazzo-Poggi.md) or go back to our [*Main Page*](index.md).
