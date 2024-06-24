# Palazzo Poggi

Palazzo Poggi was built in the 16th century based on a design by Pellegrino Tibaldi, who also created some of the interior frescoes, and it is located in the heart of the university area and has been the main headquarters of the University of Bologna since 1803.

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
