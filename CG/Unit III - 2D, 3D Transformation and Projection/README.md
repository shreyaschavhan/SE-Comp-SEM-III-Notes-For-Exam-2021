# Unit III : 2D, 3D Tranformation and Projection.

## 2D Tranformation:

* 2D Tranformation:
> * Repositioning and Resizing of an object is called as tranformation
> * Types of Tranformation:
> 	* Translation
> 	* Rotation
> 	* Scaling
> * Homogenious Co-odinates
> * Other Tranformation:
> 	* shearing 
> 	* Reflection


---

* Translation:
> * Translation is repositioning of an object in a straight line.
> * Derivation:
>	* ![image](https://user-images.githubusercontent.com/68887544/115364013-96390e80-a1e0-11eb-90e5-9b5ee3e5c0d8.png)
> * Example Numberical:
> 	*  ![image](https://user-images.githubusercontent.com/68887544/115364625-342cd900-a1e1-11eb-868c-122712a80682.png)

---

* Rotation:
> * Repositioning of an object in a circular path is called as Rotation.
> * Derivation:
> 	*  ![image](https://user-images.githubusercontent.com/68887544/115368302-93d8b380-a1e4-11eb-9e3c-7d4712651f27.png)
> 	* Matrix Representation:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115368805-13668280-a1e5-11eb-8a6c-380a146466e1.png)
> * If Anticlockwise, Rotation angle +ve
> * If Clockwise, Rotation angle -ve

---

* Scaling:
> * Zoom-In or Zoom-out of object is called as scaling
> * Scaling Factor:
> 	* scaling in x-direction : S<sub>x</sub>
> 	* scaling in y-direction : S<sub>y</sub>
> * Equation:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115370628-def3c600-a1e6-11eb-829c-f4835123a132.png)
> * Conditions:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115371255-6fcaa180-a1e7-11eb-8881-ae8a6616efa2.png)

---

* Homogenious Co-ordinates:
> * It derives the general matrix equation that covers all the equations by translation, rotation and scaling.
> * General Equation:
> 	*  ![image](https://user-images.githubusercontent.com/68887544/115372643-bec50680-a1e8-11eb-87e2-28cc673c199f.png)
> * HOmogeneous Co-ordinates (Row Major):
> 	* ![image](https://user-images.githubusercontent.com/68887544/115381574-52023a00-a1f1-11eb-9f36-d157b2233a06.png)

---

* Rotation About Arbitrary point:
> * Translate arbitrary point to origin.
> * Rotate at θ angle
> * Translate back at same arbitrary position.
> * ![image](https://user-images.githubusercontent.com/68887544/115510442-5d12a400-a29d-11eb-807f-229d74f76ccb.png)
> * Final Equation:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115510920-e9bd6200-a29d-11eb-83f8-3a5541ef5062.png)
> 

---

* Shear:
> * Slanting or tilting something is called as shear
> * types:
> 	* X - shear : Only X co-ordinate change, y is preserved
> 	* Y - shear : Only y co-ordinate change, X is preserved
> * X - Shear Equation:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115518819-3c028100-a2a6-11eb-9e16-b942724ef801.png)
> * Y - Shear Equation:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115518988-68b69880-a2a6-11eb-81d6-248f03e180d9.png)
>
> * Shearing relative to other reference line:
> 	* 

---

## 3D Tranformation:

* 3D
> * Dimension: defining a object in a physical spatial with minimum no. of co-ordinate is called as Dimension.
> * The number of ways in which we can move in a dimension is defined as no. of dimension.
> 	* 0D : We cannot move at all
>	* 1D : We can move in only one direction
> 	* 2D : We can move in two directions
> 	* 3D : We can move in all directions (3)

----

* 3D Translation:
> * 
