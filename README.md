# Text Graph Ontology

This ontology is aimed at representing a genetic text graph. A converter for TEI-Data to tgo is provided.

## Namespaces

| Prefix | Namespace                                     |
| ------ | --------------------------------------------- |
| rdf    | <http://www.w3.org/1999/02/22-rdf-syntax-ns#> |
| rdfs   | <http://www.w3.org/2000/01/rdf-schema#>       |
| tgo    | <http://www.hinkelmanns.at/tgo/>              |
| xml    | <http://www.w3.org/XML/1998/namespace>        |
| xsd    | <http://www.w3.org/2001/XMLSchema#>           |

```turtle
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix tgo: <http://www.hinkelmanns.at/tgo/> .
@prefix xml: <http://www.w3.org/XML/1998/namespace> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<http://www.hinkelmanns.at/objects/10b1db37-9763-4209-ba41-ce91e99212e5> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s11> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s6> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/29fca215-ad79-4775-a510-4e82b56cae29> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s3> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s1> ;
    tgo:weight "1" .

<http://www.hinkelmanns.at/objects/2b95ef80-b978-4c11-9dc6-19926bd5926f> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s9> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s8> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/507a44b3-bf29-497d-92a0-4c5f1b3c4cc1> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s6> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s5> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/61ef1a30-a26e-4ad4-85cc-b513a16948f7> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s12> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s11> ;
    tgo:weight "1" .

<http://www.hinkelmanns.at/objects/9a96417a-4b35-4f39-accd-5e265b072cd1> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s1> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/cc4fa6bf-dae7-407f-83ae-4ded9fe843a3> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/9c5cf32e-7d68-4ec4-9ad3-f41a7f0ab35a> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s7> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s3> ;
    tgo:weight "2" .

<http://www.hinkelmanns.at/objects/a195a4ec-d47f-4ba3-890e-340f88943ee7> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s4> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s3> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/a567de95-82a7-43b6-973a-5299ba8ecacb> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s3> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s2> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/a66c1f57-df1e-48c0-bc90-56f3e2eb8047> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s6> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s4> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/abbdc068-728e-4d46-99bc-0c4ec38009cc> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/f968cd00-232f-409e-8d88-adce909fb887> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s12> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/c16043c3-7181-477e-bd7b-04a9b341dbad> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s8> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s7> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/d1c72570-d768-4efc-8264-4ca8bf543e6c> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/10eee873-2a14-4c91-83fe-491105d0e447> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s11> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/e49cda8d-dec6-4742-9bb3-0d13a0f745b9> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s11> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s10> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/e4ff874f-d28b-45d9-bb3e-8d1a11a3760a> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s2> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s1> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/facb9810-ddad-4f22-923a-158a3223f04f> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s5> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s3> ;
    tgo:weight "1" .

<http://www.hinkelmanns.at/objects/fd80d157-d018-4ac3-9754-539faac70670> a tgo:Connector ;
    tgo:hasEnd <http://www.hinkelmanns.at/objects/s10> ;
    tgo:hasStart <http://www.hinkelmanns.at/objects/s9> ;
    tgo:weight "0" .

<http://www.hinkelmanns.at/objects/10eee873-2a14-4c91-83fe-491105d0e447> a tgo:End .

<http://www.hinkelmanns.at/objects/cc4fa6bf-dae7-407f-83ae-4ded9fe843a3> a tgo:Start .

<http://www.hinkelmanns.at/objects/f968cd00-232f-409e-8d88-adce909fb887> a tgo:End .

<http://www.hinkelmanns.at/objects/s10> a tgo:Token ;
    rdfs:label "diam" .

<http://www.hinkelmanns.at/objects/s12> a tgo:Token ;
    rdfs:label "eirmod" .

<http://www.hinkelmanns.at/objects/s2> a tgo:Token ;
    rdfs:label "ipsum" .

<http://www.hinkelmanns.at/objects/s4> a tgo:Token ;
    rdfs:label "sit" .

<http://www.hinkelmanns.at/objects/s5> a tgo:Token ;
    rdfs:label "amet" .

<http://www.hinkelmanns.at/objects/s7> a tgo:Token ;
    rdfs:label "sadipscing" .

<http://www.hinkelmanns.at/objects/s8> a tgo:Token ;
    rdfs:label "elitr" .

<http://www.hinkelmanns.at/objects/s9> a tgo:Token ;
    rdfs:label "sed" .

<http://www.hinkelmanns.at/objects/s1> a tgo:Token ;
    rdfs:label "Lorem" .

<http://www.hinkelmanns.at/objects/s6> a tgo:Token ;
    rdfs:label "consetetur" .

<http://www.hinkelmanns.at/objects/s11> a tgo:Token ;
    rdfs:label "nonumy" .

<http://www.hinkelmanns.at/objects/s3> a tgo:Token ;
    rdfs:label "dolor" .
```

## Classes

### tgo:Node

All nodes of the text graph

### tgo:End

An end point for a token graph.

Subclass of tgo:Node

### tgo:Token

A Token is the base unit of a Text. Token in this regard doesn't refere to a specific layer of text (word, sentence...).

Subclass of tgo:Node

### tgo:Start

A start point for a token graph.

Subclass of tgo:Node

### tgo:Connector

A connector represents the relation between two or more nodes.

### tgo:Path

A Path is a route through the text with a given start, end and waypoints

Subclass of tgo:Connector

## Properties

### tgo:hasWaypoint

hasWaypoint connects a Path with a Node

Domains: tgo:Path

Ranges: tgo:Node

### tgo:hasEnd

hasEnd connects a Connector with its ending node

Domains: tgo:Connector

Ranges: tgo:Node

Subclass of tgo:hasWaypoint

### tgo:hasStart

hasStart connects a Connector with its starting node

Domains: tgo:Connector

Ranges: tgo:Node

Subclass of tgo:hasWaypoint

## Data Properties

### tgo:weight

A weight of a connections is interpreted relative to the other connections starting from the same token.
I.e. if a token has two connections with weight 1 and 2, the connection with weight 1 precedes the connection with weight 2.

Domains: tgo:Connector

Ranges: xsd:int

