Elasticsearch-HBase-River / AsyncHBase 1.6 and Elasticsearch 1.4.2
==========================

An import river similar to the elasticsearch mysql river

If you're looking for an alternative sollution that uses the core hbase libraries and uses hbase replication for moving data, you can find one here:
https://github.com/posix4e/Elasticsearch-HBase-River

# Building

To build the plugin you need to have maven installed. With that in mind simply check out the project and run "mvn package" in the project directory. The plugin should then be available under target/release as a .zip file.

# Installation

Just copy the .zip file on the elasticsearch server should be using the plugin and run the "plugin" script coming with elasticsearch in the bin folder.

An Exmaple how one would call the plugin script:

	/my/elasticsearch/bin/plugin install river-hbase -url file:///path/to/plugin/river-hbase.zip

The plugin needs to be installed on all nodes of the ES cluster.

for more info on plugins check out http://www.elasticsearch.org/guide/reference/modules/plugins.html

# Usage

Check out the import.sh script, which is used to initialize the hbase river with all necessary config data.

More info on how to use rivers can be found here: http://www.elasticsearch.org/guide/reference/river/
