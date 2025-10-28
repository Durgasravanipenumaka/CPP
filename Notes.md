## What is the difference between c and cpp ?
### C :
- C is a Procedural (Structured) Programming Language .
- It focus mainly on functions and procedures.
- It follows Top-down approach(divide the program into smaller functions).
- OOPs concept is not supported.
- Less secure.
### C++ :
- CPP is a Object-Oriented Programming Language (OOP).
- It mainly focus on objects and classes.
- It follows bottom-ip approach(combine data and functions into objects).
- It supports OOP — classes, inheritance, polymorphism, abstraction, encapsulation.
- More secure — data can be hidden inside classes using access specifiers (private, protected, public).

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
- int scanf(const char *,...);               cin>>
- cin = istream class predefined object      >> = extraction operator
- ex : scanf("%d",&x);                       cin>>x;
- scanf("%d %s %f",&x,&s,&v);                cin>>x>>s>>v;

- int printf(const char *,...)                cout<<x;
- cout = ostream class predefined object     << = Insertion operator
- ex : printf("hello");                      cout<<"hello";
- printf("%d",x);                            cout<<x;

## Datatypes :
- datatypes are two types :
- 1.Primary datatype
- 2.Secondary datatype
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


- unicode table -> unisersal code table, which contains the symbols of all the languages which are world wisely certified.

#### wchart_t : 
- wide character is used to represent is used to represent symbols of unicode.
#### What is the size of wchar_t?
- 2 bytes on 16-bit complier.
- 4 bytes on 32-bit or 64-bit complier.
  
- ascii table is also part of unicode table.

#### bool :
- while(true)           while(1)
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
- 2.Reference must be unintialized at the time of its declaration.
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
- In call by reference ,formal arguments are references of the actual arguments, so formal arguments doesnot consume extra memory they refer to the actual arguments memoty blocks,so,whatever we modify on formal arguments they reflect on actual arguments.
- function call,function definition are same as call by value.










## Storage classes :
- In C we have 4 types of storage classes.
- In C++ we have 5 storage classes.
- 1.auto
- 2.register
- 3.static
- 4.extern
- 5.mutable -> applicable only to the data memmbers of a class.

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
- 1.public
- 2.private
- 3.protected

- private members are accessible only by the members of the structure or class.
- protected members are accessible only by the members and child of the class or structure.
- public members are accessible by members and non members.
- By default members of the structure are public in nature ,so we go with class datatype.

- In C++ encapsulation is implemented using structures and classes.
#### What is encapsulation?
- Binding of data and its related functionalites into a single entity is called Encapsulation.

#### Class :
- A class is a userdefined datatype , which is combination varaibles and functions.
- Variables inside the class are called as Datamembers
- Functions of a class are called member functions
- Both together are called as members of the class.

#### What is a class ?
- A class is a blue of an object.
- A class is a logical representation of an object.

#### What is an object ?
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


 








