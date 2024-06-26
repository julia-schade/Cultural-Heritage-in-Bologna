# Museo di Palazzo Poggi

The Museo di Palazzo Poggi, nestled in the historic heart of Bologna, is a testament to the city’s rich intellectual and cultural heritage. The museum is housed in the Palazzo Poggi and features a diverse range of collections that reflect the university's rich history and contributions to various fields of knowledge. Exhibits include displays on natural history, anatomy, obstetrics, physics, military architecture, and astronomy, showcasing the scientific and academic advancements made by the university over the centuries 
Today, the museum's collections provide a window into the pioneering spirit of Bologna's scholars. 

#### Collezione Aldrovandi
The Collezione Aldrovandi, assembled by the eminent naturalist Ulisse Aldrovandi, includes an extensive range of botanical, zoological, and geological specimens. Aldrovandi’s meticulous work laid the foundation for modern natural history.

#### Collezione Marsili
The Collezione Marsili, curated by Luigi Ferdinando Marsili, features an array of scientific instruments, models, and manuscripts. Marsili, a distinguished scientist and soldier, contributed significantly to the advancement of knowledge in fields such as physics, astronomy, and anatomy.

#### Overview
The Museo di Palazzo Poggi not only preserves these invaluable collections but also celebrates the ongoing legacy of scientific inquiry and discovery at the University of Bologna. Visitors can explore the museum's rich exhibits, gaining insights into the history of science and the enduring impact of Bologna's academic tradition.


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

#### 3. We isolated only items belonging to the category "NaturalHeritage”

```SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
SELECT DISTINCT ?object WHERE {
  {
    ?object ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/580641438d09beacdf6bea5446600063> 
  } 
  UNION 
  { 
    ?object arco:partOfCollection <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi> 
  }
  ?object a <https://w3id.org/arco/ontology/arco/NaturalHeritage> .
}
````

<table width="200" height="300">
  <tbody><tr>
    <th>object</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688431">https://w3id.org/arco/resource/NaturalHeritage/0800688431</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688432">https://w3id.org/arco/resource/NaturalHeritage/0800688432</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688433">https://w3id.org/arco/resource/NaturalHeritage/0800688433</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688434">https://w3id.org/arco/resource/NaturalHeritage/0800688434</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688435">https://w3id.org/arco/resource/NaturalHeritage/0800688435</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688436">https://w3id.org/arco/resource/NaturalHeritage/0800688436</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688437">https://w3id.org/arco/resource/NaturalHeritage/0800688437</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688438">https://w3id.org/arco/resource/NaturalHeritage/0800688438</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688439">https://w3id.org/arco/resource/NaturalHeritage/0800688439</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688440">https://w3id.org/arco/resource/NaturalHeritage/0800688440</a></td>
  </tr>
</tbody> </table>
   
#### 3.1 We COUNTed the results 

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
SELECT (COUNT(DISTINCT ?object) AS ?count) WHERE {
  {
    ?object ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/580641438d09beacdf6bea5446600063> 
  } 
  UNION 
  { 
    ?object arco:partOfCollection <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi> 
  }
  ?object a <https://w3id.org/arco/ontology/arco/NaturalHeritage> .
}
````

<table width="100" height="120">
<tbody><tr>
    <th>count</th>
  </tr>
  <tr>
    <td><pre>94</pre></td>
  </tr>
</tbody> </table>

#### 3.2 We used OPTIONAL to check if there are any depictions

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX foaf: <http://xmlns.com/foaf/0.1/>

SELECT DISTINCT ?object ?depiction WHERE {
  {
    ?object ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/580641438d09beacdf6bea5446600063> 
  } 
  UNION 
  { 
    ?object arco:partOfCollection <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi> 
  }
  ?object a <https://w3id.org/arco/ontology/arco/NaturalHeritage> .
  OPTIONAL { ?object foaf:depiction ?depiction }
}
````

<table width="200" height="300">
<tbody><tr>
    <th>object</th>
    <th>depiction</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688431">https://w3id.org/arco/resource/NaturalHeritage/0800688431</a></td>
    <td><a href="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935804_MPPAL105.jpg">https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935804_MPPAL105.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688431">https://w3id.org/arco/resource/NaturalHeritage/0800688431</a></td>
    <td><a href="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935809_MPPAL105a.jpg">https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935809_MPPAL105a.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688432">https://w3id.org/arco/resource/NaturalHeritage/0800688432</a></td>
    <td><a href="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935830_MPPAL107.jpg">https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935830_MPPAL107.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688432">https://w3id.org/arco/resource/NaturalHeritage/0800688432</a></td>
    <td><a href="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935833_MPPAL107a.jpg">https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935833_MPPAL107a.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688433">https://w3id.org/arco/resource/NaturalHeritage/0800688433</a></td>
    <td><a href="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935861_MPPAL108.jpg">https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935861_MPPAL108.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688433">https://w3id.org/arco/resource/NaturalHeritage/0800688433</a></td>
    <td><a href="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935863_MPPAL108a.jpg">https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935863_MPPAL108a.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688433">https://w3id.org/arco/resource/NaturalHeritage/0800688433</a></td>
    <td><a href="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935867_MPPAL108b.jpg">https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935867_MPPAL108b.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688433">https://w3id.org/arco/resource/NaturalHeritage/0800688433</a></td>
    <td><a href="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935868_MPPAL108c.jpg">https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935868_MPPAL108c.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688433">https://w3id.org/arco/resource/NaturalHeritage/0800688433</a></td>
    <td><a href="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935869_MPPAL108d.jpg">https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935869_MPPAL108d.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/NaturalHeritage/0800688433">https://w3id.org/arco/resource/NaturalHeritage/0800688433</a></td>
    <td><a href="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935872_MPPAL108e.jpg">https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935872_MPPAL108e.jpg</a></td>
  </tr>
</tbody> </table>

<br />
<br />

#### Examples for Objects

<table width="130%">
  <tbody>
    <tr>
      <th>Picture</th>
      <th>Description</th>
    </tr>
    <tr>
      <td>
        <img src="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935861_MPPAL108.jpg" alt="sassi1" width="475">
      </td>
      <td>Sfere di calcari e marmi policromi</td>
    </tr>
    <tr>
      <td>
        <img src="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15935947_MPPAL114.jpg" alt="sassi2" width="475">
      </td>
      <td>Terre sigillate</td>
    </tr>
    <tr>
      <td>
        <img src="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1070354/ICCD15938032_MPPAL174a.jpg" alt="sassi3" width="475">
      </td>
      <td>Fossile (riccio di mare)</td>
    </tr>
  </tbody>
</table>





> 🧭
> - [Next ⏭](Istituto-Delle-Scienze.md) 
> - [Previous ⏮](Project-Prep.md) 
> - [Home 🏠](index.md) 
