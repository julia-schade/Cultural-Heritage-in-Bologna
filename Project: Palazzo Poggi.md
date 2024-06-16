# Project Preperations

1. To retrieve up to 100 pairs of collections with LIMIT and their items, 1.	we started from the example on Arco website:

```PREFIX arco-cd: <https://w3id.org/arco/ontology/context-description/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
SELECT ?collection ?item
WHERE {
 ?collection a cis:CollectionCulEnt.
 ?collection arco-cd:isCollectionIn ?collectionmemb.
 ?collectionmemb arco-cd:hasMemberOfCollection ?item.
} LIMIT 100
```

> Comment: *Specifically, it looks for cultural entity collections and finds their members. The result includes the collection and each item that is a member of that collection.*


1.1 We eliminate the duplicates with DISTINCT

> Comment: *SELECT DISTINCT ?collection ?item: Adding DISTINCT ensures that each combination of ?collection and ?item in the result set is unique, thereby removing duplicates.*

```PREFIX arco-cd: <https://w3id.org/arco/ontology/context-description/>
PREFIX cis: <http://dati.beniculturali.it/cis/>
SELECT DISTINCT ?collection ?item
WHERE {
 ?collection a cis:CollectionCulEnt.
 ?collection arco-cd:isCollectionIn ?collectionmemb.
 ?collectionmemb arco-cd:hasMemberOfCollection ?item.
} LIMIT 100
```

2. We want to know which items are part of Collezione Marsili and Aldrovandi

> Comment: *We seperate the two collections.*

2.1 Collezione Marsili
```PREFIX arco-cd: <https://w3id.org/arco/ontology/context-description/>
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
2.2 Collezione Aldrovandi
```PREFIX arco-cd: <https://w3id.org/arco/ontology/context-description/>
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

3. We want to apply DISTINCT to eliminate the duplicates

3.1 DISTINCT for Collezione Marsili
```PREFIX arco-cd: <https://w3id.org/arco/ontology/context-description/> 
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
3.2 DISTINCT for Collezione Aldrovandi
```PREFIX arco-cd: <https://w3id.org/arco/ontology/context-description/> 
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

> Comment: *Now we have the raw basis for our project, as we were looking for cultural entity collections, we now have the items of the two collections of Collezione Marsili and Collezione Aldrovandi.*

# Start of the Project

