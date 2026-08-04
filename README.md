# STRING

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

STRING is a protein-protein interaction network database providing scored associations between proteins across 12,535 organisms and 59.3 million proteins, with over 20 billion interactions. The database integrates evidence from genomic context, co-expression, text mining, biochemical and genetic experiments, and curated databases.

## API

The STRING REST API provides programmatic access to:

- **Protein identifier mapping** — resolve gene names, UniProt IDs, and synonyms to STRING identifiers
- **Interaction networks** — retrieve interaction scores and network visualizations
- **Interaction partners** — find all known interaction partners for input proteins
- **Functional enrichment** — GO term, KEGG pathway, and other category enrichment analysis
- **Homology data** — Smith-Waterman similarity scores within and across species
- **Protein annotations** — functional annotations and gene set descriptions
- **PPI enrichment** — test whether a protein set is more connected than expected by chance
- **Values/Ranks enrichment** — GSEA-like ranked protein list analysis (async, API key required)

Base URL: `https://string-db.org`

API Documentation: https://string-db.org/help/api/

## Access and Licensing

All STRING data is freely available under [Creative Commons BY 4.0](https://creativecommons.org/licenses/by/4.0/). There is no cost for access, no registration required for standard endpoints, and commercial use is permitted with attribution.

For the Values/Ranks Enrichment endpoints, a free API key is required (obtained via `POST /api/json/get_api_key`).

## Usage Guidelines

- Wait 1 second between API calls to avoid server overload
- Do not run parallel scripts against the STRING API
- For large-scale data needs, use the [STRING Download page](https://string-db.org/cgi/download) instead of bulk API requests
- Use POST requests for queries with many protein identifiers

## Links

- Website: https://string-db.org
- API Docs: https://string-db.org/help/api/
- Downloads: https://string-db.org/cgi/download
- Licensing: https://string-db.org/cgi/access?footer_active_subpage=licensing
- Usage Guidelines: https://string-db.org/cgi/access?footer_active_subpage=usage
