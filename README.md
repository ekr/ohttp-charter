# Oblivious HTTP Working Group (OHTTP) Charter

In a number of different settings, interactions between clients and servers
involve information that could be sensitive when associated with client
identity.

Client-server protocols like HTTP reveal aspects of client identity to servers
through these interactions, especially source addresses.  Even without client
identity, a server might be able to build a profile of client activity by
correlating requests from the same client over time.

In a setting where the information included in requests does not need
to be correlated, the Oblivious HTTP protocol allows a server to
accept requests via a proxy.  This design provides the property that
neither the proxy nor the server is alone able to (1) map a given
request's contents to a given client identity or (2) link specific
requests to the same client. However, if they collude they are able to
do so. The proxy ensures that the server cannot see source addressing
information for clients, which prevents servers linking requests to
the same client.  Encryption ensures that the proxy is unable to read
requests or responses.

The OHTTP working group will define the Oblivious HTTP protocol, a method of
encapsulating HTTP requests and responses that provides protected, low-latency
exchanges.  The working group will define any encryption scheme necessary and
supporting data formats for carrying encapsulated requests and responses, plus
any key configuration that might be needed to use the protocol.

The OHTTP working group will include an applicability statement that documents
the limitations of this design and any usage constraints that are necessary to
ensure that the protocol is secure.  The working group will consider the
operational impact as part of the protocol design and document operational
considerations.

The working group will prioritize work on the core protocol elements as
identified.  In addition, the working group may work on other use cases and
deployment models, including those that involve discovery of OHTTP proxies or
servers.

The OHTTP working group will work closely with other groups that develop the
tools that Oblivious HTTP depends on (HTTPbis for HTTP, CFRG for HPKE) or that
might use Oblivious HTTP (DPRIVE for DNS over HTTPS).

The working group will use draft-thomson-http-oblivious as input.
