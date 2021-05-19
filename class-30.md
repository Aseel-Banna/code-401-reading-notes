# Hash Tables

* Hash is the output of an operation of converting a string value to a value that can be used for different purposes and it will be saved into hashtable.

* Buckets is the contents of each index in hashtable.

* When two keys or more hashed to the same location in the hashtable a collisions will happen.

* A bucket or node has a key and value in the hashtable.
* The quick retrieving of values that are stored in hashtable is the main idea of using them, since the time complexity is O(1).
* Hash functions are used to convert large keys smaller ones.
* A hash function should be easy to compute, has a uniform distribution and avoid the collisions.

* The key of hash code is an integer (but not random) and the input determine the output of it. 
* Arrays are used to create hashtable.
* A perfect hash that is has no collisions.
* If a collision occurs, the hash map needs to be able to handle two keys resolving to the same index with overwriting on Add() method.
* Collisions can be solved if the initial state of the buckets change.
* Hash store values by accepting a key with calculating the value of it, then using modulus, the hash will be converted to an index of an array, finally, storing the key and value by adding them to the end of linked list.
* The relation between buckets size and the collisions is inverse.

* The Internal Methods: 
  * Add()
  * Find()
  * Contains()
  * GetHash()

