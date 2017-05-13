## Reporter - Observer data stream Synchronization

While the Protofly provides transport interoperability without requiring the standardisation of messaging protocols, the Reporter -- Observer communication pattern enables semantic interoperability between Services without having to standardize Service APIs.
This pattern extends existing Observable communication patterns by using a P2P data stream synchronization solution for programmatic Objects, e.g. JSON Objects, hereafter simply called Data Objects.

To avoid concurrency inconsistencies between peers, only one peer is granted writing permissions to the Data Object -- the Reporter service.
All the other service instances have permissions only to read the Data Object -- the Observers.

As soon as the Reporter performs changes to Data Objects, they are immediately propagated to any authorized Observer by using the messaging framework.
In this way, the Data Object monitored by the Observer is always synchronized with the Data Object owned by the Reporter.

Full interoperability is achieved between two service instances by having to agree only on the usage of common formats for the Data Objects.

To be noted that, conceptually, more complex semantic interoperability and data synchronization technologies, such as Semantic Web and Operational Transformation, can be used.
