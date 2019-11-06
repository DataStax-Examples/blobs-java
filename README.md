# Inserting and retrieving Blobs in Java
This demonstrates how to handle inserting and retrieving blob data type columns in Java

Contributors: [Olivier Michallat](https://github.com/olim7t) and [Tomasz Lelek](https://github.com/tomekl007) derived from [here](https://github.com/datastax/java-driver/blob/4.x/examples/src/main/java/com/datastax/oss/driver/examples/datatypes/Blobs.java)

## Objectives

* To demonstrate how to insert and retrieve blob data type columns from a Java application.
  
## Project Layout

* App.java - The main application file 

## How this Sample Works
By default, the Java driver maps this type to {@link java.nio.ByteBuffer}. The ByteBuffer API
 * is a bit tricky to use at times, so we will show common pitfalls as well. We strongly recommend
 * that you read the {@link java.nio.Buffer} and {@link ByteBuffer} API docs and become familiar
 * with the capacity, limit and position properties.  [This tutorial](http://tutorials.jenkov.com/java-nio/buffers.html) might also help
 
## Setup and Running

### Prerequisites

* Java 8
* An Apache Cassandra(R) cluster is running and accessible through the contacts points and data center identified in [application.conf](/src/main/resources/application.conf)

### Running

e.g.
To run this application use the following command:

`mvn exec:java -Dexec.mainClass="com.datastax.examples.App"`

This will produce the following output:

`
Writing retrieved buffer to /var/folders/v5/f93lqcsx2fj4__41f7l5w5j80000gn/T/blob6758286736353817789.png
`

