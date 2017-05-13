## Protocol on-the-fly

Protocol on-the-fly extends the usage of signalling on-the-fly concept to ensure messaging protocol interoperability between any distributed software Services.
Protocol on-the-fly leverages the code on-demand support by runtime engines (e.g. JavaScript) to dynamically select, load, and instantiate the most appropriate protocol stack at run-time.
This feature enables protocols to be selected at run-time and not at design time, which brings several benefits, namely: enables protocol interoperability among distributed Services, promotes loosely coupled Service architectures, makes platform updates much easier, and minimizes standardization efforts and optimizing resources spent.
These benefits stem from the fact that Protocol Gateways can be avoided in Services' middleware.
The implementation of the protocol stack (e.g. as a JavaScript file) which is dynamically loaded and instantiated at run-time is called a ProtoStub.
