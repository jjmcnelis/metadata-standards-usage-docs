# Knowledge Network for Biocomplexity: ([KNB](http://knb.ecoinformatics.org/informatics/index.jsp/))

KNB data management software is developed in a free and open source manner, so other groups can build upon the tools. It is a [DataONE](https://dataone.org) member node.

The KNB is powered by the [Metacat data management system](https://www.dataone.org/software-tools/metacat), and is optimized for handling data sets described using the [Ecological Metadata Language](https://github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/eml.md), but can store any XML-based metadata document.

Data are exposed through the KNB Data Portal ([Metacat UI](https://github.com/NCEAS/metacatui)): https://knb.ecoinformatics.org/data

## example 1 ([EML](https://www.github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/eml-specification.md))

* **DATASET**: https://knb.ecoinformatics.org/view/urn:uuid:045c9be0-7a5a-4c01-b010-529dc21aee79
* **CITATION**:

>```
>Susan Natali, Alexander Kholodov, and Michael Loranty. 2016. Thaw depth and organic layer depth from Alaska borehole sites, 2015, 2017, 2018 (ViPER Project). Arctic Data Center. urn:uuid:045c9be0-7a5a-4c01-b010-529dc21aee79. 
>```

* **FILE**: *ViPER_Coordinates_2015.csv* (no access)
* **METADATA**: EML v2.1.1 ([XML](https://github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/specifications/orgs/knb/Dataset_for_Trade_off_between_early_.xml)) 

### XML: *eml-entity:* file level metadata fields

This is the *eml-entity* from the larger *eml-dataset* record linked [here](https://github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/specifications/orgs/knb/Dataset_for_Trade_off_between_early_.xml):

```xml
<?xml version="1.0" encoding="UTF-8"?>
<dataTable id="urn-uuid-2c1be479-e402-4a53-b7bf-d0bb31385b3f">
  <entityName>ViPER_Coordinates_2015.csv</entityName>
  <entityDescription>Location of Study</entityDescription>
  <attributeList>
    <attribute>
      <attributeName>Site</attributeName>
      <attributeLabel>Site</attributeLabel>
      <attributeDefinition>Site number, values are one through twenty four</attributeDefinition>
      <storageType>integer</storageType>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>dimensionless</standardUnit>
          </unit>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
    </attribute>
    <attribute>
      <attributeName>Transect</attributeName>
      <attributeLabel>Transect</attributeLabel>
      <attributeDefinition>Three twenty meter long transects were conducted per site</attributeDefinition>
      <storageType>integer</storageType>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>dimensionless</standardUnit>
          </unit>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
    </attribute>
    <attribute>
      <attributeName>Location</attributeName>
      <attributeLabel>Location</attributeLabel>
      <attributeDefinition>Thaw depth samples were taken along 20m transects. Values represent the beginning and ending of the transects.</attributeDefinition>
      <storageType>integer</storageType>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>dimensionless</standardUnit>
          </unit>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
    </attribute>
    <attribute>
      <attributeName>Lat</attributeName>
      <attributeLabel>Latitude</attributeLabel>
      <attributeDefinition>Latitudinal Coordinate</attributeDefinition>
      <storageType>integer</storageType>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>degree</standardUnit>
          </unit>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
    </attribute>
    <attribute>
      <attributeName>Long</attributeName>
      <attributeLabel>Longitude</attributeLabel>
      <attributeDefinition>Longitude Coordinate</attributeDefinition>
      <storageType>integer</storageType>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>degree</standardUnit>
          </unit>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
    </attribute>
  </attributeList>
</dataTable>
```

## example 2 ([EML](https://www.github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/eml-specification.md))

* **DATASET**: https://knb.ecoinformatics.org/view/doi:10.5063/F17W69K6
* **CITATION**:

>```
>Joseph Waterton and Elsa Cleland. 2016. Dataset for "Trade-off between early emergence and herbivore susceptibility mediates exotic success in an experimental California plantcommunity". Knowledge Network for Biocomplexity. doi:10.5063/F17W69K6. 
>```

* **FILE**: [*HerbivoryEmergenceTimingDataKNB.xlsx*](https://www.github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/orgs/knb/HerbivoryEmergenceTimingDataKNB.xlsx)
* **METADATA**: EML v2.1.1 ([XML](https://www.github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/orgs/knb/Dataset_for_Trade_off_between_early_.xml)) 

<!-- #region -->
### FILE: *HerbivoryEmergenceTimingDataKNB.xlsx*

*I cant display XLSX in Markdown. It's copied into the repo [here](https://www.github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/orgs/knb/HerbivoryEmergenceTimingDataKNB.xlsx).*

### XML: *eml-entity:* file level metadata fields

This entity is really skinny. Maybe EML doesn't support Microsoft XLS format well? That shouldn't matter to the metadata.

```xml
<otherEntity id="urn-uuid-151d090a-a867-4f5f-b1ce-aeb9081d6e69">
  <entityName>HerbivoryEmergenceTimingDataKNB.xlsx</entityName>
  <entityType>application/vnd.openxmlformats officedocument.spreadsheetml.sheet</entityType>
</otherEntity>
```

But the higher level dataset record is larger than the dataset record from example one. Maybe EML provides for storing the metadata that could apply to the dataset and the file at either level. Maybe it has something to do with the number of files in the dataset.
<!-- #endregion -->

## example 3 ([ISO/TS 19139 (gmd)](https://www.github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/iso-standards.md#ISO-19115))

* **DATASET**: https://knb.ecoinformatics.org/view/10.24431/rw1k43h
* **CITATION**:

>```
>Alaska Department of Fish and Game, Ben Williams, Richard Brenner, and Heath Kimball. ADF&G Central Region (Bristol Bay, Prince William Sound, Cook Inlet) Salmon Age Sex Length Data, 1957-2018. Research Workspace. 10.24431/rw1k43h, version: 10.24431_rw1k43h_202016215125. 
>```

* **FILE**: (*no access*)
* **METADATA**: http://www.isotc211.org/2005/gmd ([XML](https://www.github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/orgs/knb/10.24431_rw1k43h_202016215125.xml)) 

### XML: *This is the whole thing ...*

```xml
<?xml version="1.0" encoding="UTF-8"?>

<gmd:MD_Metadata xmlns:gmd="http://www.isotc211.org/2005/gmd" xmlns:gco="http://www.isotc211.org/2005/gco" xmlns:gmx="http://www.isotc211.org/2005/gmx" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:gmi="http://www.isotc211.org/2005/gmi" xmlns:gfc="http://www.isotc211.org/2005/gfc" xmlns:gml="http://www.opengis.net/gml/3.2" xmlns:gts="http://www.isotc211.org/2005/gts" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.isotc211.org/2005/gmd http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/gmd/gmd.xsd">
  <gmd:fileIdentifier gco:nilReason="missing"/>
  <gmd:language>
    <gco:CharacterString>eng;USA</gco:CharacterString>
  </gmd:language>
  <gmd:characterSet>
    <gmd:MD_CharacterSetCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#MD_CharacterSetCode" codeListValue="UTF-8">UTF-8</gmd:MD_CharacterSetCode>
  </gmd:characterSet>
  <gmd:hierarchyLevel>
    <gmd:MD_ScopeCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#MD_ScopeCode" codeListValue="dataset">dataset</gmd:MD_ScopeCode>
  </gmd:hierarchyLevel>
  <gmd:contact>
    <gmd:CI_ResponsibleParty>
      <gmd:organisationName>
        <gco:CharacterString>Axiom Data Science</gco:CharacterString>
      </gmd:organisationName>
      <gmd:positionName>
        <gco:CharacterString>Metadata Specialist</gco:CharacterString>
      </gmd:positionName>
      <gmd:contactInfo>
        <gmd:CI_Contact>
          <gmd:address>
            <gmd:CI_Address>
              <gmd:deliveryPoint>
                <gco:CharacterString>1016 W 6th Ave, Ste 105</gco:CharacterString>
              </gmd:deliveryPoint>
              <gmd:city>
                <gco:CharacterString>Anchorage</gco:CharacterString>
              </gmd:city>
              <gmd:administrativeArea>
                <gco:CharacterString>AK</gco:CharacterString>
              </gmd:administrativeArea>
              <gmd:postalCode>
                <gco:CharacterString>99501</gco:CharacterString>
              </gmd:postalCode>
              <gmd:country>
                <gco:CharacterString>USA</gco:CharacterString>
              </gmd:country>
              <gmd:electronicMailAddress>
                <gco:CharacterString>metadata@axiomdatascience.com</gco:CharacterString>
              </gmd:electronicMailAddress>
            </gmd:CI_Address>
          </gmd:address>
        </gmd:CI_Contact>
      </gmd:contactInfo>
      <gmd:role>
        <gmd:CI_RoleCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="pointOfContact">pointOfContact</gmd:CI_RoleCode>
      </gmd:role>
    </gmd:CI_ResponsibleParty>
  </gmd:contact>
  <gmd:dateStamp gco:nilReason="unknown">
    <gco:Date xsi:nil="true"/>
  </gmd:dateStamp>
  <gmd:metadataStandardName>
    <gco:CharacterString>ISO 19115</gco:CharacterString>
  </gmd:metadataStandardName>
  <gmd:dataSetURI gco:nilReason="unknown"/>
  <gmd:identificationInfo>
    <gmd:MD_DataIdentification>
      <gmd:citation>
        <gmd:CI_Citation>
          <gmd:title>
            <gco:CharacterString>ADF&amp;G Central Region (Bristol Bay, Prince William Sound, Cook Inlet) Salmon Age Sex Length Data, 1957-2018</gco:CharacterString>
          </gmd:title>
          <gmd:date gco:nilReason="missing"/>
          <gmd:citedResponsibleParty>
            <gmd:CI_ResponsibleParty>
              <gmd:organisationName>
                <gco:CharacterString>Alaska Department of Fish and Game</gco:CharacterString>
              </gmd:organisationName>
              <gmd:contactInfo>
                <gmd:CI_Contact>
                  <gmd:address>
                    <gmd:CI_Address>
                      <gmd:deliveryPoint>
                        <gco:CharacterString>333 Raspberry Road</gco:CharacterString>
                      </gmd:deliveryPoint>
                      <gmd:city>
                        <gco:CharacterString>Anchorage</gco:CharacterString>
                      </gmd:city>
                      <gmd:administrativeArea>
                        <gco:CharacterString>AK</gco:CharacterString>
                      </gmd:administrativeArea>
                      <gmd:postalCode>
                        <gco:CharacterString>99518</gco:CharacterString>
                      </gmd:postalCode>
                    </gmd:CI_Address>
                  </gmd:address>
                </gmd:CI_Contact>
              </gmd:contactInfo>
              <gmd:role>
                <gmd:CI_RoleCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="owner">owner</gmd:CI_RoleCode>
              </gmd:role>
            </gmd:CI_ResponsibleParty>
          </gmd:citedResponsibleParty>
          <gmd:presentationForm>
            <gmd:CI_PresentationFormCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#CI_PresentationFormCode" codeListValue="tableDigital">tableDigital</gmd:CI_PresentationFormCode>
          </gmd:presentationForm>
          <gmd:otherCitationDetails>
            <gco:CharacterString>Species: true cod pollock Pandalid shrimp tanner crab dungeness crab Pacific halibut arrowtooth flounder Pacific salmon species king crab Pacific herring Sebastes species Keywords: data rescue historical data data dissemination Alaska Department of Fish and Game survey data Multiple creation dates represent a range</gco:CharacterString>
          </gmd:otherCitationDetails>
        </gmd:CI_Citation>
      </gmd:citation>
      <gmd:abstract>
        <gco:CharacterString>Salmon age, sex, and length (ASL) data (which often includes other measurements as well) have been collected across Alaska by state biologists with the Alaska Department of Fish and Game (ADF&amp;G) since statehood (1959) and prior to that by federal biologists. These data are used for a variety of stock assessment applications, including forecasts and spawning escapement goals, and an important component of salmon management. These data are also have ecological importance as they can be used to examine trends in size and growth of salmon populations over time. In addition, physical specimens have value for examining changes in the diets and genetic characteristics of salmon populations over time. The datasets associated with this project are specific to the Central Region of ADF&amp;G's Division of Commercial Fisheries, which includes the following fisheries management areas: Prince William Sound, Upper and Lower Cook Inlet, and Bristol Bay. Data were collected from salmon in a variety of fisheries (sport, subsistence, commercial, personal use, etc.) and for research projects such as at weirs. As such, data include samples from marine and freshwater environments. Salmon ages were interpreted from the scales of fish, except in the rare instances where ages were estimated from otoliths. Salmon lengths were measured from mideye-to-fork. Age interpretation was done by biologists and technicians at area offices in Cordova, Homer, Soldotna, King Salmon, Dillingham, Anchorage, and elsewhere. Data assembled for this project are in csv formats.</gco:CharacterString>
      </gmd:abstract>
      <gmd:purpose>
        <gco:CharacterString>These data are used for a variety of stock assessment applications, including forecasts and spawning escapement goals, and an important component of salmon management. These data are also have ecological importance as they can be used to examine trends in size and growth of salmon populations over time. In addition, physical specimens have value for examining changes in the diets and genetic characteristics of salmon populations over time.</gco:CharacterString>
      </gmd:purpose>
      <gmd:credit/>
      <gmd:pointOfContact>
        <gmd:CI_ResponsibleParty>
          <gmd:individualName>
            <gco:CharacterString>Ben Williams</gco:CharacterString>
          </gmd:individualName>
          <gmd:organisationName>
            <gco:CharacterString>Alaska Department of Fish and Game</gco:CharacterString>
          </gmd:organisationName>
          <gmd:contactInfo>
            <gmd:CI_Contact>
              <gmd:address>
                <gmd:CI_Address>
                  <gmd:deliveryPoint>
                    <gco:CharacterString>PO Box 115526</gco:CharacterString>
                  </gmd:deliveryPoint>
                  <gmd:city>
                    <gco:CharacterString>Juneau</gco:CharacterString>
                  </gmd:city>
                  <gmd:administrativeArea>
                    <gco:CharacterString>Alaska</gco:CharacterString>
                  </gmd:administrativeArea>
                  <gmd:postalCode>
                    <gco:CharacterString>99811-5526</gco:CharacterString>
                  </gmd:postalCode>
                  <gmd:electronicMailAddress>
                    <gco:CharacterString>ben.williams@alaska.edu</gco:CharacterString>
                  </gmd:electronicMailAddress>
                </gmd:CI_Address>
              </gmd:address>
            </gmd:CI_Contact>
          </gmd:contactInfo>
          <gmd:role>
            <gmd:CI_RoleCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="principalInvestigator">principalInvestigator</gmd:CI_RoleCode>
          </gmd:role>
        </gmd:CI_ResponsibleParty>
      </gmd:pointOfContact>
      <gmd:pointOfContact>
        <gmd:CI_ResponsibleParty>
          <gmd:individualName>
            <gco:CharacterString>Richard Brenner</gco:CharacterString>
          </gmd:individualName>
          <gmd:organisationName>
            <gco:CharacterString>Alaska Department of Fish and Game</gco:CharacterString>
          </gmd:organisationName>
          <gmd:contactInfo>
            <gmd:CI_Contact>
              <gmd:address>
                <gmd:CI_Address>
                  <gmd:deliveryPoint>
                    <gco:CharacterString>PO BOX 115526</gco:CharacterString>
                  </gmd:deliveryPoint>
                  <gmd:city>
                    <gco:CharacterString>Juneau</gco:CharacterString>
                  </gmd:city>
                  <gmd:administrativeArea>
                    <gco:CharacterString>Alaska</gco:CharacterString>
                  </gmd:administrativeArea>
                  <gmd:postalCode>
                    <gco:CharacterString>99811-5526</gco:CharacterString>
                  </gmd:postalCode>
                  <gmd:electronicMailAddress>
                    <gco:CharacterString>richard.brenner@alaska.gov</gco:CharacterString>
                  </gmd:electronicMailAddress>
                </gmd:CI_Address>
              </gmd:address>
            </gmd:CI_Contact>
          </gmd:contactInfo>
          <gmd:role>
            <gmd:CI_RoleCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="principalInvestigator">principalInvestigator</gmd:CI_RoleCode>
          </gmd:role>
        </gmd:CI_ResponsibleParty>
      </gmd:pointOfContact>
      <gmd:pointOfContact>
        <gmd:CI_ResponsibleParty>
          <gmd:individualName>
            <gco:CharacterString>Heath Kimball</gco:CharacterString>
          </gmd:individualName>
          <gmd:organisationName>
            <gco:CharacterString>Alaska Dept Fish and Game Commercial Fisheries</gco:CharacterString>
          </gmd:organisationName>
          <gmd:positionName>
            <gco:CharacterString>Analyst Programmer</gco:CharacterString>
          </gmd:positionName>
          <gmd:contactInfo>
            <gmd:CI_Contact>
              <gmd:phone>
                <gmd:CI_Telephone>
                  <gmd:voice>
                    <gco:CharacterString>(907) 267-2894</gco:CharacterString>
                  </gmd:voice>
                </gmd:CI_Telephone>
              </gmd:phone>
              <gmd:address>
                <gmd:CI_Address>
                  <gmd:deliveryPoint>
                    <gco:CharacterString>333 Raspberry Road</gco:CharacterString>
                  </gmd:deliveryPoint>
                  <gmd:city>
                    <gco:CharacterString>Anchorage</gco:CharacterString>
                  </gmd:city>
                  <gmd:administrativeArea>
                    <gco:CharacterString>Alaska</gco:CharacterString>
                  </gmd:administrativeArea>
                  <gmd:postalCode>
                    <gco:CharacterString>99518-1599</gco:CharacterString>
                  </gmd:postalCode>
                  <gmd:country>
                    <gco:CharacterString>U.S.A.</gco:CharacterString>
                  </gmd:country>
                  <gmd:electronicMailAddress>
                    <gco:CharacterString>heath.kimball@alaska.gov</gco:CharacterString>
                  </gmd:electronicMailAddress>
                </gmd:CI_Address>
              </gmd:address>
            </gmd:CI_Contact>
          </gmd:contactInfo>
          <gmd:role>
            <gmd:CI_RoleCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="principalInvestigator">principalInvestigator</gmd:CI_RoleCode>
          </gmd:role>
        </gmd:CI_ResponsibleParty>
      </gmd:pointOfContact>
      <gmd:resourceMaintenance>
        <gmd:MD_MaintenanceInformation>
          <gmd:maintenanceAndUpdateFrequency>
            <gmd:MD_MaintenanceFrequencyCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#MD_MaintenanceFrequencyCode" codeListValue="notPlanned">notPlanned</gmd:MD_MaintenanceFrequencyCode>
          </gmd:maintenanceAndUpdateFrequency>
          <gmd:contact>
            <gmd:CI_ResponsibleParty>
              <gmd:organisationName>
                <gco:CharacterString>Axiom Data Science</gco:CharacterString>
              </gmd:organisationName>
              <gmd:positionName>
                <gco:CharacterString>Metadata Specialist</gco:CharacterString>
              </gmd:positionName>
              <gmd:contactInfo>
                <gmd:CI_Contact>
                  <gmd:address>
                    <gmd:CI_Address>
                      <gmd:deliveryPoint>
                        <gco:CharacterString>1016 W 6th Ave, Ste 105</gco:CharacterString>
                      </gmd:deliveryPoint>
                      <gmd:city>
                        <gco:CharacterString>Anchorage</gco:CharacterString>
                      </gmd:city>
                      <gmd:administrativeArea>
                        <gco:CharacterString>AK</gco:CharacterString>
                      </gmd:administrativeArea>
                      <gmd:postalCode>
                        <gco:CharacterString>99501</gco:CharacterString>
                      </gmd:postalCode>
                      <gmd:electronicMailAddress>
                        <gco:CharacterString>metadata@axiomdatascience.com</gco:CharacterString>
                      </gmd:electronicMailAddress>
                    </gmd:CI_Address>
                  </gmd:address>
                </gmd:CI_Contact>
              </gmd:contactInfo>
              <gmd:role>
                <gmd:CI_RoleCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="missing"/>
              </gmd:role>
            </gmd:CI_ResponsibleParty>
          </gmd:contact>
        </gmd:MD_MaintenanceInformation>
      </gmd:resourceMaintenance>
      <gmd:descriptiveKeywords>
        <gmd:MD_Keywords>
          <gmd:keyword>
            <gco:CharacterString>CONTINENT &gt; NORTH AMERICA &gt; UNITED STATES OF AMERICA &gt; ALASKA</gco:CharacterString>
          </gmd:keyword>
          <gmd:type>
            <gmd:MD_KeywordTypeCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#MD_KeywordTypeCode" codeListValue="place">place</gmd:MD_KeywordTypeCode>
          </gmd:type>
          <gmd:thesaurusName>
            <gmd:CI_Citation>
              <gmd:title>
                <gco:CharacterString>GCMD Locations Keywords version 8.4.1</gco:CharacterString>
              </gmd:title>
              <gmd:date gco:nilReason="unknown"/>
            </gmd:CI_Citation>
          </gmd:thesaurusName>
        </gmd:MD_Keywords>
      </gmd:descriptiveKeywords>
      <gmd:descriptiveKeywords>
        <gmd:MD_Keywords>
          <gmd:keyword gco:nilReason="missing"/>
          <gmd:type>
            <gmd:MD_KeywordTypeCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#MD_KeywordTypeCode" codeListValue="product">product</gmd:MD_KeywordTypeCode>
          </gmd:type>
          <gmd:thesaurusName>
            <gmd:CI_Citation>
              <gmd:title>
                <gco:CharacterString>Climate and Forecast Standard Names version 35</gco:CharacterString>
              </gmd:title>
              <gmd:date gco:nilReason="unknown"/>
            </gmd:CI_Citation>
          </gmd:thesaurusName>
        </gmd:MD_Keywords>
      </gmd:descriptiveKeywords>
      <gmd:descriptiveKeywords>
        <gmd:MD_Keywords>
          <gmd:keyword>
            <gco:CharacterString>Oncorhynchus gorbuscha</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>pink salmon, saumon rose, humpback, humpbacked salmon</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>Oncorhynchus keta</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>chum salmon</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>Oncorhynchus tshawytscha</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>Chinook salmon, king salmon, saumon chinook, salmón boquinegra</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>Oncorhynchus nerka</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>blueback salmon, kokanee, red salmon, sockeye salmon, saumon rouge</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>Oncorhynchus kisutch</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>coho salmon, saumon coho, salmón plateado, silver salmon</gco:CharacterString>
          </gmd:keyword>
          <gmd:thesaurusName>
            <gmd:CI_Citation>
              <gmd:title>
                <gco:CharacterString>ITIS</gco:CharacterString>
              </gmd:title>
              <gmd:date gco:nilReason="template"/>
            </gmd:CI_Citation>
          </gmd:thesaurusName>
        </gmd:MD_Keywords>
      </gmd:descriptiveKeywords>
      <gmd:descriptiveKeywords>
        <gmd:MD_Keywords>
          <gmd:keyword>
            <gco:CharacterString>holocene</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>1957 - 2018</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>September</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>August</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>July</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>June</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>May</gco:CharacterString>
          </gmd:keyword>
          <gmd:type>
            <gmd:MD_KeywordTypeCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#MD_KeywordTypeCode" codeListValue="temporal">temporal</gmd:MD_KeywordTypeCode>
          </gmd:type>
        </gmd:MD_Keywords>
      </gmd:descriptiveKeywords>
      <gmd:descriptiveKeywords>
        <gmd:MD_Keywords>
          <gmd:keyword>
            <gco:CharacterString>chum</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>pink salmon</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>coho</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>Chinook salmon</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>sockeye salmon</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>salmon</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>salmon fisheries</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>commercial fisheries</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>fisheries biology</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>salmon biology</gco:CharacterString>
          </gmd:keyword>
          <gmd:type>
            <gmd:MD_KeywordTypeCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#MD_KeywordTypeCode" codeListValue="theme">theme</gmd:MD_KeywordTypeCode>
          </gmd:type>
          <gmd:thesaurusName>
            <gmd:CI_Citation>
              <gmd:title>
                <gco:CharacterString>NPRB Keywords version 1.0</gco:CharacterString>
              </gmd:title>
              <gmd:date gco:nilReason="unknown"/>
            </gmd:CI_Citation>
          </gmd:thesaurusName>
        </gmd:MD_Keywords>
      </gmd:descriptiveKeywords>
      <gmd:descriptiveKeywords>
        <gmd:MD_Keywords>
          <gmd:keyword>
            <gco:CharacterString>Copper River</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>Cook Inlet</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>Lower Cook Inlet</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>Upper Cook Inlet</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>Prince William Sound</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>Bristol Bay</gco:CharacterString>
          </gmd:keyword>
          <gmd:type>
            <gmd:MD_KeywordTypeCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#MD_KeywordTypeCode" codeListValue="place">place</gmd:MD_KeywordTypeCode>
          </gmd:type>
        </gmd:MD_Keywords>
      </gmd:descriptiveKeywords>
      <gmd:resourceConstraints>
        <gmd:MD_Constraints>
          <gmd:useLimitation>
            <gco:CharacterString>No warranty expressed or implied is made regarding the accuracy or utility of the data, nor shall the act of distribution constitute any such warranty. This disclaimer applies both to individual use of the data and aggregate use with other data. It is strongly recommended that careful attention be paid to the contents of the metadata file associated with the data. The NPRB shall not be held liable for improper or incorrect use of the data described and/or contained herein.</gco:CharacterString>
          </gmd:useLimitation>
        </gmd:MD_Constraints>
      </gmd:resourceConstraints>
      <gmd:language>
        <gco:CharacterString>eng;USA</gco:CharacterString>
      </gmd:language>
      <gmd:topicCategory>
        <gmd:MD_TopicCategoryCode>oceans</gmd:MD_TopicCategoryCode>
      </gmd:topicCategory>
      <gmd:extent>
        <gmd:EX_Extent>
          <gmd:description>
            <gco:CharacterString>Bristol Bay, Prince William Sound, Cook Inlet</gco:CharacterString>
          </gmd:description>
          <gmd:geographicElement>
            <gmd:EX_GeographicBoundingBox>
              <gmd:westBoundLongitude>
                <gco:Decimal>-162</gco:Decimal>
              </gmd:westBoundLongitude>
              <gmd:eastBoundLongitude>
                <gco:Decimal>-141</gco:Decimal>
              </gmd:eastBoundLongitude>
              <gmd:southBoundLatitude>
                <gco:Decimal>57</gco:Decimal>
              </gmd:southBoundLatitude>
              <gmd:northBoundLatitude>
                <gco:Decimal>62</gco:Decimal>
              </gmd:northBoundLatitude>
            </gmd:EX_GeographicBoundingBox>
          </gmd:geographicElement>
        </gmd:EX_Extent>
      </gmd:extent>
      <gmd:extent>
        <gmd:EX_Extent>
          <gmd:geographicElement>
            <gmd:EX_BoundingPolygon>
              <gmd:polygon>
                <gml:Polygon gml:id="gmlid_1">
                  <gml:exterior>
                    <gml:LinearRing>
                      <gml:coordinates decimal="-143.02001953125,61.25966921642908 -141.0040283203125,61.23853141060282 -140.99853515625,60.52215754533236 -143.89892578125,60.511343283202464 -143.8868960738182,59.98507820028234 -143.887939453125,58.91031927906603 -153.30004692077637,58.87484414162803 -154.962158203125,58.205449994019915 -156.390380859375,57.47745016057072 -157.5439453125,57.47449674316678 -162.11254119873047,58.19966110122876 -162.16747283935547,58.63121664342478 -159.89501953124997,60.61932356461346 -155.32470703125,60.66241476534369 -155.07614135742185,62.12443624549497 -142.9541015625,62.226996036319726 -143.02001953125,61.25966921642908"/>
                    </gml:LinearRing>
                  </gml:exterior>
                </gml:Polygon>
              </gmd:polygon>
            </gmd:EX_BoundingPolygon>
          </gmd:geographicElement>
          <gmd:geographicElement>
            <gmd:EX_BoundingPolygon>
              <gmd:polygon>
                <gml:Point gml:id="gmlid_2">
                  <gml:coordinates decimal="-152.35153198242188,59.866883195210214"/>
                </gml:Point>
              </gmd:polygon>
            </gmd:EX_BoundingPolygon>
          </gmd:geographicElement>
          <gmd:geographicElement>
            <gmd:EX_BoundingPolygon>
              <gmd:polygon>
                <gml:Point gml:id="gmlid_3">
                  <gml:coordinates decimal="-147.20993041992188,60.54377524118842"/>
                </gml:Point>
              </gmd:polygon>
            </gmd:EX_BoundingPolygon>
          </gmd:geographicElement>
          <gmd:geographicElement>
            <gmd:EX_BoundingPolygon>
              <gmd:polygon>
                <gml:Point gml:id="gmlid_4">
                  <gml:coordinates decimal="-159.345703125,58.08949277309781"/>
                </gml:Point>
              </gmd:polygon>
            </gmd:EX_BoundingPolygon>
          </gmd:geographicElement>
        </gmd:EX_Extent>
      </gmd:extent>
      <gmd:extent>
        <gmd:EX_Extent>
          <gmd:temporalElement>
            <gmd:EX_TemporalExtent>
              <gmd:extent>
                <gml:TimePeriod gml:id="gmlid_5">
                  <gml:beginPosition>1957-01-01T00:00:00+00:00</gml:beginPosition>
                  <gml:endPosition>2018-01-01T00:00:00+00:00</gml:endPosition>
                </gml:TimePeriod>
              </gmd:extent>
            </gmd:EX_TemporalExtent>
          </gmd:temporalElement>
        </gmd:EX_Extent>
      </gmd:extent>
    </gmd:MD_DataIdentification>
  </gmd:identificationInfo>
  <gmd:contentInfo>
    <gmd:MD_FeatureCatalogueDescription>
      <gmd:language>
        <gco:CharacterString>eng; USA</gco:CharacterString>
      </gmd:language>
      <gmd:includedWithDataset>
        <gco:Boolean>true</gco:Boolean>
      </gmd:includedWithDataset>
      <gmd:featureCatalogueCitation>
        <gmd:CI_Citation>
          <gmd:title>
            <gco:CharacterString>ASL_DATA_DICTIONARY.csv</gco:CharacterString>
          </gmd:title>
          <gmd:date gco:nilReason="missing"/>
        </gmd:CI_Citation>
      </gmd:featureCatalogueCitation>
    </gmd:MD_FeatureCatalogueDescription>
  </gmd:contentInfo>
  <gmd:distributionInfo>
    <gmd:MD_Distribution>
      <gmd:distributor>
        <gmd:MD_Distributor>
          <gmd:distributorContact>
            <gmd:CI_ResponsibleParty>
              <gmd:organisationName>
                <gco:CharacterString>North Pacific Research Board</gco:CharacterString>
              </gmd:organisationName>
              <gmd:contactInfo>
                <gmd:CI_Contact>
                  <gmd:address>
                    <gmd:CI_Address>
                      <gmd:deliveryPoint>
                        <gco:CharacterString>Suite 100</gco:CharacterString>
                      </gmd:deliveryPoint>
                      <gmd:deliveryPoint>
                        <gco:CharacterString>1007 W 3rd Avenue</gco:CharacterString>
                      </gmd:deliveryPoint>
                      <gmd:city>
                        <gco:CharacterString>Anchorage</gco:CharacterString>
                      </gmd:city>
                      <gmd:administrativeArea>
                        <gco:CharacterString>AK</gco:CharacterString>
                      </gmd:administrativeArea>
                      <gmd:postalCode>
                        <gco:CharacterString>99501</gco:CharacterString>
                      </gmd:postalCode>
                      <gmd:country>
                        <gco:CharacterString>USA</gco:CharacterString>
                      </gmd:country>
                      <gmd:electronicMailAddress>
                        <gco:CharacterString>data@nprb.org</gco:CharacterString>
                      </gmd:electronicMailAddress>
                    </gmd:CI_Address>
                  </gmd:address>
                </gmd:CI_Contact>
              </gmd:contactInfo>
              <gmd:role>
                <gmd:CI_RoleCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="distributor">distributor</gmd:CI_RoleCode>
              </gmd:role>
            </gmd:CI_ResponsibleParty>
          </gmd:distributorContact>
          <gmd:distributorFormat>
            <gmd:MD_Format>
              <gmd:name>
                <gco:CharacterString>Metadata and data files available publicly through the NPRB Project Search catalog.</gco:CharacterString>
              </gmd:name>
              <gmd:version gco:nilReason="missing"/>
            </gmd:MD_Format>
          </gmd:distributorFormat>
        </gmd:MD_Distributor>
      </gmd:distributor>
    </gmd:MD_Distribution>
  </gmd:distributionInfo>
  <gmd:dataQualityInfo>
    <gmd:DQ_DataQuality>
      <gmd:scope>
        <gmd:DQ_Scope>
          <gmd:level>
            <gmd:MD_ScopeCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#MX_ScopeCode" codeListValue="dataset">dataset</gmd:MD_ScopeCode>
          </gmd:level>
        </gmd:DQ_Scope>
      </gmd:scope>
      <gmd:report>
        <gmd:DQ_QuantitativeAttributeAccuracy>
          <gmd:nameOfMeasure>
            <gco:CharacterString>Prince William Sound</gco:CharacterString>
          </gmd:nameOfMeasure>
          <gmd:evaluationMethodDescription>
            <gco:CharacterString>Most of the biological data (e.g., sex, length, weight) in the PWS ASL DB are discrete values that were measured (e.g., length, weight) or otherwise objectively determined (e.g., sex, harvest date, harvest location, etc.). As such, the values in these key data fields are believed to be true and accurate. However, aging scales is a subjective process involving discriminating false checks and growth rings from true annuli. As such, it is likely that some small portion of the assigned ages in this database may not reflect that specimen’s true and accurate age. However, we believe errors of this nature are limited because scales were aged by a small group of experienced agers.</gco:CharacterString>
          </gmd:evaluationMethodDescription>
          <gmd:result gco:nilReason="missing"/>
        </gmd:DQ_QuantitativeAttributeAccuracy>
      </gmd:report>
      <gmd:report>
        <gmd:DQ_QuantitativeAttributeAccuracy>
          <gmd:nameOfMeasure>
            <gco:CharacterString>Lower Cook Inlet</gco:CharacterString>
          </gmd:nameOfMeasure>
          <gmd:evaluationMethodDescription>
            <gco:CharacterString>Most of the biological data (e.g., sex, length, weight) in the LCI ASL DB are discrete values that were measured (e.g., length, weight) or otherwise objectively determined (e.g., sex, harvest date, harvest location, etc.). As such, the values in these key data fields are believed to be true and accurate. However, aging scales is a subjective process involving discriminating false checks and growth rings from true annuli. As such, it is likely that some small portion of the assigned ages in this database may not reflect that specimen’s true and accurate age. However, we believe errors of this nature are limited because scales were aged by a small group of experienced agers.</gco:CharacterString>
          </gmd:evaluationMethodDescription>
          <gmd:result gco:nilReason="missing"/>
        </gmd:DQ_QuantitativeAttributeAccuracy>
      </gmd:report>
      <gmd:report>
        <gmd:DQ_QuantitativeAttributeAccuracy>
          <gmd:nameOfMeasure>
            <gco:CharacterString>Upper Cook Inlet</gco:CharacterString>
          </gmd:nameOfMeasure>
          <gmd:evaluationMethodDescription>
            <gco:CharacterString>Most of the biological data (e.g., sex, length, weight) in the UCI ASL database are discrete values that were measured (e.g., length, weight) or otherwise objectively determined (e.g., sex, harvest date, harvest location, etc.). As such, the values in these key data fields are believed to be true and accurate. However, aging scales is a subjective process involving discriminating false checks and growth rings from true annuli. As such, it is likely that some small portion of the assigned ages in this database may not reflect that specimen’s true and accurate age. However, we believe errors of this nature are limited because scales were aged by a small group of trained agers.</gco:CharacterString>
          </gmd:evaluationMethodDescription>
          <gmd:result gco:nilReason="missing"/>
        </gmd:DQ_QuantitativeAttributeAccuracy>
      </gmd:report>
      <gmd:report>
        <gmd:DQ_QuantitativeAttributeAccuracy>
          <gmd:nameOfMeasure>
            <gco:CharacterString>Bristol Bay</gco:CharacterString>
          </gmd:nameOfMeasure>
          <gmd:evaluationMethodDescription>
            <gco:CharacterString>The biological data in the Bristol Bay ASL data are assessed with respect to accuracy using the procedures laid out in the Operational Plan associated with the project where the ASL was collected. Scale age accuracy is sufficient to estimate the proportion of each of the major age classes in the salmon catch and escapement in selected major river systems to within 5% of the true proportion 90% of the time (West, et al. 2012). There were several stat codes that were used from 1957-2000 that are not part of our current stat code regime and corresponding descriptions of areas were difficult to find. In cases where paper data sheets could not be used to confirm historical locations an “unknown” (999) field was used. The location was used to the most detailed level that could be confirmed (i.e. District, Subdistrict) and then 999 was used for what could not be verified (i.e. Stream, Location). It is believed that most of these fish were sampled as part of subsistence or sport fish sampling event and were largely non-sockeye fish and not part of any routine ASL sampling associated with the research activities of the Commercial Fisheries Division.</gco:CharacterString>
          </gmd:evaluationMethodDescription>
          <gmd:result gco:nilReason="missing"/>
        </gmd:DQ_QuantitativeAttributeAccuracy>
      </gmd:report>
      <gmd:report>
        <gmd:DQ_CompletenessOmission>
          <gmd:nameOfMeasure>
            <gco:CharacterString>Prince William Sound</gco:CharacterString>
          </gmd:nameOfMeasure>
          <gmd:evaluationMethodDescription>
            <gco:CharacterString>All relevant PWS ASL data 1960-2018 is included in this database.</gco:CharacterString>
          </gmd:evaluationMethodDescription>
          <gmd:result gco:nilReason="missing"/>
        </gmd:DQ_CompletenessOmission>
      </gmd:report>
      <gmd:report>
        <gmd:DQ_CompletenessOmission>
          <gmd:nameOfMeasure>
            <gco:CharacterString>Lower Cook Inlet</gco:CharacterString>
          </gmd:nameOfMeasure>
          <gmd:evaluationMethodDescription>
            <gco:CharacterString>The only relevant data not included in this LCI ASL database is a 2018 dataset collected by a private non-profit hatchery association (Cook Inlet Aquaculture Association) who stepped in to run a weir previously operated by ADF&amp;G prior to the project being cut in 2015 due to fiscal constraints. Those 2018 CIAA data were not yet available at the time the LCI ASL database was being completed. During the QA/QC process, approximately 312 of over 119 thousand ASL records (~0.26%) were excluded from the LCI ASL DB based on criteria described above in the Data Consistency Report section.</gco:CharacterString>
          </gmd:evaluationMethodDescription>
          <gmd:result gco:nilReason="missing"/>
        </gmd:DQ_CompletenessOmission>
      </gmd:report>
      <gmd:report>
        <gmd:DQ_CompletenessOmission>
          <gmd:nameOfMeasure>
            <gco:CharacterString>Upper Cook Inlet</gco:CharacterString>
          </gmd:nameOfMeasure>
          <gmd:evaluationMethodDescription>
            <gco:CharacterString>A large majority of the Upper Cook Inlet Stock ID/Catch &amp; Escapement sampling data is contained in the Central Region ASL database. The collection includes many years of data gathered by a private non-profit hatchery association, Cook Inlet Aquaculture Association, who have traditionally operated weirs in the UCI drainages when ADF&amp;G is unable to staff camps. ADF&amp;G UCI ASL data included in Central Region ASL database is as follows (as of 10/31/2019): 1.1961-1985 data includes all previous digitized data but does not include reconciliation with paper ASL data forms which often contain data that was not digitized. 2.1986-2018 data includes all previous digitized data and reconciled paper ASL data forms. These data are the most complete to date 3.2006-2007 Lower Cook Inlet Chenik Lake, statcode 24010200600 is included in this dataset ADF&amp;G Upper Cook Inlet ASL data not included in the Central Region ASL database is as follows (as of 10/31/19): 1.All chinook sampled after 2012 when Eastside Beach chinook ASL and genetic sampling was reassigned to Soldotna Sport Fish. 2.1993-1991 and 1989-1986 Offshore Test Fishery sex and length data (7 years) due to lost records 3.1993 baseline genetic &amp; ASL collection (~ 3,600 sockeye) due to lack of time to manually enter data 4.1992 baseline genetic &amp; ASL collection (~4,200 sockeye) due to lack of time to manually enter data 5.1991 ASL data taken in conjunction with an UCI salmon parasite study due to lack of time to manually enter data 6.1990 ASL data taken in conjunction with an UCI girth measurement and catchability study due to lack of time to manually enter data 7.1990-1989 Russian River weir ASL data due to lost records 8.1962 ASL data was not included in dataset because we have not deciphered the scale card numbering (many duplicates) system QA/QC on was completed to examine data for duplicates data entries, correct and consistent statcodes etc. When duplicate scale cards were encountered, we renumbered them to include a decimal. For instance scale card 1 was the same on two different dates; the earlier date would be named 1.1 and the later 1.2 etc.</gco:CharacterString>
          </gmd:evaluationMethodDescription>
          <gmd:result gco:nilReason="missing"/>
        </gmd:DQ_CompletenessOmission>
      </gmd:report>
      <gmd:report>
        <gmd:DQ_CompletenessOmission>
          <gmd:nameOfMeasure>
            <gco:CharacterString>Bristol Bay</gco:CharacterString>
          </gmd:nameOfMeasure>
          <gmd:evaluationMethodDescription>
            <gco:CharacterString>There are large chunks of missing data from this dataset. Unfortunately, large sets of the Bristol Bay dataset are not in any digital format. A rough estimate puts this at ~12,000 cards of sockeye salmon samples, and ~650 cards of Chinook salmon samples. Each of these sockeye cards could represent anywhere from 1 to 40 records which puts our rough estimate of missing sockeye samples at about 12,000-480,000 (most likely on the higher end of this range). Chinook cards hold anywhere from 1 to 10 samples which puts our rough estimate of missing Chinook samples at about 650 - 6,500 (most likely on the higher end of this range). The largest set of missing data is represented by the years 1957-1977 for the east side of Bristol Bay (Egegik, Ugashik, and Naknek-Kvichak districts). However, there are also sporadic missing samples from throughout the bay from about 1957 thorough the early 2000’s. An inventory of samples that are not included in the digital dataset is included in the metadata. This inventory was developed around 2004 by ADF&amp;G staff. It was intended to be a full inventory of all ASL sampling events that took place throughout the history of Bristol Bay. In this inventory staff took special care to go through all data types (Paper, Acetate, Scale Card, Electronic, and Database) and denote what was on hand at ADF&amp;G for each sampling event. This completed spreadsheet is considered the best inventory of what sampling was done, where data is located, and what format it is available in. The condensed version of this spreadsheet only includes sampling events that are not currently represented in this database, as well as what format it is in, and where it is stored. All sampling events after this inventory was created in 2004 are in database form and included in this dataset.</gco:CharacterString>
          </gmd:evaluationMethodDescription>
          <gmd:result gco:nilReason="missing"/>
        </gmd:DQ_CompletenessOmission>
      </gmd:report>
      <gmd:report>
        <gmd:DQ_ConceptualConsistency>
          <gmd:nameOfMeasure>
            <gco:CharacterString>Prince William Sound</gco:CharacterString>
          </gmd:nameOfMeasure>
          <gmd:evaluationMethodDescription>
            <gco:CharacterString>A variety of quality control measures were implemented at multiple steps throughout the data collection, data entry, and error checking processes. To avoid transcription errors in the field, the person recording data manually or electronically repeated the values called out by the person measuring the fish to confirm that they heard them correctly. During the period 1990–2001, when ASL data were collected on a Limnoterra FMB, the ascii output files were run through a suite of customized FORTRAN programs to summarize the data in a manner that facilitated error checking (e.g., sizes outside of expected range). During the period 2002–2018, when ASL data were collected on a Big Fin or ADF&amp;G FDMS FMB, we used a customized data entry program that implemented real-time quality control by warning the sampler when they input a value outside the list or range of values expected (e.g., length or weight smaller/larger than the smallest/largest value expected for that species. All length and weight data in the PWS ASL database were plotted and a small fraction of the total records (&lt;0.3%) were omitted from the DB when the length-weight relationship was discovered to be well outside of biological plausibility, or the length- or weight-at-age was considerably more than 2 standard deviations away from the mean length or weight for that species/age class. Along with these logical validity assessments, values in all fields were evaluated to confirm that they were valid and consistent with the range of expected values for that field.</gco:CharacterString>
          </gmd:evaluationMethodDescription>
          <gmd:result gco:nilReason="missing"/>
        </gmd:DQ_ConceptualConsistency>
      </gmd:report>
      <gmd:report>
        <gmd:DQ_ConceptualConsistency>
          <gmd:nameOfMeasure>
            <gco:CharacterString>Lower Cook Inlet</gco:CharacterString>
          </gmd:nameOfMeasure>
          <gmd:evaluationMethodDescription>
            <gco:CharacterString>A variety of quality control measures were implemented at multiple steps throughout the data collection, data entry, and error checking processes. To avoid transcription errors in the field, the person recording data manually or electronically (e.g., Juniper Systems Allegro) repeated the values called out by the person measuring the fish to confirm that they heard them correctly. During the period 1986–2001, when ASL data were collected on a Limnoterra FMB, the ascii output files were run through a suite of customized FORTRAN programs to summarize the data in a manner that facilitated error checking (e.g., sizes outside of expected range). During the period 2000–2014, when ASL data were collected on a Juniper Systems Allegro handheld PC, we used a customized data entry program that implemented real-time quality control by warning the sampler when they input a value outside the list or range of values expected (e.g., length or weight smaller/larger than the smallest/largest value expected for that species. All length and weight data in the LCI ASL database were plotted and a small fraction of the total records (&lt;0.3%) were omitted from the DB when the length-weight relationship was discovered to be well outside of biological plausibility, or the length- or weight-at-age was considerably more than 2 standard deviations away from the mean length or weight for that species/age class. Along with these logical validity assessments, values in all fields were evaluated to confirm that they were valid and consistent with the range of expected values for that field.</gco:CharacterString>
          </gmd:evaluationMethodDescription>
          <gmd:result gco:nilReason="missing"/>
        </gmd:DQ_ConceptualConsistency>
      </gmd:report>
      <gmd:report>
        <gmd:DQ_ConceptualConsistency>
          <gmd:nameOfMeasure>
            <gco:CharacterString>Upper Cook Inlet</gco:CharacterString>
          </gmd:nameOfMeasure>
          <gmd:evaluationMethodDescription>
            <gco:CharacterString>A variety of quality control measures were implemented at multiple steps throughout the data collection, data entry, error checking, and analysis processes. Through the years, sampling crews were firmly instructed to double check all manually entered data into an electronic format. Re-checks occur during scale reading and analysis for reports. ASL records have again been scanned for errors during the quality control check while assembling the UCI ASL database. Finally, after an individual year’s data is placed into the NPRB Final Data file, it’s again scanned for errors. To avoid transcription errors in the field, the person recording data manually or electronically (e.g., Juniper Systems Allegro) repeated the values called out by the person measuring the fish to confirm that they heard them correctly. During the period 1994–2013, when ASL data were collected on a Limnoterra FMB, the ascii output files were run through a suite of customized FORTRAN programs to summarize the data in a manner that facilitated error checking (e.g., sizes outside of expected range). During the period 2012–2015, when ASL data were collected on a Juniper Systems Allegro handheld PC, we used a customized data entry program that queried user if data was correct to input to database file. All length and weight data in the UCI ASL database need to be plotted to verify accuracy.</gco:CharacterString>
          </gmd:evaluationMethodDescription>
          <gmd:result gco:nilReason="missing"/>
        </gmd:DQ_ConceptualConsistency>
      </gmd:report>
      <gmd:report>
        <gmd:DQ_ConceptualConsistency>
          <gmd:nameOfMeasure>
            <gco:CharacterString>Bristol Bay</gco:CharacterString>
          </gmd:nameOfMeasure>
          <gmd:evaluationMethodDescription>
            <gco:CharacterString>A variety of quality control measures were implemented at multiple steps throughout the data collection, data entry, and error checking processes. The first firewall against errors is crew training. Senior crew train new crew and manuals are available for all software, hardware as well as how to sex and speciate Pacific Salmon species. To avoid transcription errors in the field, the person recording data manually or electronically (e.g., Juniper Systems Allegro) repeated the values called out by the person measuring the fish to confirm that they heard them correctly. The FDMS mobile software has several features to assist with the QA/QC of the data such as warning messages when unexpected or outsized values are entered. Upon uploading, the uploader must ‘verify’ the data before it is available for data reporting and summarizing. This forces the uploader to review the metadata for each sampling session before it is added to the dataset. Post-season quality control includes careful examination of the data for outliers before switching to handheld devices, a FORTRAN program program was used to compile scantron data sheets. The program also identified outliers of length and weight. All records with missing length, sex, and or age were removed from the summary and not included in the dataset. When staff moved towards excel workbooks, outliers were established by simple visual checks by sorting and filtering data. Any obvious outliers (lengths vs age, missing digits, etc) were removed or noted and not included in analysis.</gco:CharacterString>
          </gmd:evaluationMethodDescription>
          <gmd:result gco:nilReason="missing"/>
        </gmd:DQ_ConceptualConsistency>
      </gmd:report>
      <gmd:lineage>
        <gmd:LI_Lineage>
          <gmd:statement>
            <gco:CharacterString>**Prince William Sound Lineage Statement** This dataset contains salmon age, sex, and length data collected by ADF&amp;G's Division of Commercial Fisheries in the Prince William Sound management area. These data were collected between 1960 and 2018 using collection methods described below. 1960-2002: Salmon scales plucked with forceps and placed on numbered gum cards. Gum cards pressed to create scale impressions in acetate cards which are then visualized with a microfiche reader to determine age. Gum cards and acetates are organized into files by year, species, and project and stored in cabinets located in the Cordova ADF&amp;G office. Length measured in mm generally mid-eye to fork of tail (MEFL) using a fabric tape measure. Round weight measured in kg using portable scale. Sex determined from external characteristics or internal inspection of sex organs. The location of capture consists of the general location of the harvest area (and district/subdistrict for commercially harvested fish) or more specific location code for the project (weir, tower, test fishery, etc.). Capture gear (or method type) may also be included in the data record. 2003-2013: Comprehensive PWS ASL sampling methods documented for the first time in the unpublished 2003 Prince William Sound and Copper/Bering River Salmon Age, Weight, and Length Sampling Procedure Manual. This manual was updated as needed between 2003 and 2013 primarily to keep current with rapidly evolving technology (file extensions, spreadsheet programs). ASL samples were collected according to methods described in these procedure manuals. Methods for this period were very similar to historical methods except that electronic fish measuring boards were used to measure MEFL and store lengths paired with scale cards electronically. 2014-2018: ASL samples were collected by following standard operating procedures documented in the following publication; ASL sampling methods outlined in this document are very similar to those practiced historically in PWS apart from the adoption of electronic measuring and data storage technologies: Rich Brenner and Steve Moffitt. 2014. Salmon age, sex, size, and stock of origin sampling from Prince William Sound area fisheries and escapements. Alaska Department of Fish and Game, Regional Operational Plan 2A.14.02, Cordova. **Bristol Bay Lineage Statement** This dataset contains 1,970,119 records of salmon age, sex, and length (ASL) data collected by the Division of Commercial Fisheries within the Bristol Bay management area between 1957 and 2018 (Table 1). This document covers the 1,702,623 sockeye records (Table 2) and the 110,260 Chinook records (Table 3), the 124,677 Chum data (Table 4), the 17,537 Coho data (table 5), and the 15,022 Pink salmon data (table 6).` Salmon were measured from mid-eye to tail fork(+ 1 mm; METF). Prior to 2005 fish lengths were taken using a rigid measuring board or a caliper. From 2005 on fish lengths have been taken electronically using digital calipers or measuring boards. Round weights, when taken, were measured in kilograms (kg), generally to the nearest 10th of a kg, using either a portable spring scale or electronic kitchen scale. Sex was determined by examining external secondary sexual characteristics (Groot and Margolis 1991). Scales were plucked using forceps from the preferred area of each salmon: an area 2-3 rows above the lateral line, posterior to the dorsal fin and anterior to the anal fin (INPFC 1963). Scales were cleaned and mounted ridged side up on numbered gum card (40 or 48 scales per card) and then heat pressed onto acetate cards for reading and archival. Images of scale impressions were magnified 35x and projected on a microfiche reader so the number of fresh and saltwater annuli per scale could be counted to determine age. Age data is stored using the European age designation system (Koo 1962) wherein the first digit refers to the number of freshwater annuli, the second digit refers to the number of marine annuli, and the total age is the sum of the two digits plus one. For example, an age 1.2 salmon is a 4-year old salmon that spent 2 years in freshwater (in addition to an initial winter spent in the gravel as an alevin) and 2 years at sea before returning to their natal stream to spawn. Large portions of the historical paper dataset had ages originally recorded in the Gilbert-Rich format, were converted to the European age designation system over time as data were put into electronic forms. The metadata (geographic stat code, gear, species, date, etc) for each scale card is also summarized directly on the back of the gum cards on which scales are collected. Gum cards and acetates are archived together and archived by year, stat code, and species in filing cabinets located in Anchorage, Dillingham, or King Salmon. Operational plans for research projects describe ASL sampling around Bristol Bay. Buck and Brazil (2016) describe ASL sampling at the Nushagak sonar project. Brazil and Salomone (2016) describe ASL sampling at tower escapement enumeration projects. West and Brazil (2013) describe ASL sampling conducted by Inriver test fishing crews in Bristol Bay. West and Buck (In Prep.) describe ASL sampling of the commercial salmon harvest. Although methods for measuring fish and collecting and aging scales have remained fairly consistent throughout time, the data format changed has changed over the years, generally in response to evolving technology (e.g., computer hardware and software). Following are descriptions of the original data formats before they were standardized and assembled into this database. 1957-1978: ASL data during this period were generally recorded using a variety of data sheets and then hand entered to create digital records. To conserve space, a series of numerical codes representing standardized values were used in various data fields (e.g., species, gear type, length type, weight type, age type, age error codes, etc.). Header and fish records were combined so each fish also included the header information. Large amounts of ASL data from this period was stored on magnetic tapes which have been lost. Only small amounts of data from this time period exist electronically (Table 2). It appears, however, that significant amounts of this data may exist as paper records. We have recently begun efforts to enter this data although none of the fruits of this recent data entry effort is included in the dataset documented here. Preliminary examination of these paper records reveal numerous data sheet formats with a range of english and metric length/weight measurements as well as a mixture of age data in a mixture of Gilbert-Rich and European formats. Preliminary data entry efforts indicate that approximately 350/fish records per man-hour is feasible entering data directly ‘as-is’. Post-entry standardization of data will be accomplished using R. 1979-2012: ASL data during this period were generally collected on ADF&amp;G Standard AWL scantron field forms that were specifically designed for ASL (a.k.a. AWL for age, weight, length) data collection using scantron bubble sheets. Digital records were stored in MS Access DB. Minor changes to the FMB software resulted in there being two different ascii text formats over the years (1986-1990; 1991-2001). Over time, data from this era were slowly standardized to a common MS Access DB format compatible with a FORTRAN program developed by University of Washington researchers to collate and organize individual ascii files generated from the ASL scantron forms. 2005-Present: Currently all ASL data collected in Bristol Bay is done using a software ecosystem that incorporates a server-side system used to collect, collate, and manage ASL data and a separate Windows based mobile application used to collect ASL data at the point of sampling-the Fisheries Data Management System (FDMS; Sechrist et. al. In Prep.). Digital collection of ASL data at the point of sampling began in 2005 with early versions of the software currently used for commercial harvest sampling. Over time the software has been further developed and it’s use has spread throughout all ASL sampling projects such as escapement and test fishing projects. Currently digital ASL data collection in Bristol Bay is standard. Data entered through the mobile FDMS application were uploaded to the server on a daily basis where QA/QC was conducted. The mobile version of the app has standardized QA/QC built into the platform which will not allow outliers to be entered. Initially FDMS was only utilized inseason and data were archived in individual MS Access DB databases each year but more recently FDMS has become both an inseason tool and archive for digital ASL. **Upper Cook Inlet Lineage Statement** This dataset contains salmon age, sex, length (ASL), weight, and genetic data collected by ADF&amp;G's Division of Commercial Fisheries in the Upper Cook Inlet (UCI) management area. These data were collected between 1961 and 2018 using methods described below. Two events impacted sampling during this timeframe. In 1986, mid-July budget cuts led to staffing eliminations which resulted in a substantial decrease in the number of ASL samples collected for that year. In 1989, the Central District Drift fishery did not occur due to the presence of oil in Upper Cook Inlet originating from the Exxon Valdez oil spill. Salmon were manually measured from mid-eye to fork of tail (+ 1 mm; MEFL), using a meter measuring stick affixed to a rigid wooden or plastic board for sockeye, coho, pink, and chum. For chinook, a fabric tape was used due to their large size. For sampling commercial fishery sampling, two electronic fish measuring board systems were implemented, the Limnoterra FMB IV (1997-2011) and the Haglof DigiTech calipers paired with a handheld computer, Juniper Systems Allegro CX (2012-2015). In 2018, a new Fisheries Data Management System (FDMS), custom measuring board with computerized memory was used specifically for drift caught fish. When electronic measuring systems malfunctioned or were impractical to due place and time, field crews reverted to using manual measuring and paper ASL forms. All escapement sampling crews relied on manual measuring. Round weights, when taken, were measured in kilograms (kg), generally to the nearest 0.1 kg, using a portable dial scale, Salter Suspended Weigher 235, hung on a wooden tripod. Sex was generally determined from external secondary sexual characteristics (e.g., kype, humped back, etc.). Scales were plucked using forceps from the preferred area of each salmon: an area 2-3 rows above the lateral line, posterior to the dorsal fin and anterior to the anal fin. Scales were cleaned and mounted ridged side up on numbered gum card, 40 or 48 scales per card, and then heat pressed onto acetate cards for reading and archival. Images of scale impressions were magnified 40x and projected on a microfiche reader so the number of fresh and saltwater annuli per scale could be counted to determine age, which was generally recorded using the European age designation system (Koo 1962). The first digit in this system refers to the number of freshwater annuli, the second digit refers to the number of marine annuli, and the total age is the sum of the two digits plus one. For example, an age 1.2 salmon is a 4-year old salmon that spent 2 years in freshwater (first winter spent in the gravel as an alevin) and 2 years at sea. Historical age data that used the Gilbert-Rich format were converted the European age designation when input to this data set. Relevant metadata for each sample was recorded directly onto the gum cards, including: species sampled, the location of capture (e.g., district/subdistrict/stat area for commercial harvest samples; site location for escapement samples and offshore test fishery), sampling date, capture gear (e.g., drift or set gillnet, fishwheel, weir, beach seine), initials of samplers, and relevant remarks pertaining to the sample. Gum cards, acetates, and hard copy ASL forms were organized into files by year, stock/stream, and species and stored in bankers boxes located in the Soldotna ADF&amp;G warehouse. Sampling methods were described in annual in-house Stock ID/Catch and Escapement Operational Plans and periodically published in various Age and Stock Composition reports on the abundance, age, sex, and size statistics for sockeye, pink, and chum salmon in Upper Cook Inlet, which is available online (e.g., Tobias, Gist and Willette 2011: http://www.adfg.alaska.gov/FedAidPDFs/FDS13-49.pdf). Although methods for measuring fish and collecting and aging scales remained consistent throughout the time series contained in this database, the data format changed over the years, generally in response to evolving technology (e.g., computer hardware and software). Following are descriptions of the original data formats before they were standardized and assembled into this database. 1961-1983: ASL data during this period were generally recorded directly onto ADF&amp;G Standard AWL field forms that were specifically designed for ASL (a.k.a. AWL for age, weight, length) data collection. To conserve space, a series of numerical codes representing standardized values were used in various data fields (e.g., species, gear type, length type, weight type, age type, age error codes, etc.). All data was hand entered from original hard copy data forms into the current UCI Microsoft Excel standard data entry format developed for the Central Region ASL database. Some data during this time period were recorded in standard units (inches and pounds) which were converted to metric units. 1962 data was not included because we could not make sense of the scale card numbering. 1984-1990: Commercial catch ASL data during this period were generally collected using ADF&amp;G Adult Salmon Age-Length mark-sense forms. Basic sampling information was hand written on forms (e.g. card number, date, statistical code, type of fishery, gear, type of length measurement, number of scales per fish, number of cards per sampling event) then the appropriate box in a designated field was marked using a #2 pencil. A shared inter-region Optical Scanner read forms and produced an electronic file. During later years in this timeframe, when the Optical Scanner was not available, collected data was entered into an Epson HX-20 portable computer once sampling crews returned to the office. Escapement data collection continued to be hand written onto paper AWL forms then entered into an electronic format. All data were stored as text files. Data from this era were converted and standardized to the current UCI Microsoft Excel standard data entry format developed for the Central Region ASL database. 1990-1996: ASL data during this period were recorded directly onto ADF&amp;G Soldotna office AWL/ASL designed field forms. Various data fields included date, statistical location code, scale card number, sex, length, age/error code, otolith collection, parasite presence, and genetic sample numbers. Collected commercial and escapement data was hand entered into the portable Epson HX-20 computers then double checked immediately after entry. All data were stored as text files. Most data from this era were converted and standardized to the current UCI Microsoft Excel standard data entry format developed for the Central Region ASL database. It was necessary for some ASL records to be hand entered by seasonal technicians into an Excel worksheet. 1994-2013: Commercial catch ASL data during this period were collected using a Limnoterra electronic fish measuring board (FMB). Data were downloaded as ascii text files and then processed using a suite of custom programs designed to conduct quality control and reduce the raw data into standard ASL summary tables for reports (e.g., age composition, mean length and weight by age and sex, etc.). commercial catch data was converted from text files into Microsoft Excel and rearranged into the current UCI standard data entry format developed for the Central Region ASL database. Escapement sample ASL’s were previously digitized into a Microsoft Excel file and transferred directly into the Central Region ASL database. 2012-2015: Commercial catch ASL data during this period were often collected using Haglof calipers wired to a handheld Allegro computer that contained a customized data entry program. Data was then downloaded into a text file on an office computer. Text files were converted to Excel files to be assimilated into the standard data entry format developed for the Central Region ASL database. Escapement sampling and some commercial catch were not measured by calipers used ADF&amp;G Soldotna office ASL field forms to record data. This data was previously digitized into Microsoft Excel so were transferred into the Central Region ASL database. 2016-current year: All ASL data during this period were recorded directly onto updated ADF&amp;G Soldotna office ASL designed field forms. Data fields include date, statistical location code, scale card number, sex, length, age/error code, and comments. Data were digitized by seasonal technicians using Microsoft Excel into office computers then immediately double checked for accuracy. In 2018, the new FDMS salmon measuring/recording method was implemented for UCI drift catch sampling only. ASL data were easily converted from the customized program into Excel. All data from this time period was assimilated into Central Region ASL database. **Lower Cook Inlet Lineage Statement** This dataset contains salmon age, sex, and length (ASL) data collected by ADF&amp;G's Division of Commercial Fisheries in the Lower Cook Inlet management area. These data were collected between 1961 and 2014 using methods described below. After 2014, budget cuts led to curtailing a weir and the commercial catch sampling program, where virtually all of the ASL data collections were made. Salmon were measured from mid-eye to fork of tail (+ 1 mm; MEFL), generally using a fabric tape measure affixed to a rigid measuring board, but sometimes using an electronic fish measuring board (e.g., Limnoterra FMB IV, 1986-2001). Round weights, when taken, were measured in kilograms (kg), generally to the nearest 10th of a kg, using a portable spring scale (e.g., Chatillon Model IN-25), but sometimes to the nearest gram using an electronic balance (e.g., Ohaus Model CT6000-S). Sex was generally determined from external secondary sexual characteristics (e.g., kype, humped back, etc.), however a small incision near the vent was sometimes used to inspect gonads and confirm the sex. Scales were plucked using forceps from the preferred area of each salmon: an area 2-3 rows above the lateral line, posterior to the dorsal fin and anterior to the anal fin. Scales were cleaned and mounted ridged side up on numbered gum card (40 scales per card) and then heat pressed onto acetate cards for reading and archival. Images of scale impressions were magnified 35x and projected on a microfiche reader so the number of fresh and saltwater annuli per scale could be counted to determine age, which was generally recorded using the European age designation system (Koo 1962). The first digit in this system refers to the number of freshwater annuli, the second digit refers to the number of marine annuli, and the total age is the sum of the two digits plus one. For example, an age 1.2 salmon is a 4-year old salmon that spent 2 years in freshwater (first winter spent in the gravel as an alevin) and 2 years at sea. Relevant metadata for each sample was recorded directly onto the gum cards, including: species sampled, the location of capture (e.g., district/subdistrict/stat area for commercial harvest samples; weir location for escapement samples), sampling date, capture gear (e.g., set gillnet or purse seine), names of samplers, and relevant remarks pertaining to the sample. Gum cards and acetates were organized into files by year, stock/stream, and species and stored in cabinets located in the Homer ADF&amp;G office. Sampling methods were described in reports published periodically on the abundance, age, sex, and size statistics for sockeye, pink, and chum salmon in Lower Cook Inlet, which are available online (e.g., Otis and Dickson 2003: http://www.adfg.alaska.gov/FedAidPDFs/RIR.2A.2003.13.pdf). Although methods for measuring fish and collecting and aging scales remained consistent throughout the time series contained in this database, the data format changed over the years, generally in response to evolving technology (e.g., computer hardware and software). Following are descriptions of the original data formats before they were standardized and assembled into this database. 1961-1985: ASL data during this period were generally recorded directly onto ADF&amp;G Standard AWL field forms that were specifically designed for ASL (a.k.a. AWL for age, weight, length) data collection. To conserve space, a series of numerical codes representing standardized values were used in various data fields (e.g., species, gear type, length type, weight type, age type, age error codes, etc.). To facilitate including these data in the LCI ASL database, staff digitized these hard copy data using the standard data entry format that was used during the period 2003-2014 (e.g., Juniper Systems Allegro, see below). 1986-2001: ASL data during this period were generally collected using a Limnoterra electronic fish measuring board (FMB). Data were downloaded as ascii text files and then processed using a suite of custom Fortran programs designed to conduct quality control and reduce the raw data into standard ASL summary tables for reports (e.g., age composition, mean length and weight by age and sex, etc.). Minor changes to the FMB software resulted in there being two different ascii text formats over the years (1986-1990; 1991-2001). However, data from this era were standardized to a common format as they were assimilated for this ASL database project. 2000-2014: ASL data during this period were generally collected using a handheld computer (e.g., Juniper Systems, Allegro AMX-3) running a customized data entry program that provided real-time QA/QC checks (e.g., length or weight outside expected range). Data were downloaded as .csv files and then converted to MS Excel format for processing in a spreadsheet template designed to conduct further quality control (e.g., length or weight outside expected range given age) and then reduce the raw data into standard ASL summary tables for reports. Minor changes to the Allegro data entry program resulted in there being two different .csv formats over the years (2000-2002 [years when the new system was being tested and refined]; 2003-2014). However, data from this era were standardized to a common format as they were assimilated for this ASL database project.</gco:CharacterString>
          </gmd:statement>
          <gmd:processStep>
            <gmd:LI_ProcessStep>
              <gmd:description>
                <gco:CharacterString>Note that some statistical codes have changed over time. A supplemental file describing statistical code mapping over time is available upon request from ADF&amp;G as an Excel spreadsheet.</gco:CharacterString>
              </gmd:description>
              <gmd:processor>
                <gmd:CI_ResponsibleParty>
                  <gmd:individualName>
                    <gco:CharacterString>Heath Kimball</gco:CharacterString>
                  </gmd:individualName>
                  <gmd:organisationName>
                    <gco:CharacterString>Alaska Dept Fish and Game Commercial Fisheries</gco:CharacterString>
                  </gmd:organisationName>
                  <gmd:positionName>
                    <gco:CharacterString>Analyst Programmer</gco:CharacterString>
                  </gmd:positionName>
                  <gmd:contactInfo>
                    <gmd:CI_Contact>
                      <gmd:phone>
                        <gmd:CI_Telephone>
                          <gmd:voice>
                            <gco:CharacterString>(907) 267-2894</gco:CharacterString>
                          </gmd:voice>
                        </gmd:CI_Telephone>
                      </gmd:phone>
                      <gmd:address>
                        <gmd:CI_Address>
                          <gmd:deliveryPoint>
                            <gco:CharacterString>333 Raspberry Road</gco:CharacterString>
                          </gmd:deliveryPoint>
                          <gmd:city>
                            <gco:CharacterString>Anchorage</gco:CharacterString>
                          </gmd:city>
                          <gmd:administrativeArea>
                            <gco:CharacterString>Alaska</gco:CharacterString>
                          </gmd:administrativeArea>
                          <gmd:postalCode>
                            <gco:CharacterString>99508</gco:CharacterString>
                          </gmd:postalCode>
                          <gmd:country>
                            <gco:CharacterString>U.S.A.</gco:CharacterString>
                          </gmd:country>
                          <gmd:electronicMailAddress>
                            <gco:CharacterString>heath.kimball@alaska.gov</gco:CharacterString>
                          </gmd:electronicMailAddress>
                        </gmd:CI_Address>
                      </gmd:address>
                    </gmd:CI_Contact>
                  </gmd:contactInfo>
                  <gmd:role>
                    <gmd:CI_RoleCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="processor">processor</gmd:CI_RoleCode>
                  </gmd:role>
                </gmd:CI_ResponsibleParty>
              </gmd:processor>
            </gmd:LI_ProcessStep>
          </gmd:processStep>
          <gmd:source>
            <gmd:LI_Source>
              <gmd:description>
                <gco:CharacterString>This dataset contains salmon age, sex, and length data collected by ADF&amp;G's Division of Commercial Fisheries in the Prince William Sound management area.</gco:CharacterString>
              </gmd:description>
              <gmd:sourceCitation>
                <gmd:CI_Citation>
                  <gmd:title>
                    <gco:CharacterString>Prince William Sound</gco:CharacterString>
                  </gmd:title>
                  <gmd:date>
                    <gmd:CI_Date>
                      <gmd:date gco:nilReason="missing">
                        <gco:Date xsi:nil="true"/>
                      </gmd:date>
                      <gmd:dateType>
                        <gmd:CI_DateTypeCode codeList="http://www.ngdc.noaa.gov/metadata/published/xsd/schema/resources/Codelist/gmxCodelists.xml#CI_DateTypeCode" codeListValue="adopted">adopted</gmd:CI_DateTypeCode>
                      </gmd:dateType>
                    </gmd:CI_Date>
                  </gmd:date>
                  <gmd:identifier>
                    <gmd:RS_Identifier>
                      <gmd:code gco:nilReason="missing"/>
                    </gmd:RS_Identifier>
                  </gmd:identifier>
                </gmd:CI_Citation>
              </gmd:sourceCitation>
              <gmd:sourceStep>
                <gmd:LI_ProcessStep>
                  <gmd:description>
                    <gco:CharacterString>The Lineage Statement provides some of the processing steps that were applied to the data at the time they were collected and initially summarized. Following are the processing steps that were applied to archived data when they were combined and assimilated before being imported into the Central Region ASL database: 1.Converted from their original format (e.g., ascii, .csv) into MS Excel (.xls). 2.Edited to conform to a common format with standardized field names and values. (Note: when original values were edited, a comment documenting the change was recorded in a new field (e.g., DB_Edit_CMTS). 3.Plotted length-weight data to identify and remove records where the length-weight relationship was well outside the biologically plausible range (i.e., an obvious data entry error had occurred). 4.Migrated ASL data from MS Excel into an MS Access database (DB), creating a table named “ASL_ALL” that contained biological data for each fish sampled, along with some details associated with that sampling event (e.g., Sample_ID, Harvest_Date, etc.). 5.Created a related table in MS Access DB named “HEADER_ALL” that contained relevant metadata associated with each sampling event (e.g., Stock sampled, harvest location details, samplers, vessel sampled, etc.). 6.Created Look Up Tables (LUTs) for each field in the DB where a number or letter code was used to abbreviate and define a standard value. 7.Created Query Tables in MS Access DB to summarize counts of values in various fields to identify erroneous or redundant values and other incongruous issues. 8. The data was then given to Jeanette Clark (National Center for Ecological Analysis and Synthesis, Santa Barbara, California) who used SASAP funding to clean and document the data. 9.Once vetted through the above QA/QC measures, the data was transferred to Jason Lasell so it could be imported into Oracle. 10. Please note that the PWS Salmon ASL data and metadata are located here https://knb.ecoinformatics.org/view/doi:10.5063/F1FF3QMV.</gco:CharacterString>
                  </gmd:description>
                </gmd:LI_ProcessStep>
              </gmd:sourceStep>
            </gmd:LI_Source>
          </gmd:source>
          <gmd:source>
            <gmd:LI_Source>
              <gmd:description>
                <gco:CharacterString>This dataset contains salmon age, sex, and length data collected by ADF&amp;G's Division of Commercial Fisheries in the Bristol Bay management area. The Source Description above provides some of the processing steps that were applied to the data at the time they were collected and initially summarized. Following are the processing steps that were applied to archived data when they were combined and assimilated before being imported into the Central Region ASL database: Edited stat codes to conform to current definitions of locations. Over the course of this dataset there were 205 unique stat code locations used. In our current data collection protocol we use about 115. Old stat codes that are no longer in use were updated to match the current version of the code. When changes were made the historical stat code was archived in a separate field within the database so there would not be a discrepancy between paper data sheets and the database. A matrix of old and current stat codes is included in the metadata for this project. Edited to conform to a common format with standardized field names and values. The main changes revolved around species, gear, and project codes that were used differently throughout the history of the dataset. (Note: when original values were edited, a comment documenting the change was recorded in a new field. Datasets were then merged into a single dataset in .csv format Additional QA/QC of the dataset were conducted on the merged dataset. That effort is described in the Data Consistency section of this report.</gco:CharacterString>
              </gmd:description>
              <gmd:sourceCitation>
                <gmd:CI_Citation>
                  <gmd:title>
                    <gco:CharacterString>Lower Cook Inlet</gco:CharacterString>
                  </gmd:title>
                  <gmd:date gco:nilReason="missing"/>
                  <gmd:identifier>
                    <gmd:RS_Identifier>
                      <gmd:code gco:nilReason="missing"/>
                    </gmd:RS_Identifier>
                  </gmd:identifier>
                </gmd:CI_Citation>
              </gmd:sourceCitation>
              <gmd:sourceStep>
                <gmd:LI_ProcessStep>
                  <gmd:description>
                    <gco:CharacterString>Please add more information. See section for Prince William Sound as an example.</gco:CharacterString>
                  </gmd:description>
                </gmd:LI_ProcessStep>
              </gmd:sourceStep>
            </gmd:LI_Source>
          </gmd:source>
          <gmd:source>
            <gmd:LI_Source>
              <gmd:description>
                <gco:CharacterString>This dataset contains salmon age, sex, and length data collected by ADF&amp;G's Division of Commercial Fisheries in the Upper Cook Inlet management area.</gco:CharacterString>
              </gmd:description>
              <gmd:sourceCitation>
                <gmd:CI_Citation>
                  <gmd:title>
                    <gco:CharacterString>Upper Cook Inlet</gco:CharacterString>
                  </gmd:title>
                  <gmd:date gco:nilReason="missing"/>
                  <gmd:identifier>
                    <gmd:RS_Identifier>
                      <gmd:code gco:nilReason="missing"/>
                    </gmd:RS_Identifier>
                  </gmd:identifier>
                </gmd:CI_Citation>
              </gmd:sourceCitation>
              <gmd:sourceStep>
                <gmd:LI_ProcessStep>
                  <gmd:description>
                    <gco:CharacterString>The Source Description above provides some of the processing steps that were applied to the data at the time they were collected and initially summarized. Following are the processing steps that were applied to archived data when they were combined and assimilated before being imported into the Central Region ASL database: 1.Converted from their original electronic format (e.g., ascii, text files) into MS Excel (.xls). 2.Edited to conform to a common format with standardized field names and values. (Note: when original values were edited, a comment documenting the change was recorded in a “Working file” worksheet. 3.A comparison of the number of ASL records shown in a statistical area’s electronic database vs. number of paper ASL records vs. number of scales read in the Scale Reader’s Logbook was conducted. Any discrepancy between total number of records was investigated. ASL records missing or duplicated in the Central Region ASL database were found in this manner. 4.Cells without values were assigned a default value of -999 to denote that no values exist. 5.Salmon with lengths less than 400 were reinstated into the Central Region ASL database if eliminated from the original electronic format. 6.If ages were determined by otolith, a 1 was entered in the error code column. 7.A search for general data entry errors was conducted by using the Sort and Filter tools. 8.A final data check is performed after an individual year’s database is moved into the NPRN_PROJ Final Data folder in the Soldotna O-drive. All corrections are thoroughly documented in everyone’s working worksheet. 9.Once vetted through the?? QA/QC measures, the MS Excel datafiles will be transferred to Jason Lasell so it could be imported into Oracle.</gco:CharacterString>
                  </gmd:description>
                </gmd:LI_ProcessStep>
              </gmd:sourceStep>
            </gmd:LI_Source>
          </gmd:source>
          <gmd:source>
            <gmd:LI_Source>
              <gmd:description>
                <gco:CharacterString>This dataset contains salmon age, sex, and length data collected by ADF&amp;G's Division of Commercial Fisheries in the Lower Cook Inlet management area.</gco:CharacterString>
              </gmd:description>
              <gmd:sourceCitation>
                <gmd:CI_Citation>
                  <gmd:title>
                    <gco:CharacterString>Bristol Bay</gco:CharacterString>
                  </gmd:title>
                  <gmd:date gco:nilReason="missing"/>
                  <gmd:identifier>
                    <gmd:RS_Identifier>
                      <gmd:code gco:nilReason="missing"/>
                    </gmd:RS_Identifier>
                  </gmd:identifier>
                </gmd:CI_Citation>
              </gmd:sourceCitation>
              <gmd:sourceStep>
                <gmd:LI_ProcessStep>
                  <gmd:description>
                    <gco:CharacterString>The Source Description above provides some of the processing steps that were applied to the data at the time they were collected and initially summarized. Following are the processing steps that were applied to archived data when they were combined and assimilated before being imported into the Central Region ASL database: 1.Converted from their original format (e.g., ascii, .csv) into MS Excel (.xls). 2.Edited to conform to a common format with standardized field names and values. (Note: when original values were edited, a comment documenting the change was recorded in a new field (e.g., DB_Edit_CMTS). 3.Plotted length-weight data to identify and remove records where the length-weight relationship was well outside the biologically plausible range (i.e., an obvious data entry error had occurred). 4.Migrated ASL data from MS Excel into an MS Access database (DB), creating a table named “ASL_ALL” that contained biological data for each fish sampled, along with some details associated with that sampling event (e.g., Sample_ID, Harvest_Date, etc.). 5.Created a related table in MS Access DB named “HEADER_ALL” that contained relevant metadata associated with each sampling event (e.g., Stock sampled, harvest location details, samplers, vessel sampled, etc.). 6.Created Look Up Tables (LUTs) for each field in the DB where a number or letter code was used to abbreviate and define a standard value. 7.Created Query Tables in MS Access DB to summarize counts of values in various fields to identify erroneous or redundant values and other incongruous issues. 8.Once vetted through the above QA/QC measures, the MS Access DB was transferred to Jason Lasell so it could be imported into Oracle.</gco:CharacterString>
                  </gmd:description>
                </gmd:LI_ProcessStep>
              </gmd:sourceStep>
            </gmd:LI_Source>
          </gmd:source>
        </gmd:LI_Lineage>
      </gmd:lineage>
    </gmd:DQ_DataQuality>
  </gmd:dataQualityInfo>
</gmd:MD_Metadata>

```
