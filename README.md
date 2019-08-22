### Cassandra应用

1：Cassandra config

spring.data.cassandra.cluster-name=Test Cluster
spring.data.cassandra.keyspace-name= user_space
spring.data.cassandra.contact-points=127.0.0.1
spring.data.cassandra.port=9042

2：run test

java -cp geomesa-tutorials-cassandra/geomesa-tutorials-cassandra-quickstart/target/geomesa-tutorials-cassandra-quickstart-2.4.0-SNAPSHOT.jar org.geomesa.example.cassandra.CassandraQuickStart --cassandra.contact.point 127.0.0.1:9042 --cassandra.keyspace geomesa --cassandra.catalog sample_table 

3：output        

bin/geomesa-cassandra export --output-format leaflet --contact-point 127.0.0.1:9042 --key-space geomesa --catalog sample_table

![NYC taxi tracks stored in GeoMesa](https://www.geomesa.org/img/taxi.gif)