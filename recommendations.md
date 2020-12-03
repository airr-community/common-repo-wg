Recommendations from the AIRR Common Repository Working Group
=============================================================

Working Group Members: Meredith Ashby, Felix Breden, Syed Ahmad Chan Bukhari,
Tania Bubela, Christian Busse, Scott Christley, Brian Corrie, David Klatzmann,
Uri Laserson, Bjoern Peters, Adrian Thorogood, Yariv Wine, Corey Watson

Working Group Co-Chairs: Lindsay Cowell, Brian Corrie

[v0.4.0](https://github.com/airr-community/common-repo-wg/blob/v0.4.0/recommendations.md) (Approved by AIRR Community, AIRR Community Meeting, December 2017)

[v0.5.0](https://github.com/airr-community/common-repo-wg/blob/v0.5.0/recommendations.md) (revisions to use the phrase "AIRR Data Commons", August 2018)

[v0.6.0](https://github.com/airr-community/common-repo-wg/blob/v0.6.0/recommendations.md) (Ratified at AIRR Community Meeting, May 2019)

[v0.7.0](https://github.com/airr-community/common-repo-wg/blob/v0.6.0/recommendations.md) (Ratified at AIRR Community Meeting, December 2020)


Background
----------

The use of high-throughput sequencing for profiling B-cell and T-cell receptors
has resulted in a rapid increase in data generation. It is timely, therefore,
for the Adaptive Immune Receptor Repertoire (AIRR) Community to establish a
clear set of community-accepted data and metadata standards; analytical tools;
and policies and practices for infrastructure to support data deposit,
curation, storage, and use. Such actions are in accordance with the policies
of international funding bodies and publishers, which promote data deposition
and sharing. At a minimum, data on which scientific publications are based should
be made available immediately on publication. Data deposit in publicly accessible
repositories ensures that published results can be validated. Such deposition
also facilitates reuse of data for the generation of new hypotheses and new
knowledge.

The AIRR Community Common Repository Working Group (CRWG) developed a set of
recommendations that promote the deposit, sharing, and use of AIRR sequence
data. These recommendations were refined following community discussions at the
AIRR 2016 and 2017 Community Meetings and were approved through a vote by the
AIRR Community at the [AIRR Community Meeting in December 2017](https://www.antibodysociety.org/the-airr-community/meetings/communityIII/).
The current version (v0.6.0) was modified in 2018 and 2019 and was ratified at
the AIRR Community Meeting in May 2019. Current edits will be submitted for
approval at the AIRR Community Meeting in December 2020.

There are four sets of recommendations:

1. General principles for sharing of AIRR sequence data [hereinafter data];
2. Outline of the characteristics of compliant repositories for data deposit,
   storage, and access;
3. Description of the AIRR Data Commons - a distributed model for compliant
   repositories for data linked by a central registry; and
4. Specific recommendations to existing repositories of related data types.

The concluding section addresses next steps for the AIRR CRWG and the AIRR
Community more broadly.


Statement of Principles -- AIRR Data Sharing
--------------------------------------------

**Recommendation 1: Facilitate deposit, access, and use of data.** To enable
and facilitate data deposit and broad access and use, data should be made
available under the least restrictive terms possible. The default data
sharing policy should be to deposit data in a publicly accessible repository
with no restrictions over deposit, access, storage, curation, and use.

**Recommendation 2: No intellectual property restrictions.** For data deposited
in publicly accessible repositories, depositors of data and repositories should
have no right to interfere with access to and use of the data by others,
including through the assertion of any intellectual property rights.

**Recommendation 3: Legal exceptions.** Exceptions to open data sharing
(Recommendation 1) should only be considered in circumstances that require
compliance with local laws (e.g., privacy/health information) and Institutional
Review Boards (e.g., respect for participant consent).

**Recommendation 4: Exceptions for commercially valuable data.** AIRR sequence
data may be commercially valuable. In exceptional circumstances, where there is
an intent to commercialize AIRR sequence data and/or associated materials, data
generators may be prevented from publicly sharing those sequences/materials of
potential value. In these cases, data generators are nevertheless encouraged to
share the data using individually/institutionally negotiated legal instruments.


Compliant AIRR Data Repositories
--------------------------------

**Recommendation 5: Long-term storage of data at INSDC.** For long-term storage,
data and metadata should be deposited in repositories of the [International
Nucleotide Sequence Database Collaboration (INSDC)](http://insdc.org), per the
recommendations published by the AIRR Community Minimal Standards Working Group
[[DOI:10.1038/ni.3873]](https://doi.org/10.1038/ni.3873). The AIRR Community
Working Groups should work with INSDC and its individual repositories to
customize metadata capture for AIRR sequence data.

**Recommendation 6: Establishment of dedicated AIRR data repositories**.
Dedicated repositories should be established for hosting processed
repertoire-sequencing data and annotations to facilitate data queries and
cross-study meta-analyses. These repositories should link to the raw data
deposited in INSDC repositories (see Recommendation 5).

**Recommendation 7: Compliance of AIRR data repositories**. To be considered
compliant, AIRR data repositories must implement and adhere to policies and
practices that comply with Recommendations 1-4.
In addition, repositories should require submitters, during the data submission
process, to attest that they have sought appropriate informed consent or other
authorization for sharing, where necessary. AIRR data repositories will not be
required to host data that have access restrictions, but they may choose to do
so on an individual basis.

**Recommendation 8: Development of operational compliance criteria.** The AIRR
Community Working Groups should collaboratively develop operational criteria for
compliant repositories. At the operational level, a compliant repository should
use a standard, open source, data serialization framework for ensuring
interoperability, performance, maintainability, and evolution. Operational
Criteria should include implementation of:

1. A standardized set of queries that make AIRR-seq data findable and accessible;
2. Standardized data elements with exact (computable) specifications that make
   AIRR-seq data interoperable and reusable;
3. A standardized data submission process (including standardized data and
   metadata formats);
4. A system for assigning unique identifiers that ensures coordination among
   repositories/registries, for example, the system used by the OBO Foundry to
   coordinate ontology term identifiers across orthogonal ontologies.

**Recommendation 9: FAIR Digital Objects.** A compliant repository should adhere
to Digital Object Compliance Principles, such as those under development as part
of the NIH Data Commons Initiative. The principles are designed to ensure that
digital objects are Findable, Accessible, Interoperable, and Reusable (FAIR)
[[DOI:10.1038/sdata.2016.18]](https://doi.org/10.1038/sdata.2016.18). Currently,
the most basic level of Digital Object Compliance expects digital objects to
exhibit:

1. Unique digital object identifiers;
2. A minimal set of searchable metadata;
3. Physical availability through a cloud-based Commons provider;
4. Clear access rules and controls; and
5. An entry (with metadata) in one or more indices.

**Recommendation 10: Compliance with local legal norms for data access**.
A compliant repository should adhere to local legal norms that govern data
access and use. Repositories that host data whose access and use are limited
by local regulations (e.g., privacy/health/genetic information) or
institutional review/research ethics boards (e.g., participant consent) should
enable controlled access and use of such data to the maximum extent permissible.
Repositories should enable the findability of such protected data via
non-protected associated metadata. Note that the securing of these data
should not impede access to all non-protected data and associated metadata.


AIRR Data Commons - A System of Distributed Repositories Supported by a Centralized Registry
--------------------------------------------------------------------------------------------

**Recommendation 11: The dedicated AIRR repositories (Recommendations 6) should
comprise a system of multiple, distributed repositories supported by a
centralized registry** consistent with an intermediate distributed model as
described in [[DOI:10.1126/science.aaa7485]](https://doi.org/10.1126/science.aaa7485).
Dedicated AIRR repositories that are techically integrated into the distributed
system will be jointly referred to as the AIRR Data Commons.

**Recommendation 12: Maintain a central registry of AIRR Data Commons repositories.**
The registry may implement an interface that supports cross-repository queries
for a standard set of queries.


Specific Recommendations for Common Data Types and Existing Repositories of Related Data Types
----------------------------------------------------------------------------------------------

**Recommendation 13: AIRR sequences for which epitopes are known should be
deposited in the [Immune Epitope Database (IEDB)](https://www.iedb.org)**.
Links should be maintained to associated data and metadata in INSDC repositories
(Recommendation 5) and an AIRR Data Commons compliant repository
(Recommendation 6).

**Recommendation 14: AIRR sequencing studies that fall within the scope of
ImmPort should be registered there.**
Links should be maintained to associated data and metadata in INSDC repositories
(Recommendation 5) and an AIRR Data Commons compliant repository
(Recommendation 6). Links within ImmPort should also be maintained to other
data types generated within the same study.


Next Steps for AIRR CRWG, Other Working Groups, and the AIRR Community
----------------------------------------------------------------------

**Next Step 1**: The AIRR CRWG should work collaboratively with the other
Working Groups to advance development of:

1. customized metadata for submission of AIRR sequencing data to INSDC
   repositories;
2. data elements with computable specifications;
3. a standardized data submission process and associated submission formats; and
4. more detailed specifications for recommended technologies for repository
   implementation.

**Next Step 2**: The AIRR Community will need to work with repositories to
establish an accreditation system for AIRR compliant repositories. This should
include an appropriate system for the citation/attribution of the repository
and/or the data.

**Next Step 3**: The AIRR Community will need to seek funding to develop and
maintain a central registry of AIRR Data Commons repositories.

**Next Step 4**: The AIRR Community will need to seek funding to develop and
maintain the AIRR Data Commons.

**Next Step 5**: The AIRR Community will need to work with funders and journals
to establish mechanisms for compliance with these recommendations.

**Next Step 6**: The AIRR Community should work to develop consistent consent
documents that are compliant with best practices for the broad sharing of AIRR
data.
