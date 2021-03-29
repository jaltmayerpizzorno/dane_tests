# dane_tests
YAML test suite for rfc7672 DANE TLS implementations I (Juan) wrote while working
for SparkPost.

The tests are written from the perspective of a component figuring out the list
of mailhosts to connect to, using a recursive resolver.  Each case starts with
either "nexthop" to indicate a domain subject to MX resolution, or "mailhost"
for a domain not subject to that (such as a configured mailhost).  Its output
is a list named "mailhosts", with various properties indicating whether
opportunistic DANE TLS applies to specific host, what the reference identifiers
and TLSA records should apply, etc.
