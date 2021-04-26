# Unit III - Polymorphism
---

* What is function overloading? 
> * When multiple functions are used with the same name with different parameters. Such functions are called as overloaded functions and the concepts are called as function overloading.
> ```
> #include <iostream>
> using namespace std;
> 
> void function(){
> //code here
> }
> void function(int a){
> // code here
> }
> int main(){
>   cout << function() << endl;
>   cout << function(3) << endl;
>   
>   return 0;
> }
> 

---

* What is operator overloading?
> * In C++, we can make operators like (+) plus, etc do stuffs that we want and are not supposed to do by default. This is called as operator overlaoding.
> * Eventhough we can overload the operators to do other stuff, but we cannot change the semantics of the operator. For example, + is an binary operator which requires two operands to perform addition. After overloading, the plus operator will still require two operands.
> * Ex.
> ```
> #include <iostream>
> using namespace std;
>
> class complex{
> private:
>   int real, imag;
> public:
>   complex(int r=0, int i=0){
>     real = r;
>     imag = i;
>   }
>   complex operator+ (complex const &obj){
>     complex res;
>     res.real = real + obj.real;
>     res.imag = imag + obj.imag;
>     return res;
>   }
>   void print(){
>     cout << real << " + i" << imag << endl;
>   }
> };
> int main(){
>   complex c1(10, 20), c2(2,5);
>   complex c3 = c1+c2; // call operator+
>   c3.print();  
> }
> return 0;
> ```
-----------

