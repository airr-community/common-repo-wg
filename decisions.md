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

The /repertoire endpoint returns a list of “sample repertoire objects” with associated study metadata. A sample repertoire object is the description (the metadata) of the biological sample, including the processing that is applied to that sample, that is sequenced and annotated to acquire a set of rearrangements from the sample's immune repertoire.

```
/rearrangement
```

The /rearrangement endpoint returns a list of “rearrangement objects” with associated annotations. A rearrangement object is associated with a sample repertoire by the repertoire’s unique id. A rearrangement object contains the annotation information for each sequence read, including the V, D, and J gene assignments, the Junction (CDR3 and conserved Amino Acids), as well as other relevant annotation information. 

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

Conclusion: it’s challenging to enforce a globally unique ID, so CRWG API will require that INSDC accession numbers (e.g., Bioproject, Biosample, SRA) are provided so users can check for duplicates. If those accession numbers aren’t available for a specific study, the user will have to rely upon manually reviewing titles, publications, abstract, etc.

10. We will not require that repositories store the query and give it a unique identifier. However, we do see the desire for some repositories to support an asychronous query operation versus sychronous. We agreed that defining an asynchronous query mode would be useful but it places a larger burden (computational and infrastructure overhead) on the repository over a simple synchronous query mode. Therefore, we will not require repositories to support it. We will define the asynchronous query mode interface.
