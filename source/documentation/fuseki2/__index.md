---
title: Apache Jena Fuseki
slug: index
---

Apache Jena Fuseki is a SPARQL server.  It can run as a operating system
service, as a Java web application (WAR file), and as a standalone server.
It provides security (using [Apache Shiro](https://shiro.apache.org/)) and
has a user interface for server monitoring and administration.

It provides the SPARQL 1.1
[protocols for query and update](http://www.w3.org/TR/sparql11-protocol/)
as well as the
[SPARQL Graph Store protocol](http://www.w3.org/TR/sparql11-http-rdf-update/).

Fuseki is tightly integrated with [TDB](../tdb/index.html) to provide a robust,
transactional persistent storage layer, and incorporates
[Jena text query](../query/text-query.html).
It can be used to provide the protocol engine for other RDF query and
storage systems.

## Contents

- [Download](#download-fuseki)
- [Getting Started](#getting-started-with-fuseki)
- [Security](fuseki-security.html)
- [Running Fuseki](fuseki-run.html)
    - [As a standalone server with UI](fuseki-run.html#fuseki-standalone-server)
    - [As a service](fuseki-run.html#fuseki-service)
    - [As a web application](fuseki-run.html#fuseki-web-application)
    - [As an standalone SPARQL server](fuseki-main.html)
    - [As an embedded SPARQL server](fuseki-main.html)
- Architecture
    - [Server URI scheme : services and datasets](fuseki-data-services.html)
    - [Server Admin Protocol](fuseki-server-protocol.html)
- [Fuseki Configuration](fuseki-configuration.html)
- [Logging](fuseki-logging.html)
- [How to Contribute](#how-to-contribute)
- Client access
    - [Use from Java](../rdfconnection)
    - [SPARQL Over HTTP](soh.html) - scripts to help with data management.
- [Links to Standards](rdf-sparql-standards.html)

The Jena users mailing is the place to get help with Fuseki.

[Email support lists](/help_and_support/#email-support-lists)

## Download Fuseki

Releases of Apache Jena Fuseki can be downloaded from one of the mirror sites:

[Jena Downloads](/download)

and previous releases are available from [the archive](http://archive.apache.org/dist/jena/).
We strongly recommend that users use the latest official Apache releases of Jena Fuseki in
preference to any older versions.

**Fuseki download files**

Filename | Description
--------- | -----------
`fuseki-*VER*.distribution.zip` | Fuseki download, includes everything.
`fuseki-*VER*-server.jar`  | Fuseki server, as an executable jar.
`fuseki-*VER*-server.war`  | Fuseki server, as a web application archive (.war) file.

    <dependency>
       <groupId>org.apache.jena</groupId>
       <artifactId>jena-fuseki-war</artifactId>
       <type>war</type>
       <version>X.Y.Z</version>
    </dependency>

and for [Fuseki Main](fuseki-main):

    <dependency>
       <groupId>org.apache.jena</groupId>
       <artifactId>jena-fuseki-main</artifactId>
       <version>X.Y.Z</version>
    </dependency>

### Previous releases

While previous releases are available, we strongly recommend that wherever
possible users use the latest official Apache releases of Jena in
preference to using any older versions of Jena.

Previous Apache Jena releases can be found in the Apache archive area
at [http://archive.apache.org/dist/jena](http://archive.apache.org/dist/jena/)

### Development Builds

Regular development builds of all of Jena are available (these are not
formal releases) from the
[Apache snapshots maven repository](https://repository.apache.org/snapshots/org/apache/jena).
This includes packaged builds of Fuseki.

## Getting Started With Fuseki

The [quick start](fuseki-quick-start.html) section serves as a basic
guide to getting a Fuseki server running on your local machine.  

See [all the ways to run Fuseki](fuseki-run.html) for complete coverage of all the
deployment methods for Fuseki.

## How to Contribute

We welcome contributions towards making Jena a better platform for semantic
web and linked data applications.  We appreciate feature suggestions, bug
reports and patches for code or documentation.

See "[Getting Involved](/getting_involved/index.html)" for ways to
contribute to Jena and Fuseki, including patches and making github
pull-requests.

### Source code

The development codebase is available from git.

Development builds (not a formal release):
[SNAPSHOT](https://repository.apache.org/content/repositories/snapshots/org/apache/jena/jena-fuseki/)

Source code mirrored to github:
[https://github.com/apache/jena/tree/master/jena-fuseki2](https://github.com/apache/jena/tree/master/jena-fuseki2)

## Fuseki 1

Fuseki 1 is still available for legacy use. 
[Documentation for Fuseki1](/documentation/serving_data/).
