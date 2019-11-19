# Querying Blobs in Java
Binary Large Objects ( [Blobs](https://docs.datastax.com/en/ddaccql/doc/cql/cql_using/refBlob.html) ) can be useful when the data doesn't fit into a standard [Cassandra data type](https://docs.datastax.com/en/ddaccql/doc/cql/cql_reference/refDataTypes.html). Some examples of common Blob usage are for images or large files, be careful of the size of your blobs though, it's best to break them up so that each blob cell is 1MB or less. 

Contributor(s): [Olivier Michallat](https://github.com/olim7t), [Tomasz Lelek](https://github.com/tomekl007) - derived from [here](https://github.com/datastax/java-driver/blob/4.x/examples/src/main/java/com/datastax/oss/driver/examples/datatypes/Blobs.java)

## Objectives

* Demonstrate how to write and read these blob data type columns in a Java application
  
## Project Layout

* [App.java](/src/main/java/com/datastax/examples/App.java) - The main application file 

## How this Sample Works
By default, the Java DataStax Driver maps blob types to [java.nio.ByteBuffer](https://docs.oracle.com/javase/8/docs/api/java/nio/ByteBuffer.html). The ByteBuffer API is a bit tricky to use at times, so we will show common pitfalls as well. We strongly recommend that you read the [java.nio.Buffer](https://docs.oracle.com/javase/8/docs/api/java/nio/Buffer.html) and [ByteBuffer](https://docs.oracle.com/javase/8/docs/api/java/nio/ByteBuffer.html) API docs and become familiar with the capacity, limit and position properties. This [tutorial](http://tutorials.jenkov.com/java-nio/buffers.html) is also useful.
 
## Setup and Running

### Prerequisites

* Java 8
* A Cassandra cluster is running and accessible through the contacts points and data center identified in [application.conf](/src/main/resources/application.conf)

### Running

To run this application use the following command:

`mvn exec:java -Dexec.mainClass="com.datastax.examples.App"`

This will produce the following output:

```
Writing retrieved buffer to /var/folders/v5/f93lqcsx2fj4__41f7l5w5j80000gn/T/blob6758286736353817789.png
```

