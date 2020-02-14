# NASA CMR ([Common Metadata Repository](https://earthdata.nasa.gov/eosdis/science-system-description/eosdis-components/cmr/)) + UMM ([Unified Metadata Model](https://earthdata.nasa.gov/eosdis/science-system-description/eosdis-components/cmr/umm))

CMR supports multiple metadata standards through its Unified Metadata Model (UMM), which (attempts) to map existing and future standards across various data management constructs and use cases: collections, granules, services, variables, visualizations, and tools.


## examples

I have every ORNL DAAC metadata record for collections (UMM-C) and granules (UMM-G) as returned by the CMR API request for JSON format in a repository on my GitHub page: https://github.com/jjmcnelis/nasa-cmr-inventory

Note: ORNL DAAC submits metadata in ECHO-10 format.

## links

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