
## LinkedList
* LinkedList is a Doubly linked list and implements a Deque

## LinkedHashMap
for example for an LRUCache we can just use a LinkedHashMap 
* can be used to produce a copy of a map that has the same order as the original, regardless of the original map's implementation:
  ```java
  void foo(Map m) {
     Map copy = new LinkedHashMap(m);
  }
 ```
* removeEldestEntry(Map.Entry)} method may be overridden to impose a policy for removing stale mappings automatically when new mappings
  are added to the map.
 
* LinkedHashMap is not synchronized, If multiple threads access a linked hash map concurrently, and at least one of the threads modifies 
  the map structurally, it must be synchronized externally.  This can be accomplished by synchronizing on some object that encapsulates the map. 
  If no such object exists, the map should be "wrapped" using the Collections.synchronizedMap method.  This is best done at creation time, to 
  prevent accidental unsynchronized access to the map:
 ```java
  Map m = Collections.synchronizedMap(new LinkedHashMap(...));</pre> 
 ```

## HashMap


## TreeMap
- to use if you want to keep keys  in a sorted order, either in their natural order defined by Comparable interface or a custom order imposed by Comparator interface.

## TreeSet 


## String 

## Lessons 
- When a class is immutable we cache the hash code after the first time it is computed. and use the value 0 as an indicator that 
  the hash code has not yet been computed (example in String class and and netflix's servo MonitorConfig class).

## Hashing 
* If a class is immutable and the cost of computing the hash code is significant, you might consider caching the hash 
  code in the object rather than recalculating it each time it is requested. If you believe that most objects of this type 
  will be used as hash keys, then you should calculate the hash code when the instance is created. 

## Heap 

### Java's priority Queue 
- Priority queue is represented as a balanced binary heap: the two children of queue[n] are queue[2*n+1] and queue[2*(n+1)].

## Arrays


## Enums

### EnumSet 
- You don't need to use it explicitly - it's just an implementation detail. Basically, when an enum is small, EnumSet can use a very efficient 
  representation of the enum as a single int or long (I forget which) with one bit per member. When it has more elements than that representation 
  allows, JumboEnumSet is used instead.
  You don't need to worry about this - just use the members on EnumSet and you'll be fine. Just be aware that if your enums go over a certain size, 
  then enum sets become more expensive and less efficient. 

### EnumMap 

