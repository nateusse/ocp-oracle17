# Chapter 9: Collections and generics


## Terminology
**Collection** : 
Group of objects contained in a single object.

**Java Collections Framework**: 
Set of classes in java.util for storing collections ![Java Collections Framework](
    /images/ch9/collection.png)


## Interfaces
- **List** : Ordered, yes duplicate entries. Access int index
- **Set**: No duplicates
- **Queue**: Specific order
    - **Deque** : Subinterface, acess both ends
- **Map**: Key/value, no duplicate keys. No  Collection (because map needs different methods) but yes part of the Java Framework.


### list

## Generics
### Diamond operator
- Specify type, short notation. 
- Right side statement ONLY, when type can be inferred, error:

`List<> list = new ArrayList<Integer>()`
- Not as type in variable declaration

`Class InvalidUse { void use(List<> data){} }`

## Collection methods
- **add()**: `public boolean add(E element)`
- **remove()**: Once instance by call. `public boolean remove(Object object)`
- **IsEmpty()**: `public booolean isEmpty()`
- **size()**: Amount of elements `public int size()`
- **clear()**:
Bye all elements.
 `public void clear()`
 - **contains**: Call equals() `public boolean contains(Object object)`
 - **removeIf()**: Remove all elements that match the condition as method reference or block of code
    - ` public boolean removeIf(Predicate <? super E> filter)`
    - Ej: `list.removeIf(s -> s.startWith("A"));`
    - Ej: `set.removeIf (String:: is Empty);`
- **for each**: