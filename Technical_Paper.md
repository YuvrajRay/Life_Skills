# **Full-Text Search**

Full-text search is a technique that enables users to search for words or phrases within the content of documents or datasets, rather than just searching for exact matches in structured fields or specific columns.

Since changing Database mid project is complex and risky. It would be a better idea to experiment with different **search engine technologies** rather than migrating to a new Database. Following are some of the search engines that can be considered.


## Text Searchengines

### Elasticsearch

* Scalable distributed search engine
* Near real-time search
* Supports Multitenancy
* Automatic Rebalancing and Routing of shards

### Solr

* Real-time indexing capabilities
* Supports Faceted search
* Dynamic clustering
* Designed for scalability and fault tolerance

### Lucene

* Suitable for Full text search and indexing 
* Fuzzy search capable
* Recognised for implementation of Internet search
* Fully customizable - custom caching, segment merging


## Comparison

| Feature | Elasticsearch | Solr | Lucene |
| :---: | :---: | :---: | :---: |
| Ease of Use| Very easy- REST API, JSON, built-in features | Moderate- uses XML/HTTP, more manual setup | Hard - low-level Java library, no UI or API |
| Scalability | Built for distributed, cloud-native use | Scalable with SolrCloud and Zookeeper | Not inherently scalable |
| Text analyser| Rich built-in analyzer, easy to customize | Strong support, more-config heavy | Full control but require coding |
| Search accuracy & Relevancy| Smart defaults flexible turning | High-quality, customizable ranking | Most configurable but manual implementation |
| Real time search| Near real-time | Slightly slower for ingest-heavy setups | Require manual implementation |
| Horizontal scalability| Native support | Require SolrCloud & manual config | Not supportted |
| Best for | Modern apps, logging, analysis, real-time systems | Enterprise search legacy systems, e-commerce | Custom search engines inside Java apps |

  
## Sumarry

We don't need to use different Database, instead we can change to a different Search engines. For improved performance and scalability **Elasticsearch** is the best option.


## Reference
* **Sealticsearch-**  https://en.wikipedia.org/wiki/Elasticsearch
* **Solr-** https://en.wikipedia.org/wiki/Apache_Solr
* **Lucene-** https://en.wikipedia.org/wiki/Apache_Lucene

