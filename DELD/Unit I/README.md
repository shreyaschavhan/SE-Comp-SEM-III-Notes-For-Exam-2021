# Unit I : Minimization Technique

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
