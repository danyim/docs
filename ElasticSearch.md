Elasticsearch Quirks
---
- **Pagination** - Use "from" and "size" in the request body to restrict what results are returned ([Source](http://www.elasticsearch.org/guide/en/elasticsearch/reference/current/search-request-from-size.html))

- **Rescoring** - Rescore the first *n* documents of the result based off of a given criteria. Expensive operation that performs post-analysis. ***Not entirely sure if this is compatible with aggregation*** ([Source](http://www.elasticsearch.org/guide/en/elasticsearch/reference/current/search-request-rescore.html))

- **Reindexing and index aliasing** - Process to add index aliases are simple, but we need to define a process (methods, endpoints, naming schemes) before implementing ([Source](http://www.elasticsearch.org/guide/en/elasticsearch/guide/current/_index_aliases_and_zero_downtime.html))


Research topics
--

- **Keyword highlighting** - Look into this and research how it will affect our implementation of ES in terms of performance/complexity

- **On-demand reindexing** - Nice StackOverflow thread [here](http://stackoverflow.com/questions/17007646/how-to-reindex-elasticsearch-quickly) about options left to the dev regarding reindexing



Issues
--
 - Terms aggregation pagination is NOT supported. [Per this forum article](http://elasticsearch-users.115913.n3.nabble.com/ES-aggregation-and-pagination-td4052774.html) and [this Elasticsearch Github issue #4915](https://github.com/elasticsearch/elasticsearch/issues/4915)