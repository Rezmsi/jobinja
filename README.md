# jobinja
The following tools have been used in this project
Docker for cluster management
Apache Kafka as a message broker
Apache Spark as processor
Kibana as a database visualization tool
Elasticsearch as a database
Python and Pi Spark for programming
All the tools of this program are executed by a Docker cluster

1. After running the Docker Compose file and uploading the Kafka image, just run the connector settings in the text file by your Linux engine to establish a connection between Kafka and Spark.
2. Then you can run the crawler, which comes in a separate file with the names raw data and crawl items
3. Run the raw_data file. This crawler is written by Python language and the Beautiful Soup library, which crawls every single item of the desired site and sends it to a Kafka topic (raw_datas) according to the settings that can be changed.
4. Run the crawl_items file, after that the items are read from the first topic and the favorite ones are extracted and sent to a new topic (jobs_info)
5. Now we have everything we needed and we just need to read them with Spark and put a time stamp on them and send them to the database.
6. By running Kibana, we can visually see the data sent to Elastic Search
