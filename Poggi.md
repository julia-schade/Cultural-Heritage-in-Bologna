# 2. Museo di Palazzo Poggi

Description HERE

#### 1. We defined the objects related to [Museo di Palazzo Poggi](https://w3id.org/arco/resource/CulturalInstituteOrSite/580641438d09beacdf6bea5446600063) and the properties of these relationships

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
SELECT DISTINCT * WHERE { ?object ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/580641438d09beacdf6bea5446600063> }
````
<table width="200" height="300">
  <tbody><tr>
    <th>object</th>
    <th>t</th>
  </tr>
  <tr>
    <td><a href="http://dati.beniculturali.it/mibact/luoghi/resource/CulturalInstituteOrSite/104569">http://dati.beniculturali.it/mibact/luoghi/resource/CulturalInstituteOrSite/104569</a></td>
    <td><a href="http://www.w3.org/2002/07/owl#sameAs">http://www.w3.org/2002/07/owl#sameAs</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/Site/f6bb041c26283b0c4af2edd0ed2caef6">https://w3id.org/arco/resource/Site/f6bb041c26283b0c4af2edd0ed2caef6</a></td>
    <td><a href="http://dati.beniculturali.it/cis/isSiteOf">http://dati.beniculturali.it/cis/isSiteOf</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688460">https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688460</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688431">https://w3id.org/arco/resource/NaturalHeritage/0800688431</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688432">https://w3id.org/arco/resource/NaturalHeritage/0800688432</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688433">https://w3id.org/arco/resource/NaturalHeritage/0800688433</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688434">https://w3id.org/arco/resource/NaturalHeritage/0800688434</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688435">https://w3id.org/arco/resource/NaturalHeritage/0800688435</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688436">https://w3id.org/arco/resource/NaturalHeritage/0800688436</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688437">https://w3id.org/arco/resource/NaturalHeritage/0800688437</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
</tbody></table>

#### 2. We used UNION in the previous query in order to link it to Aldrovandi collection

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/>

SELECT DISTINCT * WHERE {
  { 
    ?object ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/580641438d09beacdf6bea5446600063> 
  } 
  UNION 
  { 
    ?object arco:partOfCollection <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi> 
  }
}
````

<table width="200" height="300">
  <tbody><tr>
    <th>object</th>
    <th>t</th>
  </tr>
  <tr>
    <td><a href="http://dati.beniculturali.it/mibact/luoghi/resource/CulturalInstituteOrSite/104569">http://dati.beniculturali.it/mibact/luoghi/resource/CulturalInstituteOrSite/104569</a></td>
    <td><a href="http://www.w3.org/2002/07/owl#sameAs">http://www.w3.org/2002/07/owl#sameAs</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/Site/f6bb041c26283b0c4af2edd0ed2caef6">https://w3id.org/arco/resource/Site/f6bb041c26283b0c4af2edd0ed2caef6</a></td>
    <td><a href="http://dati.beniculturali.it/cis/isSiteOf">http://dati.beniculturali.it/cis/isSiteOf</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688460">https://w3id.org/arco/resource/DemoEthnoAnthropologicalHeritage/0800688460</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688431">https://w3id.org/arco/resource/NaturalHeritage/0800688431</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688432">https://w3id.org/arco/resource/NaturalHeritage/0800688432</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688433">https://w3id.org/arco/resource/NaturalHeritage/0800688433</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688434">https://w3id.org/arco/resource/NaturalHeritage/0800688434</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688435">https://w3id.org/arco/resource/NaturalHeritage/0800688435</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688436">https://w3id.org/arco/resource/NaturalHeritage/0800688436</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688437">https://w3id.org/arco/resource/NaturalHeritage/0800688437</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
</tbody></table>

#### 2.1 We use UNION in the previous query in order to link this query to Marsili collection


```SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
SELECT DISTINCT * WHERE { 
{ 
?object ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/580641438d09beacdf6bea5446600063> . 
?object a <https://w3id.org/arco/ontology/context-description/CollectionMembership> 
} 
UNION 
{
?object ?t <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili> . 
?object a <https://w3id.org/arco/ontology/context-description/CollectionMembership> 
} 
}
````
<table width="200" height="300">
  <tbody><tr>
    <th>object</th>
    <th>t</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691111-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691111-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691112-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691112-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691113-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691113-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691114-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691114-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691115-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691115-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691116-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691116-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691117-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691117-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691118-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691118-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691119-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691119-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691120-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691120-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
</tbody></table>
   







> 🧭
> - [Next ⏭](Scienze.md) 
> - [Previous ⏮](Project-Prep.md) 
> - [Home 🏠](index.md) 
