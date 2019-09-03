# Useful links:
- [CoE Git repo on this](https://github.com/cicoe/NEON-schema.org)
- [P418/CHORDs site modeling](https://github.com/earthcubearchitecture-project418/p419dcatservices/tree/master/CHORDS)

# 2 Aug 2019
Chuck, Christine, Jane, Jeremey, TomG

## ESIP updates:
- Proposed to ESIP to create a Geoschemas Cluster.  Adam to lead with Chuck
    - On web: Github, website
    - Following bioschemas example: sub dir in github for each term.  
        - Have a spreadsheet template for going from csv to (?ttl?)
        - But don’t have LD 
- Focus on: Best practices, Building out the Vocab bits we need, Build out web and github infrastructure
- TERN: Simon Cox’s alignment work for TERN creating a vocabulary which will be of use to us/NEON
  - Has created a ‘site’.  It’s a subclass of SOSA ‘sample’.  Is effectively a plot site/research place where you capture a sample
  - linkeddata.tern.org.au
In general, we need to work out how to align formal and informal

### Discussion:
- For ground cover eg: the same term might be used for different data products where there are different values in different data products
- We could make a linkedata-NEON end point where NEON can publish their own terms and ideally associate those with formal ontologies (where relevant).
   - Can make SHACL validators for their data products terms

### Schema.org latest release: 
Has new proposed type “observation”
https://github.com/schemaorg/schemaorg/blob/master/data/releases/3.9/ext-pending.ttl

- How to align with SOSA Observable Property 
- How to align RDF datacube and SOSA: Semantic Data on the Web (OGC) WG in theory responsible for this
- Align Datacube Vocab and OBI - Another TODO

### How to start:
- We’re starting with the foundational terms we need (eg site)
- But we need a minimal example: particularly to demo interoperability
   - We can point to how NEON isn’t going off to make it again but working with the community
   - Show how this is going to make life better
   - Eg build a LD endpoint for an example dataset and show how that makes it queryable without downloading the dat?
        - ropensci/emlid
- Chuck and Jane to talk about what min demo

# 11 July 2019
Attending: Christine, Chuck, Jeremy, Jane, Tom

Review of progress and of Chuck’s slides for ESIP
https://docs.google.com/presentation/d/1PA9SpO48YI50Ky73g9QGXSgtH6Dhs1ki3cZrPCvmFmQ/edit#slide=id.g5cc53683ad_0_67

## Site:
How do we encapsulate rights and policies as relates to a site
Chuck looking at expressing the concepts as relate to the higher level view of a site vs NEON has been more focused on specifics of eg what’s on the site.

## Slides
Is there a diagram that shows how all these ontologies sit alongside each other?  Schema.org/ENVO/SWEET/BIO….

Using RDF and open world assumption: Eg SWEET uses alignment modules to eg SOSA (literally a turtle snippet)

ENVO does reasoning over the ontology itself to discover classes

What are the choices NEON needs to make to choose which ontologies we need and what alignment modules do we need?
   - Chuck: Start with schema.org.  Then when you create templates for populating json schema, you can use the larger set, so use ENVO etc there.  Google won’t use that (at least not now) but other applications can you
   - NEON already sort of using ENVO > work towards publishing a Vocabulary (RDFS) that has alignment modules to  ENVO/SWEET etc

Can we create a minimum demo by end of pilot?
Take a subset of the NEON vocab and use Suzuko(sp?) 



# 13 June 2019
Attending: Christine, Chuck

## Agenda
- Field sites map/list/csv - has a lot of rich information
- Schema.org - the minimal information set. Place has some properties
- Geojson

# 6 June 2019
Attending: 
Christine, Jeremey, Chuck, Jane, Tom

## Agenda:
- Review Chuck’s [initial modeling](https://app.gra.fo/editor/2c7f33f1-e678-49b1-a6d6-2d68692469ca)
- Explore NEON Vocabulary

## Notes:

Screenshot of model:
Builds on schema.org and [Geolink](http://schema.geolink.org/1.0/base/main.html#d4e3511)
- Key:
    - Dashed lines: Class of
    - Red: From Schema.org 
    - Yellow:  New
    - Purple: schema.org.geolink and [GBEO](https://www.gebco.net/data_and_products/)
    - Blue: stub (needs modeling out)

![](model1.png)

## Issues
Overloaded:
- Feature
- Place
- Feature of interest depends on both

Need some new classes
Research activity
Research site

## Discussion
[Research project](https://schema.org/ResearchProject): This is a type of [organisation](https://schema.org/Organization)
A problem with schema.org is there isn’t formal modeling behind it so ideally we should also create an alignment to formally modeled ontologies so a reasoner could read this properly and draw conclusions 

**How to avoid stalling while we wait on community discussions:**
- Site modeling  // Depends on Spatial and Science-on-Schema efforts
  - Will build on SOSA and Geolink
  - Activities and samples/types of observations
- NEON infrastructure to build jsonld from current EML templates  //Depends on Science-on-Schema
- NEON and schema.org.  //Depends on science on schema effort 
  - For discoverability
  - For reasoning/analytics: //Depends on selecting domain ontologies to align with
Making NEON Vocab linked //Depends on YAMZ reboot possibly?  Or not, EML-LD is a thing already

- Can NEON learn to do their own modeling and alignment creation?  Yes
   - Always build your own and then create alignment cause then if external disappears you’re safe.  Also context matters, so if slight difference between your and a community definition you can still express your 

Ideal future:
NEON provides a WFS3.0 services that serves their 'sites' //Allows people to build maps and queries etc based on these

## Next step:
- How to make new classes needed?
  - Adam and Doug thoughts?
  - Open a issue on schema.org
  - Also need to check in with Science-on-schema on the pending qs in the dataset schema
- On NEON Vocab: can we start by ‘binning’ NEON Vocab into classes: 


# 30 May 2019
Attending: Jeremey, Christine, Chuck, Jane, Ewa, Tom, Doug

## Agenda
    1. Discuss open questions in dataset schema
    2. Begin work on ‘site’ modeling.

## Notes:
Site modeling
Competency questions related to location from prior VOCamp:
A scientist might search for a given data using:  
Co-ordinates (various projections and format)
Country, State/Province
Ecological region type or Biome
Land type classification
Heat zone
Habitat
NEON site name
NEON domain
NEON 4 letter code
USGS GNIS feature name (or not GNIS)

ESIP & Science on Schema ongoing discussion about how to represent geospatial boundary

Woodhole using just reference a buoy - could NEON do the same?  
- Ecological region / Land type classification  
  - Site name / 4 letter code
    - Plot / Tower / Hut / Mamle grid
    - Sensor/Sample

IGSN - discussing site and web stack too: how to mimic science-on-schema “dataset” for type sample   ref: https://github.com/IGSN/web-metadata 

NEON also working on applying IGSN on their samples

### TODO
1. Chuck - work on modeling (gra.fo) NEON site structure (current model). > Share with Doug and Adam first.  Will be in https://gra.fo/
2. Get a csv of NEON vocabulary: Name, Def, Unit, Type

## Dataset discussion
Reviewed dataset model, punting on / to do in the future:
- Create URIs for NEON controlled vocabulary including a RDF contained definition
    - YAMZ might be useful here.  Hopefully this will get a revamp to help NEON science community come to concensus on terms iff needed
- Resolve some issues with Adam and Doug (see comments in [example](https://github.com/cicoe/NEON-schema.org/blob/master/data_sets/SingleAspiratedAirTemperature.jsonld) ). Key issues:
    - How to dereference collections
- Build infrastructure to generate jsonld end points from eml and templates
