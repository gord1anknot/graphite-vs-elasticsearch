## Elasticsearch's Model Works If:

- You don't have a way of knowing about document syntax and semantics in advance
- You're comfortable with spending time figuring out how to query it later on
- Your primary interest during queries have to do with the contents of documents, as opposed to their relationships with each other
    - Aggregations API support new [in Kibana 4.0](https://github.com/elasticsearch/kibana/tree/4.0#kibana-400) makes that last point less of an issue
