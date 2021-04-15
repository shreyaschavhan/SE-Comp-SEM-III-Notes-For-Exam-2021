# Unit II: Combinational Logic Design


* Introduction:

> * Output is dependent upon combination of input variables
> * Doesn't use any memory
> * It can have n number of inputs and n numbmer of outputs

---

* Designing setps for a combination ckt

> * Steps:
> 	* Determine the required input and output variables
> 	* Assign the letters / symbols to the input variables
> 	* Make truth tables 
> 	* determine the simplified boolean expression using k-map
> 	* Draw logic diagram using boolean expression

---

* Excess 3 - Code 

> * In excess 3 - we add 3 for each and every digit
> Example: 
>
> 22 ---> 0010 0010
> 
> 33 ---> 0011 0011
> 
> -+-+-+-+-+-+-+-+-
> 
> 55 ---> 0101 0101
>
> 25.35
> 
> 33.33
> 
> -+-+-+-+-+-+-+-+-
> 
> 58.68 ---> decode it  = 01011000.01101000

----

* BCD Code (Binary Coded Decimal)
> * 12 in binary 1100
> * 12 in BCD 0001 0010
> * In BCD, take two digits seperately and combine them.
> 

---

* Gray Code
> 
> * Known as unit distance code or reflexive code
> * Uses Ex-or gate rule for conversion
> * Binary to Gray Code 
> 	* EX.
> 	* decimal | binary | process | gray
> 	   ---|---|---|---
> 	   0 | 0000 | Take first bit as it is --> ex-or previous with current like 0 exor 0  | 0000
> 	   1 | 0001 | - | 0001
> 	   2 | 0010 | - | 0011
> 	   3 | 0011 | - | 0010
> 	   4 | 0100 | - | 0110
> 	* and so on
> 	*  with every decimal number, you will observe that only 1 bit is being changed, thats why it is known as unit distance code
> * BCD to gray:
> 	* Similar to binary to gray

---

* Gray to Binary Conversion
> * Step: 
> 	* Take first bit as it is
> 	* Cross Ex-Or 
> 	* Write the result
> * Example : ![image](https://user-images.githubusercontent.com/68887544/114829183-648f0480-9de8-11eb-8daa-0d1c14185382.png)

> Note: If you are taking gray to  binary then cross ex-or and if binary to  gray then just ex-or .

---

* BCD to Excess 3
> * Steps:
> 	* Write BCD into equivalent Decimal
> 	* Subract 3 from it
> 	* Write the resultant into BCD form

---

* Half Adder
> Designing of Half Adder:
> * Half adder is a combinational logic circuit designed to add two single bit numbers.
> * It contains two inputs and two outputs (Sum and carry)
> * ![image](https://user-images.githubusercontent.com/68887544/114831529-1d564300-9deb-11eb-919f-07467dfe6df9.png)
> * Steps:
> 	* Observe problem
> 	* Two inputs
> 	* Write truth table
> 	* Ex. 
> 	* ![image](https://user-images.githubusercontent.com/68887544/114832005-9fdf0280-9deb-11eb-8ee5-98ae70c58f75.png)
> 	* Define k-map
> 		* K-map for sum: A exor B
> 		* K-map for carry: AB
>	* Draw circuit diagram 

---

* Full Adder
> Designing Full adder
> * Full adder is a arithmetic logic circuit Designed to add two single bit numbers with a carry.
> * ![image](https://user-images.githubusercontent.com/68887544/114832646-55aa5100-9dec-11eb-94bf-4509c6340f46.png)
> * Full adder is similar to  half adder, the only difference is full adder overcomes the limitation of half adder, since half adder cannot add carry but full adder can.
> * Step I:	
>	* Truth table: 
> 	* ![image](https://user-images.githubusercontent.com/68887544/114833690-7b842580-9ded-11eb-8412-72dc94992670.png)
> 	* Draw K-map for three variable
>		* K-map for sum: A exor B exor C 
>		* K-map for carry: BCin + AB + ACin
> 	* Draw Ckt diagram

