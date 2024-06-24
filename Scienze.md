# Istituto delle Scienze

The Istituto delle Scienze, housed in Palazzo Poggi, is part of the Alma Mater Studiorum of Bologna. The foundation of the institute traces back to the 18th century, a period marked by significant advancements in scientific thought and education. 

#### Foundation and Early History 

The Istituto delle Scienze was founded in 1711 by Luigi Ferdinando Marsili, a scholar and naturalist, with the intention of fostering scientific research and education. Marsili, leveraging his own collection and connections, aimed to create a comprehensive center for scientific inquiry and learning. 

The institute initially focused on various fields including astronomy, physics, natural history, and anatomy. It played a pivotal role in advancing the scientific understanding of the time and was one of the earliest examples of a modern research institution. 

#### Development and influence 

Over the years, the Istituto delle Scienze expanded its collections and resources, incorporating extensive scientific apparatus, natural history specimens, and anatomical models. These collections were instrumental in both teaching and research. 

The institute became an integral part of the University of Bologna, contributing significantly to its reputation as a leading center for higher education and research in Europe. 

During the Enlightenment, the institute was at the forefront of scientific thought and innovation, attracting scholars and students from across Europe. It became a hub for the exchange of ideas and scientific collaboration. 

#### Modern Era 

Today, Palazzo Poggi remains a significant cultural and educational landmark. It houses various museums and collections that continue to reflect the institute’s historical contributions to science and knowledge. 

 The Istituto delle Scienze, as part of the Alma Mater Studiorum, continues to play a vital role in advancing scientific research and education, maintaining its legacy of excellence and innovation.  

#### 1. We defined the objects related to [Istituto delle Scienze](https://w3id.org/arco/resource/Site/a5e73b25845521559dceef201110b92e) and the properties of these relationships

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
SELECT DISTINCT * WHERE { ?object ?t <https://w3id.org/arco/resource/Site/a5e73b25845521559dceef201110b92e> }
````
<table width="200" height="300">
<tbody><tr>
    <th>object</th>
    <th>t</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063768-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063768-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063781-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063781-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063782-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063782-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063787-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063787-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063789-alternative-3">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063789-alternative-3</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063791-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063791-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063800-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063800-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063801-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063801-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063816-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063816-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063817-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063817-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
</tbody> </table>


#### 2. We applied UNION to the previous query in order to link it to Marsili collection

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/>  

SELECT DISTINCT *
WHERE {  
{  
?object ?t <https://w3id.org/arco/resource/Site/a5e73b25845521559dceef201110b92e>
}  

UNION  

{
?object ?t <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili>
} 
 } 
````
<table width="200" height="300">
<tbody><tr>
    <th>object</th>
    <th>t</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063768-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063768-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063781-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063781-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063782-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063782-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063787-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063787-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063789-alternative-3">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063789-alternative-3</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063791-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063791-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063800-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063800-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063801-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063801-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063816-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063816-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063817-alternative-1">https://w3id.org/arco/resource/TimeIndexedTypedLocation/0800063817-alternative-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/location/atSite">https://w3id.org/arco/ontology/location/atSite</a></td>
  </tr>
</tbody> </table>

#### 3. We isolated the DISTINCT items belonging to the category "CollectionMembership”
> 💡 We are going to do the same thing for both "Collezion<strong>e</strong> Marsili" and "Collezion<strong>i</strong> Marsili".

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/> 

SELECT DISTINCT *
WHERE {  
{  
?object ?t <https://w3id.org/arco/resource/Site/a5e73b25845521559dceef201110b92e> ;
              a <https://w3id.org/arco/ontology/context-description/CollectionMembership>  
}  

UNION  

{ 
?object ?t <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili> ;
              a <https://w3id.org/arco/ontology/context-description/CollectionMembership>  
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
</tbody> </table>

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/> 

SELECT DISTINCT *
WHERE {  
{  
?object ?t <https://w3id.org/arco/resource/Site/a5e73b25845521559dceef201110b92e> ;
              a <https://w3id.org/arco/ontology/context-description/CollectionMembership>  
}  

UNION  

{ 
?object ?t <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezioni-marsili> ;
              a <https://w3id.org/arco/ontology/context-description/CollectionMembership>  
}  

}
````

<table width="200" height="300">
<tbody><tr>
    <th>object</th>
    <th>t</th>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691143-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691143-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691144-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691144-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691145-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691145-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691146-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691146-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691148-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691148-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691149-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691149-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691150-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691150-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691151-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691151-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691152-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691152-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691153-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691153-collection-membership-1</a></td>
    <td><a href="https://w3id.org/arco/ontology/context-description/hasCollection">https://w3id.org/arco/ontology/context-description/hasCollection</a></td>
  </tr>
</tbody> </table>

#### 3.1 We COUNTED them all (69+36=105)
````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/> 

SELECT (COUNT(DISTINCT ?object) AS ?n) 
WHERE { 
{ 
?object ?t <https://w3id.org/arco/resource/Site/a5e73b25845521559dceef201110b92e> ;
             a <https://w3id.org/arco/ontology/context-description/CollectionMembership>  
} 

UNION 

{ 
?object ?t <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili> ; 
              a <https://w3id.org/arco/ontology/context-description/CollectionMembership>  
}  
} 
````
<table width="120" height="120">
  <tbody><tr>
    <th>n</th>
  </tr>
  <tr>
    <td><pre>69</pre></td>
  </tr>
</tbody>
</table>

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/> 

SELECT (COUNT(DISTINCT ?object) AS ?n) 
WHERE { 
{ 
?object ?t <https://w3id.org/arco/resource/Site/a5e73b25845521559dceef201110b92e> ;
             a <https://w3id.org/arco/ontology/context-description/CollectionMembership>  
} 

UNION 

{ 
?object ?t <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezioni-marsili> ; 
              a <https://w3id.org/arco/ontology/context-description/CollectionMembership>  
}  
} 
````
<table width="120" height="120">
  <tbody><tr>
    <th>n</th>
  </tr>
  <tr>
    <td><pre>36</pre></td>
  </tr>
</tbody>
</table>

#### 3.2 We added OPTIONAL to the queries to look for any existing related picture
````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/> 
PREFIX foaf: <http://xmlns.com/foaf/0.1/> 

SELECT DISTINCT ?object ?depiction 
WHERE {  
  {  
    ?object ?t <https://w3id.org/arco/resource/Site/a5e73b25845521559dceef201110b92e> ; 
                a <https://w3id.org/arco/ontology/context-description/CollectionMembership>  
  }  

  UNION  

  { 
    ?object ?t <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezione-marsili> ;
                  a <https://w3id.org/arco/ontology/context-description/CollectionMembership>  
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
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691111-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691111-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691112-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691112-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691113-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691113-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691114-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691114-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691115-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691115-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691116-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691116-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691117-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691117-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691118-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691118-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691119-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691119-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691120-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691120-collection-membership-1</a></td>
    <td></td>
  </tr>
</tbody>
</table>

````SPARQL
PREFIX arco: <https://w3id.org/arco/ontology/arco/> 
PREFIX foaf: <http://xmlns.com/foaf/0.1/> 

SELECT DISTINCT ?object ?depiction 
WHERE {  
  {  
    ?object ?t <https://w3id.org/arco/resource/Site/a5e73b25845521559dceef201110b92e> ; 
                a <https://w3id.org/arco/ontology/context-description/CollectionMembership>  
  }  

  UNION  

  { 
    ?object ?t <https://w3id.org/arco/resource/CollectionCulEnt/-bologna-collezioni-marsili> ;
                  a <https://w3id.org/arco/ontology/context-description/CollectionMembership>  
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
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691143-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691143-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691144-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691144-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691145-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691145-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691146-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691146-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691148-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691148-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691149-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691149-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691150-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691150-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691151-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691151-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691152-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691152-collection-membership-1</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://w3id.org/arco/resource/CollectionMembership/0800691153-collection-membership-1">https://w3id.org/arco/resource/CollectionMembership/0800691153-collection-membership-1</a></td>
    <td></td>
  </tr>
</tbody>
</table>


> 🧭
> - [Next ⏭](Specola.md) 
> - [Previous ⏮](Poggi.md) 
> - [Home 🏠](index.md) 
