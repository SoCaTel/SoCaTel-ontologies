<img src="https://platform.socatel.eu/images/socatel-logo.png" alt="SoCaTelLogo" width="250" />

# **Transformation Tools**

## LinkedPipes

[LinkedPipes](https://linkedpipes.com/) is a modular open source tool that offers the possibility to create ETL-like pipelines to transform data from various input formats into RDF. The tool offers a set of predefined components (e.g. CSV to RDF, SPARQL Endpoint Construct, etc) but the users can define their own components if needed. All components are offered by a REST API. LinkedPipes also includes several performance optimizations, especially in the transformation and loading processes.

**Input Formats**

-   CSV
-   JSON
-   XML

**Output Formats**

-   RDF files
-   Virtuoso
-   Graph store HTTP protocol

![ETL Pipeline](https://etl.linkedpipes.com/assets/snippets/pipeline.png)

**_Fig. 1:_ _Example transformation workflow in LinkedPipes. The example retrieves data from an external source using HTTP get, transforms the data into RDF using SPARQL Construct queries, stores the data into RDF files and then into Virtuoso. It also checks the file's metadata against external sources and separately stores it into Virtuoso as well._**

## Silk

[Silk](http://silkframework.org/) is an open source framework for integrating heterogeneous data sources. The main focus of Silk is to generate links between related data items within different Linked Data sources. The tool also offers the possibility to transform data from different formats into RDF, although the set of available transformations is more limited than other alternatives. Silk can be used either as a web application or from the command line with two main versions available: Silk Single Machine and Silk MapReduce.

**Input Formats**

-   CSV
-   XML
-   JSON
-   RDF

**Output Formats**

-   RDF store
-   CSV files

![](http://silkframework.org/assets/images/linkageRule.png)

**_Fig. 2:_ _Example entity linking workflow in Silk. The example loads data from two RDF datasets, applies two different similarity measures (Levenshtein distance and date comparison), and then combines the results of the two similarities to match the entities._**

## UnifiedViews

[UnifiedViews](https://unifiedviews.eu/) is an open source Extract-Transform-Load (ETL) framework that allows users to define, execute, monitor, and share RDF data processing tasks. It is part of the [PoolParty](https://www.poolparty.biz/) Semantic Suite, which is not open source itself. Similar to Silk, it is more focused on transformations and extensions made on data that is already in RDF and only offers a reduced set of components to transform data in other formats into RDF.

**I****nput Formats**

-   CSV
-   XML
-   RDF

**Output Formats**

-   RDF store

![Unified views flowchart image](https://www.poolparty.biz/wp-content/uploads/2018/08/PoolParty-UnifiedViews-7.0.png)

**_Fig. 3:_ _Example transformation workflow in UnifiedViews. The example loads data from an SQL database, converts it to RDF using SPARQL Construct queries, validates the data and then stores it into Virtuoso._**
