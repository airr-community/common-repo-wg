Recommendations from the Common Repository Working Group
========================================================

Establishing Guidelines for the Formation and Function of an Open Data
Repository for the Adaptive Immune Receptor Repertoire (AIRR) community

Authors: Bjoern Peters, Yariv Wine, David Klatzmann, Uri Laserson, Adrian
Thorogood, Sanchita Bhattacharya, Brian Corrie, Holly Longstaff, Tony Moody,
Corey Watson, Lindsay Cowell

v0.1.0
June 2016

**Overview.**  The use of high-throughput sequencing for profiling B-cell and
T-cell receptors has resulted in rapid increases in data generation in recent
years. As is now the case for many burgeoning data-driven fields in the life
sciences, this places strong demands on researchers to not only establish a
clear set of community-accepted data standards, resources, and analysis
methods, but also a clear functional and structural framework for a common
space in which generated receptor repertoire data can be deposited, stored, and
publicly shared in perpetuity.

Over the course of the past 12 months, the AIRR Common Repository Working Group
(**CRWG**) has met bi-weekly to discuss and debate issues and ideas centered
around the development of a community-wide common data repository. This effort
has culminated in a draft set of recommended guidelines in four key areas,
summarized below:

1. **Data Sharing and Access**: Includes recommendations pertaining to data
   sharing requirements/mandates, access restrictions, use of protected health
   information (**PHI**), donor informed consent, and intellectual property.

2. **Repository Infrastructure**: Includes recommendations and rationale for
   the utilization of a model that would leverage distributed repositories that
   are    integrated through a Central Registry. Detailed recommendations that
   pertain    to compliance criteria for registered repositories, specific data
   frameworks, and existing technologies able to support cross-repository
   functionality are also included in this section.

3. **Data to be Shared**: Includes recommendations on depositing processed and
   raw data in registered repositories and existing databases (e.g., SRA, IEDB,
   dbGaP and ImmPort).

4. **Coordination with the NIH Data Commons**: Includes recommendations
   centered on the adherence to standards being adopted by the broader
   scientific research community. Specifically, the Digital Object Compliance
   principles established as part of the NIH Data Commons Initiative.

**Requested Feedback from AIRR attendees.** It is the intent of the CRWG that
the draft recommendations detailed below serve as a solid foundation for a
directed discussion during the AIRR 2016 meeting, with the expressed aim of
deciding on a clear set of initiatives/goals for moving forward on the
establishment of a common AIRR repository. With this in mind, there are several
areas in which we would especially like input from AIRR attendees:

1. What data should be deposited in an AIRR repository?

2. What should the compliance criteria be for a registered repository?

3. What types of a) data queries, b) data formats/frameworks, and c)
   technologies should be supported/used by registered repositories?

4. To which existing databases should raw data be deposited? Should this be
   required for publication and/or grant funding?

5. Should there be any exceptions made for particular parties regarding
   requirements to submit raw data?

6. Other outstanding questions?


Recommendations
---------------

The AIRR Common Repository Working Group (**CRWG**) was tasked with developing
a set of recommendations for the formation of an Open Data Repository where
scientists can deposit, share, find, and reuse adaptive immune receptor
repertoire sequencing data. The current set of recommendations is detailed
below and covers a range of topics, including repository content and structure.
These recommendations should be considered a draft set for community review and
input. We welcome suggested revisions before, during, and after the AIRR June
2016 meeting.  Please join the discussion at
[https://github.com/airr-data](https://github.com/airr-data).

**Note**: A compliant repository is a repository that adheres to the
recommendations listed below:

* Recommendations 2 and 6 on Data Sharing and Access;
* Recommendations 10, 12, and 13 on Infrastructure;
* Recommendation 17 on Data To Be Shared;
* Recommendation 20 on Coordination with the NIH Data Commons.

The CRWG recognizes two levels of compliance: administrative and technical. A
repository is considered to have administrative compliance when Recommendations
2 and 4 are adhered to. A repository is considered to have technical compliance
when Recommendations 7, 9, 14, and 17 are adhered to. We recommend that only
repositories with both administrative and technical compliance be included in
the Central Registry described in Recommendations 5 and 6.


### Detailed Recommendations on Data Sharing and Access

1. The CRWG strongly recommend that funders and journals require the sharing of
   all repertoire sequencing data through a compliant repository.

2. We strongly recommend that compliant repositories provide open access to
   repertoire sequencing data for broad redistribution and reuse, meaning that
   anyone can freely access and use repertoire-sequencing data for any purpose.
   This position is in line with a broader push in science towards Open Data.

    1. While restricted access is typically applied to human whole-genome
       sequencing data, the position of this working group is that repertoire
       sequencing data are analogous to several kinds of data which are
       routinely shared without restricted access:

        1. HLA typing data,

        2. RNA-Seq data,

        3. Cancer sequencing data in which somatic mutations are shareable.

3. In support of Recommendation 2, we recommend that any repository that
   chooses to host personally identifiable information or protected health
   information, do so in such a way that the securing of these data does not
   impede access to the repertoire sequencing data and its associated, non-
   identifiable, non-protected metadata.

4. In support of Recommendation 2, we recommend that repositories require
   submitters, during the data submission process, to attest that they have
   sought appropriate informed consent or authorization for sharing, where
   necessary.

5. In support of Recommendation 2, we encourage the AIRR Community to develop
   consistent and compatible consent documents, and as a best practice, to seek
   consent from individuals for the broad sharing of their repertoire data,
   where this is feasible and appropriate.

6. In line with Recommendation 2, we recommend that no intellectual property
   restrictions or other proprietary interests, such as commercial funder
   reach-through, be imposed on data deposited in a compliant repository.

    1. In addition to reducing usability of the resource, supporting such
       restrictions complicates the design and implementation of query and
       reporting interfaces.

7. While we recommend that there be no restrictions on the use of repertoire
   sequencing data, we recommend that repositories encourage and facilitate
   appropriate attribution and citation.


 ### Detailed Recommendations on Repository Infrastructure

8. The CRWG recommends a set of multiple distributed repositories supported by
   a centralized registry. We recommend consistency with an intermediate
   distributed model, as described in
   [10.1126/science.aaa7485](http://science.sciencemag.org/content/350/6266/1312.full).

    1. The advantages of a distributed approach include:

        1. There are multiple repositories in existence, and these will not go
           away in the near future. Thus, an inclusive approach is more likely
           to get community buy-in.

        2. Supporting only one repository from the outset is likely to result
           in a suboptimal solution. It is preferable, as was done with the
           NIAID-funded Bioinformatics Resource Centers (BRCs), to start with a distributed
           approach and allow consolidation to one or a smaller number of
           repositories to happen as a function of performance.

        3. Agreeing on standards to enable interoperability is feasible.

        4. There are technologies available that enable cross-repository
           queries (such as the Beacon system used by GA4GH).

    2. The disadvantages of a distributed approach include

        1.  Duplication of effort and resources.

        2. The need to either synchronize data across resources, or to provide
           federated query interfaces (as in federated search, not federated
           database management system).

    3. The position of the CRWG is that the advantages of a distributed
       approach outweigh the disadvantages.

9. We recommend maintaining a Central Registry of compliant repositories, as
   defined above. This registry may implement an interface that supports cross-
   repository queries for a standard set of queries.

10. We strongly recommend that the conditions for inclusion in the Central
    Registry be that a repository provides unrestricted access to repertoire
    sequencing data and its associated non-identifiable, non-protected
    metadata, as outlined in Recommendations 2 and 6 above, and it supports:

    1. Standardized data elements with exact (computable) specifications;

    2. A standardized set of queries;

    3. A standardized data submission process (including standardized data and
       metadata formats).

11. We recommend that AIRR Working Groups be the forum for the AIRR Community
    to establish (and revise when appropriate) the required standards outlined
    in Recommendation 10.

12. We strongly recommend the use of a standard, open source, data
    serialization framework for ensuring interoperability, performance,
    maintainability, and evolvability. We recommend that AIRR Working Groups be
    the forum for the AIRR Community to decide upon a specific framework.
    Compliant repositories should commit to adopting the recommended framework.

    1. Examples of currently available frameworks are Apache Avro, Thrift, and
       Protocol Buffers.

    2. The current recommendation of the CRWG is Thrift.

13. We recommend that a compliant repository implement an interface that
    supports an agreed-upon set of standard queries. The interface
    implementation should be compatible with the data communication protocol in
    Recommendation 12.


 ### Detailed Recommendations on Data to be Shared

14. For any repertoire-sequencing study, the CRWG strongly recommends sharing
    of raw read sequence and quality score data, as well as processed and
    annotated data.

    1. Commercial services for AIRR sequencing (e.g., Adaptive Biotechnologies,
       iRepertoire, Distributed Bio, etc.) are becoming increasingly popular,
       but they do not have a standard for returning data, and in some cases
       they do not return raw data. We recommend that the AIRR Community
       directly engage with companies to ensure that the data they return to
       users will be compliant with the AIRR repositories.

15. We recommend that raw-read sequence and quality-score data be shared via
    deposition in the SRA.

    1. The advantages of using the SRA include:

        1. It is an established infrastructure funded for perpetuity.

        2. Its infrastructure is already designed to handle data on this scale.

        3. Users will expect repertoire-sequencing data to be there.

    2. The disadvantage of using the SRA is that it is a general-purpose
       resource. Thus, the metadata capture and query and reporting interfaces
       are not optimal for our user community. The SRA will allow some
       customization of metadata capture, however, and we recommend that AIRR
       working groups work with the SRA to do this. This disadvantage is
       further mitigated by the metadata, queries, and reports that will be
       supported by compliant repertoire-sequence data repositories described
       in Recommendation 16.

16. We recommend that dedicated repositories for repertoire-sequencing data be
    established for hosting processed repertoire-sequencing data and
    annotations, and that these constitute the nodes in the distributed-
    repository network described in Recommendation 8.

17. We recommend that compliant repositories be required to link to the raw
    data in the SRA.

18. We recommend: (i) that adaptive immune-receptor sequences for which
    epitopes are known be deposited in IEDB, (ii) that links be maintained to
    the raw data in the SRA, and (iii) that links to the processed data and
    annotations be maintained in a compliant repertoire-sequencing data
    repository.

    1. This recommendation is intended to clarify how an existing resource,
       IEDB, should be tied into the repertoire-sequencing data-repository
       framework.

    2. This recommendation is intended to ensure that receptor data and epitope
       data be linked.

19. We recommend that adaptive immune-receptor repertoire-sequencing studies be
    registered in ImmPort, that links be maintained to the raw data in the SRA,
    and the processed data and annotations in a compliant repertoire sequence
    data repository. Links within ImmPort should also be maintained to other
    data types generated within the same study.

    1. This recommendation is intended to clarify how an existing resource,
       ImmPort, should be tied into the repertoire-sequencing data-repository
       framework.

    2. This recommendation is intended to ensure that receptor data are linked
       to other data types collected from the same subjects.


 ### Detailed Recommendations on Coordination with the NIH Data Commons

20. The CRWG recommends adherence to the Digital Object Compliance principles
    being developed as part of the NIH Data Commons Initiative
    (https://datascience.nih.gov/commons/). The principles are designed to
    ensure that digital objects are Findable, Accessible, Interoperable, and
    Reproducible (FAIR).

    1. Currently, the most basic level of Digital Object Compliance expects
       digital objects to have:

        1. Unique digital object identifiers;

        2. A minimal set of searchable metadata;

        3. Physical availability through a cloud-based Commons provider;

        4. Clear access rules and controls;

        5. An entry (with metadata) in one or more indices.

21. Regarding Recommendation 20.1.1, we recommend a system for assigning
    unique identifiers that ensures coordination among the distributed
    repositories and a central registry. A system, like that used by the OBO
    Foundry to coordinate ontology term identifiers across orthogonal
    ontologies, could be used as a model.

22. Recommendation 20.1.2-5 are met via adherence to Recommendations 2, 6, 8,
    10, and 16.


### Future Work for the AIRR Working Groups

The above recommendations imply future work to be jointly undertaken by the
AIRR Working Groups, including:

1. Development of consent language, according to Recommendation 5;

2. Development of standardized data elements with computable specifications,
   queries to be supported by the distributed repositories, and a standardized
   data submission process and associated submission formats, according to
   Recommendation 10;

3. More detailed specification on recommended technologies for implementation,
   such as are mentioned in Recommendations 12 and 13;

4. Development of customized metadata for repertoire-sequencing data in the
   SRA, according to Recommendation 15.
