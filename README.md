# Introduction to Linked Data and Graph Databases

## Download the [presentation](https://github.com/liviaruback/intro_linkeddata/raw/master/intro_linked_data.pdf)  (** atualizar versão final PDF**)

## References for Linked Data principles:
http://linkeddata.org/ <br>
https://www.w3.org/DesignIssues/LinkedData.html

## Practice - Part 1:
Go to the [DBPedia SPARQL endpoind](https://dbpedia.org/sparql).

Run the query above on the endpoint to get all universities around the world :mag:

`SELECT ?univ ?numPgs ?country ?city ?popCity
WHERE {
  ?univ rdf:type <http://schema.org/CollegeOrUniversity>.  
  ?univ <http://dbpedia.org/ontology/numberOfPostgraduateStudents> ?numPgs.
  ?univ <http://dbpedia.org/property/country> ?country.
  ?univ <http://dbpedia.org/ontology/city> ?city.
  ?city <http://dbpedia.org/ontology/populationTotal> ?popCity
 }
ORDER BY desc(?numPgs)`

Check the results! :shipit:


