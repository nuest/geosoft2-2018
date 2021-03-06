# FOSS Repositories & Preservation
**Autors**: Niklas Aßelmann [@NiklasAsselmann](https://github.com/NiklasAsselmann) & Yannick Paulsen [@yhallowiegeht](https://github.com/yhallowiegeht)

---

## Table of Content

- [1 Introduction](#1-introduction)
- [2 FOSS Repositories](#2-foss-repositories)
  * [2.1 Prerequesite Knowledge](#21-prerequesite-knowledge)
    + [2.1.1 Data Repository Definition](#211-data-repository-definition)
    + [2.1.2 Basic Terminology](#212-basic-terminology)
      - [2.1.2.1 Version Control](#2121-version-control)
      - [2.1.2.2 Working Tree](#2122-working-tree)
      - [2.1.2.3 Embargo](#2123-embargo)
      - [2.1.2.4 Metadata Harvesting](#2124-metadata-harvesting)
      - [2.1.2.5 Digital Object Identifier](#2125-doi)
      - [2.1.2.6 Representational state transfer](#2126-rest)
      - [2.1.2.7 Open Researcher and Contributor ID](#2127-orcid)
    + [2.1.3 Repository vs. Archive](#213-repository-vs-archive)
  * [2.2 Overview of the repository-software](#22-overview-of-the-repository-software)
    + [2.2.1 Zenodo](#221-zenodo)
    + [2.2.2 b2share](#222-b2share)
    + [2.2.3 Inspire](#223-inspire)
    + [2.2.4 DSpace](#224-dspace)
    + [2.2.5 Fedora](#225-fedora)
    + [2.2.6 Archivematica](#226-archivematica)
  * [2.3 Comparison](#23-comparison)
    + [2.3.1 Comparison Table DSpace, Fedora & Zenodo](#231-comparison-table-dspace,-fedora-&-zenodo)
    + [2.3.2 Resume](#232-resume)
- [3 Preservation](#3-preservation)
  * [3.1 Data Preservation](#31-data-preservation)
    + [3.1.1 Generall Meaning](#311-generall-meaning)
    + [3.1.2 Goal](#312-goal)
    + [3.1.3 Methods](#313-methods)
      - [3.1.4 Data Pyramid](#314-data-pyramid)
  * [3.2 Digital Preservation](#32-digital-preservation)
    + [3.2.1 Purpose](#321-purpose)
    + [3.2.2 Problems](#322-problems)
    + [3.2.3 Foundamentels](#323-foundamentels)
      - [3.2.3.1 Appraisal](#3231-appraisal)
      - [3.2.3.1 Identification](#3231-identification)
      - [3.2.3.1 Integrity](#3231-integrity)
      - [3.2.3.1 Fixity](#3231-fixity)
      - [3.2.3.1 Characterization](#3231-characterization)
      - [3.2.3.1 Sustainability](#3231-sustainability)
      - [3.2.3.1 Renderability](#3231-renderability)
      - [3.2.3.1 Physical media obsolescence](#3231-physical-media-obsolescence)
      - [3.2.3.1 Format obsolescence](#3231-format-obsolescence)
      - [3.2.3.1 Significant properties](#3231-significant-properties)
      - [3.2.3.1 Authenticity](#3231-authenticity)
      - [3.2.3.1 Access](#3231-access)
      - [3.2.3.1 Preservation metadata](#3231-preservation-metadata)
    + [3.2.4 Strategies](#324-strategies)
      - [3.2.4.1 Online Computer Library Center 4 Point Strategie](#3241-online-computer-library-center-4-point-strategie)
      - [3.2.4.2 Refreshing](#3242-refreshing)
      - [3.2.4.3 Migration](#3243-migration)
      - [3.2.4.3 Replication](#3243-replication)
      - [3.2.4.4 Emulation](#3244-emulation)
      - [3.2.4.5 Encapsulat](#3245-encapsulat)
      - [3.2.4.6 Persistent Archives concept](#3246-persistent-archives-concept)
      - [3.2.4.7 Metadata attachment](#3247-metadata-attachment)
    + [3.2.5 Software Preservation Network (SPN)](#325-software-preservation-network--spn-)
    + [3.2.6 The OAIS Reference Model](#326-the-oais-reference-model)
- [4 Further Reading](#4-further-reading)

---

## 1 Introduction
Our topic "FOSS Repositories and Preservation is dealing with Free/Libre Open Source Software to store any kind of research data. In a world where more and more data is produzed every day, these repositories provide software that can store and preserve reseach data used by many scientiest anywhere at any time. In the following we are introducing you to some of these softwares and the basic principles of preservation.

---

## 2 FOSS Repositories
### 2.1 Prerequesite Knowledge
#### 2.1.1 Data Repository Definition
- A data repository is a digital archive and provides a structured way for users to store, preserve and make available 
research data and their metadata 
- Permalinks are a common and comfortable mean for linking and citing datasets
- It is mostly used with version control systems to store multiple versions of files 
- While a repository _can_ be configured on a local machine for a single user, 
it is often stored on a server, which can be accessed by multiple users
#### 2.1.2 Basic Terminology
##### 2.1.2.1 Version Control
- A system that records changes to a file or set of files over time so that you can recall specific versions later
##### 2.1.2.2 Working Tree
- The tree of actual checked out files, normally containing the contents of the HEAD commit's tree and any local changes not yet committed
##### 2.1.2.3 Embargo
- When publishing a dataset, a user may choose to defer the date at which the data becomes available (for example, so that it is available at the same time as an associated article)
- This means that the description and files of that dataset are not publicly available until the embargo date is reached
- Meanwhile, some other information about the dataset - such as the contributors, title, citation and associated articles become available immediately, prior to the embargo
##### 2.1.2.4 Metadata Harvesting
- the Protocol for Metadata Harvesting ([OAI-PMH](https://en.wikipedia.org/wiki/Open_Archives_Initiative_Protocol_for_Metadata_Harvesting)) is developed to harvest(collect) descriptions of records so that services can be using metadata from many different archives
- typically used by CERN-based networks ([Invenio](https://github.com/inveniosoftware/invenio))
##### 2.1.2.5 DOI
- a Digital Object Identifier ([DOI](https://en.wikipedia.org/wiki/Digital_object_identifier)) is a persistent identifier used to uniquely identify objects
- are mainly in use to identify academic, professional, and government information, such as journal articles, research reports and data sets, and official publications
##### 2.1.2.6 REST
- Representational State Transfer ([REST](https://en.wikipedia.org/wiki/Representational_state_transfer)) is an architectural style that defines a set of constraints to be used for creating web services
- RESTful web services provide interoperability between computer systems
- using a stateless protocol and standard operations, REST systems aim for fast performance, reliability, and the ability to grow, by re-using components that can be managed and updated without affecting the system as a whole
##### 2.1.2.7 ORCID
- ORCID iD ([Open Researcher and Contributor ID](https://en.wikipedia.org/wiki/ORCID)) is a nonproprietary alphanumeric code to uniquely identify scientific and other academic authors and contributors
- addresses the problem that a particular author's contributions to the scientific literature or publications in the humanities can be hard to recognize as most personal names are not unique or can change during a lifespan
#### 2.1.3 [Repository vs. Archive](https://wikidiff.com/archive/repository)
- Archive and repository are often referred synonymous
- Archives are storage rooms for files kept for historical interest
- Whereas in repositories the main interest is preservation and safety of the data
### 2.2 Overview of the repository-software
#### 2.2.0 Invenio
[![Alt-Text](images/1157480.png)](https://github.com/inveniosoftware/invenio)
- open source software framework for large-scale digital repositories that provides the tools for management of digital assets in an institutional repository and research data management systems
- initially developed by CERN
- Stable version: 3.0.0 (07.07.18) 
#### 2.2.1 Zenodo 
[![Alt-Text](images/zenodo-gradient-2500.png)](https://github.com/zenodo/zenodo)
- Research data repository based on Invenio
- Created by OpenAIRE and CERN to provide a place for researchers to deposit datasets
- Launched in 2013, allowing researchers in any subject area to upload files up to 50 GB
- General-purpose open access repository

:warning: Installation-disclaimer
while installing Zenodo with docker, add in *docker-services.yml* 
>       - "INVENIO_CELERY_BROKER_URL=amqp://guest:guest@mq:5672//"

between those two lines

>       - "INVENIO_BROKER_URL=amqp://guest:guest@mq:15711//"
>       - "INVENIO_CACHE_REDIS_URL=redis://cache:6379/0"

#### 2.2.2 b2share 
[![Alt-Text](images/logo-b2share.png)](https://github.com/EUDAT-B2SHARE/b2share)
- Research data repository based on Invenio 
- Created by EUDAT CDI services
- Launched in 2014
#### 2.2.3 Inspire 
[![Alt-Text](images/inspire_logo_hep.png)](https://github.com/inspirehep/inspire)
- Open access digital library for the field of high energy physics based on Invenio
- Successor of the Stanford Physics Information Retrieval System (SPIRES) database
- Launched in 2012
#### 2.2.4 DSpace 
[![Alt-Text](images/DSpace_transparent_logo.png)](https://github.com/DSpace/DSpace)
- Open source repository software package typically used for creating open access repositories for scholarly and/or published digital content
- Shares some feature overlap with content management systems and document management systems, the software serves as a digital archives system, focused on the long-term storage, access and preservation of digital content
- initial release in 2002 developed from MIT and HP Labs
- Stable version: 6.2 (08.09.17)
#### 2.2.5 Fedora 
[![Alt-Text](images/fedora_logo_10in.png)](https://github.com/fcrepo4/fcrepo4)
- Modular open source repository system for the management and dissemination of digital content
- It is suited for digital libraries and archives, both for access and preservation of large and complex digital collections of historic and cultural materials as well as scientific data
- Stable version: Fedora 4.7.5 (12.02.18)
#### 2.2.6 Archivematica 
[![Alt-Text](images/ArchivematicaTranslucent.png)](https://github.com/artefactual/archivematica)
- web- and standards-based, open-source application which allows to preserve long-term access to digital content
- Stable version: 1.7.2 (11.09.18)
### 2.3 Comparison 
The comparison is focused on the most accessible data repositories of this list. 
This means the 3 out of 6 which seemed the most work-in-progress, 
most well-documented and for our studies best to apply.
#### 2.3.1 Comparison Table DSpace, Fedora & Zenodo

| Name             |                                                 | DSpace                                                                                               | Fedora                                                                     | Zenodo                                                                                                                            |
|------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Vision/Idea      |                                                 | produce a choice for repository software providing  means for open available and easy to manage data | advancement of open source software and content as collaborative community | open dependable deposit for science, enabling researchers  to share and preserve research outputs. Small layer on top of Invenio. |
| Infrastructure   | development language                            | [Java](https://docs.oracle.com/javase/7/docs/api/)                                                                                                 | Java                                                                       | [Python](https://www.python.org/) & JavaScript                                                                                                                           |
|                  | installation prerequesites                               | Java JDK 8, Apache Maven 3.x, Apache Ant 1.8x, PostgreSQL, Apache Tomcat 7 [↘](https://wiki.duraspace.org/display/DSDOC6x/Installing+DSpace#InstallingDSpace-HardwareRecommendations)                                                                     | Java 8, Tomcat 7 or Jetty 9.x [↘](https://wiki.duraspace.org/display/FEDORA4x/Deploying+Fedora+4+Complete+Guide#DeployingFedora4CompleteGuide-Downloads)                                                      | Docker, PostgreSQL, Elasticsearch 2.x, Redis and RabbitMQ [↘](https://github.com/zenodo/zenodo/blob/master/docker-compose.yml/)
| Interface        | front-end integration                           | Yes, [JSPUI](https://wiki.duraspace.org/display/DSDOC5x/JSPUI+Configuration+and+Customization)(Java) or [Manakin](https://wiki.duraspace.org/display/DSPACE/Manakin+theme+tutorial)(XML)                                                                     | Yes, [Islandora](https://github.com/islandora) or [Samvera](https://github.com/samvera/hydra-pcdm)                                                    | Yes, via [Zenodo REST API](http://developers.zenodo.org/) possible                                                                                                 |
|                  | customizable                                    | Yes                                                                                                  | Yes                                                                        | Yes                                                                                                                               |
| Metadata         | exporting shema filetype                        | [OAI-PMH](https://en.wikipedia.org/wiki/Open_Archives_Initiative_Protocol_for_Metadata_Harvesting), XML and [METs](https://de.wikipedia.org/wiki/Metadata_Encoding_%26_Transmission_Standard)                                                                                | OAI-PMH, [DC](https://en.wikipedia.org/wiki/Dublin_Core), [MODS](https://en.wikipedia.org/wiki/Metadata_Object_Description_Schema), XML;  others through conversion possible                | OAI-PMH, XML                                                                                                                      |
|                  | required/customizable                           | Yes/Yes                                                                                              | Yes/Yes                                                                    | Yes/Yes                                                                                                                           |
|                  | versioning                                      | Yes                                                                                                  | Yes                                                                        | Yes                                                                                                                               |
| Security/Privacy | embargos                                        | Yes                                                                                                  | Yes with modules possible                                                  | Yes                                                                                                                               |
|                  | private/public data                             | Yes                                                                                                  | Yes                                                                        | Yes                                                                                                                               |
|                  | access control/authentication                   | Yes(groups)/Yes(passwords, [LDAP](https://en.wikipedia.org/wiki/Lightweight_Directory_Access_Protocol), IP..)                                                               | Yes/Yes(LDAP, CAS..)                                                       | Yes(communities)/Yes(OAuth, access token)                                                                                         |
| Submission       | data types                                      | All types                                                                                            | All types                                                                  | All types                                                                                                                         |
|                  | size limit                                      | 1GB(can be increased up to 4GB)                                                                      | 1TB via RestAPI                                                            | 50GB(per dataset)                                                                                                                 |
|                  | data deposit APIs                               | [SWORD](http://guides.dataverse.org/en/latest/api/sword.html)                                                                                                | SWORD                                                                      | Zenodo REST API                                                                                                                   |
| Access/Sharing   | licensing                                       | Yes                                                                                                  | Yes                                                                        | Yes                                                                                                                               |
|                  | integration of other institutional repositories | Yes, via metada-harvesting(OAI-PMH)                                                                  | Yes, via metada-harvesting(OAI-PMH)                                        | Yes, via metada-harvesting(OAI-PMH)                                                                                               |
| Analysis         | visualization                                   | No                                                                                                   | Yes, but development required([Blacklight](http://projectblacklight.org/))                                  | Yes, with development possible                                                                                                    |
|                  | graphing of tables                              | No                                                                                                   | Yes, requires solution packs                                               | Yes, with development                                                                                                             |
|                  | geographic data                                 | Yes, requires development                                                                            | Yes, requires solution packs                                               | Yes, requires development                                                                                                         |
| Archiving        | author ID                                       | [ORCID](https://en.wikipedia.org/wiki/ORCID)                                                                                                | ORCID                                                                      | creator string in metadata                                                                                                        |
|                  | version control                                 | Yes                                                                                                  | Yes                                                                        | Yes                                                                                                                               |
|                  | citation & references                           | No                                                                                                   | Yes, scholar modules                                                       | Yes                                                                                                                               |
| Preservation     | redundancy                                      | No                                                                                                   | No                                                                         |                                                                                                                                   |
|                  | [DOI](https://en.wikipedia.org/wiki/Digital_object_identifier) capability                                  | Yes(interoperability with EZID/[DataCite API](https://support.datacite.org/docs/api))                                                         | Yes(DataCite community/collection level DOI)                               | Yes(DataCite community/collection level DOI)                                                                                      |
|                  | back-up options                                 | Yes(but issues with versioning)                                                                      | Yes                                                                        | ?                                                                                                                                 |
| Admin            | tracking                                        | [SOLR](https://en.wikipedia.org/wiki/Apache_Solr)                                                                                                 | SOLR                                                                       | Code of practice for research data usage                                                                                          |
|                  | usage/download reports                          | SOLR, elastic search(Manakin)                                                                        | SOLR                                                                       | Code of practice for research data usage                                                                                          |
| Publishing       | search API/optimization                         | [Lucence](https://de.wikipedia.org/wiki/Apache_Lucene)(Java)                                                                                        | GSearch                                                                    | Zenodo REST API                                                                                                                   |
|                  | publishing workflow                             | JSPUI & [XMLUI](https://wiki.duraspace.org/display/DSDOC6x/XMLUI+Configuration+and+Customization)                                                                                        | Yes                                                                        | ?                                                                                                                                 |
|                  | RSS/social media integration                    | Yes/Yes(development required)                                                                        | Yes/?                                                                      | ?/?                                                                                                                               |
|                  | community/curators                              | Yes                                                                                                  | Yes(requires development)                                                  | Yes                                                                                                                               |
|                  | deletions possible                              | Yes                                                                                                  | Yes([CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete))                                                                  | Yes                                                                                                                               |
#### 2.3.2 Resume
- particular differences between them, which includes almost every aspect of the development process
- in the decision-process on what to pick for the project, it is about personal preferences only
- there is not a difference in difficulty of developing with one of the repositories 
- however for the most Invenio-type repositories there are docker-compose files available to simply setup the developent environment
- whereas there is not in DSpace and over the course of over 15 years of development, there has been build a big framework of software and a big load of dependencies which leads automatically to more and more effort setting it up

---

## 3 Preservation
### 3.1 Data Preservation 
[_Wikipedia Link_](https://en.wikipedia.org/wiki/Data_preservation) 
#### 3.1.1 Generall Meaning
- act of conserving and maintaining both the safety and integrity of data
#### 3.1.2 Goal
- the accurate rendering of authenticated content over time
    -“When data is lost it is as though it never existed”
#### 3.1.3 Methods
- Digital:
    - Digital Preservation: formal endeavor to ensure that digital information of continuing value remains accessible and usable
        -combination of "policies, strategies and actions that ensure this
- Archives:
    - collection of historical documents and records
- Catalogues, directories and portals:
    - consolidated resources which are kept by individual institutions
- Cyber Infrastructures:
    - consists of archive collections which are made available through the system of hardware, technologies, software, policies, services and tools
- Repositories:
    - Repositories are places where data archives and holdings can be accessed and stored. The goal of repositories is to make sure that all requirements and protocols of archives and holdings are being met, and data is being certified to ensure data integrity and user trust
    - Single-site Repositories
    - Multi-Site Repositories
    - Trusted Digital Repostitory (TDR)
        -must cooperate with the Reference Model for an Open Archival Information System, as well as adhere to a set of rules or attributes that contribute to its trust such as having persistent financial responsibility, organizational buoyancy, administrative responsibility security and safety
##### 3.1.4 Data Pyramid

![Alt-Text](images/DataPyramid.png)
<br>[_Source: Francine Berman, Got data?: a guide to data preservation in the information age (2008)_](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&ved=2ahUKEwi7jYrPmYPeAhWCFywKHQjJBBQQFjAAegQIAxAC&url=http%3A%2F%2Fwww.itpb.ucla.edu%2Fdocuments%2F2009%2Fp50-berman.pdf&usg=AOvVaw111q-vKcfasHBz12FnAg8K)

### 3.2 Digital Preservation
[_Wikipedia Link_](https://en.wikipedia.org/wiki/Digital_preservation) 
#### 3.2.1 Purpose
- [Digital Revolution](http://www.dcc.ac.uk/digital-curation/why-preserve-digital-data) make it easy to create, copy and transmit data all over the world
    - -->increasingly vast amounts of digital research data
- Research data are unique and cannot be replaced if destroyed or lost
- Where resources are "born digital", there is no other format but the digital original
- good practice for institutions and researchers to manage and retain their research data
- A data preservation programme suited to the individual institution must be used to safeguard this huge investment of time and resources
- “[Digital Heritage](http://www.unesco.org/new/en/communication-and-information/access-to-knowledge/preservation-of-documentary-heritage/digital-heritage/concept-of-digital-heritage/)” has cultural, historical, aesthetic, archaeological, scientific, ethnological or anthropological value and is increasing
#### 3.2.2 Problems
- Technological advances even more rapidly, reducing the time before a technology becomes obsolete
- Data is recorded on a transient medium, in a specific file format and needs a transient coding scheme to interpret them
- Machine needs to be interposed between the data ant the human interpreter
- Selecting the right data is difficult because there are many points of view and these are changing from time to time
#### 3.2.3 Foundamentels
##### 3.2.3.1 Appraisal
- Process of identifying records and other materials to be preserved by determining their permanent value. It is a difficult and critical process because the remaining selected records will shape researchers’ understanding of that body of records, or fonds. Archival appraisal may be performed once or at the various stages of acquisition and processing
##### 3.2.3.1 Identification
- Identification through assigned identifiers and accurate descriptive metadata. An identifier is a unique label that is used to reference an object or record, usually manifested as a number or string of numbers and letters. As a crucial element of metadata to be included in a database record or inventory, it is used in tandem with other descriptive metadata to differentiate objects and their various instantiations
##### 3.2.3.1 Integrity
- Assurance that the data is "complete and unaltered in all essential respects". Is the Cornerstone of Preservation. Unintentional changes to data are to be avoided, and responsible strategies put in place to detect unintentional changes and react as appropriately determined
##### 3.2.3.1 Fixity
- Process of validating that a file has not changed or been altered from a previous state. While checksums are the primary mechanism for monitoring fixity at the individual file level, an important additional consideration for monitoring fixity is file attendance
##### 3.2.3.1 Characterization
- Characterization of digital materials is the identification and description of what a file is and of its defining technical characteristics often captured by technical metadata, which records its technical attributes like creation or production environment
##### 3.2.3.1 Sustainability
- Unlike traditional, temporary strategies, and more permanent solutions, digital sustainability implies a more active and continuous process. Digital sustainability concentrates less on the solution and technology and more on building an infrastructure and approach that is flexible with an emphasis on interoperability, continued maintenance and continuous development
##### 3.2.3.1 Renderability
- continued ability to use and access a digital object while maintaining its inherent significant properties
##### 3.2.3.1 Physical media obsolescence
- Physical media obsolescence can occur when access to digital content requires external dependencies that are no longer manufactured, maintained, or supported. External dependencies can refer to hardware, software, or physical carriers. 
##### 3.2.3.1 Format obsolescence
- File format obsolescence can occur when adoption of new encoding formats supersedes use of existing formats, or when associated presentation tools are no longer readily available.Factors that should enter consideration when selecting sustainable file formats include disclosure, adoption, transparency, self-documentation, external dependencies, impact of patents, and technical protection mechanisms.
##### 3.2.3.1 Significant properties
- Significant properties refer to the "essential attributes of a digital object which affect its appearance, behavior, quality and usability" and which "must be preserved over time for the digital object to remain accessible and meaningful."
##### 3.2.3.1 Authenticity
- Whether analog or digital, archives strive to maintain records as trustworthy representations of what was originally received. Authenticity has been defined as “. . . the trustworthiness of a record as a record; i.e., the quality of a record that is what it purports to be and that is free from tampering or corruption”
##### 3.2.3.1 Access
- Digital preservation efforts are largely to enable decision-making in the future. Should an archive or library choose a particular strategy to enact, the content and associated metadata must persist to allow for actions to be taken or not taken at the discretion of the controlling party
##### 3.2.3.1 Preservation metadata
- There has to be information that documents the preservation process throughout the whole lifecycle of the data
#### 3.2.4 Strategies
##### 3.2.4.1 Online Computer Library Center 4 Point Strategie
- 1.Assessing the risks for loss of content posed by technology variables such as commonly used proprietary file formats and software applications
- 2. Evaluating the digital content objects to determine what type and degree of format conversion or other preservation actions should be applied
- 3. Determining the appropriate metadata needed for each object type and how it is associated with the objects
- 4. Providing access to the content
##### 3.2.4.2 Refreshing
- Refreshing is the transfer of data between two types of the same storage medium so there are no bitrot changes or alteration of data. This process has to be carried out whatever other preservation strategies are adopted and has a low risk of losing data if executed and documented properly 
##### 3.2.4.3 Migration
- Migration is the transferring of data to newer system environments; it involves change in the configuration of the underlying data without changing their intellectual content. It is time-critical and needs to be carried out as soon as new formats are introduced and before the current format gets obsolete
##### 3.2.4.3 Replication
- Creating duplicate copies of data on one or more systems is called replication. Data that exists as a single copy in only one location is highly vulnerable to software or hardware failure, intentional or accidental alteration, and environmental catastrophes like fire, flooding, etc
##### 3.2.4.4 Emulation
- Emulation is the replicating of functionality of an obsolete system. Emulation does not focus on the digital object, but on the hard- and software environment in which the object is rendered. It aims at (re)creating the environment in which the digital object was originally created. Used for more complex data where migration will lead to loss of data
##### 3.2.4.5 Encapsulat
- This method maintains that preserved objects should be self-describing, virtually "linking content with all of the information required for it to be deciphered and understood"
##### 3.2.4.6 Persistent Archives concept
- This method requires the development of comprehensive and extensive infrastructure that enables "the preservation of the organisation of collection as well as the objects that make up that collection, maintained in a platform independent form"
##### 3.2.4.7 Metadata attachment
- Metadata attached to digital files may be affected by file format obsolescence. Preservation strategies are only successful if the data is fully documented throughout their lifecycle
#### 3.2.5 Software Preservation Network (SPN)
- leading organization established to facilitate and support software preservation efforts
- preserves software through community engagement, infrastructure support, and knowledge generation
- Values:
    - Community
        - “Software spans sectors, industries and disciplinary domains. Through our shared community of practice we develop a body of shared tools, responses and strategies for preservation, reuse and sharing of software”
    - Sustainability
        - “Sustainable preservation is not achieved by a single decision or action. It requires a series of decisions made by multiple actors and stakeholders over the lifecycle of digital resources.”
    - Access
        - “Access must accommodate current and future users. The Access Breakdown is the breakdown of social structures that support information access; this breakdown necessitates system level change that acknowledges software as infrastructure.”
    - Transparency
        - “True transparency is culturally ingrained in the DNA of the organization. It encourages constructive questioning and honest probing focused on mission and guided by core beliefs.”
    - Advocacy
        - People or groups advocate to influence decisions within political, economic and social systems. “[advocacy] is integral to all aspects of archival work.”
- [_SPN Website Link_](http://www.softwarepreservationnetwork.org/)
#### 3.2.6 The OAIS Reference Model
- The functional model gives a detailed break-down of digital preservation and dissemination workflows – in short, it explains how an (idealized) archive works. It therefore is a good starting point for anyone who seeks to obtain a systematic overview of these workflows or wants to analyze and understand workflows in an existing archive.

![Alt-Text](images/OAIS1.png)

![ALT-Text](images/OAIS2.png)
<br>[_Source: OAIS Reference Model_](http://cessda.net/content/download/496/4465/file/CESSDA%20User%20Guide%20for%20digital%20preservation_2_OAIS.pdf)

#### 4 Further Reading
- Marilyn Deegan & Simon Tanner, Digital Preservation (2006)
- Francine Berman, Got data?: a guide to data preservation in the information age (2008)
- [_Long term preservation of scientific data: Lessons from jet and other domains_](https://www.sciencedirect.com/science/article/pii/S0920379612003225)
- [_GESIS Long Term Preservation_](https://www.gesis.org/en/services/archiving-and-registering/data-archiving/long-term-preservation/)
- [_NASA Earth Science Data Preservation Content Specification_](https://earthdata.nasa.gov/user-resources/standards-and-references/preservation-content-spec)

