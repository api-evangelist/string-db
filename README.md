# STRING

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
