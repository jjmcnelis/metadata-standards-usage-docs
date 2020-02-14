# EML ([Ecological Metadata Language](https://eml.ecoinformatics.org/))

>"Ecological Metadata Language (EML) is a metadata specification developed by the ecology discipline and for the ecology discipline. It is based on prior work done by the Ecological Society of America and associated efforts (Michener et al., 1997, Ecological Applications). EML is implemented as a series of XML document types that can by used in a modular and extensible manner to document ecological data. Each EML module is designed to describe one logical part of the total metadata that should be included with any ecological dataset."

(source: [Digital Curation Center](http://www.dcc.ac.uk/resources/metadata-standards/eml-ecological-metadata-language))

The [EML specification](http://knb.ecoinformatics.org/software/eml/eml-2.1.1/index.html) (currently on version 2.2.0) is mapped to [ISO 19139 (XML Schema for ISO 19115)](https://www.iso.org/standard/67253.html)

EML is extended by the [GBIF (Global Biodiversity Information Facility) Profile](https://www.gbif.org/standards) standards. It's XML Schema Document can be found [here](http://rs.gbif.org/schema/eml-gbif-profile/dev/eml-gbif-profile.xsd).

## schema (https://eml.ecoinformatics.org/eml-schema.html)

EML is defined by a set of XML Schema files that define the types and structure of a valid EML document. The schema that pertain to file level metadata are likely defined through these core modules:

* eml: top level metadata structure/container
* eml-resource: base information for all data (and other) objects
* eml-dataset: general information describing dataset resources
* **[eml-entity](https://eml.ecoinformatics.org/schema/eml-entity_xsd.html#eml-entity.xsd)**: logical characteristics of each entity in a dataset (data structure)
* **[eml-attribute](https://eml.ecoinformatics.org/schema/eml-attribute_xsd.html#eml-attribute.xsd)**: attribute level information within dataset entities
* eml-spatialVector, eml-spatialRaster, etc.

EML *entity* and *attribute* submodules are probably where a file level metadata standard is implemented.

## users

[EDI: Environmental Data Initiative](https://environmentaldatainitiative.org/) *(deliverable)*

[KNB: Knowledge Network for Biocomplexity](http://knb.ecoinformatics.org/informatics/index.jsp) *(deliverable)*

[Long-Term Ecological Research (LTER) Network](https://lternet.edu/)

[National Center for Ecological Analysis and Synthesis](https://www.nceas.ucsb.edu/)

[DataONE](https://www.dataone.org/)

## citations

Ecological Metadata Language:

```
Jones, M., O’Brien, M., Mecum, B., Boettiger, C., Schildhauer, M., Maier, M., Whiteaker, T., Earl, S., and Chong, S. 2019. Ecological Metadata Language version 2.2.0. KNB Data Repository (https://eml.ecoinformatics.org). DOI: 10.5063/f11834t2
```

Michener et al. 1997:

```
William K. Michener, James W. Brunt, John J. Helly, Thomas B. Kirchner and Susan G. Stafford. *Ecological Applications*. Vol. 7, No. 1 (Feb., 1997), pp. 330-342
```

## links

interactive schema: https://eml.ecoinformatics.org/schema/eml-resource_xsd.html

tool: [metacat](http://knb.ecoinformatics.org/knb/docs/)

portal: [morpho](http://knb.ecoinformatics.org/morphoportal.jsp)
