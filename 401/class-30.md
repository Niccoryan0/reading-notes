# 401-30 Readings

## Intro to Hash Tables
[Link](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)

- A *hash* is the result of some algorithm taking a string and converting it into a different value to be used for security or other purposes. For hashtables, the hash is used to determine the index of the array. A *bucket* is an index in the array, and can possibly hold multiple key/value pairs if collision occurs. *Collision* the result of mroe than one getting hashed to the same location.
- Hash tables can be used to hold unique values, or act as a dictionary or library.
- "The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a hash. A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value."
- Hash maps utilize array's read access and rather than adding elements from beggining to end like an array, a hash function is used to find the precise index location for an item based off it's key.
- Making a hash:
  - Add or multiply all the ASCII values together.
  - Multiply it by a prime number such as 599.
  - Use modulo to get the remainder of the result, when divided by the total size of the array.
  - Insert into the array at that index.
- The worst possible hash has all collisions, placing all items into the same bucket.
- When storing a value, hash maps:
  - Accept a key
  - Calculate the hash via this key
  - Use modulus to convert the hash into an array index
  - Store the with the value by appending both to the end of a linked list
- When reading a value:
  - Accept a key
  - Calculate the hash of the key
  - Use modulus to convert hash into array index
  - Use array index to acces the short LinkedList representing a bucket
  - Search the bucket for a node with a key/value pair matching the input key
Internal Methods
  - Add()
    - Send the key to the GetHash method.
    - Once you determine the index of where it should be placed, go to that index
    - Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
    - If something does exist, add the new key/value pair to the data structure within that bucket.
  - Find()
    - The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

  - Contains()
    - The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.

  - GetHash()
    - The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.

## Basics of Hash Table
[Link](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)

- Real world hashing examples:
  - In universities, each student is assigned a unique roll number that can be used to retrieve information about them.
  - In libraries, each book is assigned a unique number that can be used to determine information about the book, such as its exact position in the library or the users it has been issued to etc.
- Two steps to hashing implementation:
  - An element is converted into an integer by using a hash function. This element can be used as an index to store the original element, which falls into the hash table.
    - hash = hashfunc(key)
  - The element is stored in the hash table where it can be quickly retrieved using hashed key.
    - index = hash % array_size
- A good hash function is easy to compute, it must not become an algorithm itself, have uniform distribution to avoid clustering, and have as little collisions as possible.
- Seperate chaining is the use of linked lists in buckets to handle collisions.
- Applications
  - Associative arrays: Hash tables are commonly used to implement many types of in-memory tables. They are used to implement associative arrays (arrays whose indices are arbitrary strings or other complicated objects).
  - Database indexing: Hash tables may also be used as disk-based data structures and database indices (such as in dbm).
  - Caches: Hash tables can be used to implement caches i.e. auxiliary data tables that are used to speed up the access to data, which is primarily stored in slower media.
  - Object representation: Several dynamic languages, such as Perl, Python, JavaScript, and Ruby use hash tables to implement objects.
  - Hash Functions are used in various algorithms to make their computing faster

## What is a Hashtable? (Video)
[Link](https://www.youtube.com/watch?v=MfhjkfocRR0)

- Many ways to handle collisions, Linked Lists representing buckets seems common
- Paul is not good at coming up with names