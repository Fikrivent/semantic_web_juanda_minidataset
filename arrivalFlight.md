@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix schema: <https://schema.org> .
@prefix dbo: <https://dbpedia.org/ontology> .
@prefix juanda: <https://github.com/Fikrivent/semanticweb/blob/main/juanda/resource> .
@prefix jo: <https://github.com/Fikrivent/semanticweb/blob/main/juanda/predikat>.

juanda:arrivSchedule a rdfs:Class.
juanda:arrivSchedule rdfs:subClassof schema:Flight.

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
