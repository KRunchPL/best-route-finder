# Library for finding best route in the routing table

Implementation of trie-tree best route finding algorithm in Rust with additional Python bindings.

## Rust library

The Rust library (found in `best-route-finder` folder) provides a simple class that represents a routing table by storing information in trie-tree structure (one bit at tree level).

Right now it is limited to following:

* it supports IPv4 only;
* a route consist of a network address, prefix length and next-hop interface;
* two routes with the same network address and prefix length are not permitted.

The class allows you to insert a new route to the tree by string and by integers and search for the next-hop interface for a given ip address (which can also be specified by string or integer).

## Python package

The Python package is just a simple wrapper for Rust library and provides the same functionality with the small addition of creating the tree based on a list of routing table entries.
