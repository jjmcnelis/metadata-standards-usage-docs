# Environmental Data Initiative: ([EDI](https://environmentaldatainitiative.org/))

Metadata specification: [Ecological Metadata Language (EML)](https://eml.ecoinformatics.org/)

Supported community: [Long-Term Ecological Research (LTER) Network](https://lternet.edu/)

**links:**

Data portal: https://portal.edirepository.org/nis/home.jsp

EDI "metadata templates" (github): https://github.com/EDIorg/MetadataTemplates

**notes:**

Looks like [*eml-entity*](https://sbclter.msi.ucsb.edu/external/InformationManagement/EML_210schema/docs/eml-2.1.0/index.html#eml-entity) is the EML metadata construct for describing files within a dataset (*link is to spec for version 2.1.0, not the latest 2.1.1*).


## example


This is one of the more complete examples I've seen.

* DATASET: https://portal.edirepository.org/nis/metadataviewer?packageid=knb-lter-hfr.276.2
* DOI: [10.6073/pasta/8d35e09a8d49cd1309b070383ad5c97c](https://portal.edirepository.org/nis/metadataviewer?packageid=knb-lter-hfr.276.2)
* FILE: [hf276-01-DF-invertebrate.csv](https://portal.edirepository.org/nis/dataviewer?packageid=knb-lter-hfr.276.2&entityid=e804c34114d8fcea9bec08708095a7d9)

(A copy of [*hf276-01-DF-invertebrate.csv*](https://github.com/jjmcnelis/metadata-standards-usage-docs/orgs/examples/edi/hf276-01-DF-invertebrate.csv) is saved in this GitHub repository.)


### FILE: head

```csv
date,week,tag,efflux,temp,chamber,subsample,mesocosm,core.depth,leaf.decomp,invert.biomass.i,invert.abundance.i,invert.richness.i,invert.biomass.f,invert.abundance.f,invert.richness.f,microbial.biomass.c,microbial.biomass.n,spider,centipede,millipede,maggot,caterpillar,earthworm,ant,beetle
2013-07-17,1,710,NA,NA,0,A,0A,NA,0.039165738,0,0,0,0,0,0,280.7082,116.7619,0,0,0,0,0,0,0,0
2013-07-17,1,728,NA,NA,0,B,0B,NA,0.043274665,0,0,0,0,0,0,203.9996,84.8546,0,0,0,0,0,0,0,0
2013-07-17,1,701,5.503333333,18.40675,1,D,1D,2,0.040455219,0.61,13,5,0.401,6,4,273.3175,113.6877,1,2,2,0,0,7,0,1
2013-07-17,1,735,6.06,18.40675,1,A,1A,2.5,0.054841542,0.06,2,1,0.018,1,1,267.9268,111.4454,0,0,0,0,0,0,0,2
2013-07-17,1,916,5.21,18.40675,1,C,1C,3.5,0.11834962,0.07,4,4,0.007,1,1,272.0834,113.1744,1,0,0,0,0,1,0,2
2013-07-17,1,939,NA,18.40675,1,B,1B,4,0.045767275,0.46,11,5,NA,3,1,261.0754,108.5955,1,1,1,0,0,2,0,6
2013-07-17,1,730,NA,15.33955,2,D,2D,2.5,0.03926097,0.02,3,2,NA,NA,NA,266.1793,110.7185,2,0,0,0,0,0,1,0
2013-07-17,1,918,7.71,15.33955,2,A,2A,1.5,-0.073765856,0.02,3,2,NA,NA,NA,277.5849,115.4628,0,0,0,0,0,0,0,3
2013-07-17,1,936,NA,15.33955,2,B,2B,2,0.049477134,0.05,6,3,0.047,3,3,NA,NA,1,0,0,0,0,0,0,5
2013-07-17,1,749,5.53,19.60168,3,D,3D,3,0.049996038,0.14,15,7,0.014,3,3,NA,NA,1,0,3,0,0,1,7,2
2013-07-17,1,926,5.713333333,19.60168,3,A,3A,2,-0.027986241,0.02,3,3,NA,NA,NA,266.7579,110.9592,1,0,1,0,0,0,0,1
```


###  FILE: columns

The complete list:

```shell
date,
week,
tag,
efflux,
temp,
chamber,
subsample,
mesocosm,
core.depth,
leaf.decomp,
invert.biomass.i,
invert.abundance.i,
invert.richness.i,
invert.biomass.f,
invert.abundance.f,
invert.richness.f,
microbial.biomass.c,
microbial.biomass.n,
spider,
centipede,
millipede,
maggot,
caterpillar,
earthworm,
ant,
beetle
```



### XML: *eml-entity* level metadata fields

These describe the CSV file:

```xml
<entityName>hf276-01-DF-invertebrate.csv</entityName>
<entityDescription>Duke Forest common garden experiment -invertebrate</entityDescription>
<physical id="1458736063817">
    <objectName>hf276-01-DF-invertebrate.csv</objectName>
    <size unit="byte">19243</size>
    <authentication method="MD5">811b98ddd166a45e1655b000b1930dd8</authentication>
    <dataFormat>
        <textFormat>
            <numHeaderLines>1</numHeaderLines>
            <recordDelimiter>\r\n</recordDelimiter>
            <attributeOrientation>column</attributeOrientation>
            <simpleDelimited>
                <fieldDelimiter>,</fieldDelimiter>
            </simpleDelimited>
        </textFormat>
    </dataFormat>
    <distribution>
        <online>
            <url function="download">https://pasta.lternet.edu/package/data/e ...
        </online>
    </distribution>
</physical>
```


### XML: *eml-entity: attribute* level metadata fields

These describe the columns (*date* in this case):

```xml
<attribute id="1458738910423">
  <attributeName>date</attributeName>
  <attributeDefinition>date of CO2 efflux measurement</attributeDefinition>
  <measurementScale>
    <dateTime>
      <formatString>YYYY-MM-DD</formatString>
      <dateTimePrecision>1 day</dateTimePrecision>
    </dateTime>
  </measurementScale>
  <missingValueCode>
    <code>NA</code>
    <codeExplanation>missing value</codeExplanation>
  </missingValueCode>
</attribute>
```


### COMPLETE *eml-entity* XML (there are ~6 of these in the dataset):

```xml
<?xml version="1.0" encoding="UTF-8"?>
<dataTable id="hf276-01">
  <entityName>hf276-01-DF-invertebrate.csv</entityName>
  <entityDescription>Duke Forest common garden experiment -invertebrate</entityDescription>
  <physical id="1458736063817">
    <objectName>hf276-01-DF-invertebrate.csv</objectName>
    <size unit="byte">19243</size>
    <authentication method="MD5">811b98ddd166a45e1655b000b1930dd8</authentication>
    <dataFormat>
      <textFormat>
        <numHeaderLines>1</numHeaderLines>
        <recordDelimiter>\r\n</recordDelimiter>
        <attributeOrientation>column</attributeOrientation>
        <simpleDelimited>
          <fieldDelimiter>,</fieldDelimiter>
        </simpleDelimited>
      </textFormat>
    </dataFormat>
    <distribution>
      <online>
        <url function="download">https://pasta.lternet.edu/package/data/eml/knb-lter-hfr/276/2/e804c34114d8fcea9bec08708095a7d9</url>
      </online>
    </distribution>
  </physical>
  <attributeList>
    <attribute id="1458738910423">
      <attributeName>date</attributeName>
      <attributeDefinition>date of CO2 efflux measurement</attributeDefinition>
      <measurementScale>
        <dateTime>
          <formatString>YYYY-MM-DD</formatString>
          <dateTimePrecision>1 day</dateTimePrecision>
        </dateTime>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910438">
      <attributeName>week</attributeName>
      <attributeDefinition>week of the experiment</attributeDefinition>
      <measurementScale>
        <nominal>
          <nonNumericDomain>
            <textDomain>
              <definition>week of the experiment</definition>
            </textDomain>
          </nonNumericDomain>
        </nominal>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910454">
      <attributeName>tag</attributeName>
      <attributeDefinition>unique identifier number on metal tag attached to each decomposition bag</attributeDefinition>
      <measurementScale>
        <nominal>
          <nonNumericDomain>
            <textDomain>
              <definition>unique identifier number on metal tag attached to each decomposition bag</definition>
            </textDomain>
          </nonNumericDomain>
        </nominal>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910469">
      <attributeName>efflux</attributeName>
      <attributeDefinition>soil efflux (μmol CO2 mol-1) measured using LI-6400</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>dimensionless</standardUnit>
          </unit>
          <precision>0.000000001</precision>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910485">
      <attributeName>temp</attributeName>
      <attributeDefinition>mean air temperature delta (difference between chamber and average of 3 ambient reference stations) of Duke Forest warming chambers between April 2010 and July 2013 from which soil cores/invertebrates were extracted</attributeDefinition>
      <measurementScale>
        <interval>
          <unit>
            <standardUnit>celsius</standardUnit>
          </unit>
          <precision>0.00001</precision>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </interval>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910501">
      <attributeName>chamber</attributeName>
      <attributeDefinition>DF ant warming chamber from which the invertebrates originated</attributeDefinition>
      <measurementScale>
        <nominal>
          <nonNumericDomain>
            <textDomain>
              <definition>DF ant warming chamber from which the invertebrates originated</definition>
            </textDomain>
          </nonNumericDomain>
        </nominal>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910516">
      <attributeName>subsample</attributeName>
      <attributeDefinition>A-D, from 4 opposite sides of each chamber</attributeDefinition>
      <measurementScale>
        <nominal>
          <nonNumericDomain>
            <textDomain>
              <definition>A-D, from 4 opposite sides of each chamber</definition>
            </textDomain>
          </nonNumericDomain>
        </nominal>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910532">
      <attributeName>mesocosm</attributeName>
      <attributeDefinition>identifier derived from chamber and subsample</attributeDefinition>
      <measurementScale>
        <nominal>
          <nonNumericDomain>
            <textDomain>
              <definition>identifier derived from chamber and subsample</definition>
            </textDomain>
          </nonNumericDomain>
        </nominal>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910547">
      <attributeName>core.depth</attributeName>
      <attributeDefinition>depth of extracted soil core</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>centimeter</standardUnit>
          </unit>
          <precision>0.1</precision>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910563">
      <attributeName>leaf.decomp</attributeName>
      <attributeDefinition>percent leaf mass lost from decomposition bag</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>dimensionless</standardUnit>
          </unit>
          <precision>0.000000001</precision>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910579">
      <attributeName>invert.biomass.i</attributeName>
      <attributeDefinition>total mass of macroinvertebrates extracted from soil core and placed in mesocosm</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>gram</standardUnit>
          </unit>
          <precision>0.01</precision>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910594">
      <attributeName>invert.abundance.i</attributeName>
      <attributeDefinition>total number of macroinvertebrate individuals extracted from soil core and placed in mesocosm</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>number</standardUnit>
          </unit>
          <precision>1</precision>
          <numericDomain>
            <numberType>whole</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910610">
      <attributeName>invert.richness.i</attributeName>
      <attributeDefinition>total richness, at a broad morphological/order scale, of macroinvertebrates extracted from soil core and placed in mesocosm</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>number</standardUnit>
          </unit>
          <precision>1</precision>
          <numericDomain>
            <numberType>whole</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910625">
      <attributeName>invert.biomass.f</attributeName>
      <attributeDefinition>total mass of macroinvertebrates that survived to the end of the mesocosm experiment</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>gram</standardUnit>
          </unit>
          <precision>0.001</precision>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910641">
      <attributeName>invert.abundance.f</attributeName>
      <attributeDefinition>total number of macroinvertebrate individuals that survived to the end of the mesocosm experiment</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>number</standardUnit>
          </unit>
          <precision>1</precision>
          <numericDomain>
            <numberType>whole</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910657">
      <attributeName>invert.richness.f</attributeName>
      <attributeDefinition>total richness, at a broad morphological/order scale, of macroinvertebrates that survived to the end of the mesocosm experiment</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>number</standardUnit>
          </unit>
          <precision>1</precision>
          <numericDomain>
            <numberType>whole</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910672">
      <attributeName>microbial.biomass.c</attributeName>
      <attributeDefinition>microbial biomass (organic) carbon, using chloroform fumigation method in the lab of M Weintraub. TOC ug-C/g dry, calculated as difference between fumigated and K2SO4 extracted sample</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>dimensionless</standardUnit>
          </unit>
          <precision>0.0001</precision>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910688">
      <attributeName>microbial.biomass.n</attributeName>
      <attributeDefinition>microbial biomass nitrogen, using chloroform fumigation method in the lab of M Weintraub. TN ug-N/g dry, calculated as difference between fumigated and K2SO4 extracted sample.</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>dimensionless</standardUnit>
          </unit>
          <precision>0.0001</precision>
          <numericDomain>
            <numberType>real</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910703">
      <attributeName>spider</attributeName>
      <attributeDefinition>number of spiders extracted from soil core and placed in mesocosm</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>number</standardUnit>
          </unit>
          <precision>1</precision>
          <numericDomain>
            <numberType>whole</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910719">
      <attributeName>centipede</attributeName>
      <attributeDefinition>number of centipedes extracted from soil core and placed in mesocosm</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>number</standardUnit>
          </unit>
          <precision>1</precision>
          <numericDomain>
            <numberType>whole</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910735">
      <attributeName>millipede</attributeName>
      <attributeDefinition>number of millipedes extracted from soil core and placed in mesocosm</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>number</standardUnit>
          </unit>
          <precision>1</precision>
          <numericDomain>
            <numberType>whole</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910750">
      <attributeName>maggot</attributeName>
      <attributeDefinition>number of diptera larva extracted from soil core and placed in mesocosm</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>number</standardUnit>
          </unit>
          <precision>1</precision>
          <numericDomain>
            <numberType>whole</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910766">
      <attributeName>caterpillar</attributeName>
      <attributeDefinition>number of caterpillars extracted from soil core and placed in mesocosm</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>number</standardUnit>
          </unit>
          <precision>1</precision>
          <numericDomain>
            <numberType>whole</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910781">
      <attributeName>earthworm</attributeName>
      <attributeDefinition>number of earthworms extracted from soil core and placed in mesocosm</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>number</standardUnit>
          </unit>
          <precision>1</precision>
          <numericDomain>
            <numberType>whole</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910797">
      <attributeName>ant</attributeName>
      <attributeDefinition>number of ants extracted from soil core and placed in mesocosm</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>number</standardUnit>
          </unit>
          <precision>1</precision>
          <numericDomain>
            <numberType>whole</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
    <attribute id="1458738910813">
      <attributeName>beetle</attributeName>
      <attributeDefinition>number of beetles extracted from soil core and placed in mesocosm</attributeDefinition>
      <measurementScale>
        <ratio>
          <unit>
            <standardUnit>number</standardUnit>
          </unit>
          <precision>1</precision>
          <numericDomain>
            <numberType>whole</numberType>
          </numericDomain>
        </ratio>
      </measurementScale>
      <missingValueCode>
        <code>NA</code>
        <codeExplanation>missing value</codeExplanation>
      </missingValueCode>
    </attribute>
  </attributeList>
  <numberOfRecords>176</numberOfRecords>
</dataTable>
```
