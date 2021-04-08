@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix schema: <https://schema.org> .
@prefix dbo: <https://dbpedia.org/ontology> .
@prefix dbr: <https://dbpedia.org/resource/> .
@prefix owl: <http://www.w3.org/2002/07/owl#> .
@prefix yago-res: <https://yago-knowledge.org/resource/>.
@prefix juanda: <https://github.com/Fikrivent/semanticweb/blob/main/juanda/resource> .
@prefix jo: <https://github.com/Fikrivent/semanticweb/blob/main/juanda/predikat>.

juanda:arrivSchedule a rdfs:Class.
juanda:arrivSchedule rdfs:subClassof schema:Flight.

juanda:Garuda_Indonesia a schema:Organization;
	rdfs:label "Garuda Indonesia"@en;
	schema:name "Garuda Indonesia"^^xsd:text;
	owl:sameAs dbr:Garuda_Indonesia.

juanda:City_Link a schema:Organization;
	rdfs:label "City Link"@en;
	schema:name "City Link"^^xsd:text;
	owl:sameAs dbr:Citilink.

juanda:Lion_Air a schema:Organization;
	rdfs:label "Lion Air"@en;
	schema:name "Lion Air"^^xsd:text;
	owl:sameAs dbr:Lion_Air.

juanda:Jakarta a dbo:City;
	rdfs:label "Jakarta"@en;
	owl:sameAs yago-res:Jakarta.

juanda:Makassar a dbo:City;
	rdfs:label "Makassar"@en;
	rdfs:seeAlso dbr:Makassar.

juanda:Ambon a dbo:City;
	rdfs:label "Ambon"@en. 

juanda:Soekarno_Hatta a schema:Airport;
	schema:name "Soekarno - Hatta International Airport";
	schema:iatacode "CGK"^^xsd:text;
	rdfs:seeAlso dbr:Soekarno-Hatta_International_Airport.

juanda:Sultan_Hasanuddin a schema:Airport;
	schema:name "Sultan Hasanuddin International Airport";
	schema:iatacode "UPG"^^xsd:text;
	rdfs:seeAlso dbr:Sultan_Hasanuddin_International_Airport.

juanda:Pattimura a schema:Airport;
	schema:name "Pattimura International Airport";
	schema:iatacode "AMQ"^^xsd:text .

juanda:arrivalStatus a rdf:Property.
juanda:arrivalStatus rdfs:domain juanda:arrivSchedule.
juanda:arrivalStatus rdfs:range xsd:string.

juanda:FL_001 a juanda:arrivSchedule;
	schema:provider juanda:Garuda_Indonesia;
	juanda:departureAirport juanda:Soekarno_Hatta;
	schema:flightNumber "GA-306"^^xsd:text;
	schema:arrivalTime "2021-03-17 07:25:00"^^xsd:datetime;
	jo:arrivalStatus "SCHEDULED"^^xsd:string.

juanda:FL_002 a juanda:arrivSchedule;
	schema:provider juanda:City_Link;
	schema:departureAirport juanda:Sultan_Hasanuddin;
	schema:flightNumber "QG-714"^^xsd:text;
	schema:arrivalTime "2021-03-17 07:30:00"^^xsd:datetime;
	jo:arrivalStatus "SCHEDULED"^^xsd:string.

juanda:FL_003 a juanda:arrivSchedule;
	schema:provider juanda:Lion_Air;
	schema:departureAirport juanda:Pattimura;
	schema:flightNumber "JT-707"^^xsd:text;
	schema:arrivalTime "2021-03-17 13:20:00"^^xsd:datetime;
	jo:arrivalStatus "SCHEDULED"^^xsd:string.
