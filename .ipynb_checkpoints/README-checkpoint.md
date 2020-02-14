# ess/cf metadata research

## orgs
*(these four are in the deliverable?)*

* [orgs/**NSF KNB: Knowledge Network for Biocomplexity**](https://github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/orgs/knb.md)
* [orgs/**NSF EDI: Environmental Data Initiative**](https://github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/orgs/edi.md)
* [orgs/**NASA CMR: Common Metadata Repository**](https://github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/orgs/cmr.md)
* [orgs/**BCO-DMO: Biological & Chemical Oceanography Data Management Office**](https://github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/orgs/bco-cmo.md)

[KNB](https://github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/orgs/knb.md) and [EDI](https://github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/orgs/edi.md) organizations seem to have a lot in common:

* both are DataONE affiliates;
* both are use the same data access/portal infrastructure (powered by [MetacatUI](https://github.com/NCEAS/metacatui));
* both use the [Ecological Metadata Language](https://eml.ecoinformatics.org/)) metadata specification.

Other impressions:

* EDI data handlers don't do themselves any favors if they receive metadata from data providers in word documents...

## example records

* KNB
  * Dataset: https://knb.ecoinformatics.org/view/urn:uuid:045c9be0-7a5a-4c01-b010-529dc21aee79 | [XML](https://github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/specifications/eml-examples/Dataset_for_Trade_off_between_early_.xml)
  * Dataset: https://knb.ecoinformatics.org/view/doi:10.5063/F17W69K6 | [XML](https://github.com/jjmcnelis/metadata-standards-usage-docs/blob/master/specifications/eml-examples/Thaw_depth_and_organic_layer_depth_from_Alaska.xml)

* CMR
  * Dataset: All ABoVE datasets currently archived at ORNL DAAC | [JSON reformatted from ECHO-10 XML](https://raw.githubusercontent.com/jjmcnelis/nasa-cmr-inventory/master/projects/above/ds.json)
  * Granule: All granules records from [one ABoVE dataset](https://doi.org/10.3334/ORNLDAAC/1700) in an array | [JSON reformatted from ECHO-10 XML](https://github.com/jjmcnelis/nasa-cmr-inventory/blob/master/projects/above/MODIS_MAIAC_Reflectance_1700/gr.json)

```python

```
