# Unit V - Exception Handling and Templates

## &#10023; Syllabus:
> * Exception Handling:
>   * Fundamentals
>   * other error handling techniques
>   * simple exception handling - Divide by zero
>   * Multiple catching
>   * re-throwing an exception
>   * exception specifications
>   * user defined exceptions
>   * processing unexpected exceptions
>   * constructor
>   * destructor and exception handling
>   * exception and inheritance
> * Templates:
>   * The power of templates
>   * Function Template
>   * overloading function templates
>   * and class template
>   * class template and non type parameters
>   * template and friends generic functions
>   * the type name and export keywords.

---

## &#10023; Exception Handling:

* Fundamentals:
> * Exception:
>   * An exception is a problem that arises during the execution of program.
>   * Exceptions provide a way to transfer control from one part of a program to another.
>   * C++ Exception handling keywords:
>       * try
>       * catch
>       * throw
>   * throw:
>       * A program throws an exception when a problem shows up. This is done using a throw keyword.
>   * catch:
>       * A program catches an exception with an exception handler at the place in a program where you want at the place in a program where you want to handle the problem. The catch keyword indicates the catching of an exception.
>   * try:
>       * A try block identifies a block of code for which particular exceptions will be activated. It's followed by one or more catch blocks.
>   * A try/catch block is placed  around the code that might generate an exception.
>   * Code within a try/catch block is referred to as protected code.
>   * We can list down multiple catch statements to catch different type of exceptions in case our try block raises  more than one exception in different situations.
> * Throwing exception:
>   * exceptions are thrown using throw block and this throw block can be used anywhere in the code.
> * Catching exceptions:
>   * catch block catches any exception.
>   * we can specify what type of exception you expect.
>   * to catch any kind of exception we use
>        ```
>        catch(...){
>               // code
>           }
>

---

* Other exception handling techniques:
> * In C++ standard exceptions are defined in ```<exception>``` which we can use in our programs.
> * ![image](https://user-images.githubusercontent.com/68887544/116031137-adfa1200-a67a-11eb-9bea-9ec8ebe4050c.png)
> * Description of each exception:
>   * ![image](https://user-images.githubusercontent.com/68887544/116031292-ff0a0600-a67a-11eb-85b8-4f914afc1fba.png)
>   * ![image](https://user-images.githubusercontent.com/68887544/116031337-121cd600-a67b-11eb-9e09-cf3066706303.png)

----

* Simple Exception Handling - Divide by Zero:
> * ![image](https://user-images.githubusercontent.com/68887544/116037805-39c56b80-a686-11eb-8d48-fc0404e99600.png)

---

* Multiple Catching:
> * We can use multiple catch blocks for one try block
> * But we cannot use multiple try block and one catch block.

---
* Rethrowing an Exception:
> * Exception handler may decide to rethrow exception without handling it.
> * In this situation we call following statment: ``` throw;  ```
> * No arguments should be passed to throw keyword.
> * throw statement causes current exception to be thrown to next try catch clause. Exception is caught by next enclosing try..catch blocks.

---

* Exception Specifications:
> * If we wanted to throw only certain exception, we can do it using specified conditions.
> * In this case exception will be thrown only for specified conditions and not for all the conditions.
> * It is possible by adding throw list clause during function definition.
> * the syntax for creating specific expection is :
>   ```
>   return_type function_name(arguments) throw (type list){
>     // body of the function
>   }
>   
> * If we throw any other exception then abnormal program termination occurs.
> * Example of empty throw list is as follows which guarantees not to throw any type of exception.
>   * ```throw();```

---

* User Defined Exception:
> * User defined exception or custom exception is creating your own exception class and throws that exception using 'throw' keyword. This can be done by extending the class Exception.
> * This can be done using ```what()```

---

* Processing unexpected exceptions:
> * Even after handling exceptions, there may be unexpected exceptions.
> * If no exception handler found then program terminate abnormally.
> * The process of removing function from function stack during runtime is called as stack unwinding.
>

---

* Constructor, Destructor and Exception Handling:
> * ![image](https://user-images.githubusercontent.com/68887544/116042625-3e8d1e00-a68c-11eb-8b3e-a5b60c470610.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116042667-4f3d9400-a68c-11eb-9e5c-0920c9499d15.png)
>
---

* Exception and Inheritance:
> * If both base and derived class caught exception then catch block of derived class must appear before the base class.
> * If we put base class catch block first then derived class catch block will never reach.
> * It means catch block of derived class should be before catch block of base block.

----

## &#10023; Templates:

* Generic Programming:
> * In this kind of programming type  of data is specified at run time.
> * Generic programming is approach of creating generalize algorithms which are applicable for all data types.
> * Template is best example of generic programming in C++.

---

* Power of Templates:
> * It allows us to define generic classes and functions.
> * Templates are useful in achieving dynamic polymorphism.
> * Template is way of creating generalize functions and classes which are applicable for all data types without changing the definition of the program.
> * Template can be function template or class templates.

---
* Need of Templates in C++:
> * Templates are needed bcz it allows functions and classes classes to operate with generic types. This allows a function or class to work on many different data types without being rewritten for each one.

---

* Function Template:
> * General syntax for creating function template:
> ``` template<typename T>
> return_type function_name(T type argument){
> // code
> }
> ``` 
> 
> * In above syntax, T is generic variable.
> * We set any data type for T.
> * T is user-defined name and can be some other name also.
> * We can pass more than one argument to function template also.
> * We use template when we want to use different data types for same operation.
> * We use function overloading when we want to use same data type but different operations.
> * Template cannot take varying numbers of arguments. But Function overloading can take varying number of arguments.
> * In addition, a template indicates that you can operate on any data type, but it's pointless to represent this when in fact, the vast majority of templates would be specializations only.
> * Also, overloads can be virtual and template specification cannot.
> * Syntax of function calling with function template is as follows:
>   * ![image](https://user-images.githubusercontent.com/68887544/116060283-5cb04980-a69f-11eb-91a1-0ce301bed96b.png)

---

* Overloading Function Template:
> * ![image](https://user-images.githubusercontent.com/68887544/116061794-e6ace200-a6a0-11eb-87c8-fbcef93071f8.png)

---

* Overloading Class Template:
> * ![image](https://user-images.githubusercontent.com/68887544/116061884-fe846600-a6a0-11eb-80b9-8e34395d18fb.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116061919-09d79180-a6a1-11eb-862b-7f68e01e1bce.png)
> 

--- 

* Class template and Nontype parameters:
> * ![image](https://user-images.githubusercontent.com/68887544/116062125-41ded480-a6a1-11eb-9d1b-0473dfa5e1ba.png)

---

* Template and Friends Generic Functions:
> * ![image](https://user-images.githubusercontent.com/68887544/116062293-63d85700-a6a1-11eb-8e7e-604464a2ad86.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116062341-6d61bf00-a6a1-11eb-86f8-47eb7e7908c4.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116062375-7488cd00-a6a1-11eb-96d8-20a6aee63b45.png)

---

* The type name and export keyword:
> *  In a template declaration, typename can be used as an alternative to class to declare type template parameters and template parameters.
> * Inside a declaration or a definition of a template, typename can be used to declare that a dependent qualified name is a type.
> * Inside a declaration or a definition of a template, typename can be used before a non-dependent qualified type name. It has no effect in this case.
> * Inside a requirements for type requirements.
> * ![image](https://user-images.githubusercontent.com/68887544/116062895-f842b980-a6a1-11eb-9a91-21e4d4080b54.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116062935-02fd4e80-a6a2-11eb-999c-f471589fcded.png)
> 
---
> P.S. Done Unit V - Exception Handling and Templates
