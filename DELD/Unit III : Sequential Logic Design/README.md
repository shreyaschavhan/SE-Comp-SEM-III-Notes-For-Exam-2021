# Unit III: Sequential Logic Design

## &#10023; Syllabus:
> * Flip-Flop:
>   * SR
>   * JK
>   * D
>   * T
>   * Preset and Clear
>   * Master Slave JK Flip flops
>   * Truth Tables and Excitation tables
>   * Conversion from one type to another type of flip flop
> * Registers:
>   * SISO
>   * SIPO
>   * PISO
>   * PIPO
>   * Shift Registers
>   * Bidirectional Shift Register
>   * Ring counter
> * Universal Shift register counters:
>   * Asynchronous counter
>   * Synchronous counter
>   * BCD counter
>   * Johnson Counter
>   * Modulus of the counter (IC 7490)
> * Synchronous Sequential Circuit Design:
>   * Models - Moore and Mealy
>   * State Diagram and State Table
>   * Design Procedure
>   * Sequence Generator and detector.

---
## &#10023; Combinational V/s Sequential:
> ![image](https://user-images.githubusercontent.com/68887544/115987974-23aba280-a5d5-11eb-95c1-93935992b4a1.png)


## &#10023; Flip Flop

* **SR Flip Flop:**
> * Flip flops are single bit storage devices.
> * Set and Reset Flip flop
> * Logic Diagram:
>   * ![image](https://user-images.githubusercontent.com/68887544/115987575-37eea000-a5d3-11eb-8301-19afdb2f3ab7.png)
> * By using NAND gate
> * Truth Table:
>   * ![image](https://user-images.githubusercontent.com/68887544/115987829-5a34ed80-a5d4-11eb-945f-1d87cd254ca4.png)
>   * ![image](https://user-images.githubusercontent.com/68887544/115987872-98caa800-a5d4-11eb-9666-d3f9358bb867.png)
>
> * Equation For SR flip flop:
>   * ![image](https://user-images.githubusercontent.com/68887544/115989601-c287cd00-a5dc-11eb-990f-3ee57fc29d00.png)
>
---

* D Flip-Flop:
> * We can design using SR flip Flop
> * Logic Diagram:
>   * ![image](https://user-images.githubusercontent.com/68887544/115989664-07136880-a5dd-11eb-8871-dbd089b421a5.png)
> * Truth Table & cases:
>   * ![image](https://user-images.githubusercontent.com/68887544/115989790-b0f2f500-a5dd-11eb-8637-cdde98d117ed.png)
>   * Equation: ![image](https://user-images.githubusercontent.com/68887544/115989843-f3b4cd00-a5dd-11eb-897c-81c1619bb3d9.png)
>   * Also called as transparent flip flop.

---

* JK Flip Flop:
> * We are toggling SR to get JK
> * Logic Diagram:
>   * ![image](https://user-images.githubusercontent.com/68887544/115989898-4a220b80-a5de-11eb-93bc-3ed05ef69004.png)
> * Truth Table and Cases:
>   * ![image](https://user-images.githubusercontent.com/68887544/115990080-ff54c380-a5de-11eb-90b2-7c17fbfc6af4.png)

---

* T Flip Flop:
> * Toggle Flip flop 
> * You can join jk flip flop and use it as t flip flop 
> * Logic diagram:
>   * ![image](https://user-images.githubusercontent.com/68887544/115991116-a4be6600-a5e4-11eb-8a4b-123fb358234c.png)
> * Truth Table:
>   * ![image](https://user-images.githubusercontent.com/68887544/115991162-ec44f200-a5e4-11eb-8475-f80211b81422.png)
> * Equation of T-flip flop:
>   * ![image](https://user-images.githubusercontent.com/68887544/115991229-35954180-a5e5-11eb-8fff-d0af31eabdb7.png)
