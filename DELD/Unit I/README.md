# Unit I : Minimization Technique

> Note: 
> 1. Learn Truth Table
> 2. Minimization Using K-map
> 3. ![image](https://user-images.githubusercontent.com/68887544/114539271-f45e7280-9c71-11eb-8671-feab02ebe21c.png)

---

* Explain following terms: 
> * Product Term 
>   * In Y = AB + BC + AC ; AB, BC & AC are called product terms
> * Sum Term:
>   * In Y = A + C + B ; A + C + B are sum terms 

---

 * Explain SOP & POS :
 > * SOP : 
 >     * The Standard logical expression can be expressed in two forms:
 >       1. SOP 
 >       2. POS
 >     * For example, in logical expression, Y = AB + BC + AC 
 >     * In the above example, The product of input  terms i.e AB, BC & AC are summed together.
 >     * This kind of logical equation is called as SOP form. (Sum of Products)
 > * POS :
 >    * Example: Y = (A + B + C).(A' + B' + C')
 >    * In the above example, the sum of inputs are multiplied with each other.
 >    * Such kind of logical equation is known as POS form. (Product of Sum)
 > * The sum terms and product terms are not actual addition and product, They are actual OR and AND of the inputs.
 > 
---

* Non Standard and Standard SOP & POS

>   ![image](https://user-images.githubusercontent.com/68887544/114351479-4dea7280-9b88-11eb-9f71-533d9da46564.png)

---

* Conversion of Logical Expression to Standard SOP or POS form:
> * Conversion of non-standard sop to standard sop: 
>   * Step I : Find the missing literals
>   * Step II: AND (Product) this term by ORing it with it's complement 
>   * Ex.
>   
>   ![image](https://user-images.githubusercontent.com/68887544/114351847-c9e4ba80-9b88-11eb-8bfc-c6be95c10738.png)
>   * Step III: Simplify
>  
> * Conversion of non-standard POS to standard POS 
>   * Step I : Find missing literals
>   * Step II: OR(Sum) this term by ANDing it with it's complement
>   * Step III: Simplify
>   * EX.
>   
>   ![image](https://user-images.githubusercontent.com/68887544/114352280-53948800-9b89-11eb-8849-255e7f832ac8.png)

>  
 
---

* Properties:
>  * A + A = A
>  * A + BC = (A + B)(A + C)
>  * A.A = A
>  

---

* Conversion of Truth table to SOP & POS
> * SOP:  
>   * Step I: Consider output with Y = 1 only
>   * Step II: Write the product terms (0 for A' and 1 for A)
>   * Step III: Sum those product terms
> 
> * POS:
>   * Step I: Consider output with Y = 0 only
>   * Step II: Write the sum terms (1 for A' and 0 for A)
>   * Step III: Product those terms
>   

---

* Explain K-Map:
> * Easiest way to simplify boolean expression
> * Developed by Karnaugh 
> * Best of variables less than 6
> * The numbers of cells in K-map is 2^n where n is the number of variable
> * With every  cell we can change only 1 bit (According to gray code)
> 

---

* Grouping in K-map:
> * Pairs: Grouping two adjacent 1's will eliminate one variable.
> ![image](https://user-images.githubusercontent.com/68887544/114527948-2a95f500-9c66-11eb-85ff-6804d4227cf4.png)
> * Quads: Grouping a quad will eliminate two variables
> ![image](https://user-images.githubusercontent.com/68887544/114529318-772e0000-9c67-11eb-83d0-b4cbfa8962ce.png)
> 

---
* Overlapping
> * ![image](https://user-images.githubusercontent.com/68887544/114528874-0555b680-9c67-11eb-826a-4f6afa7decd8.png)

---

* Minimization using K-map:
> * ![image](https://user-images.githubusercontent.com/68887544/114537797-3e465900-9c70-11eb-86da-b7c98f26df46.png)
 ---
 
 * Binary Equivalents of Decimal numbers.

>  Decimal | Binary
>  ---| ---
>  0|	0
>  1|	1
>  2	|10
>  3	|11
>  4|	100
>  5|	101
>  6|	110
>  7|	111
>  8	|1000
>  9	|1001
>  10	|1010
>  11	|1011
>  12	|1100
>  13	|1101
>  14	|1110
>  15	|1111
>  16	|10000
>  17	|10001
>  18	|10010
>  19	|10011
>  20	|10100
>  21	|10101
>  22	|10110
>  23	|10111
>  24	|11000
>  25	|11001
>  26	|11010
>  27	|11011
>  28	|11100
>  29	|11101
>  30	|11110
>  31	|11111
>  32	|100000
>  33	|100001
>  34	|100010
>  35	|100011
>  36	|100100
>  37	|100101
>  38	|100110
>  39	|100111
>  40	|101000
>  41	|101001
>  42	|101010
>  43	|101011
>  44	|101100
>  45	|101101
>  46	|101110
>  47	|101111
>  48	|110000
>  49	|110001
>  50	|110010

---
* Quine McCluskey Method : https://www.youtube.com/watch?v=l1jgq0R5EwQ
