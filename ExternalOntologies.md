<img src="https://platform.socatel.eu/images/socatel-logo.png" alt="SoCaTelLogo" width="250" />

# **External Ontologies**

Given the diversity of the external data sources used in SoCaTel, it is highly probable that each type of source contains very specific information that cannot be easily mapped to concepts in SoCaTel's core ontology. Thus, we propose to extend the core ontology with additional, already-existing ontologies, each designed specifically for a different type of source. By doing so, the general data common to all external sources will be mapped to SoCaTel's core ontology while the more specific data will be mapped to the specific ontologies.

So far, the following external ontologies have been studied:

-   [DCAT (Open Data Sources)](ExternalOntologies.md#dcat-open-data-sources)
-   [SIOC (Social Media Sources)](ExternalOntologies.md#sioc-social-media-sources)
-   [SKOS](ExternalOntologies.md#skos)

## DCAT (Open Data Sources)

Data Catalog Vocabulary ([DCAT](https://www.w3.org/TR/vocab-dcat/)) is an RDF vocabulary designed to facilitate interoperability between data catalogs published on the Web. It is the recommended ontology to use when converting data from the CKAN standard to RDF format, as it includes an almost one-to-one mapping of CKAN concepts and properties.

[![UML model of DCAT classes and properties](https://www.w3.org/TR/vocab-dcat-1/dcat-model.jpg)](https://www.w3.org/TR/vocab-dcat-1/dcat-model.jpg)

_**Fig. 1: Main concepts and properties of the DCAT ontology.**_

## SIOC (Social Media Sources)

The Semantically-Interlinked Online Communities ([SIOC](http://rdfs.org/sioc/spec/)) ontology provides the main concepts and properties required to describe information from online communities and social networks (e.g., message boards, wikis, weblogs, etc.) in RDF format. The core ontology, depicted in Fig. 2 below, contains few mains classes that provide a general abstraction for the needed concepts. However, there are several extensions to this core ontology that provide more specific concepts, such as different sub-types of the Post and Container entities, that can be used in different cases.

As explained in  [SoCaTel Core Ontology](SoCaTelCoreOntology.md), we extended SIOC by defining the class _socatel:Page_  as a subclass of _sioc:Container_  in order to represent pages retrieved from the Facebook Data Handler.

  
  [![The main classes and properties in SIOC](http://rdfs.org/sioc/spec/img/main_classes_properties.png)](http://rdfs.org/sioc/spec/img/main_classes_properties.png)


## SKOS

The Simple Knowledge Organization System ([SKOS](https://www.w3.org/2004/02/skos/)) is an ontology developed to support the use of knowledge organization systems (KOS) such as thesauri, classification schemes, subject heading systems and taxonomies in RDF format. The ontology defines an extensive set of concepts and properties that allow the representation of a variety of relations between different concepts (e.g. equivalent, parent concept, broader concept, narrower concept, etc). At the moment, we only use _skos:Concept_  to define one or more topics for a specific data source, as exaplined  [here](SoCaTelCoreOntology.md). In the future, we should consider organizing the different topics in a _skos:ConceptScheme_  in order to more easily link different related topics together.