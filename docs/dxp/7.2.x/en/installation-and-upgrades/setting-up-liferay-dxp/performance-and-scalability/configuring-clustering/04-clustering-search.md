# Clustering Search

Search should always run on a separate environment from your Liferay DXP server. DXP supports [Elasticsearch](https://help.liferay.com/hc/en-us/articles/360028711132-Installing-Elasticsearch), 

<!--Uncomment when Solr adapters is available. 
or 
Solr 
and either of those environments
-->

which can also be clustered.

For more information on how to cluster Elasticsearch, see [Elasticsearch's distributed cluster setup](https://www.elastic.co/guide/en/elasticsearch/guide/current/distributed-cluster.html).

Once DXP servers and Elasticsearch have both been properly configured as a cluster, change your DXP instance from *embedded* mode to *remote* mode. On the first connection, the two sets of clustered servers communicate with each other the list of all IP addresses; in case of a node going down, the proper failover protocols enable. Queries and indexes can continue to be sent for all nodes.

<!-- Uncomment when Solr adapter is available. 
For more information on how to cluster Solr, see 
[Apache Solr Cloud](https://cwiki.apache.org/confluence/display/solr/SolrCloud)
documentation. 

Once @product@ servers have been properly configured as a cluster, deploy the
Liferay Solr 5 Adapter on all nodes. (This app is available for download from
Liferay Marketplace
[here](https://web.liferay.com/marketplace/-/mp/application/78803899).) Create a
Solr Cloud (cluster) managed by _Apache Solr Zookeeper_. Connect the @product@
cluster to Zookeeper and finish the final configurations to connect the two
clusters.
-->