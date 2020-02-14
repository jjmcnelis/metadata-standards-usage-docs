# NASA CMR ([Common Metadata Repository](https://earthdata.nasa.gov/eosdis/science-system-description/eosdis-components/cmr/)) + UMM ([Unified Metadata Model](https://earthdata.nasa.gov/eosdis/science-system-description/eosdis-components/cmr/umm))

CMR supports multiple metadata standards through its Unified Metadata Model (UMM), which (attempts) to map existing and future standards across various data management constructs and use cases: collections, granules, services, variables, visualizations, and tools.

* [CMR](https://earthdata.nasa.gov/eosdis/science-system-description/eosdis-components/cmr/)
* [UMM](https://earthdata.nasa.gov/eosdis/science-system-description/eosdis-components/cmr/umm)

**supported standards/specifications:**

standards/specs that have file level implementations:

* ECHO 10
* ISO 19115-1 and 19115-2

all standards/specs (i.e. implemented at collection/dataset):

* DIF 10: GCMD Directory Interchange Format for collection metadata
* ECHO 10: ECS Clearning House's format for collection and granule metadata
* SERF: GCMD's Service Entry Resource Format for service metadata
* ISO 19115-1 & 19115-2

## examples

I have every ORNL DAAC metadata record for collections (UMM-C) and granules (UMM-G) as returned by the CMR API request for JSON format in a repository on my GitHub page: https://github.com/jjmcnelis/nasa-cmr-inventory

Some direct links:

* Dataset: All ABoVE datasets currently archived at ORNL DAAC | [JSON reformatted from ECHO-10 XML](https://raw.githubusercontent.com/jjmcnelis/nasa-cmr-inventory/master/projects/above/ds.json)
* Granule: All granules records from [one ABoVE dataset](https://doi.org/10.3334/ORNLDAAC/1700) in an array | [JSON reformatted from ECHO-10 XML](https://github.com/jjmcnelis/nasa-cmr-inventory/blob/master/projects/above/MODIS_MAIAC_Reflectance_1700/gr.json)

Note: ORNL DAAC submits metadata in ECHO-10 format.

```
TODO
```
