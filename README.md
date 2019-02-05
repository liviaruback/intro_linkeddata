# Introduction to Linked Data and SPARQL by Lívia Ruback

## Download the [presentation](https://github.com/liviaruback/intro_linkeddata/raw/master/intro_linked_data.pdf)  

## References for Linked Data:
[Linked Data - Design Issues](https://www.w3.org/DesignIssues/LinkedData.html)<br>
[The Linked Open Data cloud](https://lod-cloud.net/)

## Practice 

### 1) Take a look in the Stanford University entry in DBPedia (RDF version of wikipedia)

Go to the [Stanford entry on dbpedia](http://dbpedia.org/resource/Stanford_University)

Check the results! :mag:


### 2) Give me all the properties about Stanford University

Go to the [DBPedia SPARQL endpoind](https://dbpedia.org/sparql) :link:.

Copy and paste the following SPARQL query:

```sparql
SELECT ?p ?o
WHERE{ 
  <http://dbpedia.org/resource/Stanford_University> ?p ?o
}

```
Check the results! :mag:


### 3) How many universities are in the world?

Go to the [DBPedia SPARQL endpoind](https://dbpedia.org/sparql) :link:.

Copy and paste the following SPARQL query:

```sparql
SELECT (COUNT(?univ) AS ?count)
WHERE {
   ?univ rdf:type <http://dbpedia.org/ontology/University>.     
}

```
Check the results! :mag:

### 4) Give me the universities with more than 20k postgraduate students


Go to the [DBPedia SPARQL endpoind](https://dbpedia.org/sparql) :link:.

Copy and paste the following SPARQL query:

```sparql
SELECT 
   ?univ ?numPgs 
WHERE {
   ?univ rdf:type <http://dbpedia.org/ontology/University>.  
   ?univ <http://dbpedia.org/ontology/numberOfPostgraduateStudents> ?numPgs.
   FILTER (?numPgs > 20000) 
 }
ORDER BY 
   desc(?numPgs)
```
Check the results! :mag:


### Other SPARQL queries:

Give me the universities in the United States

```sparql
SELECT ?univ 
WHERE {
   ?univ rdf:type <http://dbpedia.org/ontology/University>.
   ?univ <http://dbpedia.org/property/country> "United States"^^<http://www.w3.org/1999/02/22-rdf-syntax-ns#langString>.   
}
```

Give me the universities in the city of Paris

```sparql
SELECT ?univ 
WHERE {
   ?univ rdf:type <http://dbpedia.org/ontology/University>.
   ?univ <http://dbpedia.org/ontology/city> <http://dbpedia.org/resource/Paris>.   
}
```


