# HashCode and Equals

By default, all objects in Java inherit from the Object case the hashCode and equals methods which serve to identify if two variables refer to the same object.
The de facto behavior of the hashCode method returns the position in memory of an object, and the equals method compares the hashCode of the two objects evaluated, in this way, if the two variables refer to the same memory position, then it is said that they are the same, otherwise they are different.
In the case of Entities, the default implementation of these methods does not work correctly, because one Entity says that it is equal to another if two conditions are met:

- The two objects are of the same class.
- The value of your ID (@Id) are the same.

