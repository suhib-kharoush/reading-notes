# Hashtables

### What is a Hashtable?
1. Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

2. Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

3. Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

### Why do we use them?
1. Hold unique values
2. Dictionary
3. Library

### What Are they?
- Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.


### Structure:

- Hashing:
- - Basically, a hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.

- Creating a Hash:
- - A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement.

### Collisions:
- A collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions. To put this into perspective, the worst possible hash is one that hashes every single key to the same exact index of an array. The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.

### Bucket Sizes:
- Hash Maps can have any number of buckets. If a hash map has only a few buckets it will be densely full and have many collisions. If a hash map has more buckets it will be more sparsely populated, there will be less collisions, but there may be a lot of extra empty space.

### Basics of Hash Tables:

- Hashing is a technique that is used to uniquely identify a specific object from a group of similar objects.

### Hash function:
- A hash function is any function that can be used to map a data set of an arbitrary size to a data set of a fixed size, which falls into the hash table. The values returned by a hash function are called hash values, hash codes, hash sums, or simply hashes.

- Hash table:
![](https://he-s3.s3.amazonaws.com/media/uploads/dda3e36.jpg)

- A hash table is a data structure that is used to store keys/value pairs. It uses a hash function to compute an index into an array in which an element will be inserted or searched. By using a good hash function, hashing can work well. Under reasonable assumptions, the average time required to search for an element in a hash table is O(1).

![](https://he-s3.s3.amazonaws.com/media/uploads/2cabd32.jpg)

### Quadratic Probing:
- Quadratic probing is similar to linear probing and the only difference is the interval between successive probes or entry slots. Here, when the slot at a hashed index for an entry record is already occupied, you must start traversing until you find an unoccupied slot. The interval between slots is computed by adding the successive value of an arbitrary polynomial in the original hashed index.