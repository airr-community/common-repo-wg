Meeting Minutes for the AIRR Common Repository Working Group
============================================================

This document contains notes and minutes from conference meetings of
the AIRR Common Repository Working Group. Also, the current decision
list for the design and implementation of the CR-API.

## Complete Decision List

1. RESTful API, JSON, using the OpenAPI specification. Initial implementation in Github

```
https://github.com/airr-community/airr-standards/blob/CRWG-API/specs/common_repository_api.yaml
```

2. Two primary endpoints (“gettable” objects with unique ids)

```
/repertoire
```

A “sample repertoire” with associated study metadata.

```
/rearrangement
```

A “rearrangement object” with associated annotations. A rearrangement object is associated with a sample repertoire by the repertoire’s unique id.

3. The GDC API looks to be a good specification to build upon

```
https://docs.gdc.cancer.gov/API/Users_Guide/Search_and_Retrieval/
```

* It has a well-defined and expressive query language

* Clients can limit/request what data fields to be returned (versus all data being returned)

* It has a “loose” data model, which just indicates which entities are “linked” through an endpoint and can thus be queried upon, without specifying how that link is implemented. For example, the “case” endpoint is linked to the “diagnosis” entity, so a query can be performed on diagnosis data by having “diagnosis.” as a prefix to the field name, such as “diagnosis.state”.

* It has a “facets” parameter which requests a limited form of aggregation capability, specifically for driving summary graphics (pie charts, bar plots, etc.) on a web interface.

* JSON and TSV formats for return data.

* It has a “_mapping” endpoint which is a discovery mechanism which provides metadata about the API itself. We probably need to expand upon it.

4. We will specify relationships between entities in the API data model, but each repository can have a different backend data model, which they will need to map to the API data model.

5. Data for return will be:

* Not-flatten, JSON response
* TSV response for /rearrangement, not-flatten, only get rearrangement data
* TSV response for /repertoire, one row for each repertoire id, flatten all study metadata

6. Key repeating elements to prioritize for computationally precise standardization
* Donor species (e.g., homo sapiens) (subject)
* Donor health status (e.g., diabetes) (subject, primary sample)
* Tissue type (e.g. PBMC) (primary sample)
* Cell subset (e.g. T-cell)
* Sequence type (e.g., TRB) (also from primer selection - experimental protocol)
* Gene usage (e.g., IGHV1-69)
* CDR3 sequence ( e.g., “CASSYIKLN”)
* Receptor specificity (e.g., HIV virus)

7. We will not define a Registry API. Instead, we will utilize the DataMed (BioCaddie) discovery index. However, CRWG will define a submission standard for DataMed so that AIRR repositories can be easily retrieved.

```
https://datamed.org/index.php
```

8. The same raw data may be processed through multiple analytical pipelines, (e.g., for comparative purposes) with results from all pipelines in the repository. How do we indicate this and coordinate what gets returned?

Conclusion: each repository will return only one as the default, but each repository will determine its own default. CRWG API will specify the fields that get returned to alert the user that there are alternatives.

9. Will we coordinate repertoire and rearrangement IDs across repositories? If yes, how?

Conclusion: it’s challenging to enforce a globally unique ID, so CRWG API will  require that INSDC accession numbers (e.g., Bioproject, Biosample, SRA) are provided so users can check for duplicates. If those accession numbers aren’t available for a specific study, the user will have to rely upon manually reviewing titles, publications, abstract, etc.


## Agenda for 2018.03.15



## Agenda for 2018.03.01



## Agenda for 2018.02.15



## Agenda for 2018.02.01


We condensed all of the discussions and comments from the brainstorming document.

### Current Status

1. RESTful API, JSON, using the OpenAPI specification. Initial implementation in Github

```
https://github.com/airr-community/airr-standards/blob/CRWG-API/specs/common_repository_api.yaml
```

2. Two primary endpoints (“gettable” objects with unique ids)

```
/repertoire
```

A “sample repertoire” with associated study metadata.

```
/rearrangement
```

A “rearrangement object” with associated annotations. A rearrangement object is associated with a sample repertoire by the repertoire’s unique id.

3. The GDC API looks to be a good specification to build upon

```
https://docs.gdc.cancer.gov/API/Users_Guide/Search_and_Retrieval/
```

* It has a well-defined and expressive query language

* Clients can limit/request what data fields to be returned (versus all data being returned)

* It has a “loose” data model, which just indicates which entities are “linked” through an endpoint and can thus be queried upon, without specifying how that link is implemented. For example, the “case” endpoint is linked to the “diagnosis” entity, so a query can be performed on diagnosis data by having “diagnosis.” as a prefix to the field name, such as “diagnosis.state”.

* It has a “facets” parameter which requests a limited form of aggregation capability, specifically for driving summary graphics (pie charts, bar plots, etc.) on a web interface.

* JSON and TSV formats for return data.

* It has a “_mapping” endpoint which is a discovery mechanism which provides metadata about the API itself. We probably need to expand upon it.

4. Key repeating elements to prioritize for computationally precise standardization

* Donor species (e.g., homo sapiens) (subject) ontology: NCBI taxonomy
* Donor health status (e.g., diabetes) (subject, primary sample) ontology: Disease Ontology, others?
* Tissue type (e.g. PBMC) (primary sample) ontology: Uberon, others?
* Cell subset (e.g. T-cell) ontology: Cell Ontology, others?
* Sequence type (e.g., TRB) (also from primer selection - experimental protocol) ontology: IMGT, OBI
* Gene usage (e.g., IGHV1-69) ontology: IMGT, Sequence Ontology
* CDR3 sequence ( e.g., “CASSYIKLN”) ontology: IMGT
* Receptor specificity (e.g., HIV virus) ontology: IEDB

### Open Questions

The API cannot be completely data model agnostic, but we don’t want to force a specific data model on the repository. The GDC API has a specification for how to do that. We still need to decide what “entities” we have, and which ones are “linked” through each endpoint?
We also want to allow repositories to provide their own specialized entities. The discovery mechanism should provide the ability for the client to learn about them. Do we need to place any requirements on this?

* Analysis output (clones, lineage trees)
* Raw data/sequences
* Computation/Analysis workflow

The same raw data may be processed through multiple analytical pipelines, (e.g., for comparative purposes) with results from all pipelines in the repository, do we need to do anything special to indicate this situation?

GDC allows for simple wildcard (*) but do we want the more expressive regular expressions for CDR3 searches? Should that capability be mandatory or optional? Regular expression capability on other fields, like free text fields, as mandatory/optional?

Registry implementation. Should each repository be a registry as well? Should we define a separate API for a registry?

### Action Items

1. Continue developing API specification.

2. Integrate CRWG recommendations, CRWG design documentation, and API documentation into the airr-standards documentation structure, and thus made available on https://docs.airr-community.org

3. Continue work on ontology specifications.
* Review existing work such as NIAID GSCID/BRC metadata.
* Review what IEDB is using.
* Based on review of the above, recommend ontologies for key elements listed above.
* How will these ontologies be integrated in an implementation (client interface, web service API)?

4. Who is going to implement the initial API spec and provide feedback to CRWG? How much of a “turnkey” system do/can we provide?
