# UserAPI
Service contains user APIs

#Block diagram of project

![alt text](https://github.com/KhangarAnupama/UserAPI/blob/master/src/main/resources/BlockDiagram.png)

As shown in the diagram,

1. I have been divided the project into a microservices as follows.

A) Data Simulator
B) Data Producer 
C) Data consumer
D) User APIs

A) Data Simulator 
Git link : https://github.com/KhangarAnupama/DataSimulator

It produces geolocation data every two minutes and passed it to Data produces.

B) Data Producer 
Git link :https://github.com/KhangarAnupama/DataProducer

It accepts the data produced by the simulator and sends it to the Kafka pipeline.

C) Data Consumer
Git link : https://github.com/KhangarAnupama/DataConsumer

It consumes the data from the Kafka pipeline and saves it to the InfluDB .
It also saves the current data point in Redis cache.

D) User APIs.
Git link : https://github.com/KhangarAnupama/UserAPI

It performed the following operations.
- Register parent and kids and store data in postgres db
- Activate a device for kids
- Deactivate the device
- Send the current location of device
- Setup geofences
- Send notification if the breach happens.








