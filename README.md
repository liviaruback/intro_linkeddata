# Introduction to Linked Data and Graph Databases

## Download the [presentation](https://github.com/liviaruback/intro_linkeddata/raw/master/intro_linked_data.pdf)  (** atualizar versão final PDF**)

## References for Linked Data principles:
http://linkeddata.org/ <br>
https://www.w3.org/DesignIssues/LinkedData.html

## Practice - Part 1:
Go to the [DBPedia SPARQL endpoind](https://dbpedia.org/sparql).

Run the query above on the endpoint to get all universities around the world :mag:

`SELECT `<br>
  `&nbsp;&nbsp;?univ ?numPgs ?country ?city ?popCity<br>`<br>
`WHERE {`<br>
`  ?univ rdf:type <http://schema.org/CollegeOrUniversity>.  `<br>
`  ?univ <http://dbpedia.org/ontology/numberOfPostgraduateStudents> ?numPgs.`<br>
`  ?univ <http://dbpedia.org/property/country> ?country.`<br>
`  ?univ <http://dbpedia.org/ontology/city> ?city.`<br>
`  ?city <http://dbpedia.org/ontology/populationTotal> ?popCity`<br>
`}`<br>
`ORDER BY`<br> 
`  desc(?numPgs)`<br>

Check the results! :shipit:


<pre>
hello, this is
   just an     example
....
</pre>
