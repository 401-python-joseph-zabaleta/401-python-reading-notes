# Reading Notes 30  

## KEY NOTES

Hash maps do this to store vlaues:
- accept a key
- calculate the hash of the key
- use modulus to convert the has into an array index  
- store the key with the value by appending both to the end of a linked list  

Hash maps do this to read a value:  
- accept a key  
- calculate the has of the key  
- use modulus to convert the hash into an array index  
- use the array index to access the short LinkedList representing a bucket   
- search through the bucket looking for a node with a key/value pair that matches the key you were given.  

Internal methods of a hashtable  

- add()
    - Adds a new key/value pair to the table  
- find()
    - Finds a key/value pair  
- contains()
    - Boolean if a key/value pair exists  
- GetHash()
    - Takes a key as a string, conducts a hash, and returns the index value.


## Additional Resources  
* [Read: Intro to Hash Tables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)  
* [Watch: What is a Hash Table?](https://www.youtube.com/watch?v=MfhjkfocRR0)  
* [Read: Basics of Hash Tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)  
* [Skim: Hash Table Wiki](https://en.wikipedia.org/wiki/Hash_table)  
