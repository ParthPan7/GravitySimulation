# Gravity Simulation
**Objective** : Simulation an object free fall under influence of Gravity leveraging Graphics Library called OpenGL. However, one can use any 3D Library they prefer to simulate influence the gravity in a Physical World.


**How can we simulation be approached in 3D space given by openGL?** 

First of All, it's very crucial to imagine or visualize actual scenario which needs to be simulated.
Thereafter, modeling same scenarios from a mathematical perspective - on how that action is manipulating the 3D imaginary space afterall.

For instance, Freely falling object under influence of gravity decides to follow unidirectional motion in a negative/decreasing Y direction during each time frame confirming the conventional coordinate system of specific library/framework for rendering 3D graphics. Here in an openGL library/frameworkfollows right handed coordinate system (refer a Figure 1) per frame.



![right hand coordinate system](https://github.com/ParthPan7/GravitySimulation/blob/main/coordinate_systems_right_handed.png)

_Figure 1 : right handed coordinate system OpenGL [1]._



## **Application of Physics** ##

## What is known ?

The scenario of free fall considers no force acting on it, yet the gravity is the only force acting upon an object complying the principles of Newtonian Physics [2]. Therefore, it says that quantity of mass is almost eliminated or negligible or become a unit.

### F = ma  (using newton's law) 
Under a free fall mass, **m** is almost neligible **m = 1 kgs** and 
acceleration is always due to application of gravity so **a = g**.Therefore, **g** is a constant acceleration due to gravitational fields differing at every celestial objects or planets (for earth **g = 9.87 m/s^2** and for mars **g = 3.75 m/s^2**).  

We only know acceleration, **g** that would act on freely falling object under influence of gravity. Knowing acceleration velocity **v** could be derived at different time , **t** can be computed.

Integrating relation, _a = dv/dt_ yields first equation of motion _v = u + at_ where

_v_ = velocity of object to be computed (unknown ),

_u_ = known velocity at this point of time ( as this is IVP problem, initial value of _u_ is zero - moment when an object is actually released from any specific height).  

Substituting _g_ in _a_ : 
our desired equation becomes - _v = u + gt_ 

Also, using second equation of motion position of each point particles can be computed.

_s = s<sub>0</sub> + ut + (1/2)gt<sup>2</sup>_ 

where,

_s<sub>0</sub>_ = previous object's position

_u_ = known velocity at this point of time ( as this is IVP problem, initial value of _u_ is zero - moment when an object is actually released from any specific height).  

_t_ = delta time (difference in time frame)

_g_ = gravitational acceleration of any celestial object

_s_ = next relative position of object to be computed ( unknow )

**References:**

[1]https://learnopengl.com/Getting-started/Coordinate-Systems

[2]https://en.wikipedia.org/wiki/Free_fall 


