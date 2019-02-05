# Introduction to Linked Data and SPARQL by Lívia Ruback

## Download the [presentation](https://github.com/liviaruback/intro_linkeddata/raw/master/intro_linked_data.pdf)  (atualizar versão final)

## References for Linked Data:
[Linked Data - Design Issues](https://www.w3.org/DesignIssues/LinkedData.html)<br>
[The Linked Open Data cloud](https://lod-cloud.net/)

## Practice 

1) Take a look in the Stanford University entry in DBPedia (RDF version of wikipedia)

Go to the [Stanford entry on dbpedia](http://dbpedia.org/resource/Stanford_University)

Check the results! :mag:


2) Give me all the properties about Stanford University

Go to the [DBPedia SPARQL endpoind](https://dbpedia.org/sparql) :link:.

Copy and paste the following SPARQL query:

```sparql
SELECT ?p ?o
WHERE{ 
  <http://dbpedia.org/resource/Stanford_University> ?p ?o
}

```
Check the results! :mag:


```sparql
SELECT 
   ?univ ?numPgs ?country ?city ?popCity
WHERE {
   ?univ rdf:type <http://schema.org/CollegeOrUniversity>.  
   ?univ <http://dbpedia.org/ontology/numberOfPostgraduateStudents> ?numPgs.
   ?univ <http://dbpedia.org/property/country> ?country.
   ?univ <http://dbpedia.org/ontology/city> ?city.
   ?city <http://dbpedia.org/ontology/populationTotal> ?popCity
 }
ORDER BY 
   desc(?numPgs)
```




