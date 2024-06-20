# 3. Museo della Specola

Description HERE

#### 1. We defined the objects related to [Museo della Specola](https://w3id.org/arco/resource/CulturalInstituteOrSite/746195e222fec1e6b02657ea1fdc6aae) and the properties of these relationships

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
SELECT DISTINCT * WHERE { ?object ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/746195e222fec1e6b02657ea1fdc6aae> }
````

<table width="200" height="300">
<tbody><tr>
    <th>object</th>
    <th>t</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/Site/27641117e6d58e7482a605fdf544a034">https://w3id.org/arco/resource/Site/27641117e6d58e7482a605fdf544a034</a></td>
    <td><a href="http://dati.beniculturali.it/cis/isSiteOf">http://dati.beniculturali.it/cis/isSiteOf</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/Site/fc764649c711774ab8859a0c3c7d4747">https://w3id.org/arco/resource/Site/fc764649c711774ab8859a0c3c7d4747</a></td>
    <td><a href="http://dati.beniculturali.it/cis/isSiteOf">http://dati.beniculturali.it/cis/isSiteOf</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688048-1">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688048-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688056">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688056</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688080">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688080</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688091">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688091</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688092">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688092</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688098">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688098</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688220">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688220</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688222">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688222</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite">https://w3id.org/arco/ontology/location/hasCulturalInstituteOrSite</a></td>
  </tr>
</tbody> </table>

#### 2. We ASKED if there are any objects related to Aldrovandi Collection in this museum

> 💡 We did the same for both Marsili Collections

```SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX a-cd: <https://w3id.org/arco/ontology/context-description/>
PREFIX a-loc: <https://w3id.org/arco/ontology/location/>

ASK {
  ?object rdf:type a-cd:CollectionMembership ;
          a-cd:hasCollection <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-aldrovandi> ;
          a-loc:hasCulturalInstituteOrSite <https://w3id.org/arco/resource/CulturalInstituteOrSite/746195e222fec1e6b02657ea1fdc6aae> .
}
````

<table width="50" height="50">
<body>false</body>
</table>

#### 3. We used UNION to isolate only items belonging to the categories "ScientificOrTechnologicalHeritage" and "HistoricOrArtisticProperty"

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/>  
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>  
SELECT DISTINCT ?object
WHERE {  
  { 
?object rdf:type arco:ScientificOrTechnologicalHeritage ;
               ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/746195e222fec1e6b02657ea1fdc6aae>  
  }
 
  UNION
 
  { 
    ?object rdf:type arco:HistoricOrArtisticProperty ;
               ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/746195e222fec1e6b02657ea1fdc6aae>  
  } 
}
````

<table width="200" height="300">
<tbody><tr>
    <th>object</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688048-1">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688048-1</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688056">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688056</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688080">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688080</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688091">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688091</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688092">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688092</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688098">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688098</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688220">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688220</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688222">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688222</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688223">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688223</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688224">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688224</a></td>
  </tr>
</tbody> </table>

#### 3.1 We COUNTED the results

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/>  
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>  
SELECT DISTINCT COUNT (?object) AS ?n
WHERE {  
  { 
?object rdf:type arco:ScientificOrTechnologicalHeritage ;
               ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/746195e222fec1e6b02657ea1fdc6aae>  
  }
 
  UNION
 
  { 
    ?object rdf:type arco:HistoricOrArtisticProperty ;
               ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/746195e222fec1e6b02657ea1fdc6aae>  
  } 
}
````

<table width="100" height="120">
<tbody><tr>
    <th>n</th>
  </tr>
  <tr>
    <td><pre>160</pre></td>
  </tr>
</tbody> </table>

#### 3.2 We used OPTIONAL to check if there are any depictions

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/> 
PREFIX foaf: <http://xmlns.com/foaf/0.1/> 
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> 
 
SELECT DISTINCT ?object ?depiction WHERE { 
  {
    ?object rdf:type arco:ScientificOrTechnologicalHeritage .
    ?object ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/746195e222fec1e6b02657ea1fdc6aae> .
  }
  UNION
  {
    ?object rdf:type arco:HistoricOrArtisticProperty .
    ?object ?t <https://w3id.org/arco/resource/CulturalInstituteOrSite/746195e222fec1e6b02657ea1fdc6aae> .
  }
  OPTIONAL { ?object foaf:depiction ?depiction }
}
````

<table width="200" height="300">
<tbody><tr>
    <th>object</th>
    <th>depiction</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688048-1">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688048-1</a></td>
    <td><a href="http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15383615_livella.jpg">http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15383615_livella.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688056">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688056</a></td>
    <td><a href="http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15375144_16.jpg">http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15375144_16.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688080">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688080</a></td>
    <td><a href="http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15400316_Radiotelescopio01.jpg">http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15400316_Radiotelescopio01.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688091">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688091</a></td>
    <td><a href="http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15410724_36.jpg">http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15410724_36.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688091">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688091</a></td>
    <td><a href="http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15410726_c494bd8e%2D50eb%2D42dc%2Dbc68%2D0be16bd0de5f.jpg">http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15410726_c494bd8e%2D50eb%2D42dc%2Dbc68%2D0be16bd0de5f.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688092">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688092</a></td>
    <td><a href="http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15413763_15.jpg">http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15413763_15.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688098">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688098</a></td>
    <td><a href="http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15417559_43.jpg">http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15417559_43.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688220">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688220</a></td>
    <td><a href="http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15408550_tr.jpg">http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15408550_tr.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688222">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688222</a></td>
    <td><a href="http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15407021_igrometro.jpg">http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15407021_igrometro.jpg</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688223">https://w3id.org/arco/resource/ScientificOrTechnologicalHeritage/0800688223</a></td>
    <td><a href="http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15407025_barometro.jpg">http://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15407025_barometro.jpg</a></td>
  </tr>
</tbody> </table>


<figure>
    <img src="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15410726_c494bd8e%2D50eb%2D42dc%2Dbc68%2D0be16bd0de5f.jpg"
         alt="specola1">
    <figcaption>Telescopio, rifrattore di Adams, George (terzo quarto XVIII) </figcaption>
    <img src="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15407021_igrometro.jpg"
         alt="specola2">
    <figcaption>Igrometro a capelli</figcaption>
     <img src="https://www.sigecweb.beniculturali.it/images/fullsize/ICCD1069318/ICCD15410720_pantografo.jpg"
         alt="specola3">
    <figcaption>Pantografo (seconda metà XIX sec)</figcaption>
</figure>




































> 🧭
> - [Next ⏭](Conclusion.md) 
> - [Previous ⏮](Scienze.md)
> - [Home 🏠](index.md) 
