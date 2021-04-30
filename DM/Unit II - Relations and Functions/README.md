# Unit II - Relations and Funcitons

## &#10023; Syllabus:
> * Relations and their Properties
> * n-ary relations and their applications
> * Representing relations
> * Closures of relations
> * Equivalence relations
> * Partial orderings
> * Partitions
> * Hasse diagram
> * Lattices
> * Chains and Anti-chains
> * Transitive closure and Warshall's algorithm
> * Functions:
>   * Surjective
>   * Injective and Bijective functions >   * Identity function
>   * Partial function
>   * Invertible function
>   * constant function
>   * Inverse functions and compositions of functions
>   * The pigeonhole principle

---

## &#10023; Relations and Functions

* Relations and their properties
> * A relation R from set AxB & subset of AxB
> * R is subset of A x B
> * R<sub>max</sub> = A x B
> * R<sub>min</sub> = phi
> * ![image](https://user-images.githubusercontent.com/68887544/116503631-332c3380-a8d4-11eb-825f-35d7005e2095.png)
> * AXB != BXA ,i.e. it does not follow commutative property.
>

---

* Representation of Relations:
> * Relation as Matrix
>   * ![image](https://user-images.githubusercontent.com/68887544/116504103-3c69d000-a8d5-11eb-9def-8ef24bbf662b.png)
> * Relation as a directed graph (Digraph)
>   * ![image](https://user-images.githubusercontent.com/68887544/116504256-805cd500-a8d5-11eb-8cc3-6a15933ec1a0.png)
> * Relation as a Arrow Diagram
>   * ![image](https://user-images.githubusercontent.com/68887544/116504376-c0bc5300-a8d5-11eb-99d6-3fc74440c09b.png)
> * Relation as a table
>   * ![image](https://user-images.githubusercontent.com/68887544/116504515-1133b080-a8d6-11eb-82dd-7c719698f537.png)
>

---

* Binary Relations:
> * A binary relation R is defined to  be a subset of PxQ from set P to Q.
>   * ![image](https://user-images.githubusercontent.com/68887544/116504677-81423680-a8d6-11eb-85ab-9ef01e8d5d03.png)
>
---

* Domain of a Relation:
> * The first entry on ordered pair of R.
> * Dom(R) = {elements}
>   * ![image](https://user-images.githubusercontent.com/68887544/116504785-c8302c00-a8d6-11eb-9178-429c0daa07ce.png)
>   

---

* Range of a Relation:
> * It is the 2nd entry on the ordered pair in R.
> * Ran(R) = {a.b}
> * ![image](https://user-images.githubusercontent.com/68887544/116504883-104f4e80-a8d7-11eb-8310-278830aad97f.png)

---

* Complement of a Relation:
> * Represented by R<sup>'</sup> or R<sup>c</sup>
>   * ![image](https://user-images.githubusercontent.com/68887544/116507060-2b708d00-a8dc-11eb-903e-2ebeb2c85015.png)

---

* Inverse of Relation:
> * Denoted by R<sup>-1</sup>
> * ![image](https://user-images.githubusercontent.com/68887544/116507548-12b4a700-a8dd-11eb-8230-d1fc105f957d.png)

---

* Types of Relations:
> * Reflexive
> * Irreflexive
> * Symmetric Relation
> * Antisymmetric Relation
> * Asymmetric Relations
> * Transitive Relation
> * Equivalence relation
> * Partial order poset.

---

* Reflexive relation:
> * ![image](https://user-images.githubusercontent.com/68887544/116508038-1dbc0700-a8de-11eb-8636-be1b2d84d4a9.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116508101-42b07a00-a8de-11eb-8f6a-c9ab310eb099.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116508809-c3bc4100-a8df-11eb-8a05-a556d7461c53.png)

---

* Irreflexive Relation:
> * ![image](https://user-images.githubusercontent.com/68887544/116509168-78eef900-a8e0-11eb-92b0-c3be6182ab20.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116509329-b81d4a00-a8e0-11eb-8626-703e5b868bfc.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116509746-78a32d80-a8e1-11eb-8a81-8fdf9d59e706.png)

---

* Symmetric Relation:
> * ![image](https://user-images.githubusercontent.com/68887544/116514261-6973ae00-a8e8-11eb-8dfa-7f28a3ddcdd4.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116532090-81096180-a8fd-11eb-9b92-189408f23308.png)

---

* Anti Symmetric Relation:
> * ![image](https://user-images.githubusercontent.com/68887544/116656295-0cd8c780-a9aa-11eb-8710-a2b8ca199474.png)

---

* Asymmetric Relation:
> * ![image](https://user-images.githubusercontent.com/68887544/116656995-4c53e380-a9ab-11eb-9a2a-ea397734db17.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116657184-a18ff500-a9ab-11eb-9c61-4ac9b324a48e.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116657361-e61b9080-a9ab-11eb-849b-6e9e5572a713.png)

---

* Transitive Relation:
> * ![image](https://user-images.githubusercontent.com/68887544/116657991-ef592d00-a9ac-11eb-9ac9-d58df029f412.png)
> *  ![image](https://user-images.githubusercontent.com/68887544/116658656-ee74cb00-a9ad-11eb-89a8-7189968965f6.png)

---

* Equivalence Relation:
> * ![image](https://user-images.githubusercontent.com/68887544/116659886-e0c04500-a9af-11eb-85b1-5a139ccb0321.png)
> 
---

* Partial Order Relation:
> * ![image](https://user-images.githubusercontent.com/68887544/116660494-bde26080-a9b0-11eb-9cc3-96185268c103.png)

---

* Hasse Diagram:
> * ![image](https://user-images.githubusercontent.com/68887544/116674633-8977a000-a9c2-11eb-8d89-457b13aa30b0.png)
> * Remove Self Loop
>   * ![image](https://user-images.githubusercontent.com/68887544/116674788-b461f400-a9c2-11eb-9306-c012f0bf3a83.png)
> * Remove Transitive Lines:
>   * ![image](https://user-images.githubusercontent.com/68887544/116674987-eecb9100-a9c2-11eb-8441-81b59af3e3b8.png)
> * Remove Upward directions:
>   * ![image](https://user-images.githubusercontent.com/68887544/116675186-289c9780-a9c3-11eb-85fc-c2a323d1a970.png)
> * Simplified Hasse Diagram:
>   * ![image](https://user-images.githubusercontent.com/68887544/116675297-4d910a80-a9c3-11eb-85cb-8f94f4e9ede6.png)
> * Note: No downward relation.
> * ![image](https://user-images.githubusercontent.com/68887544/116677183-87631080-a9c5-11eb-8a22-fdb625afec8d.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116679052-ad89b000-a9c7-11eb-92ec-4b6c31912e87.png)
> 

---

* Maximal and minimal in Hasse Diagram:
> * ![image](https://user-images.githubusercontent.com/68887544/116684117-2ab82380-a9ce-11eb-9ef5-c1a2a97f07e6.png)

---

* Maximum and Minimum in Hasse Diagram:
> * ![image](https://user-images.githubusercontent.com/68887544/116685139-820ac380-a9cf-11eb-998d-c44595d12b4e.png)
---

* Upper bound and lower bound in hasse diagram:
> * ![image](https://user-images.githubusercontent.com/68887544/116685960-c34fa300-a9d0-11eb-96a5-78fce2c182ea.png)

---

* Greatest Lower bound and least upper bound in hasse diagram:
> * Q.no. 2. point fc wrong! Upper bound will be e, f and least upper bound will be f.
> * ![image](https://user-images.githubusercontent.com/68887544/116687107-49b8b480-a9d2-11eb-92c2-649a5bf8d143.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116687493-e7ac7f00-a9d2-11eb-8e46-1410d85d1d74.png)
> 
---

* Join Semi Lattice:
> * ![image](https://user-images.githubusercontent.com/68887544/116688561-82598d80-a9d4-11eb-8e60-3d139572d1dc.png)

---

* Meet semi lattice:
> * ![image](https://user-images.githubusercontent.com/68887544/116688958-1166a580-a9d5-11eb-94a6-f8d2acf9a827.png)

---

* Lattice:
> * ![image](https://user-images.githubusercontent.com/68887544/116689567-ed579400-a9d5-11eb-8c5b-91b137a45520.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116690337-de251600-a9d6-11eb-9779-a74a3fdb381c.png)
> 

---

* Sub Lattice:
> * ![image](https://user-images.githubusercontent.com/68887544/116691015-e0d43b00-a9d7-11eb-82e4-7dbc4f126030.png)


---

* Properties of Lattice:
> * ![image](https://user-images.githubusercontent.com/68887544/116691594-a1f2b500-a9d8-11eb-9c86-3889013e3b65.png)

---

* Upper bound and lower bound of a lattice:
> * ![image](https://user-images.githubusercontent.com/68887544/116691937-33fabd80-a9d9-11eb-8773-2bf0bde47430.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116692395-ec286600-a9d9-11eb-8d03-112be17e6e34.png)

---

* Complement of an element in Lattice:
> * ![image](https://user-images.githubusercontent.com/68887544/116692722-71137f80-a9da-11eb-8cef-d64b1ec252b1.png)
> * ![image](https://user-images.githubusercontent.com/68887544/116694442-eda75d80-a9dc-11eb-89c4-4482956d89d1.png)

---


 


