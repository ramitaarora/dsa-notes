# Hash Maps

Hash Maps
- In order for a relationship to be a map, every key that is used can only be the key to a single value
- A given input, when fed into the map, gives the accurate output
- <i>Hashing function</i>: a function that turns data into a string in order to get the value per key
    - A hash function takes a string as input and returns an array index as output. In order for it to return an array index, our hash map implementation needs to know the size of our array.
    - In order for our hash map implementation to guarantee that it returns an index that fits into the underlying array, the hash function will first compute a value using some scoring metric: this is the hash value, hash code, or just the hash. 
    - Our hash map implementation then takes that hash value mod the size of the array. This guarantees that the value returned by the hash function can be used as an index into the array we’re using.
- Hash functions are also known as <i>compression functions</i>
    - All hash functions greatly reduce any possible inputs (any string you can imagine) into a much smaller range of potential outputs (an integer smaller than the size of our array)
- Write a hash function
    - needs to be simple by design
    - need to be able to take whatever types of data we want to use as a key (string, number)
