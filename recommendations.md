Recommendations from the AIRR Common Repository Working Group
=============================================================

Working Group Members: Meredith Ashby, Felix Breden, Syed Ahmad Chan Bukhari, Tania Bubela, 
Scott Christley, Brian Corrie, David Klatzmann,
Uri Laserson, Bjoern Peters, Adrian Thorogood,
Yariv Wine

Working Group Co-Chairs: Lindsay Cowell, Corey Watson

v0.5.0 (draft), August 2018


Background
----------

The use of high-throughput sequencing for profiling B-cell and T-cell receptors
has resulted in a rapid increase in data generation. It is timely, therefore,
for the Adaptive Immune Receptor Repertoire (AIRR) community to establish a
clear set of community-accepted data and metadata standards; analytical tools;
and policies and practices for infrastructure to support data deposit,
curation, storage, and use. Such actions are in accordance with international
funder and journal policies that promote data deposition and data sharing – at
a minimum, data on which scientific publications are based should be made
available immediately on publication. Data deposit in publicly accessible
databases ensures that published results may be validated. Such deposition also
facilitates reuse of data for the generation of new hypotheses and new
knowledge.

The AIRR Common Repository Working Group (CRWG) developed a set of
recommendations that promote the deposit, sharing, and use of AIRR sequence
data. These recommendations were refined following community discussions at the
AIRR 2016 and 2017 Community Meetings
(https://www.antibodysociety.org/airr-meetings). 

The first three sets of recommendations: (1) state the general principles for
sharing of AIRR sequence data [hereinafter data]; (2) outline the
characteristics of compliant repositories for data deposit, storage, and access;
and (3) describe an AIRR Data Commons - a distributed model for compliant repositories for AIRR data
linked by a central registry. The fourth set of
recommendations are specific to existing repositories of related data types.
The concluding section addresses next steps for the AIRR CRWG and the AIRR
community more broadly.


Statement of Principles -- AIRR Data Sharing
--------------------------------------------

**Recommendation 1: Facilitate deposit, access, and use of data.** To enable and facilitate
data deposit and broad access and use, data should be made available under the
least restrictive terms possible. The default data
sharing policy should be to deposit data in a public domain database with no
restrictions over deposit, access, storage, curation, and use.

**Recommendation 2: No intellectual property restrictions.** For data deposited in public domain 
databases/repositories, depositors of data
and repositories should have no right to interfere with access to and use of
the data by others, including through the assertion of any intellectual
property rights.

**Recommendation 3: Legal exceptions.** Exceptions to open data sharing
(Recommendation 1) should only be considered in rare circumstances that require
compliance with local laws (e.g., privacy/health information) and Institutional
Review Boards (e.g., respect for participant consent).

**Recommendation 4: Commercially valuable AIRR sequence data.** AIRR sequence data may be commercially valuable. In exceptional circumstances, where there is an intent to commercialize AIRR sequence data and/or associated materials, data generators may be prevented from publicly sharing those sequences/materials of potential value. In these cases, data generators are nevertheless encouraged to share the data using individually/institutionally negotiated legal instruments. 


Compliant AIRR Data Repositories
------------------------------------------------------------

**Recommendation 5: For long-term storage, data and metadata should be deposited in databases of the International Nucleotide Sequence Database Collaboration (INSDC)**, per the recommendations established by the AIRR Minimal Standards Working Group. The AIRR Working Groups should work with INSDC and its individual databases to customize metadata capture for AIRR data.

**Recommendation 6: Dedicated AIRR repositories should be established for
hosting processed repertoire-sequencing data and annotations** to facilitate data queries and cross-study meta-analyses. These repositories should link to the raw data deposited in INSDC databases (see Recommendation 5).

**Recommendation 7: Compliant AIRR data repositories should state policies and
practices that comply with Recommendations 1-4.** In addition,
repositories should require submitters, during the data submission process, to
attest that they have sought appropriate informed consent or other
authorization for sharing, where necessary. AIRR data repositories will not be required to host data that have access restrictions, but they may choose to do so on an individual basis.

**Recommendation 8: The AIRR Working Groups should collaboratively develop
operational criteria for compliant repositories.** At the operational level, a compliant repository should use a standard, open source, data serialization
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

**Recommendation 9: A compliant repository should adhere to the Digital
Object Compliance Principles**, under development as part of the NIH DataCommons 
Initiative (PMC4792175). The principles are
designed to ensure that digital objects are Findable, Accessible,
Interoperable, and Reusable (FAIR). Currently, the most basic level of
Digital Object Compliance expects digital objects to have:

1. Unique digital object identifiers;
2. A minimal set of searchable metadata;
3. Physical availability through a cloud-based Commons provider;
4. Clear access rules and controls; and
5. An entry (with metadata) in one or more indices.

**Recommendation 10: Hosting PII or PHI.** For repositories that choose to host
personally identifiable information (PII) or protected health information
(PHI), the securing of these data should not impede access to the repertoire
sequencing data and its associated, non-identifiable, non-protected metadata.


AIRR Data Commons - A System of Distributed Repositories Supported by a Centralized Registry
----------------------------------------------------------------------

**Recommendation 11: The dedicated AIRR repositories (Recommendations 5) should
comprise a system of multiple, distributed repositories supported by a
centralized registry** consistent with an intermediate distributed model as described in
http://science.sciencemag.org/content/350/6266/1312.full. Dedicated AIRR repositories that are techically integrated into the distributed system will be jointly referred to as the AIRR Data Commons.

**Recommendation 12: Maintain a central registry of AIRR Data Commons repositories.**
The registry may implement an interface that supports cross-repository queries
for a standard set of queries.


Specific Recommendations for Common Datatypes and Existing Repositories of Related Data Types
---------------------------------------------------------------------------------------------

**Recommendation 13: AIRR sequences for which epitopes are known should be
deposited in the Immune Epitope Database (IEDB)** - http://www.iedb.org/.
Links should be maintained to associated data and metadata in INSDC databases 
(Recommendation 5) and a compliant AIRR data repository (Recommendation 6).

**Recommendation 14: AIRR sequencing studies that fall within the scope of ImmPort should be registered there.**
Links should be maintained to associated data and metadata in INSDC databases 
(Recommendation 5) and a compliant AIRR data repository (Recommendation 6). 
Links within ImmPort should also be maintained to other data types generated within the same study.


Next Steps for AIRR CRWG, Other Working Groups, and the AIRR Community/Association
----------------------------------------------------------------------------------

**Next Step 1**: The AIRR CRWG should work collaboratively with the other
Working Groups to advance development of:

1. customized metadata for submission of AIRR sequencing data to INSDC databases,
2. standardized queries to be supported by the distributed repositories,
3. data elements with computable specifications,
4. a standardized data submission process and associated submission formats, and
3. more detailed specifications for recommended technologies for repository implementation.

**Next Step 2**: The AIRR Community will need to work with
repositories to establish an accreditation system for AIRR compliant repositories.
This should include an appropriate system for the citation/attribution of the
repository and/or the data.

**Next Step 3**: The AIRR Community will need to seek funding to
develop and maintain a central registry of AIRR Data Commons repositories.

**Next Step 4**: The AIRR Community will need to seek funding to
develop and maintain the AIRR Data Commons.

**Next Step 5**: The AIRR Community will need to work with funders
and journals to establish mechanisms for compliance with these recommendations.

**Next Step 6**: The AIRR Community should work to develop
consistent consent documents that are compliant with best practices for the
broad sharing of AIRR data.
