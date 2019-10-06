#C++ Notes

[Geeksforgeeks](https://www.geeksforgeeks.org/c-classes-and-objects/)

## Class
User defined type that holds its own data member and member functions.

### Data members
Data variables and member functions are the functions used to manipulate these variable and together these data members and member functions defines the properties and behaviour of the objects in a Class.

## Object
Instance of a Class. When a class is defined, no memory is allocated, but when it is created, memory is allocated.

## Defining Class and Declaring Objects

```c++
class ClassName
{	Access specifier: 		// Can be private, public or protected.
	
	Data members; 			// Variables to be used.

	Member Functions() {} 	// Methods to access data members.

}; 							// Class name ends with a semicolon.
```

**Declaring Objects:** When a class is defined, only the specification for the object is defined; no memory or storage is allocated. To use the data and acess functions defined in the class, you need to create objects.

**Syntax**
```
ClassName ObjectName;
```

Data members and member functions of class can be accessed using the dot('.') operator with the object. For example if the name of the object is `obj` and you want to access the member function with the name `printName()` then you will have to write `obj.printName()`.

## Accessing Data Members

The public data members are also accessed in the same way given however the private data members are not allowed to be accessed directly by the object.

```c++
// C++ program to demonstrate
// accessing of data members

#include <bits/stdc++.h>
using namespace std;
class Geeks
{
    // Access specifier
    public:

    // Data Members.
    string geekname;

    // Member Functions()
    void printname()
    {
        cout << "Geekname is: " <<geekname;
    }
};

int main() {

    // Declare an object of class geeks
    Geeks obj1;

    // Accessing data member
    obj1.geekname = "Abhi";

    // Accessing member function
    obj1.printname();
    return 0;
}
```