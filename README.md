# DPP

<p align="center">
    <a href="../images/rdf/DPP_creatine.png" target="_blank">
        <img src="../images/rdf/DPP_creatine.png">
    </a>
</p>

### Example RDF (turtle)
```ttl
@prefix : <http://w3id.org/bind/data/v1/example-rdf/> .
@prefix obo: <http://purl.obolibrary.org/obo/> .
@prefix sio: <http://semanticscience.org/resource/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

:identifier_ a sio:SIO_000115, obo:IAO_0020000 ;
    rdfs:label "Identifier"^^xsd:string ;
    sio:SIO_000020 :role_ ;
    sio:SIO_000300 "Patient 1"^^xsd:string .

:person_ a sio:SIO_000498, obo:NCBITaxon_9606 ;
    rdfs:label "Entity: Person"^^xsd:string ;
    sio:SIO_000228 :role_ ;
    sio:SIO_000008 :age_ .

:age_ a sio:SIO_001013, obo:PATO_0000011; 
    rdfs:label "Age"^^xsd:string ;
    sio:SIO_000300 "26"^^xsd:integer .

:facility_ a sio:SIO_000688, obo:NCIT_C21541;
    rdfs:label "Facility: LUMC"^^xsd:string .
    
:role_ a obo:OBI_0000093, sio:SIO_000016 ;
    rdfs:label "Role: Patient"^^xsd:string ;
    sio:SIO_000061 :facility_ ;
    sio:SIO_000356 :creatine_process_ .

:study_id_ a sio:SIO_000115; 
    rdfs:label "Study ID"^^xsd:string ;
    sio:SIO_000300 "Study 1"^^xsd:string ;
    sio:SIO_000001 :role_ .
    
:creatine_process_ a obo:OBI_0003194, sio:SIO_000006 ;
    rdfs:label "Process: Creatine Meassurement"^^xsd:string ;
    sio:SIO_000291 :creatine_ ;
    sio:SIO_000229 :creatine_levels_ ;
    sio:SIO_000230 :sample_ .

:sample_ a sio:SIO_010412,  obo:UBERON_0001977;
    rdfs:label "Input: Sample"^^xsd:string.
    
:creatine_levels_ a sio:SIO_000015, obo:NCIT_C93940 ;
    rdfs:label "Outout: Creatine Levels"^^xsd:string ;
    sio:SIO_000221 :unit_ ;
    sio:SIO_000300 "94.8"^^xsd:string .

:unit_ a sio:SIO_000074, obo:UO_0000039;
    rdfs:label "Unit: Micromol"^^xsd:string.
    
:creatine_ a sio:SIO_010043, obo:CHEBI_16919; 
    sio:SIO_000300 "Target: Creatine"^^xsd:string .
```
