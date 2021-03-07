# homework-4
A homework about practicing object oriented programming

## Context

For this assignment you will practice object oriented programming by using the provided base class `Circle` to create a derived class called `Sphere`. **You do not need to edit circle.hpp and Circle.cpp**, these files are completed. **You will however need to edit main.cpp, to uncomment the code to test your newly created Sphere class**. You should take a look at the code for all of these files and try to understand what is going on. 
## Sphere.hpp

To begin creating the new Sphere class I recommend these attributes:

```
  float _volume;
  float _surface_area;
```

It does not have to be *exactly* that, but you do need an attribute to represent the volume of a Sphere, and an attribute to represent the surface area of a Sphere.

You must implement these constructors:

```
  Sphere();
  Sphere(float radius);
  Sphere(const Sphere &s);
```

Keep in mind that `Sphere` should inherit from `Circle`.

You should override the `set_radius` method from the `Circle` base class for `Sphere`, since volume and surface area are dependent on radius (similar to the lecture videos for `Cube` and `Pyramid`. You should also have methods to calculate `volume` and `surface area`. Again, these two methods should be similar to `Cube` and `Pyramid` classes in lecture. To learn more about the formulas used to calcuate the volume and surface area for a sphere, click [here](https://en.wikipedia.org/wiki/Sphere).

Make sure you have getters for `volume` and `surface area`. Additionally, **you must make sure that you have a public inheritence from Circle**. Then you must overload the `=` operator and the `<<` operator. These should look similar to `Circle`. As a twist, you must also overload the `*` operator but not for other Circles, but for a float. The prototype should look like this:

```
  Sphere operator*(float x);
```

When you overload this operator you must multiply `x` by the `radius` of the `Sphere` class. Remember to update `volume`, and `surface area`.

## Sphere.cpp
Of course when you implement the methods, make sure that the names of the methods are preceeded by '`Shapes::`'.

Lastly, you must create a Makefile to compile your code. **Do not upload your object code (.o files) or executables to your git!!!! Its bad practice and I will take points off your grade!**

## Rubric

|Requirement                                         |Score  |
|  :---:                                             | :---: |
|Completing the header file and prototypes           | 20%   |
|Creation of cpp files and implementation of methods | 30%   |
|Correct implementation of overloading operators     | 20%   |
|Creation of Makefile                                | 20%   |
|Clean and readable code                             | 10%   |
|Total                                               | 100%  |
