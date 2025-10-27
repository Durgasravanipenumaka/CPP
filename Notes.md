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
### 1.Primary datatype :          Derived datatype :          User-defined datatypes :
- char                            - Arrays                    - Structures
- int                             - strings                   - Unions
- float                           - pointers                  - enums
- double                                                      - Typedef
- wchar_t                                                     - class
- bool
- string

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
| Scope resolution Operator |   ::   | resolves the scope of the variable |
| Line feed operator | endl | supply the new line |
