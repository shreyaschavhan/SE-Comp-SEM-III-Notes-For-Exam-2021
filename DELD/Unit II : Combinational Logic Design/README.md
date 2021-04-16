# Unit II: Combinational Logic Design

> * Notes: 
> 	* A'B + AB' = A exor B
> 	* A + A'B = A + B

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

---

* Half Subtractor:
> * Half subtractor is a combinational ckt used to get the difference between tow single bit numbers.
> * Steps:
> 	* Truth Table
> 		* ![image](https://user-images.githubusercontent.com/68887544/114850455-66fc5900-9dfe-11eb-81a9-e05fd29aec24.png)
> 	* K-map:
>		* K-map for difference : A ex-or B
>		* K-map for borrow : A'B
> 	*  Draw ckt diagram

---

* Full Subtractor:
> * Combinational ckt used to get difference of 3 bits
> * Steps:
> 	* Truth Table:
>		* ![image](https://user-images.githubusercontent.com/68887544/114851456-7cbe4e00-9dff-11eb-89c5-1423e60bf79f.png) 
> 	* K-map:
> 		* K-map for difference: A exor B exor bout
> 		* K-map for bout : Bbin + A'B + A'bin
> 	* draw logic diagram

--- 

* Full adder using half adder:
> * Diagram:
> 	* ![image](https://user-images.githubusercontent.com/68887544/114852957-ec810880-9e00-11eb-94de-1fc7e7ea476f.png)
> * For half adder:
> 	* Sum = A exor B
> 	* Carry = AB
> * Solution:
> 	* ![image](https://user-images.githubusercontent.com/68887544/114854773-cb211c00-9e02-11eb-8bd5-514d48529dd7.png)

---

* Carry Look ahead adder:
> * Carry Genaration:
>   * ![image](https://user-images.githubusercontent.com/68887544/114856331-99a95000-9e04-11eb-8834-a13bd317767b.png)
> * Diagram :
>   * ![image](https://user-images.githubusercontent.com/68887544/114863508-7040f200-9e0d-11eb-93aa-09f0220ca09c.png)

---

* BCD Adder:
> * If sum is greater than 9 then circuit should show output 1
> * Ex. 
>   * ![image](https://user-images.githubusercontent.com/68887544/114866034-b64b8500-9e10-11eb-890f-5482d5d2cee5.png)
> * K-map for output
> * Prime implicant grouping
> * Y = S<sub>4</sub>S<sub>3</sub> + S<sub>4</sub>S<sub>2</sub>
> * Draw logic Diagram
>   * ![image](https://user-images.githubusercontent.com/68887544/114867343-4fc76680-9e12-11eb-8571-0fb66e89efa4.png)
 
---

* BCD Addition:
> * when bcd addition exceed 9 then it is invalid bcd
> * then add 6 i.e 0110 for correction 
> * you will get actual addition.

---

* Multiplexer:
> * Multiplexer is a  combinational logic circuit used to select only one input among several inputs based on selection lines
> * This can act as digital switch.
> * This is also called as data selector.
> * For a MUX there can be 2^n inputs, n selection lines & only one output
> * Block Diagram
> 	* ![image](https://user-images.githubusercontent.com/68887544/114868655-c9138900-9e13-11eb-8fcc-c22232c5270d.png)
> * 2x1 MUX:
> 	* ![image](https://user-images.githubusercontent.com/68887544/114869565-c36a7300-9e14-11eb-94c3-68b982b3190f.png)
> * 4x1 MUX:
> 	* ![image](https://user-images.githubusercontent.com/68887544/114870229-8783dd80-9e15-11eb-8687-fdc9f607c0d5.png)
>   * ![image](https://user-images.githubusercontent.com/68887544/114870301-9ff3f800-9e15-11eb-8656-967a192a521a.png)

---

* Demultiplexer (DeMux)
> * One input and many output
> * Reverse operation of multiplexer
> * one to many ckt or data distributor 
> * Block Diagram
>  * ![image](https://user-images.githubusercontent.com/68887544/114979247-2822dd80-9ea8-11eb-9fc1-5d4442f13102.png)
> * n = 2^m --> Number of  output lines
> * m = log<sub>2</sub>n --> no. of select lines

---

* Decoder:
> * Decoder is a multi-input multi-output logic circuit which decodes n inputs into 2^n possible outputs 
> * Block Diagram:
> 	* ![image](https://user-images.githubusercontent.com/68887544/114981277-5950dd00-9eab-11eb-815d-0038fb40ae97.png)
> * 2 to 4 Decoder
> 	* Truth Table
> 	 * ![image](https://user-images.githubusercontent.com/68887544/114981701-0592c380-9eac-11eb-8be1-61f069b1621d.png)
> 	* Y<sub>3</sub> = AB
>	* Y<sub>2</sub> = AB'
> 	* Y<sub>1</sub> = A'B
> 	* Y<sub>0</sub> = A'B'
> 	* Logic Diagram:
>		* ![image](https://user-images.githubusercontent.com/68887544/114982290-e183b200-9eac-11eb-917e-8e5dada818c1.png)
