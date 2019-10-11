# Overview

This is a repro environment for a github issue: https://github.com/jcustenborder/kafka-connect-transform-xml/issues/18

The environment is a copy of https://github.com/confluentinc/examples/tree/5.3.1-post/cp-all-in-one with the Kafka Connect container changed to one that has the kafka-connect-transform-xml plugin installed as shown in the [Dockerfile](connect/Dockerfile)

Steps to reproduce the issue:

* Run `docker-compose up -d --build`
* Wait some time for Kafka Connect to be up. Follow e.g. `docker logs xml-connect -f` to see when done starting
* Run `./post_connector.sh`

