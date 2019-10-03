## Description of the content in vampire-moth-globi

[![Build Status](https://travis-ci.org/ParasiteTracker/vampire-moth-dwca.svg)](https://travis-ci.org/ParasiteTracker/vampire-moth-dwca) [![GloBI](http://api.globalbioticinteractions.org/interaction.svg?accordingTo=globi:ParasiteTracker/vampire-moth-dwca)](http://globalbioticinteractions.org/?accordingTo=globi:ParasiteTracker/vampire-moth-dwca) 

[```Citation```](#Citation) / [```Interaction Types```](#interaction-types) / [```Data Definitions```](#data-definitions) / [```Included Resources```](#included-resources) /  [```Data Issues```](#data-issues) / [```Summary```](#summary)


### Description

vampire-moth-dwca is a repository for specimen occurrence data about vampire moths and their fruit-piercing relatives (Lepidoptera: Erebidae: *Calyptra* spp.). The feeding observations are from the specimens.


***Workflow***

	Edit on Symbiota -> create Darwin Core Archive -> let GloBI know where the Darwin Core Archive lives

All of the fields in the occurrences.csv dataset was produced by entering data in presently available fields in Symbiota (September 28, 2018). The records were entered or edited by a person using the occurrence editor pages in the portal, which has both ```DWC:associatedTaxa``` and ```DWC:dynamicProperties``` available to edit as free text. Once the records were entered, a Darwin Core Archive was created using the Symbiota Darwin Core Archive publishing tool and the files from that publication are directly uploaded to the GitHub repository. The contents of a Symbiota Darwin Core Archive file were uploaded to GitHub. To propagate any additions or changes to GloBI a new DWC Archive is published and the new version of the files are uploaded to GitHub.

![image of vampire-moth-dwca-symbiota](https://raw.githubusercontent.com/ParasiteTracker/vampire-moth-dwca/master/biotic-interaction-lifecycle.png)


***Entering Data in Symbiota***

Biotic interaction data can be entered through the ```DWC:dynamicProperties``` and ```DWC:associatedTaxa``` fields. 

[```DWC:associatedTaxa```](http://rs.tdwg.org/dwc/terms/associatedTaxa) is "A list (concatenated and separated) of identifiers or names of taxa and their associations with the Occurrence." The TDWG recommended best practice is to "separate the values with a vertical bar (' | '), and to separate the relationship from the taxon with a colon (':'). Examples: "host: Quercus alba", "parasitoid of:Cyclocephala signaticollis | predator of Apis mellifera".

The interactions are not explicitly defined, meaning that the word "host" or "eats" could have different meanings in different datasets because a definition of the word is not included. This is where the ```DWC:dynamicProperties``` becomes useful.

[```DWC:dynamicProperties```](http://rs.tdwg.org/dwc/terms/dynamicProperties) is a "list of additional measurements, facts, characteristics, or assertions about the record. Meant to provide a mechanism for structured content", and that structured content for biotic interactions could include the explict identifiers for the details of the interaction.

![image of vampire-moth-dwca-symbiota](https://raw.githubusercontent.com/ParasiteTracker/vampire-moth-dwca/master/Symbiota-screen.png)

Key:value formatted data entered into ```DWC:dynamicProperties``` in the above examples are: 

	targetTaxonName: Homo sapiens; 
	targetTaxonId: https://www.gbif.org/species/2436436; 
	interactionTypeName: eats; 
	interactionTypeId: http://purl.obolibrary.org/obo/RO_0002470; 
	targetBodyPartName: blood; 
	targetBodyPartId: http://purl.obolibrary.org/obo/NCIT_C12434



Key:value formatted data entered into ```DWC:associatedTaxa``` in the above examples are: 

	eats: Homo sapiens


***Publish Darwin Core Archive***

Symbiota comes with the tools to publish your data into a Darwin Core Archive. Publish your data and make it live.


***Let GloBI Know Where Your Dataset Is***

You can let GloBI know where your Darwin Core Archive RSS feed is online by [opening up an issue](https://github.com/jhpoelen/eol-globi-data/issues/new) or choose one of the other methods of sharing your data on the [GloBI contribute page](https://www.globalbioticinteractions.org/contribute). Symbiota creates the RSS feed when the archive is created (ex. UCSB RSS Feed: https://symbiota.ccber.ucsb.edu:443/webservices/dwc/rss.xml)


### Interaction Types Already in GloBI (Updated October 3, 2019)

The kinds of biotic species interactions in GloBI are mapped to terms in the Relations Ontology (RO), or EOL vocabulary. Classes to describe interactions in the RO (and other ontologies) can be searched through the [Ontobee](http://www.ontobee.org/ontology/RO?iri=http://purl.obolibrary.org/obo/RO_0002437) or [EOL Term Glossary](https://eol.org/terms/glossary/a).

|interaction|source|target|termIRI
1|eats|consumer|food|http://purl.obolibrary.org/obo/RO_0002470
2|eatenBy|food|consumer|http://purl.obolibrary.org/obo/RO_0002471
3|preysOn|predator|prey|http://purl.obolibrary.org/obo/RO_0002439
4|preyedUponBy|prey|predator|http://purl.obolibrary.org/obo/RO_0002458
5|kills|killer|victim|http://purl.obolibrary.org/obo/RO_0002626
6|killedBy|victim|killer|http://purl.obolibrary.org/obo/RO_0002627
7|parasiteOf|parasite|host|http://purl.obolibrary.org/obo/RO_0002444
8|hasParasite|host|parasite|http://purl.obolibrary.org/obo/RO_0002445
9|hostOf|host|symbiont|http://purl.obolibrary.org/obo/RO_0002453
10|hasHost|symbiont|host|http://purl.obolibrary.org/obo/RO_0002454
11|pollinates|pollinator|plant|http://purl.obolibrary.org/obo/RO_0002455
12|pollinatedBy|plant|pollinator|http://purl.obolibrary.org/obo/RO_0002456
13|pathogenOf|pathogen|host|http://purl.obolibrary.org/obo/RO_0002556
14|hasPathogen|host|pathogen|http://purl.obolibrary.org/obo/RO_0002557
15|vectorOf|vector|pathogen|http://purl.obolibrary.org/obo/RO_0002459
16|hasVector|pathogen|vector|http://purl.obolibrary.org/obo/RO_0002460
17|dispersalVectorOf|vector|seed|http://eol.org/schema/terms/DispersalVector
18|hasDispersalVector|seed|vector|http://eol.org/schema/terms/HasDispersalVector
19|symbiontOf|symbiont|symbiont|http://purl.obolibrary.org/obo/RO_0002440
20|mutualistOf|mutualist|mutualist|http://purl.obolibrary.org/obo/RO_0002442
21|commensalistOf|commensalist|commensalist|http://purl.obolibrary.org/obo/RO_0002441
22|flowersVisitedBy|plant|visitor|http://purl.obolibrary.org/obo/RO_0002623
23|visitsFlowersOf|visitor|plant|http://purl.obolibrary.org/obo/RO_0002622
24|ecologicallyRelatedTo|source|target|http://purl.obolibrary.org/obo/RO_0002321
25|coOccursWith|source|target|http://purl.obolibrary.org/obo/RO_0008506
26|interactsWith|source|target|http://purl.obolibrary.org/obo/RO_0002437




