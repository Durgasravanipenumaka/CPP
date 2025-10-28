## Print Hello world :
```cpp
#include<iostream>
using namespace std;
int main(){
        string str;
        cout<<"Enter the string:";
        getline(cin,str);
        //cin>>str;
        cout<<"Entered string:"<<str<<endl;
}
```
## Sum of Two Numbers
```cpp
#include<iostream>
using namespace std;
int main(){
        int a,b;
        cout<<"Enter a and b values:";
        cin>>a>>b;
        cout<<"sum:"<<a+b<<endl;
}
```
## Even or Odd
```cpp
#include<iostream>
using namespace std;
int main(){
        int a;
        cout<<"Enter the number :";
        cin>>a;
        if(a%2==0)
                cout<<"Even"<<endl;
        else
                cout<<"Odd"<<endl;
}
```
## Largest of Two Numbers
```cpp
#include<iostream>
using namespace std;
int main(){
        int a,b;
        cout<<"Enter the a and b values:";
        cin>>a>>b;
        if(a>b)
                cout<<a<<" is greater than "<<b<<endl;
        else
                cout<<b<<" is greater than "<<a<<endl;
}
```
## Swapping od two numbers
```cpp
#include<iostream>
using namespace std;
int main(){
        int a,b;
        cout<<"Enter a and values:";
        cin>>a>>b;
        cout<<"Numbers before swapping : "<<a<<" "<<b<<endl;
        a=a+b;
        b=a-b;
        a=a-b;
        cout<<"Numbers after swapping : "<<a<<" "<<b<<endl;
}
```
## Write a program to dynamically an array,print them,multiply use any number and display them.
```cpp
#include<iostream>
using namespace std;
int main(){
        int n;
        cout<<"Enter size of the array:";
        cin>>n;
        int *arr = new int[n];
        cout<<"Enter the elements in the array:";
        for(int i=0;i<n;i++){
                cin>>*(arr+i);
        }
        cout<<"Elements in the array :";
        for(int i=0;i<n;i++){
                cout<<arr[i]<<" ";
        }
        cout<<endl;
        int m;
        cout<<"Enter the to multiply the array:";
        cin>>m;
        cout<<"Elements after multiplied with a number:";
        for(int i=0;i<n;i++){
                cout<<arr[i]*m<<" ";
        }
        delete[] arr;
}
```
## Reverse the string 
```cpp
#include<iostream>
using namespace std;
int main(){
        string str;
        cout<<"Enter the string:";
        cin>>str;
        int len=str.length();
        for(int i=0,j=len-1;i<j;i++,j--){
                char temp=str[i];
                str[i]=str[j];
                str[j]=temp;
        }
        cout<<"string after reversing:"<<str<<endl;
}
```
## Write a C++ program using structures to read details of N employees (name, ID)
```c
#include<iostream>
using namespace std;
struct emp{
        string name;
        int empid;
};
int main(){
        int n;
        cout<<"Enter the number of employees details are taking:"<<endl;
        cin>>n;
        struct emp s[n];
        for(int i=0;i<n;i++){
                cout<<"Enter the name of the employee "<<i+1<<":";
                cin>>s[i].name;
                cout<<"Enter the id of employee "<<i+1<<":";
                cin>>s[i].empid;
        }
        cout<<"Details:"<<endl;
        for(int i=0;i<n;i++){
                cout<<"Name:"<<s[i].name<<" ";
                cout<<"Empid:"<<s[i].empid<<endl;
        }
}
```
