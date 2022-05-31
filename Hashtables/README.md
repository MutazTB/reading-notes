# Hashtables

## What is a Hashtable?

1. Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

2. Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

3. Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

## Structure
**Hashing**
Basically, a hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.

**Creating a Hash**
A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a possible suggestion:

1. Add or multiply all the ASCII values together.
2. Multiply it by a prime number such as 599.
3. Use modulo to get the remainder of the result, when divided by the total size of the array.
4. Insert into the array at that index.

## Property & Description
1. Count
Gets the number of key-and-value pairs contained in the Hashtable.

2. IsFixedSize<br>
Gets a value indicating whether the Hashtable has a fixed size.
	
3. IsReadOnly<br>
Gets a value indicating whether the Hashtable is read-only.

4. Item<br>
Gets or sets the value associated with the specified key.

5. Keys<br>
Gets an ICollection containing the keys in the Hashtable.

6. Values<br>
Gets an ICollection containing the values in the Hashtable.

## Method & Description
1. public virtual void Add(object key, object value);<br>
Adds an element with the specified key and value into the Hashtable.
	
2. public virtual void Clear();<br>
Removes all elements from the Hashtable.

3. public virtual bool ContainsKey(object key);<br>
Determines whether the Hashtable contains a specific key.
	
4. public virtual bool ContainsValue(object value);<br>
Determines whether the Hashtable contains a specific value.

5. public virtual void Remove(object key);<br>
Removes the element with the specified key from the Hashtable.

