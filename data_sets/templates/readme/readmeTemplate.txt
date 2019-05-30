<-- LIST| prefix indicates multiple entries may be generated for the element
    OS| prefix indicates include the element if SUPPLIER is TOS or AOS
    FUZZED| prefix indicates include the element if REMARKS contains "fuzzed" (case-insensitive)
    COMMASEP| prefix indicates generate a comma-separated list of values for the element
    EC| prefix indicates include the element if DP_IDQ is DP4.00200.001
    AOP| prefix indicates include the element if SUPPLIER is AOP
    IS| prefix indicates include the element if SUPPLIER is TIS or AIS (excluding EC)
    IS/OS| prefix indicates include the element if SUPPLIER is TIS or AIS (excluding EC), TOS, or AOS
    NON-AOP| prefix indicates include the element if SUPPLIER is not AOP
    NON-NULL| prefix indicates include the element if the value referenced in brackets is non-null
-->
This data package been produced by and downloaded from the National Ecological Observatory Network, managed cooperatively by Battelle. These data are provided under the terms of the NEON data policy at http://data.neonscience.org/data-policy. 

DATA PRODUCT INFORMATION
------------------------

ID: [DP_IDQ]

Name: [DP_NAME]

Description: [DP_DESC]

NEON Science Team Supplier: [SUPPLIER]

Abstract: [DP_ABSTRACT]

Brief Design Description: [DESIGN_DESC]

Brief Study Area Description: [STUDY_DESC]

[NON-NULL|Sensor(s): [SENSOR]]

Keywords: [KEYWORDS]


QUERY INFORMATION
-----------------

[NON-AOP|Date-Time for Data Publication: [QUERY DATE AS YYYY-MM-DD HH:MM (UTC)]]
[NON-AOP|Start Date-Time for Queried Data: [EML TEMPORALCOVERAGE BEGINDATE AS YYYY-MM-DD HH:MM (UTC)]]
[NON-AOP|End Date-Time for Queried Data: [EML TEMPORALCOVERAGE ENDDATE AS YYYY-MM-DD HH:MM (UTC)]]

Site: [SITE]
[NON-AOP|Geographic coordinates (lat/long datum): [EML BOUNDINGCOORDINATES]]
Domain: [DOMAIN]

[NON-AOP|This zip package was generated on: [QUERY DATE AS YYYY-MM-DD HH:MM (UTC)]]

DATA PACKAGE CONTENTS
---------------------

This zip package contains the following documentation files:

- This readme file: [NEON.DOM.SITE.DPL.DPNUM.REV.readme.GENTIME.txt]
[IS/OS|- Term descriptions, data types, and units: [NEON.DOM.SITE.DPL.DPNUM.REV.variables.GENTIME.csv]]
[OS|- Data entry validation and parsing rules: [NEON.DOM.SITE.DPL.DPNUM.REV.validation.GENTIME.csv]]
[OS|- Sampling location files: ]
[LIST|DP_SPEC.DP_SPEC_TITLE WHERE DP_SPEC.TYPE_ID IS TAXONOMY TYPE OR STATUSCODES TYPE]
[NON-AOP|- Machine-readable metadata file describing the data package: [NEON.DOM.SITE.DPL.DPNUM.REV.EML.BEGINDATE-ENDDATE.GENTIME.xml]. This file uses the Ecological Metadata Language schema. Learn more about this specification and tools to parse it at http://data.neonscience.org/faq.]
[IS|- Sensor position information: [NEON.DOM.SITE.DPL.PRNUM.REV.sensor_positions.GENTIME.csv]]
- Other related documents, such as engineering specifications, field protocols and data processing documentation: 
[LIST|DP_SPEC.DP_SPEC_NUMBER[NON-NULL|, [DP_SPEC.DP_SPEC_TITLE]]]

Additional documentation for this data product or other related documentation are available at http://data.neonscience.org/documents.

This zip package also contains [NUMBER OF DATA FILES] data files:
[LIST|FILENAME[NON-NULL| - [TABLE DESCRIPTION]]]

Basic download package definition: [BASIC_DESC]

[NON-NULL|Expanded download package definition: [EXPANDED_DESC]]


FILE NAMING CONVENTIONS
-----------------------

NEON data files are named using a series of component abbreviations separated by periods. File naming conventions for NEON data files differ between NEON science teams. A file will have the same name whether it is accessed via the data portal or the API.

[OS|NEON observational systems (OS) data files: NEON.DOM.SITE.DPL.PRNUM.REV.DESC.YYYY-MM.PKGTYPE.GENTIME.csv]

[IS|NEON instrumented systems (IS) data files: NEON.DOM.SITE.DPL.PRNUM.REV.HOR.VER.TMI.DESC.YYYY-MM.PKGTYPE.GENTIME.csv]

[EC|NEON eddy covariance (EC) data files contain multiple data products, formatted using HDF5, and delivered within a zip file:\n  zip file: NEON.DOM.SITE.DP4.00200.001.YYYY-MM.PGKTYPE.GENTIME.zip\n  monthly data files: NEON.DOM.SITE.DP4.00200.001.DESC.YYYY-MM.PKGTYPE.h5\n  daily data files: NEON.DOM.SITE.DP4.00200.001.DESC.YYYY-MM-DD.PKGTYPE.h5]

[AOP|NEON airborne observational platform (AOP) data file naming conventions:\nData product: File name structure\n------------ | -------------------\nL1 products\n   Digital camera: FLHTSTRT_EHCCCCCC(IMAGEDATETIME)-NNNN_ort.tif\n   Discrete return lidar, unclassified: NEON_DOM_SITE_DPL_LNNN-R_FLIGHTSTRT_DESC.laz\n   Discrete return lidar, classified:  NEON_DOM_SITE_DPL_EEEEEE_NNNNNNN_DESC.laz\n   Spectrometer: NEON_DOM_SITE_DPL_FLHTDATE_FFFFFF_DESC.h5\n   Waveform lidar: NEON_DOM_SITE_DPL_LNNN-R_FLIGHTSTRT_DESC.wvz (or .plz)\nL2 products\n   Spectrometer: NEON_DOM_SITE_DPL_FLHTDATE_FFFFFF_DESC.zip (or .tif)\nL3 products\n   Spectrometer / Lidar / Camera: NEON_DOM_SITE_DPL_EEEEEE_NNNNNNN_DESC.laz]

The definitions of component abbreviations are below. See NEON.DOC.002651: NEON Data Product Numbering Convention, located at http://data.neonscience.org/documents for more information.

General conventions, used for all data products:
   NEON: denotes the organizational origin of the data product and identifies the product as operational; data collected as part of a special data collection exercise are designated by a separate, unique alphanumeric code created by the PI.

   DOM: a three-character alphanumeric code, referring to the domain of data acquisition (D01 - D20).

   SITE: a four-character alphanumeric code, referring to the site of data acquisition; all sites are designated by a standardized four-character alphabetic code.

   DPL: a three-character alphanumeric code, referring to data product processing level;

   PRNUM: a five-character numeric code, referring to the data product number (see the Data Product Catalog at http://data.neonscience.org/data-product-catalog).

   REV: a three-digit designation, referring to the revision number of the data product. The REV value is incremented by 1 each time a major change is made in instrumentation, data collection protocol, or data processing such that data from the preceding revision is not directly comparable to the new.

   HOR: a three-character designation, referring to measurement locations within one horizontal plane. For example, if five surface measurements were taken, one at each of the five soil array plots, the number in the HOR field would range from 001-005. 

   VER: a three-character designation, referring to measurement locations within one vertical plane. For example, if eight air temperature measurements are collected, one at each tower vertical level, the number in the VER field would range from 010-080. If five soil temperature measurements are collected below the soil surface, the number in the VER field would range from 501-505. 

   TMI: a three-character designation, referring to the temporal representation, averaging period, or coverage of the data product (e.g., minute, hour, month, year, sub-hourly, day, lunar month, single instance, seasonal, annual, multi-annual). 000 = native resolution, 001 = native resolution (variable or regular) or 1 minute, 002 = 2 minute, 005 = 5 minute, 015 = 15 minute, 030 = 30 minute, 060 = 60 minutes or 1 hour, 100 = approximately once per minute at stream sites and once every 5-10 minutes at buoy sites (lakes/rivers), 101-103 = native resolution of replicate sensor 1, 2, and 3 respectively, 999 = Sensor conducts measurements at varied interval depending on air mass, 01D = 1 day, 01M = 1 month, 01Y = 1 year.

   DESC: an abbreviated description of the data file or table.

   YYYY-MM: the year and month of the data in the file.

   PKGTYPE: the type of data package downloaded. Options are 'basic', representing the basic download package, or 'expanded',representing the expanded download package (see more information below).

   GENTIME: the date-time stamp when the file was generated, in UTC. The format of the date-time stamp is YYYYMMDDTHHmmSSZ.

Time stamp conventions:
   YYYY: Year
   YY: Year, last two digits only
   MM: Month: 01-12
   DD: Day: 01-31
   T: Indicator that the time stamp is beginning
   HH: Hours: 00-23
   mm: Minutes: 00-59
   SS: Seconds: 00-59
   Z: Universal Time Coordinated (Universal Coordinated Time), or UTC

[AOP|AOP-specific conventions:\n   CCCCCC: Digital camera serial number\n   EEEEEE: UTM easting of lower left corner\n   FFFFFF: Numeric code for an individual flightline\n   FLHTDATE: Date of flight, YYYYMMDD\n   FLHTSTRT: Start time of flight, YYMMDDHH\n   FLIGHTSTRT: Start time of flight, YYYYMMDDHH\n   IMAGEDATETIME: Date and time of image capture, YYYYMMDDHHmmSS\n   NNN: Planned flightline number\n   NNNN: Sequential number for indexing files\n   NNNNNNN: UTM northing of lower left corner\n   R: Repeat number]

ADDITIONAL INFORMATION
----------------------

Data products that are a source of this data product:
[LIST|DERIVED DP_IDQ, DERIVED DP_NAME]

Data products that are derived from this data product:
[LIST|SOURCE DP_IDQ, SOURCE DP_NAME]

Other related data products (by sensor, protocol, or variable measured):
[LIST|RELATED DP_IDQ, RELATED DP_NAME]

[FUZZED|Protection of species of concern: At most sites, taxonomic IDs of species of concern have been 'fuzzed', i.e., reported at a higher taxonomic rank than the raw data, to avoid publishing locations of sensitive species. For a few sites with stricter regulations (e.g., Great Smoky Mountains National Park (GRSM)), records for species of concern are not published.] 

[OS|Obfuscation of Personnel Information: At times it is important to know which data were collected by particular observers. In order to protect privacy of NEON technicians while also providing a way to consistently identify different observers, we obfuscate each NEON personnel name by internally linking it to a unique string identifier (e.g., Jane Doe=ByrziN0LguMJHnInl2NM/trZeA5h+c0) and publishing only the identifier.]


CHANGE LOG
----------

[LIST|Issue Date: [DP_CHANGE_LOG.ISSUE_DATE]\nIssue: [DP_CHANGE_LOG.ISSUE]\n[LIST|       Date Range: [DP_CHANGE_LOG.DATE_RANGE_START] to [DP_CHANGE_LOG.DATE_RANGE_END]\n       Location(s) Affected: [COMMASEP|DP_CHANGE_LOG.LOCATION_AFFECTED]]\nResolution Date: [DP_CHANGE_LOG.RESOLVED_DATE]\nResolution: [DP_CHANGE_LOG.RESOLUTION]\n]

ADDITIONAL REMARKS
------------------

[DP_CATALOG.REMARKS]

NEON DATA POLICY AND CITATION GUIDELINES
----------------------------------------

Please visit http://data.neonscience.org/data-policy for more information about NEON's data policy and citation guidelines.

DATA QUALITY AND VERSIONING
---------------------------

The data contained in this file are considered provisional. Updates to the data, QA/QC and/or processing algorithms over time will occur on an as-needed basis.  Please check back to this site for updates tracked in change logs.  Query reproducibility on provisional data cannot be guaranteed. 
 
Starting in 2020 or earlier, NEON will begin to offer static versions of each data product, annotated with a globally unique identifier. Versioned IS and OS data will be produced by reprocessing each IS and OS data product from the beginning of the data collection period to approximately 12-18 months prior to the reprocessing date (to allow for calibration checks, return of external lab data, etc.). The reprocessing step will use the most recent QA/QC methods and processing algorithms. Versioned AOP data will be produced by reprocessing the entire AOP archive as advances in algorithms and processing technology are incorporated. This will typically occur in the northern winter months, between flight season peaks, and will be on the order of every 3 to 5 years in frequency.