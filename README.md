# Confluent Proactive Support: Client

# Overview

This repository contains the client application for metrics collection of proactive support.


# Development

## Requirements

This project requires Kafka 0.9 built against Scala 2.10, which as of 02-Nov-2015 is not yet officially released.
You must therefore manually build Kafka and install it to your local Maven repository:

```shell
# Install Kafka trunk/master (w/ Scala 2.10) to local maven directory
$ git clone git@github.com:confluentinc/kafka.git && cd kafka
$ ./gradlew -PscalaVersion=2.10.5 clean install
```

Also, this project requires [support-metrics-common](https://github.com/confluentinc/support-metrics-common)
and [support-metrics-fullcollector](https://github.com/confluentinc/support-metrics-fullcollector), which
you may need to build and install locally prior to running the build for this project.


## Building

This project uses the standard maven lifecycles such as:

```shell
$ mvn compile
$ mvn test
$ mvn package # creates the jar file
```


# References

* [support-metrics-server](https://github.com/confluentinc/support-metrics-server)
  -- the corresponding server application for this client application
