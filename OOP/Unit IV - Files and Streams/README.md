# Unit IV - Files and Streams

## ✧ Syllabus:
> * Data Hierarchy
> * Stream and Files
> * Stream Classes
> * Stream Errors
> * Disk File I/O with Streams
> * File Pointers
> * and Error Handling in File I/O
> * File I/O with Member Functions
> * Overloading the Extraction and Insertion Operators
> * Memory as a stream object
> * Command - Line Arguments
> * Printer output

---
## ✧ Content: 
* Data Hierarchy:
> * All computer processes works in bits, represented by 0s and 1s
> * The data processed by computers form a data hierarchy:
>   * The data items become larger and more complex in structure as we progress from bits to characters to fields to larger data aggregates:
>   * ![image](https://user-images.githubusercontent.com/68887544/115666913-cc060080-a362-11eb-9e8a-23578fbfcb23.png)

---

* Streams and Files:
> * Streams:
>   * Streams are the sequence of characters
>   * Characters can be wild card or normal.
>   * Stream works with all built in data types.
>   * Stream is an serial interface to storage, buffer files or any other storage medium.
>   * One of such example is <iostream> header file in cpp
>   * It contains __istream__ for input and __ostream__ for output.
>   * For file  handling we use __ifstream__ for input and __ofstream__ for output
>   * It acts as both source and destination.
>   * source stream refers from where input is taken.
>   * destination stream refers where output is generated.
>   * ![image](https://user-images.githubusercontent.com/68887544/115669160-99a9d280-a365-11eb-8466-cd19444953b2.png)

---

* Stream Classes:
> * The input output classes that are used to manage input and output of a system is known as stream class.
> * All classes are declared in header file.
> * Classification of stream classes:
>   * ![image](https://user-images.githubusercontent.com/68887544/115670056-9e22bb00-a366-11eb-8d17-a8e028e56b0e.png)
>   * ios is base of all Classes
>   * istream is used for input purpose
>   * ostream is used for output purpose.
>   * iostream is used for both input and output.
>   * ifstream is used for input from file.
>   * ofstream is used for output to file.
>   * fstream is used for both input and output with file.
> * Elements of iostream:
>   * ![image](https://user-images.githubusercontent.com/68887544/115671570-48e7a900-a368-11eb-9340-c5a96292f1f4.png)
> * Objects in iostream:
>   * cin : 
>       * Standard input Stream object
>       * Object of istream class 
>   * cout :
>       * Standard output stream object 
>       * Object of ostream 
>   * cerr:
>       * Standard output stream for error.
> * Manipulators in iostream class:
>   * ![image](https://user-images.githubusercontent.com/68887544/115673244-0aeb8480-a36a-11eb-8240-2893d794c957.png)
>   * ![image](https://user-images.githubusercontent.com/68887544/115673290-18087380-a36a-11eb-92d7-f67b1fb67989.png)

---

* cin & cout:
> * cout: 
>   * object of ostream class 
>   * object is connected to standard output devices
>   * it is used with insertion operator (<<)
>   * we can overlaod << to display object. 
> * cin:
>   * object of istream class
>   * object is connected to standard input Stream
>   * used with get operator >>
>   * we can overload the >> operator 

---

* Stream Errors:
> * stream errors occurs when user input characters instead of numbers, or entering string instead of character and so on.
> * functions to check state of stream:
>   * ![image](https://user-images.githubusercontent.com/68887544/115679319-1346be00-a370-11eb-975e-e954e3317c39.png)
> * Example:
>   * ![image](https://user-images.githubusercontent.com/68887544/115679602-60c32b00-a370-11eb-9cc0-88ffa53e0901.png)
>   ![image](https://user-images.githubusercontent.com/68887544/115679734-82bcad80-a370-11eb-8ad9-69620bc8393d.png)
> ![image](https://user-images.githubusercontent.com/68887544/115679757-8a7c5200-a370-11eb-83d4-8662badd0d47.png)
> ![image](https://user-images.githubusercontent.com/68887544/115679788-92d48d00-a370-11eb-90f8-3fd53f7d9f4e.png)

---

* Disk File I/O with streams:
> 1. Opening file:
>   * ofstream class is used to open the file.
>   * we create object of ofstream class to open the file
>   * after creating object, it will open the file
>   * if file doesn't already exist then new file is created.
>   * if file already exist then all the content will be truncated means erased.
>   *  ofstream header file need to be included.
>   * Ex. 
>       * ![image](https://user-images.githubusercontent.com/68887544/115680900-9e748380-a371-11eb-9feb-b0d7b6b8b321.png)
>   * It is also possible to open files with open() function.
>   * Ex.
>      * ![image](https://user-images.githubusercontent.com/68887544/115681121-d8de2080-a371-11eb-893c-b41c45f9af15.png)
> 2. Close a file.
>   * C++ close the file by default.
>   * We don't need to close the file explicitly
>   * But we can close the file explicitly using close() function.
> 3. Reading from file
> 4. Writing in file
> 5. Detecting end of file
> 

---

* File Pointers:
> * Each file has two file pointers associated with it.
>   * Input pointer 
>   * Output pointer 
> * Whenever we read or write data, pointer automatically advances to next location.
> * When we open file in read mode, input pointer is automatically located to start of the file. From start of the file we can start reading the file.
> * when we open file in write mode, all content of files are deleted and file pointer is set to beginning of the file.
> * When we want to enter new data in existing file, then we need to  open it in append mode.
> * In append mode, file pointer is set to the end of the file. 
>   * ![image](https://user-images.githubusercontent.com/68887544/115682671-4fc7e900-a373-11eb-975b-3d617abf2ab5.png)
> * Manipulating file pointers:
>   * ![image](https://user-images.githubusercontent.com/68887544/115682765-68d09a00-a373-11eb-9b0b-25391af3322d.png)

---

* Error Handling in File I/O:
> * examples: 
>   * file not found
>   * could not open file
>   * could not read file 
>   * could not write in the file 
> * Error handling is  possible by checking the return value from functions of the object.
> * Error handling functions:
>   * ![image](https://user-images.githubusercontent.com/68887544/115683439-1348bd00-a374-11eb-9190-54a3d1c69123.png)

---

* File I/O with member function:
> * open 
> * read 
> * close 
> * write

---

* Overloading the extraction and insertion operator:
>  ![image](https://user-images.githubusercontent.com/68887544/115684292-ddf09f00-a374-11eb-8301-b55fac51e5e9.png)
>  ![image](https://user-images.githubusercontent.com/68887544/115684401-f2349c00-a374-11eb-8e51-d6a61893bf2b.png)
> ![image](https://user-images.githubusercontent.com/68887544/115684446-fcef3100-a374-11eb-9a26-6f115ae0a672.png)

---

* Memory as Stream object:
> * It is useful when we need to format the output.
> * Family ofstream classes implements in-memory formatting.
> * For writing to memory we use  ostrstream class. It is subclass of ostream class.
> * For reading data from memory we use istrstream which is subclass of istream class.
> * For reading and writing we can use strstream class.
> * Ex.
>   ![image](https://user-images.githubusercontent.com/68887544/115685032-7edf5a00-a375-11eb-9a39-ab883a1d593b.png)
> ![image](https://user-images.githubusercontent.com/68887544/115685111-8f8fd000-a375-11eb-9c78-f1fefd504a26.png)

---

* Command-Line Arguments:
> * We can pass argument to functions.
> * We have main function, we can pass command line arguments to main function at the time of running the program.
> * the syntax of writing main function with command line arguments:
>   * ![image](https://user-images.githubusercontent.com/68887544/115685557-f3b29400-a375-11eb-9b7d-938e487bb39e.png)
> * Steps to run program (are not normal):
>   * Type program
>   * Save program
>   * Compile program in terminal: 
>       * Ex. gcc -o output myprogram.cpp
>   * Run Program using terminal:
>       * Ex. ./output first_arg second_arg third_arg,.....
>   

---

* Printer Output:
> ![image](https://user-images.githubusercontent.com/68887544/115686279-aaaf0f80-a376-11eb-89b6-f7d23155444e.png)
> ![image](https://user-images.githubusercontent.com/68887544/115686332-b7336800-a376-11eb-87df-d110d22c4fa9.png)
> 

----
> P.S. Done Unit IV - Files and Streams 
