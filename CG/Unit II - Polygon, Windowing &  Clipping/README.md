# Unit II - Polygon, Windowing &  Clipping

* Polygon:
> * Defination: A figure or diagram drawing by joining more than two lines is called as polygon.
> * Types of polygons:
> * The classification of polygon is based on whre the line segment joining any two points within the polygon is going to lie.
> 	- Convex Polygon: Line segment joining two points inside the polygon. (Line angle is less than 180^0)
> 	- Concave polygon: Line segment joining two points outside the polygon. (at least one angle is more than 180^0 ) 
> 	- Complex polygon: Polygon with intersecting edges in called as complex polygon.

	
---

* Inside Test:
> * We do inside test to check if the given pixel is  inside the polygon or not.
> * Even - Odd Method:
> 	* Construct a line segment between the point in question & a known to be outside polygon.
> 	* Count t he intersection of line with polygon boundaries.
> 		* Inside : Odd no. of intersection
> 		* Outside: even no. of intersection
> 	* If intersection point in vertex: Then look at other end points of line segment.
> 		* If points are on same side of constructed line then "even no. of intersection" for only that intersection
> 		* If points are on different side of constructed  line " then odd no. of intersection" for only that intersection.
> 
> * Winding number Rule:
> 	* Initialize winding no = 0
> 	* If line crosses an edge directed bottom 
> 		* to top then add 1 to winding no.
> 		* to top-botoom add -1 to winding number
> 		* left to right right to left : no value
>	* Point outside if w.no = 0
> 	* otherwise Inside

---

* Polygon Filling:
> * We have two methods to fill polygon, 
> 	* 1. seed fill and 
> 	* 2. scan line algorithm
>

---

* Seed Fill:
> 	* We have two approaches:
>		* Flood fill algorithm
> 		* Boundary fill algorithm

---

* Boundary Fill Algorithm:
> * We can use boundary fill, where boundary of polygon is of same colour.
> 	* Two methods:
> 		* 4 Connected
> 		* 8 Connected
>	* 4 connected:
>		* Step I: It checks if pixel is already in the colour that we need as output.
>		* Step II: It checks if has same colour as boundary.
>		* If not you can fill
>		* Step III: Fill
>		* Ab boundary fill yeh kehta hai ki yeh khud toh dub gaya lekin apne passwale 4 ko leke bhi dubega.
> 		* 4 connected means, the 4 pixels around the selected pixel will be filled
> 		* (x,y) ---> (x+1, y), (x-1,y), (x, y+1), (x,y-1)
>                      *  ![image](https://user-images.githubusercontent.com/68887544/115138828-1da14900-a04c-11eb-9f01-fc69297bad79.png)
>	* 8 Connected:
>		* Same as 4-connected but also diagonal elements are considered.
> 		* ![image](https://user-images.githubusercontent.com/68887544/115139146-fe0b2000-a04d-11eb-8c7d-38eb453ccbdf.png)
>	* Algorithm:
>	* 4 Connected:
>		* ```
>			boundary_fill(x,y,fill_colour, boundary_colour){
>				if(getPixel(x,y)!=boundary_colour && getPixel(x,y)!=fill_colour){
>					putPixel(x,y, fill_colour){
>						boundary_fill(x+1, y,fill_colour, boundary_colour);
>						boundary_fill(x-1, y,fill_colour, boundary_colour);
>						boundary_fill(x, y+1,fill_colour, boundary_colour);
>						boundary_fill(x, y-1,fill_colour, boundary_colour);
>					}
>				}			
>			} 
>	
>
>	* 8 Connected:
>		* ```
>			boundary_fill(x,y,fill_colour, boundary_colour){
>				if(getPixel(x,y)!=boundary_colour && getPixel(x,y)!=fill_colour){
>					putPixel(x,y, fill_colour){
>						boundary_fill(x+1, y,fill_colour, boundary_colour);
>						boundary_fill(x-1, y,fill_colour, boundary_colour);
>						boundary_fill(x, y+1,fill_colour, boundary_colour);
>						boundary_fill(x, y-1,fill_colour, boundary_colour);
>						boundary_fill(x+1, y+1,fill_colour, boundary_colour);
>						boundary_fill(x+1, y-1,fill_colour, boundary_colour);
>						boundary_fill(x-1, y+1,fill_colour, boundary_colour);
>						boundary_fill(x-1, y-1,fill_colour, boundary_colour);
>					}
>				}			
>			} 
>		
>		
---
* Flood Fill Algorithm:
> * If boundary colour is different then we use  flood fill.
> * Same as boundary fill, 4 connected 8 connected
> * Algorithm:
>	* ```
> 		flood_fill(x,y, old_colour, new_colour){
>			if(getpixel(x,y)==old_colour){
>				putpixel(x,y,new_colour){
>					flood_fill(x+1, y, old_colour, new_colour);
>					flood_fill(x-1, y, old_colour, new_colour);
>					flood_fill(x, y+1, old_colour, new_colour);
>					flood_fill(x, y-1, old_colour, new_colour);
>
>				}
>			}
>		} ```
> * same for 8 connected
