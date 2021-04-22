# Unit IV - Light, Colour, Shading and Hidden Surfaces

## Syllabus: 
> * Colour modes:
>   * Properties of Light 
>   * CIE chromaticity Diagram
>   * RGB 
>   * HSV 
>   * CMY
> * Illumination Models:
>   * Ambient Light 
>   * Diffuse reflection 
>   * Specular Reflection
>   * and the Phong model 
>   * Combined diffuse and Specular reflections with multiple light sources
>   * warn model 
> * Shading Algorithms: 
>   * Halftone
>   * Gauraud 
>   * Phong Shading 
> * Hidden Surfaces:
>   * Introduction
>   * Back face detection and removal 
>   * Algorithms: 
>       * Depth Buffer (z)
>       * Depth sorts(Painter)
>       * Area Subdivision(Warnock) 

---
 
## Colour Models:

* Properties of Light:
> * Light is an electromagnetic wave. 
> * Rays having a wavelength between 400nm to 750 nm are visible.
> * Light interacts with the material in four different ways.
>   * Emission - An object can emit the Light
>   * Absorption - An object can absorb the light 
>   * Reflection - The light might bounce off the object
>   * Refraction/Transmission - Light might pass through the object.
> * Color of object depends on a mixture of  reflected frequency from the surface of the object. If the surface reflects lower frequency then object appears reddish. This dominant lower frequency decides the color and ultimately hue of the color.
> * How pure color should appear is decided by the saturation.
> * How bright the scene should appear is decided by the brightness.
> * Purity is proportional to saturation. When hue and saturation are collectively used to describe the color, it is called chromaticity.
> * Combination pairs of colors that produce neutral color like white in return is called as complementary colors. 
>   * Ex. 
>   * Red and Cyan
>   * Green and Magenta
>   * Blue and Yellow
> * Color gamut is the set of all the visible colors to the human eye. 
> * In computer system, red, green and blue colors are combined with various intensity to produce all the colors.
> * System supporting 24 bit per pixel can produce 17 million different colors using three basic colors red, green and blue.

---

* CIE Chromaticity Diagram:
> * Chromaticity diagram represents all the possible color that the human eye can perceive. 
> * ![image](https://user-images.githubusercontent.com/68887544/115704600-329e1500-a389-11eb-8ac7-04868ab3e19d.png)
> 
---

* Color Models:
> * Color model is a system to create a wide range of colors from small set of primary colors.
> * There are two types of Color modes:
>   * Additive
>   * Subtractive

---

* RGB Color Model:
> * It is an additive color model.
> * It adds red, green and blue to produce a wide range of colors.
> * Not suitable for image processing applications.
> * It is a device dependent color model.
> * Different devices reproduce the same RGB value differently.
> * We can define this color model as a unit cube with R, G, B as its three axes.
> * Zero intensity of all three component produce black color and full intensity of them produce the white color. 
> * An equal proportion of all three colors between zero to one produce grey shade (diagonal line joining origin and opposite cube corner.)
> * ![image](https://user-images.githubusercontent.com/68887544/115705761-8b21e200-a38a-11eb-8504-5d58f0b429a1.png)
> * When anyone component has a dominant intensity, the color is a hue of primary color, and when two components have the same dominant intensity, then the color is a hue of a secondary color. A secondary color is formed by the sum of two primary colors of equal intensity.
> * When primary and its complementary secondary color are added together, the result is white. 
>   * ex. the complement of red is cyan, the complement of green is magenta and the complement of green is yellow.
> * RGB is an additive color model and any color C can be obtained by addition of R, G and B.
>   *  C = RR + GG + BB 
> * ![image](https://user-images.githubusercontent.com/68887544/115706747-9c1f2300-a38b-11eb-9345-d8a42be58630.png)
> * ![image](https://user-images.githubusercontent.com/68887544/115706796-a80ae500-a38b-11eb-8de5-4c42573c4986.png)
> 
---

* HSV Color Model:
> * H, S and V stand for Hue, Saturation and Value, repectively.
> * Hue defines the color
> * Saturation defines the purity of color
> * Value defines the intensity.
> * RGB and CMY are defined over cubic space 
> * HSV is defined over hexagon or cone shape.

---

* CMY color model:
> * CMY color model is subtractive color model.
> * C - Cyan, M - Magenta, Y - Yellow 
> * ![image](https://user-images.githubusercontent.com/68887544/115707579-9a099400-a38c-11eb-8170-e2e83aa128e1.png)

---

* Difference between RGB and HSV color model:
> * ![image](https://user-images.githubusercontent.com/68887544/115707719-c32a2480-a38c-11eb-9bc2-6b227b60d29b.png)

---

## Illumination Model:

* Illumination Model:
> * Lighting models that are used to calculate intensity at every pixel in the scene is also known as Illumination model.
> * Light Source:
>   * Light emitting source 
>   * Surface that reflects light can also act as light source.

* Ambient Light:
> * Even if the object is not directly exposed to the light source, due to reflected rays from the other  surfaces, it would be still visible. Such light is called as ambient light.
> * Ambient light is constant for all the surfaces and it scatters equally in all direction.
> * Objects illuminated using ambient Illumination model appears as a monochromatic, silhouette, unless the polygon facets of objects are given different shades.
> * If we assume that the ambient light reflected from all surfaces are the same and in all directions, then the illumination model equation would be,
>   * ![image](https://user-images.githubusercontent.com/68887544/115738815-08f5e580-a3ab-11eb-9995-6858cda044f7.png)

---
* Diffuse  and Specular Reflection 
> * Diffuse Reflection:
>   * Equal reflection of light in all direction from surface is called as diffuse reflection.
>       * ![image](https://user-images.githubusercontent.com/68887544/115739345-799d0200-a3ab-11eb-816f-df529381e5cb.png)
> * Specular Reflection:
>   * Reflection in a particular direction only is know as specular reflection.
>   * ![image](https://user-images.githubusercontent.com/68887544/115739713-c5e84200-a3ab-11eb-9eb6-3ef0e81b238a.png)
> * ![image](https://user-images.githubusercontent.com/68887544/115739973-05169300-a3ac-11eb-951f-e1234d67ba10.png)
> * Ideal diffuse Reflector or  Lambertian reflectors:
>   * If diffuse reflection scattered from the surface is equal in all direction, independent of viewing directions, such surfaces are called ideal diffuse reflector or Lambertian reflectors, since the radiated light energy from any surface is governed by Lambert's cosine law.

---

* Specular Reflection and Phong Model:
> * Specular Reflection:
>   * Reflection in a particular direction only is know as specular reflection.
>   * ![image](https://user-images.githubusercontent.com/68887544/115739713-c5e84200-a3ab-11eb-9eb6-3ef0e81b238a.png)
> *  ![image](https://user-images.githubusercontent.com/68887544/115740749-c1705900-a3ac-11eb-8612-ec76294a2a1a.png)
> * ![image](https://user-images.githubusercontent.com/68887544/115740768-c8976700-a3ac-11eb-9666-ef9c27c6586f.png)

---
* Combined Diffuse and Specular Reflections with Multiple Light Sources:
> * ![image](https://user-images.githubusercontent.com/68887544/115740991-f8466f00-a3ac-11eb-954c-f57320377a40.png)
> * ![image](https://user-images.githubusercontent.com/68887544/115741023-ff6d7d00-a3ac-11eb-94c2-05f5c88568e9.png)

---

* Warn Model:
> * Warn model provides a way to model the studio light with varying intensity in different directions.
> * ![image](https://user-images.githubusercontent.com/68887544/115741336-46f40900-a3ad-11eb-9f81-9f0701d3807d.png)

---

## Shading Algorithms:
* Gauraud Shading:
> * Flat shading/Constant intensity shading: 
>   *  We get discontinuity in flat shading so we use gauraud shading.
> * Steps:
>   * Determine the average unit  normal vector at each polygon vertex.
>   * Apply illumination model to each polygon vertex to determine polygon vertex intensity.
>   * Linearly  interpolate the vertex intensities over the surface of polygon.
> * ![image](https://user-images.githubusercontent.com/68887544/115743304-2dec5780-a3af-11eb-8ab2-094af9272ff9.png)
> 
---

