Recommendations from the AIRR Community Common Repository Working Group
=======================================================================

Working Group membership can be found on the [Common Repository Working Group AIRR Communinty page](https://www.antibodysociety.org/the-airr-community/airr-working-groups/repository/).

**Revisions:**

* [v0.4.0](https://github.com/airr-community/common-repo-wg/blob/v0.4.0/recommendations.md) (Ratified at AIRR Community Meeting, December 2017)
* [v0.5.0](https://github.com/airr-community/common-repo-wg/blob/v0.5.0/recommendations.md) (revisions to use the phrase "AIRR Data Commons", August 2018)
* [v0.6.0](https://github.com/airr-community/common-repo-wg/blob/v0.6.0/recommendations.md) (Ratified at AIRR Community Meeting, May 2019)
* [v0.7.0](https://github.com/airr-community/common-repo-wg/blob/v0.7.0/recommendations.md) (Ratified at AIRR Community Meeting, December 2020)
* [v0.8.0](https://github.com/airr-community/common-repo-wg/blob/v0.8.0/recommendations.md) (Ratified at AIRR Community Meeting, May 2022)
* [v0.9.0](https://github.com/airr-community/common-repo-wg/blob/v0.9.0/recommendations.md) (Ratified at AIRR Community Meeting, June 2024)


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

The AIRR Community (AIRR-C) Common Repository Working Group (CRWG) developed a
set of recommendations that promote the deposit, sharing, and use of AIRR sequence
data. These recommendations were refined following community discussions at the
AIRR 2016 and 2017 Community Meetings and were approved through a vote by the
AIRR Community at the [AIRR Community Meeting in December 2017](https://www.antibodysociety.org/the-airr-community/meetings/communityIII/).
The current version here is being submitted for ratification at the
[June 2024 AIRR Meeting](https://www.antibodysociety.org/the-airr-community/meetings/airr-community-meeting-vii-learnings-and-perspectives/).

There are four sets of recommendations:

1. General principles for sharing of data related to AIRR sequencing studies (hereinafter AIRR 
   Data);
2. Outline of the characteristics of compliant repositories for data deposit,
   storage, and access;
3. Description of the AIRR Data Commons - a distributed model for compliant
   repositories for data linked by a central registry; and
4. Specific recommendations to existing repositories of related data types.

The concluding section addresses next steps for the AIRR CRWG and the AIRR
Community more broadly.


Section 1: Statement of Principles - AIRR Data Sharing
------------------------------------------------------

#### Recommendation 1.1: Facilitate deposit, access, and use of data
To enable and facilitate data deposit and broad access and use, data should be
made available under the least restrictive terms possible. The default data
sharing policy should be to deposit data in a publicly accessible repository
with no restrictions over deposit, access, storage, curation, and use.

#### Recommendation 1.2: No intellectual property restrictions
For data deposited in publicly accessible repositories, depositors of data and
repositories should have no right to interfere with access to and use of the
data by others, including through the assertion of any intellectual property
rights.

#### Recommendation 1.3: Legal exceptions
Exceptions to open data sharing ([Recommendation 1.1](#recommendation-11-facilitate-deposit-access-and-use-of-data))
should only be considered in circumstances that require compliance with local
legal norms (e.g., privacy/health information) or Institutional Review Boards
(e.g., respect for participant consent).

#### Recommendation 1.4: Exceptions for commercially valuable data
AIRR Data may be commercially valuable. In exceptional circumstances, where
there is an intent to commercialize AIRR sequence data and/or associated
materials, data generators may be prevented from publicly sharing those
sequences/materials of potential value. In these cases, data generators are
nevertheless encouraged to share the data using individually/institutionally
negotiated legal instruments.


Section 2: AIRR Data Repositories
----------------------

#### Recommendation 2.1: Establishment of dedicated AIRR data repositories
Dedicated repositories should be established for hosting processed
repertoire-sequencing (AIRR-seq) data and annotations to facilitate data queries and
cross-study meta-analyses. Annotated AIRR-seq data and relevant repertoire
metadata should be deposited in AIRR-compliant repositories following the MiAIRR
data standard. These repositories should link to the raw data deposited in INSDC
repositories (see Recommendation 2.2).

#### Recommendation 2.2: Long-term storage of data at INSDC
In addition, for long-term storage, data and metadata should also be deposited
in repositories of the [International Nucleotide Sequence Database Collaboration (INSDC)](http://insdc.org),
per the recommendations published by the AIRR Community Minimal Standards
Working Group [[DOI:10.1038/ni.3873]](https://doi.org/10.1038/ni.3873). The AIRR
Community Working Groups should work with INSDC and its individual repositories
to customize metadata capture for AIRR sequence data.

#### Recommendation 2.3: Compliance of AIRR data repositories
To be considered compliant, AIRR data repositories must implement and adhere to
policies and practices that comply with [Recommendations 1.1-1.4](#recommendation-11-facilitate-deposit-access-and-use-of-data).
In addition, repositories should require submitters, during the data submission
process, to attest that they have sought appropriate informed consent or other
authorization for sharing, where necessary. AIRR data repositories will not be
required to host data that have access restrictions, but they may choose to do
so on an individual basis.

#### Recommendation 2.4: Development of operational compliance criteria
The AIRR Community Working Groups should collaboratively develop operational
criteria for compliant repositories. At the operational level, a compliant
repository should use a standard, open source, data serialization framework for
ensuring interoperability, performance, maintainability, and evolution.
Operational Criteria should include implementation of:

1. A standardized set of queries that make AIRR-seq data findable and accessible
   (AIRR Data Commons API);
2. Standardized data elements with exact (computable) specifications that make
   AIRR-seq data interoperable and reusable (AIRR Data Representation);
3. A standardized data submission process (including standardized data
   and metadata formats) (MiAIRR);
4. A system for assigning unique identifiers that ensures coordination among
   repositories/registries, for example, the system used by the OBO Foundry to
   coordinate ontology term identifiers across orthogonal ontologies.

#### Recommendation 2.5: FAIR Digital Objects
A compliant repository should ensure that digital objects are Findable, Accessible,
Interoperable, and Reusable (FAIR) [[DOI:10.1038/sdata.2016.18]](https://doi.org/10.1038/sdata.2016.18),
adhere to the FAIR principles, and follow best practices in providing
[FAIR Digital Objects](https://zenodo.org/doi/10.5281/zenodo.7781925).

#### Recommendation 2.6: Compliance with applicable legal norms for data access
A compliant repository should adhere to applicable legal norms that govern data
access and use. Repositories that host data whose access and use are limited
by local regulations (e.g., privacy/health/genetic information) or institutional
review/research ethics boards (e.g., participant consent) should enable
controlled access and use of such data to the maximum extent permissible.
Repositories should enable the findability of such protected data via
non-protected associated metadata. Note that the securing of these data
should not impede access to all non-protected data and associated metadata.


Section 3: AIRR Data Commons - A System of Distributed Repositories Supported by a Centralized Registry
--------------------------------------------------------------------------------------------

#### Recommendation 3.1: AIRR Data Commons
The dedicated AIRR repositories [(Recommendation 2.1)](#recommendation-21-establishment-of-dedicated-airr-data-repositories)
should comprise a system of multiple, distributed repositories supported by a
centralized registry consistent with an intermediate distributed model as
described in [[DOI:10.1126/science.aaa7485]](https://doi.org/10.1126/science.aaa7485).
Dedicated AIRR repositories that are techically integrated into the distributed
system will be jointly referred to as the **AIRR Data Commons (ADC)**.

#### Recommendation 3.2: Maintain a central registry of AIRR Data Commons repositories
In order to enable the ability to find and access data in the ADC, the AIRR Community should strive to maintain a registriy
AIRR compliant repositories. This registry should provide a discovery mechanism for ADC repositories.


Section 4: Specific Recommendations for Common Data Types and Existing Repositories of Related Data Types
----------------------------------------------------------------------------------------------

#### Recommendation 4.1: AIRR data with known epitopes
AIRR sequences for which epitopes are known should be deposited in recognized international
resources for such data, such as the [Immune Epitope Database (IEDB)](https://www.iedb.org).
Links should be maintained to associated data and metadata in AIRR Data Commons repositories
[(Recommendation 2.1)](#recommendation-21-establishment-of-dedicated-airr-data-repositories)
as well as INSDC repositories [(Recommendation 2.2)](#recommendation-22-long-term-storage-of-data-at-insdc).

#### Recommendation 4.2: Other related data
AIRR sequencing studies that include data beyond the scope of the ADC should link to external repositories
as appropriate. Related data sets in repositories such as [Immune Epitope Database (IEDB)](https://www.iedb.org)
or other similar resources should be referenced
where possible. Links should be maintained to associated data and metadata
in AIRR Data Commons repositories [(Recommendation 2.1)](#recommendation-21-establishment-of-dedicated-airr-data-repositories)
as well as INSDC repositories [(Recommendation 2.2)](#recommendation-22-long-term-storage-of-data-at-insdc).


Next Steps for CRWG, Other Working Groups, and the AIRR Community
-----------------------------------------------------------------

**Next Step**: The AIRR Community will need to work with repositories to
establish an accreditation system for compliance with AIRR-C standards.

**Next Step**: The AIRR Community will work on establishing an appropriate
system for the citation/attribution of the repository and/or the data.

**Next Step**: The AIRR Community will need to seek funding to develop and
maintain a central registry of AIRR Data Commons repositories.

**Next Step**: The AIRR Community will need to seek funding to develop and
maintain the AIRR Data Commons.

**Next Step**: The AIRR Community will need to work with funders and publishers
to establish mechanisms for compliance with these recommendations.


**Next Step**: The AIRR CRWG will continue to work collaboratively with the other
Working Groups to maintain and extend:

1. The AIRR Data Standards including their computable specifications; and
2. A standardized data submission process and associated submission formats.
