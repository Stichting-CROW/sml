# SML Part 1 & 2

> Semantic modelling and linking (SML) - Part 1: Generic modelling patterns
> Semantic modelling and linking (SML) - Part 2: Domain-specific modelling patterns 

```sparql
prefix sml-term: <https://w3id.org/sml/term#> .
prefix sml: <https://w3id.org/sml/def#> .
```

| file                                                | contains                                                                   | bevat                                                                                       |
|-----------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
|                                                     | **Normative files**                                                        | **Normatieve bestanden**                                                                    |
| [Terms (SKOS)](/data/sml-skos.ttl)                  | Defines the terms from NEN 2660-2:2022 as <code>skos:Concept</code>s.      | Definieert de termen uit NEN 2660-2:2022 als <code>skos:Concept</code>en.                   |
| [Classes and Properties (RDFS)](/data/sml-rdfs.ttl) | Defines RDFS classes and properties related to each SKOS term.             | Definieert de termen als RDFS-klassen en RDF-eigenschappen, gerelateerd aan de SKOS-termen. |
| [Classes and Properties (OWL)](/data/sml-owl.ttl)   | Defines OWL class and property types for the definitions in the RDFS file. | Breidt de RDFS-definities uit met OWL-klasse- en -eigenschapbepalingen.                     |
| [Shapes (SHACL)](/data/sml-shacl.ttl)               | Defines SHACL shapes for the classes and properties in the RDFS file.      | Breidt de RDFS-definities uit met SHACL-beperkingen.                                        |
|                                                     | **Concatenated files**                                                     | **Samengevoegde bestanden**                                                                 |
| [TriG](/data/concat/sml.trig)                       | As TriG (seperates normative files as named graphs)                        | Als TriG (scheidt normatieve bestanden als benoemde grafen)                                 |
| [JSON-LD](/data/concat/sml.json)                    | As JSON-LD                                                                 | Als JSON-LD                                                                                 |
| [Turtle](/data/concat/sml.ttl)                      | As Turtle                                                                  | Als Turtle                                                                                  |
| [RDF/XML](/data/concat/sml.rdf)                     | As RDF/XML                                                                 | Als RDF/XML                                                                                 |
