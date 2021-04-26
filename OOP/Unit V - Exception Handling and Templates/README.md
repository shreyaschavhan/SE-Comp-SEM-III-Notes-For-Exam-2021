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
>   * ```
>       return_type function_name(arguments) throw (type list){
>   // body of the function
> }
>   ```
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
