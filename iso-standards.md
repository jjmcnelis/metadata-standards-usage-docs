# International Standards Organization ([ISO](https://www.iso.org))

ISO metadata was created using the [Unified Modeling Language (UML)](https://www.uml.org/), a standardized general purpose modeling language often used in software engineering. Through its companion Technical Specification (ISO 19139), the ISO metadata standard is represented in a consistent Extensible Markup Language (XML) format for use worldwide. As such, the ISO data model is more easily, and consistently, reproduced within software applications that support metadata creation and content validation.

(source: [Federal Geographic Data Commission](https://www.fgdc.gov/metadata/iso-standards))

## ISO 191xx Geospatial Metadata Standards

**See the UML (content) and XML (encoding) standards in the tables on this page:**

https://www.fgdc.gov/metadata/iso-suite-of-geospatial-metadata-standards

### [ISO 19115](https://www.iso.org/standard/53798.html)

An internationally-adopted schema for describing geographic information and services. It provides information about the identification, the extent, the quality, the spatial and temporal schema, spatial reference, and distribution of digital geographic data.

(source: [Data Curation Center](http://www.dcc.ac.uk/resources/metadata-standards/iso-19115))

The first edition of ISO 19115 was published in 2003. It has since been split into parts:

* [ISO 19115/-1](https://standards.iso.org/iso/19115/): contains the fundamentals of the standard; developed to document vector and point data and geospatial data services like web-mapping applications, data catalogs, and data modeling applications.
* [ISO 19115-2](https://standards.iso.org/iso/19115/-2): contains extensions for imagery and gridded data, as well as data collected using instruments, e.g. monitoring stations and measurement devices.
* [ISO/TS 19115-3](https://standards.iso.org/iso/19115/-3): provides an XML schema implementation for the fundamental concepts compatible with ISO/TS 19139:2007 (Geographic Metadata XML, or GMD).
  * [ISO/CD TS 19139](https://schemas.wmo.int/wmdr/1.0RC4/documentation/schemadoc/namespaces/http_www_isotc211_org_2005_gmd/namespace-overview.html): Geographic information — Metadata — XML schema implementation enables interoperable XML expression of ISO19115 compliant metadata.
([source](https://www.fgdc.gov/metadata/selecting-a-geospatial-metadata-standard))

Compatibility:

* [NASA Common Metadata Repository](https://github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/data-metadata-org/cmr.md)

### [ISO 19110](https://www.iso.org/standard/57303.html)

[ISO 19110](https://standards.iso.org/iso/19110) specifies how feature types can be organized into a feature catalogue and presented to the users of a set of geographic data. Compliant feature types can be referenced or incorporated into a 19115-1 record.
