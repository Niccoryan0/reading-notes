# 401-34 Readings

## Hash Tables/Sets/Maps
I decided to look more into Hash Tables for this assignment as they are definitely the data structure that I have the least familiarity/inherent understanding of. Starting with just the basics of what they are I stumbled upon the first link below in which the top answer to that very question gives a very well put analogy about what they are and why they are so efficient. The analogy, in short but you should read it in full it's very well written, uses a library, where there's thousands of books all over the place and if we're using something like a list and we need to find a specific book, every single book must be checked first if we know the title of the book we want. However, as the answer puts it "with a bit of forethought when you fill up the library and a lot of work when you fill up the library" we can organize the library, putting each book title into a computer algorithm that will spit back a specific shelf and spot number. So we place each book in it's spot as they're added and then when someone comes in and needs to find a book, we can simply feed the title back into the algorithm and it will tell us the exact shelf and spot number where we originally placed it, much faster. I thought this analogy really encapsulated the use case and power behind Hash Tables and really helped me to get a better fundamental grasp of what we are doing when we construct and add to them. 

- If you're like me you thought at some point "Why not just use Direct Address Tables? Or some other similar data structure." Direct Address Tables do allow for the same O(1) on operations as they can be access by key directly as well, however, the main problems are that the size of the array used for the table must not be too large, as we don't want a ton of null spaces taking up storage. So we should shrink the array, which exacerbates the 2nd problem of a DAT, no two elements can have the same key. This is where Hash Tables come in. Hashing reduces the index used, making the overall array contain far less null spaces, and creates "buckets" in the spaces to allow for collision, containing multiple values attached to one key.

- HashSet : Hash Table containing only unique keys

- HashMap : Not implemented directly in C# (Dictionary is closest built-in), in Java their methods are asynchronous while Hashtable has sync methods.

(1) [Stack Overflow analogy](https://stackoverflow.com/questions/730620/how-does-a-hash-table-work)

(2) [Useful other reference](https://towardsdatascience.com/hash-tables-explained-5dc457db50da)