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

Other impressions/notes:

* EDI receives metadata in word documents ??
* [*eml-entity*](https://sbclter.msi.ucsb.edu/external/InformationManagement/EML_210schema/docs/eml-2.1.0/index.html#eml-entity) is the EML metadata construct that describes data objects (i.e. files) within a dataset (*note: that link points to the spec for version 2.1.0, not 2.1.1*).