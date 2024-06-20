# Instituto delle Scienze

Description HERE

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
