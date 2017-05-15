## Message Nodes

Message Nodes are responsible for routing messages between Hyperty Runtimes on intra- and inter-domain level.
The main tasks of Messages Nodes are:

	* Assignment of unique addresses to entities (Hyperties and Data Objects),
	* Management of routing paths between entities,
	* Gateway to support Services in a Service Provider domain,
	* Enforcement of provider policies concerning the message routing.

Message Nodes can either be implemented from scratch, as a stand-alone solution, or they can make use of existing message routing systems and enrich them with support Services for the tasks listed above.

It is the ProtoStub that acts as the *glue* between the reTHINK runtime and the Message Node.
Therefore, each Message Node and its corresponding ProtoStub forms a unit that must be designed and implemented together.
All ProtoStubs must handle a common message format, but the transport protocol between the ProtoStub and the Message Node as well as internally in the Message Node are implementation specific.

Depending on the complexity and flexibility of the Message Node, different ProtoStub models are possible.
In one extreme, the ProtoStub might just be a pipe that transports messages completely un-touched. The other extreme is a ProtoStub that already analyses and translates reTHINK messages to another format suitable for the specific Message Node.

ReTHINK provides reference implementations of Message Nodes based on Vert.x, NodeJS, and Matrix.org.
