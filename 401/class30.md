# Hashtables

![](https://res.cloudinary.com/practicaldev/image/fetch/s--c_3IL0PS--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://study.cs50.net/slideshows/1WyRdHGA7wYMYg078wXpv9qAjrELJBokRFRKGnVbnI7Q/img/0.png)

## What is a Hashtable?

Terminology:

Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a `hash`.

- Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

- Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

- Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

## Why do we use them?
- Hold unique values
- Dictionary
- Library

## What is Hashing
 A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity. This is ideal when quick lookups are required.

![](https://i0.wp.com/decbc.com/wp-content/uploads/2021/04/glossary-blockchain_Hashing_-_Functions.png?fit=2333%2C796&ssl=1)

## Collisions
A collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions.
Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a `LinkedList` in each one! 

