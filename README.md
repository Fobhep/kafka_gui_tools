## General
This repo wants to provide a comparison of common Kafka Gui tools.
Currently, mainly non-enterprise tools are presented. Possibly this repository will be extended by such tools.
Feel free to create a PR for additions.
To show the functionality the docker-compose file in this repository starts a Kafka-Cluster consisting of:

| Component 	| docker-image 	|
|---	|---	|
| zookeeper 	| confluentinc/cp-zookeeper:7.0.1 	|
| broker 	| confluentinc/cp-server:7.0.1 	|
| schema-registry 	| confluentinc/cp-schema-registry:7.0.1 	|
| connect (with datagen connector plugin) 	| cnfldemos/cp-server-connect-datagen:0.5.0-6.2.0 	|

## Usage
Either run `docker-compose up -d` to start all of the tools,
or selectively start single ones:
`docker-compose up <service>`

The connector instance allows for the deployment of a datagen-connector.
Have a look here for the config https://github.com/confluentinc/kafka-connect-datagen.
The easiest possible deployment is done by using presets:
https://github.com/confluentinc/kafka-connect-datagen/tree/master/config


## Featured Tools
| Tool Name 	| Tool Docs/Page 	| localhost port 	| service 	|
|---	|---	|---	|---	|
| Kowl 	| https://github.com/redpanda-data/kowl 	| `localhost:8080` 	| `kowl` 	|
| AKHQ 	| https://akhq.io/ 	| `localhost:8090` 	| `akhq` 	|
| Kafdrop 	| https://github.com/obsidiandynamics/kafdrop 	| `localhost:9000` 	| `kafdrop` 	|
| Kafka-UI 	| https://github.com/provectus/kafka-ui 	| `localhost:9010` 	| `kafka-ui` 	|


## Credit
The compose file is inspired by the one featured here: https://github.com/redpanda-data/kowl/blob/master/docs/local/docker-compose.yaml
