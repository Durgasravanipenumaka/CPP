## What is the difference between c and cpp ?
| **Feature**              | **C**                                                          | **C++**                                                                                         |
| ------------------------ | -------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| **Programming Paradigm** | Procedural (Structured) Programming Language                   | Object-Oriented Programming Language (OOP)                                                      |
| **Main Focus**           | Focuses on functions and procedures                            | Focuses on objects and classes                                                                  |
| **Approach**             | Follows **Top-down** approach (program divided into functions) | Follows **Bottom-up** approach (combine data and functions into objects)                        |
| **OOP Support**          | Does **not** support OOP concepts                              | Supports OOP — **classes, inheritance, polymorphism, abstraction, encapsulation**               |
| **Security**             | Less secure — no data hiding                                   | More secure — data can be hidden using **access specifiers** (`private`, `protected`, `public`) |
| **Function Overloading** | Not supported                                                  | Supported                                                                                       |
| **Encapsulation**        | Not supported                                                  | Supported                                                                                       |
| **Inheritance**          | Not supported                                                  | Supported                                                                                       |
| **Polymorphism**         | Not supported                                                  | Supported                                                                                       |
| **Namespace Feature**    | Not available                                                  | Available                                                                                       |
| **File Extension**       | `.c`                                                           | `.cpp`                                                                                          |


## Characteristics Of C++ :
- OOPs
- Not purely oops.
- General-purpose programming language.
- Complied Language.
- Faster than java and python.
- Middle level language.
- Protable/Machine independent but platform dependent.
- Powerful.
- Extensible - we can add user-defined functions.
- Dynamic allocation
- Case Sensitive
- pointers
- Strongly typed Programming language.

## Structure of c++ :
| **Concept**                  | **C (stdio.h)**                        | **C++ (iostream)**                              |
| ---------------------------- | -------------------------------------- | ----------------------------------------------- |
| **Input Function**           | `int scanf(const char *format, ...);`  | `cin >> variable;`                              |
| **Object Used for Input**    | —                                      | `cin` → predefined object of **istream** class  |
| **Operator Used for Input**  | —                                      | `>>` → **Extraction operator**                  |
| **Example 1**                | `scanf("%d", &x);`                     | `cin >> x;`                                     |
| **Example 2**                | `scanf("%d %s %f", &x, &s, &v);`       | `cin >> x >> s >> v;`                           |
| **Output Function**          | `int printf(const char *format, ...);` | `cout << variable;`                             |
| **Object Used for Output**   | —                                      | `cout` → predefined object of **ostream** class |
| **Operator Used for Output** | —                                      | `<<` → **Insertion operator**                   |
| **Example 1**                | `printf("Hello");`                     | `cout << "Hello";`                              |
| **Example 2**                | `printf("%d", x);`                     | `cout << x;`                                    |

## Datatypes :
- datatypes are two types :

  1.Primary datatype
  
  2.Secondary datatype
  
       - Derived datatype
       - User defined datatype

| **Primary Datatypes** | **Derived Datatypes** | **User-defined Datatypes** |
|------------------------|-----------------------|-----------------------------|
| char                  | Arrays                | Structures                  |
| int                   | Strings               | Unions                      |
| float                 | Pointers              | enums                       |
| double                |                       | typedef                     |
| wchar_t               |                       | Class                       |
| bool                  |                       |                             |
| string                |                       |                             |


- unicode table -> universal code table, which contains the symbols of all the languages which are world wisely certified.

#### wchart_t : 
- wide character is used to represent is used to represent symbols of unicode.
#### What is the size of wchar_t?
- 2 bytes on 16-bit complier.
- 4 bytes on 32-bit or 64-bit complier.
  
- ascii table is also part of unicode table.

#### bool :
- while(true)          // while(1)
- bool flag1=true
- bool p=false

#### string :
In C char str[20]="abcd";
- C style strings same as c in cpp.
- strings predefined function will work C style string.
- With Cstyle strings their may be wastage or storage of the memory.
- In c++ we have string datatype :
```c
string s1;
string s2="Viven";
```
- C string predefined function(like strcpy,strcat,strcmp etc) will not work here on c++ style strings
- s1=s2 -> copy
- s1==s2 -> comparison
- s1=s1+s2 -> concatination

## Operators :

| Operator Name | Symbol | Description |
|----------------|---------|-------------|
| Scope Resolution Operator | `::` | Resolves the scope of the variable |
| Line Feed Operator | `endl` | Supplies the new line |
| new | `new` | Dynamic memory allocation |
| delete | `delete` | Deallocation |
| typeid | `typeid` | Gives the datatype of the variable |

#### new : 
- Syntax : pointer = new datatype(value)
- ex :
```cpp
int *p = new int(123);
char *c = new char ch='D';
struct st *q;
q = new struct st;
```
- new syntax to create the array :
- pointer = new int[size];
```cpp
int *p = new int[5];
double *q = new int[5];
int **input(int **q,int r,int c){
      q = new int *[r];
      for(int i=0;i<r;i++){
          q[i]=new int[c];
          for(int j=0;j<c;j++){
              cout<<"Enter the elements :";
              cin>>q[i][j];
           }
       }
}
```
#### delete :
- syntax : delete pointer
```cpp
int main(){
        int *p;
        p=new int;
        cout<<"Enter the data:"<<endl;
        cin>>*p;
        cout<<*p<<endl;
        delete p;
}
```
- For dellaoction of memory :
```cpp
for(int i=0;i<r;i++){
      delete[] q[i];
}
```

## Reference variable :
- Reference variable is an alias name given to the existing variables or constants.
- Syntax : datatype &refname = existingname;
- Ex :
```cpp
int num=10;
int &ref = num;
cout<<ref; -> 120
cout<<&ref; ->Address
char ch = 'a';
char &c = ch;
```
#### Points to be noted about references :
- 1.References can be created only existing variables and constants,
- Ex :
```cpp
int n = 10;
int &r = n;    //correct

int &z;     //wrong

int a;
int &r=a;     //wrong

```
- 2.Reference must be intialized at the time of its declaration.
```cpp
int a;   
int &z;
&z=a;    //Invalid
```
- 3.Once a reference is tieup with a valid variable,it cannot be reffered to another variable.
- 4.We can create any no of references to a variable.
- we can create reference to pointer
- syntax : datatype *&ref = pointer;
- 6.we cannot create array of references.
- 7.syntax to create reference to constant
- const datatype &ref = constant;

## Difference between new and malloc :
| new | malloc |
|------|---------|
| `new` is an operator | `malloc` is a predefined function |
| **Syntax:** `new datatype;` | **Syntax:** `malloc(size_t);` |
| `new` returns a specific pointer type | `malloc` returns `void *` |
| `new` throws an exception on failure | `malloc` returns `NULL` on failure |
| `new` can allocate and initialize in a single line | `malloc` cannot allocate and initialize in a single line |
| Memory allocated with `new` cannot be resized with `realloc` | Memory allocated with `malloc` can be resized with `realloc` |
| `new` invokes a constructor | `malloc` does not invoke a constructor |
| `new` can be overloaded | `malloc` cannot be overloaded |
| `delete` invokes a destructor | `free` does not invoke a destructor |

## Functions :
- Function declaration
- Function call
- Function definition
### How do you pass value to a function ?
- In c we have 2 types :
- 1.call by value
- 2.call by reference
- In c++ we have 3 ways :
- call by value
- call by address(which is call by reference in c)
- call by reference (formal arguments reference to actual arguments )
#### call by address :
```c

```
#### call by reference :
- In call by reference ,formal arguments are references of the actual arguments, so formal arguments doesnot consume extra memory they refer to the actual arguments memoty blocks .so,whatever we modify on formal arguments they reflect on actual arguments.
- function call,function definition are same as call by value.
```cpp
#include<iostream>
using namespace std;
void inc(int &a){
        ++a;
}
int main(){
        int num=10;
        cout<<num<<endl;
        inc(num);
        cout<<num;
}
```
```cpp
#include<iostream>
using namespace std;
struct st{
        int roll;
        char name[20];
        float marks;
        char mobileno[20];
};
void input(struct st &v){
        cout<<"Enter the roll no :";
        cin>>v.roll;
        cout<<"Enter the name : ";
        cin>>v.name;
        cout<<"Enter the marks : ";
        cin>>v.marks;
        cout<<"Enter the mobileno : ";
        cin>>v.mobileno;
}
void print(struct st &v){
        cout<<v.roll<<endl;
        cout<<v.name<<endl;
        cout<<v.marks<<endl;
        cout<<v.mobileno<<endl;
}
int main(){
        struct st var;
        input(var);
        print(var);
}
```
## Return type as reference :
```cpp
#include<iostream>
using namespace std;
int & add(int a,int b){
        int c;
        c=a+b;
        return c;
}
int main(){
        int n1=10,n2=20,n3;
        n3=add(n1,n2);
        cout<<"Sum="<<n3<<endl;
}
```
- In above call by reference we returning the reference of local variable, so leads to segmentation fault.
- To make c alive we should declare c as static
### Corrected code :
```cpp
#include<iostream>
using namespace std;
int & add(int a,int b){
        static int c;
        c=a+b;
        return c;
}
int main(){
        int n1=10,n2=20,n3;
        n3=add(n1,n2);
        cout<<"Sum="<<n3<<endl;
}
```

- Default arguments to a function will avoid duplication of the codes when no of input arguments are different.
## where to supply the default values to the function ?
In function declaration.
## What should be default values ?
Any thing or any value based on our requirement.

ex:
```cpp
#include<iostream>
using namespace std;
int add(int,int,int =0,int =0,int =0);
int main(){
        cout<<add(10,20)<<endl;
        cout<<add(5,10,15)<<endl;
        cout<<add(10,20,30,40)<<endl;
}
int add(int a,int b,int c,int d,int e){
        return a+b+c+d+e;
}
```
- To make any argument as default argument ,we have to make sure arguments on the right side of it all should be default arguments.
```cpp
int add(int a,int b,int c){
       return a+b+c;
}
int add(int ,int,int=0);
int add(int ,int =0,int =0);
```

- In this example ,to make 'b' as a default argument 'c' must be default argument.
- simillarly ,to make 'a' as default argument 'b' and 'c' must be a default argument.
- Whybecause mapping of actual arguments to formal arguments are done from left to right.

## Function Overloading :
 Function overloading is a compile time polymorphism which is used to give same name to more than one function with different signatures.

## What is function signature ?
- function signature is formed by
    1.Function name
    2.Type of input arguments
    3.order of input arguments
    4.No of input arguments
- In function overloading to have different signature  either type of arguments,order of arguments or no of arguments should be different.
- Here we have same name but type of arguments are different :
```cpp
int add(int a,int b){
        return a+b;
}
double add(double a,double b){
        return a+b;
}
```
- Here we have different number of arguments are different :
```cpp
int add(int a,int b,int c){
        return a+b+c;
}
int add(int a,int b){
        return a+b;
}
```
- Here order of arguments are different :
```cpp
#include<iostream>
using namespace std;
int add(int a,float b){
        return a+b;
}
float add(float a,int b){
        return a+b;
}
```
- Here this example cannot be overloaded :
```cpp
int add(int a,float b){
        return a+b;
}
float add(int a,float b){
        return a+b;
}
```
- call by value and call by address can be overloaded.
- call by reference and call by address can be overloaded.
- call by reference and call by value cannot be overloaded.

## Storage classes :
- In C we have 4 types of storage classes.
- In C++ we have 5 storage classes.
    1.auto
    2.register
    3.static
    4.extern
    5.mutable -> applicable only to the data memmbers of a class.

## Structures :
### Difference Between C and C++ Structures : 

| **C Structures** | **C++ Structures** |
|------------------|--------------------|
| C structures are a collection of only data members. | C++ structures are a collection of data members and their related functions. |
| C structures do not support any access specifiers. | C++ structures support access specifiers. |

### What is the role of access specifiers ?
- Access specifiers decides who can access them.
- Types of access specifiers
- we have 3 types of access specifiers :
    1.public
    2.private
    3.protected
- private members are accessible only by the members of the structure or class.
- protected members are accessible only by the members and child of the class or structure.
- public members are accessible by members and non members.
- By default members of the structure are public in nature ,so we go with class datatype.
- In C++ encapsulation is implemented using structures and classes.

### What is encapsulation?
- Binding of data and its related functionalites into a single entity is called Encapsulation.

## Class :
- A class is a userdefined datatype , which is combination varaibles and functions.
- Variables inside the class are called as Datamembers
- Functions of a class are called member functions
- Both together are called as members of the class.

### What is a class ?
- A class is a blue of an object.
- A class is a logical representation of an object.

### What is an object ?
- An object is an instant of a class.
- An object is a physical entity of a class.
#### Class and Objects Example

| **Class**   | **Objects**                |
|--------------|-----------------------------|
| Fruit        | apple, banana, mango, grape |
| Vegetable    | onion, tomato, potato       |
| Flower       | rose, lily, jasmine         |

### Syntax to Create a Class in C++

```cpp
class ClassName
{
    access_specifier:
        // data members
        // member functions
};
```
### Example: Class in C++

```cpp
#include <iostream>
using namespace std;

class Bank
{
    int accno;
    char name[20];
    float bal;

public:
    void Deposit(float amt)
    {
        // code to deposit amount
        bal += amt;
    }

    void WithDrawal(float amt)
    {
        // code to withdraw amount
        if (bal >= amt)
            bal -= amt;
        else
            cout << "Insufficient Balance" << endl;
    }
};  // <-- Don't forget the semicolon here

int main()
{
    Bank b1; // object creation
    b1.Deposit(5000);
    b1.WithDrawal(2000);
    return 0;
}
```
### Syntax to Create an Object in C++

```cpp
ClassName objectName;
```
- Ex : Bank myAcc;
- The size of an object is equal to the sum of the sizes of all its data members, except when there is padding or alignment added by the compiler for memory efficiency.


- Data Members and members functions inside the member functions belongs to current calling object.
### What is calling object?
- An object which is invoking the member function is called calling object.
```cpp
int main()
{
    Bank myacc;             // (A) myacc is a stack object (automatic storage)
    Bank *ptr;              // pointer variable (uninitialized)
    ptr = &myacc;           // ptr now points to the stack object myacc
    ptr->CreateAcc();       // calling CreateAcc() on the object pointed by ptr (myacc)
    ptr->Menu();            // same as myacc.Menu()

    Bank *q;
    q = new Bank;           // (B) allocate a Bank object on the heap; constructor is called
    q->CreateAcc();         // calling on heap object
    q->Menu();
    delete q;               // destructor called; memory freed

    Bank *r;
    r = (Bank *)malloc(sizeof(Bank)); // (C) allocate raw memory, NO constructor called
    r->CreateAcc();          // **Undefined/unsafe** if CreateAcc expects object properly constructed
    r->Menu();
    free(r);                 // frees memory, but destructor NOT called
}
```

### Array of Objects in C++

An **array of objects** is a collection of objects of the same class, stored in contiguous memory locations.

#### Syntax:
```cpp
ClassName arrayName[size];
```
- Ex : student DB[5];
- DB[0] is an object
- DB[1] is an object
- DB[2] is an object
- DB[3] is an object
- DB[4] is an object

### Syntax to Define Member Function Outside the Class

```cpp
return_type ClassName :: functionName(parameter_list)
{
    // function body
}
```
## Constructors in C++ :

A **constructor** is a special member function used to **initialize an object at the time it is created**.

### Points to note
- The **constructor name is the same as the class name**.
- A constructor **must not** have a return type (not even `void`).
- Constructors are usually declared as `public` so objects can be created from outside the class.
- If you do not provide any constructor, the **compiler supplies a default constructor** (called the *implicit default constructor*).

---

## Types of constructors
1. **Default constructor**  
2. **Parameterized constructor**  
3. **Copy constructor**

---

## 1. Default constructor
- A constructor without parameters is called a **default constructor**.
- Note : An unitialized object always invokes or demands default constructor.
- When none of the constructors are supplied by the programmer complier will supply a default constructor for namesake.
- Invoked when you create an object with no arguments:  
```cpp
  Complex e1;     // default constructor called
  Rectangle r1;   // default constructor called
```

## 2.Parameterized constructor 
- A constructor that takes arguments is a parameterized constructor.
- Ex : complex e1(10,30);

## 3. Copy Constructor :
- A constructor whose input arguments or formal arguments is a reference to same class object is calles copy constructor.
- Copy constructors are invoked when we assign an exixting object to a newly created object at the time of itys declarations.
- Ex : complex e1
       complex e2=e1; // e2.complex(e1);
## Complete combined example (Default, Parameterized, Copy) :
```cpp
#include <iostream>
using namespace std;

class Student {
    int roll;
    int marks;

public:
    // Default constructor
    Student() {
        roll = 0;
        marks = 0;
        cout << "Default constructor called\n";
    }

    // Parameterized constructor
    Student(int r, int m) {
        roll = r;
        marks = m;
        cout << "Parameterized constructor called\n";
    }

    // Copy constructor
    Student(const Student &s) {
        roll = s.roll;
        marks = s.marks;
        cout << "Copy constructor called\n";
    }

    void show() {
        cout << "Roll: " << roll << ", Marks: " << marks << endl;
    }
};

int main() {
    Student s1;            // default constructor
    Student s2(10, 95);    // parameterized constructor
    Student s3 = s2;       // copy constructor

    cout << "\nStudent details:\n";
    s1.show();
    s2.show();
    s3.show();
}
```

## Copy :
C++ needs to copy data members of obj1 into obj2.
This happens using a copy constructor by default.
```cpp
ClassA obj1;
ClassA obj2 = obj1;  // Copy operation
```
- How does the copying behave with pointers or dynamically allocated memory?

1.Shallow copy

2.Deep copy

### Shallow copy :
Copy the address of dynamically allocated memory — NOT the actual data.
So two objects share the same memory location.
```cpp
#include <iostream>
using namespace std;

class Demo {
public:
    int *ptr;

    Demo(int x) {
        ptr = new int(x); // dynamic memory
    }
};

int main() {
    Demo obj1(10);
    Demo obj2 = obj1; // shallow copy

    cout << *obj1.ptr << endl; // 10
    cout << *obj2.ptr << endl; // 10

    *obj2.ptr = 20; // modify

    cout << *obj1.ptr << endl; // 20 !!
    cout << *obj2.ptr << endl; // 20
}
```
In shallow copy they copy member to member or field to field instead of copying the data pointed by members or field.
In shallow copy both destination and source objects refer to same dynamically allocated block, so if one object is modifing it reflects on another object.

- Disadvantages :
Since both objects share the same pointer: Changing one affects the other.
Also, when objects destruct: It will try to delete the same memory twice → crash (double free).

### Deep copy :
Deep copy means:
Allocate new memory and copy the content, not the address.
Each object gets its own copy of the data.

```cpp
#include <iostream>
using namespace std;

class Demo {
public:
    int *ptr;

    Demo(int x) {
        ptr = new int(x);
    }

    // Deep Copy Constructor
    Demo(const Demo &obj) {
        ptr = new int(*obj.ptr); // allocate new memory & copy value
    }
};

int main() {
    Demo obj1(10);
    Demo obj2 = obj1; // deep copy

    *obj2.ptr = 20;

    cout << *obj1.ptr << endl; // 10
    cout << *obj2.ptr << endl; // 20
}
```
- In Deep copy we copy the data pointed by members instead of addresses so that every object will have its individual copy

- Shallow copy is fine if you do not use dynamic memory (pointers).
- Deep copy is required when:
    You use new
    You have dynamically allocated arrays
    You store resources

## Destructor :
Destructor is automatically invoked to destroy the resources allocated by an object.
Destructor is invoked when n objects is about to destroy.
Destructor name is same as class prefix with tilt opeartor.
Ex : if class name is complex :
~complex(){
}

## Friend function :
Friend function is a nonmember of the class,but got the permissions to access private and protected members of the class like members of the class.

we have 3 types
  - 1.normal functions as a friend
  - 2.member function as a friend
  - 3.Entire class as a friend of another

- How to make functions as a friend to class?
Declare function declarations with friend keyword inside the class.

The friend keyword is written inside class, but the function definition is written outside.

- 1.Normal (global) function as a Friend :
A simple standalone function becomes friend.
```cpp
#include <iostream>
using namespace std;

class A {
private:
    int x;
public:
    A() { x = 10; }

    friend void display(A obj); // friend declaration
};

void display(A obj) {
    cout << "Value of x = " << obj.x; // private access allowed
}

int main() {
    A obj;
    display(obj);
}
```
display() can access x even though it's private.

- 2.Member function of one class as a Friend of another class :
Suppose Class B has a function show(), and Class A wants to allow it access.
```cpp
class A {
private:
    int x;
public:
    A() { x = 50; }

    friend void B::show(A obj);  // member of B is a friend
};

class B {
public:
    void show(A obj) {
        cout << obj.x;
    }
};
```
Only show() can access private members of A
Other functions of B cannot access A’s private data.

- 3.Friend Class :
We can make entire class B the friend of A.
```cpp
class A {
private:
    int x;
public:
    A() { x = 100; }

    friend class B;   // whole class B becomes friend
};

class B {
public:
    void display(A obj) {
        cout << obj.x; // private access allowed
    }

    void print(A obj) {
        cout << obj.x * 2; // also allowed
    }
};
```
Now all member functions of B can access A’s private data.

| Type                   | Access Scope                |
| ---------------------- | --------------------------- |
| Normal friend function | Only that one function      |
| Member function friend | Only that member function   |
| Friend class           | ALL functions of that class |


## Operator Overloading  :
Operator Overloading is a feature in C++ that allows you to redefine the behavior of an operator (like +, -, ==, etc.) when it is used with user-defined data types (classes/objects).

Operator overloading is used to enhance or improvise the functionality of the existing operators , so that they can be applied on user defined datatypes without changing their functionality, priority and associativity of operators.

It is a type of polymorphism in which an operator is overloaded to give user defined meaning to it. Overloaded operator is used to perform operation on user-defined data type. For example '+' operator can be overloaded to perform addition on various data types, like for Integer, String(concatenation) etc. 

- Syntax :
```c
return_type operator<symbol>(argument_list)
{
    // your definition
}
```
- Operators That Cannot Be Overloaded

  ❌ You cannot overload:

      :: (scope resolution)

      . (member access)

      .* (pointer-to-member)

      sizeof

      typeid

      ?: (ternary operator)

- Example :
```c
#include<iostream>
using namespace std;

class Complex {
    int real, imag;
public:
    Complex(int r=0, int i=0) {
        real = r;
        imag = i;
    }

    // Overload + operator
    Complex operator+(Complex obj) { // c1.operator+c2 ->it internally calls like this
        Complex temp;
        temp.real = real + obj.real;
        temp.imag = imag + obj.imag;
        return temp;
    }

    void display() {
        cout << real << " + " << imag << "i" << endl;
    }
};

int main() {
    Complex c1(2, 3), c2(4, 5);
    Complex c3 = c1 + c2;  // Calls operator+()
    c3.display();
    return 0;
}
```
- Operator Overloading can be done in two ways :
  1.using memeber function
  2.using friend function

Operator overloading function can be a member function if the Left operand is an Object of that class, but if the Left operand is different, then Operator overloading function must be a friend function.

- member function operator overloading

For opeartor overloading atleast one operand should be an object.

To overload opearators using member functions left operand should always be the same class object, because compiler always makes the left operand as calling object.

While opeartor is overloaded its the responsibility of the developer to makesure that functionality,priority and associavity is not changed.

Compiler suplies a hidden pointer called "this" in every member function of a class except in static member function,

"this" pointer holds the address of the calling object.

```c
#include<iostream>
using namespace std;
class complex{
        int real;
        int img;
        public:
                void input(){
                        cin>>real;//cin>>this->real
                        cin>>img;//cin>>this->img
                        cout<<"Complex number : " << real << "+" << img << "j" << endl;
                }
};
int main(){
        complex e1;
        e1.input();
}
```

"this" pointer is used to access the address or calling object itself.

Assignment opeartor overloaded function is supplied by the compiler, programmer does not supply.

When you create a class in C++, you do NOT need to write your own assignment operator (=) because the compiler automatically creates one for you.
```c
complex operator=(const complex &obj);
```
The compiler still provides a default assignment operator for your class.

Because in almost every program, you want to copy objects like:
```c
Complex c1, c2;
c1 = c2;   // assignment
```
If the data members of the class are dynamically allocated then its the responsibility of the programmer to supply the assignment operator overloaded function with deep copy.

operators that cannot be overloaded by only friend functions
 1.=
 2.[]
 3.()
 4.->


## Static Data Members :
- A static member is shared by all objects of the class.
- All static data is initialized to zero when the first object is created, if no other initialization is present.
- We can't put it in the class definition but it can be initialized outside the class using the scope resolution operator :: to identify which class it belongs to.
- When we declare a member of a class as static it means no matter how many objects of the class are created, there is only one copy of the static member.

```cpp
#include<iostream>
using namespace std;

class Demo{
        private :
                int n;
                static int s;
        public :
                void zero(){
                        n=0;
                }
                void inc(){
                        n++;
                        s++;
                        cout<<"Value of static variable is :"<<s<<endl;
                        cout<<"Value of non-static variable is :"<<n<<endl;
                }
};
int Demo::s=0;
int main(){
        Demo obj1,obj2;
        obj1.zero();
        obj1.inc();
        obj2.zero();
        obj2.inc();
}
```


## Static Member Function :
- By declaring a member functions as static, you make it independent of any particular object of the class. A static member function can be called even if no object of the class exist and the static function are accessed using only the class name and the scope resolution operator(::).
- A static member functions can only access the static member of that class.
- Static member functions have a class scope and they do not have access to this pointer of the class.
- You could use a static member function to determine whether some objects of the class have been created or not.

```cpp
#include<iostream>
using namespace std;

class Demo {
        private :
                static int s;
        public :
                static void inc(){
                        s++;
                        cout<<"S value : "<<s<<endl;
                }
};

int Demo::s=100;
int main(){
        Demo::inc();
        Demo::inc();
}
```


## Constant members of a class :
### Constant data members :
- Constant data member is a variable inside a class that cannot be changed after initialization.
- It must be initialized when the object is created.
- value remains constant for that objet's lifetime.
- constant data members should be initialized through constructor with a special syntax, once initialized they cannot be changeable.

### syntax :
```cpp
class Demo {
    const int x;   // constant data member
public:
    Demo(int a) : x(a) {}   // initialize using constructor
};
```
### code :
```cpp
#include<iostream>
using namespace std;

class Demo{
        const int x;
        public :
              Demo(int a) : x(a) {}
              void show(){
                      cout<<"x = "<<x<<endl;
              }
};

int main(){
        Demo d1(10);
        Demo d2(20);

        d1.show();
        d2.show();
}
```

 ## Constant member function :
 - A Constant member function is a function that cannot modify any data member of the class.
 - Guarantees read-only access to object data.
 - Declared using const keyword after function definition.

## syntax :
```cpp
class Demo {
public:
    void display() const;  // constant function
};
```

### code:
```cpp
#include<iostream>
using namespace std;

class Demo {
        int a;
        public :
            Demo(int x) : a(x) {}

            void show() const{
                   // a=100;   error
                    cout<<"a = "<<a<<endl;
            }
};
int main(){
        Demo d1(10);
        Demo d2(30);

        d1.show();
        d2.show();
}
```

members functions of a class are of two types
1.Mutator member functions
2.Accessor member functions

mutators member functions can access as well as modify the data members of a class.

By default member function are mutators in nature.

Accessor member functions can only access the data members , they cannot modify them

Accessor member functions also known as constant member functions or read only member functions

Values of the data members of the constant object cannot be changable.

Constant objects can only invoke constant member functions.

Mutable storage class is applicable only to the data member of the class.Mutable means can be changable.

If a data member declared as mutable , its value can be changable inside the constant member function and as well as for constantobjects.


## Inheritance :
Inheritance allows one class to reuse attributes and methods from another class. It helps you write cleaner, more efficient code by avoiding duplication.

we group the "inheritance concept" into two categories :

- derived class(child) - the class that inherits from another class
- base class(parent) - the class being inherited from

To inherit from a class, use the : symbol.

```cpp
#include<iostream>
using namespace std;

class vehicle{
        protected :
                string name = "car";
                string company = "ford";
        public :
              void display(){
                      cout<<"tu tu tu"<<endl;
              }
};

class car: public vehicle {
        public:
                string model = "Mustang";

                void showdetails(){
                        cout<<name<<" "<<company<<" "<<model<<endl;
                }
};

int main(){
        car obj;
        obj.display();
        obj.showdetails();
}
```

## multilevel inheritance :
A class can also be derived from one class, which is already derived from another class.

In the following example, Mygrandchild is derived from class Mychild (which is derived from Myclass)

```cpp
#include <iostream>
using namespace std;

// Parent class
class MyClass {
  public: 
    void myFunction() {
      cout << "Some content in parent class." ;
    }
};

// Child class
class MyChild: public MyClass {
};

// Grandchild class 
class MyGrandChild: public MyChild {
};

int main() {
  MyGrandChild myObj;
  myObj.myFunction();
  return 0;
}
```

## Multiple Inheritance :
A class can also be derived from more than one base class,using a comma-seperated list.

```cpp
// Base class
class MyClass {
  public:
    void myFunction() {
      cout << "Some content in parent class." ;
    }
};

// Another base class
class MyOtherClass {
  public:
    void myOtherFunction() {
      cout << "Some content in another class." ;
    }
};

// Derived class
class MyChildClass: public MyClass, public MyOtherClass {
};

int main() {
  MyChildClass myObj;
  myObj.myFunction();
  myObj.myOtherFunction();
  return 0;
}
```

## Polymorphism :
Polymorphism means having multiple forms of one thing. In inheritance, polymorphism is done, by function overriding, when both parent and child class have member function with same name , declaration but different definition.

## Function Overriding :
Function overriding is the mechanism using which a function defined in the base class is once again defined in the derived class. In this case, we say the function is overridden in the derived class.

### Requirements for Overriding a Function
- Inheritance should be there. Function overriding cannot be done within a class. For this we require a derived class and a base class.
- Function that is redefined must have exactly the same declaration in
both base and derived class, that means same name, same return
type and same type of input arguments .

## Compile time polymorphism :
If function symbols are resolved at compile time, it is called compile time polymorphism.

Compile time polymorphism is also called as early binding or static binding or compile time binding.

Ex : - function overloading
     - operator overloading

```cpp
#include <iostream>
using namespace std;

void add(int a, int b) {
    cout << a + b;
}

void add(double a, double b) {
    cout << a + b;
}

int main() {
    add(5, 3);        // calls int version
    add(2.5, 3.7);    // calls double version
}
```

## Run time polymorphism :
If function symbols are resolved at runtime, it is called run time polymorphism.

Run time polymorphism is also called as dynamic binding or run time binding or late binding.

ex : function overriding

To implement the run time polymorphism we need hierarchical inheritance 

parent pointer

## vitual functions
A virtual function is a member function in the base class that can be overridden in derived classes.

Virtual functions are a key part of polymorphism in C++. They let different objects respond differently to the same function call.

### Why Use Virtual Functions?
Without virtual, C++ decides which function to call based on the pointer type, not the actual object type.

Without virtual: the base function runs, even if the object is from a child class.

```cpp
class Animal {
  public:
    void sound() {
      cout << "Animal sound\n";
    }
};

class Dog : public Animal {
  public:
    void sound() {
      cout << "Dog barks\n";
    }
};

int main() {
  Animal* a;  // Declare a pointer to the base class (Animal)
  Dog d;  // Create an object of the derived class (Dog)
  a = &d;  // Point the base class pointer to the Dog object
  a->sound(); // Call the sound() function using the pointer. Since sound() is not virtual, this calls Animal's version
  return 0;
}
```
Even though a points to a Dog, it still calls Animal::sound() because the function is not virtual.

With virtual, it checks the actual object the pointer is pointing to.

With virtual: the child's version runs, like you expect.

```cpp
class Animal {
  public:
    virtual void sound() {
      cout << "Animal sound\n";
    }
};

class Dog : public Animal {
  public:
    void sound() override {
      cout << "Dog barks\n";
    }
};

int main() {
  Animal* a;
  Dog d;
  a = &d;
  a->sound(); // Outputs: Dog barks
  return 0;
}
```
Now it works! Because sound() is virtual, the call uses the actual object's function and not just the pointer type

- Use virtual only in the base class
- Use override (optional, but recommended) in the derived class for clarity




Pure virtual functions is a member function of a parent class whose definition is assigned with zero.

- Syntax : virtual returntype datatype funname()=0;

Eg : virtual void foo()=0;

For an abstract class we cannot create objects, but we can create pointers and references to it.

Note : If child class is not redefining the pure virtual functions then child class also becomes abstract class.

When a class contains virtual functions, compiler creates a virtual table.

### What is virtual table?
A virtual table is a static array of function pointers, which stores virtual functions address.

To create the connectivity between the class and virtual table compiler adds a hidden pointer called virtual pointer or vptr as a data member to the class.

Virtual table cannot be inherited.

vptr will be inherited to child class.

### Is virtual functions are faster or normal functions?
Normal functions are faster.


## Template :
Templates are powerful features of C++ which allows you to write generic programs .In simple terms, you can create a single function or a class to work with different data types using templates.

Templates are often used in larger codebase for the purpose of code reusability and flexibility of the programs.

Templates let you write a function or class that works with different data types.

The concept of templates can be used in two different ways:

 1.Function Templates

 2.Class Templates 

Templates are used to implement the generic programming in c++.

syntax to create generic functions

```cpp
template <typename T>
return_type function_name(T parameter) {
  // code
}
```

Example for function templates :

```cpp
#include<iostream>
using namespace std;
template <typename T>
T add(T a , T b){
        T c;
        c=a+b;
        return c;
}
int main(){
        cout<<add<int>(10,20)<<endl;
        cout<<add<float>(10.2,11.7)<<endl;
}
```

Example for function templates :

```cpp
#include<iostream>
using namespace std;
template <class T>
class box{
        T value;
        public:
        box(T v){
                value=v;
        }
        T getvalue(){
                return value;
        }
};

int main(){
        box<int>b1(10);
        box<string>b2("Hello");

        cout<<b1.getvalue()<<endl;
        cout<<b2.getvalue()<<endl;
}
```

## Structures :
It is a userdefined datatype that is used to combine data of different types.It is similar to an array but unlike an array, which stores elements of the same type, a structure can store elements of different data types. C++ structures can also have member functions to manipulate its data.

- create structure
A structure has to be defined before being usable in the program. It is defined using struct keyword.
```cpp
struct structure_name{
    type1 member1;
    type2 member2;
    .
    .
    typeN memberN;
};
```
This definition does not allocate any memory to the structure. We have to create structure variables separately to use it.
```cpp
structure_name var_name;
```
We can also assign some values to the members:
```cpp
struct structure_name = {val1, val2, ..., valN};
```
example :
```cpp
#include<bits/stdc++.h>
using namespace std;
struct student {
        int id;
        char name[100];
        float marks;
};
int main(){
        struct student s={01,"sravani",92.05};

        cout<<s.id<<endl;
        cout<<s.name<<endl;
        cout<<s.marks<<endl;

}
```

## Union :
In C++, union is a user-defined datatype in which we can define members of different types of data types just like structures but unlike a structure, where each member has its own memory, a union member shares the same memory location.

- create union
```cpp
union union_name{
    type1 member1;
    type2 member2;
    .
    .
    typeN memberN;
};
```
Then we can create union variables:
```cpp
union_name var_name;
```
Only one member of a union stores memory at one time.
```cpp
var_name.member1 = val
```
Example :
```cpp
#include<bits/stdc++.h>
using namespace std;
union student {
        int id;
        char name[10];
        float marks;
};
int main(){
        union student s;

        s.id=1;
        cout<<s.id<<endl;

        strcpy(s.name,"sravani");
        cout<<s.name<<endl;

        s.marks=93.07;
        cout<<s.marks<<endl;
}
```

## Enumeration
In C++, enumeration (enum) is a user-defined type that consists of a set of named integral constants. Enumerations help make the code more readable and easier to maintain by assigning meaningful names to constants.

- create Enums :
Just like all other user defined data types, enums also needs to be defined before we can use it.
```cpp
enum enum_name {
    value1, value2, value3…..valueN
};
```
Once defined, it can be used in the C++ program.
```cpp
enum_name var_name = value
```
Example :
```cpp
#include<bits/stdc++.h>
using namespace std;
int main(){
        enum student {
                male,female
        };

        student s = male;

        switch(s){
                case male :
                        cout<<"Who is he?"<<endl;
                        break;

                case female :
                        cout<<"Who is she?"<<endl;
                        break;

                default :
                        cout<<"Who is they"<<endl;
        }
}
```

## C++ Standard Template Library (STL):
In C++, the Standard Template Library (STL) provides a set of programming tools to implement algorithms and data structures like vectors, lists, queues, etc.

STL implements these data structures and algorithms using general-purpose classes and functions that have been tested rigorously.

C++ STL has 3 major components:
- Container
- Iterator
- Algorithms

### Containers :
STL containers store data and organize them in a specific manner as required.

For example, vectors store data of the same type in a sequential order. Whereas, maps store data in key-value pairs.

We can classify STL containers into 3 types:

1. Sequence Container    
    - vector
    - Dequeue
    - List
2. Associative container
    - Sets
    - Multisets
    - Maps
    - Multimaps
3. Container adaptor / Derived container
    - stack
    - queue
  
- Sequence containers: These are used to implement sequential data structures like a linked list, array, etc.
- Associative containers: These are those containers in which each element has a value that is related to a key. They are used to implement sorted data structures, for example, set, multiset, map, etc.
- Containers adapters: Container adapters can be defined as an interface used to provide functionality to the pre-existing containers.

### Iterators :
Iterators are used to access data in the containers, and it helps in traversing through elements of containers using its functions. They can be incremented and decremented as per choice and help in the manipulation of data in the container.

Iterator functions are:
- begin(): This function points the iterator to the first element of the container.
- end(): This function points the iterator to the last element of the container.

### Algorithms :
In STL, different types of algorithms can be implemented with the help of iterators. Algorithms can be defined as functions applied to the containers and provide operation for the content of the container. for example : sort(), swap(), min(), max() etc.

Types of algorithms:
  - Modifying algorithms
  - Non-modifying algorithms
  - sorting algorithms
  - searching algorithms
  - Numeric algorithms



## Encapsulation :
Encapsulation is the process of wrapping (binding) data and functions into a single unit (class) and protecting that data from outside access.

It also means data hiding using access modifiers like:
 - private
 - public
 - protected

- Example :
```cpp
class Student {
private:
    int marks;  // hidden

public:
    void setMarks(int m) {
        if (m >= 0 && m <= 100)  // validation
            marks = m;
        else
            marks = 0;
    }

    int getMarks() {
        return marks;
    }
};
```
- marks is private → cannot be accessed directly.
- setMarks() and getMarks() control how data is set and retrieved.
- This is Encapsulation.


## Abstraction :
Abstraction means showing only the important details to the user and hiding all the unnecessary internal working.

- Focus on what it does, not how it works.
```cpp
class Car {
public:
    void start() {
        // user only sees this function
        engineStart();   // hidden function
        fuelCheck();     // hidden function
        ignition();      // hidden function
    }

private:
    void engineStart() {}
    void fuelCheck() {}
    void ignition() {}
};
```


## Vector 
 A vector is a dynamic array in c++.

 It can grow and shrink in size automatically during runtime, unlike normal arrays(whose size is fixed).

 To use a vector,we must include:
 ```cpp
#include <vector>
```

syntax:
```cpp
vector<datatype> vectorname;
```

Common Functions Used with Vector

| Function         | Meaning                          |
| ---------------- | -------------------------------- |
| `push_back(x)`   | Insert element at end            |
| `pop_back()`     | Remove last element              |
| `size()`         | Returns number of elements       |
| `at(i)`          | Access element at index i (safe) |
| `operator[]`     | Access element like `v[i]`       |
| `clear()`        | Remove all elements              |
| `empty()`        | Check vector is empty or not     |
| `begin(), end()` | Used in loops/iterators          |

- code
```cpp
#include<iostream>
#include<vector>
using namespace std;
int main(){

        vector<int> v = {10,20,30};

        // Adding element at last
        v.push_back(40);

        for(int i=0;i<v.size();i++){
                cout<<v[i]<<" ";
        }
        cout<<endl;

        // Delete last element
        v.pop_back();

        // Insert element at particular position from begin
        v.insert(v.begin(),90);

        for(int i=0;i<v.size();i++){
                cout<<v[i]<<" ";
        }
        cout<<endl;

        // Insert element at particular position from end
        v.insert(v.end(),70);

        for(int i=0;i<v.size();i++){
                cout<<v[i]<<" ";
        }
        cout<<endl;

        // print element at particular position
        cout<<v.at(0)<<endl;


}
```









 








