Recommendations from the AIRR Common Repository Working Group
=============================================================

Authors: Sanchita Bhattacharya, Tania Bubela, Brian Corrie, David Klatzmann,
Uri Laserson, Holly Longstaff, Tony Moody, Bjoern Peters, Adrian Thorogood,
Yariv Wine, Corey Watson, Lindsay Cowell

v0.2.0 (draft)
August 2016


Background
----------

The use of high-throughput sequencing for profiling B-cell and T-cell receptors
has resulted in a rapid increase in data generation. It is timely, therefore,
for the Adaptive Immune Receptor Repertoire (AIRR) community to establish a
clear set of community-accepted data and metadata standards; analytical tools;
and policies and practices for infrastructure to support data deposit,
curation, storage and use. Such actions are in accordance with international
funder and journal policies that promote data deposition and data sharing – at
a minimum, data on which scientific publications are based should be made
available immediately on publication. Data deposit in publicly accessible
databases ensures that published results may be validated. Such deposition also
facilitates reuse of data for the generation of new hypotheses and new
knowledge.

The AIRR Common Repository Working Group (CRWG) developed a set of
recommendations that promote the deposit, sharing, and use of AIRR sequence
data. These recommendations were refined following community discussion at the
AIRR 2016 Community Meeting: Progress in Standards, Tools and a Common
Repository for Adaptive Immune Receptor Repertoire Data held at the National
Institutes of Health, Rockville, Maryland, USA from June 27-30, 2016.

The first three sets of recommendations: (1) state the general principles for
sharing of AIRR sequence data [hereinafter data]; (2) outline the
characteristics of compliant repositories for data deposit, storage and access;
and (3) describe a distributed model for compliant repositories for AIRR data,
linked by a central registry. The fourth set of recommendations are specific to
existing repositories of related data types. The concluding section addresses
next steps for the AIRR CRWG and the AIRR community more broadly.


Statement of Principles -- AIRR Data Sharing
--------------------------------------------

**Recommendation 1: Facilitate deposit, access and use of data.** To facilitate
data deposit and enable access and use, data should be made available under the
least restrictive terms possible (see Recommendation 3). The default data
sharing policy should be to deposit data in a public domain database with no
restrictions over deposit, access, storage, curation, and use.

**Recommendation 2: No intellectual property restrictions.** Depositors of data
and repositories should have no right to interfere with access to and use of
the data by others, including through the assertion of any intellectual
property rights.

**Recommendation 3: Legal exceptions.** Exceptions to open data sharing
(Recommendation 1) should only be considered in rare circumstances that require
compliance with local laws (e.g., privacy/health information) and Institutional
Review Boards (e.g., respect for participant consent).


Compliant AIRR Data Repositories
--------------------------------

**Recommendation 4: Raw-read sequence and quality-score data should be shared
via deposition in the Sequence Read Archive (SRA)** -
http://www.ncbi.nlm.nih.gov/sra. The AIRR Working Groups should work with the
SRA to customize metadata capture for AIRR data.

**Recommendation 5: Dedicated AIRR repositories should be established for
hosting processed repertoire-sequencing data and annotations.** These
repositories should link to the raw data in SRA (see Recommendation 4).

**Recommendation 6: Compliant AIRR data repositories should state policies and
practices that comply with Recommendations 1-3.** In addition, compliant
repositories should require submitters, during the data submission process, to
attest that they have sought appropriate informed consent or other
authorization for sharing, where necessary.

**Recommendation 7: The AIRR Working Groups should collaboratively develop
operational criteria for compliant repositories.** At the operational level, a
compliant repository should use a standard, open source, data serialization
framework for ensuring interoperability, performance, maintainability, and
evolution (e.g., Apache Avro, Thrift, and Protocol Buffers – the CRWG currently
recommends Thrift). Operational Criteria should include implementation of:

1. standardized data elements with exact (computable) specifications;
2. a standardized data submission process (including standardized data and
   metadata formats);
3. a standardized set of queries;
4. a system for assigning unique identifiers that ensures coordination among
   repositories/registries, for example, the system used by the OBO Foundry to
   coordinate ontology term identifiers across orthogonal ontologies.

**Recommendation 8: A compliant repository should adhere with the Digital
Object Compliance Principles**, under development as part of the NIH Data
Commons Initiative (https://datascience.nih.gov/commons/ ). The principles are
designed to ensure that digital objects are Findable, Accessible,
Interoperable, and Reproducible (FAIR). Currently, the most basic level of
Digital Object Compliance expects digital objects to have:

1. Unique digital object identifiers;
2. A minimal set of searchable metadata;
3. Physical availability through a cloud-based Commons provider;
4. Clear access rules and controls; and
5. An entry (with metadata) in one or more indices.

**Recommendation 9: Hosting PII or PHI.** For repositories that choose to host
personally identifiable information (PII) or protected health information
(PHI), the securing of these data should not impede access to the repertoire
sequencing data and its associated, non-identifiable, non-protected metadata.


System of Distributed Repositories Supported by a Centralized Registry
----------------------------------------------------------------------

**Recommendation 10: The dedicated AIRR repositories (Recommendation 5) should
comprise a system of multiple, distributed repositories supported by a
centralized registry** consistent with an intermediate distributed model
(http://science.sciencemag.org/content/350/6266/1312.full).

**Recommendation 11: Maintain a central registry of compliant repositories.**
The registry may implement an interface that supports cross-repository queries
for a standard set of queries.


Specific Recommendations for Common Datatypes and Existing Repositories of Related Data Types
---------------------------------------------------------------------------------------------

**Recommendation 12: AIRR sequences for which epitopes are known should be
deposited in the Immune Epitope Database (IEDB)** - http://www.iedb.org/.
Links should be maintained to the raw data in the SRA and to the processed data
and annotations in a compliant AIRR data repository.

**Recommendation 13: AIRR sequencing studies should be registered in ImmPort.**
Links should be maintained to the raw data in the SRA and the processed data
and annotations in a compliant AIRR data repository. Links within ImmPort
should also be maintained to other data types generated within the same study.


Next Steps for AIRR CRWG, Other Working Groups, and the AIRR Community/Association
----------------------------------------------------------------------------------

**Next Step 1**: The AIRR CRWG should work collaboratively with the other
Working Groups to finalize these recommendations and the recommendations from
the other Working Groups so that all recommendations may be approved by the
AIRR community, through a new association or a poll of attendees of community
meetings.  Specifically, collaborative efforts with other Working Groups should
focus on:

1. development of customized metadata for AIRR sequencing data in the SRA;
2. development of standardized data elements with computable specifications, queries to be supported by the distributed repositories, and a standardized data submission process and associated submission formats; and
3. development of more detailed specifications for recommended technologies for implementation.

**Next Step 2**: The AIRR Community/Association will need to work with
repositories to establish an accreditation system for compliant repositories.
This should include an appropriate system for the citation/attribution of the
repository and/or the data.

**Next Step 3**: The AIRR Community/Association will need to seek funding to
develop and maintain a central registry of compliant repositories.

**Next Step 4**: The AIRR Community/Association will need to seek funding to
develop and maintain dedicated repositories for AIRR data.

**Next Step 5**: The AIRR Community/Association will need to work with funders
and journals to establish mechanisms for compliance with these recommendations.

**Next Step 6**: The AIRR Community/Association should work to develop
consistent consent documents that are compliant with best practices for the
broad sharing of AIRR data.
